---
title: Bibliothèque des fonctions de date et heure
description: Bibliothèque des fonctions de date et heure
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 85b866734039ae17b0e1a8cb8e7a6f1d28af7065
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# Fonctions de date et d’heure{#date-time}

Les fonctions de date et d’heure sont utilisées pour effectuer des opérations de date et d’heure sur des valeurs dans Journey Optimizer.

## Âge{#age}

Le `age` sert à récupérer l’âge à partir d’une date donnée.

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

## Durée actuelle en millisecondes{#current-time}

Le `currentTimeInMillis` est utilisée pour récupérer l’heure actuelle en millisecondes époque.

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

## Différence entre dates{#date-diff}

Le `dateDiff` sert à récupérer la différence entre deux dates en nombre de jours.

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

Le `dayOfWeek` est utilisée pour récupérer le jour de la semaine.

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

Le `dayOfYear` est utilisée pour récupérer le jour de l’année.

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

Le `formatDate` sert à mettre en forme une valeur de date et d’heure. Le format doit être un modèle Java DateTimeFormat valide.

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

## Jours définis{#set-days}

Le `setDays` sert à définir le jour du mois pour la date et l’heure données.

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

## Définition des heures{#set-hours}

Le `setHours` sert à définir l’heure de la date et de l’heure.

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


## À UTC{#to-utc}

Le `toUTC` est utilisée pour convertir un datetime en UTC.


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


## Semaine de l&#39;année UTC{#week-of-year}

Le `weekOfYear` est utilisée pour récupérer la semaine de l’année.

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