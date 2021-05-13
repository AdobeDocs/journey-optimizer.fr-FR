---
solution: Journey Orchestration
title: Événements généraux
description: Découvrez comment utiliser les événements généraux
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 86%

---

# Événements généraux {#section_ofg_jss_dgb}

![](../assets/do-not-localize/badge.png)

Pour ce type d’événement, vous pouvez uniquement ajouter un libellé et une description. Le reste de la configuration ne peut pas être modifié. C’est l’utilisateur technique qui s’en charge. Voir [cette page](../event/about-events.md).

![](../assets/general-events.png)

Lorsque vous déposez un événement métier, il ajoute automatiquement une activité **Lire le segment**. Pour plus d&#39;informations sur les événements d&#39;activité, consultez [cette section](../event/about-events.md)

## Écoute d’événements au cours d’une période spécifique {#events-specific-time}

Une activité d’événement située sur le parcours va écouter les événements indéfiniment. Pour écouter un événement uniquement pendant une certaine période, vous devez configurer une temporisation pour l’événement.

Ce faisant, le parcours écoutera l’événement au cours de la période définie dans la temporisation. Si un événement est reçu au cours de cette période, le client sera intégré dans le chemin de l’événement. Si ce n’est pas le cas, le client va, au choix, s’engager dans un chemin de temporisation ou terminer son parcours.

Pour configurer une temporisation d’événement, procédez comme suit :

1. Activez l’option **[!UICONTROL Définir la temporisation de l’événement]** dans les propriétés de l’événement.

1. Définissez la durée pendant laquelle le parcours attendra l’événement.

1. Si vous souhaitez orienter les individus vers un chemin de temporisation, alors qu’aucun événement n’est reçu au cours de la temporisation spécifiée, activez l’option **[!UICONTROL Ajouter un itinéraire de temporisation]**. Si cette option n’est pas activée, le parcours se termine pour l’individu une fois le délai de temporisation atteint.

   ![](../assets/event-timeout.png)

Dans cet exemple, le parcours envoie un premier message de bienvenue à un client. Il n’envoie ensuite un message d’offre de réduction sur un repas que si le client entre dans le restaurant le lendemain. Nous avons donc configuré l’événement « restaurant » avec une temporisation d’un jour :

* Si le événement du restaurant est reçu moins d&#39;une journée après la notification d&#39;accueil, le message push de remise de repas est envoyé.
* Si aucun événement « restaurant » n’est reçu dans la journée qui suit, le client s’engage dans l’itinéraire de temporisation.

Notez que si vous souhaitez configurer une temporisation pour plusieurs événements placés après une activité d’**[!UICONTROL Attente]**, vous ne devez configurer ce délai que pour un seul de ces événements.

La temporisation s’applique à tous les événements postérieurs à l’activité **[!UICONTROL Attente]**. Si aucun événement n’est reçu après la temporisation spécifiée, les individus s’engagent dans un itinéraire de temporisation unique ou terminent leur parcours.

![](../assets/event-timeout-group.png)
