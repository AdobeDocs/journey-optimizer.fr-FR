---
product: journey optimizer
title: updateTimeZone
description: En savoir plus sur la fonction updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone, fonction, expression, parcours
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 92%

---

# updateTimeZone {#updateTimeZone}

Renvoie une nouvelle valeur de date et heure, avec un nouveau fuseau horaire au même instant.

## Catégorie

Date

## Syntaxe de la fonction

`updateTimeZone(<parameters>)`

## Paramètres

* identifiant de fuseau horaire : chaîne
* dateTime

## Signature et type renvoyé

`updateTimeZone(<dateTime>,<timeZone id>)`

Renvoie une date et une heure.

## Exemples

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Renvoie 2019-08-28T17:15:30.123+02:00.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@{MyExpEvent.timestamp}, "Australia/Sydney")`

Si la valeur du champ d’horodatage est `2021-11-16T16:55:12.939318+01:00`, la fonction renvoie `2021-11-17T02:55:12.942115+11:00`. 
