---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 4%

---

# Tableaux et fonctions de liste {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre des fonctions pour faciliter l&#39;interaction avec les tableaux, les listes et les chaînes.

## Dans {#in}

La fonction `in` est utilisée pour déterminer si un élément est membre d&#39;un tableau ou d&#39;une liste.

**Format**

```sql
in ({VALUE},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes ayant un anniversaire en mars, juin ou septembre.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Pas dans {#notin}

La fonction `notIn` est utilisée pour déterminer si un élément n&#39;est pas membre d&#39;un tableau ou d&#39;une liste.

>[!NOTE]
>
>La fonction `notIn` *également* garantit qu&#39;aucune valeur n&#39;est égale à null. Par conséquent, les résultats ne sont pas une négation exacte de la fonction `in`.

**Format**

```sql
notIn ({VALUE},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes dont l’anniversaire n’est ni en mars, ni en juin, ni en septembre.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersects{#intersects}

La fonction `intersects` est utilisée pour déterminer si deux tableaux ou listes ont au moins un membre commun.

**Format**

```sql
intersects({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes dont les couleurs préférées comprennent au moins une couleur rouge, bleue ou verte.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Intersection{#intersection}

La fonction `intersection` est utilisée pour déterminer les membres communs de deux tableaux ou listes.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit si la personne 1 et la personne 2 ont toutes deux des couleurs préférées de rouge, de bleu et de vert.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Sous-ensemble de {#subset}

La fonction `subsetOf` est utilisée pour déterminer si un tableau spécifique (tableau A) est un sous-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, tous les éléments du tableau A sont des éléments du tableau B.

**Format**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes qui ont visité toutes leurs villes préférées.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Supérieur de {#superset}

La fonction `supersetOf` est utilisée pour déterminer si un tableau spécifique (tableau A) est un superset d&#39;un autre tableau (tableau B). En d&#39;autres termes, ce tableau A contient tous les éléments du tableau B.

**Format**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Exemple**

La requête PQL suivante définit les personnes qui ont mangé au moins une fois des sushis et des pizzas.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Inclut{#includes}

La fonction `includes` est utilisée pour déterminer si un tableau ou une liste contient un élément donné.

**Format**

```sql
includes({ARRAY},{ITEM})
```

**Exemple**

La requête PQL suivante définit les personnes dont la couleur préférée est le rouge.

```sql
includes(person.favoriteColors,"red")
```

## Distinct{#distinct}

La fonction `distinct` permet de supprimer des valeurs de duplicata d&#39;un tableau ou d&#39;une liste.

**Format**

```sql
distinct({ARRAY})
```

**Exemple**

La requête PQL suivante spécifie les personnes qui ont passé des commandes dans plusieurs magasins.

```sql
distinct(person.orders.storeId).count() > 1
```

## Premier `n` de la baie {#first-n}

La fonction `topN` est utilisée pour renvoyer les premiers éléments `N` d&#39;un tableau, lorsqu&#39;ils sont triés par ordre croissant en fonction de l&#39;expression numérique donnée.

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

## Dernier `n` tableau

La fonction `bottomN` est utilisée pour renvoyer les derniers éléments `N` dans un tableau, lorsqu&#39;ils sont triés par ordre croissant en fonction de l&#39;expression numérique donnée.

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

La requête PQL suivante renvoie les cinq premières commandes ayant le prix le plus bas.

```sql
bottomN(orders,price, 5)
```

## Premier élément{#head}

La fonction `head` est utilisée pour renvoyer le premier élément du tableau ou de la liste.

**Format**

```sql
head({ARRAY})
```

**Exemple**

La requête PQL suivante renvoie la première des cinq premières commandes ayant le prix le plus élevé. Pour plus d&#39;informations sur la fonction `topN`, consultez la section [first `n` dans array](#first-n).

```sql
head(topN(orders,price, 5))
```
