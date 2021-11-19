---
product: adobe campaign
title: count
description: En savoir plus sur la fonction count
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 100%

---

# count {#count}

Compte les éléments de la liste sans tenir compte des valeurs « null ».

## Catégorie

Agrégation

## Syntaxe de la fonction

`count(<listAny>)`

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

## Signatures et type renvoyé

`count(<listAny>)`

Renvoie un entier.

## Exemple

`count([10,2,10,null])`

Renvoie 3.
