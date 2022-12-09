---
product: journey optimizer
title: setHours
description: En savoir plus sur la fonction setHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setHours {#setHours}

Définit les heures d’une date ou d’une date uniquement. Par exemple, si vous souhaitez attendre jusqu’à une certaine heure demain, vous pouvez forcer l’heure.

## Catégorie

Date

## Syntaxe de la fonction

`setHours(<parameter>)`

## Paramètres

| Paramètre | Type |
|--- |--- |
| date et heure | dateTime |
| date et heure sans prise en compte du fuseau horaire | dateTimeOnly |
| heures | entier |

## Signatures et type renvoyé

`setHours(<dateTime>,<hours>)`

Renvoie une date et une heure.

`setHours(<dateTimeOnly>,<hours>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

## Exemples

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Renvoie 2010-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Renvoie demain à 20 h, X étant les minutes au moment de l’évaluation de l’heure actuelle. Si l’évaluation a lieu à 02h45, l’heure renvoyée est 08h45.
