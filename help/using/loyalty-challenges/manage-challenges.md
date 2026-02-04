---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des défis de fidélité
description: Découvrez comment gérer, surveiller et optimiser les défis de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 3%

---


# Gestion des défis {#manage-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité](access-loyalty-challenges.md) - Inventaire et filtrage
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Créer des tâches](create-tasks.md) - Définir des tâches de défi
* **Gérer les défis** ◀︎ **Vous êtes ici** - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Gestion des défis {#manage-challenges-section}

### Cycle de vie du défi {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

Les défis passent par différents états au cours de leur cycle de vie :

* **Brouillon** : le défi est en cours de création ou de modification et n’est pas encore disponible pour les clients
* **Publié** : le défi est actif, le parcours associé a été créé.

### Modifier les défis {#edit-challenges}

Vous pouvez modifier les défis en les ouvrant dans l’inventaire des défis. Le comportement de modification diffère en fonction du statut du défi :

**Brouillons des défis** : vous disposez d’une fonctionnalité d’édition complète. Toutes les propriétés, tâches, contenus et messages peuvent être modifiés sans restriction.

**Défis publiés** : lorsque vous ouvrez un défi publié pour le modifier, vous devez d’abord le rétablir au statut Brouillon.

* Toutes les personnalisations apportées directement au parcours généré automatiquement seront perdues
* Le défi revient à l’état Brouillon .
* Après avoir apporté vos modifications, vous devez enregistrer et publier à nouveau le défi
* Vous devez réactiver le parcours associé pour que les clients puissent accéder au défi mis à jour

>[!IMPORTANT]
>
>La restauration d’un défi publié en version préliminaire ne peut pas être annulée. Tenez compte de l’impact sur votre parcours actif avant de continuer.

### Dupliquer les défis {#duplicate-challenges}

La duplication d’un défi crée une copie exacte avec toutes les tâches, le contenu et les messages intacts, ce qui vous permet de créer rapidement de nouvelles versions sans devoir repartir de zéro.

Pour dupliquer un défi :

1. Accédez à l’onglet **[!UICONTROL Défis]** et localisez le défi à dupliquer.

1. Sélectionnez l’icône ![](assets/do-not-localize/Smock_More_18_N.svg) en regard de ce défi et choisissez **[!UICONTROL Dupliquer]**.

1. Une copie du défi est créée. Ouvrez le défi dupliqué et modifiez les propriétés nécessaires.

1. Enregistrez le défi dupliqué et générez le parcours associé.

### Surveillance des performances {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

Suivez les performances des défis au moyen des mesures clés :

* **Mesures de participation** :
   * Inscription : nombre de clients ayant rejoint le défi
   * Participants actifs : clients actuellement engagés dans ce défi
* **Mesures d’achèvement** :
   * Taux d’achèvement : pourcentage de clients inscrits qui ont terminé le défi
   * Durée moyenne d’achèvement : temps moyen nécessaire pour terminer toutes les tâches
* **Mesures de récompense** :
   * Récompenses totales distribuées : valeur agrégée de toutes les récompenses accordées
   * Récompenses par type : répartition des récompenses par catégorie de récompense
* **Mesures d’engagement** :
   * Impressions sur les cartes de contenu : nombre de fois où des cartes de contenu de défi ont été affichées
   * Diffusion des messages : nombre de messages envoyés avec succès sur tous les canaux

Pour accéder aux données de performances :

1. Accédez à l’onglet **[!UICONTROL Défis]** dans l’inventaire des Défis de fidélité.

1. Sélectionnez le défi que vous souhaitez surveiller.

1. Ouvrez l’onglet **[!UICONTROL Performances]** pour afficher les mesures et les analyses en temps réel.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

Vous pouvez également accéder à des données de performances détaillées dans les [rapports de parcours générés automatiquement](../reports/journey-global-report-cja.md), qui fournissent des informations supplémentaires et des tendances historiques.

## Gestion des tâches {#manage-tasks}

Les tâches sont des composants réutilisables qui peuvent être utilisés pour plusieurs défis. La gestion efficace des tâches garantit la cohérence de votre programme de fidélité et facilite la mise à jour centralisée des définitions de tâche. Les tâches créées dans un défi peuvent être réutilisées dans d’autres défis, ce qui réduit la duplication et maintient la normalisation.

### Modifier les tâches {#edit-tasks}

Vous pouvez modifier des tâches existantes à partir de l’inventaire des tâches. Tenez compte des points suivants :

* **Tâches non utilisées dans les défis actifs** : peuvent être modifiées librement - toutes les propriétés peuvent être modifiées sans impact
* **Tâches utilisées dans les défis en direct** : faites preuve de prudence, car les modifications affectent tous les défis utilisant la tâche. Les modifications s’appliquent immédiatement à tous les défis de référencement

Pour modifier une tâche :

1. Accédez à l’onglet **[!UICONTROL Tâches]** dans l’inventaire des défis de fidélité.

1. Recherchez la tâche à modifier.

1. Sélectionnez le nom de la tâche pour l’ouvrir en mode d’édition.

1. Modifiez les propriétés de la tâche selon les besoins :
   * Mettre à jour le nom ou la description de la tâche
   * Modifier le type d’activité ou les attributs
   * Ajuster les éléments éligibles et les exclusions
   * Modifier les besoins en quantité ou en montant

1. Enregistrez vos modifications.

>[!WARNING]
>
>Lors de la modification d’une tâche qui est activement utilisée dans les défis en direct, pensez à créer un doublon avec une nouvelle version plutôt que de modifier l’original. Cela empêche les modifications involontaires apportées aux défis actifs et vous permet de tester les modifications avant de les appliquer.

### Supprimer les tâches {#delete-tasks}

Les tâches ne peuvent être supprimées que si elles ne sont actuellement utilisées dans aucun défi. Avant de supprimer une tâche :

* Vérifiez le nombre **[!UICONTROL Utilisé dans les défis]** dans l’inventaire des tâches
* Assurez-vous qu’aucun défi en version brouillon, planifié ou actif ne référence la tâche

Pour supprimer une tâche :

1. Accédez à l’onglet **[!UICONTROL Tâches]** dans l’inventaire des défis de fidélité.

1. Recherchez la tâche à supprimer.

1. Vérifiez que le nombre **[!UICONTROL Utilisé dans les défis]** indique 0. Si le nombre est supérieur à 0, vous devez d’abord supprimer la tâche de tous les défis avant la suppression.

1. Sélectionnez l’icône ![](assets/do-not-localize/Smock_More_18_N.svg) en regard de la tâche.

1. Choisissez **[!UICONTROL Supprimer]**.

1. Confirmez la suppression dans la boîte de dialogue.

>[!NOTE]
>
>Si une tâche est utilisée dans un défi (brouillon, planifié ou actif), vous devez d’abord la supprimer de tous les défis avant de pouvoir la supprimer. Pensez à archiver ou dupliquer les tâches au lieu de les supprimer si vous en avez besoin ultérieurement.
