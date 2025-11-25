---
solution: Journey Optimizer
product: journey optimizer
title: Événements de réaction
description: Découvrez comment utiliser les événements de réaction pour répondre aux données de suivi des messages telles que les ouvertures et les clics dans vos parcours, et comment configurer des chemins de temporisation pour les non-répondeurs.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: parcours, événements, réaction, tracking, platform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: d8fa1c7055e4e31e393e36ba16863e0f8f95ca9b
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 48%

---

# Événements de réaction {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Événements de réaction"
>abstract="Cette activité vous permet de réagir aux données de suivi liées à un message envoyé au sein du même parcours. Ces données sont collectées en temps réel au moment de leur partage avec Adobe Experience Platform."

## Vue d’ensemble {#overview}

Parmi les différentes activités d’événement disponibles dans la palette, vous trouverez l’événement **[!UICONTROL Réactions]** intégré. Cette activité vous permet de réagir aux données de suivi liées à un message envoyé au sein du même parcours. Ces données sont collectées en temps réel au moment de leur partage avec Adobe Experience Platform.

Vous pouvez réagir aux messages ouverts ou sur lesquels vous avez cliqué. Par exemple, vous pouvez envoyer un autre message si une personne a ouvert l’e-mail précédent ou cliqué dessus, ou envoyer un autre message de relance si elle n’a pas interagi avec votre communication.

Voir [Activités d’action](../building-journeys/about-journey-activities.md#action-activities).

Vous pouvez utiliser l’activité **[!UICONTROL Réaction]** pour effectuer une action en l’absence de réaction à vos messages. Pour ce faire, créez un deuxième chemin parallèlement à l’activité **[!UICONTROL Réaction]** et ajoutez une activité **[!UICONTROL Attente]**. En l&#39;absence de réaction au cours de la période définie dans l&#39;activité **[!UICONTROL Attente]**, c&#39;est le second chemin qui est choisi. Vous pouvez opter, par exemple, pour l’envoi d’un message de relance.

## Configuration des événements de réaction {#configure}

![Configuration d’événement de réaction avec options de sélection de canal et de type d’événement](assets/journey45.png)

Pour configurer les événements de réaction, procédez comme suit :

1. Placez une activité **[!UICONTROL Réaction]** **immédiatement** après une activité d’action [canal](journeys-message.md) sur la zone de travail du parcours.
1. Ajoutez un **[!UICONTROL libellé]** à la réaction. Cette étape est facultative.
1. Dans la liste déroulante, sélectionnez l’activité d’action à laquelle vous souhaitez réagir. Vous pouvez sélectionner toute activité d’action figurant dans les étapes précédentes du chemin.
1. Selon l’action que vous avez sélectionnée, choisissez ce à quoi vous souhaitez réagir.
1. Vous pouvez définir une temporisation de l’événement (entre 40 secondes et 90 jours), ainsi qu’un chemin de temporisation. Cette opération crée un deuxième chemin pour les personnes qui n’ont pas réagi pendant la durée définie. Lors du test d’un parcours qui a recours à un événement de réaction, la **[!UICONTROL Durée d’attente]** du mode test par défaut ainsi que sa valeur minimale sont de 40 secondes. Consultez [cette section](../building-journeys/testing-the-journey.md).

## Mécanismes de sécurisation et limitations {#guardrails-limitations}

* Une activité **[!UICONTROL Réaction]** doit être placée **immédiatement** après une activité d’action [canal](journeys-message.md) dans la zone de travail du parcours.
* Vous ne pouvez pas utiliser une activité **[!UICONTROL Réaction]** s’il n’y a aucune activité d’action de canal devant elle.
* Le placement d’une activité **[!UICONTROL Attente]** ou de toute autre activité entre l’action de canal et l’activité **[!UICONTROL Réaction]** n’est pas pris en charge et peut entraîner un dysfonctionnement de la réaction comme prévu.
* Les événements de réaction ne peuvent suivre que les messages envoyés dans le même parcours. Ils ne peuvent pas suivre les messages qui se produisent dans un autre parcours.
* Ils effectuent le suivi des clics sur les liens de type « suivi ». Les liens de désabonnement et de page miroir ne sont pas pris en compte.
* Le suivi des ouvertures d’email est effectué à l’aide d’une image de 0 pixel incluse dans l’e-mail. Si les clients de messagerie (tels que Gmail) bloquent les images, les ouvertures d’e-mail ne sont pas prises en compte.
