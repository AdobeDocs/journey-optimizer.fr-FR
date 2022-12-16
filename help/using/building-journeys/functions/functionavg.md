---
product: journey optimizer
title: avg
description: En savoir plus sur la fonction avg
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
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
* décimal
* integer

## Signatures et type renvoyé

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Renvoie une valeur décimale.

## Exemples

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

Renvoie 7,0.

`avg(10.2, 3)`

Renvoie 6,6.
