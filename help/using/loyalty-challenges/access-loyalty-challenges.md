---
solution: Journey Optimizer
product: journey optimizer
title: Accès aux défis de fidélité
description: Découvrez comment accéder, rechercher et filtrer les défis de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 3%

---


# Accès aux défis de fidélité {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* **Accéder aux défis de fidélité** ◀︎ **Vous êtes ici** - Inventaire et filtrage
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Créer des tâches](create-tasks.md) - Définir des tâches de défi
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Accès à l’inventaire des défis de fidélité {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

Pour accéder aux défis de fidélité, accédez à Journey Optimizer et sélectionnez **[!UICONTROL Défis de fidélité]** dans la section **[!UICONTROL parcours clients]**.

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

La page Défis de fidélité s’affiche avec deux onglets :

* **[!UICONTROL Défis]** : affichez et gérez tous les défis de fidélité

* **[!UICONTROL Tâches]** : affichez et gérez toutes les tâches qui peuvent être réutilisées à travers les défis

## Inventaire des défis {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

L’onglet Défis affiche tous les défis triés par date de dernière modification, les défis modifiés le plus récemment apparaissant en premier. Les informations affichées sont alors les suivantes :

* **[!UICONTROL Nom du défi]** : nom que vous avez attribué au défi
* **[!UICONTROL Statut]** : état actuel du défi (voir les descriptions de statut ci-dessous)
* **[!UICONTROL Type]** : type de défi (standard, en traînée ou séquentiel)
* **[!UICONTROL Date de début]** : date à laquelle le défi devient actif
* **[!UICONTROL Date de fin]** : date d’expiration du défi
* **[!UICONTROL Créé par]** : utilisateur qui a créé le défi
* **[!UICONTROL Dernière modification]** : date et heure de la dernière modification
* **[!UICONTROL Balises]** : toutes les balises appliquées au défi pour l’organisation

### Statuts des défis {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

Les défis s’affichent avec différents statuts indiquant leur statut actuel dans le cycle de vie :

* **Brouillon** : le défi est en cours de création ou de modification.
* **Planifié** : le défi est publié et sera actif à la date de début
* **En direct** : le défi est actif et les clients peuvent y participer
* **Terminé** : la date de fin du défi est dépassée ou les objectifs ont été atteints
* **Arrêté** : le défi a été arrêté manuellement avant la fin
* **Archivé** : le défi a été archivé à des fins d’organisation

Pour plus d’informations sur les transitions d’état et le cycle de vie du défi, voir [Cycle de vie du défi](manage-challenges.md#challenge-lifecycle).

### Défis liés à la recherche et au filtrage {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

Vous pouvez rapidement localiser les défis à l’aide de la recherche et des filtres :

**Rechercher:**

* Utilisez la barre de recherche pour trouver les défis en saisissant des mots-clés à partir du nom ou de la description du défi. Les mises à jour de la recherche génèrent des résultats en temps réel au fur et à mesure que vous tapez.

**Filtres:**

* Appliquez un ou plusieurs filtres pour affiner vos résultats :
   * **Statut** : filtrer par statut de défi (brouillon, planifié, actif, terminé, arrêté, archivé)
   * **Type** : filtrer par type de défi (Standard, Séquentiel, Séquentiel)
   * **Dates** : filtrez par périodes de début ou de fin.
   * **Balises** : filtrer par balises appliquées aux défis

Vous pouvez combiner plusieurs filtres simultanément. Par exemple, filtrez les défis Live Standard identifiés avec « Été 2024 » pour trouver rapidement les campagnes saisonnières actives.

Pour effacer les filtres, sélectionnez **[!UICONTROL Effacer tout]** ou supprimez des filtres individuels.

### Prendre des mesures pour relever les défis {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

Dans l’onglet Défis , vous pouvez effectuer des actions rapides sur les défis :

* **Afficher les détails du défi** : sélectionnez le nom du défi pour ouvrir sa page de détails
* **Modifier un défi** : sélectionnez le menu **[!UICONTROL Plus d’actions]** (trois points) et choisissez **[!UICONTROL Modifier]**
* **Dupliquer un défi** : sélectionnez le menu **[!UICONTROL Autres actions]** et choisissez **[!UICONTROL Dupliquer]**
* **Arrêter un défi en direct** : sélectionnez le menu **[!UICONTROL Autres actions]** et choisissez **[!UICONTROL Arrêter]**
* **Archiver un défi** : sélectionnez le menu **[!UICONTROL Autres actions]** et choisissez **[!UICONTROL Archiver]**
* **Supprimer un brouillon de défi** : sélectionnez le menu **[!UICONTROL Autres actions]** et choisissez **[!UICONTROL Supprimer]** (disponible uniquement pour les brouillons).

Pour plus d’informations sur la gestion des défis après leur création, notamment la modification des limites, les stratégies de duplication, la surveillance des performances et le dépannage, consultez [Gérer les défis](manage-challenges.md).

## Inventaire des tâches {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

L’onglet Tâches affiche toutes les tâches réutilisables qui peuvent être utilisées pour plusieurs défis. Les tâches créées ici peuvent être sélectionnées lors de la création ou de la modification d’un défi.

L&#39;inventaire des tâches affiche les informations suivantes :

* **[!UICONTROL Nom de la tâche]** : nom que vous avez attribué à la tâche
* **[!UICONTROL Type de tâche]** : type d’action (achat, montant des dépenses, visite, engagement, événement personnalisé)
* **[!UICONTROL Description]** : brève description de ce que la tâche requiert
* **[!UICONTROL Créé par]** : utilisateur qui a créé la tâche.
* **[!UICONTROL Dernière modification]** : date et heure de la dernière modification
* **[!UICONTROL Utilisé dans les défis]** : nombre de défis utilisant actuellement cette tâche

### Agir sur les tâches {#tasks-actions}

Dans l’onglet Tâches , vous pouvez effectuer des actions sur les tâches :

* **Afficher les détails de la tâche** : sélectionnez le nom de la tâche pour afficher la configuration complète
* **Modifier une tâche** : sélectionnez le menu **[!UICONTROL Autres actions]** (points de suspension) et choisissez **[!UICONTROL Modifier]**
* **Dupliquer une tâche** : sélectionnez le menu **[!UICONTROL Autres actions]** et choisissez **[!UICONTROL Dupliquer]**
* **Supprimer une tâche** : sélectionnez le menu **[!UICONTROL Autres actions]** et choisissez **[!UICONTROL Supprimer]** (uniquement si elle n’est utilisée dans aucun défi actif)
* **Afficher l’utilisation** : voir quels défis utilisent actuellement la tâche.

## Étapes suivantes {#next-steps}

Maintenant que vous savez comment accéder à l’inventaire des défis de fidélité et naviguer dans celui-ci :

* [Créer des défis](create-challenges.md) - Découvrez comment créer votre premier défi et configurer des tâches
* [Créer des tâches](create-tasks.md) - Découvrez comment définir des tâches réutilisables pour les défis
* [Gérer les défis](manage-challenges.md) - Découvrez comment modifier, surveiller et optimiser les défis
