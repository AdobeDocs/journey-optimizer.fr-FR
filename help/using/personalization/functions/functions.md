---
title: Prise en main des fonctions d’assistance
description: Bibliothèque de fonctions d’assistance Journey Optimizer
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 100%

---

# Prise en main des fonctions d’assistance{#functionsL}

Utilisez le langage de modèle [!DNL Journey Optimizer] pour effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions des données, des conditions, et les manipuler dans le contexte de la personnalisation. Découvrez les instructions de syntaxe de personnalisation dans [cette page](../personalization-syntax.md).

➡️ [Découvrez comment utiliser les fonctions d&#39;assistance](#video) (vidéo)

Le langage de modèle est utilisé dans les fonctions d&#39;assistance disponibles dans la liste déroulante de personnalisation de l&#39;éditeur d&#39;expression, comme ci-dessous :

![](../assets/access-helper-functions.png)

Dans l&#39;éditeur d&#39;expression [!DNL Journey Optimizer], les fonctions d&#39;assistance sont regroupées en trois catégories : [Fonctions](#functions-helper), [Assistants](#helper-helper) et [Opérateurs](#operators-helper).

Sélectionnez une catégorie pour accéder aux sous-catégories et fonctions.

Accédez aux sous-catégories en cliquant sur l’icône `>`. Sélectionnez une fonction en cliquant sur l’icône `+` : la fonction est automatiquement ajoutée à l’écran de personnalisation.

Cliquez sur l’icône `...` pour afficher la description de la fonction et l’ajouter à vos favoris. [En savoir plus](../personalize.md#fav)

## Fonctions{#functions-helper}

### Fonctions de tableau

<table>
    <tr>
        <td><a href="aggregation.md#average">Average</a></td><td>Cette fonction renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>Cette fonction permet de déterminer si un élément est un membre d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Cette fonction renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a></td><td>Cette fonction renvoie le nombre d'éléments dans le tableau donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Includes</a></td><td>Cette fonction détermine si un tableau ou une liste contient un élément donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a></td><td>Cette fonction détermine si un élément n'est pas membre d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Cette fonction récupère les valeurs d'un tableau ou d'une liste dont les valeurs en double sont supprimées.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a></td><td>Cette fonction détermine si deux tableaux ou deux listes ont au moins un membre commun.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset of</a></td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sous-ensemble d'un autre tableau (tableau B), c'est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">First item</a></td><td>Cette fonction renvoie le premier élément d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Last n in array</a></td><td>Cette fonction renvoie les derniers éléments "N" d'un tableau, lorsqu'ils sont triés dans l'ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Cette fonction renvoie la somme de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">First n in array</a></td><td>Cette fonction renvoie les premiers éléments "N" d'un tableau, lorsqu'ils sont triés dans l'ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Cette fonction renvoie la plus grande de toutes les valeurs sélectionnées dans un tableau.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a></td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sur-ensemble d'un autre tableau (tableau B), c'est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
</table>

### Fonctions de date/heure{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Âge</a></td><td>Cette fonction récupère l’âge à partir d’une date donnée.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Heure actuelle en millisecondes</a></td><td>Cette fonction récupère l’heure actuelle en millisecondes epoch.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Différence de date</a></td><td>Cette fonction récupère la différence entre deux dates en nombre de jours</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Jour de la semaine</a></td><td>Cette fonction récupère le jour de la semaine.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Jour de l’année</a></td><td>Cette fonction récupère le jour de l’année.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Date de format</a></td><td>Cette fonction permet de formater une valeur de date et d’heure.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Définir les jours</a></td><td>Cette fonction définit le jour du mois pour la date et l’heure données.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Définir les jours</a></td><td>Cette fonction définit l’heure de la date et de l’heure.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">En UTC</a></td><td>Cette fonction convertit une date-heure en UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semaine de l’année</a></td><td>Cette fonction renvoie la semaine de l’année.</td>
    </tr>
</table>
</table>

### Fonctions de mappage {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Get</a></td><td>Cette fonction est utilisée pour récupérer la valeur d'un mappage pour une clé donnée.</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Keys</a></td><td>Cette fonction est utilisée pour récupérer toutes les clés d'un mappage donné.</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Values</a></td><td>Cette fonction récupère toutes les valeurs d'un mappage donné.</td>
    </tr>
</table>

**Fonctions d&#39;objet**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Fonction isNotNull</a></td><td>Cette fonction permet de déterminer s'il existe une référence d'objet.</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Fonction isNull</a></td><td>Cette fonction permet de déterminer si une référence d'objet n'existe pas.</td>
    </tr>
</table>

### Fonctions de chaîne {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Cette fonction permet de mettre en majuscule la première lettre de chaque mot d'une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Cette fonction permet de combiner deux chaînes en une seule.</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>Cette fonction permet de déterminer si une chaîne contient une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Does not contain</a></td><td>Cette fonction permet de déterminer si une chaîne ne contient pas une sous-chaîne donnée.</td>
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
        <td><a href="string.md#equals">Equals</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée, avec respect de la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Equals Ignore Case</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée, sans respect de la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extract Email Domain</a></td><td>Cette fonction est utilisée pour extraire le domaine d'une adresse e-mail.</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">isEmpty</a></td><td>Cette fonction permet de vérifier si une chaîne ou une expression est vide.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Left trim</a></td><td>Cette fonction supprime les espaces blancs au début d'une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Cette fonction est utilisée pour obtenir le nombre de caractères d'une chaîne ou d'une expression.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Like</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à un modèle donné.</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Lower Case</a></td><td>Cette fonction convertit une chaîne en minuscules.</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Matches</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à une expression régulière donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Not equals to</a></td><td>Cette fonction permet de déterminer si une chaîne est différente d'une chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Regular expression group</a></td><td>Cette fonction est utilisée pour extraire des informations spécifiques en fonction de l'expression régulière fournie.</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a></td><td>Cette fonction remplace une sous-chaîne donnée dans une chaîne par une autre sous-chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Replace all</a></td><td>Cette fonction remplace toutes les sous-chaînes d'un texte correspondant à la "cible" par la chaîne de "remplacement" littérale spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Right trim</a></td><td>Cette fonction supprime les espaces blancs à la fin d'une chaîne. </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a></td><td>Cette fonction est utilisée pour fractionner une chaîne selon un caractère donné.</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Starts with</a></td><td>Cette fonction permet de déterminer si une chaîne commence par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Title Case</a></td><td>Cette fonction permet de mettre en majuscules les premières lettres de chaque mot d'une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Trim</a></td><td>Cette fonction supprime les espaces blancs du début et de la fin d'une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Upper case</a></td><td>Cette fonction convertit une chaîne en majuscules.</td>
    </tr>
</table>


## Assistants{#helper-helper}

Les assistants sont détaillés dans [cette page](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>Cette fonction est utilisée pour effectuer une itération sur un tableau</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">If</a></td><td>Cette fonction est utilisée pour définir un bloc conditionnel. Si l'évaluation de l'expression renvoie 'true', le bloc est rendu.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Cette fonction permet à une expression d'être stockée en tant que variable et d'être utilisée ultérieurement dans une requête.</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>Cette fonction est utilisée pour définir un bloc conditionnel. Si l'évaluation de l'expression renvoie 'false', le bloc est rendu.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>Cette fonction est utilisée pour modifier le jeton d'évaluation d'une partie de modèle.</td>
    </tr>
</table>

## Opérateurs{#operators-helper}

### Fonctions arithmétiques  {#arithmetic-helper}

Les fonctions arithmétiques sont utilisées pour effectuer des calculs de base sur des valeurs.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Addition</a></td><td>Cet opérateur est utilisé pour trouver la somme de deux expressions d'argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Divide</a></td><td>Cet opérateur est utilisé pour trouver le quotient de deux expressions d'argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplication</a></td><td>Cet opérateur est utilisé pour trouver le produit de deux expressions d'argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Remainder</a> </td><td>Cet opérateur est utilisé pour trouver le reste après la division des deux expressions d'argument.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Subtraction</a> </td><td>Cet opérateur détecte la différence entre deux expressions.</td>
    </tr>
</table>


### Fonctions booléennes  {#boolean-functions}

Les fonctions booléennes sont utilisées pour exécuter une logique booléenne sur différents éléments.

<table>
    <tr>
        <td><a href="operators.md#and">And</a></td><td>Cet opérateur crée une conjonction logique.</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">If</a></td><td>Cet opérateur résout une expression selon qu'une condition spécifiée est vraie ou non.</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Not</a></td><td>Cet opérateur crée une négation logique.</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Or</a></td><td>Cet opérateur crée une disjonction logique.</td>
    </tr>
</table>


### Fonctions de comparaison  {#comparison-functions}

Les fonctions de comparaison sont utilisées pour comparer les différentes expressions et valeurs, renvoyant &#39;true&#39; ou &#39;false&#39; en conséquence.

<table>
    <tr>
        <td><a href="operators.md#and">Equals to</a></td><td>Cette opération vérifie si les valeurs sont égales.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>Cet opérateur vérifie si la première valeur est supérieure à la seconde valeur.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Greater or equals to</a></td><td>Cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde valeur</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">N’est pas égal à</a></td><td>Cet opérateur vérifie si l'expression donnée n'est pas égale à la valeur donnée.</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Less than or equals to</a> </td><td>Cet opérateur vérifie si la première valeur est inférieure ou égale à la deuxième valeur.</td>
    </tr>
</table>

## Vidéo pratique{#video}

Découvrez comment transformer des valeurs de personnalisation à l&#39;aide de fonctions d&#39;assistance à la personnalisation et comprendre différents cas d&#39;utilisation des fonctions d&#39;assistance.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
