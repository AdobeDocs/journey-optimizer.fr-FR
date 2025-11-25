---
title: Bibliothèque de fonctions mathématiques
description: Bibliothèque de fonctions mathématiques
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '244'
ht-degree: 100%

---

# Fonctions mathématiques {#math}

Découvrez comment utiliser des fonctions mathématiques dans l’éditeur de personnalisation.

## Absolu {#absolute}

La fonction `absolute` est utilisée pour convertir un nombre vers sa valeur absolue.

**Syntaxe**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

La fonction `formatNumber` sert à mettre en forme n’importe quel nombre dans sa représentation sensible à la langue.

Elle accepte un nombre et une chaîne représentant les paramètres régionaux et renvoie une chaîne formatée du nombre dans les paramètres régionaux souhaités.

**Syntaxe**

```sql
{%= formatNumber(number/double,string) %}: string
```

Vous pouvez utiliser la mise en forme et les paramètres régionaux valides comme spécifié dans la [Documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) et les [Paramètres régionaux pris en charge](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}.

**Exemple**

Cette requête renvoie une chaîne formatée en arabe correspondant à 123456,789 comme numéro d’entrée.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Aléatoire {#random}

La fonction `random` est utilisée pour renvoyer une valeur aléatoire comprise entre 0 et 1.

**Syntaxe**

```sql
{%= random() %}: double
```

## Arrondir à l’unité inférieure {#round-down}

La fonction `roundDown` sert à arrondir un nombre à l’unité inférieure.

**Syntaxe**

```sql
{%= roundDown(double) %}: double
```

## Arrondir à l’unité supérieure {#round-up}

La fonction `roundUp` sert à arrondir un nombre à l’unité supérieure.

**Syntaxe**

```sql
{%= roundUp(double) %}: double
```

## To hex string {#to-hex-string}

La fonction `toHexString` convertit n’importe quel nombre en sa chaîne hexadécimale.

**Syntaxe**

```sql
{%= toHexString(number) %}: string
```

**Exemple**

Cette requête renvoie la valeur hexadécimale de 158, soit 9e.

```sql
{%= toHexString(158) %}
```

## To Int {#to-int}

La fonction `toInt` est utilisée pour convertir n’importe lequel de ces types (nombre, double, entier, long, flottant, court, octet, booléen, chaîne) en entier.

**Syntaxe**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Exemple**

Cette requête renvoie la valeur d’entier de 42,6, soit 42.

```sql
{%= toInt(42.6) %}: integer
```

## En pourcentage {#to-percentage}

La fonction `toPercentage` est utilisée pour convertir un nombre en pourcentage.

**Syntaxe**

```sql
{%= toPercentage(double) %}: string
```

## En précision {#to-precision}

La fonction `toPrecision` est utilisée pour convertir un nombre à la précision requise.

**Syntaxe**

```sql
{%= toPrecision(double,int) %}: string
```

## To string {#to-string}

La fonction **toString** convertit n’importe quel nombre en sa représentation sous forme de chaîne.

**Syntaxe**

```sql
{%= toString(string) %}: string
```

**Exemple**

Cette requête renvoie « 12 ».

```sql
{%= toString(12) %} 
```
