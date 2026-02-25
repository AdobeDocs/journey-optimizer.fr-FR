---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des activités de parcours
description: Prise en main des activités de parcours
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: parcours, activités, commencer, événements, action
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
version: Journey Orchestration
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 72%

---

# Prise en main des activités de parcours {#about-journey-activities}

Combinez des activités d’événement, d’orchestration et d’action afin de créer des scénarios cross-canal à plusieurs étapes.

## Activités d’événement {#event-activities}

Les parcours personnalisés commencent par des événements tels qu’un achat en ligne. Une fois qu’un profil entre dans un parcours, il le parcourt tout seul. Chaque profil peut suivre un chemin et un rythme différents. Lorsque vous commencez avec un événement, le parcours se déclenche lorsque l’événement arrive. Chaque profil suit ensuite les étapes définies dans votre parcours.

Les événements configurés par l’utilisateur ou l’utilisatrice technique (voir [cette page](../event/about-events.md)) apparaissent dans la première catégorie de la palette. Cette catégorie se trouve dans la partie gauche de l&#39;écran. Les activités d’événement suivantes sont disponibles :

* [Événements généraux](../building-journeys/general-events.md)
* [Réaction](../building-journeys/reaction-events.md)
* [Qualification d’audience](../building-journeys/audience-qualification-events.md)

![Palette des activités d’événement dans le concepteur de parcours](assets/journey43.png)

Pour démarrer votre parcours, faites glisser et déposez une activité d’événement. Vous pouvez également double-cliquer sur celle-ci.

![Glisser-déposer d’une activité d’événement dans le concepteur de parcours](assets/journey44.png)

## Activités d’orchestration {#orchestration-activities}

Les activités d’orchestration sont des conditions qui permettent de déterminer l’étape suivante du parcours. Ces conditions peuvent inclure le fait que la personne ait un dossier d’assistance ouvert ou qu’elle ait effectué un achat. Ils peuvent également inclure les prévisions météorologiques locales ou indiquer si la personne a atteint 10 000 points de fidélité.

Les activités d’orchestration ci-dessous sont disponibles dans la palette située dans la partie gauche de l’écran :

* [Optimiser](optimize.md)
* [Lecture d’audience](read-audience.md)
* [Attente](wait-activity.md)
* [Décision de contenu](content-decision.md)
* [Recherche de jeu de données](dataset-lookup.md)

![Palette des activités d’orchestration dans le concepteur de parcours](assets/journey-orchestration-activities.png)

## Activités d’action {#action-activities}

Les actions sont ce que vous souhaitez qu’il se produise à la suite d’un déclencheur, comme l’envoi d’un message. Il s’agit de l’élément du parcours que le client ou la cliente rencontre.

La catégorie **[!UICONTROL Actions]** se trouve dans la palette située dans la partie gauche de l’écran, sous **[!UICONTROL Événements]** et **[!UICONTROL Orchestration]**. Les activités d’action suivantes sont disponibles :

* [Actions de canal intégrées](../building-journeys/journey-action.md) disponible à partir de l’activité **Action**
* [Actions personnalisées](../building-journeys/using-custom-actions.md)
* [Saut](../building-journeys/jump.md)

![Palette des activités d’action dans le concepteur de parcours](assets/journey58.png)

Ces activités représentent les différents canaux de communication disponibles. Vous pouvez les combiner pour créer un scénario cross-canal.

Vous pouvez également configurer des actions spécifiques pour envoyer des messages :

* Si vous utilisez un système tiers pour envoyer des messages, vous pouvez créer une action personnalisée spécifique. [En savoir plus](../action/action.md)

* Si vous utilisez [!DNL Adobe Campaign] et [!DNL Adobe Journey Optimizer], reportez-vous aux sections suivantes :

   * [[!DNL Adobe Journey Optimizer] et [!DNL Adobe Campaign] v7/v8](../action/acc-action.md)
   * [[!DNL Adobe Journey Optimizer] et  [!DNL Adobe Campaign]  Standard](../action/acs-action.md)
   * [[!DNL Adobe Journey Optimizer] et  [!DNL Adobe Marketo Engage]](../action/marketo-engage.md)

## Bonnes pratiques {#best-practices}

Utilisez ces recommandations pour que les parcours soient lisibles, cohérents et faciles à résoudre.

### Ajouter un libellé

La plupart des activités vous permettent de définir un **[!UICONTROL libellé]**. Un suffixe est alors ajouté au nom qui apparaît sous votre activité dans la zone de travail. Cela s’avère utile si vous utilisez plusieurs fois la même activité dans votre parcours et souhaitez faciliter son identification. Cela facilite également le débogage en cas d’erreurs et rend les rapports plus lisibles. Vous pouvez, en outre, ajouter une **[!UICONTROL description]** facultative.

![Champs Libellé et Description dans les propriétés de l’activité de parcours](assets/journey-action-label.png)

>[!NOTE]
>
>Pour certaines activités, leur identifiant est également visible dans le volet. Cet identifiant peut être utilisé dans les rapports sous la forme d’une clé plus stable que le libellé, qui peut changer.

### Gérer les paramètres avancés {#advanced-parameters}

La plupart des activités affichent un certain nombre de paramètres avancés et/ou techniques que vous ne pouvez pas modifier.

![Champs de paramètres avancés dans les propriétés de l’activité de parcours](assets/journey-advanced-parameters.png)

Pour une meilleure lisibilité, masquez ces paramètres à l’aide du bouton **[!UICONTROL Masquer les champs en lecture seule]** situé en haut du volet de droite.

![Icône Masquer les champs en lecture seule dans les propriétés de l’activité de parcours](assets/journey-hide-read-only-fields.png)

Dans certains contextes précis, vous pouvez remplacer les valeurs de ces paramètres pour une utilisation spécifique. Pour forcer une valeur, cliquez sur l’icône **[!UICONTROL Activer le remplacement du paramètre]** à droite du champ. [En savoir plus](../configuration/primary-email-addresses.md#override-execution-address-journey)

![Option Activer la substitution de paramètre dans les propriétés de l’activité E-mail](assets/journey-enable-parameter-override.png)

>[!NOTE]
>
>Si les paramètres avancés sont masqués, cliquez sur le bouton **[!UICONTROL Afficher les champs en lecture seule]**.
>
>![Icône Masquer les champs en lecture seule dans les propriétés de l’activité de parcours](assets/journey-show-read-only-fields.png){width=60%}

### Ajouter un chemin d’accès alternatif

Lorsqu’une erreur se produit dans une action ou une condition, le parcours d’une personne s’arrête. La seule façon de le faire continuer est de cocher la case **[!UICONTROL Ajouter un chemin alternatif en cas de temporisation ou d’erreur]**. Consultez [cette section](../building-journeys/using-the-journey-designer.md#paths)

![Option Ajouter un chemin alternatif dans les propriétés de l’activité Condition](assets/journey42.png)

## Dépannage {#troubleshooting}

Avant de tester et de publier votre parcours, vérifiez que toutes les activités sont correctement configurées. Vous ne pouvez pas effectuer de tests ou de publications si des erreurs sont détectées par le système.

Découvrez [dans cette page](troubleshooting.md) comment résoudre les erreurs dans les activités et dans le parcours.

Voir aussi [ Surveillance et dépannage ](../../rp_landing_pages/troubleshoot-journey-landing-page.md)
