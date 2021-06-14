---
title: Bibliothèque de fonctions d’objets
description: Bibliothèque de fonctions d’objets
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 52%

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
