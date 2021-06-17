---
solution: Journey Orchestration
title: Événements généraux
description: Découvrez comment utiliser les événements généraux
feature: Parcours
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: 285942ec51859a4cea888d9974f79f52acf3aabf
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 63%

---

# Événements généraux {#section_ofg_jss_dgb}

Pour ce type d’événement, vous pouvez uniquement ajouter un libellé et une description. Le reste de la configuration ne peut pas être modifié. C’est l’utilisateur technique qui s’en charge. Voir [cette page](../event/about-events.md).

![](../assets/general-events.png)

Lorsque vous déposez un événement commercial, il ajoute automatiquement une activité **Lecture de segment** . Pour plus d&#39;informations sur les événements métier, consultez [cette section](../event/about-events.md)

## Écoute d’événements au cours d’une période spécifique {#events-specific-time}

Une activité d’événement située sur le parcours va écouter les événements indéfiniment. Pour écouter un événement uniquement pendant une certaine période, vous devez configurer une temporisation pour l’événement.

Ce faisant, le parcours écoutera l’événement au cours de la période définie dans la temporisation. Si un événement est reçu au cours de cette période, le client sera intégré dans le chemin de l’événement. Si ce n’est pas le cas, le client va, au choix, s’engager dans un chemin de temporisation ou terminer son parcours.

Pour configurer une temporisation d’événement, procédez comme suit :

1. Activez l’option **[!UICONTROL Définir le délai d’expiration de l’événement]** dans les propriétés de l’événement.

1. Définissez la durée pendant laquelle le parcours attendra l’événement.

1. Si vous souhaitez envoyer les individus dans un chemin d’accès au délai d’expiration alors qu’aucun événement n’est reçu au cours du délai d’expiration spécifié, activez l’option **[!UICONTROL Définir un chemin d’accès au délai d’expiration]** . Si cette option n’est pas activée, le parcours se termine pour l’individu une fois le délai de temporisation atteint.

   ![](../assets/event-timeout.png)

Dans cet exemple, le parcours envoie un premier message de bienvenue à un client. Il n’envoie ensuite un message d’offre de réduction sur un repas que si le client entre dans le restaurant le lendemain. Nous avons donc configuré l’événement « restaurant » avec une temporisation d’un jour :

* Si l’événement &quot;restaurant&quot; est reçu moins d’un jour après la notification push de bienvenue, l’activité push de remise sur un repas est envoyée.
* Si aucun événement « restaurant » n’est reçu dans la journée qui suit, le client s’engage dans l’itinéraire de temporisation.

Notez que si vous souhaitez configurer un délai d’expiration sur plusieurs événements placés après une activité **[!UICONTROL Attente]** , vous devez configurer le délai d’expiration sur l’un de ces événements uniquement.

Le délai d’expiration s’applique à tous les événements placés après l’activité **[!UICONTROL Attente]** . Si aucun événement n’est reçu avant le délai d’expiration spécifié, les individus s’engagent dans un seul chemin d’accès au délai d’expiration ou mettent fin à leur parcours.

![](../assets/event-timeout-group.png)
