---
title: Prise en main des fonctions d’assistance
description: Bibliothèque des fonctions d’assistance de Journey Optimizer
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 315c3e8c04b2e3944d0d5b2befb205acbe0ef7c9
workflow-type: tm+mt
source-wordcount: '1744'
ht-degree: 0%

---

# Prise en main des fonctions d’assistance{#functions}

Utilisation [!DNL Journey Optimizer] langage de modèle pour effectuer des opérations sur des données, telles que des calculs, le formatage ou les conversions de données, les conditions et les manipuler dans le contexte de la personnalisation. Découvrez les instructions relatives à la syntaxe de la personnalisation dans la section [cette page](../personalization-syntax.md).

➡️ [Découvrez comment utiliser les fonctions d’assistance dans cette vidéo](#video)

Le langage de modèle est utilisé dans les fonctions d’assistance disponibles dans la liste déroulante de personnalisation de l’éditeur d’expression, comme ci-dessous :

![](../assets/access-helper-functions.png)

Dans le [!DNL Journey Optimizer] Editeur d&#39;expression, les fonctions d&#39;assistance sont regroupées en trois catégories : [Fonctions](#functions-helper), [Helpers](#helper-helper) et [Opérateurs](#operators-helper).

Sélectionnez une catégorie pour accéder aux sous-catégories et fonctions.

Accédez aux sous-catégories en cliquant sur le `>` icône . Sélectionnez une fonction en cliquant sur la fonction `+` icon : la fonction est automatiquement ajoutée à l’écran de personnalisation.

Cliquez sur le bouton `...` pour afficher la description de la fonction et l’ajouter à vos favoris. [En savoir plus](../personalize.md#fav)

## Fonctions{#functions-helper}

### Fonctions d’agrégation et de tableau

<table>
    <tr>
        <td><a href="aggregation.md#average">Moyenne</a></td><td>Cette fonction renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a></td><td>Cette fonction renvoie le nombre d’éléments dans le tableau donné.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Nombre uniquement nul</a></td><td>Cette fonction comptabilise le nombre de valeurs "null" dans la liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Compter avec valeur nulle</a></td><td>Cette fonction comptabilise tous les éléments de la liste, y compris les valeurs "null".</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Cette fonction récupère les valeurs d’un tableau ou d’une liste dont les valeurs en double sont supprimées.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Comptage distinct avec valeur nulle</a></td><td>Cette fonction comptabilise le nombre de valeurs différentes, y compris les valeurs "null".</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Premier élément</a></td><td>Cette fonction renvoie le premier élément d’un tableau ou d’une liste</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">First n in array</a></td><td>Cette fonction renvoie les premiers éléments "N" d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction de l’expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Dans</a></td><td>Cette fonction permet de déterminer si un élément est membre d’un tableau ou d’une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclut</a></td><td>Cette fonction détermine si un tableau ou une liste contient un élément donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a></td><td>Cette fonction détermine si deux tableaux ou deux listes ont au moins un membre commun</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">N dernier dans le tableau</a></td><td>Cette fonction renvoie les derniers éléments "N" d’un tableau, lorsqu’ils sont triés dans l’ordre croissant en fonction de l’expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Cette fonction renvoie la plus grande de toutes les valeurs sélectionnées dans un tableau.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Cette fonction renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau .</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a></td><td>Cette fonction détermine si un élément n’est pas membre d’un tableau ou d’une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sous-ensemble de</a></td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sous-ensemble d’un autre tableau (tableau B), c’est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Somme</a></td><td>Cette fonction renvoie la somme de toutes les valeurs sélectionnées dans le tableau .</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a></td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sur-ensemble d’un autre tableau (tableau B), c’est-à-dire si ce tableau A contient tous les éléments du tableau B.</td>
    </tr>
</table>

### Fonctions de date et d’heure{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Age</a></td><td>Cette fonction récupère l’âge à partir d’une date donnée.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Durée actuelle en millisecondes</a></td><td>Cette fonction récupère l’heure actuelle en millisecondes époque</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Différence entre dates</a></td><td>Cette fonction récupère la différence entre deux dates en nombre de jours</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Jour de la semaine</a></td><td>Cette fonction récupère le jour de la semaine.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Jour de l’année</a></td><td>Cette fonction récupère le jour de l’année</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Date de format</a></td><td>Cette fonction formate une valeur de date et d’heure</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Définir les jours</a></td><td>Cette fonction définit le jour du mois pour la date et l’heure données</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Définition des heures</a></td><td>Cette fonction définit l’heure de la date et de l’heure</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">À UTC</a></td><td>Cette fonction convertit un datetime en UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semaine de l’année</a></td><td>Cette fonction renvoie la semaine de l’année</td>
    </tr>
</table>
</table>

### Fonctions de mappage {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Get</a></td><td>Cette fonction est utilisée pour récupérer la valeur d’une carte pour une clé donnée.</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Clés</a></td><td>Cette fonction est utilisée pour récupérer toutes les clés d’une carte donnée.</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valeurs</a></td><td>Cette fonction récupère toutes les valeurs d’une carte donnée.</td>
    </tr>
</table>

### Fonctions mathématiques {#math-functions}

<table>
    <tr>
        <td><a href="objects.md#absolute">Absolu</a></td><td>Cette fonction convertit un nombre dont la valeur est absolue</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">Random</a></td><td>Cette fonction renvoie une valeur aléatoire comprise entre 0 et 1</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-down">Arrondir</a></td><td>Cette fonction arrondit un nombre</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-up">Tour à tour</a></td><td>Cette fonction arrondit un nombre</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-percentage">En pourcentage</a></td><td>Cette fonction convertit un nombre en pourcentage</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-precision">Précision</a></td><td>Cette fonction convertit un nombre à la précision requise</td>
    </tr>
</table>

### Fonctions d’objet {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">N’est pas nul</a></td><td>Cette fonction permet de déterminer s’il existe une référence d’objet.</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Is null</a></td><td>Cette fonction permet de déterminer si une référence d’objet n’existe pas.</td>
    </tr>
</table>

### Fonctions de chaîne {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Cette fonction permet de mettre en majuscules la première lettre de chaque mot d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Cette fonction permet de combiner deux chaînes en une seule.</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contient</a></td><td>Cette fonction permet de déterminer si une chaîne contient une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Ne contient pas</a></td><td>Cette fonction permet de déterminer si une chaîne ne contient pas de sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Ne se termine pas par</a></td><td>Cette fonction permet de déterminer si une chaîne ne se termine pas par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Ne commence pas par</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Encode 64</a></td><td>Cette fonction est utilisée pour coder ou décoder une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Se termine par</a></td><td>Cette fonction permet de déterminer si une chaîne se termine par une sous-chaîne donnée.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Est égal à</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée, en respectant la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Est égal à Ignorer la casse</a></td><td>Cette fonction permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée, sans respect de la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extract Email Domain</a></td><td>Cette fonction est utilisée pour extraire le domaine d’une adresse électronique.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Obtention de l’hôte d’URL</a></td><td>Cette fonction est utilisée pour obtenir l’hôte d’URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Obtention du chemin d’URL</a></td><td>Cette fonction est utilisée pour obtenir le chemin d’URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Obtenir le protocole url</a></td><td>Cette fonction est utilisée pour obtenir le protocole url</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Index de</a></td><td>Cette fonction renvoie la position (dans le premier argument) de la première occurrence du deuxième paramètre. Renvoie -1 s’il n’y a aucune correspondance</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Cette fonction permet de vérifier si une chaîne ou une expression est vide.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">N’est pas vide</a></td><td>Cette fonction renvoie true si la chaîne du paramètre n’est pas vide.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Dernier index de</a></td><td>Cette fonction renvoie la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Rognage gauche</a></td><td>Cette fonction supprime les espaces blancs au début d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Longueur</a></td><td>Cette fonction est utilisée pour obtenir le nombre de caractères d’une chaîne ou d’une expression.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Comme</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à un modèle spécifié.</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minuscule</a></td><td>Cette fonction convertit une chaîne en minuscules</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Masque</a></td><td>Cette fonction est utilisée pour remplacer une partie d’une chaîne par des caractères "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Correspond à</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à une expression régulière spécifique.</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Cette fonction renvoie le hachage md5 de la chaîne d’entrée.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Différent de</a></td><td>Cette fonction permet de déterminer si une chaîne n’est pas égale à la chaîne spécifiée.</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Différent De La Case Ignorer</a></td><td>Cette fonction compare deux chaînes en ignorant la casse.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Groupe d’expressions régulières</a></td><td>Cette fonction est utilisée pour extraire des informations spécifiques, en fonction de l’expression régulière fournie.</td>
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
        <td><a href="string.md#split">Partage</a></td><td>Cette fonction est utilisée pour fractionner une chaîne selon un caractère donné.</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Commence par</a></td><td>Cette fonction permet de déterminer si une chaîne commence par une sous-chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Chaîne à date</a></td><td>Cette fonction est utilisée pour convertir une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Chaîne à entier</a></td><td>Cette fonction Convertit une valeur string en valeur entière.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Chaîne à nombre</a></td><td>Cette fonction est utilisée pour convertir une chaîne en nombre. Elle renvoie la même chaîne que la sortie pour une entrée non valide.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Sous-chaîne</a></td><td>Cette fonction renvoie la sous-chaîne de l’expression de chaîne entre l’index de début et l’index de fin.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Cas de titre</a></td><td>Cette fonction permet de mettre en majuscules les premières lettres de chaque mot d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">À Bool</a></td><td>Cette fonction convertit une valeur d’argument en valeur booléenne, selon son type.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Heure de la date</a></td><td>Cette fonction est utilisée pour convertir une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">À Date Heure uniquement</a></td><td>Cette fonction convertit une valeur d’argument en une valeur de date et d’heure uniquement. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Rogner</a></td><td>Cette fonction supprime les espaces blancs du début et de la fin d’une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">majuscule</a></td><td>Cette fonction convertit une chaîne en majuscules</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Décodage de l’URL</a></td><td>Cette fonction est utilisée pour décoder une chaîne codée en URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Encode d'URL</a></td><td>Cette fonction est utilisée pour encoder une chaîne en URL.</td>
    </tr>
</table>


## Helpers{#helper-helper}

Les assistants sont présentés dans la section [cette page](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valeur de secours par défaut</a></td><td>Cette fonction permet d’effectuer le rendu d’une variable avec la valeur par défaut.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Chaque</a></td><td>Cette fonction est utilisée pour effectuer une itération sur un tableau</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">If</a></td><td>Cette fonction est utilisée pour définir un bloc conditionnel. Si l’évaluation de l’expression renvoie true (vrai), le bloc est rendu.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Cette fonction permet à une expression d’être stockée en tant que variable et d’être utilisée ultérieurement dans une requête.</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Sauf</a></td><td>Cette fonction est utilisée pour définir un bloc conditionnel. Si l’évaluation de l’expression renvoie false, le bloc est rendu.</td>
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
        <td><a href="arithmetic-functions.md#divide">Diviser</a></td><td>Cet opérateur est utilisé pour trouver le quotient de deux expressions d’argument.</td>
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


### Fonctions booléennes {#boolean-functions}

Les fonctions booléennes sont utilisées pour exécuter une logique booléenne sur différents éléments.

<table>
    <tr>
        <td><a href="operators.md#and">Et</a></td><td>Cet opérateur crée une conjonction logique.</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Ou</a></td><td>Cet opérateur crée une disjonction logique.</td>
    </tr>
</table>


### Fonctions de comparaison {#comparison-functions}

Les fonctions de comparaison sont utilisées pour comparer différentes expressions et valeurs, renvoyant true ou false en conséquence.

<table>
    <tr>
        <td><a href="operators.md#equals">Est égal à</a></td><td>Cette opération vérifie si les valeurs sont égales.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Supérieur à</a></td><td>Cet opérateur vérifie si la première valeur est supérieure à la seconde valeur.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Supérieur ou égal à</a></td><td>Cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde valeur</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Inférieur ou égal à</a> </td><td>Cet opérateur vérifie si la première valeur est inférieure ou égale à la seconde valeur.</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">N’est pas égal à</a></td><td>Cet opérateur vérifie si l'expression donnée n'est pas égale à la valeur donnée.</td>
    </tr>
</table>

## Vidéo pratique{#video}

Découvrez comment transformer des valeurs de personnalisation à l’aide de fonctions d’assistance à la personnalisation et comprendre différents cas d’utilisation des fonctions d’assistance.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
