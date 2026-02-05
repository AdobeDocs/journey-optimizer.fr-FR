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
mini-toc-levels: 1
source-git-commit: 342df0950622de1c4c246bf624d05843671e199f
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---


# Création de tâches {#create-tasks}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md)
* [Accéder aux défis et aux tâches et les gérer](access-loyalty-challenges.md)
* [Créer des défis](create-challenges.md)
* **Créer des tâches** ◀︎ **Vous êtes ici**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **privée**. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

Les tâches définissent les actions ou jalons spécifiques que les clients doivent effectuer pour gagner des récompenses dans un défi de fidélité. Vous pouvez configurer les types de tâches, les quantités et les exigences en matière de produits afin de créer des expériences de fidélité attrayantes et personnalisées.

Chaque tâche représente une action mesurable qui contribue à l&#39;achèvement du défi. Les tâches sont des composants réutilisables qui peuvent être créés indépendamment, puis ajoutés à un ou plusieurs défis, ou créés directement au sein d’un défi.

## Création d’une tâche {#create-task}

Vous pouvez créer des tâches à partir de deux points d’entrée. Le processus de configuration est le même, quel que soit l’endroit où vous commencez.

>[!BEGINTABS]

>[!TAB Dans l’inventaire des tâches]

Sélectionnez l’onglet **[!UICONTROL Tâches]** et sélectionnez **[!UICONTROL Créer une tâche]**. Les tâches créées à partir de l’inventaire sont enregistrées et disponibles pour réutilisation à travers plusieurs défis.

![](assets/task-create-inventory.png)

>[!TAB À partir d’un défi]

Ouvrir un défi existant ou en créer un nouveau. Sélectionnez **[!UICONTROL Ajouter une tâche]** et cliquez sur le bouton **[!UICONTROL Nouveau]**. Les tâches créées de cette manière sont automatiquement ajoutées à votre défi et sont également enregistrées dans l’inventaire des tâches pour être réutilisées dans d’autres défis.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Choisir l’activité du client {#choose-activity}

Sélectionnez le type d’activité que les clients doivent effectuer pour terminer cette tâche :

* **[!UICONTROL Achat]** : les clients doivent acheter un ou plusieurs articles pour terminer cette tâche
* **[!UICONTROL Dépenses]** : les clients doivent dépenser un montant spécifié pour terminer cette tâche

Pour sélectionner une activité, cliquez sur l’icône **+** et sélectionnez l’activité du client qui correspond le mieux à vos objectifs de résultat. Chaque type d’activité possède des attributs configurables spécifiques pour définir et définir plus en détail les exigences des tâches.
![](assets/task-create-activity.png)

## Définir les attributs de la tâche {#define-attributes}

Configurez les attributs de la tâche en fonction du type d’activité sélectionné. Parcourez les onglets ci-dessous pour afficher les attributs disponibles pour chaque type d’activité :

>[!BEGINTABS]

>[!TAB Activité d’achat]

Attributs disponibles pour les activités **Achat** :

* **[!UICONTROL Quantité]** : saisissez le nombre d’articles qui doivent être achetés pour terminer cette tâche.
* **[!UICONTROL Éléments et exclusions éligibles]** : définissez les éléments ou les groupes d’éléments qui sont pris en compte pour l’achèvement de la tâche, et ceux qui ne le sont pas. [En savoir plus sur les éléments et exclusions éligibles](#eligible-items-exclusions)
* **[!UICONTROL Montant minimum de la valeur de dépense]** : définissez une exigence de montant minimum d’achat.
* **[!UICONTROL Nombre maximum de transactions]** : limitez le nombre de transactions pouvant être utilisées pour terminer la tâche.

![](assets/task-create-purchase.png)

>[!TAB Activité de dépense]

Attributs disponibles pour les activités **Dépenses** :

* **[!UICONTROL Montant]** : saisissez le montant total des dépenses requises pour terminer la tâche.
* **[!UICONTROL Éléments et exclusions éligibles]** : définissez les éléments ou les groupes d’éléments qui sont pris en compte pour l’achèvement de la tâche, et ceux qui ne le sont pas. [En savoir plus sur les éléments et exclusions éligibles](#eligible-items-exclusions)
* **[!UICONTROL Nombre maximal de transactions]** : indiquez le nombre de transactions autorisées pour répondre à l’exigence de dépenses. Vous pouvez activer cet attribut à partir de l’icône des paramètres.

![](assets/task-create-spend.png)

>[!ENDTABS]

## Définir les éléments éligibles et les exclusions {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Pour les activités **Achat** et **Dépenses**, vous pouvez utiliser l’attribut **[!UICONTROL Articles et exclusions éligibles]** pour définir les articles et groupes éligibles et ceux qui sont exclus. Cela vous permet de cibler des produits, des catégories ou des emplacements spécifiques pour vous aligner sur vos objectifs de défi.

Par exemple, vous pouvez limiter une tâche de dépense à des catégories de produits spécifiques ou exclure les cartes-cadeaux ou les articles promotionnels du comptage pour terminer la tâche.

![](assets/tasks-create-eligible.png)

* Pour définir des articles éligibles, saisissez des ID d’article, des catégories ou des ID de destination spécifiques, séparés par des virgules dans le champ **[!UICONTROL Les achats de tâches éligibles sont limités à ce qui suit]**. Si vous laissez ce champ vide, tous les achats sont éligibles par défaut. Vous pouvez également saisir des `*` pour rendre explicitement tous les achats éligibles.

  Exemple : `SKU001, SKU002, CategoryA`

* Pour exclure des éléments de la tâche, saisissez des ID d’élément, des catégories ou des ID de destination spécifiques dans le champ **[!UICONTROL Les éléments suivants sont exclus de cette tâche]**.

  Exemple : `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## Définir les propriétés de la tâche {#define-task-properties}

Dans le volet **[!UICONTROL Propriétés]** de la tâche, configurez les informations de base sur la tâche :

* **[!UICONTROL Nom de la tâche]** : saisissez un nom explicite pour la tâche.
* **[!UICONTROL Description de la tâche]** : la description est générée automatiquement en fonction de l’activité et des attributs configurés. Pour saisir une description personnalisée, désactivez l’option de génération automatique et saisissez la description dans le champ de texte.

![](assets/tasks-create-properties.png)

Après avoir configuré tous les attributs et propriétés, sélectionnez **[!UICONTROL Créer]** pour enregistrer la tâche. La tâche est enregistrée dans votre inventaire de tâches et, si elle est créée à partir d’un défi, est automatiquement ajoutée à ce défi.
