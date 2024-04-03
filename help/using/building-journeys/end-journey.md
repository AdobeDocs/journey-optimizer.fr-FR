---
solution: Journey Optimizer
product: journey optimizer
title: Fin de parcours
description: Découvrez comment un parcours se termine dans Journey Optimizer.
feature: Journeys
role: User
level: Intermediate
keywords: reprise, parcours, fin, dynamique, arrêt
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: ht
source-wordcount: '660'
ht-degree: 100%

---

# Terminer un parcours{#journey-ending}

Un parcours peut se terminer pour un individu dans deux contextes spécifiques :

* Le client arrive à la dernière activité d&#39;un chemin.
* Le client arrive à une activité **Condition** (ou à une activité **Attente** avec une condition) et ne répond à aucune des conditions.

Il peut alors rejoindre de nouveau le parcours si la rentrée est autorisée. Voir [cette page](../building-journeys/journey-gs.md#change-properties)

Pour terminer un parcours actif, nous vous recommandons de le fermer. L’arrivée de nouveaux clients dans le parcours sera alors bloquée. Les clients qui ont déjà rejoint le parcours peuvent l’expérimenter jusqu’à la fin. Consultez [cette section](../building-journeys/journey.md#close-journey)

Vous pouvez arrêter un parcours uniquement lorsqu’une urgence s’est produite et qu’il doit être mis fin immédiatement à tout traitement sur un parcours. Les personnes qui l’ont déjà rejoint sont toutes stoppées dans leur progression. Consultez [cette section](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Notez que vous ne pouvez pas reprendre un parcours fermé ou arrêté.

## Balise de fin de parcours{#end-tag}

Lors de la création d’un parcours, une « balise de fin » s’affiche à la fin de chaque chemin. Ce nœud ne peut pas être ajouté par un utilisateur, ne peut pas être supprimé et seul son libellé peut être modifié. Il marque la fin de chaque chemin du parcours. Si le parcours comporte plusieurs chemins, il est conseillé d’ajouter un libellé à chaque fin pour faciliter la lecture des rapports. Consultez [cette page](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Fermeture d’un parcours{#close-journey}

Les raisons suivantes peuvent entraîner la fermeture d&#39;un parcours :

* Le parcours est fermé manuellement par le biais du bouton **[!UICONTROL Fermer aux nouvelles entrées]**.
* Un parcours basé sur un segment « unique » qui a terminé son exécution.
* Après la dernière occurrence d’un parcours récurrent basé sur une audience.

Le fait de fermer un parcours manuellement assure que les clients qui l’ont déjà rejoint puissent terminer leur chemin, mais que les nouveaux utilisateurs ne puissent pas le rejoindre. Lorsqu&#39;un parcours est fermé (pour l&#39;une des raisons ci-dessus), le statut **[!UICONTROL Fermé]** lui est attribué. Il n’est alors plus accessible aux nouveaux individus. En revanche, les personnes qui ont déjà intégré le parcours peuvent le terminer normalement.

Au-delà de 30 jours, un parcours Lecture d’audience passe au statut **Terminé**. Ce comportement est défini uniquement sur 30 jours (c’est-à-dire sur la valeur par défaut du délai d’expiration du parcours), car toutes les informations relatives aux profils déjà entrés dans le parcours sont supprimées 30 jours après leur entrée. Les personnes toujours présentes dans le parcours sont automatiquement affectées. Elles quittent le parcours après le délai d’expiration de 30 jours.

Consultez cette [section](../building-journeys/journey-gs.md#global_timeout).

La version d&#39;un parcours fermé ne peut pas être redémarrée ni supprimée. Vous pouvez la dupliquer ou en créer une nouvelle version. Seuls les parcours terminés peuvent être supprimés.

Pour fermer un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Fermer aux nouvelles entrées]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez fermer.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![](assets/finish_drop_down_list.png)

1. Cliquez sur **[!UICONTROL Fermer aux nouvelles entrées]** et confirmez dans la boîte de dialogue.

## Arrêt d’un parcours{#stop-journey}

Si nécessaire, il est possible d’arrêter la progression de tous les individus dans le parcours. L’arrêt du parcours entraîne la temporisation de tous les individus qui en font partie. Cependant, le fait d’arrêter un parcours suppose qu&#39;il soit mis un terme à la progression de toutes les personnes qui y participent. Le parcours est simplement mis à l&#39;arrêt. Si vous souhaitez mettre fin à un parcours, nous vous recommandons de le fermer.

La version d’un parcours arrêté ne peut pas être redémarrée.

À l’arrêt, le statut du parcours est défini sur **[!UICONTROL Arrêté]**.

Vous pouvez arrêter un parcours, par exemple, si un spécialiste marketing se rend compte que le parcours cible une audience incorrecte ou si une action personnalisée censée diffuser des messages ne fonctionne pas correctement. Pour arrêter un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Arrêter]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez arrêter.
1. En haut à droite, cliquez sur la flèche vers le bas.
   ![](assets/finish_drop_down_list.png)
1. Cliquez sur **[!UICONTROL Arrêter]** et confirmez dans la boîte de dialogue.
