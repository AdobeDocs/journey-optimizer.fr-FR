---
product: journey optimizer
title: inNextHours
description: En savoir plus sur la fonction inNextHours
feature: Journeys
role: Developer
level: Experienced
keywords: inNextHours, fonction, expression, parcours
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
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
| delta | Entier |

## Signatures et type renvoyé

`inNextHours(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.
