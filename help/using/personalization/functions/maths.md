---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Fonctions mathématiques {#math}

![](../../assets/do-not-localize/badge.png)

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur les valeurs de [!DNL Profile Query Language] (PQL).

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
