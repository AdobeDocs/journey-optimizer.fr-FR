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
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '249'
ht-degree: 100%

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
