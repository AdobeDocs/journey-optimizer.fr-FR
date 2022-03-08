---
product: adobe campaign
title: countWithNull
description: En savoir plus sur la fonction countWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 100%

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
