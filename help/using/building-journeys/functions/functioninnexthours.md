---
product: adobe campaign
title: inNextHours
description: En savoir plus sur la fonction inNextHours
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 100%

---

# inNextHours {#inNextHours}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta heures.

## Catégorie

Date

## Syntaxe de la fonction

`inNextHours(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | integer |

## Signatures et type renvoyé

`inNextHours(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Renvoie true.
