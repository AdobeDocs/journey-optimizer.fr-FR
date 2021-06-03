---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 51%

---

# Fonctions arithmétiques {#maths}

![](../../assets/do-not-localize/badge.png)

Fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur les valeurs.

## Addition{#add}

La fonction `+` (addition) est utilisée pour trouver la somme de deux expressions d’argument.

**Format**

```sql
{%= double + double %}
```

**Exemple**

L&#39;opération suivante additionne le prix de deux produits différents.

```sql
{%= product1.price + product2.price %}
```

## Multiplication{#multiply}

La fonction `*` (multiplication) est utilisée pour trouver le produit de deux expressions d’argument.

**Format**

```sql
{%= double * double %}
```

**Exemple**

L’opération suivante recherche le produit de l’inventaire et le prix d’un produit pour trouver la valeur brute du produit.

```sql
{%= product.inventory * product.price %}
```

## Soustraction{#substract}

La fonction `-` (soustraction) permet de trouver la différence entre deux expressions d’argument.

**Format**

```sql
{%= double - double %}
```

**Exemple**

L&#39;opération suivante permet de constater la différence de prix entre deux produits différents.

```sql
{%= product1.price - product2.price %}
```

## Division{#divide}

La fonction `/` (division) est utilisée pour trouver le quotient de deux expressions d’argument.

**Format**

```sql
{%= double / double %}
```

**Exemple**

L’opération suivante recherche le quotient entre le total des produits vendus et le total des revenus générés pour visualiser le coût moyen par article.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Reste{#remainder}

La fonction `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d’argument.

**Format**

```sql
{%= double % double %}
```

**Exemple**

L’opération suivante vérifie si l’âge de la personne est divisé par cinq.

```sql
{%= person.age % 5 = 0 %}
```
