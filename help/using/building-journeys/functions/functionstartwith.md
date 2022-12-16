---
product: journey optimizer
title: startWith
description: En savoir plus sur la fonction startWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '43'
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
