---
product: journey optimizer
title: containIgnoreCase
description: En savoir plus sur la fonction containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase, fonction, expression, parcours
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 92%

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
