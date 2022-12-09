---
solution: Journey Optimizer
product: journey optimizer
title: Fin du parcours
description: Découvrez comment un parcours se termine dans Journey Optimizer
feature: Journeys
role: User
level: Beginner
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Fin d’un parcours{#journey-ending}

Un parcours peut se terminer pour un individu dans deux contextes spécifiques :

* La personne arrive à la dernière activité d’un chemin.
* La personne arrive à un **Condition** (ou une **Attente** activité avec une condition) et ne correspond à aucune des conditions.

La personne peut alors revenir dans le parcours si une rentrée est autorisée. Voir [cette page](../building-journeys/journey-gs.md#change-properties)

Pour terminer un parcours actif, nous vous recommandons de le fermer. L&#39;arrivée de nouveaux clients dans le parcours sera alors bloquée. Les clients qui sont déjà entrés dans le parcours peuvent l’expérimenter jusqu’à la fin. Voir [cette section](../building-journeys/journey.md#close-journey)

Vous ne pouvez arrêter un parcours que si une urgence s’est produite et que tous les traitements doivent être terminés immédiatement. Les personnes qui sont déjà entrées dans un parcours sont toutes arrêtées dans leur progression. Voir [cette section](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Notez que vous ne pouvez pas reprendre un parcours fermé ou arrêté.

## Balise de fin de parcours{#end-tag}

Lors de la création d’un parcours, une &quot;balise de fin&quot; s’affiche à la fin de chaque chemin. Ce noeud ne peut pas être ajouté par un utilisateur, ne peut pas être supprimé et seul son libellé peut être modifié. Il marque la fin de chaque chemin du parcours. Si le parcours comporte plusieurs chemins, il est recommandé d’ajouter un libellé à chaque fin afin de faciliter la lecture des rapports. Voir [cette page](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Fermeture d’un parcours{#close-journey}

Un parcours peut se fermer pour les raisons suivantes :

* Le parcours est fermé manuellement via la variable **[!UICONTROL Close to new entrances]** bouton .
* Parcours basé sur un segment à une seule prise de vue dont l’exécution est terminée.
* Après la dernière occurrence d’un parcours récurrent basé sur des segments.

La fermeture manuelle d’un parcours permet de s’assurer que les clients qui y sont déjà entrés puissent terminer leur chemin, mais que les nouveaux utilisateurs ne puissent pas y accéder. Lorsqu’un parcours est fermé (pour l’une des raisons ci-dessus), il a le statut **[!UICONTROL Closed]**. Le parcours cesse de laisser de nouveaux individus entrer dans le parcours. Les personnes déjà engagées dans le parcours peuvent terminer le parcours normalement. Après le délai d’expiration global par défaut de 30 jours, le parcours passe à la variable **Terminé** statut. Voir [section](../building-journeys/journey-gs.md#global_timeout).

Une version de parcours fermée ne peut pas être redémarrée ni supprimée. Vous pouvez en créer une nouvelle version ou la dupliquer. Seuls les parcours terminés peuvent être supprimés.

Pour fermer un parcours de la liste, cliquez sur le bouton **[!UICONTROL Ellipsis]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également :

1. Dans le **[!UICONTROL Journeys]** , cliquez sur le parcours à fermer.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![](assets/finish_drop_down_list.png)

1. Cliquez sur **[!UICONTROL Close to new entrances]** et confirmez dans la boîte de dialogue.

## Arrêt d’un parcours{#stop-journey}

Si vous devez arrêter la progression de tous les individus dans le parcours, vous pouvez l’arrêter. L’arrêt du parcours expire tous les individus du parcours. Toutefois, l’arrêt d’un parcours implique que les personnes qui y sont déjà entrées soient toutes arrêtées dans leur progression. Le parcours est simplement désactivé. Si vous souhaitez mettre fin à un parcours, nous vous recommandons de le fermer.

Une version de parcours arrêtée ne peut pas être redémarrée.

Lorsqu’il est arrêté, l’état du parcours est défini sur **[!UICONTROL Stopped]**.

Vous pouvez arrêter un parcours, par exemple, si un marketeur se rend compte que l’audience ciblée n’est pas la bonne ou qu’une action personnalisée censée diffuser des messages ne fonctionne pas correctement. Pour arrêter un parcours dans la liste, cliquez sur le bouton **[!UICONTROL Ellipsis]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également :

1. Dans le **[!UICONTROL Journeys]** , cliquez sur le parcours que vous souhaitez arrêter.
1. En haut à droite, cliquez sur la flèche vers le bas.
   ![](assets/finish_drop_down_list.png)
1. Cliquez sur **[!UICONTROL Stop]** et confirmez dans la boîte de dialogue.
