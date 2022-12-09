---
title: Bibliothèque des fonctions des opérateurs
description: Bibliothèque des fonctions des opérateurs
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Opérateurs {#operators}

## Fonctions booléennes {#boolean-functions}

Les fonctions booléennes sont utilisées pour exécuter une logique booléenne sur différents éléments.

### Et{#and}

Le `and` sert à créer une conjonction logique.

**Format**

```sql
{%= query1 and query2 %}
```

**Exemple**

L&#39;opération suivante renverra toutes les personnes ayant pour pays d&#39;origine la France et année de naissance 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Ou{#or}

Le `or` est utilisée pour créer une disjonction logique.

**Format**

```sql
{%= query1 or query2 %}
```

**Exemple**

L&#39;opération suivante renverra toutes les personnes ayant pour pays d&#39;origine la France ou année de naissance 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

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

## Fonctions de comparaison {#comparison-functions}

Les fonctions de comparaison sont utilisées pour comparer différentes expressions et valeurs, renvoyant true ou false en conséquence.

### Est égal à{#equals}

Le `=` (est égal) vérifie si une valeur ou expression est égale à une autre valeur ou expression.

**Format**

```sql
{%= expression = value %}
```

**Exemple**

L&#39;opération suivante vérifie si le pays de l&#39;adresse du domicile est la France.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Différent de{#notequal}

Le `!=` (différent de) la fonction vérifie si une valeur ou expression est **not** égal à une autre valeur ou expression.

**Format**

```sql
{%= expression != value %}
```

**Exemple**

L&#39;opération suivante vérifie si le pays de l&#39;adresse du domicile n&#39;est pas la France.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Supérieur à{#greaterthan}

Le `>` (supérieur à) permet de vérifier si la première valeur est supérieure à la seconde.

**Format**

```sql
{%= expression1 > expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées strictement après 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Supérieur ou égal à{#greaterthanorequal}

Le `>=` (supérieur ou égal à) permet de vérifier si la première valeur est supérieure ou égale à la seconde.

**Format**

```sql
{%= expression1 >= expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées en 1970 ou après.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Inférieur à{#lessthan}

Le `<` (inférieur à) permet de vérifier si la première valeur est inférieure à la seconde.

**Format**

```sql
{%= expression1 < expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées avant 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Inférieur ou égal à{#lessthanorequal}

Le `<=` (inférieur ou égal à) permet de vérifier si la première valeur est inférieure ou égale à la seconde.

**Format**

```sql
{%= expression1 <= expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées en 2000 ou avant.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Opérations avec des nombres**
