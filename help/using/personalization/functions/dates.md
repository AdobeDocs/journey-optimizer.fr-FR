---
title: Bibliothèque des fonctions de date et heure
description: Bibliothèque des fonctions de date et heure
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: ht
source-wordcount: '262'
ht-degree: 100%

---

# Fonctions de date/heure{#date-time}

Les fonctions de date et d’heure sont utilisées pour effectuer des opérations de date et d’heure sur des valeurs dans Journey Optimizer.

## Âge{#age}

La fonction `age` sert à récupérer l’âge à partir d’une date donnée.

**Format**

```sql
 {%= age(date) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(date) %}
```
-->

## Heure actuelle en millisecondes{#current-time}

La fonction `currentTimeInMillis` est utilisée pour récupérer l’heure actuelle en millisecondes Epoch.

**Format**

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

**Format**

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

**Format**

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

**Format**

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

**Format**

```sql
{%= formatDate(date, format) %}
```

Où la première chaîne correspond à l’attribut date et la seconde à la manière dont vous souhaitez que la date soit convertie et affichée.

>[!NOTE]
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de formatage des dates Java comme résumé [dans la documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemple**

L’opération suivante renvoie la date au format suivant : MM/JJ/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Définir les jours{#set-days}

La fonction `setDays` sert à définir le jour du mois pour la valeur date-heure donnée.

**Format**

```sql
{%= setDays(date, day) %}
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

**Format**

```sql
{%= setHours(date, hour) %}
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


**Format**

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

**Format**

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
