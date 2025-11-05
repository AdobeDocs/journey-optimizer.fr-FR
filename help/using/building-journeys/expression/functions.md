---
solution: Journey Optimizer
product: journey optimizer
title: Fonctions
description: En savoir plus sur les fonctions
feature: Journeys
role: Developer
level: Experienced
keywords: fonction, expressions, éditeur, parcours
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# Fonctions {#functions}

Une fonction peut avoir différentes signatures (ensemble différent de paramètres ordonnés). Une signature de fonction peut avoir de 0 à N expressions sous la forme de paramètres ordonnés.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

Chaque fonction renvoie une valeur de type spécifique.

Voici la liste des fonctions prises en charge :

## Fonctions principales

| Catégorie | Fonction |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| Agrégation | [avg](../functions/aggregation-functions.md#avg) |
| Agrégation | [count](../functions/aggregation-functions.md#count) |
| Agrégation | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| Agrégation | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| Agrégation | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| Agrégation | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| Agrégation | [max](../functions/aggregation-functions.md#max) |
| Agrégation | [min](../functions/aggregation-functions.md#min) |
| Agrégation | [sum](../functions/aggregation-functions.md#sum) |
| Conversion | [toBool](../functions/conversion-functions.md#toBool) |
| Conversion | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| Conversion | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Conversion | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Conversion | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Conversion | [toDuration](../functions/conversion-functions.md#toDuration) |
| Conversion | [toInteger](../functions/conversion-functions.md#toInteger) |
| Conversion | [toString](../functions/conversion-functions.md#toString) |
| Date | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| Date | [inLastDays](../functions/date-functions.md#inLastDays) |
| Date | [inLastHours](../functions/date-functions.md#inLastHours) |
| Date | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| Date | [inLastYears](../functions/date-functions.md#inLastYears) |
| Date | [inNextDays](../functions/date-functions.md#inNextDays) |
| Date | [inNextHours](../functions/date-functions.md#inNextHours) |
| Date | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| Date | [inNextYears](../functions/date-functions.md#inNextYears) |
| Date | [now](../functions/date-functions.md#now) |
| Date | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| Date | [setHours](../functions/date-functions.md#setHours) |
| Date | [setDays](../functions/date-functions.md#setDays) |
| Date | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
| Liste | [distinct](../functions/list-functions.md#distinct) |
| Liste | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Liste | [filter](../functions/list-functions.md#filter) |
| Liste | [getListItem](../functions/list-functions.md#getListItem) |
| Liste | [in](../functions/list-functions.md#in) |
| Liste | [intersect](../functions/list-functions.md#intersect) |
| Liste | [limit](../functions/list-functions.md#limit) |
| Liste | [listSize](../functions/list-functions.md#listSize) |
| Liste | [serializeList](../functions/list-functions.md#serializeList) |
| Liste | [sort](../functions/list-functions.md#sort) |
| Math | [random](../functions/functionrandom.md) |
| Math | [round](../functions/functionround.md) |
| Chaîne | [concat](../functions/functionconcat.md) |
| Chaîne | [contain](../functions/functioncontain.md) |
| Chaîne | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| Chaîne | [endWith](../functions/functionendwith.md) |
| Chaîne | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| Chaîne | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| Chaîne | [indexOf](../functions/functionindexof.md) |
| Chaîne | [isEmpty](../functions/functionisempty.md) |
| Chaîne | [isNotEmpty](../functions/functionisnotempty.md) |
| Chaîne | [lastIndexOf](../functions/functionlastindexof.md) |
| Chaîne | [length](../functions/functionlength.md) |
| Chaîne | [lower](../functions/functionlower.md) |
| Chaîne | [matchRegExp](../functions/functionmatchregexp.md) |
| Chaîne | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| Chaîne | [replace](../functions/functionreplace.md) |
| Chaîne | [replaceAll](../functions/functionreplaceall.md) |
| Chaîne | [split](../functions/functionsplit.md) |
| Chaîne | [startWith](../functions/functionstartwith.md) |
| Chaîne | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| Chaîne | [substr](../functions/functionsubstr.md) |
| Chaîne | [trim](../functions/functiontrim.md) |
| Chaîne | [upper](../functions/functionupper.md) |
| Chaîne | [uuid](../functions/functionuuid.md) |
