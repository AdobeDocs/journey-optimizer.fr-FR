---
product: journey optimizer
title: Fonctions mathématiques
description: En savoir plus sur les fonctions mathématiques
feature: Journeys
role: Developer
level: Experienced
keywords: mathématiques, fonctions, expression, parcours, calcul, nombre
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: ht
source-wordcount: '156'
ht-degree: 100%

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
* Entier

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

