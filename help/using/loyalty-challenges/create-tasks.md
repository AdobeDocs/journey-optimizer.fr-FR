---
solution: Journey Optimizer
product: journey optimizer
title: Création de tâches pour les défis de fidélité
description: Découvrez comment créer et configurer des tâches pour les défis de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 2%

---


# Création de tâches {#create-tasks}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité](access-loyalty-challenges.md) - Inventaire et filtrage
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* **Créer des tâches** ◀︎ **Vous êtes ici** - Définir des tâches de type Défi
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Vue d’ensemble {#overview}

Les tâches définissent les actions ou jalons spécifiques que les clients doivent effectuer pour gagner des récompenses dans un défi de fidélité. Vous pouvez configurer les types de tâches, les quantités, les exigences en matière de produits et les valeurs de récompense pour créer des expériences de fidélité attrayantes et personnalisées.

Chaque tâche représente une action mesurable qui contribue à l&#39;achèvement du défi. Les tâches sont des composants réutilisables qui peuvent être créés indépendamment, puis ajoutés à un ou plusieurs défis, ou créés directement au sein d’un défi.

### Fonctionnement des tâches dans différents types de défis {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

Selon votre type de défi (Standard, Séquentiel ou Séquentiel), les clients exécutent les tâches différemment :

* **Défis standard** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre
* **Défis en série** : les clients effectuent la même tâche plusieurs fois de suite
* **Défis séquentiels** : les clients exécutent des tâches dans un ordre défini

## Création d’une tâche {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

Vous pouvez créer des tâches à partir de deux points d’entrée. Le processus de configuration est le même, quel que soit l’endroit où vous commencez.

+++À partir de l’inventaire des tâches

1. Accédez à **[!UICONTROL Défis de fidélité]** dans Journey Optimizer.

1. Sélectionnez l’onglet **[!UICONTROL Tâches]**.

1. Sélectionnez **[!UICONTROL Créer une tâche]**.

Les tâches créées à partir de l’inventaire sont enregistrées et disponibles pour réutilisation à travers plusieurs défis.

+++

+++À partir d’un défi

1. Ouvrir un défi existant ou en créer un nouveau.

1. Accédez à la section **[!UICONTROL Tâches]**.

1. Sélectionnez **[!UICONTROL Ajouter une tâche]** puis choisissez **[!UICONTROL Créer une tâche]**.

Les tâches créées de cette manière sont automatiquement ajoutées à votre défi et sont également enregistrées dans l’inventaire des tâches pour être réutilisées dans d’autres défis.

+++

### Définir les propriétés de la tâche {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

Configurez les informations de base sur la tâche :

* **Nom de la tâche** : saisissez un nom explicite pour la tâche. Ce nom est visible pour vous et votre équipe, mais peut ne pas être affiché pour les clients selon la conception de votre carte de contenu.
* **Description de la tâche** : (facultatif) ajoutez des détails sur l’objectif ou les exigences de la tâche.

### Choisir l’activité du client {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

Sélectionnez le type d’activité client que les clients doivent effectuer pour terminer cette tâche :

* **[!UICONTROL Achat]** : les clients doivent acheter un ou plusieurs articles pour terminer cette tâche
* **[!UICONTROL Dépenses]** : les clients doivent dépenser un montant spécifié pour terminer cette tâche

Sélectionnez l’activité du client qui correspond le mieux à vos objectifs de résultat. Chaque type d’activité possède des attributs configurables spécifiques pour définir et définir plus en détail les exigences des tâches.

### Définition des attributs {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

Configurez les attributs de tâche en fonction du type d’activité sélectionné :

+++Pour l’activité d’achat

Configurez les attributs suivants :

* **Quantité** : saisissez le nombre d’articles à acheter pour terminer cette tâche
* **Éléments et exclusions éligibles** : définissez les éléments ou les groupes d’éléments qui sont pris en compte pour l’achèvement de la tâche, et ceux qui ne le sont pas. En savoir plus sur [définition des éléments et exclusions éligibles](#eligible-items-exclusions)

**Attributs facultatifs** (configurez-les à l’aide de l’icône paramètres) :

* **Montant minimum de la valeur de dépense** : définissez une exigence de montant minimum d’achat
* **Nombre maximum de transactions** : limitez le nombre de transactions pouvant être utilisées pour terminer la tâche

+++

+++Pour l’activité de dépenses

Configurez les attributs suivants :

* **Montant** : saisissez le montant total des dépenses requises pour terminer la tâche
* **Nombre maximal de transactions** : indiquez le nombre de transactions autorisées pour répondre à l’exigence de dépenses. Vous pouvez désactiver cet attribut à partir de l&#39;icône des paramètres si vous ne souhaitez pas limiter le nombre de transactions
* **Éléments et exclusions éligibles** : (facultatif) définissez les éléments ou groupes d’éléments qui sont pris en compte dans l’achèvement de la tâche et ceux qui ne le sont pas. En savoir plus sur [définition des éléments et exclusions éligibles](#eligible-items-exclusions)

+++

Après avoir configuré tous les attributs, sélectionnez **[!UICONTROL Créer]** pour enregistrer la tâche. La tâche est enregistrée dans votre inventaire de tâches et, si elle est créée à partir d’un défi, est automatiquement ajoutée à ce défi.

## Définir les éléments éligibles et les exclusions {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Pour les activités Achat et Dépenses, vous pouvez définir des articles et des groupes éligibles et également exclure des articles et des groupes. Cela vous permet de cibler des produits, des catégories ou des emplacements spécifiques pour vous aligner sur vos objectifs de défi.

**Cas d’utilisation :**

* Créez une tâche qui récompense les clients pour leurs achats de café mais exclut les produits de dédouanement
* Limiter une tâche de dépense à des catégories de produits spécifiques
* Exclure les cartes-cadeaux ou les articles promotionnels du comptage pour terminer la tâche

### Configuration des éléments éligibles {#configure-eligible-items}

Pour définir les éléments éligibles, utilisez la section **[!UICONTROL Les achats de tâches éligibles sont limités à ce qui suit]** :

* Saisissez des ID d’article, des catégories ou des ID de destination spécifiques, séparés par des virgules
* Exemple : `SKU001, SKU002, CategoryA, StoreLocation123`
* **Conseil** : saisissez la `*` pour rendre tous les achats éligibles (comportement par défaut si vide)

### Configurer les exclusions {#configure-exclusions}

Pour exclure des éléments de la tâche, utilisez la section **[!UICONTROL Les éléments suivants sont exclus de cette tâche]** :

* Saisissez des ID d&#39;article, des catégories ou des ID de destination spécifiques qui ne doivent pas être pris en compte pour l&#39;achèvement de la tâche
* Exemple : `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* Exclusions courantes : articles de vente ou de dédouanement, cartes-cadeaux, articles promotionnels

>[!NOTE]
>
>Les exclusions ont priorité sur les éléments éligibles. Si un élément correspond à la fois à un élément éligible et à une exclusion, il sera exclu de la tâche.

## Étapes suivantes {#next-steps}

Maintenant que vous savez comment créer et configurer des tâches :

* [Créer des défis](create-challenges.md) - Découvrez comment créer des défis complets et configurer des récompenses
* [Gérer les défis](manage-challenges.md) - Découvrez comment modifier, surveiller et optimiser les défis
