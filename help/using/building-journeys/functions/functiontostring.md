---
product: journey optimizer
title: toString
description: En savoir plus sur la fonction toString
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString, fonction, expression, parcours
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: ht
source-wordcount: '128'
ht-degree: 100%

---

# toString {#toString}

Convertit une valeur d’argument en valeur de chaîne, selon son type. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

## Catégorie

Conversion

## Syntaxe de la fonction

`toString(<parameter>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| dateTime | Convertit la date au format UTC |
| dateTimeOnly | Convertit la date au format UTC |
| durée | Convertit le paramètre dans le nombre de millisecondes correspondant sous forme de chaîne |
| Entier | Convertit la valeur en représentation sous forme de chaîne (1 devient « 1 »). |
| Décimal | Convertit la valeur en représentation sous forme de chaîne (1,5 devient « 1,5 »). |
| Booléen | Convertit la valeur booléenne en chaîne « true » si true, en chaîne « false » si false |

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

Renvoie « 4 ».

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Renvoie la représentation sous forme de chaîne du champ dateOnly (champ de date XDM) donné, par exemple « 18/08/2023 ».

`toString(toDuration(1520))`

Renvoie « PT1.52S ».
