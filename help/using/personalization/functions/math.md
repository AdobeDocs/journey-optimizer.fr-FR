---
title: Bibliothèque de fonctions mathématiques
description: Bibliothèque de fonctions mathématiques
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 100%

---

# Fonctions mathématiques {#math}

Découvrez comment utiliser les fonctions mathématiques dans l’éditeur d’expression.

## Absolu {#absolute}

La fonction `absolute` est utilisée pour convertir un nombre dont la valeur est absolue.

**Format**

```sql
{%= absolute(int) %}: int
```

## Aléatoire {#random}

La fonction `random` est utilisée pour renvoyer une valeur aléatoire comprise entre 0 et 1.

**Format**

```sql
{%= random() %}: double
```

## Arrondir à l’unité inférieure {#round-down}

La fonction `roundDown` sert à arrondir un nombre à l’unité inférieure.

**Format**

```sql
{%= roundDown(double) %}: double
```

## Arrondir à l’unité supérieure {#round-up}

La fonction `Count only null` sert à arrondir un nombre à l’unité supérieure.

**Format**

```sql
{%= roundUp(double) %}: double
```

## En pourcentage {#to-percentage}

La fonction `toPercentage` est utilisée pour convertir un nombre en pourcentage.

**Format**

```sql
{%= toPercentage(double) %}: string
```

## En précision {#to-precision}

La fonction `toPrecision` est utilisée pour convertir un nombre à la précision requise.

**Format**

```sql
{%= toPrecision(double,int) %}: string
```
