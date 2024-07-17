---
product: journey optimizer
title: endWith
description: En savoir plus sur la fonction endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, fonction, expression, parcours
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
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
