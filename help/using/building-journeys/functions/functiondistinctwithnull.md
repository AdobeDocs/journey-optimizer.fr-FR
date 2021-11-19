---
product: adobe campaign
title: distinctWithNull
description: En savoir plus sur la fonction distinctWithNull
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 95%

---

# distinctWithNull {#distinctWithNull}

Renvoie les valeurs distinctes de la liste. Si la liste comporte au moins une valeur « null », une valeur « null » est incluse dans la liste renvoyée.

## Catégorie

Liste

## Syntaxe de la fonction

`distinctWithNull(<parameter>)`

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

## Signatures et types renvoyés

`distinctWithNull(<listInteger>)`

Renvoie une liste de nombres entiers.

`distinctWithNull(<listDecimal>)`

Renvoie une liste de nombres décimaux.

`distinctWithNull(<listString>)`

Renvoie une liste de chaînes.

`distinctWithNull(<listDateTimeOnly>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`distinctWithNull(<listDateTime>)`

Renvoie une liste de dates et heures.

`distinctWithNull(<listDateOnly>)`

Renvoie une liste de dates.

`distinctWithNull(<listBoolean>)`

Renvoie une liste de valeurs booléennes.

`distinctWithNull(<listDuration>)`

Renvoie une liste de durées.

## Exemples

`distinctWithNull([10,2,10,null])`

Renvoie [10, 2, null]
