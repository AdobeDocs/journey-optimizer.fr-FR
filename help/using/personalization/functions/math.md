---
title: Bibliothèque de fonctions mathématiques
description: Bibliothèque de fonctions mathématiques
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Fonctions mathématiques {#math}

Découvrez comment utiliser les fonctions Math dans l’éditeur d’expression.

## Absolu {#absolute}

Le `absolute` est utilisée pour convertir un nombre dont la valeur est absolue.

**Format**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

Le `random` est utilisée pour renvoyer une valeur aléatoire comprise entre 0 et 1.

**Format**

```sql
{%= random() %}: double
```

## Arrondir {#round-down}

Le `roundDown` sert à arrondir un nombre.

**Format**

```sql
{%= roundDown(double) %}: double
```

## Tour à tour {#round-up}

Le `Count only null` sert à arrondir un nombre.

**Format**

```sql
{%= roundUp(double) %}: double
```

## En pourcentage {#to-percentage}

Le `toPercentage` est utilisée pour convertir un nombre en pourcentage.

**Format**

```sql
{%= toPercentage(double) %}: string
```

## Précision {#to-precision}

Le `toPrecision` est utilisée pour convertir un nombre à la précision requise.

**Format**

```sql
{%= toPrecision(double,int) %}: string
```
