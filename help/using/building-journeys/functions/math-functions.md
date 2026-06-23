---
product: journey optimizer
title: Fonctions mathématiques
description: En savoir plus sur les fonctions mathématiques
feature: Journeys
role: Developer
level: Experienced
keywords: mathématiques, fonctions, expression, parcours, calcul, nombre
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 32%

---

# Fonctions mathématiques {#math-functions}

Les fonctions mathématiques fournissent des opérations mathématiques essentielles pour les calculs numériques dans vos expressions de parcours. Ces fonctions vous permettent d’effectuer des calculs numériques et des transformations précis sur vos données.

Utilisez des fonctions mathématiques lorsque vous devez :

* générer des valeurs aléatoires pour les tests, l’échantillonnage ou la randomisation ([random](#random)) ;
* arrondir les nombres décimaux à l’entier le plus proche pour une présentation des données plus épurée ([round](#round)) ;
* effectuer des calculs mathématiques sur des champs numériques ;
* transformer les valeurs numériques pour la logique métier et la prise de décision.

Les fonctions mathématiques gèrent les types décimaux et entiers, et gèrent automatiquement les conversions de type pour garantir des résultats précis dans vos expressions de parcours.

## random {#random}

Génère un nombre aléatoire compris entre 0 et 1.

+++Syntaxe

`random()`

+++

+++Signature et type renvoyé

`random()`

Renvoie une valeur décimale.

+++

## round {#round}

Renvoie l’entier le plus proche de l’argument avec des arrondis tendant vers l’infini positif.

+++Syntaxe

`round(<parameters>)`

+++

+++Paramètres

* décimal
* entier

+++

+++Signatures et type renvoyé

`round(<decimal>)`

`round(<integer>)`

Renvoie un nombre entier.

+++

+++Exemples

`round(3.14)`

Renvoie 3.

`round(3.54)`

Renvoie 4.

`round(-3.14)`

Renvoie -3.

`round(3)`

Renvoie 3.

+++

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente les deux fonctions mathématiques disponibles dans les expressions de parcours AJO : `random` pour générer une décimale aléatoire comprise entre 0 et 1, et `round` pour arrondir une décimale ou un entier à l’entier le plus proche.

**Intentions:**
* Générez une valeur décimale aléatoire comprise entre 0 et 1 pour la logique d’échantillonnage ou de randomisation à l’aide de `random`
* Arrondissez un nombre décimal à l’entier le plus proche à l’aide de `round`.
* Appliquer l&#39;arrondi dans la logique métier où les nombres entiers sont requis des calculs décimaux

**Glossaire:**
* **random** : fonction qui renvoie une valeur décimale pseudo-aléatoire de 0 (inclus) à 1 (exclusif) *(spécifique au produit)*
* **round** : fonction qui renvoie l’entier le plus proche de l’entrée, avec des demi-valeurs arrondies vers l’infini positif

**Mécanismes de sécurisation :**
* `random()` ne prend aucun paramètre
* `round` accepte une entrée décimale ou entière et renvoie toujours un entier
* Les liens en `round` sont résolus en arrondissant vers l&#39;infini positif (p. ex., de 3,5 à 4, de -3,5 à -3)

**Terminologie:**
* Nom canonique : Fonctions mathématiques — Acronyme : aucune — variantes : fonctions mathématiques, fonctions numériques
* Synonymes : « round » = « round to closer integer »
* Ne pas confondre : « round » (arrondit à l’entier le plus proche) ≠ fonctions de conversion telles que `toInteger` (tronque la partie décimale sans arrondi)

**FAQ:**
* **Q : Qu&#39;est-ce que `random()` retourne ?** — Renvoie un nombre décimal aléatoire compris entre 0 et 1.
* **Q : Comment gère-t-`round` les nombres négatifs ?** — Il arrondit vers l&#39;infini positif, donc `round(-3.14)` renvoie -3 et `round(-3.54)` renvoie également -3 (entier le plus proche vers l&#39;infini positif).
* **Q : Quelle est la différence entre `round` et `toInteger` ?** — `round` arrondit à l&#39;entier le plus proche (3,7 devient 4), tandis que `toInteger` tronque la partie décimale sans arrondir (3,7 devient 3).
* **Q : Est-ce que `random` prend des paramètres ?** — Non, `random()` ne nécessite aucun paramètre et renvoie toujours une décimale entre 0 et 1.

+++
