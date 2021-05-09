---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Fonctions d&#39;objet {#objects}

![](../../assets/do-not-localize/badge.png)

## Est nul

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

## N’est pas nul

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
