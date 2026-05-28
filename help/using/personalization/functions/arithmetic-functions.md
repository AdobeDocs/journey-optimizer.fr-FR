---
title: Bibliothèque de fonctions arithmétiques
description: Bibliothèque de fonctions arithmétiques
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
TQID: https://experienceleague.adobe.com/vQcfLG40Xhz4-ebm--J875oU4o-6BXC0SvNq24OOyTk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 180
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
