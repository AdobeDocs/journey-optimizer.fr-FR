---
title: Bibliothèque de fonctions de mappage
description: Bibliothèque de fonctions de mappage
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '102'
ht-degree: 100%

---

# Fonctions de mappage{#maps}

Utilisez les fonctions de mappage dans la personnalisation pour faciliter l’interaction avec les mappages.

## Obtenir{#get}

La fonction `get` est utilisée pour récupérer la valeur d&#39;une carte pour une clé donnée.

**Syntaxe**

```sql
{%= get(map, string) %}
```

**Exemple**

L&#39;opération suivante renvoie la valeur de la carte d&#39;identité pour la clé `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Clés{#keys}

La fonction `keys` est utilisée pour récupérer toutes les clés d&#39;une carte donnée.

**Syntaxe**

```sql
{%= keys(map) %}
```

**Exemple**

L&#39;opération suivante renvoie toutes les clés pour la carte `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valeurs{#values}

La fonction `values` est utilisée pour récupérer toutes les valeurs d&#39;une carte donnée.

**Syntaxe**

```sql
{%= values(map) %}
```

**Exemple**

L&#39;opération suivante renvoie toutes les valeurs pour la carte `identityMap`.

```sql
{%= values(identityMap) %}
```
