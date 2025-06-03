---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des activités du parcours
description: Prise en main des activités du parcours
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: parcours, activités, commencer, événements, action
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 84beb9ba9646cb1b40bcfd8a180fc98963a8ff0b
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 63%

---

# Prise en main des activités du parcours {#about-journey-activities}

Combinez les différentes activités d&#39;événement, d&#39;orchestration et d&#39;action afin de créer des scénarios cross-canal à plusieurs étapes.

## Activités d’événement {#event-activities}

Les parcours personnalisés sont déclenchés par des événements, tels qu’un achat en ligne. Une fois qu’un profil entre dans un parcours, il évolue de manière individuelle, et deux individus ne peuvent pas évoluer à la même vitesse ou sur le même chemin. Lorsque vous commencez votre parcours avec un événement, le parcours se déclenche à la réception de l’événement. Ensuite, chaque personne du parcours suit individuellement les étapes suivantes définies dans votre parcours.

Les événements configurés par l’utilisateur ou l’utilisatrice technique (voir [cette page](../event/about-events.md)) sont tous affichés dans la première catégorie de la palette, dans la partie gauche de l’écran. Les activités d’événement suivantes sont disponibles :

* [Événements généraux](../building-journeys/general-events.md)
* [Réaction](../building-journeys/reaction-events.md)
* [Qualification de l’audience](../building-journeys/audience-qualification-events.md)

![Palette des activités d&#39;événement dans le concepteur de parcours ](assets/journey43.png)

Pour démarrer votre parcours, effectuez un glisser-déposer d’une activité d’événement. Vous pouvez également double-cliquer sur celle-ci.

![Activité d’événement de glisser-déposer dans le concepteur de parcours ](assets/journey44.png)

## Activités d’orchestration {#orchestration-activities}

Les activités d’orchestration sont des conditions différentes qui permettent de déterminer l’étape suivante du parcours. Ces conditions peuvent inclure le fait de savoir si la personne a un dossier d’assistance ouvert, les prévisions météorologiques à son emplacement actuel, si elle a effectué un achat ou si elle a atteint 10 000 points de fidélité.

Les activités d’orchestration ci-dessous sont disponibles dans la palette située dans la partie gauche de l’écran :

* [Condition](../building-journeys/condition-activity.md)
* [Attente](../building-journeys/wait-activity.md)
* [Lecture d’audience](../building-journeys/read-audience.md)

![Palette des activités d’orchestration dans le concepteur de parcours ](assets/journey49.png)

## Activités d’action {#action-activities}

Les actions sont ce que vous souhaitez qu’il se produise à la suite d’un déclencheur, comme l’envoi d’un message. Il s’agit de l’élément du parcours que le client ou la cliente rencontre.

La catégorie **[!UICONTROL Actions]** se trouve dans la palette située dans la partie gauche de l’écran, sous **[!UICONTROL Événements]** et **[!UICONTROL Orchestration]**. Les activités d’action suivantes sont disponibles :

* [Actions de canal intégrées](../building-journeys/journeys-message.md)
* [Actions personnalisées](../building-journeys/using-custom-actions.md)
* [Sauter](../building-journeys/jump.md)

![Palette des activités d&#39;action dans le concepteur de parcours ](assets/journey58.png)

Ces activités représentent les différents canaux de communication disponibles. Vous pouvez les combiner pour créer un scénario cross-canal.

<!--If you have configured custom actions, they also appear here. [Learn more](../building-journeys/using-custom-actions.md)-->

Vous pouvez également configurer des actions spécifiques pour envoyer des messages :

* Si vous utilisez un système tiers pour envoyer des messages, vous pouvez créer une action personnalisée spécifique. [En savoir plus](../action/action.md)

* Si vous utilisez Campaign et Journey Optimizer, reportez-vous aux sections suivantes :

   * [[!DNL Journey Optimizer] et Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] et Campaign Standard](../action/acs-action.md)

## Bonnes pratiques {#best-practices}

### Ajouter un libellé

La plupart des activités vous permettent de définir un **[!UICONTROL libellé]**. Cela ajoute un suffixe au nom qui s’affiche sous votre activité dans la zone de travail. Cela s’avère utile si vous utilisez plusieurs fois la même activité dans votre parcours et souhaitez faciliter son identification. Cela facilite également le débogage en cas d’erreurs et facilite la lecture des rapports. Vous pouvez, en outre, ajouter une **[!UICONTROL description]** facultative.

![](assets/journey-action-label.png)

>[!NOTE]
>
>Pour certaines activités, leur identifiant est également visible dans le volet. Cet identifiant peut être utilisé dans les rapports sous la forme d’une clé plus stable que le libellé, qui peut changer.

### Gérer les paramètres avancés {#advanced-parameters}

La plupart des activités affichent un certain nombre de paramètres avancés et/ou techniques que vous ne pouvez pas modifier.

![](assets/journey-advanced-parameters.png)

Pour une meilleure lisibilité, masquez ces paramètres à l’aide du bouton **[!UICONTROL Masquer les champs en lecture seule]**.

![](assets/journey-hide-read-only-fields.png)

Dans certains contextes précis, vous pouvez remplacer les valeurs de ces paramètres pour une utilisation spécifique. Pour forcer une valeur, cliquez sur l’icône **[!UICONTROL Activer le remplacement du paramètre]** à droite du champ. [En savoir plus](../configuration/primary-email-addresses.md#journey-parameters).

![](assets/journey-enable-parameter-override.png)

### Ajouter un chemin d’accès alternatif

Lorsqu’une erreur se produit dans une action ou une condition, le parcours d’une personne s’arrête. La seule façon de le faire continuer est de cocher la case **[!UICONTROL Ajouter un chemin alternatif en cas de temporisation ou d’erreur]**. Consultez [cette section](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
