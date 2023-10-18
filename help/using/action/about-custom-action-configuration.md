---
solution: Journey Optimizer
product: journey optimizer
title: Configurer une action personnalisée
description: Découvrez comment configurer une action personnalisée
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, tiers, personnalisé, parcours, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1278'
ht-degree: 96%

---

# Configurer une action personnalisée {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Actions personnalisées "
>abstract="Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, utilisez des actions personnalisées pour configurer la connexion de ce système aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/), Firebase, etc."

Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, utilisez des actions personnalisées pour configurer la connexion de ce système aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target="_blank"}, Firebase, etc.

Les actions personnalisées sont des actions supplémentaires définies par les utilisateurs techniques et mises à la disposition des spécialistes marketing. Une fois configurés, elles apparaissent dans la palette gauche de votre parcours, dans la catégorie **[!UICONTROL Action]**. En savoir plus sur [cette page](../building-journeys/about-journey-activities.md#action-activities).

## Limites{#custom-actions-limitations}

Les actions personnalisées sont assorties de quelques limites répertoriées dans [cette page](../start/guardrails.md).

Dans les paramètres d’action personnalisés, vous pouvez transmettre une collection simple, ainsi qu’une collection d’objets. En savoir plus au sujet de ces limites de collection sur [cette page](../building-journeys/collections.md#limitations).

Notez également qu’un format spécifique est attendu pour les paramètres d’action personnalisés (par exemple : chaîne, décimal, etc.). Vous devez veiller au respect de cette exigence. En savoir plus sur ce [cas d’utilisation](../building-journeys/collections.md).

## Bonnes pratiques{#custom-action-enhancements-best-practices}

Une limite de limitation de 150 000 appels de plus de 30 secondes est définie pour toutes les actions personnalisées. Cette limite a été définie en fonction de l’utilisation de la clientèle, afin de protéger les points d’entrée externes ciblés par des actions personnalisées. Vous devez prendre cela en compte dans vos parcours basés sur l’audience en définissant un taux de lecture approprié (5 000 profils/s lors de l’utilisation d’actions personnalisées). Si nécessaire, vous pouvez remplacer ce paramètre en définissant une limitation ou un ralentissement plus élevé via nos API de limitation/ralentissement. Consultez [cette page](../configuration/external-systems.md).

Vous ne devez pas cibler les points d’entrée publics avec des actions personnalisées pour diverses raisons :

* Sans limitation ou ralentissement approprié, il existe un risque d’envoyer trop d’appels à un point d’entrée public qui ne prend pas en charge un tel volume.
* Les données de profil peuvent être envoyées par le biais d’actions personnalisées, de sorte que le ciblage d’un point d’entrée public peut entraîner le partage accidentel d’informations personnelles en externe.
* Vous n’avez aucun contrôle sur les données renvoyées par les points d’entrée publics. Si un point d’entrée modifie son API ou commence à envoyer des informations incorrectes, celles-ci seront rendues disponibles dans les communications envoyées, avec des impacts négatifs potentiels.

## Consentement et gouvernance des données {#privacy}

Dans Journey Optimizer, vous pouvez appliquer des politiques de gouvernance des données et de consentement à vos actions personnalisées, afin d’empêcher l’exportation de champs spécifiques vers des systèmes tiers ou d’exclure les clients qui n’ont pas consenti à recevoir des communications par e-mail, push ou SMS. Pour plus d’informations, consultez les pages suivantes :

* [Gouvernance des données](../action/action-privacy.md).
* [Consentement](../action/action-privacy.md).


## Étapes de configuration {#configuration-steps}

Les principales étapes nécessaires pour configurer une action personnalisée sont les suivantes :

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**. Dans la section **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Gérer]**. Cliquez sur **[!UICONTROL Créer une action]** pour créer une nouvelle action. Le volet de configuration des actions s&#39;ouvre dans la droite de l&#39;écran.

   ![](assets/custom2.png)

1. Saisissez le nom de l&#39;action.

   >[!NOTE]
   >
   >N&#39;utilisez ni espaces ni caractères spéciaux. Utilisez 30 caractères au maximum.

1. Ajoutez une description à l&#39;action. Cette étape est facultative.
1. Le nombre de parcours qui font appel à cette action apparaît dans le champ **[!UICONTROL Utilisé(e) dans]**. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours utilisant cette action.
1. Définissez les différents paramètres de **[!UICONTROL Configuration d&#39;URL]**. Voir [cette page](../action/about-custom-action-configuration.md#url-configuration).
1. Configurez la section **[!UICONTROL Authentification]**. Cette configuration est la même que pour les sources de données.  Consultez [cette section](../datasource/external-data-sources.md#custom-authentication-mode).
1. Définissez les **[!UICONTROL paramètres d&#39;action]**. Voir [cette page](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   L&#39;action personnalisée est maintenant configurée et prête à être utilisée dans vos parcours. Voir [cette page](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Lorsqu&#39;une action personnalisée est utilisée dans un parcours, la plupart des paramètres sont en lecture seule. Vous ne pouvez modifier que les champs **[!UICONTROL Nom]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** et la section **[!UICONTROL Authentification.]**

## Configuration du point d’entrée {#url-configuration}

Lors de la configuration d’une action personnalisée, vous devez définir les paramètres de **[!UICONTROL configuration de point d’entrée]** suivants :

![](assets/action-response1bis.png){width="70%" align="left"}

1. Dans le champ **[!UICONTROL URL]**, spécifiez l&#39;URL du service externe :

   * Si l’URL est statique, saisissez l’URL dans ce champ.

   * Si l’URL comprend un chemin dynamique, saisissez uniquement la partie statique de l’URL, c’est-à-dire le schéma, l’hôte, le port et, éventuellement, une partie statique du chemin.

     Exemple : `https://xxx.yyy.com/somethingstatic/`

     Vous spécifiez le chemin dynamique de l’URL lors de l’ajout de l’action personnalisée à un parcours. [En savoir plus](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Pour des raisons de sécurité, nous vous recommandons vivement d’utiliser le schéma HTTPS pour l’URL. L&#39;utilisation des adresses Adobe qui ne sont pas publiques et des adresses IP n&#39;est pas autorisée.
   >
   >Seuls les ports par défaut sont autorisés lors de la définition d’une action personnalisée : 80 pour http et 443 pour https.

1. Sélectionnez la **[!UICONTROL Méthode]** d’appel : il peut s’agir de **[!UICONTROL POST]**, **[!UICONTROL GET]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > Le méthode **DELETE** n’est pas prise en charge. Si vous devez mettre à jour une ressource existante, sélectionnez la méthode **PUT**.

1. Définissez les en-têtes et les paramètres de requête :

   * Dans la section **[!UICONTROL En-têtes]**, cliquez sur **[!UICONTROL Ajouter un champ d’en-tête]** pour définir les en-têtes HTTP du message de requête à envoyer au service externe. Les champs d’en-tête **[!UICONTROL Type de contenu]** et **[!UICONTROL CharSet]** sont définis par défaut. Vous ne pouvez pas modifier ni supprimer ces champs.

   * Dans la section **[!UICONTROL Paramètres de requête]**, cliquez sur **[!UICONTROL Ajouter un champ de paramètre de requête]** pour définir les paramètres à ajouter à l’URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Saisissez le libellé ou le nom du champ.

1. Sélectionnez le type : **[!UICONTROL Constant]** ou **[!UICONTROL Variable]**. Si vous avez sélectionné **[!UICONTROL Constant]**, saisissez la valeur constante dans le champ **[!UICONTROL Valeur]**. Si vous avez sélectionné **[!UICONTROL Variable]**, vous spécifiez cette variable lors de l’ajout de l’action personnalisée à un parcours. [En savoir plus](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Après avoir ajouté l’action personnalisée à un parcours, vous pouvez toujours y ajouter des champs d’en-tête si le parcours a le statut de brouillon. Si vous ne souhaitez pas que le parcours soit affecté par les modifications de configuration, dupliquez l’action personnalisée et ajoutez les champs d’en-tête à la nouvelle action personnalisée.
   >
   >Les en-têtes sont validés conformément à des règles d’analyse. En savoir plus dans [cette documentation](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Définir les paramètres de payload {#define-the-message-parameters}

1. Dans la section **[!UICONTROL Requête]**, collez un exemple de payload JSON à envoyer au service externe. Ce champ est facultatif et disponible uniquement pour les méthodes d’appel POST et PUT.

1. Dans la section **[!UICONTROL Réponse]**, collez un exemple de payload renvoyée par l’appel. Ce champ est facultatif et disponible pour toutes les méthodes d’appel. Pour plus d’informations sur l’utilisation des réponses d’appel API dans les actions personnalisées, reportez-vous à la section [cette page](../action/action-response.md).

>[!NOTE]
>
>La fonctionnalité de réponse est actuellement disponible en version Beta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>L’exemple de payload ne peut pas contenir de valeurs nulles. Les noms de champ de la payload ne peuvent pas contenir de caractère &quot;.&quot; . Ils ne peuvent pas commencer par le caractère &quot;$&quot;.

Vous aurez la possibilité de définir le type de paramètre (par exemple : string, integer, etc.).

Vous pourrez également préciser si le paramètre est une constante ou une variable :

* Le paramètre « **Constant** » signifie que la valeur du paramètre est définie dans le volet de configuration des actions par une persona ayant un rôle technique. La valeur reste identique dans tous les parcours Elle ne varie pas et le marketeur ne la voit pas lors de l’utilisation de l’action personnalisée dans le parcours. Il peut s&#39;agir, par exemple, d&#39;un identifiant attendu par le système tiers. Dans ce cas, le champ situé à droite du bouton bascule Constante/Variable correspond à la valeur transmise.
* Le paramètre « **Variable** » signifie que la valeur du paramètre varie. Le spécialiste marketing qui utilise cette action personnalisée dans un parcours sera libre de transmettre la valeur de son choix ou bien d’indiquer où récupérer la valeur de ce paramètre (à partir de l’événement, d‘Adobe Experience Platform, etc.). Dans ce cas, le champ situé à droite du bouton bascule Constante/Variable correspond au libellé que le spécialiste marketing voit dans le parcours pour nommer ce paramètre.

![](assets/customactionpayloadmessage2.png)