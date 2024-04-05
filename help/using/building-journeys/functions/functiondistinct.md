---
product: journey optimizer
title: distinct
description: En savoir plus sur la fonction distinct
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinct, fonction, expression, parcours
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 100%

---

# distinct {#distinct}

Renvoie les valeurs ou objets distincts d’une liste donnée. Les entrées « null » sont ignorées.

## Catégorie

Liste

## Syntaxe de la fonction

`distinct(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | Chaîne | Ce paramètre est facultatif et uniquement pour listObject. Si le paramètre n’est pas fourni, un objet est considéré comme dupliqué si tous les attributs ont les mêmes valeurs. Dans le cas contraire, un objet est considéré comme dupliqué si l’attribut donné a la même valeur. |

## Signatures et types renvoyés

`distinct(<listInteger>)`

Renvoie une liste de nombres entiers.

`distinct(<listDecimal>)`

Renvoie une liste de nombres décimaux.

`distinct(<listString>)`

Renvoie une liste de chaînes.

`distinct(<listDateTimeOnly>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`distinct(<listDateTime>)`

Renvoie une liste de dates et heures.

`distinct(<listDateOnly>)`

Renvoie une liste de dates.

`distinct(<listBoolean>)`

Renvoie une liste de valeurs booléennes.

`distinct(<listDuration>)`

Renvoie une liste de durées.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Renvoie une liste d’objets.


## Exemples

`distinct([10,2,10,null])`

Renvoie `[10, 2]`.
