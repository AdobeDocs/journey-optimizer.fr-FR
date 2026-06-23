---
product: journey optimizer
title: Fonctions de date
description: Découvrir les fonctions de date
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
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1275
ht-degree: 65%

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

>[!NOTE]
>
>Les fonctions de cette page sont disponibles dans les expressions de parcours. Certaines fonctions telles que `now()` ne sont pas disponibles dans l’éditeur de personnalisation du contenu des e-mails. [En savoir plus](../../personalization/functions/dates.md)

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
| delta | entier |

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
| delta | entier |

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
| delta | entier |

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
| delta | entier |

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
| delta | entier |

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
| delta | entier |

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
| delta | entier |

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
| delta | entier |

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
>Cette fonction n’est disponible que dans les expressions de parcours. Pour la personnalisation des e-mails et d’autres contenus, utilisez plutôt `getCurrentZonedDateTime()`. [En savoir plus](../../personalization/functions/dates.md#get-current-zoned-date-time)

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
| jours | entier |

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

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente toutes les fonctions de date et d’heure disponibles dans les expressions de parcours AJO, couvrant la manière d’obtenir l’heure actuelle, de vérifier si une date se situe dans une fenêtre temporelle relative et de modifier les composants date/heure.

**Intentions:**
* Obtenez la date-heure actuelle (avec fuseau horaire facultatif) à l’aide de `now` ou `nowWithDelta`
* Récupérer l’heure actuelle sous la forme d’un entier epoch à l’aide de `currentTimeInMillis`
* Vérifiez si une date/heure fait partie des N derniers jours, heures, mois ou années à l’aide de `inLastDays`, `inLastHours`, `inLastMonths` ou `inLastYears`
* Vérifiez si une date/heure figure dans les N jours, heures, mois ou années suivants à l’aide de `inNextDays`, `inNextHours`, `inNextMonths` ou `inNextYears`
* Forcer une heure ou un jour spécifique du mois sur une valeur datetime à l’aide de `setHours` ou `setDays`
* Convertissez une heure en un fuseau horaire différent tout en conservant le même instant à l’aide de `updateTimeZone`

**Glossaire:**
* **dateTime** : valeur date-heure qui inclut des informations de décalage de fuseau horaire *(spécifiques au produit)*
* **dateTimeOnly** : valeur date-heure sans informations de fuseau horaire *(spécifique au produit)*
* **millisecondes epoch** : nombre entier représentant le nombre de millisecondes écoulées depuis 1970-01-01T00:00:00Z
* **delta** : décalage entier (positif ou négatif) utilisé avec `nowWithDelta` pour décaler l’heure actuelle d’un nombre d’années, de mois, de jours, d’heures, de minutes ou de secondes

**Mécanismes de sécurisation :**
* `now()` n’est disponible que dans les expressions de parcours ; pour la personnalisation des e-mails, utilisez plutôt `getCurrentZonedDateTime()`
* L’ID de fuseau horaire dans `nowWithDelta` doit être une constante de chaîne — les références aux champs et les expressions dynamiques ne sont pas prises en charge
* L’ID du fuseau horaire dans `updateTimeZone` doit être une constante de chaîne

**Terminologie:**
* Nom canonique : Fonctions de date — Acronyme : none — variantes : fonctions date-heure, fonctions temporelles
* Synonymes : « now() » = « current datetime »; « currentTimeInMillis() » = « current epoch milliseconds »
* Ne pas confondre : « inLastDays » (regarde en arrière) ≠ « inNextDays » (regarde en avant)
* Ne pas confondre : « setHours » (remplace le composant heure) ≠ « nowWithDelta » (décale l’heure actuelle)
* Ne pas confondre : « updateTimeZone » (même instant, représentation de fuseau horaire différente) ≠ « setHours » (modifie la valeur de l’heure elle-même)

**FAQ:**
* **Q : Puis-je utiliser des `now()` dans le contenu de personnalisation d’e-mail ?** — Non, `now()` n&#39;est disponible que dans les expressions de parcours. Utilisez `getCurrentZonedDateTime()` pour la personnalisation des e-mails.
* **Q : Comment puis-je vérifier si un événement s’est produit au cours des dernières 24 heures ?** — Utiliser `inLastHours(@event{MyEvent.timestamp}, 24)`.
* **Q : Comment puis-je obtenir le décalage horaire actuel de 2 heures dans le passé ?** — Utiliser `nowWithDelta(-2, "hours")`.
* **Q : Qu&#39;est-ce que `updateTimeZone` fait différemment de `setHours` ?** — `updateTimeZone` conserve le même instant dans le temps, mais l&#39;exprime dans un fuseau horaire différent, tandis que `setHours` modifie en fait le composant heure de la valeur datetime.
* **Q : Le paramètre de fuseau horaire dans `nowWithDelta` peut-il être un champ de profil ?** — Non, l&#39;ID de fuseau horaire doit être une constante de chaîne ; les références aux champs ne sont pas prises en charge.

+++
