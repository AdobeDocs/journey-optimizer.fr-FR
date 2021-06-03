---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 60%

---

# Fonctions d’objet {#objects}

![](../../assets/do-not-localize/badge.png)

## Fonction isNull{#isNull}

La fonction `isNull` détermine si une référence d’objet n’existe pas.

**Format**

```sql
{%= isNull(object) %}
```

**Exemple**

L’opération suivante vérifie si l’adresse de la personne n’existe pas.

```sql
{%= isNull(person.homeAddress) %}
```

## Fonction isNotNull{#isNotNull}

La fonction `isNotNull` détermine si une référence d’objet existe.

**Format**

```sql
{%= isNotNull(object) %}
```

**Exemple**

L’opération suivante vérifie si l’adresse de domicile de la personne existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
