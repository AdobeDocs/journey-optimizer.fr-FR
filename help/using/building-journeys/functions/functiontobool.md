---
product: journey optimizer
title: toBool
description: En savoir plus sur la fonction toBool
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# toBool {#toBool}

Convertit une valeur d’argument en valeur booléenne, selon son type.

* À partir de la chaîne : Essayez de convertir la valeur de chaîne en valeur booléenne, à partir de &quot;true&quot; si la valeur de chaîne est &quot;true&quot;, à partir de false dans le cas contraire.
* Numérique : true si la valeur numérique n’est pas égale à 0, false dans le cas contraire

## Catégorie

Conversion

## Syntaxe de la fonction

`toBool(<parameter>)`

## Paramètres

* décimal
* boolean
* string
* entier

## Signatures et types renvoyés

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Renvoie une valeur booléenne.

## Exemples

`toBool("true")`

`toBool(1)`

Renvoie true.

`toBool("this is not a boolean")`

Renvoie false.
