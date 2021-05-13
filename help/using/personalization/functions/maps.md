---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 85%

---

# Fonctions de mappage {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre des fonctions pour faciliter l&#39;interaction avec les cartes.

## Get

La fonction `get` est utilisée pour récupérer la valeur d’une carte pour une clé donnée.

**Format**

```sql
get({MAP},{STRING})
```

**Exemple**

La requête PQL suivante renvoie la valeur de la carte d’identité pour la clé `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Keys

La fonction `keys` est utilisée pour récupérer toutes les clés d’une carte donnée.

**Format**

```sql
keys({MAP})
```

**Exemple**

La requête PQL suivante renvoie toutes les clés pour la carte `identityMap`.

```sql
keys(identityMap)
```

## Values

La fonction `values` est utilisée pour récupérer toutes les valeurs d’une carte donnée.

**Format**

```sql
values({MAP})
```

**Exemple**

La requête PQL suivante renvoie toutes les valeurs pour la carte `identityMap`.

```sql
values(identityMap)
```
