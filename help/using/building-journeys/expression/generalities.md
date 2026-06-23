---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxe de l’éditeur d’expression avancé
description: Découvrir la syntaxe utilisée dans l’éditeur d’expression avancé
feature: Journeys
role: Developer
level: Experienced
keywords: syntaxe, éditeur, parcours
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 40%

---

# Syntaxe de l’éditeur d’expression avancé {#syntax}

Les principes de base de la syntaxe lors de l’utilisation de l’[éditeur d’expression avancé](expressionadvanced.md) sont répertoriés ci-dessous. <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Parenthèses et priorité des expressions {#parentheses-and-expression-priority}

Il est possible d’utiliser des parenthèses pour améliorer la lisibilité d’une expression complexe. _(&lt;expression>)_ est l’équivalent de _&lt;expression>_. Il est également possible d’utiliser des parenthèses pour définir l’ordre d’évaluation et l’associativité.

Les expressions sont évaluées de gauche à droite. L’associativité des opérateurs arithmétiques doit être appliquée : les multiplications et les divisions sont prioritaires sur les additions et les soustractions. Pour imposer un ordre spécifique, il est nécessaire d’ajouter des parenthèses afin de délimiter les opérations. Par exemple :

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expression | Évaluation |
|--- |--- |
| `4 + 2 * 10` | <ul><li>« * » a la priorité sur « + » : 2*10 est évalué → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Les parenthèses modifient la priorité : (4 + 2) est évalué → 6</li><li> 6 * 10 → 60</li></ul> |

## Sensible à la casse {#case-sensitivity}

Les règles de respect de la casse sont les suivantes :

* Tous les opérateurs (et, ou, etc.) doivent être écrits en minuscules. Par exemple, _`<expression1>`and`<expression2>`_ est une expression valide, contrairement à l’expression _`<expression1>`AND`<expression2>`_.
* Tous les noms de fonctions sont sensibles à la casse. Par exemple, _inAudience()_ est valide, contrairement à la fonction _INAUDIENCE()_.
* Les références aux champs et les valeurs constantes respectent la casse : ces éléments ne sont pas intégrés au langage (par opposition aux opérateurs et aux fonctions), mais créés par l’utilisateur.

## Type d’expression renvoyé {#returned-expression-type}

Selon le contexte d’utilisation, l’éditeur d’expression peut renvoyer différentes valeurs.

| Utilisation de l’éditeur d’expression avancé | Type d’expression renvoyé attendu |
|--- |--- |
| Condition (condition de source de données, condition de date) | booléen |
| Retardateur personnalisé | dateTimeOnly |
| Mapping des paramètres d’action | Tous |

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page couvre les principales règles de syntaxe de l&#39;éditeur d&#39;expression avancé de Parcours : la priorité de l&#39;opérateur avec des parenthèses, le respect de la casse pour les opérateurs et les fonctions, ainsi que le type de retour attendu pour chaque contexte de l&#39;éditeur.

**Intentions:**

* Contrôle de l’ordre d’évaluation des expressions en plaçant les sous-expressions entre parenthèses
* Écrivez les opérateurs (`and`, `or`, `not`) en minuscules pour éviter les erreurs de syntaxe
* Utilisez des noms de fonction correctement mis en casse (par exemple `inAudience()` non `INAUDIENCE()`).
* Sachez que les conditions doivent renvoyer une valeur booléenne, que les minuteurs personnalisés doivent renvoyer une valeur `dateTimeOnly` et que les mappages des paramètres d’action peuvent renvoyer n’importe quel type

**Glossaire:**

* **Priorité des expressions** : ordre dans lequel les opérateurs sont évalués ; les multiplications et les divisions ont la priorité sur les additions et les soustractions *(spécifiques au produit)*
* **Respect de la casse** : dans l’éditeur avancé, les opérateurs doivent être en minuscules, les noms de fonction sont sensibles à la casse et les références aux champs sont sensibles à la casse lorsqu’elles sont créées par l’utilisateur *(spécifique au produit)*
* **dateTimeOnly** : type de retour requis pour les expressions de minuteur personnalisées (activité d’attente) ; représente une date-heure sans *de fuseau horaire (spécifique au produit)*

**Mécanismes de sécurisation :**

* Opérateurs (`and`, `or`, `not`, etc.) doit être écrit en minuscules — les variantes en majuscules ne sont pas valides
* Tous les noms de fonction sont sensibles à la casse — `inAudience()` est valide, mais `INAUDIENCE()` ne l’est pas
* L’arithmétique suit la priorité standard : `*` et `/` évaluent avant `+` et `-` ; utilisez des parenthèses pour remplacer.
* Les conditions renvoient toujours une valeur booléenne ; les minuteries personnalisées renvoient toujours `dateTimeOnly`

**Terminologie:**

* Nom canonique : Syntaxe de l’éditeur d’expression avancé — Acronyme : none — variantes : syntaxe d’expression, syntaxe de l’éditeur
* Synonymes : « priorité d’expression » = « priorité de l’opérateur » ; « parenthèses » = « crochets » (dans le contexte de l’expression)
* Ne pas confondre : respect de la casse pour les opérateurs (les opérateurs doivent être en minuscules) ≠ respect de la casse pour les références de champ (les noms de champ sont créés par l’utilisateur et respectent la casse tels qu’ils sont écrits)

**FAQ:**

* **Q : Est-ce que `4 + 2 * 10` évaluez à 60 ou 24 ?** — Il évalue à 24 car `*` a la priorité sur `+` ; utilisez `(4 + 2) * 10` pour obtenir 60.
* **Q : Puis-je écrire des `AND` en majuscules dans une expression ?** — Non ; tous les opérateurs doivent être en minuscules (`and`, `or`, `not`).
* **Q : Les noms de fonctions sont-ils sensibles à la casse ?** — Oui ; `inAudience()` est valide, mais `INAUDIENCE()` ne l&#39;est pas.
* **Q : Quel type une expression de condition doit-elle renvoyer ?** — Booléen.
* **Q : Quel type de retour est requis pour une expression du minuteur d’activité d’attente personnalisée ?** — `dateTimeOnly`.

+++
