---
product: adobe campaign
title: inLastHours
description: En savoir plus sur la fonction inLastHours
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 100%

---

# inLastHours {#inLastHours}

Renvoie « true » si une date et une heure données sont comprises entre maintenant et maintenant - delta heures.

## Catégorie

Date

## Syntaxe de la fonction

`inLastHours(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | integer |

## Signatures et type renvoyé

`inLastHours(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Renvoie true.

`inLastHours(@{MyEvent.timestamp}, 4)`

Renvoie true.
