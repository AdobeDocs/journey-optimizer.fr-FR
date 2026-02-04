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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Accès aux défis de fidélité {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* **Accéder aux défis de fidélité** ◀︎ **Vous êtes ici** - Inventaire et filtrage
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

## Accès à l’inventaire des défis de fidélité {#access-inventory}

Pour accéder aux défis de fidélité :

1. Dans Adobe Journey Optimizer, sélectionnez **[!UICONTROL Défis de fidélité]** dans le menu de navigation de gauche sous la section **[!UICONTROL parcours clients]**.

2. La page Défis de fidélité s’affiche avec deux onglets :
   * **[!UICONTROL Défis]** : affichez et gérez tous les défis de fidélité
   * **[!UICONTROL Tâches]** : affichez et gérez toutes les tâches qui peuvent être réutilisées à travers les défis

Par défaut, l’onglet **[!UICONTROL Défis]** est sélectionné, affichant tous les défis existants de votre organisation.

## Onglet Défis {#challenges-tab}

L’onglet Défis affiche tous les défis triés par date de dernière modification, les défis modifiés le plus récemment apparaissant en premier.

### Comprendre l’inventaire des défis {#inventory-overview}

L’inventaire des défis affiche tous les défis avec les informations suivantes :

* **[!UICONTROL Nom du défi]** : nom que vous avez attribué au défi
* **[!UICONTROL Statut]** : état actuel du défi (voir les descriptions de statut ci-dessous)
* **[!UICONTROL Type]** : type de défi (standard, en traînée ou séquentiel)
* **[!UICONTROL Date de début]** : date à laquelle le défi devient actif
* **[!UICONTROL Date de fin]** : date d’expiration du défi
* **[!UICONTROL Créé par]** : utilisateur qui a créé le défi
* **[!UICONTROL Dernière modification]** : date et heure de la dernière modification
* **[!UICONTROL Balises]** : toutes les balises appliquées au défi pour l’organisation

### Statuts des défis {#challenge-statuses}

Les défis peuvent avoir les statuts suivants :

* **[!UICONTROL Brouillon]** : le défi est en cours de création ou de modification, mais pas encore publié.
* **[!UICONTROL Planifié]** : le défi est publié et doit commencer à une date ultérieure
* **[!UICONTROL En direct]** : le défi est actuellement actif et disponible pour le public cible
* **[!UICONTROL Terminé]** : le défi a dépassé sa date de fin ou tous les objectifs ont été atteints
* **[!UICONTROL Arrêté]** : le défi a été arrêté manuellement avant la fin
* **[!UICONTROL Archivé]** : le défi a été archivé à des fins d’organisation

### Défis liés à la recherche et au filtrage {#search-challenges}

Utilisez la fonctionnalité de recherche pour rechercher rapidement des défis spécifiques par nom ou description.

Vous pouvez également appliquer des filtres pour réduire la liste des défis en fonction de critères spécifiques. Vous pouvez combiner plusieurs filtres pour affiner votre recherche.

Vous pouvez filtrer les défis par statut actuel, par type de défi, en fonction de leurs dates de début ou de fin, ou par balises que vous avez appliquées à l’organisation.

### Prendre des mesures pour relever les défis {#inventory-actions}

Dans l’onglet Défis , vous pouvez effectuer des actions rapides sur les défis :

* **Afficher les détails du défi** : sélectionnez un nom de défi pour ouvrir sa page de détails
* **Modifier un défi** : sélectionnez le menu Autres actions (points de suspension) et choisissez **[!UICONTROL Modifier]**
* **Dupliquer un défi** : sélectionnez le menu Plus d’actions et choisissez **[!UICONTROL Dupliquer]**
* **Arrêter un défi en direct** : sélectionnez le menu Autres actions et choisissez **[!UICONTROL Arrêter]**
* **Archiver un défi** : sélectionnez le menu Autres actions et choisissez **[!UICONTROL Archiver]**
* **Supprimer un brouillon de défi** : sélectionnez le menu Autres actions et choisissez **[!UICONTROL Supprimer]** (disponible uniquement pour les brouillons).

### Créer un nouveau défi {#create-from-inventory}

Pour créer un nouveau défi à partir de l’onglet Défis :

1. Sélectionnez **[!UICONTROL Créer un défi]** dans le coin supérieur droit.

2. Le workflow de création de défi démarre.

Pour obtenir des instructions détaillées, voir [Créer des défis](create-challenges.md).

## Onglet Tâches {#tasks-tab}

L’onglet Tâches affiche toutes les tâches réutilisables qui peuvent être utilisées pour plusieurs défis. Les tâches créées ici peuvent être sélectionnées lors de la création ou de la modification d’un défi.

### Présentation de l’inventaire des tâches {#tasks-inventory-overview}

L&#39;inventaire des tâches affiche toutes les tâches avec les informations suivantes :

* **[!UICONTROL Nom de la tâche]** : nom que vous avez attribué à la tâche
* **[!UICONTROL Type de tâche]** : type d’action (achat, montant des dépenses, visite, engagement, événement personnalisé)
* **[!UICONTROL Description]** : brève description de ce que la tâche requiert
* **[!UICONTROL Créé par]** : utilisateur qui a créé la tâche.
* **[!UICONTROL Dernière modification]** : date et heure de la dernière modification
* **[!UICONTROL Utilisé dans les défis]** : nombre de défis utilisant actuellement cette tâche

### Créer des tâches à partir de l’onglet Tâches {#create-tasks-from-tab}

Vous pouvez créer des tâches de deux manières :

1. **Dans l’onglet Tâches** (recommandé pour les tâches réutilisables) :
   * Accédez à l’onglet **[!UICONTROL Tâches]**
   * Sélectionnez **[!UICONTROL Créer une tâche]**
   * Configurer les propriétés de la tâche (nom, type, quantité, filtres de produit, récompenses)
   * Enregistrez la tâche pour la rendre disponible pour une utilisation dans n’importe quel défi

2. **Lors de la création d’un défi** (pour les tâches spécifiques à un défi) :
   * Lors de la création du défi, sélectionnez **[!UICONTROL Ajouter une tâche]** dans la section Tâches
   * Choisissez **[!UICONTROL Créer une tâche]** ou sélectionnez une tâche existante
   * Les tâches ainsi créées sont également enregistrées dans l’inventaire des tâches et peuvent être réutilisées

>[!TIP]
>
>Il est recommandé de créer des tâches à partir de l’onglet Tâches lorsque vous prévoyez d’utiliser la même tâche pour plusieurs défis. Cela garantit la cohérence et facilite la mise à jour centralisée des définitions de tâche.

### Agir sur les tâches {#tasks-actions}

Dans l’onglet Tâches , vous pouvez effectuer des actions sur les tâches :

* **Afficher les détails de la tâche** : sélectionnez un nom de tâche pour afficher la configuration complète
* **Modifier une tâche** : sélectionnez le menu Autres actions (points de suspension) et choisissez **[!UICONTROL Modifier]**
* **Dupliquer une tâche** : sélectionnez le menu Autres actions et choisissez **[!UICONTROL Dupliquer]**
* **Supprimer une tâche** : sélectionnez le menu Plus d’actions et choisissez **[!UICONTROL Supprimer]** (uniquement si elle n’est utilisée dans aucun défi actif)
* **Afficher l’utilisation** : voir quels défis utilisent actuellement la tâche.

## Étapes suivantes {#next-steps}

Maintenant que vous savez comment accéder à l’inventaire des défis de fidélité et naviguer dans celui-ci :

* [Créer des défis](create-challenges.md) - Découvrez comment créer votre premier défi
* [Gérer les défis](manage-challenges.md) - Découvrez comment modifier et surveiller les défis
