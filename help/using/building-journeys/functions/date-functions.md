---
product: journey optimizer
title: Fonctions de date
description: En savoir plus sur les fonctions de date
feature: Journeys
role: Developer
level: Experienced
keywords: date, fonctions, expression, parcours, heure
version: Journey Orchestration
exl-id: 68c102c1-f1c7-44b7-893f-9a3b7e0854b6
TQID: https://experienceleague.adobe.com/C2Z5SufckUxCNf9TsloziZS-Q3KPzmgMVNGJGiwDQ08
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 834
ht-degree: 0%

---

# Fonctions de date {#date-functions}

Les fonctions de date vous permettent de manipuler et d’utiliser des valeurs de date et d’heure dans vos expressions de parcours. Ces fonctions sont essentielles pour les conditions temporelles, la planification et les calculs temporels de vos parcours client.

Utilisez des fonctions de date lorsque vous devez :

* Obtenez l’heure ou la date actuelles avec une gestion spécifique des fuseaux horaires ([now](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))
* Vérifiez si une date se situe dans une plage de temps spécifique ([inLastDays](#inLastDays), [inLastHours](#inLastHours), [inLastMonths](#inLastMonths), [inLastYears](#inLastYears), [inNextDays](#inNextDays), [inNextHours](#inNextHours), [inNextMonths](#inNextMonths), [inNextYears](#inNextYears))
* Modifier les composants de date et d’heure ([setHours](#setHours), [setDays](#setDays), [updateTimeZone](#updateTimeZone))
* Effectuer des calculs et des comparaisons temporels
* Conversion entre différents formats d&#39;heure et représentations

Les fonctions de date fournissent un contrôle précis sur la logique temporelle, ce qui vous permet de créer des conditions et des chemins de parcours sensibles au temps qui répondent à des périodes et à des plannings spécifiques.

>[!NOTE]
>
>Les fonctions de cette page sont disponibles dans les expressions de parcours. Certaines fonctions telles que `now()` ne sont pas disponibles dans l’éditeur de personnalisation du contenu des e-mails. [&#x200B; En savoir plus &#x200B;](../../personalization/functions/dates.md)

## currentTimeInMillis {#currentTimeInMillis}

Renvoie l’heure actuelle en millisecondes Epoch.

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

Renvoie « 1544712617131 ».

+++

## inLastDays {#inLastDays}

Renvoie true si une valeur dateTime donnée se situe entre maintenant et maintenant - jours delta.

+++Syntaxe

`inLastDays(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie true si l’heure donnée est comprise entre maintenant et maintenant - delta hours.

+++Syntaxe

`inLastHours(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie « true » si une date ou une dateTime donnée se situe entre maintenant et maintenant - mois delta.

+++Syntaxe

`inLastMonths(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie « true » si une date ou une dateTime donnée se situe entre maintenant et maintenant - années delta.

+++Syntaxe

`inLastYears(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie « true » si une date ou dateTime donnée se situe entre maintenant et maintenant + delta days.

+++Syntaxe

`inNextDays(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie true si une date ou une dateTime donnée est comprise entre maintenant et maintenant + delta hours.

+++Syntaxe

`inNextHours(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie « true » si une date ou une dateTime donnée se situe entre maintenant et maintenant + delta months.

+++Syntaxe

`inNextMonths(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

Renvoie « true » si une date ou une dateTime donnée se situe entre maintenant et maintenant + années delta.

+++Syntaxe

`inNextYears(<dateTime>,<delta>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| date-heure | dateTime |
| delta | nombre entier |

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

>[!NOTE]
>
>Cette fonction n’est disponible que dans les expressions de parcours. Pour la personnalisation des e-mails et d’autres contenus, utilisez plutôt `getCurrentZonedDateTime()`. [&#x200B; En savoir plus &#x200B;](../../personalization/functions/dates.md#get-current-zoned-date-time)

+++Syntaxe

`now(<parameter>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| chaîne | Identifiant du fuseau horaire (optionnel) |

+++

+++Signatures et type renvoyé

`now()`

`now("<timeZone id>")`

Renvoie une valeur dateTime.

+++

+++Exemples

`now()`

Renvoie 2023-06-:30Z.

`toString(now())`

Renvoie « 2023-06-03T06 :30Z »

`now("Europe/Paris")`

Renvoie 2023-06-:30+02:00.

+++

## nowWithDelta {#nowWithDelta}

Renvoie la date/heure actuelle avec un décalage. Si un ID de fuseau horaire est spécifié, le décalage de fuseau horaire est appliqué. Pour plus d’informations sur les types de données, consultez [cette page](../expression/data-types.md).

+++Syntaxe

`nowWithDelta(<parameters>)`

+++

+++Paramètres

| Paramètre | Description |
|--- |--- |
| delta | valeur entière positive ou négative |
| partie de date | années, mois, jours, heures, minutes ou secondes sous forme de chaîne |
| id de fuseau horaire | représentation sous forme de chaîne de la valeur du fuseau horaire. Pour plus d&#39;informations, voir [Types de données](../expression/data-types.md). L’ID du fuseau horaire doit être une constante de chaîne. Il ne peut pas s’agir d’une référence de champ ou d’une expression. |

+++

+++Signatures et type renvoyé

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Renvoie une valeur dateTime.

+++

+++Exemples

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Renvoie une valeur dateTime il y a exactement 2 heures.

+++

## setHours {#setHours}

Définit les heures d’une date/heure ou d’une date/heure uniquement. Par exemple, si vous souhaitez attendre jusqu&#39;à une certaine heure demain, vous pouvez forcer l&#39;heure.

+++Syntaxe

`setHours(<parameter>)`

+++

+++Paramètres

| Paramètre | Type |
|--- |--- |
| date-heure | dateTime |
| heure de la date sans tenir compte du fuseau horaire | dateTimeOnly |
| heures | nombre entier |

+++

+++Signatures et type renvoyé

`setHours(<dateTime>,<hours>)`

Renvoie une valeur datetime.

`setHours(<dateTimeOnly>,<hours>)`

Renvoie une valeur datetime sans tenir compte du fuseau horaire.

+++

+++Exemples

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Renvoie 2023-12-:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Retourne demain à 20h:XY, XY étant le procès-verbal au moment de l&#39;évaluation de l&#39;heure actuelle. Si l’évaluation a lieu à 2:45 h, l’heure renvoyée sera 20 :45.

+++

## setDays {#setDays}

Définit le jour d’une date/heure ou d’une date/heure uniquement. Par exemple, si vous souhaitez attendre jusqu’à un certain jour du mois, vous pouvez forcer le jour.

+++Syntaxe

`setDays(<parameter>)`

+++

+++Paramètres

| Paramètre | Type |
|--- |--- |
| date-heure | dateTime |
| heure de la date sans tenir compte du fuseau horaire | dateTimeOnly |
| jours | nombre entier |

+++

+++Signatures et type renvoyé

`setDays(<dateTime>,<days>)`

Renvoie une valeur datetime.

`setDays(<dateTimeOnly>,<days>)`

Renvoie une valeur datetime sans tenir compte du fuseau horaire.

+++

+++Exemples

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Renvoie 2023-12-:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Renvoie une nouvelle date et une nouvelle heure, avec un nouveau fuseau horaire sur le même instant.

+++Syntaxe

`updateTimeZone(<parameters>)`

+++

+++Paramètres

* id de fuseau horaire : chaîne
* dateTime

+++

+++Signature et type renvoyé

`updateTimeZone(<dateTime>,<timeZone id>)`

Renvoie une valeur datetime.

+++

+++Exemples

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Renvoie 2023-08-:15:30.123+02:00.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Si la valeur du champ d’horodatage est `2021-11-16T16:55:12.939318+01:00`, la fonction renvoie `2021-11-17T02:55:12.942115+11:00`.

+++
