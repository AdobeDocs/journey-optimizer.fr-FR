---
product: journey optimizer
title: countWithNull
description: En savoir plus sur la fonction countWithNull
feature: Journeys
role: Developer
level: Experienced
keywords: countWithNull, fonction, expression, parcours
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
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
