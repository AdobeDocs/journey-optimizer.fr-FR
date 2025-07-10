---
solution: Journey Optimizer
product: journey optimizer
title: Commencer les campagnes orchestrées
description: Découvrez comment commencer avec des campagnes orchestrées
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: ea4b65ae05f219203754ed6e5ddd7effc795ff56
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 6%

---

# Commencer les campagnes orchestrées {#orchestrated-camp}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| <b>[Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)</b><br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

&#x200B;# Prise en main de l’orchestration des campagnes {#gs}

L’orchestration des campagnes dans [!DNL Adobe Journey Optimizer] alimente des campagnes marketing sophistiquées et lancées par la marque sur l’ensemble des canaux, ce qui vous permet de stimuler l’engagement, le chiffre d’affaires et la fidélisation de la clientèle à grande échelle.

Bien que le marketing cross-canal soit essentiel, les campagnes orchestrées le rendent transparent. Grâce à une interface visuelle par glisser-déposer, vous pouvez concevoir et automatiser des workflows marketing complexes, de la segmentation à la diffusion des messages, sur plusieurs canaux. Tout se passe dans un environnement intuitif, conçu pour la vitesse, le contrôle et l’efficacité.

Ce module apporte **orchestration de campagnes par lots** à [!DNL Journey Optimizer], ce qui vous permet d’effectuer les opérations suivantes :

* Créer et exécuter des **campagnes à plusieurs étapes** (par exemple, promotions saisonnières, lancements de nouveaux produits),
* Diffusez des **messages personnalisés et cohérents** sur n’importe quel canal,
* Coordonner **segmentation, traitement des fichiers et gestion des tâches** en un seul endroit,
* Autoriser la collaboration par le biais des approbations et des affectations de tâches

## Fonctionnalités principales

L’orchestration des campagnes repose sur quatre piliers principaux :

1. **Audiences À La Demande**

   Exécutez instantanément des requêtes sur les jeux de données pour créer des segments d’audience à l’aide de n’importe quelle combinaison de types et de dimensions de données.

1. **Segmentation et envoi d’entités multiples**

   Allez au-delà des campagnes basées sur les personnes : utilisez des entités telles que des catalogues de produits, des emplacements de magasin ou des données de service pour cibler avec précision.

1. **Visibilité et précision de la pré-envoi**

   Obtenez le nombre exact de segmentations et la portée complète de la campagne avant le lancement, pour garantir la précision et la confiance.

1. **Workflows de campagne à plusieurs étapes**

   Concevez des campagnes en plusieurs étapes, des messages quotidiens aux campagnes complexes telles que les promotions saisonnières ou les lancements de produits majeurs.

## Campagnes et parcours orchestrés

Même si la visualisation des campagnes orchestrées présente des similitudes avec les parcours, elle résout différents objectifs et cas d’utilisation :

* **Parcours** - 1 à 1 canevas où chaque profil parcourt les différentes étapes à son propre rythme. L’état de chaque client est conservé dans son contexte pour déclencher des actions en temps réel.

* **Campagnes orchestrées** - Contrairement aux parcours, les campagnes orchestrées fonctionnent à l’aide d’une zone de travail par lots qui calcule les segments. Tous les profils sont traités ensemble en même temps.

## Conditions préalables

Avant d’utiliser des campagnes orchestrées, il est essentiel de vérifier que vous disposez des autorisations appropriées. L’accès aux campagnes orchestrées est limité aux utilisateurs affectés à un **[!UICONTROL profil de produit]** approprié, tel que l’administrateur de campagne orchestrée, l’approbateur de campagne orchestrée, le responsable de campagne orchestré ou la visionneuse de campagne orchestrée.

Si vous ne parvenez pas à accéder aux fonctionnalités de Campaign orchestrée, contactez votre administrateur pour demander les autorisations nécessaires.

➡️[En savoir plus sur les profils de produit liés aux campagnes orchestrées](../administration/ootb-product-profiles.md)

## Explorons plus en détail

Maintenant que vous avez une compréhension de ce que sont les campagnes orchestrées, il est temps d’examiner plus en détail ces sections de documentation pour commencer à utiliser la fonctionnalité.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Accéder et gérer des workflows" src="assets/do-not-localize/workflow-access.jpeg">
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
