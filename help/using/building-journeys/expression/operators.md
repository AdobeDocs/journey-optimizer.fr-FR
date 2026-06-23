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
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 54%

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

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page est une référence complète des opérateurs disponibles dans l’éditeur d’expression avancé de Parcours, couvrant les opérateurs logiques (`and`, `or`, `not`), de comparaison (`==`, `!=`, `>`, `>=`, `<`, `<=`, `is null`, `is not null`, `has null`), arithmétiques (`+`, `-`, `/`), de vérification de type mathématique (`*`, `%` `is numeric` `is integer` `is decimal`), de concaténation de chaîne et d’arithmétique de date.

**Intentions:**

* Combinez des conditions booléennes en utilisant des opérateurs logiques `and`, `or` et `not`
* Vérifier si une valeur de champ ou d&#39;expression est nulle ou non à l&#39;aide de `is null` / `is not null`
* Détecter les valeurs nulles dans une liste à l’aide de l’opérateur `has null`
* Comparez des valeurs numériques, datetime et datetimeonly à l’aide de `>`, `>=`, `<`, `<=`, `==` et `!=`
* Exécuter des opérations arithmétiques sur des valeurs numériques à l’aide de `+`, `-`, `/`, `*` et `%`
* Ajoutez une durée à une valeur dateTime, dateTimeOnly ou duration à l&#39;aide de l&#39;opérateur `+`

**Glossaire:**

* **Opérateur unaire** : opérateur appliqué à un seul opérande ; il peut être gauche (par exemple, `not`) ou droit (par exemple, `is null`) *(spécifique au produit)*
* **Opérateur binaire** : opérateur appliqué entre deux opérandes (par exemple `and`, `==`, `+`) *(spécifique au produit)*
* **has null** : un opérateur unaire droit qui retourne true si une liste contient au moins un élément null *(product-specific)*
* **est numérique / est un entier / est décimal** : les opérateurs de vérification de type qui renvoient une valeur booléenne en fonction du sous-type numérique de l’expression *(spécifique au produit)*

**Mécanismes de sécurisation :**

* Lors de l&#39;utilisation de la multiplication (`*`), les deux opérandes doivent être du même type numérique (entier ou décimal) — le mélange des types provoque une erreur
* Lors de l’utilisation de l’opérateur `+` pour l’arithmétique de date, l’expression doit être mise entre parenthèses pour éviter les erreurs d’analyse
* Les opérateurs de comparaison (`>`, `>=`, `<`, `<=`) ne sont valides qu&#39;entre les types compatibles : Datetime avec Datetime, DatetimeOnly avec DatetimeOnly ou numeric avec numeric — toute autre combinaison est interdite
* Une `""` de chaîne vide n&#39;est pas considérée comme nulle — `has null` renvoie false pour une liste contenant des `""`
* Les opérateurs `==` et `!=` n’effectuent aucun contrôle de type de données entre les opérandes

**Terminologie:**

* Nom canonique : Opérateurs — Acronyme : none — variantes : opérateurs d’expression, opérateurs de parcours
* Synonymes : `and` = « logique ET »; `or` = « logique OU »; `not` = « logique NON »; `%` = « modulo »
* Ne pas confondre : `is null` (l’expression n’a pas de valeur évaluée) ≠ `== null` (syntaxe non valide) ; `has null` (la liste contient la valeur null) ≠ `is null` (l’expression elle-même est null)

**FAQ:**

* **Q : Puis-je multiplier directement un entier par une décimale ?** — Non ; les deux opérandes de `*` doivent être du même type. Utilisez `3.0 * 4.0` (les deux décimales) ou `3 * 4` (les deux entiers).
* **Q : Comment ajouter 15 minutes à une dateTime ?** — Utiliser `(toDateTime("...")) + (toDuration("PT15M"))`.
* **Q : Quelle est la différence entre `is null` et `has null` ?** — `is null` vérifie si une seule expression n&#39;a pas de valeur évaluée ; `has null` vérifie si une liste contient au moins un élément null.
* **Q : Est-ce que `"" has null` renvoie true ?** — Non ; une chaîne vide n&#39;est pas considérée comme nulle, le résultat est donc faux.
* **Q : Pourquoi `3 * 4.0` provoque-t-il une erreur ?** — L&#39;opérateur `*` exige que les deux opérandes soient du même type numérique ; le mélange de nombres entiers et décimaux n&#39;est pas autorisé.

+++
