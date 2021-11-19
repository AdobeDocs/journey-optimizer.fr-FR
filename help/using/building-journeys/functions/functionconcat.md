---
product: adobe campaign
title: concat
description: En savoir plus sur la fonction concat
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 100%

---

# concat {#concat}

Concatène deux paramètres de chaîne ou une liste de chaînes.

## Catégorie

Chaîne

## Syntaxe de la fonction

`concat(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Liste | listString |
| chaîne | chaîne |

## Signature et type renvoyé

`concat(<string>,<string>)`

`concat(<listString>)`

Renvoie une chaîne.

## Exemple

`concat("Hello","World")`

Renvoie « HelloWorld ».

`concat(["Hello"," ","World"])`

Renvoie « Hello World ».
