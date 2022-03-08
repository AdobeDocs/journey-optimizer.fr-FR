---
product: adobe campaign
title: min
description: En savoir plus sur la fonction min
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '92'
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
* nombre entier
* décimal
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

`min(@{BarBeacon.inventory},5)`

`min([10,3,8])`

Renvoie 3.

`min([10,null,8])`

Renvoie 8.
