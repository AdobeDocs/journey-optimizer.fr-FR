---
product: journey optimizer
title: split
description: En savoir plus sur la fonction split
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: split, fonction, expression, parcours
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 07682901ec94d5b736d364130aaf48f9dfe982a3
workflow-type: ht
source-wordcount: '67'
ht-degree: 100%

---

# split {#split}

Partage la première chaîne d’arguments avec une chaîne de séparateur (deuxième chaîne d’arguments, qui peut être une expression régulière) pour produire une liste de chaînes (jetons).

## Catégorie

Chaîne

## Syntaxe de la fonction

`split(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne d’entrée | chaîne |
| chaîne de séparateur | chaîne |

## Signatures et type renvoyé

`split(<input string>, <separator string>)`

Renvoie une fonction listString.

## Exemple

`split("A_B_C", "_")`

Renvoie `["A","B","C"]`

Exemple avec un champ d’événement &#39;event.appVersion&#39; avec la valeur : « 20.45.2.3434 »

`split(@{event.appVersion}, "\\.")`

Renvoie `["20", "45", "2", "3434"]`
