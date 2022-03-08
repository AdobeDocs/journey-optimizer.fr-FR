---
product: adobe campaign
title: inLastYears
description: En savoir plus sur la fonction inLastYears
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '44'
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
| delta | integer |

## Signatures et type renvoyé

`inLastYears(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

## Exemples

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Renvoie true.
