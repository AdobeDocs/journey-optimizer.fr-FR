---
product: journey optimizer
title: sum
description: En savoir plus sur la fonction sum
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sum, fonction, expression, parcours
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '57'
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
* duration
* Entier
* Décimal

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

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Renvoie 21.

`sum([10.5,null,8.1])`

Renvoie 18.6.
