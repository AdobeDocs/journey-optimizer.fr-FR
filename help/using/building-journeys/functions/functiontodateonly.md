---
product: journey optimizer
title: toDateOnly
description: En savoir plus sur la fonction toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, fonction, expression, parcours
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 96%

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

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

tous renvoient un objet dateOnly représentant 18/08/2023.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Renvoie une valeur dateOnly.
