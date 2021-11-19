---
product: adobe campaign
title: startWithIgnoreCase
description: En savoir plus sur la fonction startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 100%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Renvoie « true » si le deuxième paramètre est un préfixe du premier sans tenir compte de la casse.

## Catégorie

Chaîne

## Syntaxe de la fonction

`startWithIgnoreCase(<parameters>)`

## Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | chaîne |
| préfixe | chaîne |

## Signature et type renvoyé

`startWithIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`startWithIgnoreCase("rowing is great", "RO")`

Renvoie true.
