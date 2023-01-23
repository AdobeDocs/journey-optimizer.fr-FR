---
product: journey optimizer
title: inLastYears
description: En savoir plus sur la fonction inLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears, fonction, expression, parcours
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 91%

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
| delta | integer |

## Signatures et type renvoyé

`inLastYears(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Renvoie true.
