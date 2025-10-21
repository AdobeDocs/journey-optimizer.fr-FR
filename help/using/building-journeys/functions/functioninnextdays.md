---
product: journey optimizer
title: inNextDays
description: En savoir plus sur la fonction inNextDays
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextDays, fonction, expression, parcours
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# inNextDays {#inNextDays}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta jours.

## Catégorie

Date

## Syntaxe de la fonction

`inNextDays(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

## Signatures et type renvoyé

`inNextDays(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.
