---
product: journey optimizer
title: matchRegExp
description: En savoir plus sur la fonction matchRegExp
feature: Journeys
role: Developer
level: Experienced
keywords: matchRegExp, fonction, expression, parcours
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 100%

---

# matchRegExp {#matchRegExp}

Renvoie « true » si la chaîne du premier paramètre correspond à l’expression régulière du second paramètre. Pour plus d’informations, consultez [cette page](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Catégorie

Chaîne

## Syntaxe de la fonction

`matchRegExp(<parameters>)`

## Paramètres

| Paramètre | Type |
|--- |--- |
| chaîne | chaîne |
| regexp | chaîne |

## Signature et type renvoyé

`matchRegExp(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`matchRegExp("12345", "\\d+")`

Renvoie true.
