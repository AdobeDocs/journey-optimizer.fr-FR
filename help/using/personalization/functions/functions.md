---
title: Bibliothèque des fonctions d'assistance
description: Bibliothèque des fonctions d’assistance Journey Optimizer
translation-type: tm+mt
source-git-commit: 1220db4c2210338ca4fb8b4df9d1d96288f0e72d
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 7%

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

Ils sont regroupés en trois catégories : [Fonctions](#functions-helper), [Assistants](#helper-helper) et [Opérateurs](#operators-helper).

### Fonctions{#functions-helper}

**Fonctions de tableau**

<table>
    <tr><td>[Average](agrégation.md#average)</td><td>[In](array-liste.md#in)</td><td>[Minimum](agrégation.md#minimum) (min)</td></tr>
    <tr><td>[Count](agrégation.md#count)</td><td>[Inclut](array-liste.md#inclut)</td><td>[Not in](array-liste.md#notin) (notIn)</td></tr>
    <tr><td>[Distinct](array-liste.md#distinct)</td><td>[Intersects](array-liste.md#intersects)</td><td>[Sous-ensemble de](array-liste.md#subset)</td></tr>
    <tr><td>[Premier élément](array-liste.md#head) (head)</td><td>[N dernier dans le tableau](array-liste.md#last-n) (lastN)</td><td>Sum</td></tr>
    <tr><td>[Premier n dans la baie](array-liste.md#first-n) (topN)</td><td>[Maximum](agrégation.md#maximum) (max.)</td><td>[Paramètre supérieur de](array-liste.md#superset)</td></tr>
</table>

* [Moyenne](aggregation.md#average)
* [Count](aggregation.md#count)
* [Distinct](arrays-list.md#distinct)
* [Premier élément](arrays-list.md#head)  (en-tête)
* [Premier n dans la baie](arrays-list.md#first-n)  (topN)
* [Dans](arrays-list.md#in)
* [Inclut](arrays-list.md#includes)
* [Intersectes](arrays-list.md#intersects)
* [N dernier dans le tableau](arrays-list.md#last-n)  (lastN)
* [Maximum](aggregation.md#maximum) (max.)
* [Minimum](aggregation.md#minimum) (min)
* [Not in](arrays-list.md#notin) (notIn)
* [Sous-ensemble de](arrays-list.md#subset)
* Somme
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

### Aide{#helper-helper}

* [Chaque](../personalization-syntax.md#each)
* [if](../personalization-syntax.md#if)
* let
* [Sauf](../personalization-syntax.md#unless)
* [with](../personalization-syntax.md#with)

### Les opérateurs{#operators-helper}

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

```sql
{%=lowerCase(string)%}
```

Exemple :

Cette fonction convertit le prénom du profil en lettres minuscules.

```sql
{%=lowerCase(profile.person.name.firstName)%}
```

### majuscule{#upper}

La fonction **upper** convertit une chaîne en lettres minuscules.

Syntaxe :

```sql
{%=upperCase(string)%}
```

Exemple :

Cette fonction convertit le nom de profil en majuscules.

```sql
{%=upperCase(profile.person.name.lastName)%}
```
