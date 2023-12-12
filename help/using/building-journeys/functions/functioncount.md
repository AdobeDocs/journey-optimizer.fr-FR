---
product: journey optimizer
title: count
description: En savoir plus sur la fonction count
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, fonction, expression, parcours
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: ad113c0414b20ac2f758ad06a44315b24a3d3d0c
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 100%

---

# count {#count}

Compte les éléments de la liste sans tenir compte des valeurs « null ».

## Catégorie

Agrégation

## Syntaxe de la fonction

`count(<listAny>)`

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

## Signatures et type renvoyé

`count(<listAny>)`

Renvoie un entier.

## Exemple

`count([10,2,10,null])`

Renvoie 3.
