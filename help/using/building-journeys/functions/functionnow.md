---
product: journey optimizer
title: now
description: En savoir plus sur la fonction now
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: now, fonction, expression, parcours
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 92%

---

# now {#now}

Renvoie la date actuelle au format date et heure. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

## Catégorie

Date

## Syntaxe de la fonction

`now(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne |  |

## Signatures et type renvoyé

`now()`

`now("<timeZone id>")`

Renvoie une valeur dateTime.

## Exemples

`now()`

Renvoie 2019-06-03T06:30Z.

`toString(now())`

Renvoie « 2019-06-03T06:30Z »

`now("Europe/Paris")`

Renvoie 2019-06-03T08:30+02:00.
