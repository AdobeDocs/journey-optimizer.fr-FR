---
product: journey optimizer
title: split
description: En savoir plus sur la fonction split
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# split {#split}

Divise la première chaîne d’argument avec une chaîne de séparateur (deuxième chaîne d’argument, qui peut être une expression régulière) pour produire une liste de chaînes (jetons).

## Catégorie

Chaîne

## Syntaxe de la fonction

`split(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne d’entrée | string |
| chaîne de séparateur | string |

## Signatures et type renvoyé

`split(<input string>, <separator string>)`

Renvoie une listString.

## Exemple

`split(["A_B_C"], "_")`

Renvoie `["A","B","C"]`

Exemple avec un champ d’événement &quot;event.appVersion&quot; avec la valeur : &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Renvoie `["20", "45", "2", "3434"]`
