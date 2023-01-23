---
product: journey optimizer
title: distinctCountWithNull
description: En savoir plus sur la fonction distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, fonction, expression, parcours
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 94%

---

# distinctCountWithNull {#distinctCountWithNull}

Compte le nombre de valeurs différentes, y compris les valeurs « null ».

>[!NOTE]
>
>Si la liste cible est un listObject, cette fonction ne peut être utilisée que dans les expressions d’action personnalisées.

## Catégorie

Agrégation

## Syntaxe de la fonction

`distinctCountWithNull(<listAny>)`

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

`distinctCountWithNull(<listAny>)`

Renvoie un entier.

## Exemple

`distinctCountWithNull([10,2,10,null])`

Renvoie 3.
