---
solution: Journey Optimizer
product: journey optimizer
title: Gérer les balises dans les parcours
description: Gérer les balises dans les parcours
feature: Journeys, Tags
topic: Content Management
role: User
level: Intermediate
keywords: parcours, balises
exl-id: 44c255d1-121c-47d4-b407-161626ca3cb4
version: Journey Orchestration
source-git-commit: 302db58525a7b2648bb9c44bc9b42da787ca9c43
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 41%

---

# Gérer les balises dans les parcours {#journey_tags}

En tant qu’utilisateur ou utilisatrice de Journey Optimizer, vous pouvez identifier vos parcours à l’aide de balises. Les balises constituent un moyen simple et rapide de classer des objets afin de faciliter leur recherche.

## Balises et conventions de nommage {#tags-vs-naming}

Les équipes s’appuient souvent sur des conventions de nommage complexes pour stocker les métadonnées directement dans les noms de parcours, par exemple : *Marketing tout au long du cycle de vie - Éducation - Intégration des clients V2 - Éducation des applications - T3 2025*. Bien qu’elle soit bien intentionnée, cette approche présente une faiblesse majeure : à mesure que le travail s’étend à tous les membres de l’équipe, la convention est rarement appliquée de manière cohérente et les listes parcours deviennent difficiles à parcourir.

**Les catégories de balises** dans Journey Optimizer offrent une meilleure alternative. Au lieu de coder les métadonnées dans le nom, vous joignez des balises classées à chaque parcours (par exemple, équipe, objectif, phase, trimestre) et utilisez des filtres pour les localiser. Les noms de parcours peuvent alors se concentrer sur ce qui compte vraiment : le jalon du client piloté.

Avantages des catégories de balises par rapport aux conventions de nommage :

* **Cohérence** — Les balises sont sélectionnées dans une liste contrôlée et ne sont pas saisies librement.
* **Filtrabilité** : toute combinaison de valeurs de balise peut être utilisée pour découper instantanément la liste de parcours.
* **Clarté** — Les noms de parcours restent courts et axés sur les jalons.
* **Évolutivité** : l’ajout d’une nouvelle dimension de métadonnées implique la création d’une catégorie de balises, et non la réécriture d’une convention de nommage.

Pour obtenir un workflow de configuration recommandé, voir [Configurer des catégories de balises pour la gestion des parcours &#x200B;](#tags-setup) ci-dessous.

## Ajouter des balises à un parcours

Le champ **Balises**, dans les propriétés du parcours, vous permet d’ajouter des balises à votre parcours. Vous pouvez sélectionner une balise existante ou en créer une nouvelle. Commencez à saisir le nom de la balise souhaitée et sélectionnez-la dans la liste. Si elle n’est pas disponible, cliquez sur **Créer** pour créer une balise et l’ajouter à votre parcours. Vous pouvez définir autant de balises que vous le souhaitez.

![Panneau Balises dans les propriétés de parcours pour la catégorisation et l’organisation](assets/tags1.png)

La liste des balises définies s’affiche sous le champ **Balises**.

>[!NOTE]
>
> Les balises sont sensibles à la casse.
> 
> Si vous dupliquez ou créez une autre version d’un parcours, les balises sont conservées.

## Filtrer les balises

La liste des parcours comporte une colonne dédiée permettant de visualiser facilement les balises.

Un filtre est également disponible pour afficher uniquement les parcours comportant les balises souhaitées.

![Liste déroulante de sélection des balises avec les balises disponibles pour la classification des parcours](assets/tags2.png)

Vous pouvez ajouter ou supprimer des balises de n’importe quel type de parcours (actif, brouillon, etc.). Cliquez sur l’icône **Plus d’actions** en regard du parcours, puis sélectionnez **Modifier les balises**.

![Liste de parcours filtrée par balises affichant les parcours classés par catégorie](assets/tags3.png)

## Gérer les balises

L’administration peut supprimer des balises et les classer par catégorie dans le menu **Balises**, sous **Administration**. Consultez cette [documentation](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=fr).

>[!NOTE]
>
> Les balises définies dans les parcours sont ajoutées à la catégorie intégrée « Non classé ».

## Configurer des catégories de balises pour la gestion des parcours {#tags-setup}

Pour remplacer une convention de nommage complexe par une approche basée sur les balises dans l’ensemble de votre équipe, procédez comme suit.

**Étape 1 — Créer des catégories de balises (Admin)**

Dans **[!UICONTROL Administration]** > **[!UICONTROL Balises]**, créez une catégorie pour chaque attribut de métadonnées que votre équipe code actuellement dans des noms de parcours, par exemple : *Équipe*, *Objectif marketing*, *Campagne*, *Phase*, *Trimestre*.

**Étape 2 — Renseigner chaque catégorie avec des valeurs de balise (Admin)**

Dans chaque catégorie, créez les balises qui représentent toutes les valeurs possibles. Par exemple, la catégorie *Phase* peut contenir : *Sensibilisation*, *Intégration*, *Rétention*, *Reconquête*.

**Étape 3 — Application de balises lors de la création de parcours (utilisateurs)**

À chaque création d’un parcours, sélectionnez la balise appropriée dans chaque catégorie des propriétés du parcours. En règle générale, un parcours comporte une balise par catégorie.

**Étape 4 : nommer les parcours pour le jalon, filtrer par balises**

Veillez à ce que le nom du parcours reste axé sur le jalon client qu’il franchit (par exemple, *Première transaction de fidélité*). Utilisez les filtres de balises dans la liste des parcours pour localiser les parcours à l’aide d’une combinaison de métadonnées, sans recourir à l’analyse de nom.

>[!TIP]
>
>Pour une discussion plus large sur cette approche et ses avantages à grande échelle, consultez [Bonnes pratiques pour les parcours avancés dans Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.
