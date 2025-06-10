---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser le créateur de règles
description: Découvrez comment créer des règles pour vos campagnes orchestrées
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: dd1a9b6e14617014756e5b4449578a1f7bf805b4
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 19%

---


# Utiliser le créateur de règles {#orchestrated-rule-builder}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interrogation de la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](orchestrate-activities.md)<br/><br/>[Envoyez des messages avec des campagnes orchestrées](send-messages.md)<br/><br/>[Lancez et surveillez la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | <b>[Utiliser le créateur de règles](orchestrated-rule-builder.md)</b><br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Combiner](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Les campagnes orchestrées s’accompagnent d’un créateur de règles qui simplifie le processus de filtrage de la base de données en fonction de divers critères. Le créateur de règles gère efficacement des requêtes très complexes et longues, offrant ainsi une flexibilité et une précision accrues.

En outre, il prend en charge les filtres prédéfinis dans les conditions, ce qui permet aux utilisateurs et utilisatrices d’affiner facilement leurs requêtes tout en utilisant des expressions et des opérateurs avancés pour des stratégies de segmentation et un ciblage d’audience complets.

## Accéder au créateur de règles

Le créateur de règles est disponible lors de la création d’une requête dans une activité **[!UICONTROL Créer une audience]** pour cibler une audience. Il vous permet de spécifier la population que vous souhaitez cibler et de créer facilement de nouvelles audiences adaptées à vos besoins.

![image illustrant une activité créer une audience](assets/rule-builder-query.png)

## Interface du créateur de règles {#interface}

Le créateur de règles fournit une zone de travail centrale dans laquelle vous créez votre requête, ainsi qu’un volet Propriétés qui fournit des informations sur la règle.

![Image illustrant l’interface du créateur de règles](assets/rule-builder-interface.png)

* La **zone de travail centrale** permet d’ajouter et de combiner les différents composants afin de créer votre règle. [Découvrez comment créer une règle](../orchestrated/build-query.md)

* Le volet **[!UICONTROL Propriétés des règles]** fournit des informations sur votre règle. Il vous permet d’effectuer diverses opérations pour vérifier la règle et vous assurer qu’elle répond à vos besoins.

  Ce volet s’affiche lors de la création d’une requête pour créer une audience. [Découvrir comment vérifier et valider votre requête](build-query.md#check-and-validate-your-query)
