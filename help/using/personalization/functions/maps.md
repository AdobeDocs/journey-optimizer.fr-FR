---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 6%

---

# Fonctions de mappage{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre des fonctions pour faciliter l&#39;interaction avec les cartes.

## Get{#get}

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

## Clés{#keys}

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

## Valeurs {#values}

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
