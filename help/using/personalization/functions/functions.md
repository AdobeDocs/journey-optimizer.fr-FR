---
title: Prise en main des fonctions d’assistance
description: Bibliothèque de fonctions d’assistance Journey Optimizer
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 76%

---

# Prise en main des fonctions d’assistance{#functions}

Utilisez le langage de modèle [!DNL Journey Optimizer] pour effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions des données, des conditions, et les manipuler dans le contexte de la personnalisation. Découvrez les instructions de syntaxe de personnalisation dans [cette page](../personalization-syntax.md).

➡️ [Découvrez comment utiliser les fonctions d&#39;assistance dans cette vidéo](#video)

Le langage de modèle est utilisé dans les fonctions d&#39;assistance disponibles dans la liste déroulante de personnalisation de l&#39;éditeur d&#39;expression, comme ci-dessous :

![](../assets/access-helper-functions.png)

Dans l&#39;éditeur d&#39;expression [!DNL Journey Optimizer], les fonctions d&#39;assistance sont regroupées en trois catégories : [Fonctions](#functions-helper), [Assistants](#helper-helper) et [Opérateurs](#operators-helper).

Sélectionnez une catégorie pour accéder aux sous-catégories et fonctions.

Accédez aux sous-catégories en cliquant sur l’icône `>`. Sélectionnez une fonction en cliquant sur l’icône `+` : la fonction est automatiquement ajoutée à l’écran de personnalisation.

Cliquez sur l’icône `...` pour afficher la description de la fonction et l’ajouter à vos favoris. [En savoir plus](../personalize.md#fav)

## Fonctions{#functions-helper}

### Fonctions d’agrégation et de tableau

<table>
    <tr>
        <td><a href="aggregation.md#average">Average</a></td><td>Cette fonction renvoie la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a></td><td>Cette fonction renvoie le nombre d'éléments dans le tableau donné.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Nombre uniquement nul</a></td><td>Cette fonction comptabilise le nombre de valeurs "null" dans la liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Compter avec valeur nulle</a></td><td>Cette fonction comptabilise tous les éléments de la liste, y compris les valeurs "null".</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Cette fonction récupère les valeurs d'un tableau ou d'une liste dont les valeurs en double sont supprimées.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Comptage distinct avec valeur nulle</a></td><td>Cette fonction comptabilise le nombre de valeurs différentes, y compris les valeurs "null".</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">First item</a></td><td>Cette fonction renvoie le premier élément d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">First n in array</a></td><td>Cette fonction renvoie les premiers éléments "N" d'un tableau, lorsqu'ils sont triés dans l'ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>Cette fonction permet de déterminer si un élément est un membre d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Includes</a></td><td>Cette fonction détermine si un tableau ou une liste contient un élément donné.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a></td><td>Cette fonction détermine si deux tableaux ou deux listes ont au moins un membre commun.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Last n in array</a></td><td>Cette fonction renvoie les derniers éléments "N" d'un tableau, lorsqu'ils sont triés dans l'ordre croissant en fonction de l'expression numérique donnée.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Cette fonction renvoie la plus grande de toutes les valeurs sélectionnées dans un tableau.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Cette fonction renvoie la plus petite de toutes les valeurs sélectionnées dans le tableau.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a></td><td>Cette fonction détermine si un élément n'est pas membre d'un tableau ou d'une liste.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset of</a></td><td>Cette fonction détermine si un tableau spécifique (tableau A) est un sous-ensemble d'un autre tableau (tableau B), c'est-à-dire si tous les éléments du tableau A sont des éléments du tableau B.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Cette fonction renvoie la somme de toutes les valeurs sélectionnées dans le tableau.</td>
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
        <td><a href="dates.md#set-hours">Définition des heures</a></td><td>Cette fonction définit l’heure de la date et de l’heure.</td>
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

### Fonctions mathématiques {#math-functions}

<table>
    <tr>
        <td><a href="objects.md#absolute">Absolu</a></td><td>Cette fonction convertit un nombre dont la valeur est absolue</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">Aléatoire</a></td><td>Cette fonction renvoie une valeur aléatoire comprise entre 0 et 1</td>
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

### Fonctions d&#39;objet {#object-functions}

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
        <td><a href="string.md#get-url-host">Obtention de l’hôte d’URL</a></td><td>Cette fonction est utilisée pour obtenir l’hôte d’URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Obtention du chemin d’URL</a></td><td>Cette fonction est utilisée pour obtenir le chemin d’URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Obtenir le protocole url</a></td><td>Cette fonction est utilisée pour obtenir le protocole url</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Index de</a></td><td>Cette fonction renvoie la position (dans le premier argument) de la première occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">isEmpty</a></td><td>Cette fonction permet de vérifier si une chaîne ou une expression est vide.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">N’est pas vide</a></td><td>Cette fonction renvoie true si la chaîne du paramètre n’est pas vide.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Dernier index de</a></td><td>Cette fonction renvoie la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.</td>
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
        <td><a href="string.md#mask">Masque</a></td><td>Cette fonction est utilisée pour remplacer une partie d’une chaîne par des caractères "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Matches</a></td><td>Cette fonction permet de déterminer si une chaîne correspond à une expression régulière donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Cette fonction renvoie le hachage md5 de la chaîne d’entrée.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Not equal to</a></td><td>Cette fonction permet de déterminer si une chaîne est différente d'une chaîne donnée.</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Différent De La Case Ignorer</a></td><td>Cette fonction compare deux chaînes en ignorant la casse.</td>
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
        <td><a href="string.md#titleCase">Title Case</a></td><td>Cette fonction permet de mettre en majuscules les premières lettres de chaque mot d'une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">À Bool</a></td><td>Cette fonction Convertit une valeur d’argument en valeur booléenne, selon son type.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Heure de la date</a></td><td>Cette fonction est utilisée pour convertir une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">À Date Heure uniquement</a></td><td>Cette fonction convertit une valeur d’argument en une valeur de date et d’heure uniquement. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Trim</a></td><td>Cette fonction supprime les espaces blancs du début et de la fin d'une chaîne.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Upper case</a></td><td>Cette fonction convertit une chaîne en majuscules.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Décodage de l’URL</a></td><td>Cette fonction est utilisée pour décoder une chaîne codée en URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Url encore</a></td><td>Cette fonction est utilisée pour encoder une chaîne en URL.</td>
    </tr>
</table>


## Assistants{#helper-helper}

Les assistants sont détaillés dans [cette page](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valeur de secours par défaut</a></td><td>Cette fonction permet d’effectuer le rendu d’une variable avec la valeur par défaut.</td>
    </tr>
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
        <td><a href="operators.md#or">Or</a></td><td>Cet opérateur crée une disjonction logique.</td>
    </tr>
</table>


### Fonctions de comparaison  {#comparison-functions}

Les fonctions de comparaison sont utilisées pour comparer les différentes expressions et valeurs, renvoyant &#39;true&#39; ou &#39;false&#39; en conséquence.

<table>
    <tr>
        <td><a href="operators.md#equals">Est égal à</a></td><td>Cette opération vérifie si les valeurs sont égales.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>Cet opérateur vérifie si la première valeur est supérieure à la seconde valeur.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Greater or equals to</a></td><td>Cet opérateur vérifie si la première valeur est supérieure ou égale à la seconde valeur</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Less than or equals to</a> </td><td>Cet opérateur vérifie si la première valeur est inférieure ou égale à la deuxième valeur.</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Not equals to</a></td><td>Cet opérateur vérifie si l'expression donnée n'est pas égale à la valeur donnée.</td>
    </tr>
</table>

## Vidéo pratique{#video}

Découvrez comment transformer des valeurs de personnalisation à l&#39;aide de fonctions d&#39;assistance à la personnalisation et comprendre différents cas d&#39;utilisation des fonctions d&#39;assistance.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
