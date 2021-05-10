---
title: Bibliothèque des fonctions d'assistance
description: Bibliothèque des fonctions d’assistance Journey Optimizer
translation-type: tm+mt
source-git-commit: a7b1c24b1a5a07807050237d3e89c51ced28c749
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 8%

---


# Langage de modèle et fonctions d&#39;assistance {#functionsL}

![](../../assets/do-not-localize/badge.png)


## A propos du modèle de langue

Utilisez le langage de modèle Journey Optimizer pour effectuer des opérations sur les données, telles que des calculs, le formatage ou les conversions de données, les conditions et les manipuler dans le contexte de la personnalisation.

Les fonctions disponibles sont répertoriées dans les pages suivantes :

* [Opérateurs](operators.md)
* [Agrégation](aggregation.md)
* [Tableaux et liste](arrays-list.md)
* [Mathématique](maths.md)
* [Mappages](maps.md)
* [Objets](objects.md)
* [Chaîne](string.md)

La langue de modèle est exploitée dans les fonctions d’aide disponibles dans la liste déroulante Personnalisation de l’éditeur d’expressions.

![](../assets/access-helper-functions.png)

Ils sont regroupés en trois catégories : Fonctions, assistants et opérateurs

### Fonctions

**Fonctions de tableau**

* [Moyenne](aggregation.md#average)
* [Count](aggregation.md#count)
* [Distinct](arrays-list.md#distinct)
* [Premier élément](arrays-list.md#head)  (en-tête)
* [Premier n dans la baie](arrays-list.md#first-n)  (topN)
* [Dans](arrays-list.md#in)
* [Inclut](arrays-list.md#includes)
* [Intersectes](arrays-list.md#intersects)
* [N dernier dans le tableau](arrays-list.md#last-n)  (lastN)
* [Maximum](aggregation.md#maximum)
* [Minimum](aggregation.md#minimum)
* [Pas dans](arrays-list.md#notin)
* [Sous-ensemble de](arrays-list.md#subset)
* Sum
* [Paramètre supérieur à](arrays-list.md#superset)

**Fonctions de mappage**

* [Get](maps.md#get)
* [Clés](maps.md#keys)
* [Valeurs](maps.md#values)

**Fonctions d’objet**

* [N’est pas nul](objects.md#isNotNull)
* [Est nul](objects.md#isNull)

**Fonctions de chaîne**

* Camel Case
* Concat
* [Contient](string.md#contains)
* [Ne contient pas](string.md#doesNotContain)
* [Ne se termine pas par](string.md#doesNotEndWith)
* [Ne commence pas par](string.md#doesNotStartWith)
* Encode64
* [Se termine par](string.md#endsWith)
* [Est égal à](string.md#equals)
* Est égal àIgnoreCase
* IsEmpty
* Length
* [Comme](string.md#like)
* [Minuscule](#lower)
* [Correspond à](string.md#matches)
* MD5
* [Différent de](string.md#notEqualTo)
* [Groupe](string.md#regexGroup)  d’expressions régulières (regexGroup)
* Replace
* ReplaceAll
* Partage
* [Commence par](string.md#startsWith)
* Cas de titre
* Rogner
* [majuscule](#upper)

### Assistance

* [Chaque](../personalization-syntax.md#each)
* [if](../personalization-syntax.md#if)
* let
* [Sauf](../personalization-syntax.md#unless)
* [with](../personalization-syntax.md#with)

### Les opérateurs

Ces opérateurs ne peuvent être utilisés qu&#39;avec des nombres.

* [Ajout](maths.md#add) (+) - Cet opérateur ajoute deux nombres
* [Et](operators.md#and) (et) - Cet opérateur crée une conjonction logique
* [Division](maths.md#divide) (/) - Cet opérateur est utilisé pour trouver le quotient de deux nombres.
* [Est égal à](operators.md#and) (=) - Cette opération vérifie si les valeurs sont égales.
* [Supérieur à](operators.md#greaterthan) (>) : cet opérateur vérifie si la première valeur est supérieure à la seconde.
* [Supérieur ou égal à](operators.md#greaterthanorequal) (>=) : cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde.
* [Multiplication](maths.md#multiply)  (*) : cet opérateur multiplie deux nombres
* [Négation](operators.md#not) (!) - Cet opérateur crée une négation logique
* [N’est pas égal à](operators.md#notequal)  (=!) - Cet opérateur vérifie si l&#39;expression donnée n&#39;est pas égale à la valeur donnée
* [Or](operators.md#or) (or) : cet opérateur crée une disjonction logique.
* [Remainder](maths.md#remainder) (%) - Cet opérateur est utilisé pour calculer les restes après avoir divisé deux nombres.
* Plus petit que (&lt;) : cet opérateur vérifie si la première valeur est inférieure à la seconde.
* Plus petit ou égal à (&lt;=) : cet opérateur vérifie si la première valeur est inférieure ou égale à la seconde.
* [Substraction](maths.md#substract) (-) - Cet opérateur sous-chaîne deux nombres

## Fonctions

### Minuscule{#lower}

La fonction **lowerCase** convertit une chaîne en lettres minuscules.

Syntaxe :

```
{%=lowerCase(string)%}
```

Exemple :

Cette fonction convertit le prénom du profil en lettres minuscules.

```
{%=lowerCase(profile.person.name.firstName)%}
```

### majuscule{#upper}

La fonction **upper** convertit une chaîne en lettres minuscules.

Syntaxe :

```
{%=upperCase(string)%}
```

Exemple :

Cette fonction convertit le nom de profil en majuscules.

```
{%=upperCase(profile.person.name.lastName)%}
```
