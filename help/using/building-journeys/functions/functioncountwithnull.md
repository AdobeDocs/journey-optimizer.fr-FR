---
product: journey optimizer
title: countWithNull
description: En savoir plus sur la fonction countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, fonction, expression, parcours
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 100%

---

# countWithNull {#countWithNull}

Compte tous les éléments de la liste, y compris les valeurs « null ».

Notez que le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## Catégorie

Agrégation

## Syntaxe de la fonction

`countWithNull(<listAny>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Signature et type renvoyé

`countWithNull(<listAny>)`

Renvoie un entier.

## Exemple

`countWithNull([10,2,10,null])`

Renvoie 4.
