---
product: journey optimizer
title: toInteger
description: En savoir plus sur la fonction toInteger
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# toInteger {#toInteger}

Convertit une valeur d’argument en nombre entier.

## Catégorie

Conversion

## Syntaxe de la fonction

`toInteger(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| string | convertit la valeur de chaîne en entier |
| dateTime | convertit la date en millisecondes (nombre de millisecondes de l’époque) |
| décimal | convertit en entier en supprimant la partie décimale (exemple : 1,5 devient 1) |
| boolean | convertit la valeur booléenne en 1 si true, 0 si false |

## Signatures et type renvoyé

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Renvoie un entier.

## Exemples

`toInteger("4")`

Renvoie 4.
