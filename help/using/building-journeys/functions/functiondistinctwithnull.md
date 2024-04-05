---
product: journey optimizer
title: distinctWithNull
description: En savoir plus sur la fonction distinctWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, fonction, expression, parcours
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 100%

---

# distinctWithNull {#distinctWithNull}

Renvoie les valeurs ou objets distincts d’une liste donnée. Si la liste comporte au moins une entrée « null », une entrée « null » est présente dans la liste renvoyée.

Notez que le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## Catégorie

Liste

## Syntaxe de la fonction

`distinctWithNull(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Liste à traiter. |

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
