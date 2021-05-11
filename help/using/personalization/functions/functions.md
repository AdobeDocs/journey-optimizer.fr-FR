---
title: Bibliothèque des fonctions d'assistance
description: Bibliothèque des fonctions d’assistance Journey Optimizer
translation-type: tm+mt
source-git-commit: 6326dbd0efdca6f7013e5fa4b59eb0e39d302bc3
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

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
    <tr>
        <td><a href="aggregation.md#average">Moyenne</a></td><td>Cette fonction renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Dans</a></td><td>Cette fonction permet de déterminer si un élément est membre d'une baie ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a>(min)</td><td>Cette fonction renvoie la plus petite des valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a></td><td>Cette fonction renvoie le nombre d'éléments dans le tableau donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclut</a></td><td>Cette fonction détermine si un tableau ou une liste contient un élément donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a>(notIn)</td><td>Cette fonction détermine si un élément n'est pas membre d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Cette fonction récupère les valeurs d'un tableau ou d'une liste dont les valeurs de duplicata sont supprimées.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersectes</a></td><td>Cette fonction détermine si deux baies ou listes ont au moins un membre commun</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sous-ensemble de</a>(sous-ensembleDe)</td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sous-ensemble d'un autre tableau (tableau B), c'est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Premier élément</a> (en-tête)</td><td>Cette fonction renvoie le premier élément du tableau ou de la liste</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">N dernier dans le tableau</a> (lastN)</td><td>Cette fonction renvoie les derniers éléments "N" d'un tableau, lorsqu'ils sont triés par ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td>Sum</td><td></td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Premier n dans la baie</a> (topN)</td><td>Cette fonction renvoie les premiers éléments "N" d'un tableau, lorsqu'ils sont triés par ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a>(max.)</td><td>Cette fonction renvoie la plus grande de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Paramètre supérieur à</td><td>Cette fonction se termine si un tableau spécifique (tableau A) est un superset d'un autre tableau (tableau B), c'est-à-dire si ce tableau A contient tous les éléments du tableau B.</td>
    </tr>
</table>


**Fonctions de mappage**

* [Get](maps.md#get)
* [Clés](maps.md#keys)
* [Valeurs](maps.md#values)

**Fonctions d’objet**

* [N’est pas nul](objects.md#isNotNull)
* [Est nul](objects.md#isNull)

**Fonctions de chaîne**

<table>
    <tr>
        <td>Camel Case</td>
        <td>Concat</td>
        <td>[Contient](string.md#contains)</td>
    </tr>
    <tr>
        <td>[Ne contient pas](string.md#doesNotContain)</td>
        <td>[Ne se termine pas par](string.md#doesNotEndWith)</td>
        <td>[Ne début pas avec](string.md#doesNotStartWith)</td>
    </tr>
    <tr>
        <td>Encode64</td>
        <td>[Se termine par](string.md#endsWith)</td>
        <td>[Est égal à](string.md#equals)</td>
    </tr>
    <tr>
        <td>Est égal àIgnoreCase</td>
        <td>IsEmpty</td>
        <td>Length</td>
    </tr>
    <tr>
        <td>[J’aime](string.md#like)</td>
        <td>[Minuscule](string.md#lower)</td>
        <td>[Correspond](string.md#match)</td>
    </tr>
    <tr>
        <td> MD5</td>
        <td>[N’est pas égal à](string.md#notEqualTo)</td>
        <td>[Groupe d’expressions régulières](string.md#regexGroup) (regexGroup)</td>
    </tr>
    <tr>
        <td>Replace</td><td>ReplaceAll</td>
        <td>Partage</td>
        <td>[Débuts avec](string.md#démarreAvec)</td>
    </tr>
    <tr>
        <td>Cas de titre</td>
        <td>Rogner</td>
        <td>[majuscule](string.md#upper)</td>
    </tr>
</table>

### Aide{#helper-helper}

* [Chaque](../personalization-syntax.md#each)
* [if](../personalization-syntax.md#if)
* let
* [Sauf](../personalization-syntax.md#unless)
* [with](../personalization-syntax.md#with)

### Les opérateurs{#operators-helper}

Ces opérateurs ne peuvent être utilisés qu&#39;avec des nombres.

<table>
    <tr>
        <td>[Ajout](maths.md#add) (+)</td>
        <td>Cet opérateur ajoute deux nombres</td>
    </tr>
    <tr>
        <td>[And](opérateurs.md#and) (et)</td>
        <td>Cet opérateur crée une conjonction logique.</td>
    </tr>
    <tr>
        <td>[Division](maths.md#split) (/)</td>
        <td>Cet opérateur est utilisé pour trouver le quotient de deux nombres.</td>
    </tr>
    <tr>
        <td>[Est égal à](opérateurs.md#and) (=)</td>
        <td>Cette opération vérifie si les valeurs sont égales.</td>
    </tr>
    <tr>
        <td>[Supérieur à](opérateurs.md#supérieur à)</td>
        <td>Cet opérateur vérifie si la première valeur est supérieure à la seconde.</td>
    </tr>
    <tr>
        <td>[Supérieur ou égal à](opérateurs.md#plus grand nombre d’instances)</td>
        <td>Cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde.</td>
    </tr>
    <tr>
        <td>[Multiplication](maths.md#multiply) (*) </td>
        <td>Cet opérateur multiplie deux nombres</td>
    </tr>
    <tr>
        <td>[Négation](opérateurs.md#not) (!) </td>
        <td>Cet opérateur crée une négation logique.</td>
    </tr>
    <tr>
        <td>[Non égal à](opérateurs.md#notqual) (=!) </td>
        <td>Cet opérateur vérifie si une expression donnée n'est pas égale à la valeur donnée.</td>
    </tr>
    <tr>
        <td>[Or](opérateurs.md#or) (ou) </td>
        <td>Cet opérateur crée une disjonction logique.</td>
    </tr>
    <tr>
        <td>[Remainder](maths.md#reste) (%) </td>
        <td>Cet opérateur est utilisé pour calculer les restes après avoir divisé deux nombres.</td>
    </tr>
    <tr>
        <td>Plus petit que</td>
        <td>Cet opérateur vérifie si la première valeur est inférieure à la seconde.</td>
    </tr>
    <tr>
        <td>Plus petite ou égale à</td>
        <td>Cet opérateur vérifie si la première valeur est inférieure ou égale à la seconde.</td>
    </tr>
    <tr>
        <td>[Substraction](maths.md#subact) (-) </td>
        <td>Cet opérateur sous-chaîne deux nombres</td>
    </tr>
</table>
