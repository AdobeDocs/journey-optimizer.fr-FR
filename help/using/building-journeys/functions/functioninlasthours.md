---
product: journey optimizer
title: inLastHours
description: En savoir plus sur la fonction inLastHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastHours, fonction, expression, parcours
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '49'
ht-degree: 100%

---

# inLastHours {#inLastHours}

Renvoie « true » si une date et une heure données sont comprises entre maintenant et maintenant - delta heures.

## Catégorie

Date

## Syntaxe de la fonction

`inLastHours(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | integer |

## Signatures et type renvoyé

`inLastHours(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Renvoie true.

`inLastHours(@{MyEvent.timestamp}, 4)`

Renvoie true.
