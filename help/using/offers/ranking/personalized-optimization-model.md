---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Modèle d’optimisation personnalisé
description: En savoir plus sur les modèles d’optimisation personnalisée
badge: label="Hérité" type="Informative"
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: c73b3092-e96d-4957-88e6-500e99542782
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 100%

---

# Modèle d’optimisation personnalisé {#personalized-optimization-model}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

## Vue d’ensemble {#overview}

En tirant parti des technologies de pointe en matière de machine learning et de deep learning supervisés, l’optimisation personnalisée permet à une personne professionnelle (spécialiste marketing) de définir des objectifs commerciaux et d’utiliser ses données clients pour entraîner des modèles orientés métier afin de fournir des offres personnalisées et d’optimiser les KPI.

![](../../rn/assets/do-not-localize/ai-ranking.gif)

## Exigences relatives aux jeux de données

Pour entraîner un modèle d’optimisation personnalisé, le jeu de données doit répondre aux exigences minimales suivantes :

* Au moins 2 offres du jeu de données doivent avoir au moins 250 événements d’affichage et 25 événements de succès (par exemple, des clics ou des conversions) au cours des 30 derniers jours.
* Les offres comportant moins de 250 affichages et/ou 25 événements de succès au cours des 30 derniers jours peuvent être incluses dans le trafic personnalisé, mais sont traitées par le modèle de personnalisation comme performantes au niveau de l’offre ayant obtenu le pire score jusqu’à ce qu’elles dépassent ce seuil.
* Les offres comportant moins de 250 affichages et/ou 25 événements de succès au cours des 30 derniers jours peuvent toujours être incluses dans le trafic d’exploration.

Jusqu’au premier entraînement d’un modèle d’optimisation personnalisé, les offres d’une stratégie de sélection utilisant un modèle d’optimisation personnalisé sont diffusées de manière aléatoire.

## Principales hypothèses et limites du modèle {#key}

Afin de tirer pleinement parti de l’utilisation de l’optimisation personnalisée, il existe certaines hypothèses et limites clés à connaître.

* **Les offres sont suffisamment différentes pour que les utilisateurs aient des préférences différentes parmi les offres prises en compte**. Si les offres sont trop similaires, le modèle obtenu a moins d’impact, car les réponses semblent aléatoires.
Par exemple, si une banque propose deux offres de cartes de crédit dont la seule différence est la couleur, la carte conseillée n’a pas d’importance. Par contre, si chaque carte comporte des conditions différentes, cela explique pourquoi certains clients en choisissent une et fournit suffisamment de différence entre les offres pour créer un modèle plus performant.
* **La composition du trafic utilisateur est stable**. Si la composition du trafic utilisateur change considérablement au cours de l’entraînement et de la prédiction du modèle, les performances de ce dernier peuvent se dégrader. Supposons, par exemple, que, lors de la phase d’entraînement du modèle, seules les données pour les utilisateurs et utilisatrices de l’audience A soient disponibles, mais que le modèle entraîné soit utilisé pour générer des prédictions pour les utilisateurs et utilisatrices de l’audience B, les performances du modèle pourraient alors être affectées.
* **Les performances des offres ne changent pas considérablement sur une courte période** lorsque ce modèle est mis à jour chaque semaine et que les modifications apportées aux performances sont répercutées lors des mises à jour du modèle. Par exemple, un produit était très populaire auparavant, mais un rapport public identifie le produit comme nocif pour notre santé, et ce produit devient impopulaire extrêmement rapidement. Dans ce scénario, le modèle peut continuer à prédire ce produit jusqu’à ce que le modèle se mette à jour avec les changements de comportement de l’utilisateur.

## Fonctionnement {#how}

Le modèle apprend les interactions de fonctionnalités complexes entre les offres, les informations des utilisateurs et utilisatrices, ainsi que les informations contextuelles afin de recommander des offres personnalisées aux utilisateurs et utilisatrices finaux/finales. Les fonctionnalités sont des entrées dans le modèle.

Il existe trois types de fonctionnalités :

| Types de fonctionnalités | Comment ajouter des fonctionnalités aux modèles |
|--------------|----------------------------|
| Objets de prise de décision (placementID, activityID, decisionScopeID) | Partie des événements d’expérience des commentaires sur la gestion des décisions envoyés à AEP |
| Audiences | Il est possible d’ajouter de 0 à 50 audiences en tant que fonctionnalités lors de la création du modèle d’IA dédiée au classement |
| Données contextuelles | Partie des événements d’expérience des commentaires sur la prise de décisions envoyés à AEP. Données contextuelles disponibles à ajouter au schéma : Détails du commerce, Détails du canal, Détails de l’application, Détails web, Détails de l’environnement, Détails de l’appareil, placeContext |

Le modèle comporte deux phases :

* Dans la phase d’**entraînement de modèle hors ligne**, un modèle est entraîné en apprenant et en mémorisant les interactions de fonctionnalités dans les données historiques.
* Dans la phase d’**inférence en ligne**, les offres des candidats sont classées en fonction des scores en temps réel générés par le modèle. Contrairement aux techniques de filtrage collaboratif traditionnelles, difficiles à inclure pour les utilisateurs et utilisatrices et les offres, l’optimisation personnalisée est une méthode de recommandation basée sur le deep learning, qui permet d’inclure et d’apprendre des modèles d’interaction de fonctionnalités complexes et non linéaires.

Voici un exemple simplifié illustrant l’idée de base derrière l’optimisation personnalisée. Supposons que nous ayons un jeu de données qui stocke les interactions historiques entre les utilisateurs et les offres, comme illustré dans la figure 1. Il existe :

* Deux offres, offer_1 et offer_2,
* Deux fonctionnalités, feature_1 et feature_2,
* Une colonne de réponse.

La valeur de feature_1, feature_2 et la réponse est 0 ou 1. Lorsque nous examinons les cases bleues et orange dans la figure 1, nous constatons que pour offer_1, les réponses sont plus susceptibles d’être 1 lorsque feature_1 et feature_2 ont les mêmes valeurs, tandis que pour offer_2, les libellés sont plus susceptibles d’être 1 lorsque feature_1 est 0 et feature_2 est 1. Nous pouvons également constater que dans la zone rouge, offer_1 est diffusé lorsque feature_1 est 0 et feature_2 est 1 et que la réponse est 0. En fonction du modèle que nous observons dans les zones orange, lorsque feature_1 est 0 et feature_2 est 1, offer_2 est probablement une meilleure recommandation.

En gros, il s’agit d’apprendre et de mémoriser les interactions des caractéristiques historiques et de les appliquer pour générer des prédictions personnalisées.

![](../assets/perso-ranking-schema.png)

## Problème du démarrage à froid {#cold-start}

Un problème de démarrage à froid se produit lorsqu’il n’y a pas assez de données pour faire une recommandation. Pour l’optimisation personnalisée, il existe deux types de problèmes de démarrage à froid.

* **Après avoir créé un nouveau modèle d’IA sans données historiques**, les offres seront diffusées de manière aléatoire pendant une période afin de collecter des données, et les données seront utilisées pour former le premier modèle.
* **Une fois le premier modèle libéré**, 10 % du trafic total seront affectés à une diffusion aléatoire tandis que 90 % du trafic seront utilisés pour les recommandations de modèle. Par conséquent, si de nouvelles offres étaient ajoutées au modèle d’IA, elles seraient diffusées dans le cadre des 10 % de trafic. Les données collectées sur ces offres déterminent le nombre de fois où elles sont sélectionnées parmi les 90 % de trafic au fur et à mesure de la mise à jour du modèle.

## Nouvel entraînement {#re-training}

Les modèles seront entraînés de nouveau afin d’apprendre les dernières interactions de fonctionnalités et d’atténuer chaque semaine la dégradation des performances de ceux-ci.
