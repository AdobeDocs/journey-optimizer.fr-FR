---
title: Bibliothèque de fonctions de tableau
description: Bibliothèque de fonctions de tableau
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 100%

---

# Fonctions de liste et de tableau {#arrays}

Utilisez ces fonctions pour faciliter l&#39;interaction avec des tableaux, des listes et des chaînes.

## Distinct{#distinct}

La fonction `distinct` est utilisée pour obtenir les valeurs d&#39;un tableau ou d&#39;une liste dont les valeurs en double sont supprimées.

**Format**

```sql
{%= distinct(array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont passé des commandes dans plusieurs magasins.

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

L&#39;opération suivante renvoie la première des cinq premières commandes au prix le plus élevé. Vous trouverez plus d&#39;informations sur la fonction `topN` dans la section [First `n` in array](#first-n).

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
| `{AMOUNT}` | Nombre d&#39;éléments à renvoyer. |

**Exemple**

L&#39;opération suivante renvoie les cinq premières commandes au prix le plus élevé.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

La fonction `in` permet de déterminer si un élément est un membre d&#39;un tableau ou d&#39;une liste.

**Format**

```sql
{%= in(value, array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire est en mars, juin ou septembre.

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

L&#39;opération suivante définit les personnes dont le rouge est l&#39;une des couleurs préférées.

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

L&#39;opération suivante définit les personnes dont les couleurs préférées comprennent au moins le rouge, le bleu ou le vert.

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
| `{AMOUNT}` | Nombre d&#39;éléments à renvoyer. |

**Exemple**

L&#39;opération suivante renvoie les cinq premières commandes au prix le plus bas.

```sql
{%= bottomN(orders,price, 5) %}
```


## Not in{#notin}

La fonction `notIn` permet de déterminer si un élément n&#39;est pas un membre d&#39;un tableau ou d&#39;une liste.

>[!NOTE]
>
>La fonction `notIn` assure *également* qu&#39;aucune valeur n&#39;est nulle. Par conséquent, les résultats ne sont pas une négation exacte de la fonction `in`.

**Format**

```sql
{%= notIn(value, array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire n&#39;est ni en mars, ni en juin, ni en septembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subset of{#subset}

La fonction `subsetOf` sert à déterminer si un tableau spécifique (tableau A) est un sous-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, elle permet de déterminer si tous les éléments du tableau A sont des éléments du tableau B.

**Format**

```sql
{%= subsetOf(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont visité toutes leurs villes préférées.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superset of{#superset}

La fonction `supersetOf` sert à déterminer si un tableau spécifique (tableau A) est un sur-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, elle permet de déterminer si le tableau A contient tous les éléments du tableau B.

**Format**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont mangé des sushis et de la pizza au moins une fois.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
