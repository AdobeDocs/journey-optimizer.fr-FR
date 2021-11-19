---
product: adobe campaign
title: toDateOnly
description: En savoir plus sur la fonction toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 100%

---

# toDateOnly{#toDateOnly}

Convertit une valeur dʼargument en une valeur de date uniquement.

## Catégorie

Conversion

## Syntaxe de la fonction

`toDateOnly(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| date au format ISO-8601 ou « AAAA-MM-JJ » (format de date XDM) | chaîne |
| date | date |

## Signatures et types renvoyés

`toDateOnly(<date>)`

`toDateOnly(<string>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

## Exemples

`toDateOnly("2016-08-18")`

renvoie un objet dateOnly représentant 2016-08-18.
