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
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 2%

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
* **Planifié** : le défi a été publié et sera automatiquement activé à la date de début spécifiée
* **En direct** : le défi est actuellement actif et les clients peuvent y participer
* **Terminé** : le défi est terminé - la date de fin est dépassée ou tous les objectifs ont été atteints
* **Arrêté** : le défi a été arrêté manuellement avant d’atteindre son achèvement naturel
* **Archivé** : le défi a été archivé à des fins d’organisation et n’est plus visible dans l’inventaire principal

### Modifier les défis {#edit-challenges}

Vous pouvez modifier les défis en fonction de leur statut actuel :

* **Brouillons de défis** : fonctionnalité de modification complète - toutes les propriétés peuvent être modifiées
* **Défis planifiés/en direct** : modification limitée - vous pouvez mettre à jour le contenu, les messages et étendre les dates, mais vous ne pouvez pas modifier la structure de défi principale (type, audience ou définitions de tâche)

Pour modifier un défi :

1. Accédez à l’onglet **[!UICONTROL Défis]** dans l’inventaire des Défis de fidélité.

1. Recherchez le défi à modifier.

1. Sélectionnez le nom du défi pour l’ouvrir en mode d’édition.

1. Apportez vos modifications en fonction du statut du défi :
   * **Brouillons de défis** : modifiez des propriétés, des tâches, du contenu ou des messages
   * **Défis planifiés/en direct** : mettez à jour les cartes de contenu, les messages ou étendez les dates de fin selon les besoins.

1. Enregistrez vos modifications. Pour les défis planifiés ou en direct, les modifications prennent effet immédiatement ou conformément à votre planning de mise à jour.

>[!NOTE]
>
>Pour les modifications nécessitant des modifications majeures (telles que la modification du type de défi, de l’audience ou de la structure de tâche), dupliquez le défi et créez une nouvelle version au lieu de modifier la version existante.

### Dupliquer les défis {#duplicate-challenges}

Dupliquez les défis pour :

* Réexécution des défis réussis pour de nouvelles périodes
* Créer des variations pour différentes audiences
* Mettre à jour les exigences de tâche ou les récompenses
* Réactiver les défis arrêtés ou terminés

La duplication d’un défi crée une copie exacte avec toutes les tâches, le contenu et les messages intacts, ce qui vous permet de créer rapidement de nouvelles versions sans devoir repartir de zéro.

Pour dupliquer un défi :

1. Accédez à l’onglet **[!UICONTROL Défis]** dans l’inventaire des Défis de fidélité.

1. Recherchez le défi à dupliquer.

1. Sélectionnez le menu Autres actions (points de suspension) en regard de ce défi.

1. Choisissez **[!UICONTROL Dupliquer]**.

1. Une copie du défi est créée avec « [ Copy ] » ajouté à son nom.

1. Ouvrez le défi dupliqué et modifiez les propriétés nécessaires :
   * Mettre à jour le nom du défi
   * Ajuster les dates de début et de fin
   * Modifiez l’audience cible si nécessaire.
   * Modifiez les tâches, les récompenses, le contenu ou les messages selon les besoins

1. Examinez et publiez le défi dupliqué.

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

1. Sélectionnez le menu Autres actions (points de suspension) en regard de la tâche.

1. Choisissez **[!UICONTROL Supprimer]**.

1. Confirmez la suppression dans la boîte de dialogue.

>[!NOTE]
>
>Si une tâche est utilisée dans un défi (brouillon, planifié ou actif), vous devez d’abord la supprimer de tous les défis avant de pouvoir la supprimer. Pensez à archiver ou dupliquer les tâches au lieu de les supprimer si vous en avez besoin ultérieurement.
