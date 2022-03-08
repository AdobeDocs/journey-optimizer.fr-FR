---
product: adobe campaign
title: containIgnoreCase
description: En savoir plus sur la fonction containIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
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
| chaîne recherché(e) | chaîne |

## Signature et type renvoyé

`containIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`containIgnoreCase("rowing is great", "GREAT")`

Renvoie true.
