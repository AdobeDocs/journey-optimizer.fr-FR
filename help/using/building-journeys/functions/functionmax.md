---
product: journey optimizer
title: max
description: En savoir plus sur la fonction max
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: max, fonction, expression, parcours
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 100%

---

# max{#max}

Renvoie la valeur maximale d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.

## Catégorie

Agrégation

## Syntaxe de la fonction

`max(<parameter>)`

## Paramètres

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* durée
* nombre entier
* décimal
* dateTime
* dateTimeOnly

## Signatures et types renvoyés

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

## Exemples

`max(@{BarBeacon.inventory},5)`

`max([10,3,8])`

Renvoie 10.

`max([10,null,8])`

Renvoie 10.
