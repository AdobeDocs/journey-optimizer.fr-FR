---
product: journey optimizer
title: Fonctions de date
description: Découvrir les fonctions de date
feature: Journeys
role: Developer
level: Experienced
keywords: date, fonctions, expression, parcours, heure
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: ht
source-wordcount: '791'
ht-degree: 100%

---

# Fonctions de date {#date-functions}

Les fonctions de date permettent de manipuler et d’utiliser des valeurs de date et d’heure dans vos expressions de parcours. Ces fonctions sont essentielles pour les conditions temporelles, la planification et les calculs temporels de vos parcours clientèle.

Utilisez les fonctions de date lorsque vous devez :

* Obtenir l’heure ou la date actuelle avec une gestion spécifique des fuseaux horaires ([now](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))
* Vérifie si une date se situe dans une période spécifique ([inLastDays](#inLastDays), [inLastHours](#inLastHours), [inLastMonths](#inLastMonths), [inLastYears](#inLastYears), [inNextDays](#inNextDays), [inNextHours](#inNextHours), [inNextMonths](#inNextMonths), [inNextYears](#inNextYears))
* Modifier les composants de date et d’heure ([setHours](#setHours), [setDays](#setDays), [updateTimeZone](#updateTimeZone))
* Effectuer des calculs et des comparaisons temporels
* Convertit entre différents formats et représentations temporels

Les fonctions de date apportent un contrôle précis sur la logique temporelle, ce qui vous permet de créer des conditions et des chemins de parcours sensibles au temps qui réagissent à des calendriers et à des plannings spécifiques.

## currentTimeInMillis {#currentTimeInMillis}

Renvoie l’heure actuelle en millisecondes depuis le début de l’époque.

+++Syntaxe

`currentTimeInMillis()`

+++

+++Paramètres

Cette fonction n’utilise aucun paramètre.

+++

+++Signatures et type renvoyé

`currentTimeInMillis()`

Renvoie un entier.

+++

+++Exemples

`currentTimeInMillis()`

Renvoie « 1544712617131 ».

+++

## inLastDays {#inLastDays}

Renvoie « true » si une valeur dateTime donnée est comprise entre maintenant et maintenant - delta jours.

+++Syntaxe

`inLastDays(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inLastDays(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.

+++

## inLastHours {#inLastHours}

Renvoie « true » si une date et une heure données sont comprises entre maintenant et maintenant - delta heures.

+++Syntaxe

`inLastHours(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inLastHours(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Renvoie true.

+++

## inLastMonths {#inLastMonths}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant - delta mois.

+++Syntaxe

`inLastMonths(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inLastMonths(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.

+++

## inLastYears {#inLastYears}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant - delta ans.

+++Syntaxe

`inLastYears(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inLastYears(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.

+++

## inNextDays {#inNextDays}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta jours.

+++Syntaxe

`inNextDays(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inNextDays(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.

+++

## inNextHours {#inNextHours}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta heures.

+++Syntaxe

`inNextHours(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inNextHours(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie true.

+++

## inNextMonths {#inNextMonths}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta mois.

+++Syntaxe

`inNextMonths(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inNextMonths(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Renvoie true.

+++

## inNextYears {#inNextYears}

Renvoie « true » si une date ou une valeur dateTime donnée est comprise entre maintenant et maintenant + delta ans.

+++Syntaxe

`inNextYears(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date et heure | dateTime |
| delta | Entier |

+++

+++Signatures et type renvoyé

`inNextYears(<dateTime>,<integer>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Renvoie true.

+++

## now {#now}

Renvoie la date actuelle au format date et heure. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

+++Syntaxe

`now(<parameter>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | Identifiant du fuseau horaire (facultatif) |

+++

+++Signatures et type renvoyé

`now()`

`now("<timeZone id>")`

Renvoie une valeur dateTime.

+++

+++Exemples

`now()`

Renvoie 2023-06-03T06:30Z.

`toString(now())`

Renvoie « 2023-06-03T06 :30Z ».

`now("Europe/Paris")`

Renvoie 2023-06-03T08:30+02:00.

+++

## nowWithDelta {#nowWithDelta}

Renvoie la date et l’heure actuelles, ainsi qu’un décalage. Si un identifiant de fuseau horaire est spécifié, le décalage de fuseau horaire est appliqué. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

+++Syntaxe

`nowWithDelta(<parameters>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| delta | valeur entière positive ou négative |
| partie de date | années, mois, jours, heures, minutes ou secondes sous forme de chaîne |
| identifiant de fuseau horaire | Représentation, sous forme de chaîne, de la valeur du fuseau horaire. Pour en savoir plus, voir [Types de données](../expression/data-types.md). L’identifiant de fuseau horaire doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ni d’une expression. |

+++

+++Signatures et type renvoyé

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Renvoie une valeur dateTime.

+++

+++Exemples

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Renvoie une valeur dateTime il y a exactement 2 heures.

+++

## setHours {#setHours}

Définit les heures d’une date ou d’une date sans prise en compte du fuseau horaire. Par exemple, si vous voulez attendre jusqu’à une certaine heure demain, vous pouvez forcer l’heure.

+++Syntaxe

`setHours(<parameter>)`

+++

+++Paramètres

| Paramètre | Type |
|--- |--- |
| date et heure | dateTime |
| date et heure sans prise en compte du fuseau horaire | dateTimeOnly |
| heures | entier |

+++

+++Signatures et type renvoyé

`setHours(<dateTime>,<hours>)`

Renvoie une date et une heure.

`setHours(<dateTimeOnly>,<hours>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

+++

+++Exemples

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Renvoie demain à 20:XY h, XY représentant le nombre de minutes au moment de lʼévaluation de lʼheure en cours. Si lʼévaluation se produit à 2:45 h, lʼheure renvoyée sera 20:45 h.

+++

## setDays {#setDays}

Définit le jour d’une date ou d’une date sans prise en compte du fuseau horaire. Par exemple, si vous voulez attendre jusqu’à un certain jour du mois, vous pouvez forcer le jour.

+++Syntaxe

`setDays(<parameter>)`

+++

+++Paramètres

| Paramètre | Type |
|--- |--- |
| date et heure | dateTime |
| date et heure sans prise en compte du fuseau horaire | dateTimeOnly |
|  jours | Entier |

+++

+++Signatures et type renvoyé

`setDays(<dateTime>,<days>)`

Renvoie une date et une heure.

`setDays(<dateTimeOnly>,<days>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

+++

+++Exemples

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Renvoie 2023-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Renvoie une nouvelle valeur de date et heure, avec un nouveau fuseau horaire au même instant.

+++Syntaxe

`updateTimeZone(<parameters>)`

+++

+++Paramètres

* identifiant de fuseau horaire : chaîne
* dateTime

+++

+++Signature et type renvoyé

`updateTimeZone(<dateTime>,<timeZone id>)`

Renvoie une date et une heure.

+++

+++Exemples

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Renvoie 2023-08-28T17:15:30.123+02:00.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Si la valeur du champ de date et d’heure est `2021-11-16T16:55:12.939318+01:00`, la fonction renvoie `2021-11-17T02:55:12.942115+11:00`.

+++

