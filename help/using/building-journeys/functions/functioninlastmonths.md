---
product: journey optimizer
title: inLastMonths
description: En savoir plus sur la fonction inLastMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastMonths, fonction, expression, parcours
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# inLastMonths {#inLastMonths}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant - delta mois.

## Catégorie

Date

## Syntaxe de la fonction

`inLastMonths(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | integer |

## Signatures et type renvoyé

`inLastMonths(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

Renvoie true.
