---
product: journey optimizer
title: distinctCountWithNull
description: En savoir plus sur la fonction distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, fonction, expression, parcours
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 100%

---

# distinctCountWithNull {#distinctCountWithNull}

Compte le nombre de valeurs différentes, y compris les valeurs « null ».

Notez que le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## Catégorie

Agrégation

## Syntaxe de la fonction

`distinctCountWithNull(<listAny>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Signature et type renvoyé

`distinctCountWithNull(<listAny>)`

Renvoie un entier.

## Exemple

`distinctCountWithNull([10,2,10,null])`

Renvoie 3.
