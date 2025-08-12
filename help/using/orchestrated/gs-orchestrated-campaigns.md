---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les campagnes orchestrées
description: Découvrez comment commencer avec les campagnes orchestrées
short-description: Découvrez les fonctionnalités clés et les cas pratiques des campagnes orchestrées.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 4510cfde1579fbabe7deb1289f70f13ee21a3d4a
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 30%

---


# Commencer avec les campagnes orchestrées {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orchestration de campagne</b><br/>Fractionner, combiner, enrichir et manipuler des jeux de données relationnelles pour définir votre audience<br/><br/> <b>Tirer parti des données multi-entités</b><br/>Découvrir comment les campagnes orchestrées peuvent tirer parti des jeux de données relationnelles pour enrichir les données pour la segmentation et la personnalisation.<br/><br/><b>Segmentation ad hoc et nombres exacts</b><br/>Créer votre segment étape par étape avec des nombres exacts<br/><br/><b>Canaux disponibles</b><br/>E-mail, SMS, Notifications push, Courrier"

L’orchestration des campagnes dans [!DNL Adobe Journey Optimizer] alimente des campagnes marketing sophistiquées et lancées par la marque sur l’ensemble des canaux, ce qui vous permet de stimuler l’engagement, le chiffre d’affaires et la fidélisation de la clientèle à grande échelle.

>[!IMPORTANT]
>
>Pour accéder à l’orchestration de Campaign, votre licence doit inclure le package **Journey Optimizer - Campagnes et Parcours** ou **Journey Optimizer - Campagnes**. Contactez votre représentant Adobe pour confirmer votre licence et effectuer une mise à jour si nécessaire.

Bien que le marketing cross-canal soit essentiel, les campagnes orchestrées le rendent transparent. Grâce à une interface visuelle par glisser-déposer, vous pouvez concevoir et automatiser des workflows marketing complexes, depuis la segmentation jusqu’à la diffusion des messages, sur plusieurs canaux. Tout se passe dans un environnement intuitif, conçu pour assurer vitesse, contrôle et efficacité.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Fonctionnalités principales

L’orchestration des campagnes repose sur quatre piliers principaux :

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Audiences à la demande" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>Audiences à la demande</b><br/>Interrogez instantanément les jeux de données pour créer des segments d’audience à l’aide de n’importe quelle combinaison de types et de dimensions de données.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentation et envoi d’entités multiples" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentation et envoi d’entités multiples</b><br/>allez au-delà des campagnes basées sur les personnes : utilisez des entités telles que des catalogues de produits, des emplacements de magasin ou des données de service pour cibler avec précision.<br/><br/>
Prise en charge de l’envoi à plusieurs niveaux, où un message est envoyé par profil et par entité secondaire associée. Ces entités secondaires peuvent inclure des adresses de contact, des réservations, des abonnements, des contrats ou d’autres données liées. Cela permet, par exemple, d’envoyer les campagnes à toutes les adresses connues d’un profil ou pour chaque réservation associée à ce profil.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilité et précision de la pré-envoi" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Visibilité et précision de l’envoi préalable</b><br/>obtenez un nombre exact de segmentations et une portée complète de la campagne avant le lancement, pour garantir la précision et la confiance.</td></tr>
<tr style="border: 0;">
<td><img alt="Workflows de campagne à plusieurs étapes" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Workflows de campagne à plusieurs étapes</b><br/>Concevez des campagnes à plusieurs étapes, des messages quotidiens aux campagnes complexes telles que les promotions saisonnières ou les lancements de produits majeurs.</td></tr>
</table>

## Campagnes et parcours orchestrés

Même si la visualisation des campagnes orchestrées présente des similitudes avec les parcours, elle résout différents objectifs et cas d’utilisation :

* **Parcours** - 1 à 1 canevas où chaque profil parcourt les différentes étapes à son propre rythme. L’état de chaque client est conservé dans son contexte pour déclencher des actions en temps réel.

* **Campagnes orchestrées** - Contrairement aux parcours, les campagnes orchestrées utilisent une zone de travail par lots qui calcule les segments. Tous les profils sont traités ensemble en même temps.

Les deux zones de travail sont optimisées pour leurs cas d’utilisation respectifs : la zone de travail de Parcours publie les parcours qui ont tendance à vivre plus longtemps, tandis que la zone de travail de Campaign est conçue pour les exécutions itératives et incrémentielles d’une campagne par lots.

## Que contient une campagne orchestrée ? {#gs-ms-campaign-inside}

La zone de travail de campagne orchestrée est une représentation de ce qui est censé se produire. Elle décrit les différentes tâches à effectuer et la manière dont elles sont liées.

![image montrant une zone de travail de campagne orchestrée](assets/canvas-example.png)

Chaque campagne orchestrée contient :

* des **Activités** : une activité est une tâche à effectuer. Les différentes activités disponibles sont représentées sur le diagramme par des icônes. Chaque activité possède des propriétés spécifiques et d’autres propriétés communes à toutes les activités.

  Dans un diagramme de Campagne orchestrée, une même activité peut générer plusieurs tâches, notamment en cas de boucle ou d&#39;actions récurrentes.

* **Transitions** : les transitions relient une activité source à une activité de destination et définissent leur ordre.

* **Tables de travail** : la table de travail contient toutes les informations véhiculées par la transition. Chaque campagne orchestrée utilise plusieurs tables de travail. Les données transmises dans ces tableaux peuvent être utilisées tout au long du cycle de vie de la campagne orchestrée.

## Explorons plus en détail.

Maintenant que vous avez une compréhension de ce que sont les campagnes orchestrées, il est temps d’examiner plus en détail ces sections de documentation pour commencer à utiliser la fonctionnalité.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Accéder aux campagnes et les gérer" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Étapes de configuration</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Lead" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>Créer une campagne orchestrée</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Peu fréquent" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Utiliser les activités</strong></a>
</div>
<p></td>
</tr></table>
