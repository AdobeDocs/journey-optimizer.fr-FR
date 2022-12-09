---
title: Bibliothèque des fonctions d’agrégation
description: Bibliothèque des fonctions d’agrégation
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Fonctions d’agrégation {#aggregation}

Les fonctions d’agrégation sont utilisées pour regrouper plusieurs valeurs afin de former une seule valeur de résumé.

## Moyenne{#average}

Le `average` renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= average(array) %}
```

**Exemple**

L’opération suivante renvoie le prix moyen de toutes les commandes.

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

Le `count` renvoie le nombre d’éléments dans le tableau donné.

**Format**

```sql
{%= count(array) %}
```

**Exemple**

L’opération suivante renvoie le nombre de commandes dans le tableau .

```sql
{%= count(orders) %}
```

## Maximum{#max}

Le `max` renvoie la plus grande de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= max(array) %}
```

**Exemple**

L’opération suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
{%=max(orders.order.price)%}
```

## Minimum{#min}

Le `min` renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= min(array) %}
```

**Exemple**

L’opération suivante renvoie le prix le plus bas de toutes les commandes.

```sql
{%=min(orders.order.price) %}
```

## Somme{#sum}

Le `sum` renvoie la somme de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
{%= sum(array) %}
```

**Exemple**

L&#39;opération suivante renvoie la somme des prix de toutes les commandes.

```sql
{%=sum(orders.order.price)%}
```
