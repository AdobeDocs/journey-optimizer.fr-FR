---
product: adobe campaign
title: in
description: En savoir plus sur la fonction in
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 100%

---

# in {#in}

Vérifie si la valeur du premier argument figure dans la liste. La vérification est effectuée par l’intermédiaire d’un opérateur Equal sur chaque valeur d’argument. Elle renvoie true si la valeur de l’argument est trouvée, false dans le cas contraire.

Le type de l’`<expression>` doit correspondre aux éléments de la liste. Pour mémoire, les types d’éléments de la liste doivent correspondre les uns aux autres.

## Catégorie

Liste

## Syntaxe de la fonction

`in(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Chaîne | Chaîne |
| Booléen | Booléen |
| Nombre entier | Nombre entier |
| Décimal | Décimal |
| Durée | Durée |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |

## Signature et type renvoyé

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Renvoie une valeur booléenne.

## Exemple

`in(4,[4,5,3,4])`

Renvoie true.

`in(8,[4,5,3,4])`

Renvoie false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
