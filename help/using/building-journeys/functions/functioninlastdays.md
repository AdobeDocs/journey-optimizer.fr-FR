---
product: journey optimizer
title: inLastDays
description: En savoir plus sur la fonction inLastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, fonction, expression, parcours
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '48'
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
