---
product: journey optimizer
title: toInteger
description: En savoir plus sur la fonction toInteger
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger, fonction, expression, parcours
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 100%

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
| chaîne | convertit la valeur de la chaîne en nombre entier |
| dateTime | convertit la date en millisecondes (nombre de millisecondes depuis le début de l’époque) |
| décimal | convertit la valeur d’argument en nombre entier en supprimant la partie décimale (exemple : 1,5 devient 1) |
| booléen | convertit la valeur booléenne en 1 si true, 0 si false |

## Signatures et type renvoyé

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Renvoie un nombre entier.

## Exemples

`toInteger("4")`

Renvoie 4.
