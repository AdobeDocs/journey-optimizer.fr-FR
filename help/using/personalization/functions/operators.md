---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 5304db1456f0541d18823f862ae420892e46fd89
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 8%

---

# Les opérateurs {#operators}

![](../../assets/do-not-localize/badge.png)

## Et {#and}

La fonction `and` est utilisée pour créer une conjonction logique.

**Format**

```sql
{QUERY} and {QUERY}
```

**Exemple**

L&#39;opération suivante permettra de renvoyer toutes les personnes ayant le pays d&#39;origine comme Canada et année de naissance en 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Ou{#or}

La fonction `or` est utilisée pour créer une disjonction logique.

**Format**

```sql
{QUERY} or {QUERY}
```

**Exemple**

L&#39;opération suivante permettra à toutes les personnes qui ont un pays d&#39;origine de retourner au Canada ou à l&#39;année de naissance de 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Not{#not}

La fonction `not` (ou `!`) est utilisée pour créer une négation logique.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Exemple**

L&#39;opération suivante rendra au Canada toutes les personnes qui n&#39;ont pas leur pays d&#39;origine.

```sql
not (homeAddress.countryISO = "CA")
```

## If{#if}

La fonction `if` est utilisée pour résoudre une expression selon si une condition spécifiée est vraie.

**Format**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argument | Description |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | Expression booléenne qui est en cours de test. |
| `{TRUE_EXPRESSION}` | Expression dont la valeur sera utilisée si `{TEST_EXPRESSION}` est true. |
| `{FALSE_EXPRESSION}` | Expression dont la valeur sera utilisée si `{TEST_EXPRESSION}` est false. |

**Exemple**

L&#39;opération suivante définit la valeur sur `1` si le pays d&#39;origine est le Canada et `2` si le pays d&#39;origine n&#39;est pas le Canada.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Est égal à{#equals}

La fonction `=` (est égal à) vérifie si une valeur ou une expression est égale à une autre valeur ou expression.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Exemple**

L&#39;opération suivante vérifie si le pays d&#39;adresse d&#39;origine est au Canada.

```sql
homeAddress.countryISO = "CA"
```

## N’est pas égal{#notequal}

La fonction `!=` (différent) vérifie si une valeur ou une expression est **différente de** égale à une autre valeur ou expression.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Exemple**

L&#39;opération suivante vérifie si le pays d&#39;adresse d&#39;origine n&#39;est pas au Canada.

```sql
homeAddress.countryISO != "CA"
```

## Supérieur à{#greaterthan}

La fonction `>` (supérieure à) est utilisée pour vérifier si la première valeur est supérieure à la seconde.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Exemple**

L’opération suivante définit les personnes dont les anniversaires ne tombent pas en janvier ou février.

```sql
person.birthMonth > 2
```

## Supérieur ou égal à{#greaterthanorequal}

La fonction `>=` (supérieure ou égale à) est utilisée pour vérifier si la première valeur est supérieure ou égale à la seconde.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Exemple**

L’opération suivante définit les personnes dont les anniversaires ne tombent pas en janvier ou février.

```sql
person.birthMonth >= 3
```

## Inférieur à{#lessthan}

La fonction de comparaison `<` (inférieur à) permet de vérifier si la première valeur est inférieure à la seconde.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire est en janvier.

```sql
person.birthMonth < 2
```

## Inférieur ou égal à{#lessthanorequal}

La fonction de comparaison `<=` (inférieure ou égale à) permet de vérifier si la première valeur est inférieure ou égale à la seconde.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire est en janvier ou février.

```sql
person.birthMonth <= 2
```

## Ajoute{#add}

La fonction `+` (addition) est utilisée pour rechercher la somme de deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Exemple**

L&#39;opération suivante représente le prix de deux produits différents.

```sql
product1.price + product2.price
```

## Multiplier{#multiply}

La fonction `*` (multiplication) est utilisée pour trouver le produit de deux expressions d&#39;arguments.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Exemple**

L&#39;opération suivante recherche le produit de l&#39;inventaire et le prix d&#39;un produit pour trouver la valeur brute du produit.

```sql
product.inventory * product.price
```

## Soustraire{#substract}

La fonction `-` (soustraction) permet de trouver la différence entre deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Exemple**

L&#39;opération suivante identifie la différence de prix entre deux produits différents.

```sql
product1.price - product2.price
```

## Diviser {#divide}

La fonction `/` (division) est utilisée pour trouver le quotient de deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Exemple**

L&#39;opération suivante recherche le quotient entre le total des produits vendus et le total des recettes pour déterminer le coût moyen par article.

```sql
totalProduct.price / totalProduct.sold
```

## Reste{#remainder}

La fonction `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;âge de la personne est divisible de cinq ans.

```sql
person.age % 5 = 0
```
