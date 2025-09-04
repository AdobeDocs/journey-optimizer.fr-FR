---
product: journey optimizer
title: concat
description: En savoir plus sur la fonction concat
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat, fonction, expression, parcours
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '44'
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
| chaîne | Chaîne |

## Signature et type renvoyé

`concat(<string>,<string>)`

`concat(<listString>)`

Renvoie une chaîne.

## Exemple

`concat("Hello","World")`

Renvoie « HelloWorld ».

`concat(["Hello"," ","World"])`

Renvoie « Hello World ».
