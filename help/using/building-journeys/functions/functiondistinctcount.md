---
product: journey optimizer
title: distinctCount
description: En savoir plus sur la fonction distinctCount
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 100%

---

# distinctCount{#distinctCount}

Compte le nombre de valeurs différentes en ignorant les valeurs « null ».

## Catégorie

Agrégation

## Syntaxe de la fonction

`distinctCount(<listAny>)`

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

`distinctCount(<listAny>)`

Renvoie un entier.

## Exemple

`distinctCount([10,2,10,null])`

Renvoie 2.
