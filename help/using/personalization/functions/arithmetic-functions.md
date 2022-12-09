---
title: Bibliothèque de fonctions arithmétiques
description: Bibliothèque de fonctions arithmétiques
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Fonctions arithmétiques {#maths}

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur les valeurs.

## Ajouter{#add}

Le `+` (addition) est utilisée pour trouver la somme de deux expressions d’argument.

**Format**

```sql
{%= double + double %}
```

**Exemple**

L&#39;opération suivante additionne le prix de deux produits différents.

```sql
{%= product1.price + product2.price %}
```

## Multiplier{#multiply}

Le `*` (multiplication) est utilisée pour trouver le produit de deux expressions d’argument.

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

Le `-` (soustraction) est utilisée pour trouver la différence entre deux expressions d’argument.

**Format**

```sql
{%= double - double %}
```

**Exemple**

L&#39;opération suivante permet de constater la différence de prix entre deux produits différents.

```sql
{%= product1.price - product2.price %}
```

## Diviser{#divide}

Le `/` (division) est utilisée pour trouver le quotient de deux expressions d’argument.

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

Le `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d’argument.

**Format**

```sql
{%= double % double %}
```

**Exemple**

L’opération suivante vérifie si l’âge de la personne est divisé par cinq.

```sql
{%= person.age % 5 = 0 %}
```
