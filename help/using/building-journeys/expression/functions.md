---
solution: Journey Optimizer
product: journey optimizer
title: Fonctions
description: Découvrez les fonctions dans les expressions de parcours
feature: Journeys
role: Developer
level: Experienced
keywords: fonction, expressions, éditeur, parcours, données, manipulation
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 11%

---

# Fonctions {#functions}

Les fonctions sont les blocs de création des expressions de parcours dynamique dans Adobe Journey Optimizer. Ils vous permettent de transformer, calculer, valider et manipuler des données en temps réel pour créer des expériences client personnalisées. Avec plus de 60 fonctions organisées en catégories intuitives, vous pouvez créer des conditions sophistiquées, effectuer des calculs complexes et prendre des décisions basées sur les données à chaque étape du parcours client.

## Compréhension des fonctions

Les fonctions des expressions de parcours suivent un modèle de syntaxe cohérent :

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**Caractéristiques principales :**

* **Signatures multiples** : une fonction peut avoir différentes signatures (différents ensembles de paramètres ordonnés) pour s’adapter à divers cas d’utilisation
* **Renvois spécifiques au type** : chaque fonction a un type renvoyé spécifique (chaîne, entier, booléen, date, liste, etc.)
* **Paramètres zéro à N** : les fonctions peuvent accepter des expressions 0 à N en tant que paramètres ordonnés, ce qui vous offre une certaine flexibilité quant à leur utilisation

## Pourquoi utiliser des fonctions ?

Les fonctions vous permettent d’effectuer les opérations suivantes :

* **Créer des conditions dynamiques** - Chemins de parcours de branche basés sur l’évaluation des données en temps réel
* **Personnaliser à grande échelle** - Personnalisez le contenu et les expériences à l’aide des données client et des informations comportementales
* **Automatiser les décisions** - Créer une logique intelligente sans intervention manuelle
* **Transformer les données** - Convertissez, formatez et manipulez les types de données pour garantir leur compatibilité
* **Effectuer des calculs** - Exécuter des opérations mathématiques et des analyses statistiques
* **Valider les entrées** - Vérifiez la qualité et l’exhaustivité des données avant d’effectuer une action

## Fonctions par catégorie

Parcourez les fonctions organisées selon leur objectif principal afin de trouver rapidement l’outil adapté à vos besoins.

### Adobe Experience Platform {#aep-functions}

**Segmentation et ciblage d’audience**

Évaluez l’appartenance à une audience pour créer des chemins de parcours personnalisés en fonction des segments de clients définis dans Adobe Experience Platform.

| Fonction | Description |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Vérifier si un individu appartient à une audience spécifique |

[Affichage des détails de la fonction Adobe Experience Platform →](../functions/functioninaudience.md)

### Fonctions d’agrégation {#aggregation-functions}

**Calculs statistiques et synthèse des données**

Effectuez des calculs sur des ensembles de valeurs afin d’obtenir des informations telles que des moyennes, des nombres, des sommes et des valeurs min./max. Essentiel pour la prise de décision axée sur les données.

| Fonction | Description |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Calculer la valeur moyenne |
| [count](../functions/aggregation-functions.md#count) | Compter les éléments non nuls |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Compter uniquement les valeurs nulles |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Comptabiliser tous les éléments, y compris les nulls |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Compter les valeurs uniques non nulles |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Compter les valeurs uniques, y compris les nulles |
| [max](../functions/aggregation-functions.md#max) | Rechercher la valeur maximale |
| [min](../functions/aggregation-functions.md#min) | Rechercher la valeur minimale |
| [sum](../functions/aggregation-functions.md#sum) | Calculer la somme totale |

[Affichage de toutes les fonctions d’agrégation →](../functions/aggregation-functions.md)

### Fonctions de conversion {#conversion-functions}

**Transformation du type de données**

Convertissez des données entre différents types (chaîne, entier, décimal, booléen, date, durée) pour garantir la compatibilité entre les opérations et les sources de données.

| Fonction | Description |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Convertir en booléen |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Convertir en date uniquement (pas d’heure) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Convertir en date avec heure |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Convertir en date-heure sans fuseau horaire |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Convertir en nombre décimal |
| [toDuration](../functions/conversion-functions.md#toDuration) | Convertir en durée |
| [toInteger](../functions/conversion-functions.md#toInteger) | Convertir en entier |
| [toString](../functions/conversion-functions.md#toString) | Convertir en chaîne |

[Afficher toutes les fonctions de conversion →](../functions/conversion-functions.md)

### Fonctions de date {#date-functions}

**manipulation de la date et de l’heure**

Utilisez les dates, heures et fuseaux horaires pour créer des conditions temporelles, planifier des actions et effectuer des calculs temporels.

| Fonction | Description |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Obtenir l’heure actuelle en millisecondes |
| [inLastDays](../functions/date-functions.md#inLastDays) | Vérifier si la date est comprise dans les N derniers jours |
| [inLastHours](../functions/date-functions.md#inLastHours) | Vérifier si la date est comprise dans les N dernières heures |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Vérifier si la date est comprise dans les N derniers mois |
| [inLastYears](../functions/date-functions.md#inLastYears) | Vérifier si la date est comprise dans les N dernières années |
| [inNextDays](../functions/date-functions.md#inNextDays) | Vérifier si la date se situe dans les N prochains jours |
| [inNextHours](../functions/date-functions.md#inNextHours) | Vérifier si la date se situe dans les N heures suivantes |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Vérifier si la date se situe dans les N prochains mois |
| [inNextYears](../functions/date-functions.md#inNextYears) | Vérifier si la date se situe dans les N prochaines années |
| [now](../functions/date-functions.md#now) | Obtenir la date et l’heure actuelles |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Obtenir l’heure actuelle avec décalage |
| [setHours](../functions/date-functions.md#setHours) | Définir des heures spécifiques dans date-heure |
| [setDays](../functions/date-functions.md#setDays) | Définir des jours spécifiques dans date-heure |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Mettre à jour le fuseau horaire de date-heure |

[Afficher toutes les fonctions de date →](../functions/date-functions.md)

### Fonctions de liste {#list-functions}

**Manipulation et analyse des collections**

Filtrez, triez, transformez et analysez des tableaux et des listes pour travailler avec des structures de données complexes et effectuer des opérations sur les ensembles.

| Fonction | Description |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Obtenir des valeurs uniques (à l’exclusion des valeurs nulles) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Obtenir des valeurs uniques (y compris les valeurs nulles) |
| [filtrer](../functions/list-functions.md#filter) | Filtrer la liste en fonction de critères |
| [getListItem](../functions/list-functions.md#getListItem) | Obtenir un élément à un index spécifique |
| [in](../functions/list-functions.md#in) | Vérifier si la valeur existe dans la liste |
| [intersect](../functions/list-functions.md#intersect) | Recherche d’éléments communs entre les listes |
| [limit](../functions/list-functions.md#limit) | Limiter le nombre d&#39;éléments renvoyés |
| [listSize](../functions/list-functions.md#listSize) | Get size of list |
| [serializeList](../functions/list-functions.md#serializeList) | Convertir la liste en chaîne |
| [sort](../functions/list-functions.md#sort) | Tri des éléments de liste |

[Afficher toutes les fonctions de liste →](../functions/list-functions.md)

### Fonctions mathématiques {#math-functions}

**Opérations mathématiques**

Effectuer des calculs numériques et des transformations pour le traitement des données et la logique métier.

| Fonction | Description |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Générer un nombre aléatoire (0-1) |
| [round](../functions/math-functions.md#round) | Arrondir à l’entier le plus proche |

[Afficher toutes les fonctions mathématiques →](../functions/math-functions.md)

### Fonctions de chaîne {#string-functions}

**Manipulation et validation de texte**

Traitez, transformez, recherchez et validez des données de texte pour la création de contenu dynamique et la logique conditionnelle.

| Fonction | Description |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Concaténer des chaînes |
| [contain](../functions/string-functions.md#contain) | Vérifier si la chaîne contient une sous-chaîne |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | Le contrôle contient (non-respect de la casse) |
| [endWith](../functions/string-functions.md#endWith) | Vérifier si la chaîne se termine par le suffixe |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | La vérification se termine par (non-respect de la casse) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Comparer les chaînes (non-respect de la casse) |
| [indexOf](../functions/string-functions.md#indexOf) | Rechercher la position de la première occurrence |
| [isEmpty](../functions/string-functions.md#isEmpty) | Vérifier si la chaîne est vide |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Vérifier si la chaîne n’est pas vide |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Rechercher la position de la dernière occurrence |
| [length](../functions/string-functions.md#length) | Obtenir la longueur de chaîne |
| [lower](../functions/string-functions.md#lower) | Convertir en minuscules |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Faire correspondre l’expression régulière |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Vérification non égale (non-respect de la casse) |
| [replace](../functions/string-functions.md#replace) | Remplacer la première occurrence |
| [replaceAll](../functions/string-functions.md#replaceAll) | Remplacer toutes les occurrences |
| [split](../functions/string-functions.md#split) | Fractionner la chaîne en tableau |
| [startWith](../functions/string-functions.md#startWith) | Vérifier si la chaîne commence par le préfixe |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | La vérification commence par (non-respect de la casse) |
| [substr](../functions/string-functions.md#substr) | Extraire la sous-chaîne |
| [trim](../functions/string-functions.md#trim) | Supprimer les espaces de début et de fin |
| [upper](../functions/string-functions.md#upper) | Convertir en majuscules |
| [uuid](../functions/string-functions.md#uuid) | Générer l’UUID |

[Afficher toutes les fonctions de chaîne →](../functions/string-functions.md)

## Étapes suivantes

Maintenant que vous comprenez les fonctions disponibles, explorez :

* **[Éditeur d’expression avancé](expressionadvanced.md)** - Découvrez comment créer des expressions complexes à l’aide de l’éditeur avancé
* **[Syntaxe des expressions](generalities.md)** - Principal des règles de syntaxe pour l’écriture d’expressions de parcours
* **[Opérateurs](operators.md)** - Découvrez les opérateurs que vous pouvez utiliser avec les fonctions pour créer une logique.
* **[Références de champ](field-references.md)** - Découvrez comment référencer des champs de données dans vos expressions
