---
product: journey optimizer
title: toDuration
description: En savoir plus sur la fonction toDuration
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c78e30c5-99ee-4dc7-a03a-17f7ee65f83a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# toDuration {#toDuration}

Convertit une valeur d’argument en une durée. Pour plus d’informations sur les types de données, reportez-vous à la section [cette page](../expression/data-types.md).

## Catégorie

Conversion

## Syntaxe de la fonction

`toDuration(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| string | Formats basés sur le format de durée ISO-8601 PnDTnHnMn.nS avec des jours considérés comme exactement 24 heures |
| entier | nombre de millisecondes |

Si expression de chaîne : Les formats acceptés sont basés sur le format de durée ISO-8601 PnDTnHnMn.nS avec des jours considérés comme étant exactement de 24 heures.

La chaîne commence par un signe facultatif, indiqué par le symbole ASCII négatif ou positif. Si elle est négative, toute la période est annulée. La lettre ASCII &quot;P&quot; est la suivante en majuscules ou en minuscules. Il existe ensuite quatre sections, chacune constituée d’un nombre et d’un suffixe. Les sections comportent des suffixes en ASCII de &quot;D&quot;, &quot;H&quot;, &quot;M&quot; et &quot;S&quot; pour les jours, heures, minutes et secondes, acceptés en majuscules ou en minuscules. Les suffixes doivent se produire dans l’ordre. La lettre ASCII &quot;T&quot; doit se produire avant la première occurrence, le cas échéant, d’une section d’heure, de minute ou de seconde. Au moins une des quatre sections doit être présente, et si &quot;T&quot; est présent, il doit y avoir au moins une section après &quot;T&quot;. La partie numérique de chaque section doit contenir un ou plusieurs chiffres ASCII. Le nombre peut être précédé du symbole ASCII négatif ou positif. Le nombre de jours, heures et minutes doit être analysé jusqu’au nombre de jours. Le nombre de secondes doit être analysé avec la fraction facultative. La virgule peut être un point ou une virgule. La partie fractionnaire peut comporter de zéro à 9 chiffres.

## Signatures et type renvoyé

`toDuration(<string>)`

`toDuration(<integer>)`

Renvoie une durée.

## Exemples

`toDuration("PT10H")`

Renvoie une durée de 10 heures.

`toDuration("PT4S")`

Renvoie une durée de 4 s.

`toDuration(4000)`

Renvoie une durée de 4 s.
