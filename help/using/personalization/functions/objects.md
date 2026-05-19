---
title: Bibliothèque de fonctions d'objets
description: Bibliothèque de fonctions d'objets
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
TQID: https://experienceleague.adobe.com/EdvzBXdtv1Mm4yIZ8ehu4tx6uQBxnpcXTMVQIc1oQkI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 100%

---

# Fonctions d&#39;objet {#objects}

## Est nul{#isNull}

La fonction `isNull` détermine si une référence d&#39;objet n&#39;existe pas.

**Syntaxe**

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

**Syntaxe**

```sql
{%= isNotNull(object) %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;adresse de la personne existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
