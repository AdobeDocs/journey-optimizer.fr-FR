---
title: Bibliothèque de fonctions d'objets
description: Bibliothèque de fonctions d'objets
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: ht
source-wordcount: '57'
ht-degree: 100%

---

# Fonctions d&#39;objet {#objects}

## Est nul{#isNull}

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

## N’est pas nul{#isNotNull}

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
