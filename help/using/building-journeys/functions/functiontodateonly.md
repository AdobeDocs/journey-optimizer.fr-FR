---
product: adobe campaign
title: toDateOnly
description: En savoir plus sur la fonction toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 100%

---

# toDateOnly{#toDateOnly}

Convertit un argument en une valeur de type dateOnly. Pour plus d’informations sur les types de données, consultez cette [section](../expression/data-types.md).

## Catégorie

Conversion

## Syntaxe de la fonction

`toDateOnly(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Représentation sous forme de chaîne d’une date au format « AAAA-MM-JJ » (format XDM). Prend également en charge le format ISO-8601 : seule la partie **full-date** est prise en compte (voir [RFC 3339, section 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | chaîne |
| date et heure | dateTime |
| date et heure sans prise en compte du fuseau horaire | dateTimeOnly |
| valeur entière d’une époque en millisecondes | nombre entier |

## Signatures et types renvoyés

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Renvoie une valeur de type dateOnly.

## Exemples

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

tous renvoient un objet dateOnly représentant 2016-08-18.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Renvoie une valeur dateOnly.
