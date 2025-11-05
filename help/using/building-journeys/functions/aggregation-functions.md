---
product: journey optimizer
title: Fonctions d’agrégation
description: En savoir plus sur les fonctions d’agrégation
feature: Journeys
role: Developer
level: Experienced
keywords: agrégation, fonctions, expression, parcours, moyenne, nombre, max, min, somme
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 88%

---

# Fonctions d’agrégation {#aggregation-functions}

Les fonctions d&#39;agrégation sont utilisées pour effectuer des calculs sur un ensemble de valeurs et renvoyer une seule valeur. Ces fonctions sont particulièrement utiles lorsque vous utilisez des listes et des tableaux dans vos expressions de parcours.

## avg {#avg}

Renvoie la valeur moyenne d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.

+++Syntaxe

`avg(<parameter>)`

+++

+++Paramètres

Types pris en charge :

* listInteger
* listDecimal
* Décimal
* Entier

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

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

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

## countWithNull {#countWithNull}

Compte tous les éléments de la liste, y compris les valeurs « null ».

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

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

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

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
* durée
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
* durée
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
* durée
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
