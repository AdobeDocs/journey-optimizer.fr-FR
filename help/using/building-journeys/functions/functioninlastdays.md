---
product: journey optimizer
title: inLastDays
description: En savoir plus sur la fonction inLastDays
feature: Journeys
role: Developer
level: Experienced
keywords: inLastDays, fonction, expression, parcours
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '46'
ht-degree: 100%

---

# inLastDays {#inLastDays}

Renvoie « true » si une valeur dateTime donnée est comprise entre maintenant et maintenant - delta jours.

## Catégorie

Date

## Syntaxe de la fonction

`inLastDays(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

## Signatures et type renvoyé

`inLastDays(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.
