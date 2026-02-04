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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 2%

---


# Création de tâches {#create-tasks}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité et les gérer](access-loyalty-challenges.md) - Inventaire, défis et gestion des tâches
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* **Créer des tâches** ◀︎ **Vous êtes ici** - Définir des tâches de type Défi

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

Les tâches définissent les actions ou jalons spécifiques que les clients doivent effectuer pour gagner des récompenses dans un défi de fidélité. Vous pouvez configurer les types de tâches, les quantités et les exigences en matière de produits afin de créer des expériences de fidélité attrayantes et personnalisées.

Chaque tâche représente une action mesurable qui contribue à l&#39;achèvement du défi. Les tâches sont des composants réutilisables qui peuvent être créés indépendamment, puis ajoutés à un ou plusieurs défis, ou créés directement au sein d’un défi.

## Création d’une tâche {#create-task}

Vous pouvez créer des tâches à partir de deux points d’entrée. Le processus de configuration est le même, quel que soit l’endroit où vous commencez.

>[!BEGINTABS]

>[!TAB Dans l’inventaire des tâches]

Sélectionnez l’onglet **[!UICONTROL Tâches]** et sélectionnez **[!UICONTROL Créer une tâche]**.

![](assets/task-create-inventory.png)

Les tâches créées à partir de l’inventaire sont enregistrées et disponibles pour réutilisation à travers plusieurs défis.

>[!TAB À partir d’un défi]

Ouvrir un défi existant ou en créer un nouveau. Sélectionnez **[!UICONTROL Ajouter une tâche]** et cliquez sur le bouton **[!UICONTROL Nouveau]**.

![](assets/task-create-challenge.png)

Les tâches créées de cette manière sont automatiquement ajoutées à votre défi et sont également enregistrées dans l’inventaire des tâches pour être réutilisées dans d’autres défis.

>[!ENDTABS]

## Choisir l’activité du client {#choose-activity}

Sélectionnez le type d’activité que les clients doivent effectuer pour terminer cette tâche :

* **[!UICONTROL Achat]** : les clients doivent acheter un ou plusieurs articles pour terminer cette tâche
* **[!UICONTROL Dépenses]** : les clients doivent dépenser un montant spécifié pour terminer cette tâche

Pour sélectionner un type d’activité, cliquez sur l’icône `+` et sélectionnez l’activité du client qui correspond le mieux à vos objectifs de résultat. Chaque type d’activité possède des attributs configurables spécifiques pour définir et définir plus en détail les exigences des tâches.

![](assets/task-create-activitiy.png)

## Définition des attributs {#define-attributes}

Configurez les attributs de tâche en fonction du type d’activité sélectionné :

>[!BEGINTABS]

>[!TAB Activité d’achat]

![](assets/task-create-purchase.png)

Configurez les attributs suivants :

* **[!UICONTROL Quantité]** : saisissez le nombre d’articles à acheter pour terminer cette tâche
* **[!UICONTROL Éléments et exclusions éligibles]** : définissez les éléments ou les groupes d’éléments qui sont pris en compte pour l’achèvement de la tâche, et ceux qui ne le sont pas. En savoir plus sur [définition des éléments et exclusions éligibles](#eligible-items-exclusions)

**Attributs facultatifs** (activé via l’icône des paramètres) :

* **[!UICONTROL Montant minimum de la valeur de dépense]** : définissez une exigence de montant minimum d’achat
* **[!UICONTROL Nombre maximum de transactions]** : limitez le nombre de transactions pouvant être utilisées pour terminer la tâche

>[!TAB Activité de dépense]

![](assets/task-create-spend.png)

Configurez les attributs suivants :

* **[!UICONTROL Montant]** : saisissez le montant total des dépenses requises pour terminer la tâche.
* **[!UICONTROL Nombre maximal de transactions]** : indiquez le nombre de transactions autorisées pour répondre à l’exigence de dépenses. Vous pouvez désactiver cet attribut à partir de l&#39;icône des paramètres si vous ne souhaitez pas limiter le nombre de transactions.
* **[!UICONTROL Éléments et exclusions éligibles]** : (facultatif) définissez les éléments ou groupes d’éléments qui sont pris en compte dans l’achèvement de la tâche et ceux qui ne le sont pas. En savoir plus sur [définition des éléments et exclusions éligibles](#eligible-items-exclusions)

>[!ENDTABS]

## Définir les éléments éligibles et les exclusions {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Pour les activités **Achat** et **Dépenses**, vous pouvez utiliser l’attribut **[!UICONTROL Articles et exclusions éligibles]** pour définir les articles et groupes éligibles et ceux qui sont exclus. Cela vous permet de cibler des produits, des catégories ou des emplacements spécifiques pour vous aligner sur vos objectifs de défi.

Les cas d’utilisation incluent : la limitation d’une tâche de dépense à des catégories de produits spécifiques ou l’exclusion des cartes-cadeaux ou des articles promotionnels du comptage pour l’achèvement de la tâche.

![](assets/tasks-create-eligible.png)

* Pour définir les éléments éligibles, utilisez la section **[!UICONTROL Les achats de tâches éligibles sont limités à ce qui suit]**. Saisissez des ID d’article, des catégories ou des ID de destination spécifiques, séparés par des virgules.

  Exemple : `SKU001, SKU002, CategoryA`

  Saisissez `*` pour que tous les achats soient éligibles (comportement par défaut si vide).

* Pour exclure des éléments de la tâche, utilisez la section **[!UICONTROL Les éléments suivants sont exclus de cette tâche]**. Saisissez des ID d&#39;article, des catégories ou des ID de destination spécifiques qui ne doivent pas être pris en compte pour l&#39;achèvement de la tâche.

  Exemple : `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

  >[!NOTE]
  >
  >Les exclusions ont priorité sur les éléments éligibles. Si un élément correspond à la fois à un élément éligible et à une exclusion, il sera exclu de la tâche.

## Définir les propriétés de la tâche {#define-task-properties}

Dans le volet **[!UICONTROL Propriétés]** de la tâche, configurez les informations de base sur la tâche :

* **[!UICONTROL Nom de la tâche]** : saisissez un nom explicite pour la tâche. Ce nom est visible pour vous et votre équipe, mais peut ne pas être affiché pour les clients selon la conception de votre carte de contenu.
* **[!UICONTROL Description de la tâche]** : la description est générée automatiquement en fonction du type d’activité et des attributs que vous configurez pour la tâche. Vous pouvez désactiver la génération automatique et saisir une description personnalisée si nécessaire.

![](assets/tasks-create-properties.png)

Après avoir configuré tous les attributs et propriétés, sélectionnez **[!UICONTROL Créer]** pour enregistrer la tâche. La tâche est enregistrée dans votre inventaire de tâches et, si elle est créée à partir d’un défi, est automatiquement ajoutée à ce défi.
