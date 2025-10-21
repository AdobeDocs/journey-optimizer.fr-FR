---
product: journey optimizer
title: limit
description: En savoir plus sur la fonction limit
feature: Journeys
role: Developer
level: Experienced
keywords: limite, fonction, expression, parcours
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 100%

---

# limit {#limit}

Renvoie les N premiers ou derniers éléments d’une liste.

## Catégorie

Liste

## Syntaxe de la fonction

`limit(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à prendre en compte. Pour listObject, il doit s’agir d’une référence de champ. |
| numberOfItems | Entier | Nombre d’éléments à renvoyer à partir de la liste donnée. |
| firstOrLastItems | Booléen | Ce paramètre est facultatif (true par défaut). true renvoie les premiers éléments. false renvoie les derniers éléments. |

## Signature et type renvoyé

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Renvoie une liste de chaînes.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Renvoie une liste de nombres entiers.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Renvoie une liste de nombres décimaux.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Renvoie une liste de valeurs booléennes.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Renvoie une liste de dates.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Renvoie une liste de dates et heures.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Renvoie une liste de durées.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Renvoie une liste d’objets.

## Exemple

`limit(["A", "B", "C", "D", "E"], 3)`

Renvoie `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Renvoie `["C","D","E"]`.
