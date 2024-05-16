---
solution: Journey Optimizer
product: journey optimizer
title: Événements généraux
description: Découvrez comment utiliser les événements généraux
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: personnalisé, général, événement, parcours
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 5b7faccbf563c6877a1077b0f6012418848c0ccb
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 74%

---

# Événements généraux {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Événements unitaires"
>abstract="Les événements vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l’individu progressant dans le parcours. Pour ce type d&#39;événement, vous pouvez uniquement ajouter un libellé et une description. La configuration de l’événement est effectuée par un ingénieur de données et ne peut pas être modifiée."

Les événements vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l&#39;individu progressant dans le parcours.

Pour ce type d&#39;événement, vous pouvez uniquement ajouter un libellé et une description. Le reste de la configuration ne peut pas être modifié. C&#39;est l&#39;utilisateur technique qui s&#39;en charge. Voir [cette page](../event/about-events.md).

![](assets/general-events.png)

Lorsque vous déposez un événement métier, cela ajoute automatiquement une activité **Lecture d’audience**. Pour plus d&#39;informations sur les événements métier, consultez [cette section](../event/about-events.md)

## Écoute d&#39;événements au cours d&#39;une période spécifique {#events-specific-time}

Une activité d&#39;événement située sur le parcours va écouter les événements indéfiniment. Pour écouter un événement uniquement pendant une certaine période, vous devez configurer une temporisation pour l&#39;événement.

Ce faisant, le parcours écoutera l&#39;événement au cours de la période définie dans la temporisation. Si un événement est reçu au cours de cette période, le client sera intégré dans le chemin de l&#39;événement. Si ce n’est pas le cas, le client ou la cliente va emprunter le chemin de temporisation s’il est défini, soit continuer ce parcours.

Si aucun chemin de temporisation n’est défini, le paramètre de temporisation agit comme une activité d’attente, ce qui fait que le profil attend pendant une certaine période qui peut être arrêtée si un événement se produit. Si vous souhaitez que les profils soient exclus de ce parcours après temporisation, vous devez définir un chemin de temporisation.

Pour configurer une temporisation d’événement, procédez comme suit :

1. Activez l&#39;option **[!UICONTROL Définir la temporisation de l&#39;événement]** dans les propriétés de l&#39;événement.

1. Définissez la durée pendant laquelle le parcours attendra l&#39;événement. La durée maximale est de 29 jours.

1. Si vous souhaitez orienter les personnes vers un chemin de temporisation, alors qu’aucun événement n’est reçu au cours de la temporisation spécifiée, activez l’option **[!UICONTROL Ajouter un chemin de temporisation]**. Si cette option n’est pas activée, le parcours se poursuit pour l’individu une fois le délai d’expiration atteint. Nous vous recommandons de toujours activer la variable **Définition d’un chemin de temporisation** .

   ![](assets/event-timeout.png)

Dans cet exemple, le parcours envoie un premier e-mail de bienvenue à un client après son entrée dans le hall. Il n’envoie ensuite un email de réduction sur un repas que si le client entre dans le restaurant le lendemain. Nous avons donc configuré l&#39;événement « restaurant » avec une temporisation d&#39;un jour :

* Si l’événement &quot;restaurant&quot; est reçu moins d’un jour après l’e-mail de bienvenue, l’e-mail de remise sur le repas est envoyé.
* Si aucun événement « restaurant » n’est reçu dans la journée qui suit, le client ou la cliente suit le chemin de temporisation.

Notez que si vous souhaitez configurer une temporisation pour plusieurs événements placés après une activité **[!UICONTROL Attente]**, vous ne devez configurer ce délai que pour un seul de ces événements.

Le délai d’expiration défini s’applique à tous les événements situés après la variable **[!UICONTROL Attente]** activité :

* Si un événement est reçu dans le délai d’expiration, l’individu se dirige vers le chemin de l’événement reçu.
* Si aucun événement n’est reçu pendant le délai d’expiration, l’individu se dirige vers la branche de délai d’expiration de l’événement où le délai d’expiration a été défini.

![](assets/event-timeout-group.png)
