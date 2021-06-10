---
title: Événements de réaction
description: En savoir plus sur les événements de réaction
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '357'
ht-degree: 100%

---

# Événements de réaction {#section_dhx_gss_dgb}

![](../assets/do-not-localize/badge.png)

Parmi les différentes activités d’événement disponibles dans la palette, vous trouverez l’événement **[!UICONTROL Réactions]** intégré. Cette activité vous permet de réagir aux données de suivi liées à un message envoyé au sein du même parcours. Ces données sont collectées en temps réel au moment de leur partage avec Adobe Experience Platform. Dans le cas des notifications push, vous pouvez réagir aux messages envoyés, aux messages en échec et à ceux sur lesquels un utilisateur a cliqué. Pour les SMS, vous pouvez réagir aux messages envoyés ou en échec. Dans le cas des e-mails, vous pouvez réagir aux messages envoyés, ouverts et en échec, ainsi qu’à ceux sur lesquels un utilisateur a cliqué.

Vous pouvez également utiliser ce mécanisme pour effectuer une action en l’absence de réaction à vos messages. Pour ce faire, créez un deuxième chemin parallèlement à l’activité de réaction et ajoutez une activité d’attente. En l’absence de réaction au cours de la période définie dans l’activité d’attente, ce deuxième chemin sera choisi. Vous pouvez opter, par exemple, pour l’envoi d’un message de relance.

Notez que vous ne pouvez utiliser une activité de réaction dans la zone de travail que s’il existe au préalable une activité **Message**.

Voir [À propos des activités d’action](../building-journeys/about-journey-activities.md#action-activities).

![](../assets/journey45.png)

La procédure de configuration des événements de réaction comprend les étapes suivantes :

1. Ajoutez un **[!UICONTROL libellé]** à la réaction. Cette étape est facultative.
1. Dans la liste déroulante, sélectionnez l’activité d’action à laquelle vous souhaitez réagir. Vous pouvez sélectionner toute activité d’action figurant dans les étapes précédentes du chemin.
1. Selon l’action que vous avez sélectionnée, choisissez ce à quoi vous souhaitez réagir.
1. Vous pouvez définir une temporisation de l’événement (entre 40 secondes et 30 jours) ainsi qu’un itinéraire de temporisation. Cette opération créera un second itinéraire pour les individus n’ayant pas réagi pendant la durée définie. Lors du test d’un parcours qui a recours à un événement de réaction, la **[!UICONTROL Durée d’attente]** du mode test par défaut ainsi que sa valeur minimale sont de 40 secondes. Consultez [cette section](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Les événements de réaction ne peuvent pas suivre les messages qui se produisent dans un autre parcours.
>
>Ils effectuent le suivi des clics sur les liens de type « suivi ». Les liens de désabonnement et de page miroir ne sont pas pris en compte.

>[!IMPORTANT]
>
>Les clients de messagerie tels que Gmail autorisent le blocage d’images. Le suivi des ouvertures d’email est effectué à l’aide d’une image de 0 pixel incluse dans l’email. Si les images sont bloquées, les ouvertures d’email ne sont pas prises en compte.
