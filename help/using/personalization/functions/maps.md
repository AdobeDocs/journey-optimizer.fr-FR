---
title: Bibliothèque de fonctions de mappage
description: Bibliothèque de fonctions de mappage
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Fonctions de mappage{#maps}

Utilisez les fonctions de carte dans la personnalisation pour faciliter l’interaction avec les cartes.

## Get{#get}

Le `get` est utilisée pour récupérer la valeur d’une carte pour une clé donnée.

**Format**

```sql
{%= get(map, string) %}
```

**Exemple**

L’opération suivante récupère la valeur de la carte d’identité pour la clé `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Clés{#keys}

Le `keys` est utilisée pour récupérer toutes les clés d’une carte donnée.

**Format**

```sql
{%= keys(map) %}
```

**Exemple**

L’opération suivante récupère toutes les clés de la carte. `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valeurs{#values}

Le `values` est utilisée pour récupérer toutes les valeurs d’une carte donnée.

**Format**

```sql
{%= values(map) %}
```

**Exemple**

L’opération suivante récupère toutes les valeurs de la carte. `identityMap`.

```sql
{%= values(identityMap) %}
```
