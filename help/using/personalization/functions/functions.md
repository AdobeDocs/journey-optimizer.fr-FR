---
title: Bibliothèque des fonctions d'assistance
description: Bibliothèque des fonctions d’assistance Journey Optimizer
translation-type: tm+mt
source-git-commit: 3fa63e103c2185062ff779c35d19387aea523f62
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---


# Langage de modèle et fonctions d&#39;assistance {#functionsL}

![](../../assets/do-not-localize/badge.png)


## A propos du modèle de langue

Utilisez le langage de modèle Journey Optimizer pour effectuer des opérations sur les données, telles que des calculs, le formatage ou les conversions de données, les conditions et les manipuler dans le contexte de la personnalisation.

La langue de modèle est exploitée dans les fonctions d’aide disponibles dans la liste déroulante Personnalisation de l’éditeur d’expressions.

![](../assets/access-helper-functions.png)

Ils sont regroupés en trois catégories : [Fonctions](#functions-helper), [Assistants](#helper-helper) et [Opérateurs](#operators-helper).

### Fonctions{#functions-helper}

**Fonctions de tableau**

<table>
    <tr>
        <td><a href="aggregation.md#average">Moyenne</a>  (moyenne)</td><td>Cette fonction renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a> (in)</td><td>Cette fonction permet de déterminer si un élément est membre d'une baie ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a> (min)</td><td>Cette fonction renvoie la plus petite des valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a> (count)</td><td>Cette fonction renvoie le nombre d'éléments dans le tableau donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclut</a>  (inclut)</td><td>Cette fonction détermine si un tableau ou une liste contient un élément donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a> (notIn)</td><td>Cette fonction détermine si un élément n'est pas membre d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a>  (distinct)</td><td>Cette fonction récupère les valeurs d'un tableau ou d'une liste dont les valeurs de duplicata sont supprimées.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a>  (intersectes)</td><td>Cette fonction détermine si deux baies ou listes ont au moins un membre commun</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sous-ensemble de</a> (sous-ensembleDe)</td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sous-ensemble d'un autre tableau (tableau B), c'est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Premier élément</a>  (en-tête)</td><td>Cette fonction renvoie le premier élément du tableau ou de la liste</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">N dernier dans le tableau</a>  (lastN)</td><td>Cette fonction renvoie les derniers éléments "N" d'un tableau, lorsqu'ils sont triés par ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td>Sum</td><td></td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Premier n dans la baie</a>  (topN)</td><td>Cette fonction renvoie les premiers éléments "N" d'un tableau, lorsqu'ils sont triés par ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a> (max.)</td><td>Cette fonction renvoie la plus grande de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a> (supersetOf)</td><td>Cette fonction se termine si un tableau spécifique (tableau A) est un superset d'un autre tableau (tableau B), c'est-à-dire si ce tableau A contient tous les éléments du tableau B.</td>
    </tr>
</table>


**Fonctions de mappage**

<table>
    <tr>
        <td><a href="maps.md#get">Get</a> (get)</td><td>Cette fonction est utilisée pour récupérer la valeur d'un mappage pour une clé donnée.</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Touches</a>  (clés)</td><td>Cette fonction est utilisée pour récupérer toutes les clés d'un mappage donné.</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valeurs</a>  (valeurs)</td><td>Cette fonction récupère toutes les valeurs d’un mappage donné.</td>
    </tr>
</table>

**Fonctions d’objet**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">N’est pas nul</a>  (isNotNull)</td><td>Cette fonction permet de déterminer s’il existe une référence d’objet.</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Est nul</a>  (isNull)</td><td>Cette fonction permet de déterminer si une référence d'objet n'existe pas.</td>
    </tr>
</table>

**Fonctions de chaîne**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Camel Case</a>  (chamelCase)</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Concat</a>  (Concat)</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contient</a>  (contient)</td><td>Cette fonction est utilisée pour déterminer si une chaîne contient une sous-chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Ne contient</a>  pas (ne contient pas)</td><td>Cette fonction est utilisée pour déterminer si une chaîne ne contient pas de sous-chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Ne se termine pas par</a>  (nePasTerminerAvec)</td><td>Cette fonction est utilisée pour déterminer si une chaîne ne se termine pas par une sous-chaîne spécifiée.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">N'est pas début avec</a>  (nePasDémarrerAvec)</td><td>Cette fonction est utilisée pour déterminer si une chaîne ne se début pas avec une sous-chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Encode64</a> ()</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Se termine par</a>  (se termine par)</td><td>Cette fonction est utilisée pour déterminer si une chaîne se termine par une sous-chaîne spécifiée.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Est égal</a> (=)</td><td>Cette fonction est utilisée pour déterminer si une chaîne ne se début pas avec une sous-chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">EqualsIgnoreCase</a> ()</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">IsEmpty</a> ()</td><td>Cette fonction est utilisée pour </td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Length</a> ()</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="string.md#like">J’aime</a>  (j’aime)</td><td>Cette fonction permet de déterminer si une chaîne correspond à un modèle spécifié.</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minuscule</a>  (minuscule)</td><td>Cette fonction convertit une chaîne en lettres minuscules</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#matches">Correspond</a> (correspond)</td><td>Cette fonction permet de déterminer si une chaîne correspond à une expression régulière spécifique.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">MD5</a> ()</td><td>Cette fonction est utilisée pour </td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">N’est pas égal à</a>  (notEqualsTo)</td><td>Cette fonction est utilisée pour déterminer si une chaîne n'est pas égale à la chaîne spécifiée.</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Groupe</a>  d’expressions régulières (regexGroup)</td><td>Cette fonction est utilisée pour extraire des informations spécifiques, en fonction de l'expression régulière fournie.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Replace</a> (replace)</td><td>Cette fonction est utilisée pour </td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Remplacer tout</a>  (replaceAll)</td><td>Cette fonction est utilisée pour</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Fractionner</a>  (fractionner)</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Débuts avec</a>  (commence par)</td><td>Cette fonction est utilisée pour déterminer si une chaîne est début avec une sous-chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Case</a>  de titre (titleCase)</td><td>Cette fonction est utilisée pour</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Rognage</a>  (rognage)</td><td>Cette fonction est utilisée pour</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Majuscule</a>  (majuscule)</td><td>Cette fonction convertit une chaîne en majuscules</td>
    </tr>
</table>

### Aide{#helper-helper}

* Chacun - [En savoir plus](../personalization-syntax.md#each)
* Si - [En savoir plus](../personalization-syntax.md#if)
* Laisser - En savoir plus
* Sauf si - [En savoir plus](../personalization-syntax.md#unless)
* Avec - [En savoir plus](../personalization-syntax.md#with)

### Les opérateurs{#operators-helper}

Ces opérateurs ne peuvent être utilisés qu&#39;avec des nombres.

<table>
    <tr>
        <td><a href="operators.md#add">Addition</a> ('+')</td><td>Cet opérateur ajoute deux nombres</td>
    </tr>
    <tr>
        <td><a href="operators.md#and">Et</a>  (et)</td><td>Cet opérateur crée une conjonction logique.</td>
    <tr>
        <td><a href="operators.md#divide">Diviser</a> (/)</td><td>Cet opérateur est utilisé pour trouver le quotient de deux nombres.</td>
    </tr>
    <tr>
        <td><a href="operators.md#and">Est égal à</a> (=)</td><td>Cette opération vérifie si les valeurs sont égales.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Supérieur à</a> ()</td><td>Cet opérateur vérifie si la première valeur est supérieure à la seconde.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Supérieur ou égal à</a>  (=&gt;)</td><td>Cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde.</td>
    </tr>
    <tr>
        <td><a href="operators.md#multiply">Multiplication</a> (*)</td><td>Cet opérateur multiplie deux nombres</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Négation</a> (!)</td><td>Cet opérateur crée une négation logique.</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">N’est pas égal à</a>  (=!)</td><td>Cet opérateur vérifie si une expression donnée n'est pas égale à la valeur donnée.</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Ou</a> (ou)</td><td>Cet opérateur crée une disjonction logique.</td>
    </tr>
    <tr>
        <td><a href="operators.md#remainder">Remainder</a> (%)</td><td>Cet opérateur est utilisé pour calculer les restes après avoir divisé deux nombres.</td>
    </tr>
    <tr>
        <td><a href="operators.md#remainder">Plus petit que</a> ()</td><td>Cet opérateur vérifie si la première valeur est inférieure à la seconde.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Plus petit ou égal à</a> ()</td><td>Cet opérateur vérifie si la première valeur est inférieure ou égale à la seconde.</td>
    </tr>
    <tr>
        <td><a href="operators.md#substract">Substraction</a> ()</td><td>Cet opérateur sous-chaîne deux nombres</td>
    </tr>
</table>
