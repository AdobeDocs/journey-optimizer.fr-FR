---
product: adobe campaign
title: toString
description: En savoir plus sur la fonction toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 100%

---

# toString {#toString}

Convertit une valeur d’argument en valeur de chaîne, selon son type. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

## Catégorie

Conversion

## Syntaxe de la fonction

`toString(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| dateTime | Convertit la date au format UTC |
| dateTimeOnly | Convertit la date au format UTC |
| durée | Convertit le paramètre dans le nombre de millisecondes correspondant sous forme de chaîne |
| nombre entier | Convertit la valeur en représentation sous forme de chaîne (1 devient « 1 ») |
| décimal | Convertit la valeur en représentation sous forme de chaîne (1,5 devient « 1,5 ») |
| booléen | Convertit la valeur booléenne en chaîne « true » si true, en chaîne « false » si false |

## Signatures et type renvoyé

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Renvoie une chaîne.

## Exemple

`toString(4)`

Renvoie « 4 ».
