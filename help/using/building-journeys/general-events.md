---
solution: Journey Optimizer
title: Événements généraux
description: Découvrez comment utiliser les événements généraux
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 8a859af9ad09ca3f240ff6f355d4e5f34d2e4eac
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 100%

---

# Événements généraux {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Événements généraux"
>abstract="Pour ce type d&#39;événement, vous pouvez uniquement ajouter un libellé et une description. Le reste de la configuration ne peut pas être modifié. C&#39;est l&#39;utilisateur technique qui s&#39;en charge."

Pour ce type d&#39;événement, vous pouvez uniquement ajouter un libellé et une description. Le reste de la configuration ne peut pas être modifié. C&#39;est l&#39;utilisateur technique qui s&#39;en charge. Voir [cette page](../event/about-events.md).

![](assets/general-events.png)

Lorsque vous déposez un événement métier, cela ajoute automatiquement une activité **Lecture de segment**. Pour plus d&#39;informations sur les événements métier, consultez [cette section](../event/about-events.md)

## Écoute d&#39;événements au cours d&#39;une période spécifique {#events-specific-time}

Une activité d&#39;événement située sur le parcours va écouter les événements indéfiniment. Pour écouter un événement uniquement pendant une certaine période, vous devez configurer une temporisation pour l&#39;événement.

Ce faisant, le parcours écoutera l&#39;événement au cours de la période définie dans la temporisation. Si un événement est reçu au cours de cette période, le client sera intégré dans le chemin de l&#39;événement. Dans le cas contraire, le client intègrera un itinéraire de temporisation ou terminera son parcours. 

Pour configurer une temporisation d’événement, procédez comme suit :

1. Activez l&#39;option **[!UICONTROL Définir la temporisation de l&#39;événement]** dans les propriétés de l&#39;événement.

1. Définissez la durée pendant laquelle le parcours attendra l&#39;événement.

1. Si vous souhaitez orienter les individus vers un chemin de temporisation, alors qu&#39;aucun événement n&#39;est reçu au cours de la temporisation spécifiée, activez l&#39;option **[!UICONTROL Ajouter un itinéraire de temporisation]**. Si cette option n&#39;est pas activée, le parcours se termine pour l&#39;individu une fois le délai de temporisation atteint.

   ![](assets/event-timeout.png)

Dans cet exemple, le parcours envoie un premier message de bienvenue à un client. Il n&#39;envoie ensuite un message d&#39;offre de réduction sur un repas que si le client entre dans le restaurant le lendemain. Nous avons donc configuré l&#39;événement « restaurant » avec une temporisation d&#39;un jour :

* Si l&#39;événement « restaurant » est reçu moins de 1 jour après la notification push de bienvenue, l&#39;activité push de remise sur un repas est envoyée.
* Si aucun événement « restaurant » n&#39;est reçu dans la journée qui suit, le client s&#39;engage dans l&#39;itinéraire de temporisation.

Notez que si vous souhaitez configurer une temporisation pour plusieurs événements placés après une activité **[!UICONTROL Attente]**, vous ne devez configurer ce délai que pour un seul de ces événements.

La temporisation s&#39;applique à tous les événements postérieurs à l&#39;activité **[!UICONTROL Attente]**. Si aucun événement n&#39;est reçu avant la temporisation spécifiée, les individus s&#39;engagent dans un itinéraire de temporisation unique ou terminent leur parcours.

![](assets/event-timeout-group.png)
