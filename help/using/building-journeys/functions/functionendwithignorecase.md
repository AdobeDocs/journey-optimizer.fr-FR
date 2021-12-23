---
product: adobe campaign
title: endWithIgnoreCase
description: En savoir plus sur la fonction endWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '48'
ht-degree: 100%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Vérifie si la chaîne du premier argument se termine par une chaîne spécifique (chaîne du deuxième argument), sans tenir compte de la casse.

## Catégorie

Chaîne

## Syntaxe de la fonction

`endWithIgnoreCase(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
| suffixe | chaîne |

## Signature et type renvoyé

`endWithIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`endWithIgnoreCase("rowing is great", "AT")`

Renvoie true.
