---
solution: Journey Optimizer
product: journey optimizer
title: Recherche, filtrage, organisation
description: En savoir plus à propos de l’interface utilisateur de Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
source-git-commit: b5fa17bfc888236994e73474c35b1aaafcda3ebe
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 100%

---


# Recherche, filtrage, organisation {#search-filter-organize}

## Recherche{#unified-search}

Depuis n’importe où dans l’interface Adobe Journey Optimizer, utilisez la recherche Adobe Experience Cloud unifiée au centre de la barre supérieure pour rechercher des ressources, des parcours, des jeux de données et plus encore dans vos sandbox.

Commencez à saisir du contenu pour afficher les meilleurs résultats. Les articles d’aide sur les mots-clés saisis apparaissent également dans les résultats.

![](assets/unified-search.png)

Appuyez sur **Entrée** pour accéder à tous les résultats et filtrer par objet métier.

![](assets/search-and-filter.png)

## Filtrer les listes{#filter-lists}

Dans la plupart des listes, utilisez la barre de recherche pour rechercher des éléments spécifiques et définir des critères de filtrage.

Pour accéder aux filtres, cliquez sur l’icône en forme de filtre en haut à gauche d’une liste. Le menu Filtrer vous permet de filtrer les éléments affichés selon différents critères : vous pouvez choisir d’afficher uniquement les éléments d’un certain type ou statut, ceux que vous avez créés ou ceux que vous avez modifiés au cours des 30 derniers jours. Les options varient en fonction du contexte.

De plus, vous pouvez utiliser les balises unifiées pour filtrer une liste en fonction des balises affectées à un objet. Pour l’instant, les balises sont disponibles pour les parcours et les campagnes. [Découvrir comment utiliser les balises](#tags)

>[!NOTE]
>
>Notez que les colonnes affichées peuvent être personnalisées à l&#39;aide du bouton de configuration en haut à droite des listes. La personnalisation est enregistrée pour chaque utilisateur.

Il est possible d’effectuer des actions de base sur chaque élément des différentes listes. Vous pouvez par exemple dupliquer ou supprimer un élément.

![](assets/journey4.png)

## Utiliser des balises unifiées {#tags}

Avec les [balises unifiées](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=fr) Adobe Experience Platform, vous pouvez facilement classer vos parcours et campagnes Journey Optimizer pour améliorer la recherche dans les listes.

>[!AVAILABILITY]
>
>Les balises unifiées sont actuellement en version Beta. La documentation et les fonctionnalités peuvent changer.

### Ajouter des balises à un objet

Le champ **Balises**, dans les propriétés du [parcours](../building-journeys/journey-gs.md#change-properties) ou de la [campagne](../campaigns/create-campaign.md#create), vous permet d’ajouter des balises à votre objet. Vous pouvez sélectionner une balise existante ou créer une nouvelle balise.

Commencez à saisir le nom de la balise souhaitée et sélectionnez-la dans la liste. Si elle n’est pas disponible, cliquez sur **Créer** pour créer une balise et l’ajouter. Vous pouvez définir autant de balises que vous le souhaitez.

![](assets/tags1.png)

La liste des balises définies s’affiche sous le champ **Balises**.

>[!NOTE]
>
> Les balises sont sensibles à la casse.
> 
> Si vous dupliquez ou créez une nouvelle version d’un parcours ou d’une campagne, les balises sont conservées.

### Filtrer les balises

Les listes des parcours et des campagnes comportent une colonne dédiée permettant de visualiser facilement les balises.

Un filtre est également disponible pour afficher uniquement les parcours ou les campagnes comportant les balises souhaitées.

![](assets/tags2.png)

Vous pouvez ajouter ou supprimer des balises de n’importe quel type de parcours ou de campagne (dynamique, brouillon, etc.). Cliquez sur l’icône **Plus d’actions** en regard de l’objet, puis sélectionnez **Modifier les balises**.

![](assets/tags3.png)

### Gérer les balises

L’administration peut supprimer des balises et les classer par catégorie dans le menu **Balises**, sous **Administration**. En savoir plus sur la gestion des balises dans la [documentation sur les balises unifiées](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html?lang=fr).

>[!NOTE]
>
> Les balises créées directement à partir du champ **[!UICONTROL Balises]** dans Journey Optimizer sont automatiquement ajoutées à la catégorie intégrée « Non classé ».
