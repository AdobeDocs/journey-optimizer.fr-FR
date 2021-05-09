---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Fonctions de mappage {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre des fonctions pour faciliter l&#39;interaction avec les cartes.

## Get

La fonction `get` est utilisée pour récupérer la valeur d&#39;un mappage pour une clé donnée.

**Format**

```sql
get({MAP},{STRING})
```

**Exemple**

La requête PQL suivante obtient la valeur de la carte d&#39;identité pour la clé `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Clés

La fonction `keys` est utilisée pour récupérer toutes les clés d&#39;un mappage donné.

**Format**

```sql
keys({MAP})
```

**Exemple**

La requête PQL suivante récupère toutes les clés de la carte `identityMap`.

```sql
keys(identityMap)
```

## Valeurs

La fonction `values` est utilisée pour récupérer toutes les valeurs d’une carte donnée.

**Format**

```sql
values({MAP})
```

**Exemple**

La requête PQL suivante récupère toutes les valeurs de la carte `identityMap`.

```sql
values(identityMap)
```
