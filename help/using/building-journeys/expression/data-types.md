---
solution: Journey Optimizer
product: journey optimizer
title: Types de données
description: En savoir plus sur les types de données dans les expressions avancées
feature: Journeys
role: Developer
level: Experienced
keywords: expression, données, type de données, parcours
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0UKY3G4hyMnSkzh8wlMx-yQ1yymKjs6FuIBdGo1SJqc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1124
ht-degree: 59%

---

# Types de données {#data-types}

D’un point de vue technique, une constante contient toujours un type de données. Dans une expression littérale, nous ne spécifions que la valeur. Le type de données peut être déduit de la valeur (par exemple : chaîne, entier, décimal, etc.). Pour des cas spécifiques, tels que la date et l’heure, des fonctions dédiées sont utilisées pour la représentation.

Les sections ci-dessous fournissent des informations sur les différentes expressions de type de données et sur leur représentation.

## string {#string}

**Description**

Séquence de caractères courante. Pas de taille spécifique, à l’exception de la taille implicite provenant de l’environnement, comme la quantité de mémoire disponible.

Format JSON : chaîne

Format de sérialisation : UTF-8

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

## integer {#integer}

**Description**

Valeur entière comprise entre -2^63 et 2^63-1.

Format JSON : nombre

**Représentation littérale**

```json
<integer value>
```

**Exemple**

```json
42
```

## decimal {#decimal}

**Description**

Nombre décimal. Représente une valeur flottante :

* valeur finie positive la plus grande de type double, (2-2^-52)x2^1023
* valeur normale positive la plus petite de type double, 2-1022
* valeur non nulle positive la plus petite de type double, 2 p-1074

Format JSON : nombre

Format de sérialisation : utilisation de « . » comme séparateur décimal.

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

Valeur booléenne en minuscules : true ou false

Format JSON : booléen

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

## dateOnly {#date-only}

**Description**

Représente une valeur de date uniquement sans fuseau horaire, sous la forme année-mois-jour.

Il sʼagit dʼune description de la date, telle quʼelle est utilisée pour les anniversaires.

Format JSON : chaîne.

Format : AAAA-MM-JJ (ISO-8601), par exemple : « 2021-03-11 ».

Elle doit être encapsulée dans une fonction toDateOnly.

Il utilise DateTimeFormatter SO_LOCAL_DATE_TIME pour désérialiser et sérialiser la valeur. [En savoir plus](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**Représentation littérale**

```json
date("<dateOnly in ISO-8601 format>")  
```

**Exemple**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**Description**

Représente une valeur de date et d’heure sans fuseau horaire, sous la forme année-mois-jour-heure-minute-seconde-milliseconde.

Format JSON : chaîne.

Ce type ne stocke ni ne représente un fuseau horaire. Il s’agit plutôt d’une description de la date, telle qu’elle est utilisée pour les anniversaires, associée à l’heure locale telle qu’elle est affichée sur une horloge murale.

Il ne peut pas représenter un instant sur la ligne de temps sans informations supplémentaires telles qu’un décalage ou un fuseau horaire.

Elle doit être encapsulée dans une fonction toDateTimeOnly.

Format de sérialisation : format date-heure avec décalage étendu ISO-8601.

Il utilise DateTimeFormatter SO_LOCAL_DATE_TIME pour désérialiser et sérialiser la valeur. [En savoir plus](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME"){_blank}.

**Représentation littérale**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**Exemples**

```json
date("2024-02-19T00.00.000")
date("2024-02-19T00.00")
```

## dateTime {#date-time}

**Description**

Constante de date et d’heure qui tient également compte du fuseau horaire. Elle représente une valeur de date et d’heure avec un décalage par rapport à UTC.

Elle peut être vue comme un point de la ligne du temps avec les informations supplémentaires du décalage. C’est une façon de représenter un « moment » précis en un point du globe.

Format JSON : chaîne.

Elle doit être encapsulée dans une fonction toDateTime.

Format de sérialisation : format date-heure avec décalage étendu ISO-8601.

Il utilise DateTimeFormatter ISO_OFFSET_DATE_TIME pour désérialiser et sérialiser la valeur. [En savoir plus](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME){_blank}.

Vous pouvez également transmettre un entier qui transmet une valeur d’époque. [En savoir plus](https://www.epochconverter.com){_blank}.

Le fuseau horaire peut être spécifié par un décalage ou un code de fuseau horaire (par exemple : Europe/Paris, Z ; ce qui signifie UTC).

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
date("2024-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2023-12-03T15:15:30Z")
```

```json
toDateTime("2023-12-03T15:15:30.123Z")
```

```json
toDateTime("2023-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2023-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## duration {#duration}

**Description**

Ce type représente une durée basée sur le temps, telle que « 34,5 secondes ». Elle modélise une durée ou un laps de temps exprimé en millisecondes.

Les unités temporelles prises en charge sont les suivantes : millisecondes, secondes, minutes, heures, jours où un jour équivaut à 24 heures. Les années et les mois ne sont pas pris en charge, car ils ne représentent pas un laps de temps fixe.

Format JSON : chaîne.

Elle doit être encapsulée dans une fonction toDuration.

Format de sérialisation : pour désérialiser un identifiant de fuseau horaire, la fonction Java java.time est utilisée.

Duration.parse : les formats acceptés sont basés sur le format de durée ISO-8601 PnDTnHnMn.nS, avec des jours durant exactement 24 heures. [En savoir plus](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-){_blank}.

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

Le polymorphisme n’est pas pris en charge. Par conséquent, toutes les expressions contenues dans la liste doivent être du même type.

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

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page décrit tous les types de données pris en charge dans l’éditeur d’expression avancé de Parcours (chaîne, entier, décimal, booléen, dateOnly, dateTimeOnly, dateTime, durée et liste), ainsi que leurs formats JSON, règles de sérialisation et syntaxe de représentation littérale.

**Intentions:**

* Identifier la syntaxe littérale correcte pour chaque type de données lors de l’écriture d’expressions de parcours
* Comprenez la différence entre les types `dateOnly`, `dateTimeOnly` et `dateTime` et quand les utiliser
* Représente une valeur de durée au format ISO-8601 ou en millisecondes avec la fonction `toDuration()`
* Construire une expression de liste avec des crochets syntaxiques à utiliser dans les opérations de collection
* Utilisez des fonctions de conversion (`toDateTime`, `toDateTimeOnly`, `toDuration`, `toDateOnly`) pour créer des constantes typées

**Glossaire:**

* **dateOnly** : date sans fuseau horaire, au format AAAA-MM-JJ ; adaptée aux dates d’anniversaire ou de calendrier *(spécifiques au produit)*
* **dateTimeOnly** : date et heure sans informations de fuseau horaire ; ne peut pas représenter un instant spécifique sans *de décalage (spécifique au produit)*
* **dateTime** : constante date-heure qui comprend un décalage UTC, représentant un instant spécifique. Elle peut également être créée à partir d’un *entier d’époque (spécifique au produit)*
* **durée** : quantité basée sur le temps modélisée en millisecondes ; utilise le format de `PnDTnHnMn.nS` ISO-8601 ; les années et les mois ne sont pas pris en charge *(spécifiques au produit)*
* **list** : collection d’expressions du même type séparées par des virgules, délimitées par des crochets *(spécifiques au produit)*

**Mécanismes de sécurisation :**

* La durée prend uniquement en charge les millisecondes, les secondes, les minutes, les heures et les jours. Les années et les mois ne sont pas pris en charge, car il ne s&#39;agit pas de périodes fixes
* Une valeur `duration` doit être encapsulée dans `toDuration()` — elle ne peut pas être exprimée sous la forme d&#39;un littéral nu
* Toutes les expressions d&#39;un `list` doivent avoir le même type — le polymorphisme n&#39;est pas pris en charge
* `dateTimeOnly` ne peut pas représenter un instant dans le temps sans décalage ou fuseau horaire supplémentaire

**Terminologie:**

* Nom canonique : Types de données — Acronyme : none — variantes : types de données d’expression, types de données de parcours
* Synonymes : « dateTime » = « date-heure avec fuseau horaire »; « dateTimeOnly » = « date-heure locale »
* Ne pas confondre : `dateOnly` (pas d’heure) ≠ `dateTimeOnly` (date + heure, pas de fuseau horaire) ≠ `dateTime` (date + heure + fuseau horaire/décalage)

**FAQ:**

* **Q : Quelle est la différence entre `dateTimeOnly` et `dateTime` ?** — `dateTimeOnly` n’a ni fuseau horaire ni décalage et ne peut pas représenter un instant précis ; `dateTime` inclut un décalage UTC et représente un moment spécifique dans le temps.
* **Q : Comment exprimer une durée de 2 jours et 3 heures ?** — Utiliser `toDuration("P2DT3H")`.
* **Q : Puis-je mélanger des entiers et des chaînes dans une expression de liste ?** — Non ; toutes les expressions d&#39;une liste doivent être du même type.
* **Q : Comment créer un `dateTime` à partir d’un horodatage d’époque en millisecondes ?** — Utilisez `toDateTime(<epoch in milliseconds>)`, par exemple `toDateTime(1560762190189)`.
* **Q : Le littéral booléen `true` ou `True`-il correct ?** — Utilisez des `true` ou des `false` en minuscules ; les variantes en majuscules ne sont pas valides.

+++
