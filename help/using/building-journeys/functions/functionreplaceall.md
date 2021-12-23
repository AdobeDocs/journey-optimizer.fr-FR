---
product: adobe campaign
title: replaceAll
description: En savoir plus sur la fonction replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '75'
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
| cible | chaîne |
| remplacement | chaîne |

## Signature et type renvoyé

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Renvoie une chaîne.

## Exemple

`replaceAll("Hello World", "l", "x")`

Renvoie « Hexxo Worxd ».
