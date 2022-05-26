---
product: adobe campaign
title: distinctWithNull
description: En savoir plus sur la fonction distinctWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 0facae9e7eafc9f6fcbefbdc6d5563322eaf1251
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 40%

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
| keyAttributeName | chaîne | Ce paramètre est facultatif et uniquement pour listObject. Si le paramètre n’est pas fourni, un objet est considéré comme dupliqué si tous les attributs ont les mêmes valeurs. Dans le cas contraire, un objet est considéré comme dupliqué si l’attribut donné a la même valeur. |

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

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

Renvoie une liste d’objets.

## Exemples

`distinctWithNull([10,2,10,null])`

Renvoie [10, 2, null]
