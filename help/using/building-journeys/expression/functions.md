---
solution: Journey Optimizer
product: journey optimizer
title: Fonctions
description: En savoir plus sur les fonctions
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: fonction, expressions, éditeur, parcours
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
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
| Agrégation | [avg](../functions/functionavg.md) |
| Agrégation | [count](../functions/functioncount.md) |
| Agrégation | [countOnlyNull](../functions/functioncountonlynull.md) |
| Agrégation | [countWithNull](../functions/functioncountwithnull.md) |
| Agrégation | [distinctCount](../functions/functiondistinctcount.md) |
| Agrégation | [distinctCountWithNull](../functions/functiondistinctcountwithnull.md) |
| Agrégation | [max](../functions/functionmax.md) |
| Agrégation | [min](../functions/functionmin.md) |
| Agrégation | [sum](../functions/functionsum.md) |
| Conversion | [toBool](../functions/functiontobool.md) |
| Conversion | [toDateOnly](../functions/functiontodateonly.md) |
| Conversion | [toDateTime](../functions/functiontodatetime.md) |
| Conversion | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| Conversion | [toDecimal](../functions/functiontodecimal.md) |
| Conversion | [toDuration](../functions/functiontoduration.md) |
| Conversion | [toInteger](../functions/functiontointeger.md) |
| Conversion | [toString](../functions/functiontostring.md) |
| Date | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| Date | [inLastDays](../functions/functioninlastdays.md) |
| Date | [inLastHours](../functions/functioninlasthours.md) |
| Date | [inLastMonths](../functions/functioninlastmonths.md) |
| Date | [inLastYears](../functions/functioninlastyears.md) |
| Date | [inNextDays](../functions/functioninnextdays.md) |
| Date | [inNextHours](../functions/functioninnexthours.md) |
| Date | [inNextMonths](../functions/functioninnextmonths.md) |
| Date | [inNextYears](../functions/functioninnextyears.md) |
| Date | [now](../functions/functionnow.md) |
| Date | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Date | [setHours](../functions/functionsethours.md) |
| Date | [setDays](../functions/functionsetdays.md) |
| Date | [updateTimeZone](../functions/functionupdatetimezone.md) |
| Liste | [distinct](../functions/functiondistinct.md) |
| Liste | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Liste | [filter](../functions/functionfilter.md) |
| Liste | [getListItem](../functions/functiongetlistitem.md) |
| Liste | [in](../functions/functionin.md) |
| Liste | [intersect](../functions/functionintersect.md) |
| Liste | [limit](../functions/functionlimit.md) |
| Liste | [listSize](../functions/functionlistsize.md) |
| Liste | [serializeList](../functions/functionserializelist.md) |
| Liste | [sort](../functions/functionsort.md) |
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
