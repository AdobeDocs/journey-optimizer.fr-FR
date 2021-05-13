---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 96%

---

# Tableaux et fonctions de liste {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre des fonctions pour faciliter l&#39;interaction avec les tableaux, les listes et les chaînes.

## In

La fonction `in` permet de déterminer si un élément est un membre d’un tableau ou d’une liste.

**Format**

```sql
in ({VALUE},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire est en mars, juin ou septembre.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Not in

La fonction `notIn` permet de déterminer si un élément n’est pas un membre d’un tableau ou d’une liste.

>[!NOTE]
>
>La fonction `notIn` assure *également* qu’aucune valeur n’est nulle. Par conséquent, les résultats ne sont pas une négation exacte de la fonction `in`.

**Format**

```sql
notIn ({VALUE},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire n’est ni en mars, ni en juin, ni en septembre.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersects

La fonction `intersects` permet de déterminer si deux tableaux ou deux listes ont au moins un membre commun.

**Format**

```sql
intersects({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes dont les couleurs préférées comprennent au moins le rouge, le bleu ou le vert.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Intersection

La fonction `intersection` sert à déterminer les membres communs à deux tableaux ou deux listes.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit si la personne 1 et la personne°2 ont toutes deux des couleurs préférées parmi le rouge, le bleu et le vert.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Subset of

La fonction `subsetOf` sert à déterminer si un tableau spécifique (tableau A) est un sous-ensemble d’un autre tableau (tableau B). En d’autres termes, elle permet de déterminer si tous les éléments du tableau A sont des éléments du tableau B.

**Format**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes qui ont visité toutes leurs villes préférées.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Superset of

La fonction `supersetOf` sert à déterminer si un tableau spécifique (tableau A) est un sur-ensemble d’un autre tableau (tableau B). En d’autres termes, elle permet de déterminer si le tableau A contient tous les éléments du tableau B.

**Format**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes qui ont mangé des sushis et de la pizza au moins une fois.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Includes

La fonction `includes` permet de déterminer si un tableau ou une liste contient un élément donné.

**Format**

```sql
includes({ARRAY},{ITEM})
```

**Exemple**

La requête PQL suivante définit les personnes dont le rouge est l’une des couleurs préférées.

```sql
includes(person.favoriteColors,"red")
```

## Distinct

La fonction `distinct` est utilisée pour supprimer les doublons d’un tableau ou d’une liste.

**Format**

```sql
distinct({ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes qui ont passé des commandes dans plusieurs magasins.

```sql
distinct(person.orders.storeId).count() > 1
```

## First `n` in array {#first-n}

La fonction `topN` est utilisée pour renvoyer les premiers éléments `N` d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction d’une expression numérique donnée.

**Format**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Description |
| --------- | ----------- |
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété dans laquelle trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d’éléments à renvoyer. |

**Exemple**

La requête PQL suivante renvoie les cinq premières commandes au prix le plus élevé.

```sql
topN(orders,price, 5)
```

## Last `n` in array

La fonction `bottomN` est utilisée pour renvoyer les derniers éléments `N` d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction d’une expression numérique donnée.

**Format**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Description |
| --------- | ----------- | 
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété dans laquelle trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d’éléments à renvoyer. |

**Exemple**

La requête PQL suivante renvoie les cinq premières commandes au prix le plus bas.

```sql
bottomN(orders,price, 5)
```

## First item

La fonction `head` est utilisée pour renvoyer le premier élément du tableau ou de la liste.

**Format**

```sql
head({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie la première des cinq premières commandes au prix le plus élevé. Vous trouverez plus d’informations sur la fonction `topN` dans la section [First `n` in array](#first-n).

```sql
head(topN(orders,price, 5))
```
