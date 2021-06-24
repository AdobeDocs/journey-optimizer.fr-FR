---
title: Bibliothèque de fonctions arithmétiques
description: Bibliothèque de fonctions arithmétiques
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 96%

---

# Fonctions arithmétiques  {#maths}

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur des valeurs.

## Addition{#add}

La fonction `+` (addition) est utilisée pour trouver la somme de deux expressions d&#39;argument.

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

La fonction `*` (multiplication) est utilisée pour trouver le produit de deux expressions d&#39;argument.

**Format**

```sql
{%= double * double %}
```

**Exemple**

L&#39;opération suivante trouve le produit de l&#39;inventaire et du prix d&#39;un produit pour obtenir la valeur brute du produit.

```sql
{%= product.inventory * product.price %}
```

## Soustraction{#substract}

La fonction `-` (soustraction) permet de trouver la différence entre deux expressions d&#39;argument.

**Format**

```sql
{%= double - double %}
```

**Exemple**

L&#39;opération suivante trouve la différence de prix entre deux produits différents.

```sql
{%= product1.price - product2.price %}
```

## Division{#divide}

La fonction `/` (division) est utilisée pour trouver le quotient de deux expressions d&#39;argument.

**Format**

```sql
{%= double / double %}
```

**Exemple**

L&#39;opération suivante trouve le quotient entre le total des produits vendus et le total des revenus obtenus pour déterminer le coût moyen par article.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Reste{#remainder}

La fonction `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d&#39;argument.

**Format**

```sql
{%= double % double %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;âge de la personne est divisible par cinq.

```sql
{%= person.age % 5 = 0 %}
```
