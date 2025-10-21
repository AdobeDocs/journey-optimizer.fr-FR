---
product: journey optimizer
title: inNextMonths
description: En savoir plus sur la fonction inNextMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextMonths, fonction, expression, parcours
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# inNextMonths {#inNextMonths}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta mois.

## Catégorie

Date

## Syntaxe de la fonction

`inNextMonths(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

## Signatures et type renvoyé

`inNextMonths(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Renvoie true.
