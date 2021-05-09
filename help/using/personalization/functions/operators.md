---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# Opérateurs {#operators}

![](../../assets/do-not-localize/badge.png)

## Et

La fonction `and` est utilisée pour créer une conjonction logique.

**Format**

```sql
{QUERY} and {QUERY}
```

**Exemple**

La requête suivante de la LPQ remettra à toutes les personnes ayant le pays d&#39;origine le Canada et l&#39;année de naissance de 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Ou

La fonction `or` est utilisée pour créer une disjonction logique.

**Format**

```sql
{QUERY} or {QUERY}
```

**Exemple**

La requête suivante de la LPQ remettra à toutes les personnes ayant le pays d&#39;origine le Canada ou l&#39;année de naissance de 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Non

La fonction `not` (ou `!`) est utilisée pour créer une négation logique.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Exemple**

La requête suivante de la LPQ rendra au Canada toutes les personnes qui n&#39;ont pas leur pays d&#39;origine.

```sql
not (homeAddress.countryISO = "CA")
```

## If

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

La requête suivante définit la valeur sur `1` si le pays d&#39;origine est le Canada et `2` si le pays d&#39;origine n&#39;est pas le Canada.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Est égal à

La fonction `=` (est égal à) vérifie si une valeur ou une expression est égale à une autre valeur ou expression.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Exemple**

La requête PQL suivante vérifie si le pays d&#39;adresse d&#39;origine est au Canada.

```sql
homeAddress.countryISO = "CA"
```

## N’est pas égal

La fonction `!=` (différent) vérifie si une valeur ou une expression est **différente de** égale à une autre valeur ou expression.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Exemple**

La requête PQL suivante vérifie si le pays d&#39;adresse d&#39;origine n&#39;est pas au Canada.

```sql
homeAddress.countryISO != "CA"
```

## Supérieur à

La fonction `>` (supérieure à) est utilisée pour vérifier si la première valeur est supérieure à la seconde.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont les anniversaires ne tombent pas en janvier ou février.

```sql
person.birthMonth > 2
```

## Supérieur ou égal à

La fonction `>=` (supérieure ou égale à) est utilisée pour vérifier si la première valeur est supérieure ou égale à la seconde.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont les anniversaires ne tombent pas en janvier ou février.

```sql
person.birthMonth >= 3
```

## Inférieur à

La fonction de comparaison `<` (inférieur à) permet de vérifier si la première valeur est inférieure à la seconde.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont l&#39;anniversaire a lieu en janvier.

```sql
person.birthMonth < 2
```

## Inférieur ou égal à

La fonction de comparaison `<=` (inférieure ou égale à) permet de vérifier si la première valeur est inférieure ou égale à la seconde.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Exemple**

La requête PQL suivante définit les personnes dont l&#39;anniversaire est en janvier ou février.

```sql
person.birthMonth <= 2
```

## Ajoute

La fonction `+` (addition) est utilisée pour rechercher la somme de deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Exemple**

La requête PQL suivante résume le prix de deux produits différents.

```sql
product1.price + product2.price
```

## Multiplier

La fonction `*` (multiplication) est utilisée pour trouver le produit de deux expressions d&#39;arguments.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Exemple**

La requête suivante de la LPQ recherche le produit de l&#39;inventaire et le prix d&#39;un produit pour déterminer la valeur brute du produit.

```sql
product.inventory * product.price
```

## Soustraire

La fonction `-` (soustraction) permet de trouver la différence entre deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Exemple**

La requête PQL suivante identifie la différence de prix entre deux produits différents.

```sql
product1.price - product2.price
```

## Diviser

La fonction `/` (division) est utilisée pour trouver le quotient de deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Exemple**

La requête suivante de PQL recherche le quotient entre le total des produits vendus et le total des sommes gagnées pour déterminer le coût moyen par article.

```sql
totalProduct.price / totalProduct.sold
```

## Reste

La fonction `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Exemple**

La requête PQL suivante vérifie si l&#39;âge de la personne est divisible de cinq ans.

```sql
person.age % 5 = 0
```
