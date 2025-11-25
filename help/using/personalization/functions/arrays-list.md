---
title: Bibliothèque de fonctions de tableau
description: Bibliothèque de fonctions de tableau
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 07a582db495ecbfae97b6d299b65b06c0cdf8c14
workflow-type: ht
source-wordcount: '592'
ht-degree: 100%

---

# Fonctions de liste et de tableau {#arrays}

Utilisez ces fonctions pour faciliter l&#39;interaction avec des tableaux, des listes et des chaînes.

## Nombre uniquement nul {#count-only-null}

La fonction `countOnlyNull` sert à compter le nombre de valeurs nulles dans une liste.

**Syntaxe**

```sql
{%= countOnlyNull(array) %}
```

**Exemple**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Renvoie 3.

## Nombre avec nul {#count-with-null}

La fonction `countWithNull` est utilisée pour compter tous les éléments d’une liste, y compris les valeurs nulles.

**Syntaxe**

```sql
{%= countWithNull(array) %}
```

**Exemple**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Renvoie 6.

## Distinct{#distinct}

La fonction `distinct` est utilisée pour obtenir les valeurs d&#39;un tableau ou d&#39;une liste dont les valeurs en double sont supprimées.

**Syntaxe**

```sql
{%= distinct(array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont passé des commandes dans plusieurs magasins.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Nombre distinct avec nul {#distinct-count-with-null}

La fonction `distinctCountWithNull` sert à compter le nombre de valeurs différentes dans une liste, y compris les valeurs nulles.

**Syntaxe**

```sql
{%= distinctCountWithNull(array) %}
```

**Exemple**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Renvoie 3.

## Premier élément{#head}

La fonction `head` est utilisée pour renvoyer le premier élément dans un tableau ou une liste.

**Syntaxe**

```sql
{%= head(array) %}
```

**Exemple**

L&#39;opération suivante renvoie la première des cinq principales commandes au prix le plus élevé. Vous trouverez plus d&#39;informations sur la fonction `topN` dans la section [First `n` in array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Trier et obtenir les N premiers dans le tableau {#first-n}

La fonction `topN` trie un tableau par ordre décroissant en fonction de l’expression numérique donnée et renvoie les `N` premiers éléments. Si la taille du tableau est inférieure à `N`, il renvoie l’ensemble du tableau trié.

Cette fonction
**Syntaxe**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Description |
| --------- | ----------- |
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété dans laquelle trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d&#39;éléments à renvoyer. |

**Exemple**

L’opération suivante renvoie les cinq premières commandes au prix le plus bas.

```sql
{%= topN(orders,price, 5) %}
```

## Dans{#in}

La fonction `in` permet de déterminer si un élément est un membre d&#39;un tableau ou d&#39;une liste.

**Syntaxe**

```sql
{%= in(value, array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire est en mars, juin ou septembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Inclut{#includes}

La fonction `includes` permet de déterminer si un tableau ou une liste contient un élément donné.

**Syntaxe**

```sql
{%= includes(array,item) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont le rouge est l&#39;une des couleurs préférées.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersections{#intersects}

La fonction `intersects` permet de déterminer si deux tableaux ou deux listes ont au moins un membre commun.

**Syntaxe**

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

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Trier et obtenir les N derniers dans le tableau {#last-n}

La fonction `bottomN` trie un tableau par ordre croissant en fonction de l’expression numérique donnée et renvoie les `N` premiers éléments. Si la taille du tableau est inférieure à `N`, il renvoie l’ensemble du tableau trié.

**Syntaxe**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Description |
| --------- | ----------- | 
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété dans laquelle trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d&#39;éléments à renvoyer. |

**Exemple**

L’opération suivante renvoie les cinq dernières commandes au prix le plus élevé.

```sql
{%= bottomN(orders,price, 5) %}
```

## Pas dans{#notin}

La fonction `notIn` permet de déterminer si un élément n&#39;est pas un membre d&#39;un tableau ou d&#39;une liste.

>[!NOTE]
>
>La fonction `notIn` assure *également* qu&#39;aucune valeur n&#39;est nulle. Par conséquent, les résultats ne sont pas une négation exacte de la fonction `in`.

**Syntaxe**

```sql
{%= notIn(value, array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire n&#39;est ni en mars, ni en juin, ni en septembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Sous-ensemble de{#subset}

La fonction `subsetOf` sert à déterminer si un tableau spécifique (tableau A) est un sous-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, elle permet de déterminer si tous les éléments du tableau A sont des éléments du tableau B.

**Syntaxe**

```sql
{%= subsetOf(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont visité toutes leurs villes préférées.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Sur-ensemble de{#superset}

La fonction `supersetOf` sert à déterminer si un tableau spécifique (tableau A) est un sur-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, elle permet de déterminer si le tableau A contient tous les éléments du tableau B.

**Syntaxe**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont mangé des sushis et de la pizza au moins une fois.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```
