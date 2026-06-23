---
product: journey optimizer
title: Fonctions d’agrégation
description: Découvrir les fonctions d’agrégation
feature: Journeys
role: Developer
level: Experienced
keywords: agrégation, fonctions, expression, parcours, moyenne, nombre, max, min, somme
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 65%

---

# Fonctions d’agrégation {#aggregation-functions}

Les fonctions d’agrégation effectuent des calculs sur un ensemble de valeurs et renvoient un seul résultat résumé. Ces fonctions vous permettent d’analyser les données dans vos expressions de parcours en calculant des moyennes, en recherchant des valeurs minimales et maximales, en comptant les éléments et en additionnant les valeurs numériques.

Utilisez des fonctions d’agrégation lorsque vous devez :

* calculer des valeurs statistiques à partir de listes ou de tableaux ([avg](#avg), [sum](#sum), [min](#min), [max](#max)) ;
* compter les éléments dans les collections ([count](#count), [countOnlyNull](#countOnlyNull), [countWithNull](#countWithNull)), avec des options pour inclure ou exclure les valeurs nulles ;
* déterminer des valeurs uniques dans les jeux de données ([distinctCount](#distinctCount), [distinctCountWithNull](#distinctCountWithNull)).
* Prendre des décisions axées sur les données en fonction de mesures calculées

Les fonctions d’agrégation gèrent automatiquement les valeurs nulles en fonction de leur comportement spécifique, ce qui facilite l’utilisation des données du monde réel qui peuvent contenir des valeurs manquantes ou non définies.


## avg {#avg}

Renvoie la valeur moyenne d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.

+++Syntaxe

`avg(<parameter>)`

+++

+++Paramètres

Types pris en charge :

* listInteger
* listDecimal
* décimal
* entier

+++

+++Signatures et type renvoyé

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Renvoie une valeur décimale.

+++

+++Exemples

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Renvoie 7,0.

`avg(10.2, 3)`

Renvoie 6,6.

+++

## count {#count}

Compte les éléments de la liste sans tenir compte des valeurs « null ».

+++Syntaxe

`count(<listAny>)`

`count(<listObject>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. Un listObject ne peut pas contenir d’objet null. |

+++

+++Signatures et type renvoyé

`count(<listAny>)`

Renvoie un entier.

+++

+++Exemples

`count([10,2,10,null])`

Renvoie 3.

`count(@event{my_event.productListItems})`

Renvoie le nombre d’objets dans le tableau d’objets donné (type listObject). Remarque : un objet listObject ne peut pas contenir d’objet null.

+++

## countOnlyNull {#countOnlyNull}

Compte le nombre de valeurs « null » dans la liste.

+++Syntaxe

`countOnlyNull(<listAny>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Signatures et type renvoyé

`countOnlyNull(<listAny>)`

Renvoie un entier.

+++

+++Exemples

`countOnlyNull([10,2,10,null])`

Renvoie 1.

+++

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## countWithNull {#countWithNull}

Compte tous les éléments de la liste, y compris les valeurs « null ».

+++Syntaxe

`countWithNull(<listAny>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Signatures et type renvoyé

`countWithNull(<listAny>)`

Renvoie un entier.

+++

+++Exemples

`countWithNull([10,2,10,null])`

Renvoie 4.

+++

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## distinctCount {#distinctCount}

Compte le nombre de valeurs différentes en ignorant les valeurs « null ».

+++Syntaxe

`distinctCount(<listAny>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | Chaîne | Ce paramètre est facultatif et uniquement pour listObject. Si le paramètre n’est pas fourni, un objet est considéré comme dupliqué si tous les attributs ont les mêmes valeurs. Dans le cas contraire, un objet est considéré comme dupliqué si l’attribut donné a la même valeur. |

+++

+++Signatures et type renvoyé

`distinctCount(<listAny>)`

Renvoie un entier.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Renvoie une liste d’objets.

+++

+++Exemples

`distinctCount([10,2,10,null])`

Renvoie 2.

`distinctCount(@event{my_event.productListItems})`

Renvoie le nombre d’objets strictement distincts dans le tableau d’objets donné (type listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Renvoie le nombre d’objets ayant une valeur d’attribut {} « SKU » distincte.

+++

## distinctCountWithNull {#distinctCountWithNull}

Compte le nombre de valeurs différentes, y compris les valeurs « null ».

+++Syntaxe

`distinctCountWithNull(<listAny>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Signatures et type renvoyé

`distinctCountWithNull(<listAny>)`

Renvoie un entier.

+++

+++Exemples

`distinctCountWithNull([10,2,10,null])`

Renvoie 3.

+++

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## max {#max}

Renvoie la valeur maximale d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.

+++Syntaxe

`max(<parameter>)`

+++

+++Paramètres

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* Entier
* Décimal
* dateTime
* dateTimeOnly

+++

+++Signatures et types renvoyés

`max(<listDuration>)`

Renvoie une durée.

`max(<listInteger>)`

Renvoie une durée.

`max(<listDateTimeOnly>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

`max(<listDateTime>)`

Renvoie une date et une heure.

`max(<listDateOnly>)`

Renvoie une date.

`max(<listDecimal>)`

Renvoie une valeur décimale.

`max(<decimal>,<decimal>)`

Renvoie une valeur décimale.

`max(<duration>,<duration>)`

Renvoie une durée.

`max(<dateTime>,<dateTime>)`

Renvoie une date et une heure.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

`max(<integer>,<integer>)`

Renvoie un entier.

+++

+++Exemples

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Renvoie 10.

`max([10,null,8])`

Renvoie 10.

+++

## min {#min}

Renvoie la valeur minimale d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.

+++Syntaxe

`min(<parameters>)`

+++

+++Paramètres

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* Entier
* Décimal
* dateTime
* dateTimeOnly

+++

+++Signatures et types renvoyés

`min(<listDuration>)`

Renvoie une durée.

`min(<listInteger>)`

Renvoie une durée.

`min(<listDateTimeOnly>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

`min(<listDateTime>)`

Renvoie une date et une heure.

`min(<listDateOnly>)`

Renvoie une date.

`min(<listDecimal>)`

Renvoie une valeur décimale.

`min(<decimal>,<decimal>)`

Renvoie une valeur décimale.

`min(<duration>,<duration>)`

Renvoie une durée.

`min(<dateTime>,<dateTime>)`

Renvoie une date et une heure.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

`min(<integer>,<integer>)`

Renvoie un entier.

+++

+++Exemples

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Renvoie 3.

`min([10,null,8])`

Renvoie 8.

+++

## sum {#sum}

Renvoie la somme des valeurs d’un ensemble d’expressions. Les valeurs « null » sont ignorées.

+++Syntaxe

`sum(<parameters>)`

+++

+++Paramètres

* listInteger
* listDecimal
* duration
* Entier
* Décimal

+++

+++Signatures et types renvoyés

`sum(<listDecimal>)`

Renvoie une valeur décimale.

`sum(<listInteger>)`

Renvoie un entier.

`sum(<integer>,<integer>)`

Renvoie un entier.

`sum(<decimal>,<decimal>)`

Renvoie une valeur décimale.

+++

+++Exemples

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Renvoie 21.

`sum([10.5,null,8.1])`

Renvoie 18.6.

+++

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente toutes les fonctions d’agrégation disponibles dans les expressions de parcours AJO, couvrant la manière de calculer des moyennes, des sommes, des valeurs min/max, des nombres et des nombres distincts sur des listes et des tableaux.

**Intentions:**
* Calculer la moyenne d’une liste de valeurs numériques à l’aide de `avg`
* Additionner des valeurs numériques dans une liste ou à partir de champs d&#39;événement à l&#39;aide de `sum`
* Rechercher la valeur minimale ou maximale dans une liste à l’aide de `min` ou `max`
* Compter les éléments non nuls, nuls uniquement ou tous les éléments d’une liste utilisant `count`, `countOnlyNull` ou `countWithNull`
* Compter les valeurs distinctes dans une liste, avec ou sans valeurs NULL, en utilisant `distinctCount` ou `distinctCountWithNull`
* Filtrer des objets uniques dans un listObject en fonction d’un attribut de clé spécifique à l’aide de `distinctCount` avec un paramètre de clé

**Glossaire:**
* **listObject** : liste d’objets complexes (références de champ) ; ne peut pas contenir d’objets nuls *(spécifiques au produit)*
* **listAny** : liste de tout type scalaire pris en charge (chaîne, booléen, entier, décimal, durée, dateTime, dateTimeOnly, dateOnly) *(spécifique au produit)*
* **Valeur Null** : élément absent ou non défini dans une liste ; la plupart des fonctions d’agrégation ignorent les valeurs Null, sauf si la fonction les gère explicitement (par exemple, `countOnlyNull`, `countWithNull`, `distinctCountWithNull`)

**Mécanismes de sécurisation :**
* `countOnlyNull`, `countWithNull` et `distinctCountWithNull` ne prennent pas en charge le type de paramètre `<listObject>`
* `distinctCount` sur un `listObject` nécessite que la liste soit une référence de champ, et non un littéral intégré
* `count` sur un `listObject` nécessite que la liste soit une référence de champ ; un listObject ne peut pas contenir d’objets null

**Terminologie:**
* Nom canonique : Fonctions d’agrégation — Acronyme : none — Variantes : fonctions d’agrégation, fonctions de collection
* Synonymes : « count » = « count non null elements » ; « countWithNull » = « count all elements includes nulls »
* Ne pas confondre : « distinctCount » (ignore les nulls) ≠ « distinctCountWithNull » (inclut les nulls comme valeur distincte)

**FAQ:**
* **Q : Est-ce que `avg` inclut les valeurs nulles dans son calcul ?** — Non, `avg` ignore automatiquement les valeurs nulles.
* **Q : Quelle est la différence entre `count` et `countWithNull` ?** — `count` exclut les valeurs nulles du total, tandis que `countWithNull` compte chaque élément, y compris les nulles.
* **Q : Puis-je utiliser `countOnlyNull` sur un listObject ?** — Non, `<listObject>` n&#39;est pas pris en charge par `countOnlyNull`, `countWithNull` ou `distinctCountWithNull`.
* **Q : Comment compter des objets distincts dans un tableau en fonction d’un attribut spécifique ?** — Utilisez `distinctCount(@event{...}, "attributeName")` en indiquant le nom de l&#39;attribut de clé comme deuxième paramètre.
* **Q : Que renvoie-`max` lorsque la liste contient des nulls ?** — `max` ignore les valeurs nulles et renvoie le maximum parmi les éléments non nuls.

+++
