---
product: journey optimizer
title: inNextYears
description: En savoir plus sur la fonction inNextYears
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 100%

---

# inNextYears {#inNextYears}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta ans.

## Catégorie

Date

## Syntaxe de la fonction

`inNextYears(<dateTime>,<delta>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | integer |

## Signatures et type renvoyé

`inNextYears(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Renvoie true.
