---
product: journey optimizer
title: serializeList
description: En savoir plus sur la fonction serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, fonction, expression, parcours
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 100%

---

# serializeList {#serializeList}

Convertit une liste donnée (tout type sauf listObject) en chaîne.

## Catégorie

Liste

## Syntaxe de la fonction

`serializeList(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Liste à convertir en chaîne. |
| separator | Chaîne | Séparateur entre chaque élément de liste dans la chaîne de sortie. |
| addQuotes | Booléen | Ce paramètre indique si chaque élément de la chaîne de sortie doit inclure des guillemets (true) ou non (false). |

## Signature et type renvoyé

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Renvoie une chaîne.

## Exemple

`serializeList(["Hello","World"], " ", false)`

Renvoie « Hello World ».

`serializeList(["Hello", "World"], ",", true)`

Renvoie « Hello », « World ».
