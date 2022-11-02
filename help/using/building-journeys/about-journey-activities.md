---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des activités de parcours
description: Prise en main des activités de parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 49%

---

# Prise en main des activités de parcours {#about-journey-activities}

Combinez les différentes activités d&#39;événement, d&#39;orchestration et d&#39;action afin de créer des scénarios cross-canal à plusieurs étapes.

## Activités d’événement {#event-activities}

Les événements sont ce qui déclenche un parcours personnalisé, comme un achat en ligne. Une fois que quelqu&#39;un entre dans un parcours, il se déplace à travers en tant qu&#39;individu, et pas deux individus ne se déplacent à la même vitesse ou le même chemin. Lorsque vous lancez votre parcours avec un événement, celui-ci est déclenché à la réception de l’événement. Chaque personne du parcours suit ensuite, individuellement, les étapes suivantes définies dans votre parcours.

Événements configurés par l’utilisateur technique (voir [cette page](../event/about-events.md)) sont toutes affichées dans la première catégorie de la palette, sur le côté gauche de l’écran. Les activités d&#39;événement suivantes sont disponibles :

* [Événements généraux](../building-journeys/general-events.md)
* [Réaction](../building-journeys/reaction-events.md)
* [Qualification du segment](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Commencez votre parcours en faisant glisser et déposer une activité d’événement. Vous pouvez également double-cliquer sur celle-ci.

![](assets/journey44.png)

## Activités d’orchestration {#orchestration-activities}

Les activités d’orchestration sont des conditions différentes qui permettent de déterminer l’étape suivante du parcours. Cela peut être le cas si la personne a un cas de soutien ouvert ou non, les prévisions météorologiques à son emplacement actuel, si elle a effectué un achat ou non, ou si elle a atteint 10 000 points de fidélité.

Les activités d’orchestration ci-dessous sont disponibles dans la palette située dans la partie gauche de l’écran :

* [Condition](../building-journeys/condition-activity.md)
* [Attente](../building-journeys/wait-activity.md)
* [Lecture de segment](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Activités d&#39;action {#action-activities}

Les actions sont ce que vous voulez qu’il se produise à la suite d’un déclencheur, comme l’envoi d’un message. C’est le parcours que le client rencontre.

Dans la palette, située à gauche de l’écran, au-dessous **[!UICONTROL Événements]** et **[!UICONTROL Orchestration]**, vous pouvez trouver la variable **[!UICONTROL Actions]** catégorie. Les activités d&#39;action suivantes sont disponibles :

* [E-mail, SMS, Push](../building-journeys/journeys-message.md)
* [Actions personnalisées](../building-journeys/using-custom-actions.md)
* [Sauter](../building-journeys/jump.md)

![](assets/journey58.png)

Ces activités représentent les différents canaux de communication disponibles. Vous pouvez les combiner pour créer un scénario cross-canal.

Si vous avez configuré des actions personnalisées, elles s’affichent également à cet emplacement. [En savoir plus](../building-journeys/using-custom-actions.md)).

## Bonnes pratiques {#best-practices}

La plupart des activités vous permettent de définir un **[!UICONTROL libellé]**. Vous pouvez ainsi ajouter un suffixe au nom qui apparaîtra sous votre activité dans la zone de travail. Cela s’avère utile si vous utilisez plusieurs fois la même activité dans votre parcours et souhaitez faciliter son identification. Cela facilite également le débogage lorsque des erreurs se produisent et permet une lecture plus facile des rapports. Vous pouvez, en outre, ajouter une **[!UICONTROL description]** facultative.

![](assets/journey59bis.png)

Lorsqu&#39;une erreur se produit dans une action ou une condition, le parcours d&#39;un individu s&#39;arrête. La seule façon de le faire continuer est de cocher la case **[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d&#39;erreur]**. Consultez [cette section](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
