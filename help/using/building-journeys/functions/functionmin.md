---
product: journey optimizer
title: min
description: En savoir plus sur la fonction min
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: min, fonction, expression, parcours
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 100%

---

# min {#min}

Renvoie la valeur minimale d’un ensemble d’expressions, exprimée sous la forme d’une liste ou de deux expressions. Les valeurs « null » sont ignorées.

## Catégorie

Agrégation

## Syntaxe de la fonction

`min(<parameters>)`

## Paramètres

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

## Signatures et types renvoyés

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

## Exemples

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Renvoie 3.

`min([10,null,8])`

Renvoie 8.
