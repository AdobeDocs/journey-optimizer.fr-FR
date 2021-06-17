---
title: Bibliothèque de fonctions de tableau
description: Bibliothèque de fonctions de tableau
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 66%

---

# Tableaux et fonctions de liste {#arrays}

Utilisez ces fonctions pour faciliter l’interaction avec des tableaux, des listes et des chaînes.

## Distinct{#distinct}

La fonction `distinct` est utilisée pour obtenir des valeurs d’un tableau ou d’une liste dont les valeurs en double sont supprimées.

**Format**

```sql
{%= distinct(array) %}
```

**Exemple**

L’opération suivante spécifie les personnes qui ont passé des commandes dans plusieurs magasins.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## First item{#head}

La fonction `head` est utilisée pour renvoyer le premier élément du tableau ou de la liste.

**Format**

```sql
{%= head({array}) %}
```

**Exemple**

L’opération suivante renvoie la première des cinq premières commandes au prix le plus élevé. Vous trouverez plus d’informations sur la fonction `topN` dans la section [First `n` in array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## First `n` in array {#first-n}

La fonction `topN` est utilisée pour renvoyer les premiers éléments `N` d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction d’une expression numérique donnée.

**Format**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Description |
| --------- | ----------- |
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété dans laquelle trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d’éléments à renvoyer. |

**Exemple**

L’opération suivante renvoie les cinq premières commandes au prix le plus élevé.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

La fonction `in` permet de déterminer si un élément est un membre d’un tableau ou d’une liste.

**Format**

```sql
{%= in(value, array) %}
```

**Exemple**

L’opération suivante définit les personnes dont l’anniversaire a lieu en mars, juin ou septembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Includes{#includes}

La fonction `includes` permet de déterminer si un tableau ou une liste contient un élément donné.

**Format**

```sql
{%= includes(array,item) %}
```

**Exemple**

L’opération suivante définit les personnes dont la couleur préférée inclut le rouge.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersects{#intersects}

La fonction `intersects` permet de déterminer si deux tableaux ou deux listes ont au moins un membre commun.

**Format**

```sql
{%= intersects(array1, array2) %}
```

**Exemple**

L’opération suivante définit les personnes dont les couleurs préférées comprennent au moins le rouge, le bleu ou le vert.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Last `n` in array{#last-n}

La fonction `bottomN` est utilisée pour renvoyer les derniers éléments `N` d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction d’une expression numérique donnée.

**Format**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Description |
| --------- | ----------- | 
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété dans laquelle trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d’éléments à renvoyer. |

**Exemple**

L’opération suivante renvoie les cinq premières commandes au prix le plus bas.

```sql
{%= bottomN(orders,price, 5) %}
```


## Not in{#notin}

La fonction `notIn` permet de déterminer si un élément n’est pas un membre d’un tableau ou d’une liste.

>[!NOTE]
>
>La fonction `notIn` assure *également* qu’aucune valeur n’est nulle. Par conséquent, les résultats ne sont pas une négation exacte de la fonction `in`.

**Format**

```sql
{%= notIn(value, array) %}
```

**Exemple**

L’opération suivante définit les personnes dont l’anniversaire n’est pas en mars, juin ou septembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subset of{#subset}

La fonction `subsetOf` sert à déterminer si un tableau spécifique (tableau A) est un sous-ensemble d’un autre tableau (tableau B). En d’autres termes, elle permet de déterminer si tous les éléments du tableau A sont des éléments du tableau B.

**Format**

```sql
{%= subsetOf(array1, array2) %}
```

**Exemple**

L’opération suivante définit les personnes qui ont visité toutes leurs villes préférées.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superset of{#superset}

La fonction `supersetOf` sert à déterminer si un tableau spécifique (tableau A) est un sur-ensemble d’un autre tableau (tableau B). En d’autres termes, elle permet de déterminer si le tableau A contient tous les éléments du tableau B.

**Format**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemple**

L’opération suivante définit les personnes qui ont mangé des sushis et des pizzas au moins une fois.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







