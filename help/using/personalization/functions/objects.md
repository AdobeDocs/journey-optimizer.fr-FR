---
title: Bibliothèque de fonctions d'objets
description: Bibliothèque de fonctions d'objets
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: ht
source-wordcount: '59'
ht-degree: 100%

---

# Fonctions d&#39;objet {#objects}

## isNull{#isNull}

La fonction `isNull` détermine si une référence d&#39;objet n&#39;existe pas.

**Format**

```sql
{%= isNull(object) %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;adresse de la personne n&#39;existe pas.

```sql
{%= isNull(person.homeAddress) %}
```

## Fonction isNotNull{#isNotNull}

La fonction `isNotNull` détermine si une référence d&#39;objet existe.

**Format**

```sql
{%= isNotNull(object) %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;adresse de la personne existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
