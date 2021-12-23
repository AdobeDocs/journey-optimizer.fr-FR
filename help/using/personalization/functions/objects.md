---
title: Bibliothèque de fonctions d'objets
description: Bibliothèque de fonctions d'objets
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: ht
source-wordcount: '57'
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
