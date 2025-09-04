---
product: journey optimizer
title: startWith
description: En savoir plus sur la fonction startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, fonction, expression, parcours
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 100%

---

# startWith {#startWith}

Renvoie « true » si le deuxième paramètre est un préfixe du premier.

## Catégorie

Chaîne

## Syntaxe de la fonction

`startWith(<parameters>)`

## Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | chaîne |
| préfixe | chaîne |

## Signature et type renvoyé

`startWith(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`startWith("Hello World", "Hello")`

Renvoie true.

`startWith("Hello World", "World")`

Renvoie false.
