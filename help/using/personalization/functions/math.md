---
title: Bibliothèque de fonctions mathématiques
description: Bibliothèque de fonctions mathématiques
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: ht
source-wordcount: '215'
ht-degree: 100%

---

# Fonctions mathématiques {#math}

Découvrez comment utiliser les fonctions mathématiques dans l’éditeur d’expression.

## Absolu {#absolute}

La fonction `absolute` est utilisée pour convertir un nombre dont la valeur est absolue.

**Syntaxe**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

La fonction `formatNumber` sert à mettre en forme n’importe quel nombre dans sa représentation sensible à la langue.

Elle accepte un nombre et une chaîne représentant le paramètre régional et renvoie une chaîne formatée du nombre dans le paramètre régional souhaité.

**Syntaxe**

```sql
{%= formatNumber(number/double,string) %}: string
```

Vous pouvez utiliser la mise en forme et des paramètres régionaux valides comme indiqué dans la [Documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) et les [Paramètres régionaux pris en charge](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

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

La fonction `Count only null` sert à arrondir un nombre à l’unité supérieure.

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
