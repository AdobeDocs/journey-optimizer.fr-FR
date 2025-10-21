---
product: journey optimizer
title: avg
description: En savoir plus sur la fonction avg
feature: Journeys
role: Engineer
level: Experienced
keywords: avg, fonction, expression, parcours
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 100%

---

# avg {#avg}

Renvoie la valeur moyenne d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.


## Catégorie

Agrégation

## Syntaxe de la fonction

`avg(<parameter>)`

## Paramètres

Types pris en charge :

* listInteger
* listDecimal
* Décimal
* Entier

## Signatures et type renvoyé

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Renvoie une valeur décimale.

## Exemples

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Renvoie 7,0.

`avg(10.2, 3)`

Renvoie 6,6.
