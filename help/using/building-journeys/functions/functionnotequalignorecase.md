---
product: journey optimizer
title: notEqualIgnoreCase
description: En savoir plus sur la fonction notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, fonction, expression, parcours
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 100%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Vérifie si la chaîne du premier argument est différente de la chaîne du deuxième argument, en ignorant les considérations de casse.

## Catégorie

Chaîne

## Syntaxe de la fonction

`notEqualIgnoreCase(<parameters>)`

## Paramètres

* Chaîne

## Signature et type renvoyé

`notEqualIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

## Exemple

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
