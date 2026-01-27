---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des filtres prédéfinis
description: Découvrez comment enregistrer, appliquer et gérer des filtres prédéfinis dans des campagnes orchestrées
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# Utiliser des filtres prédéfinis {#predefined-filters}

Les filtres prédéfinis sont des règles enregistrées que vous pouvez réutiliser dans le créateur de règles. Utilisez-les pour éviter de reconstruire des requêtes courantes et pour normaliser la logique de ciblage sur les campagnes orchestrées.

Vous pouvez marquer les filtres prédéfinis comme favoris, les partager avec d’autres utilisateurs et ajouter des paramètres afin que les champs sélectionnés puissent être modifiés lorsque le filtre est appliqué.

## Créer un filtre prédéfini {#create}

Enregistrez un filtre personnalisé à partir du créateur de règles pour le rendre disponible pour une utilisation ultérieure. Procédez comme suit :

1. Ouvrez le créateur de règles et définissez vos conditions de filtrage. [Découvrir comment créer une règle](../orchestrated/build-query.md)

1. Facultatif : pour rendre certains champs modifiables lors de l’utilisation du filtre, sélectionnez le champ et activez **[!UICONTROL Définir en tant que paramètre]**. Lorsque vous appliquez le filtre, seuls ces champs peuvent être modifiés.

   ![](assets/predefined-filter-parameter-enable.png)

1. Pour enregistrer le filtre, cliquez sur **[!UICONTROL Sélectionner ou enregistrer le filtre]**, puis sélectionnez **[!UICONTROL Enregistrer comme filtre]**.

   ![](assets/predefined-filter-save.png)

1. Saisissez un libellé et une description pour le filtre, puis cliquez sur **[!UICONTROL Enregistrer]**.

   * Pour enregistrer le filtre en tant que favori, activez l’option **[!UICONTROL Filtre favori]**. En savoir plus dans [cette section](#fav-filter).
   * Pour rendre le filtre accessible aux autres utilisateurs, activez l’option **[!UICONTROL Filtre partagé]**. En savoir plus dans [cette section](#share-filter).

   ![](assets/predefined-filter-save-name.png)

Votre filtre personnalisé est désormais disponible dans la liste **Filtres prédéfinis**.

## Utilisation d’un filtre prédéfini dans une règle {#apply}

Les filtres prédéfinis sont disponibles lors de la définition de requêtes dans le créateur de règles.

1. Dans le volet **[!UICONTROL Propriétés des règles]**, cliquez sur **[!UICONTROL Sélectionner ou enregistrer le filtre]**.

1. Choisissez **[!UICONTROL Sélectionner un filtre prédéfini]** et sélectionnez un filtre. Vous pouvez également sélectionner directement un filtre prédéfini dans la liste s’il a été ajouté aux favoris.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >La sélection d’un filtre prédéfini remplace la règle qui a été créée dans la zone de travail par le filtre sélectionné.

1. Le filtre s’ouvre dans la zone de travail. Continuez à modifier la condition si nécessaire.

   ![](assets/predefined-filter-added.png)

   Si le filtre que vous avez sélectionné contient des paramètres, seuls les champs marqués comme paramètres peuvent être modifiés. Elles s’affichent dans le volet en regard du volet **[!UICONTROL Propriétés des règles]**.

   ![](assets/predefined-filter-parameter-apply.png)

   Pour modifier le filtre prédéfini lui-même, cliquez sur le bouton ![points de suspension](assets/do-not-localize/rule-builder-icon-more.svg) et sélectionnez **[!UICONTROL Basculer vers l’édition de règles]**. Toutes les modifications s’appliquent uniquement à la règle en cours de création. Le filtre prédéfini n’est pas modifié.

   ![](assets/predefined-filter-parameter-edit.png)

## Enregistrer un filtre comme favori {#fav-filter}

Lors de la création d’un filtre prédéfini, activez l’option **[!UICONTROL Filtre des favoris]** pour afficher ce filtre prédéfini dans vos favoris.

Lorsqu’un filtre est enregistré en tant que favori, il apparaît dans la section **[!UICONTROL Filtres favoris]** de la liste des filtres, comme illustré ci-dessous :

![Section Filtres favoris](assets/predefined-filter-favorites.png)

## Partage d’un filtre prédéfini {#share-filter}

Par défaut, les filtres prédéfinis que vous créez sont privés et visibles uniquement par vous. Pour rendre un filtre accessible aux autres opérateurs et opératrices de votre organisation, activez l’option **[!UICONTROL Filtre partagé]**.

![Option de filtre partagé](assets/predefined-filter-shared.png)

Les filtres partagés apparaissent dans la liste des filtres prédéfinis pour tous les utilisateurs et utilisatrices, ce qui leur permet d’utiliser ces filtres dans leurs propres règles.

## Gestion des filtres prédéfinis {#manage-predefined-filter}

Pour modifier ou supprimer des filtres prédéfinis, procédez comme suit :

1. Ouvrez la liste de filtres prédéfinis à l’aide du bouton **[!UICONTROL Sélectionner ou enregistrer le filtre]** dans la version de règle.

1. Sélectionnez le bouton ![bouton représentant des points de suspension](assets/do-not-localize/rule-builder-icon-more.svg) à côté d’un filtre et choisissez l’action souhaitée.

![](assets/predefined-filters-edit.png)
