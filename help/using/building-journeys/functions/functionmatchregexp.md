---
product: journey optimizer
title: matchRegExp
description: En savoir plus sur la fonction matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---

# matchRegExp {#matchRegExp}

Renvoie true si la chaîne du premier paramètre correspond à l’expression régulière du deuxième paramètre. Pour plus d’informations, voir [cette page](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Catégorie

Chaîne

## Syntaxe de la fonction

`matchRegExp(<parameters>)`

## Paramètres

| Paramètre | Type |
|--- |--- |
| string | string |
| regexp | string |

## Signature et type renvoyé

`matchRegExp(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`matchRegExp("username@adobe.com", "*adobe")`

Renvoie true.
