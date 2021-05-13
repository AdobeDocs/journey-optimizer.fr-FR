---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 85%

---

# Fonctions d&#39;agrégation {#aggregation}

![](../../assets/do-not-localize/badge.png)

Les fonctions d’agrégation sont utilisées pour regrouper plusieurs valeurs dans des tableaux [!DNL Profile Query Language] (PQL) afin de former une seule valeur de synthèse.

## Count

La fonction `count` renvoie le nombre d’éléments dans le tableau donné.

**Format**

```sql
count({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie le nombre de commandes du tableau.

```sql
count(orders)
```

## Sum

La fonction `sum` renvoie la somme de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
sum({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie la somme des prix de toutes les commandes.

```sql
sum(orders.order.price)
```

## Average

La fonction `average` renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
average({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie le prix moyen de toutes les commandes.

```sql
average(orders.order.price)
```

## Minimum

La fonction `min` renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
min({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie le prix le plus bas de toutes les commandes.

```sql
min(orders.order.price)
```

## Maximum

La fonction `max` renvoie la plus grande de toutes les valeurs sélectionnées dans le tableau.

**Format**

```sql
max({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
max(orders.order.price)
```
