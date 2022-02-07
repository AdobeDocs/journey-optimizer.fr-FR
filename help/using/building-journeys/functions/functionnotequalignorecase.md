---
product: adobe campaign
title: notEqualIgnoreCase
description: En savoir plus sur la fonction notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 100%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Vérifie si la chaîne du premier argument est différente de la chaîne du deuxième argument, en ignorant les considérations de casse.

## Catégorie

Chaîne

## Syntaxe de la fonction

`notEqualIgnoreCase(<parameters>)`

## Paramètres

* chaîne

## Signature et type renvoyé

`notEqualIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
