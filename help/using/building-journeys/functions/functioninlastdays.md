---
product: adobe campaign
title: inLastDays
description: En savoir plus sur la fonction inLastDays
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 100%

---

# inLastDays {#inLastDays}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant - delta jours.

## Catégorie

Date

## Syntaxe de la fonction

`inLastDays(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | integer |

## Signatures et type renvoyé

`inLastDays(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

Renvoie true.
