---
title: Bibliothèque des fonctions d'agrégation
description: Bibliothèque des fonctions d'agrégation
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 100%

---

# Fonctions d&#39;agrégation {#aggregation}

Les fonctions d&#39;agrégation sont utilisées pour regrouper plusieurs valeurs afin de former une seule valeur de synthèse.

## Count{#count}

La fonction `count` renvoie le nombre d&#39;éléments dans le tableau donné.

**Format**

```sql
{%= count(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le nombre de commandes dans le tableau.

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

L&#39;opération suivante renvoie le prix moyen de toutes les commandes.

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

L&#39;opération suivante renvoie le prix le plus bas de toutes les commandes.

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

L&#39;opération suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
{%=max(orders.order.price)%}
```
