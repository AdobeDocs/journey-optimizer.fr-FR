---
title: Bibliothèque de fonctions d’objets
description: Bibliothèque de fonctions d’objets
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 52%

---

# Fonctions d’objet {#objects}

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
