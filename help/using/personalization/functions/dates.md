---
title: Bibliothèque des fonctions de date et heure
description: Bibliothèque des fonctions de date et heure
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 2444d8fbe3a86feb0497d754b4f57f234fa29e49
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 100%

---

# Fonctions de date/heure{#date-time}

Les fonctions de date et d’heure sont utilisées pour effectuer des opérations de date et d’heure sur des valeurs dans Journey Optimizer.

## Âge{#age}

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


## Jour de la semaine{#day-week}

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

## Date de format{#format-date}

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
> Vous pouvez utiliser des fonctions de formatage des dates Java comme résumé dans la [documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemple**

L’opération suivante renvoie la date au format suivant : MM/JJ/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Formater la date avec la prise en charge des paramètres régionaux{#format-date-locale}

La fonction `formatDate` permet de formater une valeur d’heure et de date au format de la langue correspondante, c’est-à-dire dans le paramètre régional souhaité. Le format doit être un modèle Java DateTimeFormat valide.

**Syntaxe**

```sql
{%= formatDate(datetime, format, locale) %}
```

Lorsque la première chaîne correspond à l’attribut de date, la seconde valeur correspond à la manière dont vous souhaitez que la date soit convertie et affichée, tandis que la troisième valeur représente le paramètre régional au format chaîne.

>[!NOTE]
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de formatage des dates Java comme résumé dans la [documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Vous pouvez utiliser la mise en forme et les paramètres régionaux valides comme indiqué dans la [Documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) et les [Paramètres régionaux pris en charge](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Exemple**

L’opération ci-dessous renvoie la date au format suivant : MM/JJ/AA, dans le paramètre régional FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

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


## Semaine de l’année UTC{#week-of-year}

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