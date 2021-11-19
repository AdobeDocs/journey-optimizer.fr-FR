---
product: adobe campaign
title: sum
description: En savoir plus sur la fonction sum
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 100%

---

# sum {#sum}

Renvoie la somme des valeurs d’un ensemble d’expressions. Les valeurs « null » sont ignorées.

## Catégorie

Agrégation

## Syntaxe de la fonction

`sum(<parameters>)`

## Paramètres

* listInteger
* listDecimal
* durée
* integer
* decimal

## Signatures et types renvoyés

`sum(<listDecimal>)`

Renvoie une valeur décimale.

`sum(<listInteger>)`

Renvoie un entier.

`sum(<integer>,<integer>)`

Renvoie un entier.

`sum(<decimal>,<decimal>)`

Renvoie une valeur décimale.

## Exemples

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

Renvoie 21.

`sum([10.5,null,8.1])`

Renvoie 18,6.
