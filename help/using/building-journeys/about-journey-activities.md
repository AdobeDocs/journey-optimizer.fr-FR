---
title: À propos des activités de parcours
description: En savoir plus sur les activités de parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 65%

---

# À propos des activités de parcours {#about-journey-activities}

![](../assets/do-not-localize/badge.png)

Combinez les différentes activités d’événement, d’orchestration et d’action afin de créer des scénarios cross-canal à plusieurs étapes.

## Activités d’événement {#event-activities}

Les événements configurés par l’utilisateur technique (voir [cette page](../event/about-events.md)) sont tous affichés dans la première catégorie de la palette, dans la partie gauche de l’écran. Les événements activités suivants sont disponibles :

* [Événements généraux](../building-journeys/general-events.md)
* [Réaction](../building-journeys/reaction-events.md)
* [Qualification du segment](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

Début votre parcours en faisant glisser et en déplaçant une activité de événement. Vous pouvez également double-cliquer sur celle-ci.

![](../assets/journey44.png)

## Activités d’orchestration {#orchestration-activities}

Les activités d’orchestration ci-dessous sont disponibles dans la palette située dans la partie gauche de l’écran :

* [Condition](../building-journeys/condition-activity.md)
* [Fin](../building-journeys/end-activity.md)
* [Attente](../building-journeys/wait-activity.md)
* [Segment lu](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## Activités d&#39;action {#action-activities}

La catégorie **[!UICONTROL Actions]** se trouve dans la palette située dans la partie gauche de l’écran, sous **[!UICONTROL Événements]** et **[!UICONTROL Orchestration.]** Les activités d’action suivantes sont disponibles :

* [Message](../building-journeys/journeys-message.md)
* [Actions personnalisées](../building-journeys/using-custom-actions.md)
* [Sauter](../building-journeys/jump.md)

![](../assets/journey58.png)

Ces activités représentent les différents canaux de communication disponibles. Vous pouvez les combiner pour créer un scénario cross-canal.

Si vous avez configuré des actions personnalisées, elles s’affichent ici (voir [cette page](../building-journeys/using-custom-actions.md)).

## Bonnes pratiques {#best-practices}

La plupart des activités vous permettent de définir une **[!UICONTROL étiquette]**. Ceci ajoute un suffixe au nom qui apparaîtra sous votre activité dans la trame. Cela s’avère utile si vous utilisez plusieurs fois la même activité dans votre parcours et souhaitez les identifier plus facilement. Cela facilite également le débogage lorsque des erreurs se produisent et permet une lecture plus facile des rapports. Vous pouvez, en outre, ajouter une **[!UICONTROL description]** facultative.

![](../assets/journey59bis.png)

Lorsqu’une erreur se produit dans une action ou une condition, le parcours d’un individu s’arrête. La seule façon de le faire continuer est de cocher la case **[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d’erreur]**. Consultez [cette section](../building-journeys/using-the-journey-designer.md#paths).

![](../assets/journey42.png)
