---
product: journey optimizer
title: toBool
description: En savoir plus sur la fonction toBool
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool, fonction, expression, parcours
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '78'
ht-degree: 100%

---

# toBool {#toBool}

Convertit une valeur d’argument en valeur booléenne, selon son type.

* À partir d’une chaîne : la fonction tente de convertir la valeur de chaîne en valeur booléenne. Renvoie true si la valeur de chaîne est « true », sinon renvoie false.
* À partir d’une valeur numérique : renvoie true si la valeur numérique n’est pas égale à 0, sinon renvoie false.

## Catégorie

Conversion

## Syntaxe de la fonction

`toBool(<parameter>)`

## Paramètres

* décimal
* booléen
* chaîne
* nombre entier

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
