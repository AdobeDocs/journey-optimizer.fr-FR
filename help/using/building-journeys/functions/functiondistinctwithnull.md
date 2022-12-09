---
product: journey optimizer
title: distinctWithNull
description: En savoir plus sur la fonction distinctWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# distinctWithNull {#distinctWithNull}

Renvoie les valeurs ou objets distincts d’une liste donnée. Si la liste comporte au moins une entrée null, une entrée null sera présente dans la liste renvoyée.

## Catégorie

Liste

## Syntaxe de la fonction

`distinctWithNull(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | string | Ce paramètre est facultatif et uniquement pour listObject. Si le paramètre n’est pas fourni, un objet est considéré comme dupliqué si tous les attributs ont les mêmes valeurs. Dans le cas contraire, un objet est considéré comme dupliqué si l’attribut donné a la même valeur. |

## Signatures et types renvoyés

`distinctWithNull(<listInteger>)`

Renvoie une liste de nombres entiers.

`distinctWithNull(<listDecimal>)`

Renvoie une liste de décimales.

`distinctWithNull(<listString>)`

Renvoie une liste de chaînes.

`distinctWithNull(<listDateTimeOnly>)`

Renvoie une liste de dates et heures sans prendre en compte le fuseau horaire.

`distinctWithNull(<listDateTime>)`

Renvoie une liste de dates et heures.

`distinctWithNull(<listDateOnly>)`

Renvoie une liste de dates.

`distinctWithNull(<listBoolean>)`

Renvoie une liste de valeurs booléennes.

`distinctWithNull(<listDuration>)`

Renvoie une liste de durées.

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

Renvoie une liste d’objets.

## Exemples

`distinctWithNull([10,2,10,null])`

Renvoie [10, 2, null]
