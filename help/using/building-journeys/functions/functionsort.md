---
product: adobe campaign
title: sort
description: En savoir plus sur la fonction sort
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 100%

---

# sort {#sort}

Trie une liste de valeurs dans l’ordre naturel. Le premier argument est la liste des valeurs, le second est une valeur booléenne indiquant si le tri est croissant (true) ou décroissant (false).

## Catégorie

Liste

## Syntaxe de la fonction

`sort(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |
| Booléen | Booléen |

## Signature et type renvoyé

`sort(<listInteger>,<boolean>)`

Renvoie une liste de nombres entiers.

`sort(<listDecimal>,<boolean>)`

Renvoie une liste de nombres décimaux.

`sort(<listString>,<boolean>)`

Renvoie une liste de chaînes.

`sort(<listDateTimeOnly>,<boolean>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`sort(<listDateTime>,<boolean>)`

Renvoie une liste de dates et heures.

`sort(<listDateOnly>,<boolean>)`

Renvoie une liste de dates.

`sort(<listBoolean>,<boolean>)`

Renvoie une liste de valeurs booléennes.

## Exemple

`sort(["A", "C", "B"], true)`

Renvoie `["A","B","C"]`.

`sort([1, 3, 2], false)`

Renvoie `[3, 2, 1]`.
