---
product: journey optimizer
title: setHours
description: En savoir plus sur la fonction setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, fonction, expression, parcours
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

---

# setHours {#setHours}

Définit les heures d’une date ou d’une date sans prise en compte du fuseau horaire. Par exemple, si vous voulez attendre jusqu’à une certaine heure demain, vous pouvez forcer l’heure.

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

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Renvoie demain à 20:XY h, XY représentant le nombre de minutes au moment de lʼévaluation de lʼheure en cours. Si lʼévaluation se produit à 2:45 h, lʼheure renvoyée sera 20:45 h.
