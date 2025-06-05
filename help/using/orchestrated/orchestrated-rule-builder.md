---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser le créateur de règles
description: Découvrez comment créer des règles pour vos campagnes orchestrées
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 16%

---


# Utiliser le créateur de règles {#orchestrated-rule-builder}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interrogation de la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](gs-campaign-creation.md) | [Créer une campagne orchestrée](create-orchestrated-campaign.md)<br/><br/>[Orchestrer des activités](orchestrate-activities.md)<br/><br/>[Envoyer des messages avec des campagnes orchestrées](send-messages.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Combiner](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

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

* La **zone de travail centrale** permet d’ajouter et de combiner les différents composants afin de créer votre règle. Une barre d’outils propose des options permettant de manipuler facilement les composants de règle :

  | Icône de la barre d’outils | Description |
  |--- |--- |
  | ![Icône de sélection Déplacer vers le haut](assets/do-not-localize/rule-builder-icon-up.svg) | Déplacez le composant d’une ligne vers le haut. |
  | ![Icône de sélection Déplacer vers le bas](assets/do-not-localize/rule-builder-icon-down.svg) | Déplacez le composant vers le bas d’une ligne. |
  | ![Icône de sélection de groupe](assets/do-not-localize/rule-builder-icon-group.svg) | Placez deux composants dans un groupe. |
  | ![ Icône Dissocier la sélection ](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Séparez les composants d’un seul groupe. |
  | ![icône Développer tout](assets/do-not-localize/rule-builder-icon-expand.svg) | Développez tous les groupes. |
  | ![Icône Réduire tout](assets/do-not-localize/rule-builder-icon-collapse.svg) | Réduire tous les groupes. |
  | ![Icône Tout supprimer](assets/do-not-localize/rule-builder-icon-delete.svg) | Supprimez tous les groupes et composants. |

* Le volet **[!UICONTROL Propriétés des règles]** fournit des informations sur votre règle. Il vous permet d’effectuer diverses opérations pour vérifier la règle et vous assurer qu’elle répond à vos besoins.

  Ce volet s’affiche lors de la création d’une requête pour créer une audience. [Découvrir comment vérifier et valider votre requête](build-query.md#check-and-validate-your-query)
