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
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
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
| Chaîne | [concat](../functions/string-functions.md#concat) |
| Chaîne | [contain](../functions/string-functions.md#contain) |
| Chaîne | [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) |
| Chaîne | [endWith](../functions/string-functions.md#endWith) |
| Chaîne | [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) |
| Chaîne | [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) |
| Chaîne | [indexOf](../functions/string-functions.md#indexOf) |
| Chaîne | [isEmpty](../functions/string-functions.md#isEmpty) |
| Chaîne | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| Chaîne | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| Chaîne | [length](../functions/string-functions.md#length) |
| Chaîne | [lower](../functions/string-functions.md#lower) |
| Chaîne | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| Chaîne | [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) |
| Chaîne | [replace](../functions/string-functions.md#replace) |
| Chaîne | [replaceAll](../functions/string-functions.md#replaceAll) |
| Chaîne | [split](../functions/string-functions.md#split) |
| Chaîne | [startWith](../functions/string-functions.md#startWith) |
| Chaîne | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| Chaîne | [substr](../functions/string-functions.md#substr) |
| Chaîne | [trim](../functions/string-functions.md#trim) |
| Chaîne | [upper](../functions/string-functions.md#upper) |
| Chaîne | [uuid](../functions/string-functions.md#uuid) |
