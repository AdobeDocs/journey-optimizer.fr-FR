---
title: Bibliothèque de fonctions de mappage
description: Bibliothèque de fonctions de mappage
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 51%

---

# Fonctions de carte{#maps}

Utilisez les fonctions de carte dans la personnalisation pour faciliter l’interaction avec les cartes.

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
