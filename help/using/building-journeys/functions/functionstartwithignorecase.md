---
product: journey optimizer
title: startWithIgnoreCase
description: En savoir plus sur la fonction startWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase, fonction, expression, parcours
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Renvoie « true » si le deuxième paramètre est un préfixe du premier sans tenir compte de la casse.

## Catégorie

Chaîne

## Syntaxe de la fonction

`startWithIgnoreCase(<parameters>)`

## Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | chaîne |
| préfixe | chaîne |

## Signature et type renvoyé

`startWithIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`startWithIgnoreCase("rowing is great", "RO")`

Renvoie true.
