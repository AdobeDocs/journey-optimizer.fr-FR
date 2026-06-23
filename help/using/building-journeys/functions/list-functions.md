---
product: journey optimizer
title: Fonctions de liste
description: En savoir plus sur les fonctions de liste
feature: Journeys
role: Developer
level: Experienced
keywords: liste, fonctions, expression, parcours, tableau, collection
version: Journey Orchestration
exl-id: b17245ba-4ffa-4f5b-914e-4c0972e9c7c4
TQID: https://experienceleague.adobe.com/XWWixhfBVKw-kdgO4WPWrtiIqA8sFt0ql0IVZ-2QsUI
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
source-wordcount: 1642
ht-degree: 70%

---

# Fonctions de liste {#list-functions}

Les fonctions de liste vous permettent de manipuler et d’utiliser des collections de valeurs dans vos expressions de parcours. Ces fonctions sont essentielles pour le filtrage, le tri, la transformation et l’analyse des tableaux et des listes dans vos parcours clients.

Utilisez des fonctions de liste lorsque vous devez :

* filtrer et extraire des éléments spécifiques des collections en fonction de critères ([filter](#filter), [getListItem](#getListItem)) ;
* trier et organiser les éléments de liste par ordre croissant ou décroissant ([sort](#sort)) ;
* Supprime les doublons et obtenir des valeurs uniques des listes ([distinct](#distinct), [distinctWithNull](#distinctWithNull))
* vérifie si des valeurs existent dans les collections ([in](#in)) ;
* limiter le nombre d’éléments renvoyés par une liste ([limit](#limit)) ;
* Obtenir la taille d’une liste ([listSize](#listSize)) ou transformer des listes en différents formats ([serializeList](#serializeList))
* effectuer des opérations définies telles que la recherche d’éléments communs entre les listes ([intersect](#intersect)).

Les fonctions de liste fournissent des outils puissants pour travailler avec des structures de données complexes, ce qui permet une manipulation de données sophistiquée et une logique conditionnelle basée sur les contenus de collection.

## distinct {#distinct}

Renvoie les valeurs ou objets distincts d’une liste donnée. Les entrées « null » sont ignorées.

+++Syntaxe

`distinct(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | Chaîne | Ce paramètre est facultatif et uniquement pour listObject. Si le paramètre n’est pas fourni, un objet est considéré comme dupliqué si tous les attributs ont les mêmes valeurs. Dans le cas contraire, un objet est considéré comme dupliqué si l’attribut donné a la même valeur. |

+++

+++Signatures et types renvoyés

`distinct(<listInteger>)`

Renvoie une liste de nombres entiers.

`distinct(<listDecimal>)`

Renvoie une liste de nombres décimaux.

`distinct(<listString>)`

Renvoie une liste de chaînes.

`distinct(<listDateTimeOnly>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`distinct(<listDateTime>)`

Renvoie une liste de dates et heures.

`distinct(<listDateOnly>)`

Renvoie une liste de dates.

`distinct(<listBoolean>)`

Renvoie une liste de valeurs booléennes.

`distinct(<listDuration>)`

Renvoie une liste de durées.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Renvoie une liste d’objets.

+++

+++Exemples

`distinct([10,2,10,null])`

Renvoie `[10, 2]`.

+++

## distinctWithNull {#distinctWithNull}

Renvoie les valeurs ou objets distincts d’une liste donnée. Si la liste comporte au moins une entrée « null », une entrée « null » est présente dans la liste renvoyée.

+++Syntaxe

`distinctWithNull(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Liste à traiter. |

+++

+++Signatures et types renvoyés

`distinctWithNull(<listInteger>)`

Renvoie une liste de nombres entiers.

`distinctWithNull(<listDecimal>)`

Renvoie une liste de nombres décimaux.

`distinctWithNull(<listString>)`

Renvoie une liste de chaînes.

`distinctWithNull(<listDateTimeOnly>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`distinctWithNull(<listDateTime>)`

Renvoie une liste de dates et heures.

`distinctWithNull(<listDateOnly>)`

Renvoie une liste de dates.

`distinctWithNull(<listBoolean>)`

Renvoie une liste de valeurs booléennes.

`distinctWithNull(<listDuration>)`

Renvoie une liste de durées.

+++

+++Exemples

`distinctWithNull([10,2,10,null])`

Renvoie [10, 2, null]

+++

**Remarque :** le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## filter {#filter}

Renvoie une valeur listObject avec les objets dont lʼattribut clé correspond à lʼune des valeurs clés données.

+++Syntaxe

`filter(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToFilter | listObject | liste dʼobjects à filtrer. Il doit être une référence de champ. |
| keyAttributeName | Chaîne | nom de lʼattribut dans les objets de la liste donnée, utilisé comme clé pour le filtrage |
| keyValueList | list | tableau de valeurs clés pour le filtrage |

+++

+++Signatures et types renvoyés

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Renvoie une valeur listObject.

+++

+++Exemples

Voici un exemple dʼune payload transmise dans un événement entrant « myevent » :

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Vous pouvez utiliser lʼexpression suivante :

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Renvoie une valeur listObject contenant les deux objets avec « product2 » et « product3 » comme id.

+++

## getListItem {#getListItem}

Renvoie l’élément de la liste à l’index donné.

+++Syntaxe

`getListItem(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | entier |

+++

+++Signatures et type renvoyé

`getListItem(<listInteger>,<index>)`

Renvoie un entier.

`getListItem(<listDecimal>,<index>)`

Renvoie une valeur décimale.

`getListItem(<listString>,<index>)`

Renvoie une chaîne.

`getListItem(<listDateTimeOnly>,<index>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

`getListItem(<listDateTime>,<index>)`

Renvoie une date et une heure.

`getListItem(<listDateOnly>,<index>)`

Renvoie une liste de dates.

`getListItem(<listBoolean>,<index>)`

Renvoie une valeur booléenne.

`getListItem(<listDuration>,<index>)`

Renvoie une durée.

+++

+++Exemples

`getListItem([10, 2, 3], 1)`

Renvoie « 2 »

`getListItem(["A", "B", "C"], 2)`

Renvoie « C »

Exemples avec un champ d’événement &#39;event.appVersion&#39; avec la valeur : « 20.45.2.3434 »

`split(@event{event.appVersion}, "\\.")`

Renvoie `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Renvoie « 20 »

+++

## in {#in}

Vérifie si la valeur du premier argument figure dans la liste. La vérification est effectuée par l’intermédiaire d’un opérateur Equal sur chaque valeur d’argument. Elle renvoie true si la valeur de l’argument est trouvée, false dans le cas contraire.

Le type de l’`<expression>` doit correspondre aux éléments de la liste. Pour mémoire, les types d’éléments de la liste doivent correspondre les uns aux autres.

+++Syntaxe

`in(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| Chaîne | Chaîne |
| Booléen | Booléen |
| Nombre entier | Nombre entier |
| Décimal | Décimal |
| Durée | Durée |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |

+++

+++Signature et type renvoyé

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Renvoie une valeur booléenne.

+++

+++Exemples

`in(4,[4,5,3,4])`

Renvoie true.

`in(8,[4,5,3,4])`

Renvoie false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

Renvoie les valeurs communes dans les deux listes dʼentrée. Si lʼune des deux listes est nulle, elle renvoie une liste vide.

+++Syntaxe

`intersect(<parameters>)`

+++

+++Paramètres

| Paramètre | Type |
|-----------|------------------|
| list 1 | list |
| list 2 | list |

+++

+++Signatures et types renvoyés

`intersect(listString,listString)` : listString

`intersect(listDecimal,listDecimal)` : listDecimal

`intersect(listInteger,listInteger)` : listInteger

`intersect(listDateTime,listDateTime)` : listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)` : listDateTimeOnly

`intersect(listDateOnly,listDateOnly)` : listDateOnly

`intersect(listDuration,listDuration)` : listDuration

`intersect(listBoolean,listBoolean)` : listBoolean

Renvoie une liste.

+++

+++Exemples

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Renvoie [« sports », « news »]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Renvoie les éléments communs entre les attributs du profil et la liste de catégories donnée.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Renvoie les éléments communs entre les attributs du profil et le champ dʼévénement donné.

+++

## limit {#limit}

Renvoie les N premiers ou derniers éléments d’une liste.

+++Syntaxe

`limit(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à prendre en compte. Pour listObject, il doit s’agir d’une référence de champ. |
| numberOfItems | Entier | Nombre d’éléments à renvoyer à partir de la liste donnée. |
| firstOrLastItems | Booléen | Ce paramètre est facultatif (true par défaut). true renvoie les premiers éléments. false renvoie les derniers éléments. |

+++

+++Signature et type renvoyé

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

Renvoie une liste de chaînes.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

Renvoie une liste de nombres entiers.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

Renvoie une liste de nombres décimaux.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

Renvoie une liste de valeurs booléennes.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

Renvoie une liste de dates.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

Renvoie une liste de dates et heures.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

Renvoie une liste de durées.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

Renvoie une liste d’objets.

+++

+++Exemples

`limit(["A", "B", "C", "D", "E"], 3)`

Renvoie `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Renvoie `["C","D","E"]`.

+++

## listSize {#listSize}

Compte le nombre d’éléments dans la liste.

+++Syntaxe

`listSize(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. Un listObject ne peut pas contenir d’objet null. |

+++

+++Signatures et type renvoyé

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Renvoie un nombre entier.

`listSize(<listObject>)`

+++

+++Exemples

`listSize([10,2,3])`

Renvoie 3.

`listSize(@event{my_event.productListItems})`

Renvoie le nombre d’objets dans le tableau d’objets donné (type listObject).

+++

## serializeList {#serializeList}

Convertit une liste donnée (tout type sauf listObject) en chaîne.

+++Syntaxe

`serializeList(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Liste à convertir en chaîne. |
| séparateur | chaîne | Séparateur entre chaque élément de liste dans la chaîne de sortie. |
| addQuotes | booléen | Ce paramètre indique si chaque élément de la chaîne de sortie doit inclure des guillemets (true) ou non (false). |

+++

+++Signature et type renvoyé

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Renvoie une chaîne.

+++

+++Exemples

`serializeList(["Hello","World"], " ", false)`

Renvoie « Hello World ».

`serializeList(["Hello", "World"], ",", true)`

Renvoie « Hello », « World ».

+++

## sort {#sort}

Trie une liste de valeurs ou d’objets dans l’ordre naturel.

+++Syntaxe

`sort(<parameters>)`

+++

+++Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à trier. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | Chaîne | Ce paramètre est uniquement destiné à listObject. Le nom de lʼattribut dans les objets de la liste donnée, utilisé comme clé pour le tri. |
| sortingOrder | Booléen | ascendant (true) ou descendant (false) |

+++

+++Signature et type renvoyé

`sort(<listInteger>,<boolean>)`

Renvoie une liste de nombres entiers.

`sort(<listDecimal>,<boolean>)`

Renvoie une liste de nombres décimaux.

`sort(<listString>,<boolean>)`

Renvoie une liste de chaînes.

`sort(<listDateTimeOnly>,<boolean>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`sort(<listDateTime>,<boolean>)`

Renvoie une liste de dates et heures.

`sort(<listDateOnly>,<boolean>)`

Renvoie une liste de dates.

`sort(<listBoolean>,<boolean>)`

Renvoie une liste de valeurs booléennes.

`sort(<listObject>,<string>,<boolean>)`

Renvoie une liste d’objets.

+++

+++Exemples

`sort(["A", "C", "B"], true)`

Renvoie `["A","B","C"]`.

`sort([1, 3, 2], false)`

Renvoie `[3, 2, 1]`.

`sort(@event{my_event.productListItems}, "SKU", true)`

Renvoie une valeur listObject classée par attribut SKU (ordre ascendant).

+++

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente toutes les fonctions de liste disponibles dans les expressions de parcours AJO, couvrant la manière de filtrer, trier, dédupliquer, vérifier l’appartenance, limiter, sérialiser et rechercher les intersections des listes et des tableaux.

**Intentions:**
* Supprimer les valeurs en double d&#39;une liste à l&#39;aide de `distinct` (en ignorant les nulls) ou `distinctWithNull` (en conservant les nulls)
* Filtrez un listObject pour renvoyer uniquement les objets correspondant à des valeurs de clé spécifiques à l’aide de `filter`
* Récupérer un élément à un index spécifique d’une liste à l’aide de `getListItem`
* Vérifier si une valeur existe dans une liste à l’aide de `in`
* Recherche d’éléments communs à deux listes à l’aide de `intersect`
* Renvoyer les N premiers ou derniers éléments d’une liste à l’aide de `limit`
* Compter le nombre total d’éléments dans une liste à l’aide de `listSize`
* Convertir une liste en chaîne délimitée à l’aide de `serializeList`
* Trier une liste par ordre croissant ou décroissant à l’aide de `sort`

**Glossaire:**
* **listObject** : liste d’objets complexes qui doivent être une référence de champ ; ne peut pas contenir d’objets nuls *(spécifiques au produit)*
* **keyAttributeName** : paramètre de chaîne facultatif utilisé avec `distinct`, `filter` et `sort` pour identifier l’attribut d’objet à utiliser pour la déduplication, le filtrage ou le tri des *(spécifique au produit)*
* **intersect** : opération set renvoyant uniquement les éléments présents dans les deux listes d’entrée

**Mécanismes de sécurisation :**
* `distinctWithNull` ne prend pas en charge le type de paramètre `<listObject>`
* `filter` nécessite que le paramètre listObject soit une référence de champ, et non un littéral intégré
* `listSize` sur un listObject nécessite que la liste soit une référence de champ ; un listObject ne peut pas contenir d’objets null
* `serializeList` ne prend pas en charge le type de `listObject`

**Terminologie:**
* Nom canonique : Fonctions de liste — Acronyme : none — variantes : fonctions de collection, fonctions de tableau
* Synonymes : « listSize » = « count list elements » ; « serializeList » = « join list to string »
* Ne pas confondre : « distinct » (ignore les nulls) ≠ « distinctWithNull » (conserve la valeur null comme valeur distincte)
* Ne les confondez pas : « limit » avec le troisième paramètre `true` (renvoie les N premiers éléments) ≠ « limit » avec `false` (renvoie les N derniers éléments).
* Ne pas confondre : « intersect » (éléments communs entre deux listes) ≠ « filter » (éléments correspondant à des valeurs de clé spécifiques)

**FAQ:**
* **Q : Comment puis-je obtenir les 3 premiers éléments d&#39;une liste ?** — Utilisez `limit(myList, 3)` ou `limit(myList, 3, true)` ; par défaut, les premiers éléments sont renvoyés.
* **Q : Comment puis-je obtenir les 3 derniers éléments d&#39;une liste ?** — Utiliser `limit(myList, 3, false)`.
* **Q : Quelle est la différence entre `distinct` et `distinctWithNull` ?** — `distinct` ignore les valeurs nulles et les exclut du résultat ; `distinctWithNull` traite les valeurs nulles comme une valeur distincte et inclut une entrée nulle si des valeurs nulles sont présentes.
* **Q : Puis-je filtrer une liste de chaînes avec des `filter` ?** — Non, `filter` fonctionne uniquement sur `listObject` ; pour les listes scalaires, utilisez `in` ou `distinct` pour la déduplication.
* **Q : Comment puis-je vérifier si une valeur se trouve dans une liste ?** — Utilisez `in(value, myList)`, qui renvoie true si la valeur figure dans la liste.
* **Q : Puis-je trier un listObject en fonction d’un attribut spécifique ?** — Oui, utilisez `sort(@event{...}, "attributeName", true)` où le deuxième paramètre est le nom de l&#39;attribut et le troisième est le sens du tri (true = croissant).

+++
