---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 66%

---

# Fonctions de carte{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre des fonctions permettant de faciliter l’interaction avec les cartes.

## Get{#get}

La fonction `get` est utilisée pour récupérer la valeur d’une carte pour une clé donnée.

**Format**

```sql
{%= get(map, string) %}
```

**Exemple**

L’opération suivante récupère la valeur de la carte d’identité pour la clé `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Keys{#keys}

La fonction `keys` est utilisée pour récupérer toutes les clés d’une carte donnée.

**Format**

```sql
{%= keys(map) %}
```

**Exemple**

L’opération suivante récupère toutes les clés pour la carte `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Values{#values}

La fonction `values` est utilisée pour récupérer toutes les valeurs d’une carte donnée.

**Format**

```sql
{%= values(map) %}
```

**Exemple**

L’opération suivante récupère toutes les valeurs de la carte `identityMap`.

```sql
{%= values(identityMap) %}
```
