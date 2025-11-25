---
solution: Journey Optimizer
product: journey optimizer
title: Opérateurs
description: En savoir plus sur les opérateurs dans les expressions avancées
feature: Journeys
role: Developer
level: Experienced
keywords: expression, syntaxe, opérateurs, éditeur, parcours
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '551'
ht-degree: 100%

---

# Opérateurs {#operators}

Il existe deux types d’opérateurs : unaires et binaires. Les opérateurs unaires sont répartis en deux catégories : gauche et droite.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Remarques importantes{#important-notes}

* Lors de l’utilisation d’une multiplication (`*`), les deux champs d’opération doivent avoir le même type, entier ou décimal. Exemple :
   * L’exemple suivant est correct :`3.0 * 4.0`
   * `3 * 4.0` entraîne une erreur

* Lors de l’utilisation de l’opérateur `+`, l’expression doit être encapsulée entre parenthèses. Exemple :
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))` est correct.
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))` entraîne une erreur

## Logique  {#logical}

### and

```json
<expression1> and <expression2>
```

&lt;expression1> et &lt;expression2> doivent être booléens. Le résultat est booléen.

Exemple :

```json
3.14 > 2 and 3.15 < 1
```

### or

```json
<expression1> or <expression2>
```

&lt;expression1> et &lt;expression2> doivent être booléens. Le résultat est booléen.

Exemple :

```json
3.14 > 2 or 3.15 < 1
```

### not

```json
not <expression>
```

&lt;expression> doit être booléen. Le résultat est booléen.

Exemple :

```json
not 3.15 < 1
```

## Comparaison {#comparison}

### est nul

```json
<expression> is null
```

Le résultat est booléen.

Notez que null signifie que l’expression n’a pas de valeur évaluée.

Exemple :

```json
@event{BarBeacon.location} is null
```

### n’est pas nul

```json
<expression> is not null
```

Le résultat est booléen.

Notez que null signifie que l’expression n’a pas de valeur évaluée.

Exemple :

```json
@event{BarBeacon.location} is not null
```

### est nul

```json
<expression> has null
```

&lt;expression> doit être une liste. Le résultat est booléen.

Utile pour identifier qu’une liste contient au moins une valeur « null ».

Exemple :

```json
["foo", "bar", null] has null
```

Renvoie true.

```json
["foo", "bar", ""] has null
```

Renvoie false car «  » n’est pas considéré comme « null ».

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Pour &lt;expression1> et &lt;expression2> il n’existe aucun contrôle de type de données.

Exemple :

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>Pour &lt;expression1> et &lt;expression2> il n’existe aucun contrôle de type de données.

Le résultat est booléen.

Exemple :

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Il est possible de comparer une valeur Datetime à une autre valeur Datetime.

Il est possible de comparer une valeur Datetimeonly à une autre valeur Datetimeonly.

Il est possible de comparer des nombres entiers ou décimaux à d’autres nombres entiers ou décimaux.

Toute autre combinaison est interdite.

Le résultat est booléen.

Exemple :

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Il est possible de comparer une valeur Datetime à une autre valeur Datetime.

Il est possible de comparer une valeur Datetimeonly à une autre valeur Datetimeonly.

Il est possible de comparer des nombres entiers ou décimaux à d’autres nombres entiers ou décimaux.

Toute autre combinaison est interdite.

Le résultat est booléen.

Exemple :

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Il est possible de comparer une valeur Datetime à une autre valeur Datetime.

Il est possible de comparer une valeur Datetimeonly à une autre valeur Datetimeonly.

Il est possible de comparer des nombres entiers ou décimaux à d’autres nombres entiers ou décimaux.

Toute autre combinaison est interdite.

Le résultat est booléen.

Exemple :

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Il est possible de comparer une valeur Datetime à une autre valeur Datetime.

Il est possible de comparer une valeur Datetimeonly à une autre valeur Datetimeonly.

Il est possible de comparer des nombres entiers ou décimaux à d’autres nombres entiers ou décimaux.

Toute autre combinaison est interdite.

Le résultat est booléen.

Exemple :

```json
42 <= 3.14
```

## Arithmétique {#arithmetic}

### +

```json
<expression1> + <expression2>
```

Les deux expressions doivent être numériques (nombres entiers ou décimaux).

Le résultat est également numérique.

Exemple :

```json
1 + 2
```

Renvoie 3.

### -

```json
<expression1> - <expression2>
```

Les deux expressions doivent être numériques (nombres entiers ou décimaux).

Le résultat est également numérique.

Exemple :

```json
2 - 1 
```

Renvoie 1.

### /

```json
<expression1> / <expression2>
```

Les deux expressions doivent être numériques (nombres entiers ou décimaux).

Le résultat est également numérique.

&lt;expression2> ne doit pas être égale à 0 (renvoie 0).

Exemple :

```json
4 / 2
```

Renvoie 2.

### *

```json
<expression1> * <expression2>
```

Les deux expressions doivent être numériques (nombres entiers ou décimaux).

Le résultat est également numérique.

Exemple :

```json
3 * 4
```

Renvoie 12.

### %

```json
<expression1> % <expression2>
```

Les deux expressions doivent être numériques (nombres entiers ou décimaux).

Le résultat est également numérique.

Exemple :

```json
3 % 2
```

Renvoie 1.

## Math {#math}

### est numérique

```json
<expression> is numeric
```

Le type d’expression est entier ou décimal.

Exemple :

```json
@ is numeric
```

### est un entier

```json
<expression> is integer
```

Le type d’expression est entier.

Exemple :

```json
@ is integer
```

### est décimal

```json
<expression> is decimal
```

Le type d’expression est décimal.

Exemple :

```json
@ is decimal
```

## Chaîne {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

Cet opérateur concatène deux expressions.

L’une des expressions doit être une chaîne de caractères.

Exemple :

```json
"the current time is " + (now())
```

Renvoie « Il est actuellement 2023-09-23T09:30:06.693Z ».

```json
(now()) + " is the current time"
```

Renvoie « 2023-09-23T09:30:06.693Z est l’heure actuelle ».

```json
"a" + "b" + "c" + 1234
```

Renvoie « abc1234 ».

## Date {#date}

### +

```json
<expression> + <duration>
```

Permet d’ajouter une durée à une valeur dateTimeOnly ou à une durée.

Exemple :

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Renvoie une valeur _dateTime_ 2023-12-03T15:30:30Z.

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

Renvoie une valeur _dateTimeOnly_ 2023-12-03T15:30:30.

```json
(now()) + (toDuration("PT1H"))
```

Renvoie une valeur _dateTime_ (avec fuseau horaire UTC) une heure plus tard que l’heure actuelle.

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Renvoie une valeur _duration_ PT2H.
