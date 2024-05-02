---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les politiques de consentement
description: Découvrez comment utiliser les politiques de consentement d’Adobe Experience Platform.
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: politiques, gouvernance, platform, healthcare shield, consentement
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 72%

---

# Utiliser les politiques de consentement {#consent-management}

Vos données peuvent être soumises à des restrictions d’utilisation définies par votre organisation ou par des réglementations juridiques. Il est donc important de s’assurer que vos opérations de données dans Journey Optimizer sont conformes aux [politiques d’utilisation des données](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=fr){target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=fr#marketing-actions){target="_blank"} que vous avez le droit d’appliquer les données.

Les **politiques de consentement** constituent un type de politiques d’utilisation des données disponible. Elles vous permettent d’adopter et d’appliquer facilement des politiques marketing afin de respecter les préférences de consentement de vos clientes et clients. [En savoir plus sur l’application des politiques](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html?lang=fr){target="_blank"}

>[!IMPORTANT]
>
>Les politiques de consentement ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** et **Privacy and Security Shield**.

Par exemple, vous pouvez [créer des politiques de consentement](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=fr#consent-policy){target="_blank"} dans Experience Platform pour exclure les clientes et clients qui n’ont pas consenti à recevoir des communications par e-mail, notification push ou SMS.

* Pour les canaux sortants natifs (Email, Push, SMS, Courrier), la logique est la suivante :

   * Par défaut, si un profil s’est désabonné de la réception des communications de votre part, le profil correspondant est exclu des prochaines diffusions.

   * Si vous disposez de l’Adobe **Bouclier sanitaire** ou **Protection de la vie privée et protection**, vous pouvez créer une stratégie de consentement personnalisée qui remplace la logique par défaut. Par exemple, vous pouvez définir une stratégie pour envoyer uniquement des messages électroniques à toutes les personnes qui se sont inscrites. En l’absence de stratégie personnalisée, la stratégie par défaut s’applique.

  Pour appliquer une stratégie personnalisée, vous devez définir une action marketing dans cette stratégie et l’associer à une surface de canal. [En savoir plus](#surface-marketing-actions)

Au niveau du parcours, vous pouvez appliquer des politiques de consentement à vos actions personnalisées :

* Lors de la **configuration d’une action personnalisée**, vous pouvez définir un canal et une action marketing. [En savoir plus](#consent-custom-action)
* Lors de l’ajout de l’**action personnalisée dans un parcours**, vous pouvez définir une action marketing supplémentaire. [En savoir plus](#consent-journey)

## Utilisation des stratégies de consentement via les surfaces des canaux {#surface-marketing-actions}

Dans [!DNL Journey Optimizer], le consentement est géré par le [Schéma de consentement](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=fr){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=fr#choice-values){target="_blank"} d’Experience Platform.

Pour modifier la valeur du champ de consentement, vous pouvez créer une stratégie de consentement personnalisée dans laquelle vous définissez une action marketing et les conditions sous lesquelles cette action est effectuée. [En savoir plus sur les actions marketing](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=fr#marketing-actions){target="_blank"}

Par exemple, si vous souhaitez créer une stratégie de consentement pour cibler uniquement les profils ayant consenti à recevoir des communications par e-mail, procédez comme suit.

1. Assurez-vous que votre entreprise a acheté l’Adobe **Bouclier sanitaire** ou **Protection de la vie privée et protection** offres complémentaires. [En savoir plus](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=fr){target="_blank"}

1. Dans Adobe Experience Platform, créez une stratégie personnalisée (à partir du **[!UICONTROL Privacy]** > **[!UICONTROL Stratégies]** ). [Découvrez comment](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-policy){target="_blank"}

   <!--![](assets/consent-policy-create.png)-->

1. Choisissez la **[!UICONTROL Stratégie de consentement]** saisissez et configurez une condition comme suit. [Découvrez comment configurer les stratégies de consentement](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=fr#consent-policy){target="_blank"}

   1. Sous , **[!UICONTROL If]** , sélectionnez **[!UICONTROL Ciblage des emails]** action marketing par défaut.

      <!--![](assets/consent-policy-marketing-action.png)-->

      >[!NOTE]
      >
      >Les principales actions marketing proposées par Adobe sont répertoriées dans la section [ce tableau](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#core-actions){target="_blank"}. The steps to create a custom marketing action are listed in [this section](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-marketing-action){target="_blank"}.

   1. Sélectionnez ce qui se passe lorsque l’action marketing s’applique. Dans cet exemple, sélectionnez **[!UICONTROL Consentement du marketing par e-mail]**.

   ![](assets/consent-policy-then.png)

1. Enregistrez et [enable](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#enable){target="_blank"} cette politique.

1. Dans Journey Optimizer, créez une surface d&#39;email. [Voici comment procéder](../configuration/channel-surfaces.md#create-channel-surface)

1. Dans les détails de la surface de l&#39;email, sélectionnez le **[!UICONTROL Ciblage des emails]** action marketing.

   ![](assets/surface-marketing-action.png)

Toutes les stratégies de consentement associées à cette action marketing sont automatiquement exploitées afin de respecter les préférences de vos clients.

Dans cet exemple, toute [email](../email/create-email.md) l&#39;utilisation de cette surface dans une opération ou un parcours n&#39;est envoyée qu&#39;aux profils qui ont consenti à recevoir des emails de votre part. Les profils qui n’ont pas consenti à recevoir des communications par courrier électronique sont exclus.

## Utiliser des politiques de consentement par le biais d’actions personnalisées {#journey-custom-actions}

### Remarques importantes {#important-notes}

Dans Journey Optimizer, le consentement peut également être utilisé dans des actions personnalisées. Si vous souhaitez l’utiliser avec les fonctionnalités de message intégré, vous devez utiliser une activité de condition pour filtrer les clients dans votre parcours.

Avec la gestion du consentement, deux activités de parcours sont analysées :

* Lecture d’audience : l’audience récupérée est prise en compte.
* Action personnalisée : la gestion du consentement prend en compte les attributs utilisés ([paramètres d’action](../action/about-custom-action-configuration.md#define-the-message-parameters)) ainsi que la ou les actions marketing définies (action marketing requise et action marketing supplémentaire).
* Les attributs qui font partie d’un groupe de champs utilisant le schéma d’union prêt à l’emploi ne sont pas pris en charge. Ces attributs seront masqués dans l’interface. Vous devez créer un autre groupe de champs utilisant un autre schéma.
* Les politiques de consentement s’appliquent uniquement lorsqu’une action marketing (requise ou supplémentaire) est définie au niveau de l’action personnalisée.

Toutes les autres activités utilisées dans un parcours ne sont pas prises en compte. Si vous commencez votre parcours avec une qualification d’audience, l’audience n’est pas prise en compte.

Dans un parcours, si un profil est exclu par une politique de consentement dans une action personnalisée, le message ne lui est pas envoyé, mais il continue le parcours. Le profil n’atteint pas le chemin de délai d’expiration et erreur lors de l’utilisation d’une condition.

Avant d’actualiser les politiques dans une action personnalisée placée dans un parcours, assurez-vous que votre parcours ne comporte aucune erreur.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

### Configurer l’action personnalisée {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Définition d’une action marketing requise"
>abstract="L’action marketing requise vous permet de définir l’action marketing associée à votre action personnalisée. Par exemple, si vous utilisez cette action personnalisée pour envoyer des e-mails, vous pouvez sélectionner Ciblage des e-mails. Lorsqu’elles sont utilisées dans un parcours, toutes les politiques de consentement associées à cette action marketing sont récupérées et exploitées. Elle ne peut pas être modifiée dans la zone de travail."

Lors de la configuration d’une action personnalisée, deux champs peuvent être utilisés pour la gestion du consentement.

Le **Canal** vous permet de sélectionner le canal associé à cette action personnalisée : **E-mail**, **SMS** ou **Notification push**. Il préremplit le champ **Action marketing requise** avec l’action marketing par défaut pour le canal sélectionné. Si vous sélectionnez **Autre**, aucune action marketing n’est définie par défaut.

![](assets/consent1.png)

L’**Action marketing requise** vous permet de définir l’action marketing associée à votre action personnalisée. Par exemple, si vous utilisez cette action personnalisée pour envoyer des e-mails, vous pouvez sélectionner **Ciblage des e-mails**. Lorsqu’elles sont utilisées dans un parcours, toutes les politiques de consentement associées à cette action marketing sont récupérées et utilisées. Une action marketing par défaut est sélectionnée, mais vous pouvez cliquer sur la flèche vers le bas pour sélectionner n’importe quelle action marketing disponible dans la liste.

![](assets/consent2.png)

Pour certains types de communications importantes, par exemple un message transactionnel envoyé pour réinitialiser le mot de passe du client, vous pouvez ne pas appliquer de politique de consentement. Vous pouvez ensuite sélectionner **Aucune** dans le champ **Action marketing requise**.

Les autres étapes de configuration d’une action personnalisée sont présentées dans [cette section](../action/about-custom-action-configuration.md#consent-management).

### Création du parcours {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Action marketing requise"
>abstract="Une action marketing requise est définie lors de la création d’une action personnalisée. Cette action marketing requise ne peut pas être supprimée de l’action ou modifiée."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Action marketing supplémentaire"
>abstract="Ajoutez une autre action marketing en plus de celle requise. Les règles de consentement liées aux deux actions marketing seront appliquées."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualiser les politiques de consentement qui s’appliqueront au moment de l’exécution"
>abstract="Les actions marketing apportent des politiques de consentement qui combinent des paramètres d’action et des valeurs de consentement de profil individuel pour filtrer les utilisateurs. Obtenez la dernière définition de ces politiques en cliquant sur le bouton pour l’actualiser."

Lors de l’ajout de l’action personnalisée dans un parcours, plusieurs options vous permettent de gérer le consentement. Cliquez sur le bouton **Afficher les champs en lecture seule** pour afficher tous les paramètres.

Le **Canal** et l’**Action marketing requise**, définis lors de la configuration de l’action personnalisée, s’affichent en haut de l’écran. Vous ne pouvez pas modifier ces champs.

![](assets/consent4.png)

Vous pouvez définir une **Action marketing supplémentaire** pour définir le type d’action personnalisée. Vous pouvez ainsi définir l’objectif de l’action personnalisée dans ce parcours. Outre l’action marketing requise, généralement spécifique à un canal, vous pouvez définir une action marketing supplémentaire qui est spécifique à l’action personnalisée dans ce parcours particulier. Par exemple : une communication relative à un entraînement, une newsletter, une communication sur la condition physique, etc. L’action marketing requise et l’action marketing supplémentaire s’appliquent toutes deux.

![](assets/consent3.png)

Cliquez sur le bouton **Actualiser les politiques**, en bas de l’écran, pour mettre à jour et vérifier la liste des politiques prises en compte pour cette action personnalisée. Elle est fournie à titre d’information uniquement, lors de la création d’un parcours. Avec les parcours en direct, les politiques de consentement sont récupérées et mises à jour automatiquement toutes les 6 heures.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-audience.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Les autres étapes de configuration d’une action personnalisée dans un parcours sont présentées dans [cette section](../building-journeys/using-custom-actions.md).
