---
product: journey optimizer
title: Fonctions de conversion
description: En savoir plus sur les fonctions de conversion
feature: Journeys
role: Developer
level: Experienced
keywords: conversion, fonctions, expression, parcours, type, convertir
version: Journey Orchestration
source-git-commit: 451a9e1e5d5e6e1408849e8d1c5c9644a95359da
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 89%

---

# Fonctions de conversion {#conversion-functions}

Les fonctions de conversion vous permettent de transformer des données d’un type en un autre dans vos expressions de parcours. Ces fonctions sont essentielles pour garantir la compatibilité des données et une gestion appropriée des types de données lorsque vous travaillez avec différentes sources de données et opérations.

Utilisez des fonctions de conversion lorsque vous devez :

* Convertir les valeurs de chaîne en types numériques, booléens ou dates ([toInteger](#toInteger), [toDecimal](#toDecimal), [toBool](#toBool))
* Transformer les dates et heures entre différents formats et représentations ([toDateTime](#toDateTime), [toDateTimeOnly](#toDateTimeOnly), [toDateOnly](#toDateOnly))
* Convertir les valeurs numériques entre les types entier et décimal ([toInteger](#toInteger), [toDecimal](#toDecimal))
* Convertir les valeurs au format chaîne ([toString](#toString)) ou en durée ([toDuration](#toDuration))
* Assurer la compatibilité des types pour les comparaisons et les opérations
* Traiter les données provenant de sources externes qui peuvent avoir différents formats de type

Chaque fonction de conversion gère automatiquement les règles et les cas Edge spécifiques au type, ce qui rend la transformation des données plus fiable et plus prévisible dans vos expressions de parcours.

## toBool {#toBool}

Convertit une valeur d’argument en valeur booléenne, selon son type.

* À partir d’une chaîne : la fonction tente de convertir la valeur de chaîne en valeur booléenne. Renvoie true si la valeur de chaîne est « true », sinon renvoie false.
* À partir d’une valeur numérique : renvoie true si la valeur numérique n’est pas égale à 0, sinon renvoie false.

+++Syntaxe

`toBool(<parameter>)`

+++

+++Paramètres

* décimal
* booléen
* chaîne
* nombre entier

+++

+++Signatures et types renvoyés

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`toBool("true")`

`toBool(1)`

Renvoie true.

`toBool("this is not a boolean")`

Renvoie false.

+++

## toDateOnly {#toDateOnly}

Convertit un argument en une valeur de type dateOnly. Pour plus d’informations sur les types de données, consultez cette [section](../expression/data-types.md).

+++Syntaxe

`toDateOnly(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| Représentation sous forme de chaîne d’une date au format « AAAA-MM-JJ » (format XDM). Prend également en charge le format ISO-8601 : seule la partie **full-date** est prise en compte (voir [RFC 3339, section 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | chaîne |
| date et heure | dateTime |
| date et heure sans prise en compte du fuseau horaire | dateTimeOnly |
| valeur entière d’une époque en millisecondes | nombre entier |

+++

+++Signatures et types renvoyés

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Renvoie une valeur de type dateOnly.

+++

+++Exemples

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

renvoient tous un objet dateOnly représentant 18/08/2023.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Renvoie une valeur dateOnly.

+++

## toDateTime {#toDateTime}

Convertit les paramètres en une valeur de date et d’heure, selon leurs types.

+++Syntaxe

`toDateTime(<parameters>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | date et heure au format ISO-8601. Représentation sous forme de chaîne d’une heure avec des informations de fuseau horaire |
| Chaîne | id de fuseau horaire. Identifiant de fuseau horaire (par exemple, « UTC », « Europe/Paris ») |
| dateOnly | représente une date sans fuseau horaire, sous la forme année-mois-jour |
| dateTimeOnly | représente une valeur datetime sans fuseau horaire, affichée sous la forme année-mois-jour-heure-minute-seconde-milliseconde |
| Entier | valeur entière d’une époque en millisecondes |

+++

+++Signatures et types renvoyés

`toDateTime(<string>)`

`toDateTime(<string>, <dateOnly>)`

`toDateTime(<string>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Renvoie une valeur **dateTime**.

+++

+++Exemples

`toDateTime("2023-08-18T23:17:59.123Z")`

Renvoie 2023-08-18T23:17:59.123Z.

La chaîne ISO-8601 inclut déjà des informations sur le fuseau horaire.

`toDateTime("Europe/Paris", toDateOnly("2023-08-18"))`

Renvoie 2023-08-18T00:00:00.000+02:00

Vous créez ainsi une valeur dateTime en combinant un fuseau horaire avec une valeur de date seule. L’heure est définie sur minuit (00:00:00) dans le fuseau horaire spécifié.

`toDateTime("UTC", toDateTimeOnly("2023-08-18T23:17:59.123"))`

Renvoie 2023-08-18T23:17:59.123Z.

Cela crée une valeur dateTime en appliquant un fuseau horaire à une valeur dateTimeOnly (qui ne contient aucune information de fuseau horaire).

`toDateTime(1560762190189)`

Renvoie 2019-06-17T09:03:10.189Z

Convertit une date et une heure Unix en millisecondes en une valeur dateTime.

+++

>[!NOTE]
>
>L’identifiant de fuseau horaire doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ni d’une expression. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

## toDateTimeOnly {#toDateTimeOnly}

Convertit une valeur d’argument en une date et une heure sans prise en compte du fuseau horaire.

+++Syntaxe

`toDateTimeOnly(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure au format ISO-8601 ou AAAA-MM-JJ (format de date XDM) | chaîne |
| date et heure | dateTime |

+++

+++Signatures et types renvoyés

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

+++

+++Exemples

`toDateTimeOnly ("2023-08-18")`

Renvoie une valeur dateTime représentant 2023-08-18T00:00:00.000.

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

Convertit une valeur d’argument en valeur décimale, selon son type.

+++Syntaxe

`toDecimal(<parameter>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | convertit la valeur de la chaîne en valeur décimale |
| dateTime | convertit la date en millisecondes (nombre de millisecondes depuis le début de l’époque) |
| booléen | convertit la valeur booléenne en 1 si true, 0 si false |
| nombre entier | convertit en valeur décimale (exemple :1 devient 1,0) |

+++

+++Signatures et types renvoyés

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Renvoie une valeur décimale.

+++

+++Exemples

`toDecimal("4.0")`

Renvoie 4.0.

+++

## toDuration {#toDuration}

Convertit une valeur d’argument en une durée. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

+++Syntaxe

`toDuration(<parameter>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | Formats basés sur le format de durée ISO-8601 PnDTnHnMn.nS pour une durée du jour considérée comme durant exactement 24 heures |
| nombre entier | nombre de millisecondes |

Si l’expression contient une chaîne : les formats acceptés sont basés sur le format de durée ISO-8601 PnDTnHnMn.nS pour une durée du jour considérée comme durant exactement 24 heures.

La chaîne commence par un signe facultatif, indiqué par le symbole ASCII négatif ou positif. S’il est négatif, toute la période est annulée. Vient ensuite la lettre ASCII « P », en majuscule ou en minuscule. Viennent ensuite quatre sections, chacune constituée d’un nombre et d’un suffixe. Les sections contiennent les suffixes en ASCII « D », « H », « M » et « S » pour les jours, heures, minutes et secondes, acceptés en majuscules ou en minuscules. Les suffixes doivent se succéder dans l’ordre. La lettre ASCII « T » doit apparaître avant la première occurrence, le cas échéant, d’une section d’heure, de minute ou de seconde. L’une au moins des quatre sections doit être présente, et si la lettre « T » est présente, elle doit être suivie d’au moins une section. La partie numérique de chaque section doit contenir un ou plusieurs chiffres ASCII. Le nombre peut être précédé du symbole ASCII négatif ou positif. Le nombre de jours, heures et minutes doit être converti en nombre long. Le nombre de secondes doit être converti en nombre long avec la fraction facultative. La virgule peut être un point ou une virgule. La partie fractionnaire peut comporter de zéro à 9 chiffres.

+++

+++Signatures et type renvoyé

`toDuration(<string>)`

`toDuration(<integer>)`

Renvoie une durée.

+++

+++Exemples

`toDuration("PT10H")`

Renvoie une durée de 10 heures.

`toDuration("PT4S")`

Renvoie une durée de 4 s.

`toDuration(4000)`

Renvoie une durée de 4 s.

+++

## toInteger {#toInteger}

Convertit une valeur d’argument en nombre entier.

+++Syntaxe

`toInteger(<parameter>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | convertit la valeur de la chaîne en nombre entier |
| dateTime | convertit la date en millisecondes (nombre de millisecondes depuis le début de l’époque) |
| décimal | convertit la valeur d’argument en nombre entier en supprimant la partie décimale (exemple : 1,5 devient 1) |
| booléen | convertit la valeur booléenne en 1 si true, 0 si false |

+++

+++Signatures et type renvoyé

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Renvoie un nombre entier.

+++

+++Exemples

`toInteger("4")`

Renvoie 4.

+++

## toString {#toString}

Convertit une valeur d’argument en valeur de chaîne, selon son type. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

+++Syntaxe

`toString(<parameter>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| dateTime | Convertit la date au format UTC |
| dateTimeOnly | Convertit la date au format UTC |
| durée | Convertit le paramètre dans le nombre de millisecondes correspondant sous forme de chaîne |
| Entier | Convertit la valeur en représentation sous forme de chaîne (1 devient « 1 »). |
| Décimal | Convertit la valeur en représentation sous forme de chaîne (1,5 devient « 1,5 »). |
| Booléen | Convertit la valeur booléenne en chaîne « true » si true, en chaîne « false » si false |

+++

+++Signatures et type renvoyé

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Renvoie une chaîne.

+++

+++Exemples

`toString(4)`

Renvoie « 4 ».

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Renvoie la représentation sous forme de chaîne du champ dateOnly (champ de date XDM) donné, par exemple « 18/08/2023 ».

`toString(toDuration(1520))`

Renvoie « PT1.52S ».

+++

