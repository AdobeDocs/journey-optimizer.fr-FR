---
product: journey optimizer
title: toDateOnly
description: En savoir plus sur la fonction toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# toDateOnly{#toDateOnly}

Convertit un argument en une valeur de type dateOnly. Pour en savoir plus sur les types de données, reportez-vous à cette section [section](../expression/data-types.md).

## Catégorie

Conversion

## Syntaxe de la fonction

`toDateOnly(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Représentation sous forme de chaîne d’une date au format &quot;AAAA-MM-JJ&quot; (format XDM). Prend également en charge le format ISO-8601 : only **full-date** partie est prise en compte (voir [RFC 3339, section 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | string |
| date et heure | dateTime |
| date et heure sans fuseau horaire | dateTimeOnly |
| valeur entière d’une époque en millisecondes | entier |

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
