---
product: adobe campaign
title: startWithIgnoreCase
description: En savoir plus sur la fonction startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
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
