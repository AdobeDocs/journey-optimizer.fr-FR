---
product: journey optimizer
title: inNextHours
description: En savoir plus sur la fonction inNextHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
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
