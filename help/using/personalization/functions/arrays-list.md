---
title: Bibliothèque de fonctions de tableau
description: Bibliothèque de fonctions de tableau
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Tableaux et fonctions de liste {#arrays}

Utilisez ces fonctions pour faciliter l’interaction avec des tableaux, des listes et des chaînes.

## Count only null {#count-only-null}

Le `countOnlyNull` sert à compter le nombre de valeurs &quot;null&quot; dans une liste.

**Format**

```sql
{%= countOnlyNull(array) %}
```

**Exemple**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Renvoie 3.

## Compter avec valeur nulle {#count-with-null}

Le `countWithNull` est utilisée pour compter tous les éléments d’une liste, y compris les valeurs nulles.

**Format**

```sql
{%= countWithNull(array) %}
```

**Exemple**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Renvoie 6.

## Distinct{#distinct}

Le `distinct` est utilisée pour obtenir des valeurs d’un tableau ou d’une liste dont les valeurs en double sont supprimées.

**Format**

```sql
{%= distinct(array) %}
```

**Exemple**

L’opération suivante spécifie les personnes qui ont passé des commandes dans plusieurs magasins.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Comptage distinct avec valeur nulle {#distinct-count-with-null}

Le `distinctCountWithNull` sert à compter le nombre de valeurs différentes dans une liste, y compris les valeurs &quot;null&quot;.

**Format**

```sql
{%= distinctCountWithNull(array) %}
```

**Exemple**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Renvoie 3.

## Premier élément{#head}

Le `head` est utilisée pour renvoyer le premier élément d’un tableau ou d’une liste.

**Format**

```sql
{%= head(array) %}
```

**Exemple**

L’opération suivante renvoie la première des cinq premières commandes au prix le plus élevé. En savoir plus sur la variable `topN` se trouve dans la fonction [first `n` in array](#first-n) .

```sql
{%= head(topN(orders,price, 5)) %}
```

## First `n` in array {#first-n}

Le `topN` est utilisée pour renvoyer la première fonction `N` éléments d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction d’une expression numérique donnée.

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

## Dans{#in}

Le `in` sert à déterminer si un élément est membre d’un tableau ou d’une liste.

**Format**

```sql
{%= in(value, array) %}
```

**Exemple**

L’opération suivante définit les personnes dont l’anniversaire a lieu en mars, juin ou septembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Inclut{#includes}

Le `includes` sert à déterminer si un tableau ou une liste contient un élément donné.

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

Le `intersects` sert à déterminer si deux tableaux ou deux listes ont au moins un membre commun.

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

## Dernière `n` in array{#last-n}

Le `bottomN` sert à renvoyer la dernière fonction `N` éléments d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction d’une expression numérique donnée.

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

Le `notIn` sert à déterminer si un élément n’est pas membre d’un tableau ou d’une liste.

>[!NOTE]
>
>Le `notIn` function *également* s’assure qu’aucune valeur n’est nulle. Par conséquent, les résultats ne sont pas une négation exacte de la variable `in` fonction .

**Format**

```sql
{%= notIn(value, array) %}
```

**Exemple**

L’opération suivante définit les personnes dont l’anniversaire n’est pas en mars, juin ou septembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Sous-ensemble de{#subset}

Le `subsetOf` sert à déterminer si un tableau spécifique (tableau A) est un sous-ensemble d’un autre tableau (tableau B). En d’autres termes, que tous les éléments du tableau A sont des éléments du tableau B.

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

Le `supersetOf` sert à déterminer si un tableau spécifique (tableau A) est un sur-ensemble d’un autre tableau (tableau B). En d’autres termes, ce tableau A contient tous les éléments du tableau B.

**Format**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemple**

L’opération suivante définit les personnes qui ont mangé des sushis et des pizzas au moins une fois.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
