---
title: Bibliothèque des fonctions d’assistance
description: Bibliothèque de fonctions d’assistance Journey Optimizer
feature: Personnalisation
topic: Personnalisation
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 7%

---


# Langage de modèle et fonctions d’assistance {#functionsL}

![](../../assets/do-not-localize/badge.png)

Utilisez le [!DNL Journey Optimizer] langage de modèle pour effectuer des opérations sur les données, telles que des calculs, le formatage ou les conversions des données, les conditions et les manipuler dans le contexte de la personnalisation. Découvrez les directives de syntaxe de personnalisation dans [cette page](../personalization-syntax.md).

Le langage de modèle est utilisé dans les fonctions d’assistance disponibles dans la liste déroulante de personnalisation de l’éditeur d’expression, comme ci-dessous :

![](../assets/access-helper-functions.png)

Dans l’ [!DNL Journey Optimizer] éditeur d’expression, les fonctions d’assistance sont regroupées en trois catégories : [Fonctions](#functions-helper), [assistants](#helper-helper) et [Opérateurs](#operators-helper).

## Fonctions{#functions-helper}

**Fonctions de tableau**

<table>
    <tr>
        <td><a href="aggregation.md#average">moyen</a></td><td>Cette fonction renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>Cette fonction permet de déterminer si un élément est membre d’un tableau ou d’une liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Cette fonction renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau .</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a></td><td>Cette fonction renvoie le nombre d’éléments dans le tableau donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Includes</a></td><td>Cette fonction détermine si un tableau ou une liste contient un élément donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a></td><td>Cette fonction détermine si un élément n’est pas membre d’un tableau ou d’une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Cette fonction récupère les valeurs d’un tableau ou d’une liste dont les valeurs en double sont supprimées.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a></td><td>Cette fonction détermine si deux tableaux ou deux listes ont au moins un membre commun</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset of</a></td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sous-ensemble d’un autre tableau (tableau B), c’est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">First item</a></td><td>Cette fonction renvoie le premier élément d’un tableau ou d’une liste</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">N dernier dans le tableau</a></td><td>Cette fonction renvoie les derniers éléments "N" d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction de l’expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Cette fonction renvoie la somme de toutes les valeurs sélectionnées dans le tableau .</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">First n in array</a></td><td>Cette fonction renvoie les premiers éléments "N" d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction de l’expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Cette fonction renvoie la plus grande de toutes les valeurs sélectionnées dans un tableau.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a></td><td>Cette fonction se termine si un tableau spécifique (tableau A) est un sur-ensemble d’un autre tableau (tableau B), c’est-à-dire si ce tableau A contient tous les éléments du tableau B.</td>
    </tr>
</table>


**Fonctions de mappage**

<table>
    <tr>
        <td><a href="maps.md#get">Get</a></td><td>Cette fonction est utilisée pour récupérer la valeur d’une carte pour une clé donnée.</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Keys</a></td><td>Cette fonction est utilisée pour récupérer toutes les clés d’une carte donnée.</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Values</a></td><td>Cette fonction récupère toutes les valeurs d’une carte donnée.</td>
    </tr>
</table>

**Fonctions d’objet**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Fonction isNotNull</a></td><td>Cette fonction permet de déterminer s’il existe une référence d’objet.</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Fonction isNull</a></td><td>Cette fonction permet de déterminer si une référence d’objet n’existe pas.</td>
    </tr>
</table>

**Fonctions de chaîne**

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Cette fonction permet de mettre en majuscules la première lettre de chaque mot d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Cette fonction permet de combiner deux chaînes en une seule.</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>Cette fonction permet de déterminer si une chaîne contient une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Does not contain</a></td><td>Cette fonction permet de déterminer si une chaîne ne contient pas de sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Does not end with</a></td><td>Cette fonction permet de déterminer si une chaîne ne se termine pas par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Does not start with</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Encode 64</a></td><td>Cette fonction est utilisée pour coder ou décoder une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Ends with</a></td><td>Cette fonction permet de déterminer si une chaîne se termine par une sous-chaîne donnée.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Equals</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée, en respectant la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Est égal à Ignorer la casse</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée, sans respect de la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extract Email Domain</a></td><td>Cette fonction est utilisée pour extraire le domaine d’une adresse électronique.</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Cette fonction permet de vérifier si une chaîne ou une expression est vide.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Rognage gauche</a></td><td>Cette fonction supprime les espaces blancs au début d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Cette fonction est utilisée pour obtenir le nombre de caractères d’une chaîne ou d’une expression.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Like</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à un modèle spécifié.</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minuscule</a></td><td>Cette fonction convertit une chaîne en minuscules</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Matches</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à une expression régulière spécifique.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">N’est pas égal à</a></td><td>Cette fonction permet de déterminer si une chaîne n’est pas égale à la chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Regular expression group</a></td><td>Cette fonction est utilisée pour extraire des informations spécifiques, en fonction de l’expression régulière fournie.</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Remplacer</a></td><td>Cette fonction remplace une sous-chaîne donnée dans une chaîne par une autre sous-chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Remplacer tout</a></td><td>Cette fonction remplace toutes les sous-chaînes d’un texte correspondant à "target" par la chaîne littérale "remplacement" spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Rognage droit</a></td><td>Cette fonction supprime les espaces blancs de la fin d’une chaîne. </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a></td><td>Cette fonction est utilisée pour fractionner une chaîne selon un caractère donné.</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Starts with</a></td><td>Cette fonction permet de déterminer si une chaîne commence par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Cas de titre</a></td><td>Cette fonction permet de mettre en majuscules les premières lettres de chaque mot d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Rogner</a></td><td>Cette fonction supprime les espaces blancs du début et de la fin d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">majuscule</a></td><td>Cette fonction convertit une chaîne en majuscules</td>
    </tr>
</table>


## Assistants{#helper-helper}

Les assistants sont détaillés dans [cette page](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>Cette fonction est utilisée pour effectuer une itération sur un tableau</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">If</a></td><td>Cette fonction est utilisée pour définir un bloc conditionnel. Si l’évaluation de l’expression renvoie true (vrai), le bloc est rendu.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Cette fonction permet à une expression d’être stockée en tant que variable et d’être utilisée ultérieurement dans une requête.</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>Cette fonction est utilisée pour définir un bloc conditionnel. Si l’évaluation de l’expression renvoie false, le bloc est rendu.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Avec</a></td><td>Cette fonction est utilisée pour modifier le jeton d’évaluation de template-part.</td>
    </tr>
</table>

## Opérateurs{#operators-helper}

### Fonctions arithmétiques {#arithmetic-helper}

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur les valeurs.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Ajout</a></td><td>Cet opérateur est utilisé pour trouver la somme de deux expressions d’argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Division</a></td><td>Cet opérateur est utilisé pour trouver le quotient de deux expressions d’argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplication</a></td><td>Cet opérateur est utilisé pour trouver le produit de deux expressions d’argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Reste</a> </td><td>Cet opérateur est utilisé pour trouver le reste après la division des deux expressions d’argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Substitution</a> </td><td>Cet opérateur détecte la différence entre deux expressions</td>
    </tr>
</table>


### Fonctions booléennes

Fonctions booléennes sont utilisés pour exécuter une logique booléenne sur différents éléments.

<table>
    <tr>
        <td><a href="operators.md#and">And</a></td><td>Cet opérateur crée une conjonction logique.</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">If</a></td><td>Cet opérateur résout une expression selon qu’une condition spécifiée est vraie ou non.</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Not</a></td><td>Cet opérateur crée une négation logique</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Ou</a></td><td>Cet opérateur crée une disjonction logique.</td>
    </tr>
</table>


### Fonctions de comparaison

Fonctions de comparaison sont utilisées pour comparer différentes expressions et valeurs, renvoyant true ou false en conséquence.

<table>
    <tr>
        <td><a href="operators.md#and">Égal</a></td><td>Cette opération vérifie si les valeurs sont égales.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Supérieur à</a></td><td>Cet opérateur vérifie si la première valeur est supérieure à la seconde valeur.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Supérieur ou égal à</a></td><td>Cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde valeur</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">N’est pas égal à</a></td><td>Cet opérateur vérifie si l'expression donnée n'est pas égale à la valeur donnée.</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Inférieur ou égal à</a> </td><td>Cet opérateur vérifie si la première valeur est inférieure ou égale à la seconde valeur.</td>
    </tr>
</table>

