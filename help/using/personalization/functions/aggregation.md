---
title: Bibliothèque des fonctions d'agrégation
description: Bibliothèque des fonctions d'agrégation
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '157'
ht-degree: 100%

---

# Fonctions d&#39;agrégation {#aggregation}

Les fonctions d&#39;agrégation sont utilisées pour regrouper plusieurs valeurs afin de former une seule valeur de synthèse.

## Moyenne{#average}

La fonction `average` renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.

**Syntaxe**

```sql
{%= average(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le prix moyen de toutes les commandes.

```sql
{%=average(orders.order.price)%}
```

## Nombre{#count}

La fonction `count` renvoie le nombre d&#39;éléments dans le tableau donné.

**Syntaxe**

```sql
{%= count(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le nombre de commandes dans le tableau.

```sql
{%= count(orders) %}
```

## Maximum{#max}

La fonction `max` renvoie la plus grande de toutes les valeurs sélectionnées dans le tableau.

**Syntaxe**

```sql
{%= max(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
{%=max(orders.order.price)%}
```

## Minimum{#min}

La fonction `min` renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau.

**Syntaxe**

```sql
{%= min(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le prix le plus bas de toutes les commandes.

```sql
{%=min(orders.order.price) %}
```

## Somme{#sum}

La fonction `sum` renvoie la somme de toutes les valeurs sélectionnées dans le tableau.

**Syntaxe**

```sql
{%= sum(array) %}
```

**Exemple**

L&#39;opération suivante renvoie la somme des prix de toutes les commandes.

```sql
{%=sum(orders.order.price)%}
```
