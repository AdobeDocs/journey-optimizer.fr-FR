---
title: Bibliothèque des fonctions de date et heure
description: Bibliothèque des fonctions de date et heure
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 48b3ef3d2e041ea49d1b0c91cc72ea04237a5e33
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 98%

---

# Fonctions de date/heure{#date-time}

Les fonctions de date et d’heure sont utilisées pour effectuer des opérations de date et d’heure sur des valeurs dans Journey Optimizer.

>[!NOTE]
>
>La fonction `now()` n’est pas disponible dans l’éditeur de personnalisation. Utilisez `getCurrentZonedDateTime()` ou `currentTimeInMillis()` à la place pour les valeurs de date et d’heure actuelles. [En savoir plus](../../email/code-content.md#date-time-limitations)

## Ajouter des jours {#add-days}

La fonction `addDays` ajuste une date donnée d’un nombre de jours spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

**Syntaxe**

```sql
{%= addDays(date, number) %}
```

+++Exemple

* Entrée : `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Sortie : `2024-11-11T17:19:51Z`

+++

## Ajouter des heures {#add-hours}

La fonction `addHours` ajuste une date donnée d’un nombre d’heures spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

**Syntaxe**

```sql
{%= addHours(date, number) %}
```

+++Exemple

* Entrée : `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Sortie : `2024-11-01T18:19:51Z`

+++

## Ajouter des minutes {#add-minutes}

La fonction `addMinutes` ajuste une date donnée d’un nombre de minutes spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

**Syntaxe**

```sql
{%= addMinutes(date, number) %}
```

+++Exemple

* Entrée : `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Sortie : `2024-11-01T18:09:51Z`

+++

## Ajouter des mois {#add-months}

La fonction `addMonths` ajuste une date donnée d’un nombre de mois spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

**Syntaxe**

```sql
{%= addMonths(date, number) %}
```

+++Exemple

* Entrée : `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Sortie : `2025-01-01T17:19:51Z`

+++

## Ajouter des secondes {#add-seconds}

La fonction `addSeconds` ajuste une date donnée d’un nombre de secondes spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

**Syntaxe**

```sql
{%= addSeconds(date, number) %}
```

+++Exemple

* Entrée : `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Sortie : `2024-11-01T17:20:01Z`

+++

## Ajouter des années {#add-years}

La fonction `addYears` ajuste une date donnée d’un nombre d’années spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

**Syntaxe**

```sql
{%= addYears(date, number) %}
```

+++Exemple

* Entrée : `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Sortie : `2026-11-01T17:19:51Z`

+++

## Ancienneté{#age}

La fonction `age` sert à récupérer l’âge à partir d’une date donnée.

**Syntaxe**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Ancienneté en jours {#age-days}

La fonction `ageInDays` calcule l’ancienneté d’une date donnée en jours, c’est-à-dire le nombre de jours écoulés entre la date donnée et la date actuelle, négatif pour les dates futures et positif pour les dates passées.

**Syntaxe**

```sql
{%= ageInDays(date) %}
```

+++Exemple

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asie/Calcutta)

* Entrée : `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Sortie : `5`

+++

## Ancienneté en mois {#age-months}

La fonction `ageInMonths` calcule l’ancienneté d’une date donnée en mois, c’est-à-dire le nombre de mois écoulés entre la date donnée et la date actuelle, négatif pour les dates futures et positif pour les dates passées.

**Syntaxe**

```sql
{%= ageInMonths(date) %}
```

+++Exemple

currentDate = 2025-01-07T12:22:46.993748+05:30(Asie/Calcutta)

* Entrée : `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Sortie : `12`

+++

## Comparer les dates {#compare-dates}

La fonction `compareDates` compare la première date d’entrée à l’autre. Renvoie 0 si la valeur date1 est égale à date2, -1 si la valeur date1 est antérieure à date2 et 1 si la valeur date1 est postérieure à date2.

**Syntaxe**

```sql
{%= compareDates(date1, date2) %}
```

+++Exemple

* Entrée : `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Sortie : `-1`

+++

## Convertir ZonedDateTime {#convert-zoned-date-time}

La fonction `convertZonedDateTime` convertit une date-heure en un fuseau horaire donné.

**Syntaxe**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Exemple

* Entrée : `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Sortie : `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## Heure actuelle en millisecondes{#current-time}

La fonction `currentTimeInMillis` est utilisée pour récupérer l’heure actuelle en millisecondes Epoch.

**Syntaxe**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Différence de date{#date-diff}

La fonction `dateDiff` sert à récupérer la différence entre deux dates en nombre de jours.

**Syntaxe**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Jour du mois {#day-month}

La fonction `dayOfMonth` renvoie le nombre représentant le jour du mois.

**Syntaxe**

```sql
{%= dayOfMonth(datetime) %}
```

+++Exemple

* Entrée : `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Sortie : `5`

+++


## Jour de la semaine {#day-week}

La fonction `dayOfWeek` est utilisée pour récupérer le jour de la semaine.

**Syntaxe**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Jour de l’année{#day-year}

La fonction `dayOfYear` est utilisée pour récupérer le jour de l’année.

**Syntaxe**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Différence en secondes {#diff-seconds}

La fonction `diffInSeconds` renvoie la différence entre deux dates en nombre de secondes.

**Syntaxe**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Exemple

* Entrée : `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Sortie : `50`

+++

## Extraire les heures {#extract-hours}

La fonction `extractHours` extrait le composant des heures d’un horodatage donné.

**Syntaxe**

```sql
{%= extractHours(date) %}
```

+++Exemple

* Entrée : `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `17`

+++

## Extraire les minutes {#extract-minutes}

La fonction `extractMinutes` extrait le composant des minutes d’un horodatage donné.

**Syntaxe**

```sql
{%= extractMinutes(date) %}
```

+++Exemple

* Entrée : `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `19`

+++

## Extraire les mois {#extract-months}

La fonction `extractMonth` extrait le composant des mois d’un horodatage donné.

**Syntaxe**

```sql
{%= extractMonths(date) %}
```

+++Exemple

* Entrée : `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `11`

+++

## Extraire les secondes {#extract-seconds}

La fonction `extractSeconds` extrait le composant des secondes d’un horodatage donné.

**Syntaxe**

```sql
{%= extractSeconds(date) %}
```

+++Exemple

* Entrée : `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `51`

+++

## Mettre en forme la date{#format-date}

La fonction `formatDate` sert à formater une valeur de date et d’heure. Le format doit être un modèle Java DateTimeFormat valide.

**Syntaxe**

```sql
{%= formatDate(datetime, format) %}
```

Où la première chaîne correspond à l’attribut date et la seconde à la manière dont vous souhaitez que la date soit convertie et affichée.

>[!NOTE]
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de mise en forme des dates de Java, tel que cela est résumé dans la [documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}.

**Exemple**

L’opération suivante renvoie la date au format suivant : MM/JJ/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

### Caractères de motif {#pattern-characters}

Certaines lettres de motif peuvent ressembler à d’autres, mais représenter des concepts différents.

| Motif | Signification | Exemple (pour `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Année civile (année standard) | `2023` |
| `Y` | Année basée sur les semaines (ISO 8601). Peut varier à la fin de l’année. | `2024` (puisque le 31 décembre 2023 tombe dans la première semaine de 2024) |
| `M` | Mois de l’année (1-12 ou texte comme `Jan`, `January`) | `12` ou `Dec`. |
| `m` | Minute de l’heure (0-59) | `15` |
| `d` | Jour du mois (1-31) | `31` |
| `D` | Jour de l’année (1-366) | `365` |

### Formater la date avec la prise en charge des paramètres régionaux{#format-date-locale}

La fonction `formatDate` peut être utilisée pour formater une valeur d’heure et de date au format de la langue correspondante, c’est-à-dire dans les paramètres régionaux souhaités. Le format doit être un modèle Java DateTimeFormat valide.

**Syntaxe**

```sql
{%= formatDate(datetime, format, locale) %}
```

Lorsque la première chaîne correspond à l’attribut de date, la seconde valeur correspond à la manière dont vous souhaitez que la date soit convertie et affichée, tandis que la troisième valeur représente les paramètres régionaux au format chaîne.

>[!NOTE]
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de formatage des dates Java comme résumé dans la [documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Vous pouvez utiliser la mise en forme et les paramètres régionaux valides comme indiqué dans la [Documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) et les [Paramètres régionaux pris en charge](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Exemple**

L’opération ci-dessous renvoie la date au format suivant : MM/jj/AA, dans les paramètres régionaux FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

## Obtenir la CurrentZonedDateTime {#get-current-zoned-date-time}

La fonction `getCurrentZonedDateTime` renvoie la date et l’heure actuelles avec les informations de fuseau horaire.

**Syntaxe**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Exemple

* Entrée : `{%= getCurrentZonedDateTime() %}`
* Sortie : `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Différence en heures {#hours-difference}

La fonction `diffInHours` renvoie la différence entre deux dates en nombre d’heures.

**Syntaxe**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Exemple

* Entrée : `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Sortie : `10`

+++

## Différence en minutes{#diff-minutes}

La fonction `diffInMinutes` sert à renvoyer la différence entre deux dates en nombre de minutes.

**Syntaxe**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Exemple

* Entrée : `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Sortie : `60`

+++

## Différence en mois {#months-difference}

La fonction `diffInMonths` renvoie la différence entre deux dates en nombre de mois.

**Syntaxe**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Exemple

* Entrée : `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Sortie : `3`

+++

## Définir les jours{#set-days}

La fonction `setDays` sert à définir le jour du mois pour la valeur date-heure donnée.

**Syntaxe**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Définir des heures{#set-hours}

La fonction `setHours` sert à définir l’heure de la valeur date-heure.

**Syntaxe**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## En date/heure {#to-date-time}

La fonction `ToDateTime` convertit une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.

**Syntaxe**

```sql
{%= toDateTime(string, string) %}
```

+++Exemple

* Entrée : `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Sortie : `2024-11-01T17:19:51Z`

+++

## En UTC{#to-utc}

La fonction `toUTC` est utilisée pour convertir une heure en UTC.

**Syntaxe**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Tronquer au début de la journée {#truncate-day}

La fonction `truncateToStartOfDay` modifie une date-heure donnée en la définissant sur le début de la journée et sur 00:00.

**Syntaxe**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Exemple

* Entrée : `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Sortie : `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

La fonction `truncateToStartOfQuarter` tronque une date-heure au premier jour de son trimestre (par exemple, 1er janvier, 1er avril, 1er juillet, 1er octobre) à 00:00.

**Syntaxe**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Exemple

* Entrée : `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

La fonction `truncateToStartOfWeek` modifie une date-heure donnée en la définissant sur le début de la semaine (lundi à 00:00).

**Syntaxe**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Exemple

* Entrée : `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Sortie : `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

La fonction `truncateToStartOfYear` modifie une date-heure donnée en la tronquant au premier jour de l’année (1er janvier) à 00:00.

**Syntaxe**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Exemple

* Entrée : `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `2024-01-01T00:00Z`

+++

## Semaine de l’année {#week-of-year}

La fonction `weekOfYear` est utilisée pour récupérer la semaine de l’année.

**Syntaxe**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Différence en années {#diff-years}

La fonction `diffInYears` sert à renvoyer la différence entre deux dates en nombre d’années.

**Syntaxe**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Exemple

* Entrée : `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Sortie : `5`

+++
