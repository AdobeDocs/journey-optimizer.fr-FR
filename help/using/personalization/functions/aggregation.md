---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 54%

---

# Fonctions d’agrégation {#aggregation}

![](../../assets/do-not-localize/badge.png)

Les fonctions d’agrégation sont utilisées pour regrouper plusieurs valeurs afin de former une seule valeur de résumé.

## Count{#count}

La fonction `count` renvoie le nombre d’éléments dans le tableau donné.

**Format**

```sql
{%= count(array) %}
```

**Exemple**

L’opération suivante renvoie le nombre de commandes dans le tableau .

```sql
{%= count(orders) %}
```

## Sum{#sum}

La fonction `sum` renvoie la somme de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= sum(array) %}
```

**Exemple**

L&#39;opération suivante renvoie la somme des prix de toutes les commandes.

```sql
{%=sum(orders.order.price)%}
```

## Average{#average}

La fonction `average` renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= average(array) %}
```

**Exemple**

L’opération suivante renvoie le prix moyen de toutes les commandes.

```sql
{%=average(orders.order.price)%}
```

## Minimum{#min}

La fonction `min` renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= min(array) %}
```

**Exemple**

L’opération suivante renvoie le prix le plus bas de toutes les commandes.

```sql
{%=min(orders.order.price)%}
```

## Maximum{#max}

La fonction `max` renvoie la plus grande de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= max(array) %}
```

**Exemple**

L’opération suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
{%=max(orders.order.price)%}
```
