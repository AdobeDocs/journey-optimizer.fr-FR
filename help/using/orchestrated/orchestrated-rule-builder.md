---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser le créateur de règles
description: Découvrez comment créer des règles pour vos campagnes orchestrées
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 21%

---


# Utiliser le créateur de règles {#orchestrated-rule-builder}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | <b>[Utiliser le créateur de règles](orchestrated-rule-builder.md)</b><br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

Les campagnes orchestrées s’accompagnent d’un créateur de règles qui simplifie le processus de filtrage de la base de données en fonction de divers critères. Le créateur de règles gère efficacement des requêtes très complexes et longues, offrant ainsi une flexibilité et une précision accrues.

Il prend également en charge les filtres prédéfinis dans des conditions, ce qui vous permet d’affiner facilement les requêtes tout en utilisant des expressions et des opérateurs avancés pour le ciblage d’audience et les stratégies de segmentation complètes.

## Accéder au créateur de règles

Le concepteur de requête est disponible dans tout contexte où vous devez définir des règles pour filtrer les données.

| Utilisation | Exemple |
|  ---  |  ---  |
| **Créer des audiences** : spécifiez la population que vous souhaitez cibler dans vos campagnes orchestrées à l’aide d’une activité **[!UICONTROL Créer une audience]** et créez facilement de nouvelles audiences adaptées à vos besoins. [Découvrir comment créer des audiences](../orchestrated/activities/build-audience.md) | ![Image montrant comment accéder à l’interface de création d’audience](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Créer une condition dans la zone de travail de campagne** : appliquez les règles de la zone de travail de campagne à l’aide d’une activité **[!UICONTROL Partage]** pour vous aligner sur vos besoins spécifiques. [Découvrez comment utiliser une activité Partage](../orchestrated/activities/split.md) | ![Image montrant comment accéder aux options de personnalisation d’un workflow](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Créer des filtres avancés** : créez des règles pour filtrer les données affichées dans les listes, telles que les logs de workflow ou les dimensions de ciblage. | ![Image montrant comment personnaliser les filtres de liste](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interface du créateur de règles {#interface}

Le créateur de règles fournit une zone de travail centrale dans laquelle vous créez votre requête, ainsi qu’un volet Propriétés qui fournit des informations sur la règle.

![Image illustrant l’interface du créateur de règles](assets/rule-builder-interface.png)

* La **zone de travail centrale** permet d’ajouter et de combiner les différents composants afin de créer votre règle. [Découvrez comment créer une règle](../orchestrated/build-query.md)

* Le volet **[!UICONTROL Propriétés des règles]** fournit des informations sur votre règle. Il vous permet d’effectuer diverses opérations pour vérifier la règle et vous assurer qu’elle répond à vos besoins.

  Ce volet s’affiche lors de la création d’une requête pour créer une audience. [Découvrir comment vérifier et valider votre requête](build-query.md#check-and-validate-your-query)
