---
product: journey optimizer
title: endWith
description: En savoir plus sur la fonction endWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: ht
source-wordcount: '43'
ht-degree: 100%

---

# endWith {#endWith}

Renvoie « true » si le deuxième paramètre est un suffixe du premier.

## Catégorie

Chaîne

## Syntaxe de la fonction

`endWith(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
| suffixe | chaîne |

## Signature et type renvoyé

`endWith(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`endWith("Hello World", "World")`

Renvoie true.

`endWith("Hello World", "Hello")`

Renvoie false.
