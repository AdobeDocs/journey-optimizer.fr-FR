---
product: journey optimizer
title: containIgnoreCase
description: En savoir plus sur la fonction containIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: containIgnoreCase, fonction, expression, parcours
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '52'
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
| chaîne recherchée | Chaîne |

## Signature et type renvoyé

`containIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`containIgnoreCase("rowing is great", "GREAT")`

Renvoie true.
