---
product: journey optimizer
title: toString
description: En savoir plus sur la fonction toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# toString {#toString}

Convertit une valeur d’argument en valeur string, selon son type. Pour plus d’informations sur les types de données, reportez-vous à la section [cette page](../expression/data-types.md).

## Catégorie

Conversion

## Syntaxe de la fonction

`toString(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| dateTime | convertit la date au format UTC date |
| dateTimeOnly | convertit la date au format UTC date |
| durée | Convertir en nombre de millisecondes correspondant sous forme de chaîne |
| entier | convertit la valeur en représentation sous forme de chaîne (1 devient &quot;1&quot;) |
| décimal | convertit la valeur en représentation sous forme de chaîne (1,5 devient &quot;1,5&quot;) |
| boolean | Convertit la valeur booléenne en &quot;true&quot; si true, &quot;false&quot; si false |

## Signatures et type renvoyé

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Renvoie une chaîne.

## Exemple

`toString(4)`

Renvoie &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Renvoie la représentation sous forme de chaîne du champ dateOnly donné (champ XDM Date), par exemple &quot;2016-08-18&quot;.
