---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 99%

---

# Opérateurs {#operators}

![](../../assets/do-not-localize/badge.png)

## And

La fonction `and` sert à créer une conjonction logique.

**Format**

```sql
{QUERY} and {QUERY}
```

**Exemple**

La requête suivante PQL renverra toutes les personnes ayant pour pays d’origine le Canada et pour année de naissance 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Or

La fonction `or` est utilisée pour créer une disjonction logique.

**Format**

```sql
{QUERY} or {QUERY}
```

**Exemple**

La requête suivante PQL renverra toutes les personnes ayant pour pays d’origine le Canada ou pour année de naissance 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Not

La fonction `not` (ou `!`) est utilisée pour créer une négation logique.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Exemple**

La requête suivante PQL renverra toutes les personnes qui n’ont pas pour pays d’origine le Canada.

```sql
not (homeAddress.countryISO = "CA")
```

## If

La fonction `if` est utilisée pour résoudre une expression selon qu’une condition spécifiée est vraie ou non.

**Format**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argument | Description |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | L’expression booléenne en cours de test. |
| `{TRUE_EXPRESSION}` | L’expression dont la valeur sera utilisée si `{TEST_EXPRESSION}` est vraie. |
| `{FALSE_EXPRESSION}` | L’expression dont la valeur sera utilisée si `{TEST_EXPRESSION}` est fausse. |

**Exemple**

La requête PQL suivante définit la valeur sur `1` si le pays d’origine est le Canada et sur `2` si le pays d’origine n’est pas le Canada.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Est égal à

La fonction `=` (est égal) vérifie si une valeur ou expression est égale à une autre valeur ou expression.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Exemple**

La requête PQL suivante vérifie si le pays de l’adresse du domicile est le Canada.

```sql
homeAddress.countryISO = "CA"
```

## Différent de

La fonction `!=` (différent de) vérifie si une valeur ou expression est **différente** d’une autre valeur ou expression.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Exemple**

La requête PQL suivante vérifie si le pays de l’adresse du domicile n’est pas le Canada.

```sql
homeAddress.countryISO != "CA"
```

## Supérieur à

La fonction `>` (supérieur à) permet de vérifier si la première valeur est supérieure à la seconde.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire ne tombe ni en janvier ni en février.

```sql
person.birthMonth > 2
```

## Supérieur ou égal à

La fonction `>=` (supérieur ou égal à) permet de vérifier si la première valeur est supérieure ou égale à la seconde.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire ne tombe ni en janvier ni en février.

```sql
person.birthMonth >= 3
```

## Inférieur à

La fonction `<` (inférieur à) permet de vérifier si la première valeur est inférieure à la seconde.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire tombe en janvier.

```sql
person.birthMonth < 2
```

## Inférieur ou égal à

La fonction `<=` (inférieur ou égal à) permet de vérifier si la première valeur est inférieure ou égale à la seconde.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire tombe en janvier ou en février.

```sql
person.birthMonth <= 2
```

## Addition

La fonction `+` (addition) est utilisée pour trouver la somme de deux expressions d’argument.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Exemple**

La requête PQL suivante additionne le prix de deux produits différents.

```sql
product1.price + product2.price
```

## Multiplication

La fonction `*` (multiplication) est utilisée pour trouver le produit de deux expressions d’argument.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Exemple**

La requête PQL suivante trouve le produit de l’inventaire et du prix d’un produit pour obtenir la valeur brute du produit.

```sql
product.inventory * product.price
```

## Soustraction

La fonction `-` (soustraction) permet de trouver la différence entre deux expressions d’argument.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Exemple**

La requête PQL suivante trouve la différence de prix entre deux produits différents.

```sql
product1.price - product2.price
```

## Division

La fonction `/` (division) est utilisée pour trouver le quotient de deux expressions d’argument.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Exemple**

La requête PQL suivante trouve le quotient entre le total des produits vendus et le total des revenus obtenus pour déterminer le coût moyen par article.

```sql
totalProduct.price / totalProduct.sold
```

## Reste

La fonction `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d’argument.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Exemple**

La requête PQL suivante vérifie si l’âge de la personne est divisible par cinq.

```sql
person.age % 5 = 0
```
