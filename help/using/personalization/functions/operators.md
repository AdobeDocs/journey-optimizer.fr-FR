---
title: Bibliothèque des fonctions des opérateurs
description: Bibliothèque des fonctions des opérateurs
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '308'
ht-degree: 100%

---

# Opérateurs {#operators}

## Fonctions booléennes {#boolean-functions}

Les fonctions booléennes sont utilisées pour exécuter une logique booléenne sur différents éléments.

### Et{#and}

La fonction `and` est utilisée pour convertir un nombre en pourcentage.

**Syntaxe**

```sql
{%= query1 and query2 %}
```

**Exemple**

L&#39;opération suivante renverra toutes les personnes ayant pour pays d&#39;origine la France et pour année de naissance 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Ou{#or}

La fonction `or` est utilisée pour créer une disjonction logique.

**Syntaxe**

```sql
{%= query1 or query2 %}
```

**Exemple**

L&#39;opération suivante renverra toutes les personnes ayant pour pays d&#39;origine la France ou pour année de naissance 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## Fonctions de comparaison  {#comparison-functions}

Les fonctions de comparaison sont utilisées pour comparer les différentes expressions et valeurs, renvoyant &#39;true&#39; ou &#39;false&#39; en conséquence.

### Égal à{#equals}

La fonction `=` (égal à) vérifie si une valeur ou expression est égale à une autre valeur ou expression.

**Syntaxe**

```sql
{%= expression = value %}
```

**Exemple**

L&#39;opération suivante vérifie si le pays de l&#39;adresse du domicile est la France.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Différent de{#notequal}

La fonction `!=` (différent de) vérifie si une valeur ou expression est **différente** d&#39;une autre valeur ou expression.

**Syntaxe**

```sql
{%= expression != value %}
```

**Exemple**

L&#39;opération suivante vérifie si le pays de l&#39;adresse du domicile n&#39;est pas la France.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Supérieur à{#greaterthan}

La fonction `>` (supérieur à) permet de vérifier si la première valeur est supérieure à la seconde.

**Syntaxe**

```sql
{%= expression1 > expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées strictement après 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Supérieur ou égal à{#greaterthanorequal}

La fonction `>=` (supérieur ou égal à) permet de vérifier si la première valeur est supérieure ou égale à la seconde.

**Syntaxe**

```sql
{%= expression1 >= expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées en 1970 ou après.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Inférieur à{#lessthan}

La fonction `<` (inférieur à) permet de vérifier si la première valeur est inférieure à la seconde.

**Syntaxe**

```sql
{%= expression1 < expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées avant 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Inférieur ou égal à{#lessthanorequal}

La fonction `<=` (inférieur ou égal à) permet de vérifier si la première valeur est inférieure ou égale à la seconde.

**Syntaxe**

```sql
{%= expression1 <= expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées en 2000 ou avant.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Opérations avec des nombres**
