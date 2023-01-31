---
product: journey optimizer
title: inNextDays
description: En savoir plus sur la fonction inNextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays, fonction, expression, parcours
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
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
| delta | integer |

## Signatures et type renvoyé

`inNextDays(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

Renvoie true.
