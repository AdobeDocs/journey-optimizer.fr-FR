---
product: journey optimizer
title: inLastYears
description: En savoir plus sur la fonction inLastYears
feature: Journeys
role: Developer
level: Experienced
keywords: inLastYears, fonction, expression, parcours
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '48'
ht-degree: 100%

---

# inLastYears {#inLastYears}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant - delta ans.

## Catégorie

Date

## Syntaxe de la fonction

`inLastYears(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

## Signatures et type renvoyé

`inLastYears(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.
