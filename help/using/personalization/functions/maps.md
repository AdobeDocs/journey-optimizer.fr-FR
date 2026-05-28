---
title: Bibliothèque de fonctions de mappage
description: Bibliothèque de fonctions de mappage
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
TQID: https://experienceleague.adobe.com/KeitEe0NQxxc-snCyWSGlov-OyUgiva6ddzrCTxEKSs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 102
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
