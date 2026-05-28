---
title: Bibliothèque des fonctions de date et heure
description: Bibliothèque des fonctions de date et heure
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
TQID: https://experienceleague.adobe.com/J-aZtYitBu8T4oSwTwKNNDeA-7tA4l8Wi5YZ1WLcT3E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1762
ht-degree: 64%

---

# Fonctions de date et d’heure{#date-time}

Les fonctions de date et d’heure sont utilisées pour effectuer des opérations de date et d’heure sur des valeurs dans Journey Optimizer.

>[!NOTE]
>
>La fonction `now()` n’est pas disponible dans l’éditeur de personnalisation. Utilisez plutôt `getCurrentZonedDateTime()` ou `currentTimeInMillis()` pour les valeurs actuelles de date et d’heure. [En savoir plus](../../email/code-content.md#date-time-limitations)

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

+++Exemple — Jours restants avant un événement

L’opération suivante renvoie le nombre de jours entre aujourd’hui et une date ultérieure stockée dans le profil (par exemple, une date de fin d’abonnement ou une date d’événement) :

```sql
{%= dateDiff(getCurrentZonedDateTime(), stringToDate(profile.events.subscriptionEndDate)) %}
```

+++

+++Exemple concret : compte à rebours dans la ligne d’objet

Utilisez `dateDiff` pour créer un compte à rebours dynamique pour les objets ou le contenu des e-mails :

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%} — use them before they're gone!
{%else%}
Your points have expired.
{%/if%}
```

Sortie (exemple) : `Your points expire in 7 days — use them before they're gone!`

+++

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

La fonction `dayOfWeek` est utilisée pour récupérer le jour de la semaine. Elle renvoie un entier compris entre 1 (lundi) et 7 (dimanche) selon la norme ISO-8601.

**Syntaxe**

```sql
{%= dayOfWeek(datetime) %}
```

+++Exemple — Détection des week-ends dans le contenu personnalisé

Utilisez cette fonction dans les e-mails ou le contenu pour adapter la messagerie en fonction de la journée. L’opérateur de comparaison dans PQL est `=` (un seul est égal à, et non `==`) :

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — your request will be processed on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

| Day | Valeur renvoyée |
|-----|----------------|
| Lundi | 1 |
| Mardi | 2 |
| Mercredi | 3 |
| Jeudi | 4 |
| Vendredi | 5 |
| Samedi | 6 |
| Dimanche | 7 |

+++

>[!NOTE]
>
>`dayOfWeek()` est conçu pour la **personnalisation du contenu** (par exemple, l’adaptation du corps du texte de l’e-mail en fonction du jour). Si vous devez **acheminer les profils différemment dans un parcours** en fonction du jour de la semaine (par exemple, ignorer les week-ends pour une activité Attente ), utilisez l’option intégrée **Condition de temps → Jour de la semaine** disponible directement dans l’activité Condition de parcours . [En savoir plus](../../building-journeys/condition-activity.md#date_condition)

## Jour de l’année{#day-year}

La fonction `dayOfYear` est utilisée pour récupérer le jour de l’année.

**Syntaxe**

```sql
{%= dayOfYear(datetime) %}
```

+++Exemple

* Entrée : `{%= dayOfYear(stringToDate("2024-03-15T00:00:00Z")) %}`
* Sortie : `75`

+++

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

+++Exemple concret : afficher l’heure actuelle sous la forme HH:MM uniquement

Combinez `extractHours` et `extractMinutes` pour effectuer le rendu de la partie heure uniquement sans date, jour ou année :

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is confirmed for {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Sortie (exemple) : `Your appointment is confirmed for 14:05.`

La garde de début de zéro (`{%#if m < 10%}0{%/if%}`) garantit que les minutes inférieures à 10 sont affichées sous la forme de deux chiffres (par exemple, `09` au lieu de `9`).

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

Où le premier paramètre est l’attribut date-heure et où la seconde valeur correspond à la manière dont vous souhaitez que la date soit convertie et affichée.

>[!NOTE]
>
> La fonction `formatDate` nécessite un type de champ **date-heure** en entrée, et non une chaîne. Si votre champ est stocké en tant que type de chaîne dans votre schéma XDM, vous devez d’abord le convertir en date et heure à l’aide d’une fonction de conversion telle que `stringToDate()` ou `toDateTime()`. Voir les exemples ci-dessous.
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de mise en forme des dates de Java, tel que cela est résumé dans la [documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}.

**Exemples**

+++Formater un champ date-heure

L’opération suivante formate un champ date et heure au format MM/JJ/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

+++Convertir d’abord une chaîne en date

Si votre champ est stocké sous la forme d’une chaîne, vous devez d’abord le convertir en une date et une heure à l’aide de `stringToDate()` avant de le mettre en forme.

```sql
{%= formatDate(stringToDate(profile.person.birthDayAndMonth), "MM/DD/YY") %}
```

+++

+++Format de date complet avec nom du jour

L’opération suivante renvoie un format de date complet avec le nom du jour, le nom du mois, le jour et l’année.

```sql
{%= formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy") %}
```

Sortie : `Wednesday January 01 2020`

+++

+++Date dynamique basée sur l’heure du système

Vous pouvez formater l’heure actuelle du système pour générer des dates dynamiques. L’opération suivante renvoie la date actuelle au format MM/jj/AAAA.

```sql
{%= formatDate(getCurrentZonedDateTime(), "MM/dd/YYYY") %}
```

Sortie (le 30 janvier 2026) : `01/30/2026`

+++

+++Format du jour de la semaine

Vous pouvez extraire le jour de la semaine sous une forme abrégée.

```sql
{%= formatDate(getCurrentZonedDateTime(), "EEE") %}
```

Sortie : `Sun` (pour dimanche), `Mon` (pour lundi), `Tue` (pour mardi), etc.

Pour une sortie en minuscules, combinez-la à la fonction `lowerCase` :

```sql
{%= lowerCase(formatDate(getCurrentZonedDateTime(), "EEE")) %}
```

Sortie : `sun`, `mon`, `tue`, etc.

+++

+++Formatage d’une date et heure à partir d’un événement de contexte

Lors de l’utilisation d’un horodatage à partir d’un attribut de contexte d’événement de parcours, deux exigences s’appliquent :

* **Envelopper l&#39;horodatage avec`toDateTime()`** — Les horodatages des événements contextuels ne sont pas automatiquement reconnus comme des valeurs de date et d&#39;heure par `formatDate()`.
* **Placer les identifiants d’événement numériques dans des accents graves** — si votre identifiant d’événement est un nombre (par exemple, `1697323153`), il doit être placé dans une séquence d’échappement avec des accents graves dans le chemin d’expression, sinon l’éditeur génère une erreur de syntaxe PQL.
* **Utiliser la syntaxe `{% let %}` ou `{%= %}`** — vous pouvez soit attribuer le résultat à une variable avec `{% let %}` et effectuer le rendu avec `{{varName}}`, soit utiliser directement la syntaxe du `{%= %}` intégré.

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
{{appointmentDate}}
```

Sortie (exemple) : `18/03/2026 14:30`

+++

>[!CAUTION]
>
>**Erreur courante : « entrée incohérente &#39;(&#39; en attente de \&lt;EOF\>«**
>
>Cette erreur de syntaxe PQL se produit lors de l’utilisation de `formatDate()` avec un horodatage d’événement de contexte intégré (`{%= formatDate(...) %}`). Les causes les plus courantes sont un identifiant d’événement numérique qui n’est pas encapsulé dans des accents graves (`` ` ``) ou un champ d’horodatage transmis directement à `formatDate()` sans l’encapsuler d’abord dans `toDateTime()`. Pour résoudre les deux problèmes, utilisez le modèle d’affectation de `{% let %}` illustré dans l’exemple ci-dessus.

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

+++Exemple

Définissez le jour du mois sur le 1er :

* Entrée : `{%= setDays(stringToDate("2024-11-15T17:19:51Z"), 1) %}`
* Sortie : `2024-11-01T17:19:51Z`

+++

## Définir des heures{#set-hours}

La fonction `setHours` sert à définir l’heure de la valeur date-heure.

**Syntaxe**

```sql
{%= setHours(datetime, hour) %}
```

+++Exemple — Définition d&#39;une date-heure à une heure spécifique

* Entrée : `{%= setHours(stringToDate("2024-11-01T17:19:51Z"), 0) %}`
* Sortie : `2024-11-01T00:19:51Z`

+++

+++Exemple concret : X jours avant une date de fin dynamique

Pour cibler un profil X jours avant une date stockée dans son profil (par exemple, l’expiration de l’abonnement), utilisez `addDays` avec une valeur négative :

```sql
{%= addDays(stringToDate(profile.subscription.endDate), -7) %}
```

Pour normaliser également l’heure à une heure fixe (par exemple, 9 h), combinez avec `setHours` :

```sql
{%= setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9) %}
```

+++

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

+++Exemple

* Entrée : `{%= weekOfYear(stringToDate("2024-11-01T17:19:51Z")) %}`
* Sortie : `44`

+++

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
