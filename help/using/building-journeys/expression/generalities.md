---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxe
description: En savoir plus sur l’éditeur d’expression avancé
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Syntaxe de l’éditeur d’expression avancé {#syntax}

## Parenthèses et priorité des expressions{#parentheses-and-expression-priority}

Il est possible d’utiliser des parenthèses pour rendre une expression complexe plus lisible. _(&lt;expression>)_ est l’équivalent de _&lt;expression>_. Vous pouvez également utiliser des parenthèses pour définir l’ordre d’évaluation et l’associativité.

Les expressions seront évaluées de gauche à droite. L&#39;associativité des opérateurs arithmétiques doit être appliquée : les multiplications et les divisions sont prioritaires sur les ajouts et les soustractions. Pour imposer un ordre spécifique, des parenthèses doivent être ajoutées pour délimiter les opérations. Par exemple :

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expression | Évaluation |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&quot;*&quot; a la priorité sur &quot;+&quot; : 2 * 10 est évalué → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Les parenthèses modifient la priorité : (4 + 2) est évalué → 6</li><li> 6 * 10 → 60</li></ul> |

## Respect de la casse{#case-sensitivity}

Voici les différentes règles de respect de la casse :

* Tous les opérateurs (et, ou, etc.) doit être écrit en minuscules. Par exemple, _`<expression1>`et`<expression2>`_ est une expression valide, tandis que l’expression _`<expression1>`ET`<expression2>`_ ne l’est pas.
* Tous les noms de fonction sont sensibles à la casse. Par exemple, _inSegment()_ est valide, tandis que la fonction _INSEGMENT()_ ne l’est pas.
* Les références de champ et les valeurs constantes sont sensibles à la casse : ne sont pas des éléments intégrés du langage (par opposition aux opérateurs et aux fonctions), ils sont créés par l’utilisateur final.

## Type d’expression renvoyé{#returned-expression-type}

Selon le contexte d’utilisation, l’éditeur d’expression peut renvoyer différentes valeurs.

| Utilisation de l’éditeur d’expression avancé | Type d’expression renvoyé attendu |
|--- |--- |
| Condition (condition de source de données, condition de date) | boolean |
| Timer personnalisé | dateTimeOnly |
| Mappage des paramètres d’action | Quelconque |
