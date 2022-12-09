---
solution: Journey Optimizer
product: journey optimizer
title: Événements généraux
description: Découvrez comment utiliser les événements généraux
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Événements généraux {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Événements généraux"
>abstract="Les événements vous permettent de déclencher unitairement vos parcours pour envoyer des messages, en temps réel, à l’individu qui participe au parcours. Pour ce type d&#39;événement, vous pouvez uniquement ajouter un libellé et une description. La configuration de l’événement est effectuée par un ingénieur de données et ne peut pas être modifiée."

Les événements vous permettent de déclencher unitairement vos parcours pour envoyer des messages, en temps réel, à l’individu qui participe au parcours.

Pour ce type d&#39;événement, vous pouvez uniquement ajouter un libellé et une description. Le reste de la configuration ne peut pas être modifié. Elle a été effectuée par l’utilisateur technique. Voir [cette page](../event/about-events.md).

![](assets/general-events.png)

Lorsque vous déposez un événement d’entreprise, il ajoute automatiquement une **Lecture de segment** activité. Pour plus d’informations sur les événements professionnels, reportez-vous à la section [cette section](../event/about-events.md)

## Écoute des événements pendant une période spécifique {#events-specific-time}

Une activité d’événement positionnée dans le parcours écoute les événements indéfiniment. Pour écouter un événement uniquement pendant une certaine période, vous devez configurer un délai d’expiration pour l’événement.

Le parcours écoutera alors l’événement au cours de la période spécifiée dans le délai d’expiration. Si un événement est reçu au cours de cette période, la personne se trouve dans le chemin de l’événement. Si ce n’est pas le cas, le client va soit s’engager dans un chemin d’accès au délai d’expiration, soit terminer son parcours.

Pour configurer un délai d’expiration pour un événement, procédez comme suit :

1. Activez la variable **[!UICONTROL Define the event timeout]** dans les propriétés de l’événement.

1. Spécifiez la durée pendant laquelle le parcours attendra l’événement.

1. Si vous souhaitez envoyer les individus dans un chemin d’accès au délai d’expiration alors qu’aucun événement n’est reçu au cours du délai d’expiration spécifié, activez la variable **[!UICONTROL Set a timeout path]** . Si cette option n’est pas activée, le parcours se termine pour l’individu une fois le délai d’expiration atteint.

   ![](assets/event-timeout.png)

Dans cet exemple, le parcours envoie un premier message de bienvenue à un client. Il envoie ensuite une notification push de remise sur un repas uniquement si le client entre dans le restaurant le lendemain. Nous avons donc configuré l’événement &quot;restaurant&quot; avec un délai d’expiration d’un jour :

* Si l’événement &quot;restaurant&quot; est reçu moins d’un jour après la notification push de bienvenue, l’activité push de remise sur un repas est envoyée.
* Si aucun événement &quot;restaurant&quot; n’est reçu le lendemain, le client passe par le chemin d’accès au délai d’expiration.

Notez que si vous souhaitez configurer un délai d’expiration pour plusieurs événements placés après un événement **[!UICONTROL Wait]** vous ne devez configurer le délai d’expiration que pour l’un de ces événements.

Le délai d’expiration s’applique à tous les événements placés après la **[!UICONTROL Wait]** activité. Si aucun événement n’est reçu avant le délai d’expiration spécifié, les individus s’engagent dans un seul chemin d’accès au délai d’expiration ou terminent leur parcours.

![](assets/event-timeout-group.png)
