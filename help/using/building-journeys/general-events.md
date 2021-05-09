---
solution: Journey Orchestration
title: Événements généraux
description: Découvrez comment utiliser les événements généraux
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Événements généraux {#section_ofg_jss_dgb}

![](../assets/do-not-localize/badge.png)

Pour ce type de événement, vous pouvez uniquement ajouter une étiquette et une description. Le reste de la configuration ne peut pas être modifié. Il a été effectué par l’utilisateur technique. Voir [cette page](../event/about-events.md).

![](../assets/general-events.png)

Lorsque vous déposez un événement métier, il ajoute automatiquement une activité **Lire le segment**. Pour plus d&#39;informations sur les événements d&#39;activité, consultez [cette section](../event/about-events.md)

## Écoute des événements pendant une période spécifique {#events-specific-time}

Une activité événement positionnée dans le parcours écoute les événements indéfiniment. Pour écouter un événement uniquement pendant une certaine période, vous devez configurer un délai d’expiration pour le événement.

Le parcours écoute ensuite le événement pendant la durée spécifiée dans le délai d’attente. Si un événement est reçu au cours de cette période, la personne s&#39;écoule dans le chemin du événement. Dans le cas contraire, le client va soit suivre un délai d’expiration, soit terminer son parcours.

Pour configurer un délai d’expiration pour un événement, procédez comme suit :

1. Activez l&#39;option **[!UICONTROL Activer le délai d&#39;expiration du événement]** à partir des propriétés du événement.

1. Indiquez la durée d’attente du événement par le parcours.

1. Si vous souhaitez envoyer les individus dans un chemin de délai d’attente lorsqu’aucun événement n’est reçu dans le délai d’attente spécifié, activez l’option **[!UICONTROL Définir le chemin d’expiration]**. Si cette option n’est pas activée, le parcours se terminera pour l’utilisateur une fois le délai dépassé.

   ![](../assets/event-timeout.png)

Dans cet exemple, le parcours envoie un premier message de bienvenue à un client. Il envoie alors une remise de repas uniquement si le client entre dans le restaurant le lendemain. Nous avons donc configuré le événement de restaurant avec un délai d&#39;attente d&#39;un jour :

* Si le événement du restaurant est reçu moins d&#39;une journée après la notification d&#39;accueil, le message push de remise de repas est envoyé.
* Si aucun événement de restaurant n’est reçu le lendemain, la personne passe par le chemin du délai d’attente.

Notez que si vous souhaitez configurer un dépassement de délai sur plusieurs événements positionnés après une activité **[!UICONTROL Wait]**, vous devez configurer le dépassement de délai sur un seul de ces événements uniquement.

Le délai d’attente s’applique à tous les événements postérieurs à l’activité **[!UICONTROL Wait]**. Si aucun événement n’est reçu après le délai d’attente spécifié, les individus suivent un seul chemin d’expiration ou terminent leur parcours.

![](../assets/event-timeout-group.png)
