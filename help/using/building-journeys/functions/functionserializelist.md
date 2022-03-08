---
product: adobe campaign
title: serializeList
description: En savoir plus sur la fonction serializeList
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 100%

---

# serializeList {#serializeList}

Convertit en chaîne la liste (tous types possibles) indiquée dans le premier paramètre. Le deuxième paramètre représente le séparateur à utiliser. Le troisième paramètre est une valeur booléenne indiquant si chaque élément de l’expression doit inclure des guillemets.

## Catégorie

Liste

## Syntaxe de la fonction

`serializeList(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Chaîne | Chaîne |
| Booléen | Booléen |
| DateTimeOnly | DateTimeOnly |
| Liste | listString |
| Liste | listBoolean |
| Liste | listPoint |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |

## Signature et type renvoyé

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

Renvoie une chaîne.

## Exemple

`serializeList(["Hello","World"], " ", false)`

Renvoie « Hello World ».

`serializeList(["Hello", "World"], ",", true)`

Renvoie « Hello », « World ».
