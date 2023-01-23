---
product: journey optimizer
title: countWithNull
description: En savoir plus sur la fonction countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, fonction, expression, parcours
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 92%

---

# countWithNull {#countWithNull}

Compte tous les éléments de la liste, y compris les valeurs « null ».

## Catégorie

Agrégation

## Syntaxe de la fonction

`countWithNull(<listAny>)`

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

## Signature et type renvoyé

`countWithNull(<listAny>)`

Renvoie un entier.

## Exemple

`countWithNull([10,2,10,null])`

Renvoie 4.
