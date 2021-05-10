---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 5%

---

# Fonctions mathématiques {#math}

![](../../assets/do-not-localize/badge.png)

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur les valeurs de [!DNL Profile Query Language] (PQL).

## Ajoute{#add}

La fonction `+` (addition) est utilisée pour rechercher la somme de deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Exemple**

L&#39;opération suivante représente le prix de deux produits différents.

```
{%=product1.price + product2.price%}
```

## Multiplier{#multiply}

La fonction `*` (multiplication) est utilisée pour trouver le produit de deux expressions d&#39;arguments.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Exemple**

L&#39;opération suivante recherche le produit de l&#39;inventaire et le prix d&#39;un produit pour trouver la valeur brute du produit.

```
{%=product.inventory * product.price%}
```

## Soustraire{#substract}

La fonction `-` (soustraction) permet de trouver la différence entre deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Exemple**

L&#39;opération suivante identifie la différence de prix entre deux produits différents.

```
{%=product1.price - product2.price%}
```

## Diviser {#divide}

La fonction `/` (division) est utilisée pour trouver le quotient de deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Exemple**

L&#39;opération suivante recherche le quotient entre le total des produits vendus et le total des recettes pour déterminer le coût moyen par article.

```
{%=totalProduct.price / totalProduct.sold%}
```

## Reste{#remainder}

La fonction `%` (modulo/reste) est utilisée pour trouver le reste après la division des deux expressions d&#39;argument.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;âge de la personne est divisible de cinq ans.

```
{%=person.age % 5 = 0%}
```
