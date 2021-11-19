---
product: adobe campaign
title: endWith
description: En savoir plus sur la fonction endWith
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 100%

---

# endWith {#endWith}

Renvoie « true » si le deuxième paramètre est un suffixe du premier.

## Catégorie

Chaîne

## Syntaxe de la fonction

`endWith(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
| suffixe | chaîne |

## Signature et type renvoyé

`endWith(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`endWith("Hello World", "World")`

Renvoie true.

`endWith("Hello World", "Hello")`

Renvoie false.
