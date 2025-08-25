---
product: journey optimizer
title: replaceAll
description: En savoir plus sur la fonction replaceAll
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replaceAll, fonction, expression, parcours
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

---

# replaceAll {#replaceAll}

Remplace toutes les occurrences correspondant à la chaîne cible par la chaîne de remplacement dans la chaîne de base.

Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ». 

## Catégorie

Chaîne

## Syntaxe de la fonction

`replaceAll(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|--------------|
| base | chaîne |
| cible | string (RegExp) |
| remplacement | chaîne |

## Signature et type renvoyé

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Renvoie une chaîne.

## Exemple{#example}

`replaceAll("Hello World", "l", "x")`

Renvoie « Hexxo Worxd ».

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Reportez-vous à l’exemple de [cette page](../functions/functionreplace.md#example_2).
