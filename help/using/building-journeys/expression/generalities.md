---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxe
description: En savoir plus sur lʼéditeur d’expression avancé
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: syntaxe, éditeur, parcours
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '231'
ht-degree: 100%

---

# Syntaxe de l’éditeur d’expression avancé {#syntax}

## Parenthèses et priorité des expressions{#parentheses-and-expression-priority}

Il est possible d’utiliser des parenthèses pour améliorer la lisibilité d’une expression complexe. _(&lt;expression>)_ est l’équivalent de _&lt;expression>_. Il est également possible d’utiliser des parenthèses pour définir l’ordre d’évaluation et l’associativité.

Les expressions sont évaluées de gauche à droite. L’associativité des opérateurs arithmétiques doit être appliquée : les multiplications et les divisions sont prioritaires sur les additions et les soustractions. Pour imposer un ordre spécifique, il est nécessaire d’ajouter des parenthèses afin de délimiter les opérations. Par exemple :

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expression | Évaluation |
|--- |--- |
| `4 + 2 * 10` | <ul><li>« * » a la priorité sur « + » : 2 * 10 est évalué → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Les parenthèses modifient la priorité : (4 + 2) est évalué → 6</li><li> 6 * 10 → 60</li></ul> |

## Sensible à la casse{#case-sensitivity}

Les règles de respect de la casse sont les suivantes :

* Tous les opérateurs (and, or, etc.) doivent être en minuscules. Par exemple, _`<expression1>`and`<expression2>`_ est une expression valide, contrairement à l’expression _`<expression1>`AND`<expression2>`_.
* Tous les noms de fonctions sont sensibles à la casse. Par exemple, _inAudience()_ est valide, contrairement à la fonction _INAUDIENCE()_.
* Les références aux champs et les valeurs constantes respectent la casse : ces éléments ne sont pas intégrés au langage (par opposition aux opérateurs et aux fonctions), mais créés par l’utilisateur.

## Type d’expression renvoyé{#returned-expression-type}

Selon le contexte d’utilisation, l’éditeur d’expression peut renvoyer différentes valeurs.

| Utilisation de l’éditeur d’expression avancé | Type d’expression renvoyé attendu |
|--- |--- |
| Condition (condition de source de données, condition de date) | booléen |
| Retardateur personnalisé | dateTimeOnly |
| Mappage des paramètres d’action | Tous |
