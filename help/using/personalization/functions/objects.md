---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Fonctions d&#39;objet {#objects}

![](../../assets/do-not-localize/badge.png)

## Est nul{#isNull}

La fonction `isNull` détermine si une référence d&#39;objet n&#39;existe pas.

**Format**

```sql
isNull({OBJECT})
```

**Exemple**

La requête PQL suivante vérifie si l’adresse de domicile de la personne n’existe pas.

```sql
isNull(person.homeAddress)
```

## N’est pas nul{#isNotNull}

La fonction `isNotNull` détermine si une référence d&#39;objet existe.

**Format**

```sql
isNotNull({OBJECT})
```

**Exemple**

La requête PQL suivante vérifie si l&#39;adresse de domicile de la personne existe.

```sql
isNotNull(person.homeAddress)
```
