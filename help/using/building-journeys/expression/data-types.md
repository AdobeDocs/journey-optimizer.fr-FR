---
solution: Journey Optimizer
product: journey optimizer
title: Types de données
description: En savoir plus sur les types de données dans les expressions avancées
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# Types de données {#data-types}

D’un point de vue technique, une constante contient toujours un type de données. Dans l’expression littérale, nous spécifions uniquement la valeur. Le type de données peut être déduit de la valeur (par exemple chaîne, entier, décimal, etc.). Pour des cas spécifiques tels que la date et l’heure, nous utilisons des fonctions dédiées pour la représentation.

Les sections ci-dessous fournissent des informations sur les différentes expressions de type de données et sur la manière dont elles sont représentées.

## string {#string}

**Description**

Séquence de caractères courante. Il n’a pas de taille spécifique, à l’exception de celle implicite provenant de l’environnement, comme la quantité de mémoire disponible.

Format JSON : Chaîne

Format de sérialisation : UTF-8

**Représentation littérale**

```json
"<value>"
```

```json
'<value>'
```

**Exemple**

```json
"hello world"
```

```json
'hello world'
```

## entier {#integer}

**Description**

Valeur entière comprise entre -2^63 et 2^63-1.

Format JSON : Nombre

**Représentation littérale**

```json
<integer value>
```

**Exemple**

```json
42
```

## décimal {#decimal}

**Description**

Nombre décimal. Il représente une valeur flottante :

* valeur finie positive la plus grande de type double, (2-2^-52)x2^1023
* valeur normale positive la plus petite de type double, 2-1022
* valeur non nulle positive la plus petite de type double, 2 p-1074

Format JSON : Nombre

Format de sérialisation : en utilisant &#39;.&#39; comme séparateur décimal.

**Représentation littérale**

```json
<integer value>.<integer value>
```

**Exemple**

```json
3.14
```

## boolean {#boolean}

**Description**

Valeur booléenne en minuscules : true ou false

Format JSON : Booléen

**Représentation littérale**

```json
true
```

```json
false
```

**Exemple**

```json
true
```

## dateOnly {#date-only}

**Description**

Représente une date uniquement sans fuseau horaire, affichée sous la forme d’un jour d’un mois d’année.

Il s’agit d’une description de la date, telle qu’elle est utilisée pour les anniversaires.

Format JSON : Chaîne.

Le format est le suivant : AAAA-MM-JJ (ISO-8601), par exemple : &quot;2021-03-11&quot;.

Il peut être encapsulé dans une fonction toDateOnly.

Il utilise DateTimeFormatter ISO_LOCAL_DATE_TIME pour désérialiser et sérialiser la valeur. [En savoir plus](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**Représentation littérale**

```json
date("<dateOnly in ISO-8601 format>")  
```

**Exemple**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**Description**

Représente une date et une heure sans fuseau horaire, sous la forme année-mois-jour-heure-minute-seconde-milliseconde.

Format JSON : Chaîne.

Il ne stocke ni ne représente de fuseau horaire. Il s’agit plutôt d’une description de la date, telle qu’elle est utilisée pour les anniversaires, associée à l’heure locale telle qu’elle est affichée sur une horloge murale.

Il ne peut pas représenter un instant sur la ligne de temps sans informations supplémentaires telles qu’un décalage ou un fuseau horaire.

Il peut être encapsulé dans une fonction toDateTimeOnly.

Format de sérialisation : Format date-heure de décalage étendu ISO-8601.

Il utilise DateTimeFormatter ISO_LOCAL_DATE_TIME pour désérialiser et sérialiser la valeur. [En savoir plus](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME&quot;)

**Représentation littérale**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**Exemples**

```json
date("2021-02-19T00.00.000")
date("2021-02-19T00.00")
```

## dateTime {#date-time}

**Description**

Constante de date et d’heure qui prend également en compte le fuseau horaire. Il représente une date et une heure avec un décalage par rapport à UTC.

Elle peut être vue comme un instant dans le temps avec les informations supplémentaires du décalage. C&#39;est une façon de représenter un &quot;moment&quot; spécifique à un certain endroit du monde.

Format JSON : Chaîne.

Il peut être encapsulé dans une fonction toDateTime .

Format de sérialisation : Format date-heure de décalage étendu ISO-8601.

Il utilise DateTimeFormatter ISO_OFFSET_DATE_TIME pour désérialiser et sérialiser la valeur. [En savoir plus](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME)

Vous pouvez également transmettre un entier qui transmet une valeur d’époque. [En savoir plus](https://www.epochconverter.com)

Le fuseau horaire peut être spécifié par un décalage ou un code de fuseau horaire (exemple : Europe/Paris, Z - ce qui signifie UTC).

**Représentation littérale**

```json
toDateTime("<dateTime in ISO-8601 format>")
```

```json
date("<dateTime in ISO-8601 format>")
```

```json
toDateTime(<integer value of an epoch in milliseconds>)
```

**Exemples**

```json
date("2021-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2011-12-03T15:15:30Z")
```

```json
toDateTime("2011-12-03T15:15:30.123Z")
```

```json
toDateTime("2011-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2011-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## durée {#duration}

**Description**

Il représente une durée basée sur le temps, telle que &quot;34,5 secondes&quot;. Elle modélise une quantité ou une durée en millisecondes.

Les unités temporelles prises en charge sont les suivantes : millisecondes, secondes, minutes, heures, jours où un jour équivaut à 24 heures. Les années et les mois ne sont pas pris en charge, car il ne s’agit pas d’une période fixe.

Format JSON : Chaîne.

Elle doit être encapsulée dans une fonction toDuration.

Format de sérialisation : Pour désérialiser un identifiant de fuseau horaire, il utilise la fonction java.time.

Duration.parse : les formats acceptés sont basés sur le format de durée ISO-8601 PnDTnHnMn.nS avec des jours considérés exactement comme étant de 24 heures. [En savoir plus](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-)

**Représentation littérale**

```json
toDuration("<duration in ISO-8601 format>")
```

```json
toDuration(<duration in milliseconds>)
```

**Exemple**

```json
toDuration("PT5S") -- parses as 5 seconds
```

```json
toDuration(500) -- parses as 500ms
```

```json
toDuration("PT20.345S") -- parses as "20.345 seconds"
```

```json
toDuration("PT15M") -- parses as "15 minutes" (where a minute is 60 seconds)
```

```json
toDuration("PT10H")  -- parses as "10 hours" (where an hour is 3600 seconds)
```

```json
toDuration("P2D") -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
```

```json
toDuration("P2DT3H4M") -- parses as "2 days, 3 hours and 4 minutes"
```

```json
toDuration("P-6H3M") -- parses as "-6 hours and +3 minutes"
```

```json
toDuration("-P6H3M") -- parses as "-6 hours and -3 minutes"
```

```json
toDuration("-P-6H+3M") -- parses as "+6 hours and -3 minutes"
```

## list {#list}

**Description**

Liste d’expressions séparées par des virgules utilisant des crochets comme délimiteurs.

Le polymorphisme n’est pas pris en charge. Par conséquent, toutes les expressions contenues dans la liste doivent avoir le même type.

**Représentation littérale**

```json
[<expression>, <expression>, ... ]
```

**Exemple**

```json
["value1","value2"]
```

```json
[3,5]
```

```json
[toDuration(500),toDuration(800)]
```
