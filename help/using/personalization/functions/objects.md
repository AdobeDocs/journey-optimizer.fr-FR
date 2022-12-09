---
title: Bibliothèque de fonctions d’objets
description: Bibliothèque de fonctions d’objets
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Fonctions d’objet {#objects}

## Is null{#isNull}

Le `isNull` détermine si une référence d’objet n’existe pas.

**Format**

```sql
{%= isNull(object) %}
```

**Exemple**

L’opération suivante vérifie si l’adresse de la personne n’existe pas.

```sql
{%= isNull(person.homeAddress) %}
```

## N’est pas nul{#isNotNull}

Le `isNotNull` détermine si une référence d’objet existe.

**Format**

```sql
{%= isNotNull(object) %}
```

**Exemple**

L’opération suivante vérifie si l’adresse de domicile de la personne existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
