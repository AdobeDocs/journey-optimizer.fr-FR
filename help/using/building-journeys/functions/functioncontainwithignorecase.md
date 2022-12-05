---
product: journey optimizer
title: containIgnoreCase
description: En savoir plus sur la fonction containIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# containIgnoreCase {#containIgnoreCase}

Vérifie si la chaîne du deuxième argument est contenue dans la chaîne du premier argument, sans tenir compte de la casse.

## Catégorie

Chaîne

## Syntaxe de la fonction

`containIgnoreCase(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
| chaîne recherchée | chaîne |

## Signature et type renvoyé

`containIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`containIgnoreCase("rowing is great", "GREAT")`

Renvoie true.
