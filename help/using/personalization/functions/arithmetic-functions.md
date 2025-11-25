---
title: Bibliothèque de fonctions arithmétiques
description: Bibliothèque de fonctions arithmétiques
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '180'
ht-degree: 100%

---

# Fonctions arithmétiques {#maths}

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur des valeurs.

## Addition{#add}

La fonction `+` (addition) est utilisée pour trouver la somme de deux expressions d&#39;argument.

**Syntaxe**

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

**Syntaxe**

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

**Syntaxe**

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

**Syntaxe**

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

**Syntaxe**

```sql
{%= double % double %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;âge de la personne est divisible par cinq.

```sql
{%= person.age % 5 = 0 %}
```
