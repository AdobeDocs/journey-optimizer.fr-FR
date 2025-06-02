---
solution: Journey Optimizer
product: journey optimizer
title: Guide de dépannage pour les actions entrantes dans parcours
description: Découvrez comment déboguer et résoudre les problèmes liés aux actions entrantes dans parcours Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: actions entrantes, dépannage, parcours, débogage, aide autonome, vérification, erreurs
source-git-commit: 86b83f8b368a77ef96581c422f19f35d939e51f4
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 1%

---


# Résolution des problèmes liés aux actions entrantes dans parcours {#troubleshooting-inbound-actions}

Les actions entrantes, telles que les expériences in-app, web et basées sur du code, sont des composants essentiels de [!DNL Journey Optimizer], car elles permettent un engagement personnalisé avec les utilisateurs et utilisatrices pendant leur parcours. Cependant, un comportement inattendu, tel qu’un contenu entrant manquant ou une diffusion continue après la sortie d’un profil du parcours, peut se produire.

Ce guide fournit un processus détaillé pour déboguer les problèmes liés aux actions entrantes dans un parcours, afin de vous aider à les identifier et à les résoudre indépendamment avant de contacter l’assistance.

<!--This guide addresses the two most common scenarios with inbound actions in a journey. They are as follows:

* A profile enters the inbound step, but the user does not receive the expected inbound content.
* A user continues to receive inbound content even after the profile exits the journey.

## Benefits {#benefits}

- Faster issue resolution through self-help.
- Reduced dependency on support teams.
- Improved understanding of inbound action functionality.
- Enhanced customer experience and confidence in using AJO.-->

## Conditions préalables {#prerequisites}

Avant de commencer le dépannage, vérifiez les points suivants :

1. Configurez une session **Assurance**. Découvrez comment le faire dans la documentation d’[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

1. Accédez au parcours contenant l’action entrante pour récupérer le nom du parcours et l’ID de version.

   >[!NOTE]
   >
   >L’ID de version de parcours se trouve dans l’URL après *parcours/* (par exemple : *86232fb1-2932-4036-8198-55dfec606fd7*).

   ![](assets/troubleshoot-inbound-retrieve-journey-id.png)

1. Cliquez sur l’action entrante pour en afficher les détails. Récupérez le libellé et l’identifiant de l’action entrante.

   ![](assets/troubleshoot-inbound-retrieve-action-id.png)

1. Obtenez l’espace de noms et l’identifiant du profil pour identifier celui qui rencontre des problèmes. Selon votre configuration, l’espace de noms peut être ECID, e-mail ou ID client, par exemple. Découvrez comment rechercher un profil dans la documentation [Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/ui/user-guide#browse-identity){target="_blank"}.

## Scénario 1 : l’utilisateur n’a pas reçu le contenu entrant {#scenario-1}

Dans ce scénario, un profil a rejoint l’action entrante dans le parcours, mais même après 30 minutes, le contenu entrant correspondant ne s’affiche pas dans l’appareil/client à l’étape de déclenchement de la configuration.


### Pré-contrôles {#pre-checks}

1. **Le jeu de données entrant du Parcours est activé pour l’ingestion de profil**

   L&#39;action entrante utilise le jeu de données **Parcours entrant** pour les mises à jour de profil pendant l&#39;exécution. Assurez-vous que le jeu de données est activé pour les profils dans le sandbox actuel. [En savoir plus sur les jeux de données](../data/get-started-datasets.md)

2. Identité **&#39;joai&#39; définie dans les identités de la plateforme**

   L’action entrante utilise l’espace de noms **&#39;joai&#39;** dans le `segmentMembership` de profil pour activer le profil de l’étape entrante. Vérifiez qu’elle a été définie dans les identités de plateforme pour le sandbox. En savoir plus sur [Experience Platform Identity Service](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/home){target="_blank"}

### Étapes de débogage {#debugging-steps}

Le graphique ci-dessous montre la séquence des étapes de débogage que vous pouvez suivre :

![](assets/troubleshoot-inbound-scenario-1-steps.png){width="70%" align="center"}

### Étape 1 : vérifier si l’appareil/le client reçoit le contenu d’Edge Network {#step-1}

Commencez par vérifier si l’appareil ou le client obtient le contenu attendu.

>[!BEGINTABS]

>[!TAB Canal in-app]

1. Accédez à la session [Assurance](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"} et sélectionnez la section **[!UICONTROL Messagerie In-App]** dans le panneau de gauche.

1. Dans l’onglet **[!UICONTROL Messages sur l’appareil]**, cliquez sur la liste déroulante **[!UICONTROL Messages]** et recherchez un message avec le nom par parcours suivi de « - Message in-app ». Si présent, cela signifie que le message in-app est présent sur l’appareil/le client et que le problème peut être lié au déclencheur in-app.

1. Si le message est introuvable, le message in-app n’a pas été reçu par l’appareil/le client. Accédez à l’[étape suivante](#step-2) pour plus de débogage.

>[!TAB Canal web]

Rendez-vous sur la page et examinez l’onglet Mise en réseau , ou vérifiez la payload de réponse Edge dans la section **[!UICONTROL Edge Delivery]** de la session [Assurance](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!TAB Canal d’expérience basé sur le code]

Exécutez une requête curl à l’aide de l’API [Adobe](https://developer.adobe.com/data-collection-apis/docs/api/) et vérifiez la payload de réponse Edge dans la section **[!UICONTROL Edge Delivery]** de la session [Assurance](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!ENDTABS]

#### Étape 2 : vérifier si Edge Network renvoie le contenu {#step-2}

Cette étape permet de s’assurer que l’Edge Network renvoie le contenu entrant attendu pour le rendu sur l’appareil ou le client.

Lorsqu’un profil entre dans une action entrante dans un parcours, il est automatiquement qualifié en segment d’audience spécial (dans l’espace de noms **joai**) correspondant à l’action de parcours entrante.

Lorsqu’un client adresse une requête à Edge Network pour un profil et une surface donnés, le profil est éligible pour recevoir du contenu pour les actions de parcours entrant ciblant cette surface uniquement si le profil est actuellement membre du segment **joai** correspondant.

Pour déboguer le comportement d’Edge Network, procédez comme suit.

1. Ouvrez la vue **[!UICONTROL Edge Delivery]** dans la session Assurance. Cette vue fournit des informations sur l’exécution de l’action entrante sur le serveur Edge Network. Pour en savoir plus, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.

   <!--![](assets/troubleshoot-inbound-scenario-1-edge-delivery.png)-->

1. Vérifiez si l’activité Edge correspondant à l’action entrante est répertoriée dans les sections **[!UICONTROL Activités qualifiées]** ou **[!UICONTROL Activités non qualifiées]** :

   * Si, dans la section **Activités qualifiées**, le profil est qualifié pour l’action de parcours entrante, et le contenu doit être renvoyé.
   * Si dans la section **Activités non qualifiées** le profil n’était pas qualifié pour l’action de parcours entrante. Pour plus d’informations, consultez les raisons d’exclusion .
   * Si dans **aucune section**, soit un problème est survenu lors de la publication de l’action de parcours entrante dans Edge Network, soit l’URI de surface demandé ne correspondait pas aux paramètres de configuration du canal pour l’action entrante.

   >[!NOTE]
   >
   >Pour rechercher votre activité Edge dans la session **Assurance**, recherchez l’activité où **[!UICONTROL audienceNamespace]** est **joai** et **[!UICONTROL audienceSegmentId]** est `<JourneyVersionID>_<JourneyAction ID>` (par exemple : *86232fb1-2932-4036-8198-55dfec606fd7_708f718d-8503-4427-ad8d-8e28979b554c*).

1. Si votre activité se trouve dans la section **[!UICONTROL Activités non qualifiées]** et que la raison de l’exclusion est *’le segment n’est pas actif’*, cela signifie que le serveur de diffusion Edge Network ne pense pas que le profil fait partie du segment d’audience **joai** approprié.

   Vous pouvez vérifier si le segment **joai** est présent dans la vue du profil du serveur de diffusion Edge Network en ouvrant l’élément **segmentsMap** de la section Profil et en recherchant la présence de l’identifiant de segment **joai**.

1. Si le serveur de diffusion d’Edge Network ne voit pas le profil comme se trouvant dans le segment **joai** approprié, passez à l’étape suivante.<!--use the Platform Profile viewer UI to check if the expected **joai** segment is in a realized state in the Edge profile. Learn more in the [Experience Platform Profile UI documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/ui/user-guide){target="_blank"}-->

#### Étape 3 : vérifier si l’appartenance à l’audience joai s’est propagée à Edge Network {#step-3}

Cette étape permet de vérifier que le profil Edge a été correctement mis à jour lorsque le profil a rejoint l’action de parcours entrant et qu’il a été qualifié dans le segment **joai** correspondant.

Lorsqu’un profil est qualifié dans un segment **joai**, il est d’abord mis à jour sur le Hub, puis l’appartenance au segment est projetée au profil Edge pour être utilisé par le serveur de diffusion Edge Network.

>[!NOTE]
>
>La propagation de Hub vers Edge peut prendre jusqu’à 15 à 30 minutes à partir du moment où le profil est mis à jour sur le Hub.

Pour vérifier la présence du segment **joai** dans l’attribut `segmentMembership` du profil Edge, procédez comme suit.

1. Accédez au menu **[!UICONTROL Client]** > **[!UICONTROL Profils]** dans le volet de navigation de gauche [!DNL Journey Optimizer] et accédez au profil à l’aide de l’espace de noms et de l’identifiant. En savoir plus sur [Real-time Customer Profiles](../audience/get-started-profiles.md)

1. Sélectionnez l’onglet **[!UICONTROL Attributs]** et choisissez la vue **[!UICONTROL Edge]**.
   <!--cannot see Hub/Edge wiews for the profile-->

1. Cliquez sur **[!UICONTROL Affichage JSON]** pour ouvrir l’affichage JSON du profil.

   ![](assets/troubleshoot-inbound-profile-view-json.png)

1. Accédez à l’attribut **[!UICONTROL segmentMembership]** et vérifiez si le `<JourneyVersionID>_<ActionID>` d’identifiant du segment est présent dans l’espace de noms **joai** et s’il est à l’état **[!UICONTROL réalisé]** <!--or existing?-->.

   ![](assets/troubleshoot-inbound-profile-json-realized.png)

   * S’il est présent, cela signifie que le segment **joai** correspondant à l’action de parcours entrante a été correctement propagé au profil Edge.

   * S&#39;il n&#39;est pas affiché dans la vue du profil du serveur de diffusion Edge Network, il peut y avoir un problème lié à la manière dont le serveur de diffusion charge le profil Edge.

1. Si l’identifiant de segment **joai** n’est pas présent ou s’il est à l’état **[!UICONTROL sorti]**, cela signifie qu’il n’a pas (encore) été propagé vers Edge.

   Patientez 15 à 30 minutes pour que les valeurs `segmentMembership` soient propagées du Hub vers Edge. S’il n’est toujours pas présent, passez à l’étape suivante.

<!--The next step is to check whether the audience segment is present in the profile on the Hub.-->

#### Étape 4 : vérifier si l’appartenance à l’audience joai est présente dans le profil sur le Hub {#step-4}

Cette étape permet de s’assurer que le profil Hub a été correctement mis à jour lorsque le profil a rejoint l’action de parcours entrant et qu’il a été qualifié dans le segment **joai** correspondant.

>[!NOTE]
>
>L’ingestion de l’appartenance au segment **joai** dans le profil Hub peut prendre jusqu’à 15 à 30 minutes à partir du moment où le profil a rejoint l’action de parcours entrant.

Pour vérifier la présence du segment **joai** dans l’attribut `segmentMembership` du profil Hub, procédez comme suit.

1. Accédez au menu **[!UICONTROL Client]** > **[!UICONTROL Profils]** dans le volet de navigation de gauche [!DNL Journey Optimizer] et accédez au profil à l’aide de l’espace de noms et de l’identifiant. En savoir plus sur [Real-time Customer Profiles](../audience/get-started-profiles.md)

1. Sélectionnez l’onglet **[!UICONTROL Attributs]** et choisissez la vue **[!UICONTROL Hub]**. <!--cannot see Hub/Edge wiews for the profile-->

1. Cliquez sur **[!UICONTROL Affichage JSON]** pour ouvrir l’affichage JSON du profil.

1. Accédez à l’attribut **[!UICONTROL segmentMembership]** et vérifiez si le `<JourneyVersionID>_<ActionID>` d’identifiant du segment est présent dans l’espace de noms **joai** et s’il est à l’état **[!UICONTROL réalisé]** <!--or existing?-->.

   * S’il est présent, cela signifie que le segment **joai** correspondant à l’action de parcours entrante a été correctement ingéré dans le profil Hub.

   * S’il n’a pas été trouvé dans le profil Edge après au moins 30 minutes, un problème peut se produire avec le système de projection d’Edge.

1. Si l’identifiant de segment **joai** n’est pas présent ou s’il est à l’état **[!UICONTROL sorti]**, cela signifie que le profil n’était pas (encore) correctement qualifié dans le segment d’audience spécial **joai** lors de la saisie de l’action de parcours entrant correspondante.

   Patientez 15 à 30 minutes pour que les valeurs `segmentMembership` soient ingérées dans le profil sur le Hub. S’il n’est toujours pas présent, passez à l’étape suivante.

#### Étape 5 : si le client/appareil n’obtient toujours pas le contenu attendu {#step-5}

Si vous avez suivi toutes les étapes ci-dessus et que vous ne constatez pas le comportement attendu après avoir attendu 30 à 60 minutes que l’appartenance à un segment se propage vers Edge Network, contactez l’assistance clientèle d’Adobe ou votre représentant Adobe.

Incluez autant de détails que possible à partir des étapes de débogage, tels que :

* l’étape où vous constatez le comportement inattendu ;
* l’identifiant de version du parcours ;
* l’identifiant de l’action de parcours ;
* la trace Assurance complète ;
* la vue JSON du profil Edge ;
* la vue JSON du profil Hub ;
* etc.

## Scénario 2 : l’utilisateur reçoit toujours le contenu entrant même après que le profil a quitté le parcours {#scenario-2}

Ce scénario est l’inverse du [scénario 1](#scenario-1). Lorsqu’un profil quitte un parcours, il ne devrait plus être qualifié pour les segments d’audience **joai** correspondant aux actions entrantes dans le parcours.

Suivez les mêmes étapes de débogage que pour [Scénario 1](#debugging-steps) pour vérifier si le profil Hub, le profil Edge et le serveur de diffusion Edge Network reflètent correctement le statut d’appartenance au segment **joai** approprié et si le client ne reçoit plus le contenu entrant.

<!--
## Additional Notes {#additional-notes}

- **Propagation Time:** Segment membership updates can take up to 15-30 minutes to propagate from the Hub to the Edge Network.
- **Support:** If issues persist after following the steps, open a support ticket with details such as:
  - Journey Version ID and Journey Action ID.
  - Assurance trace.
  - JSON views of Edge and Hub profiles.
  - Debugging observations.

## Reference Section {#reference-section}

- [Assurance Setup Guide](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/tutorials/using-assurance)
- [Adobe Experience Platform Documentation](https://experienceleague.adobe.com/docs/experience-platform/home.html)
- [Streaming Ingestion APIs Troubleshooting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=fr)

## Warnings and Notes {#warnings-and-notes}

> **Warning:** Ensure the `joai` namespace is correctly configured in Platform Identities. Misconfiguration can lead to qualification issues for inbound actions.

> **Note:** Segment membership updates may take up to 30 minutes to propagate. Plan debugging sessions accordingly.

## Cross-References {#cross-references}

- [Testing the Journey](../building-journeys/testing-the-journey.md)
- [Using the Journey Designer](../building-journeys/using-the-journey-designer.md#paths)
- [Troubleshooting Custom Actions](../action/troubleshoot-custom-action.md)
-->