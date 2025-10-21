---
product: journey optimizer
title: toDecimal
description: En savoir plus sur la fonction toDecimal
feature: Journeys
role: Engineer
level: Experienced
keywords: decimal, fonction, expression, parcours
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 100%

---

# toDecimal {#toDecimal}

Convertit une valeur d’argument en valeur décimale, selon son type.

## Catégorie

Conversion

## Syntaxe de la fonction

`toDecimal(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | convertit la valeur de la chaîne en valeur décimale |
| dateTime | convertit la date en millisecondes (nombre de millisecondes depuis le début de l’époque) |
| booléen | convertit la valeur booléenne en 1 si true, 0 si false |
| nombre entier | convertit en valeur décimale (exemple :1 devient 1,0) |

## Signatures et types renvoyés

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Renvoie une valeur décimale.

## Exemples

`toDecimal("4.0")`

Renvoie 4.0.
