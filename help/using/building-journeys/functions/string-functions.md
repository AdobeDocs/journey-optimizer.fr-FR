---
product: journey optimizer
title: Fonctions de chaîne
description: Découvrez les fonctions de chaîne
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
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1140
ht-degree: 0%

---

# Fonctions de chaîne {#string-functions}

Les fonctions de chaîne vous permettent de manipuler et d’utiliser des valeurs de texte dans vos expressions de parcours. Ces fonctions sont essentielles pour le traitement de texte, la validation, la transformation et l’analyse dans vos parcours clients.

Utilisez des fonctions de chaîne lorsque vous devez :

* Concaténer et combiner plusieurs valeurs de texte ([concat](#concat))
* Recherchez des modèles de texte ou des sous-chaînes spécifiques ([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp))
* Comparer des chaînes avec une correspondance sensible à la casse ou insensible à la casse ([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase))
* Vérifiez que la chaîne commence et se termine ([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase)).
* Extraire des parties de texte à l’aide d’opérations de sous-chaîne ([substr](#substr))
* Transformer le texte en majuscules ou en minuscules ([majuscule](#upper), [inférieure](#lower), [rognage](#trim))
* Vérifiez si les chaînes sont vides ou contiennent des valeurs spécifiques ([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty))
* Remplacer des modèles de texte par de nouvelles valeurs ([replace](#replace), [replaceAll](#replaceAll))
* Diviser les chaînes en tableaux pour un traitement ultérieur ([division](#split))
* Obtenir la longueur de la chaîne ([length](#length)) ou générer les identifiants uniques ([uuid](#uuid))

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
| chaîne | chaîne |

+++

+++Signature et type renvoyé

`concat(<string>,<string>)`

`concat(<listString>)`

Renvoie une chaîne.

+++

+++Exemples

`concat("Hello","World")`

Renvoie « HelloWorld ».

`concat(["Hello"," ","World"])`

Renvoie « Hello World ».

+++

## contain {#contain}

Vérifie si la deuxième chaîne d&#39;arguments est contenue dans la première chaîne d&#39;arguments.

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

Vérifie si la deuxième chaîne d&#39;arguments est contenue dans la première chaîne d&#39;arguments, sans prendre en compte la casse.

+++Syntaxe

`containIgnoreCase(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
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

Renvoie vrai si le deuxième paramètre est un suffixe du premier.

+++Syntaxe

`endWith(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
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

Vérifie si la première chaîne d’arguments se termine par une chaîne spécifique (deuxième chaîne d’arguments), en ne tenant pas compte de la casse.

+++Syntaxe

`endWithIgnoreCase(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |
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

Compare la première chaîne d’arguments à la seconde chaîne d’arguments, en ignorant les considérations de casse.

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

Renvoie la position (dans le premier argument) de la première occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

+++Syntaxe

`indexOf(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne | String |
| valeur spécifiée | String |

+++

+++Signature et type renvoyé

`indexOf(<string>,<string>)`

Renvoie un entier.

+++

+++Exemples

`indexOf("Hello", "l")`

Renvoie 2.

Explication :

Dans « Hello », la première occurrence de « l » est à la position 2.

+++

## isEmpty {#isEmpty}

Renvoie vrai si la chaîne du paramètre ne comporte aucun caractère.

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

Renvoie true si la chaîne du paramètre n’est pas vide.

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
| chaîne | String |
| valeur spécifiée | String |

+++

+++Signature et type renvoyé

`lastIndexOf(<string>,<string>)`

Renvoie un entier.

+++

+++Exemples

`lastIndexOf("Hello", "l")`

Renvoie 3.

Explication :

Dans « Hello », la dernière occurrence de « l » est à la position 3.

+++

## longueur {#length}

Renvoie le nombre de caractères de l’expression de chaîne dans le paramètre.

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

Renvoie une version en minuscules du paramètre .

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

Renvoie « a ».

+++

## matchRegExp {#matchRegExp}

Renvoie vrai si la chaîne du premier paramètre correspond à l’expression régulière du deuxième paramètre. Pour plus d’informations, voir [cette page](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Syntaxe

`matchRegExp(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|--- |--- |
| chaîne | chaîne |
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

Vérifiez si la première chaîne d’arguments et la deuxième chaîne d’arguments sont différentes, en ignorant les considérations de casse.

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

Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

+++Syntaxe

`replace(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|--------------|
| socle | chaîne |
| cible | string (RegExp) |
| substitution | chaîne |

+++

+++Signature et type renvoyé

`replace(<base>,<target>,<replacement>)`

Renvoie une chaîne.

+++

+++Exemples

`replace("Hello World", "l", "x")`

Renvoie « Hexlo World ».

**Exemple avec RegExp:**

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Voici un exemple :

* chaîne à évaluer : `|OFFER_A|OFFER_B`
* fourni par un attribut de profil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Chaîne à remplacer : `|OFFER_A`
* Chaîne remplacée par : `''`
* Vous devez ajouter `\\` avant le caractère `|`.

L’expression est :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La chaîne renvoyée est : `|OFFER_B`

Vous pouvez également créer la chaîne à remplacer à partir d’un attribut donné :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Remplace toutes les occurrences correspondant à la chaîne cible par la chaîne de remplacement dans la chaîne de base.

Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

+++Syntaxe

`replaceAll(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|--------------|
| socle | chaîne |
| cible | string (RegExp) |
| substitution | chaîne |

+++

+++Signature et type renvoyé

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Renvoie une chaîne.

+++

+++Exemples

`replaceAll("Hello World", "l", "x")`

Renvoie « Hexxo Word ».

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Reportez-vous à l’exemple de la fonction [replace](#replace).

+++

## scinder {#split}

Divise la première chaîne d’arguments par une chaîne de séparation (la deuxième chaîne d’arguments, qui peut être une expression régulière) afin de produire une liste de chaînes (jetons).

+++Syntaxe

`split(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| chaîne d’entrée | chaîne |
| chaîne de séparation | chaîne |

+++

+++Signatures et type renvoyé

`split(<input string>, <separator string>)`

Renvoie une valeur listString.

+++

+++Exemples

`split("A_B_C", "_")`

Renvoie `["A","B","C"]`

Exemple avec un champ d’événement « event.appVersion » avec la valeur : « 20.45.2.3434 »

`split(@event{event.appVersion}, "\\.")`

Renvoie `["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

Renvoie vrai si le deuxième paramètre est un préfixe du premier.

+++Syntaxe

`startWith(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | chaîne |
| préfixe | chaîne |

+++

+++Signature et type renvoyé

`startWith(<string>,<string>)`

Renvoyer une valeur booléenne.

+++

+++Exemples

`startWith("Hello World", "Hello")`

Renvoie true.

`startWith("Hello World", "World")`

Renvoie false.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Renvoie vrai si le deuxième paramètre est un préfixe du premier sans tenir compte de la casse.

+++Syntaxe

`startWithIgnoreCase(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-------------|--------|
| chaîne | chaîne |
| préfixe | chaîne |

+++

+++Signature et type renvoyé

`startWithIgnoreCase(<string>,<string>)`

Renvoyer une valeur booléenne.

+++

+++Exemples

`startWithIgnoreCase("rowing is great", "RO")`

Renvoie true.

+++

## substr {#substr}

Renvoie la sous-chaîne de l’expression de chaîne entre l’index de début et l’index de fin. Si l’index de fin n’est pas défini, il se trouve entre l’index de début et la fin.

+++Syntaxe

`substr(<parameters>)`

+++

+++Paramètres

| Paramètre | type |
|-------------|----------|
| chaîne | chaîne |
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

Renvoie « World ».

`substr("Hello World", 0, 5)`

Renvoie « Hello ».

+++

## rogner {#trim}

Supprime les espaces de début et de fin.

+++Syntaxe

`trim(<parameters>)`

+++

+++Paramètre

| Paramètre | Type |
|-----------|------------------|
| chaîne | chaîne |

+++

+++Signature et type renvoyé

`trim(<string>)`

Renvoie une chaîne.

+++

+++Exemples

`trim(" Hello ")`

Renvoie « Hello ».

+++

## upper {#upper}

Renvoie une version en majuscules du paramètre .

+++Syntaxe

`upper(<parameters>)`

+++

+++Signature et type renvoyé

`upper(<string>)`

Renvoie une chaîne.

+++

+++Exemples

`upper("b")`

Renvoie « B ».

+++

## uuid {#uuid}

Génère un UUID aléatoire (Universal Unique IDentifier).

+++Syntaxe

`uuid()`

+++

+++Paramètres 

Cette fonction ne nécessite aucun paramètre.

+++

+++Signature et type renvoyé

`uuid()`

Renvoie une chaîne.

+++

+++Exemples

`uuid()`

Renvoie « 79e70b7f-8a85-400b-97a1-9f9826121553 ».

+++
