---
product: journey optimizer
title: Fonctions de chaîne
description: En savoir plus sur les fonctions de chaîne
feature: Journeys
role: Developer
level: Experienced
keywords: chaîne, fonctions, expression, parcours, texte, manipulation
version: Journey Orchestration
exl-id: 8186c564-56fa-417a-afd3-8e479e5b23b9
TQID: https://experienceleague.adobe.com/wrP3c7l3uHzN6w3l-fXBQOSb5Tx2NuW-6iyogKpDPc8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1668
ht-degree: 68%

---

# Fonctions de chaîne {#string-functions}

Les fonctions de chaîne vous permettent de manipuler et d’utiliser des valeurs de texte dans vos expressions de parcours. Ces fonctions sont essentielles pour le traitement de texte, la validation, la transformation et l’analyse dans vos parcours clients.

Utilisez des fonctions de chaîne lorsque vous devez :

* concaténer et combiner plusieurs valeurs de texte ([concat](#concat)) ;
* rechercher des modèles de texte ou des sous-chaînes spécifiques ([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp)) ;
* comparer des chaînes avec une correspondance sensible ou insensible à la casse ([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase)) ;
* vérifier que la chaîne commence et se termine ([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase)) ;
* extraire des parties de texte à l’aide d’opérations de sous-chaîne ([substr](#substr)) ;
* transformer le texte en majuscules ou en minuscules ([majuscule](#upper), [inférieure](#lower), [rognage](#trim)) ;
* vérifier si les chaînes sont vides ou contiennent des valeurs spécifiques ([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty)) ;
* remplacer des modèles de texte par de nouvelles valeurs ([replace](#replace), [replaceAll](#replaceAll)) ;
* partager les chaînes en tableaux pour un traitement ultérieur ([division](#split)) ;
* obtenir la longueur de la chaîne ([length](#length)) ou générer les identifiants uniques ([uuid](#uuid)).

Les fonctions de chaîne fournissent des fonctionnalités complètes de manipulation de texte, permettant un traitement des données sophistiqué et une logique conditionnelle basée sur le contenu texte de vos expressions de parcours.

## concat {#concat}

Concatène deux paramètres de chaîne ou une liste de chaînes.

+++Syntaxe

`concat(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| Liste | listString |
| chaîne | string |

+++

+++Signature et type renvoyé

`concat(<string>,<string>)`

`concat(<listString>)`

Renvoie une chaîne.

+++

+++Exemples

`concat("Hello","World")`

Renvoie « HelloWorld ».

`concat(["Hello"," ","World"])`

Renvoie « Hello World ».

+++

## contain {#contain}

Vérifie si la chaîne du deuxième argument est contenue dans la chaîne du premier argument.

+++Syntaxe

`contain(<parameters>)`

+++

+++Paramètres

* chaîne

+++

+++Signature et type renvoyé

`contain(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`contain("rowing is great", "great")`

Renvoie true.

+++

## containIgnoreCase {#containIgnoreCase}

Vérifie si la chaîne du deuxième argument est contenue dans la chaîne du premier argument, sans tenir compte de la casse.

+++Syntaxe

`containIgnoreCase(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | Chaîne |
| chaîne recherchée | chaîne |

+++

+++Signature et type renvoyé

`containIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`containIgnoreCase("rowing is great", "GREAT")`

Renvoie true.

+++

## endWith {#endWith}

Renvoie « true » si le deuxième paramètre est un suffixe du premier.

+++Syntaxe

`endWith(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | Chaîne |
| suffixe | chaîne |

+++

+++Signature et type renvoyé

`endWith(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`endWith("Hello World", "World")`

Renvoie true.

`endWith("Hello World", "Hello")`

Renvoie false.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

Vérifie si la chaîne du premier argument se termine par une chaîne spécifique (chaîne du deuxième argument), sans tenir compte de la casse.

+++Syntaxe

`endWithIgnoreCase(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | Chaîne |
| suffixe | chaîne |

+++

+++Signature et type renvoyé

`endWithIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`endWithIgnoreCase("rowing is great", "AT")`

Renvoie true.

+++

## equalIgnoreCase {#equalIgnoreCase}

Compare la chaîne du premier argument à la chaîne du deuxième argument, en ignorant les considérations de casse.

+++Syntaxe

`equalIgnoreCase(<parameters>)`

+++

+++Paramètres

* chaîne

+++

+++Signature et type renvoyé

`equalIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

Renvoie true.

+++

## indexOf {#indexOf}

Renvoie la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

+++Syntaxe

`indexOf(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | Chaîne |
| valeur spécifiée | Chaîne |

+++

+++Signature et type renvoyé

`indexOf(<string>,<string>)`

Renvoie un entier.

+++

+++Exemples

`indexOf("Hello", "l")`

Renvoie 2.

Explication :

Dans « Hello », la première occurrence de « l » est en position 2.

+++

## isEmpty {#isEmpty}

Renvoie « true » si la chaîne du paramètre ne contient aucun caractère.

+++Syntaxe

`isEmpty(<parameters>)`

+++

+++Paramètres

* chaîne

+++

+++Signature et type renvoyé

`isEmpty(<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`isEmpty("")`

Renvoie true.

`isEmpty("Hello World")`

Renvoie false.

`isEmpty(<null>)`

Renvoie false.

+++

## isNotEmpty {#isNotEmpty}

Renvoie « true » si la chaîne du paramètre n’est pas vide.

+++Syntaxe

`isNotEmpty(<parameters>)`

+++

+++Paramètres

* chaîne

+++

+++Signature et type renvoyé

`isNotEmpty(<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`isNotEmpty("")`

Renvoie false.

`isNotEmpty("hello")`

Renvoie true.

+++

## lastIndexOf {#lastIndexOf}

Renvoie la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

+++Syntaxe

`lastIndexOf(<parameters>)`

+++

+++Paramètre

| Paramètre | Type |
|-----------|------------------|
| chaîne | Chaîne |
| valeur spécifiée | Chaîne |

+++

+++Signature et type renvoyé

`lastIndexOf(<string>,<string>)`

Renvoie un entier.

+++

+++Exemples

`lastIndexOf("Hello", "l")`

Renvoie 3.

Explication :

Dans « Hello », la dernière occurrence de « l » est en position 3.

+++

## length {#length}

Renvoie le nombre de caractères de l’expression sous forme de chaîne dans le paramètre.

+++Syntaxe

`length(<parameters>)`

+++

+++Paramètre

* chaîne

+++

+++Signature et type renvoyé

`length(<string>)`

Renvoie un entier.

+++

+++Exemples

`length("Hello World")`

Renvoie 11.

+++

## lower {#lower}

Renvoie une version en minuscules du paramètre.

+++Syntaxe

`lower(<parameter>)`

+++

+++Paramètre

* chaîne

+++

+++Signature et type renvoyé

`lower(<string>)`

Renvoie une chaîne.

+++

+++Exemples

`lower("A")`

Renvoie « a ».

+++

## matchRegExp {#matchRegExp}

Renvoie « true » si la chaîne du premier paramètre correspond à l’expression régulière du second paramètre. Pour plus d’informations, consultez [cette page](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Syntaxe

`matchRegExp(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|--- |--- |
| chaîne | Chaîne |
| regexp | chaîne |

+++

+++Signature et type renvoyé

`matchRegExp(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`matchRegExp("12345", "\\d+")`

Renvoie true.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

Vérifie si la chaîne du premier argument est différente de la chaîne du deuxième argument, en ignorant les considérations de casse.

+++Syntaxe

`notEqualIgnoreCase(<parameters>)`

+++

+++Paramètres

* chaîne

+++

+++Signature et type renvoyé

`notEqualIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

Remplace la première occurrence correspondant à la chaîne cible par la chaîne de remplacement dans la chaîne de base.

Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

+++Syntaxe

`replace(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|--------------|
| base | chaîne |
| cible | string (RegExp) |
| remplacement | chaîne |

+++

+++Signature et type renvoyé

`replace(<base>,<target>,<replacement>)`

Renvoie une chaîne.

+++

+++Exemples

`replace("Hello World", "l", "x")`

Renvoie « Hexlo World ».

**Exemple avec RegExp :**

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Voici un exemple :

* chaîne à évaluer : `|OFFER_A|OFFER_B`
* fourni par un attribut de profil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Chaîne à remplacer : `|OFFER_A`
* Chaîne remplacée par : `''`
* Vous devez ajouter `\\` avant le caractère `|`.

L’expression est la suivante :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La chaîne renvoyée est la suivante : `|OFFER_B`

Vous pouvez également créer la chaîne à remplacer à partir d’un attribut donné :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Remplace toutes les occurrences correspondant à la chaîne cible par la chaîne de remplacement dans la chaîne de base.

Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

+++Syntaxe

`replaceAll(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|--------------|
| base | chaîne |
| cible | string (RegExp) |
| remplacement | chaîne |

+++

+++Signature et type renvoyé

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Renvoie une chaîne.

+++

+++Exemples

`replaceAll("Hello World", "l", "x")`

Renvoie « Hexxo Worxd ».

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Reportez-vous à l’exemple de la fonction [replace](#replace).

+++

## split {#split}

Partage la première chaîne d’arguments avec une chaîne de séparateur (deuxième chaîne d’arguments, qui peut être une expression régulière) pour produire une liste de chaînes (jetons).

+++Syntaxe

`split(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne d’entrée | string |
| chaîne de séparateur | chaîne |

+++

+++Signatures et type renvoyé

`split(<input string>, <separator string>)`

Renvoie une fonction listString.

+++

+++Exemples

`split("A_B_C", "_")`

Renvoie `["A","B","C"]`

Exemple avec un champ d’événement &#39;event.appVersion&#39; avec la valeur : « 20.45.2.3434 »

`split(@event{event.appVersion}, "\\.")`

Renvoie `["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

Renvoie « true » si le deuxième paramètre est un préfixe du premier.

+++Syntaxe

`startWith(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | Chaîne |
| préfixe | chaîne |

+++

+++Signature et type renvoyé

`startWith(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`startWith("Hello World", "Hello")`

Renvoie true.

`startWith("Hello World", "World")`

Renvoie false.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Renvoie « true » si le deuxième paramètre est un préfixe du premier sans tenir compte de la casse.

+++Syntaxe

`startWithIgnoreCase(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | Chaîne |
| préfixe | chaîne |

+++

+++Signature et type renvoyé

`startWithIgnoreCase(<string>,<string>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`startWithIgnoreCase("rowing is great", "RO")`

Renvoie true.

+++

## substr {#substr}

Renvoie la sous-chaîne de l’expression sous forme de chaîne entre l’index de début et l’index de fin. Si l’index de fin n’est pas défini, il se trouve entre l’index de début et la fin.

+++Syntaxe

`substr(<parameters>)`

+++

+++Paramètres

| Paramètre | type |
|-------------|----------|
| string | Chaîne |
| beginIndex | nombre entier |
| endIndex | nombre entier |

+++

+++Signature et type renvoyé

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Renvoie une chaîne.

+++

+++Exemples

`substr("Hello World",6)`

Renvoie « World ».

`substr("Hello World", 0, 5)`

Renvoie « Hello ».

+++

## trim {#trim}

Supprime les espaces de début et de fin.

+++Syntaxe

`trim(<parameters>)`

+++

+++Paramètre

| Paramètre | Type |
|-----------|------------------|
| chaîne | string |

+++

+++Signature et type renvoyé

`trim(<string>)`

Renvoie une chaîne.

+++

+++Exemples

`trim(" Hello ")`

Renvoie « Hello ».

+++

## upper {#upper}

Renvoie une version en majuscules du paramètre.

+++Syntaxe

`upper(<parameters>)`

+++

+++Signature et type renvoyé

`upper(<string>)`

Renvoie une chaîne.

+++

+++Exemples

`upper("b")`

Renvoie « B ».

+++

## uuid {#uuid}

Génère un UUID (Universal Unique Identifier) aléatoire.

+++Syntaxe

`uuid()`

+++

+++Paramètres 

Cette fonction ne requiert pas de paramètres.

+++

+++Signature et type renvoyé

`uuid()`

Renvoie une chaîne.

+++

+++Exemples

`uuid()`

Renvoie « 79e70b7f-8a85-400b-97a1-9f9826121553 »

+++

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente toutes les fonctions de chaîne disponibles dans les expressions de parcours AJO, couvrant la recherche de texte, la comparaison, la transformation, l’extraction, la validation, le remplacement, le fractionnement et la génération d’identifiants uniques.

**Intentions:**
* Concaténer plusieurs chaînes à l’aide de `concat`
* Rechercher une sous-chaîne dans une chaîne (sensible à la casse ou non) à l’aide de `contain` ou `containIgnoreCase`
* Comparer deux chaînes en ignorant la casse à l’aide de `equalIgnoreCase` ou `notEqualIgnoreCase`
* Vérifiez si une chaîne commence ou se termine par un préfixe ou un suffixe spécifique en utilisant `startWith`, `endWith` et leurs variantes non sensibles à la casse
* Extraire une sous-chaîne par position d’index à l’aide de `substr`
* Remplacez la première ou toutes les occurrences d’un modèle dans une chaîne à l’aide de `replace` ou `replaceAll`
* Fractionner une chaîne en une liste de jetons à l’aide d’un séparateur utilisant `split`
* Générer un UUID aléatoire pour les besoins d&#39;identifiant unique à l&#39;aide de `uuid`
* Vérifier si une chaîne est vide ou non à l’aide de `isEmpty` ou `isNotEmpty`

**Glossaire:**
* **RegExp** : modèle d’expression régulière utilisé comme paramètre cible dans `replace`, `replaceAll` et `matchRegExp` - les caractères spéciaux doivent être précédés d’une séquence d’échappement `\\`
* **UUID** : identifiant unique universel — identifiant de chaîne généré de manière aléatoire et renvoyé par `uuid()`
* **substr** : extrait une partie d’une chaîne en spécifiant un index de début et un index de fin facultatif (basé sur zéro)

**Mécanismes de sécurisation :**
* Le paramètre `target` dans `replace` et `replaceAll` est traité comme un RegExp ; les caractères spéciaux (par exemple, `|`, `.`) doivent être précédés d’une séquence d’échappement avec `\\`
* `replace` remplace uniquement la première occurrence correspondante ; utilisez `replaceAll` pour remplacer chaque occurrence
* `isEmpty` renvoie false pour les valeurs nulles (non true) ; null n’est pas considéré comme une chaîne vide
* `indexOf` et `lastIndexOf` renvoient -1 lorsqu’aucune correspondance n’est trouvée
* Les positions d&#39;index de chaîne sont basées sur zéro (le premier caractère est à la position 0)

**Terminologie:**
* Nom canonique : fonctions de chaîne — Acronyme : none — variantes : fonctions de texte, fonctions de manipulation de chaîne
* Synonymes : « contain » = « vérification de la sous-chaîne » ; « split » = « tokenize string » ; « trim » = « strip whitespace »
* Ne pas confondre : « replace » (première occurrence uniquement) ≠ « replaceAll » (toutes les occurrences)
* Ne pas confondre : « indexOf » (position de la première occurrence) ≠ « lastIndexOf » (position de la dernière occurrence)
* Ne les confondez pas : « isEmpty » (true uniquement pour les chaînes vides) ≠ vérification null (isEmpty renvoie false pour null)
* Ne pas confondre : « equalIgnoreCase » (renvoie true si égal ignore la casse) ≠ « notEqualIgnoreCase » (renvoie true si différent ignore la casse)

**FAQ:**
* **Q : Comment puis-je vérifier si une chaîne contient une sous-chaîne indépendamment de la casse ?** — Utilisez `containIgnoreCase("myString", "searchTerm")`, qui renvoie true si le terme de recherche est trouvé dans tous les cas.
* **Q : Quelle est la différence entre `replace` et `replaceAll` ?** — `replace` ne remplace que la première occurrence correspondante ; `replaceAll` remplace chaque occurrence de la chaîne.
* **Q : Pourquoi dois-je échapper le caractère `|` dans `replace` ?** — Le paramètre cible est traité comme une expression régulière ; `|` est un caractère RegExp spécial et doit être placé dans une séquence d&#39;échappement comme `\\|` pour être traité comme une barre verticale.
* **Q : Est-ce que `isEmpty` renvoie la valeur true pour null ?** — Non, `isEmpty` renvoie false pour null ; il renvoie uniquement true pour une `""` de chaîne de longueur nulle.
* **Q : Comment extraire le numéro de version majeur d’une chaîne de version telle que « 20.45.2.3434 » ?** — Utilisez `getListItem(split(@event{event.appVersion}, "\\."), 0)` pour fractionner par point et récupérer le premier élément.
* **Q : Comment générer un identifiant unique dans une expression de parcours ?** — Utilisez `uuid()`, qui renvoie une chaîne UUID générée de manière aléatoire sans paramètres requis.

+++
