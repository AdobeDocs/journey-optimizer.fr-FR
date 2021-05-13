---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 89%

---

# Fonctions d&#39;objet {#objects}

![](../../assets/do-not-localize/badge.png)

## Fonction isNull

La fonction `isNull` détermine si une référence d’objet n’existe pas.

**Format**

```sql
isNull({OBJECT})
```

**Exemple**

La requête PQL suivante vérifie si l’adresse de la personne n’existe pas.

```sql
isNull(person.homeAddress)
```

## Fonction isNotNull

La fonction `isNotNull` détermine si une référence d’objet existe.

**Format**

```sql
isNotNull({OBJECT})
```

**Exemple**

La requête PQL suivante vérifie si l’adresse de la personne existe.

```sql
isNotNull(person.homeAddress)
```
