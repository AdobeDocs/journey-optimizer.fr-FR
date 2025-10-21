---
product: journey optimizer
title: getListItem
description: En savoir plus sur la fonction gstListItem
feature: Journeys
role: Engineer
level: Experienced
keywords: getListItem, fonction, expression, parcours
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 100%

---

# getListItem {#gestListItem}

Renvoie l’élément de la liste à l’index donné.

## Catégorie

Liste

## Syntaxe de la fonction

`getListItem(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | Entier |

## Signatures et type renvoyé

`getListItem(<listInteger>,<index>)`

Renvoie un entier.

`getListItem(<listDecimal>,<index>)`

Renvoie une valeur décimale.

`getListItem(<listString>,<index>)`

Renvoie une chaîne.

`getListItem(<listDateTimeOnly>,<index>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

`getListItem(<listDateTime>,<index>)`

Renvoie une date et une heure.

`getListItem(<listDateOnly>,<index>)`

Renvoie une liste de dates.

`getListItem(<listBoolean>,<index>)`

Renvoie une valeur booléenne.

`getListItem(<listDuration>,<index>)`

Renvoie une durée.

## Exemple

`getListItem([10, 2, 3], 1)`

Renvoie « 2 »

`getListItem(["A", "B", "C"], 2)`
Renvoie « C »

Exemples avec un champ d’événement &#39;event.appVersion&#39; avec la valeur : « 20.45.2.3434 »

`split(@event{event.appVersion}, "\\.")`

Renvoie `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Renvoie « 20 »
