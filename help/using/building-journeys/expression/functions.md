---
solution: Journey Optimizer
product: journey optimizer
title: Fonctions
description: En savoir plus sur les fonctions dans les expressions de parcours
feature: Journeys
role: Developer
level: Experienced
keywords: fonction, expressions, éditeur, parcours, données, manipulation
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---

# Fonctions {#functions}

Les fonctions sont les blocs fondateurs des expressions de parcours dynamique dans Adobe Journey Optimizer. Elles permettent de transformer, calculer, valider et manipuler des données en temps réel pour créer des expériences clientèle personnalisées. Avec plus de 60 fonctions organisées en catégories intuitives, vous pouvez créer des conditions sophistiquées, effectuer des calculs complexes et prendre des décisions basées sur les données à chaque étape du parcours clientèle.

## Comprendre les fonctions

Les fonctions des expressions de parcours suivent un modèle de syntaxe cohérent :

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**Caractéristiques principales :**

* **Signatures multiples** : une fonction peut avoir différentes signatures (différents ensembles de paramètres ordonnés) pour s’adapter à divers cas d’utilisation.
* **Renvois spécifiques au type** : chaque fonction a un type renvoyé spécifique (chaîne, entier, booléen, date, liste, etc.).
* **Paramètres zéro à N** : les fonctions peuvent accepter des expressions 0 à N en tant que paramètres ordonnés, ce qui assure une certaine flexibilité quant à leur utilisation.

## Pourquoi utiliser les fonctions ?

Les fonctions permettent d’effectuer les opérations suivantes :

* **Créer des conditions dynamiques** - Divisez des chemins de parcours sur la base d’une évaluation des données en temps réel.
* **Personnaliser à grande échelle** - Personnalisez le contenu et les expériences à l’aide des données clientèle et des informations comportementales.
* **Automatiser les décisions** - Créez une logique intelligente sans intervention manuelle.
* **Transformer les données** - Convertissez, mettez en forme et manipulez les types de données pour garantir leur compatibilité.
* **Effectuer des calculs** - Exécutez des opérations mathématiques et des analyses statistiques.
* **Valider les entrées** - Vérifiez la qualité et l’exhaustivité des données avant d’effectuer une action.

## Fonctions par catégorie

Parcourez les fonctions organisées selon leur objectif principal afin de trouver rapidement l’outil adapté à vos besoins.

### Adobe Experience Platform {#aep-functions}

**Segmentation d’audience et ciblage**

Évaluez l’appartenance à une audience pour créer des chemins de parcours personnalisés en fonction des segments de clientèle définis dans Adobe Experience Platform.

| Fonction | Description |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Vérifie si un individu appartient à une audience spécifique. |

[Affiche des détails de la fonction Adobe Experience Platform →](../functions/functioninaudience.md)

### Fonctions d’agrégation {#aggregation-functions}

**Calculs statistiques et synthèse des données**

Effectuez des calculs sur des ensembles de valeurs afin d’obtenir des informations telles que des moyennes, des nombres, des sommes et des valeurs minimum et maximum. Essentiel pour la prise de décision axée sur les données.

| Fonction | Description |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Calcule la valeur moyenne. |
| [count](../functions/aggregation-functions.md#count) | Compte les éléments non nuls. |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Compte uniquement les valeurs nulles. |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Compte tous les éléments, y compris les nuls. |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Compte les valeurs uniques non nulles. |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Compte les valeurs uniques, y compris les nulles. |
| [max](../functions/aggregation-functions.md#max) | Trouve la valeur maximale |
| [min](../functions/aggregation-functions.md#min) | Trouve la valeur minimale |
| [sum](../functions/aggregation-functions.md#sum) | Calcule la somme totale |

[Affiche toutes les fonctions d’agrégation →](../functions/aggregation-functions.md)

### Fonctions de conversion {#conversion-functions}

**Transformation du type de données**

Convertissez des données entre différents types (chaîne, entier, décimal, booléen, date, durée) pour garantir la compatibilité entre les opérations et les sources de données.

| Fonction | Description |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Convertit en booléen |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Convertit en date uniquement (pas d’heure) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Convertit en date avec heure |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Convertit en date-heure sans fuseau horaire |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Convertit en nombre décimal |
| [toDuration](../functions/conversion-functions.md#toDuration) | Convertit en durée |
| [toInteger](../functions/conversion-functions.md#toInteger) | Convertit en entier |
| [toString](../functions/conversion-functions.md#toString) | Convertit en chaîne |

[Affiche toutes les fonctions de conversion →](../functions/conversion-functions.md)

### Fonctions de date {#date-functions}

**Manipulation de date et d’heure**

Utilisez les dates, heures et fuseaux horaires pour créer des conditions temporelles, planifier des actions et effectuer des calculs temporels.

| Fonction | Description |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Obtient l’heure actuelle en millisecondes |
| [inLastDays](../functions/date-functions.md#inLastDays) | Vérifie si la date est comprise dans les N derniers jours |
| [inLastHours](../functions/date-functions.md#inLastHours) | Vérifie si la date est comprise dans les N dernières heures |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Vérifiee si la date est comprise dans les N derniers mois |
| [inLastYears](../functions/date-functions.md#inLastYears) | Vérifie si la date est comprise dans les N dernières années |
| [inNextDays](../functions/date-functions.md#inNextDays) | Vérifie si la date est comprise dans les N prochains jours |
| [inNextHours](../functions/date-functions.md#inNextHours) | Vérifie si la date est comprise dans les N prochaines heures |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Vérifie si la date est comprise dans les N prochains mois |
| [inNextYears](../functions/date-functions.md#inNextYears) | Vérifie si la date est comprise dans les N prochaines années |
| [now](../functions/date-functions.md#now) | Obtient la date et l’heure actuelles |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Obtient l’heure actuelle avec décalage |
| [setHours](../functions/date-functions.md#setHours) | Définit des heures spécifiques dans date-heure |
| [setDays](../functions/date-functions.md#setDays) | Définit des jours spécifiques dans date-heure |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Met à jour le fuseau horaire de date-heure |

[Affiche toutes les fonctions de date →](../functions/date-functions.md)

### Fonctions de liste {#list-functions}

**Manipulation et analyse des collections**

Filtrez, triez, transformez et analysez des tableaux et des listes pour travailler avec des structures de données complexes et effectuer des opérations sur des ensembles.

| Fonction | Description |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Obtient des valeurs uniques (à l’exclusion des valeurs nulles) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Obtient des valeurs uniques (y compris les valeurs nulles) |
| [filter](../functions/list-functions.md#filter) | Filtre la liste en fonction de critères |
| [getListItem](../functions/list-functions.md#getListItem) | Obtient un élément à un index spécifique |
| [in](../functions/list-functions.md#in) | Vérifie si la valeur existe dans la liste |
| [intersect](../functions/list-functions.md#intersect) | Recherche des éléments communs entre les listes |
| [limit](../functions/list-functions.md#limit) | Limite le nombre d’éléments renvoyés |
| [listSize](../functions/list-functions.md#listSize) | Obtient la taille de la liste |
| [serializeList](../functions/list-functions.md#serializeList) | Convertit la liste en chaîne |
| [sort](../functions/list-functions.md#sort) | Trie des éléments de liste |

[Affiche toutes les fonctions de liste →](../functions/list-functions.md)

### Fonctions mathématiques {#math-functions}

**Opérations mathématiques**

Effectuez des calculs numériques et des transformations pour le traitement des données et la logique métier.

| Fonction | Description |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Génère un nombre aléatoire (0-1) |
| [round](../functions/math-functions.md#round) | Arrondit à l’entier le plus proche |

[Affiche toutes les fonctions mathématiques →](../functions/math-functions.md)

### Fonctions de chaîne {#string-functions}

**Manipulation et validation de texte**

Traitez, transformez, recherchez et validez des données de texte pour la création de contenu dynamique et la logique conditionnelle.

| Fonction | Description |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Concatène des chaînes |
| [contain](../functions/string-functions.md#contain) | Vérifie si la chaîne contient une sous-chaîne |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | Vérifie si contient (non-respect de la casse) |
| [endWith](../functions/string-functions.md#endWith) | Vérifie si la chaîne se termine par le suffixe |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | Vérifie si se termine par (non-respect de la casse) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Comparer les chaînes (non-respect de la casse) |
| [indexOf](../functions/string-functions.md#indexOf) | Rechercher la position de la première occurrence |
| [isEmpty](../functions/string-functions.md#isEmpty) | Vérifie si la chaîne est vide |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Vérifie que la chaîne n’est pas vide |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Recherche la position de la dernière occurrence |
| [length](../functions/string-functions.md#length) | Obtient la longueur de chaîne |
| [lower](../functions/string-functions.md#lower) | Convertit en minuscules |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Fait correspondre une expression régulière |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Vérifie l’inégalité (non-respect de la casse) |
| [replace](../functions/string-functions.md#replace) | Remplace la première occurrence |
| [replaceAll](../functions/string-functions.md#replaceAll) | Remplace toutes les occurrences |
| [split](../functions/string-functions.md#split) | Partage une chaîne en tableau |
| [startWith](../functions/string-functions.md#startWith) | Vérifie si la chaîne commence par le préfixe |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | Vérifie si commence par (non-respect de la casse) |
| [substr](../functions/string-functions.md#substr) | Extrait la sous-chaîne |
| [trim](../functions/string-functions.md#trim) | Supprime les espaces de début et de fin |
| [upper](../functions/string-functions.md#upper) | Convertit en majuscules |
| [uuid](../functions/string-functions.md#uuid) | Génère l’UUID |

[Affiche toutes les fonctions de chaîne →](../functions/string-functions.md)

## Étapes suivantes

Maintenant que vous comprenez les fonctions disponibles, découvrez ce qui suit :

* **[Éditeur d’expression avancé](expressionadvanced.md)** : découvrez comment créer des expressions complexes à l’aide de l’éditeur avancé.
* **[Syntaxe des expressions](generalities.md)** : maîtrisez des règles de syntaxe pour écrire des expressions de parcours.
* **[Opérateurs](operators.md)** : découvrez les opérateurs que vous pouvez utiliser avec les fonctions pour créer une logique.
* **[Références de champ](field-references.md)** : découvrez comment référencer des champs de données dans vos expressions.
