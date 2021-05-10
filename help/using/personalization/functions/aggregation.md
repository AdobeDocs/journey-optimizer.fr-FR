---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 4f097636e059c5d0676b0129cdbdb125e5ad9415
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---

# Fonctions d&#39;agrégation {#aggregation}

![](../../assets/do-not-localize/badge.png)

Les fonctions d’agrégation sont utilisées pour regrouper plusieurs valeurs dans des tableaux [!DNL Profile Query Language] (PQL) afin de former une seule valeur de synthèse.

## Count{#count}

La fonction `count` renvoie le nombre d&#39;éléments contenus dans le tableau donné.

**Format**

```sql
count({ARRAY})
```

**Exemple**

L&#39;opération suivante renvoie le nombre de commandes dans le tableau.

```sql
{%=count(orders)%}
```

## Sum{#sum}

La fonction `sum` renvoie la somme de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
sum({ARRAY})
```

**Exemple**

L&#39;opération suivante renvoie la somme de tous les prix des commandes.

```sql
{%=sum(orders.order.price)%}
```

## Moyenne{#average}

La fonction `average` renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
average({ARRAY})
```

**Exemple**

L&#39;opération suivante renvoie le prix moyen de toutes les commandes.

```sql
{%=average(orders.order.price)%}
```

## Minimum{#min}

La fonction `min` renvoie la plus petite des valeurs sélectionnées dans le tableau.

**Format**

```sql
min({ARRAY})
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
max({ARRAY})
```

**Exemple**

L&#39;opération suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
{%=max(orders.order.price)%}
```
