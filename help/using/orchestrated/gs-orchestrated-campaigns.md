---
solution: Journey Optimizer
product: journey optimizer
title: Commencer les campagnes orchestrées
description: Découvrez comment commencer avec les campagnes orchestrées.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 19%

---

# Commencer les campagnes orchestrées {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="Campagnes orchestrées"
>abstract="**Orchestration des campagnes**<br/> divisez, combinez, enrichissez et manipulez des jeux de données relationnels pour définir votre audience<br/><br/>"

**Exploiter les données multi-entités**<br/> Découvrez comment les campagnes orchestrées peuvent tirer parti des jeux de données relationnelles pour enrichir les données pour la segmentation et la personnalisation <br/><br/>**Segmentation ad hoc et nombres exacts**<br/> Créez votre segment étape par étape avec des nombres exacts <br/><br/>**Canaux disponibles**<br/> E-mail, SMS, notifications push, publipostage direct »

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| <b>[Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)</b><br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Commencer avec les activités](activities/about-activities.md)<br/><br/>Activités :<br/>[Rendez-vous](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Changement de dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combiner](activities/combine.md) - [Déduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Branchement](activities/fork.md) - [Réconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Partage](activities/split.md) - [Attente](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

L’orchestration des campagnes dans [!DNL Adobe Journey Optimizer] alimente des campagnes marketing sophistiquées et lancées par la marque sur l’ensemble des canaux, ce qui vous permet de stimuler l’engagement, le chiffre d’affaires et la fidélisation de la clientèle à grande échelle.

Bien que le marketing cross-canal soit essentiel, les campagnes orchestrées le rendent transparent. Grâce à une interface visuelle par glisser-déposer, vous pouvez concevoir et automatiser des workflows marketing complexes, de la segmentation à la diffusion des messages, sur plusieurs canaux. Tout se passe dans un environnement intuitif, conçu pour la vitesse, le contrôle et l’efficacité.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Fonctionnalités principales

L’orchestration des campagnes repose sur quatre piliers principaux :

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Audiences à la demande" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>Audiences à la demande</b><br/>Interrogez instantanément les jeux de données pour créer des segments d’audience à l’aide de n’importe quelle combinaison de types et de dimensions de données.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentation et envoi d’entités multiples" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>Segmentation et envoi d’entités multiples</b><br/>allez au-delà des campagnes basées sur les personnes : utilisez des entités telles que des catalogues de produits, des emplacements de magasin ou des données de service pour cibler avec précision.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilité et précision de la pré-envoi" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>Visibilité et précision de l’envoi préalable</b><br/>obtenez un nombre exact de segmentations et une portée complète de la campagne avant le lancement, pour garantir la précision et la confiance.</td></tr>
<tr style="border: 0;">
<td><img alt="Workflows de campagne à plusieurs étapes" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>Workflows de campagne à plusieurs étapes</b><br/>Concevez des campagnes à plusieurs étapes, des messages quotidiens aux campagnes complexes telles que les promotions saisonnières ou les lancements de produits majeurs.</td></tr>
</table>

## Campagnes et parcours orchestrés

Même si la visualisation des campagnes orchestrées présente des similitudes avec les parcours, elle résout différents objectifs et cas d’utilisation :

* **Parcours** - 1 à 1 canevas où chaque profil parcourt les différentes étapes à son propre rythme. L’état de chaque client est conservé dans son contexte pour déclencher des actions en temps réel.

* **Campagnes orchestrées** - Contrairement aux parcours, les campagnes orchestrées fonctionnent à l’aide d’une zone de travail par lots qui calcule les segments. Tous les profils sont traités ensemble en même temps.

## Conditions préalables

Avant d’utiliser des campagnes orchestrées, il est essentiel de vérifier que vous disposez des autorisations appropriées. L’accès aux campagnes orchestrées est limité aux utilisateurs affectés à un **[!UICONTROL profil de produit]** approprié, tel que l’administrateur de campagne orchestrée, l’approbateur de campagne orchestrée, le responsable de campagne orchestré ou la visionneuse de campagne orchestrée.

Si vous ne parvenez pas à accéder aux fonctionnalités de Campaign orchestrée, contactez votre administrateur pour demander les autorisations nécessaires.

➡️ [En savoir plus sur les profils de produit liés aux campagnes orchestrées](../administration/ootb-product-profiles.md)

## Explorons plus en détail

Maintenant que vous avez une compréhension de ce que sont les campagnes orchestrées, il est temps d’examiner plus en détail ces sections de documentation pour commencer à utiliser la fonctionnalité.

<table><tr style="border: 0; text-align: center;">
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
