---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Changement de dimension
description: Découvrir comment utiliser l’activité « Changement de dimension »
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 34%

---

# Changement de dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Générer un complément"
>abstract="Vous pouvez générer une transition sortante supplémentaire avec la population restante, qui a été exclue en tant que doublon. Pour ce faire, activez l’option **Générer un complément**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Activité Changement de dimension"
>abstract="Cette activité vous permet de modifier la dimension de ciblage à mesure que vous créez une audience. Elle déplace l’axe en fonction du modèle de données et de la dimension d’entrée. Par exemple, vous pouvez passer de la dimension « contrats » à la dimension « clientèle »."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](../access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](../gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](../orchestrate-activities.md)<br/><br/>[Lancez et surveillez la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser le créateur de règles](../orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](../build-query.md)<br/><br/>[Modifier les expressions](../edit-expressions.md)<br/><br/>[Reciblage](../retarget.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - <b>[Modifier la dimension](change-dimension.md)</b> - [Activités de canal](channels.md) - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

En tant que spécialiste marketing, vous pouvez améliorer le ciblage des audiences en passant d’une entité de données à une entité associée au sein d’une campagne orchestrée. Vous pouvez ainsi aller au-delà des profils utilisateur et vous concentrer sur des comportements spécifiques, tels que les achats, les réservations ou d’autres interactions.

Pour ce faire, utilisez l’activité **[!UICONTROL Modifier la dimension]**. Elle permet d’ajuster la dimension de ciblage au cours de la campagne orchestrée.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **[!UICONTROL Changement de dimension]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Modifier la dimension]** à votre campagne orchestrée.

   ![](../assets/orchestrated-change-dimension.png)

1. Définissez la **[!UICONTROL Nouvelle dimension cible]**. Lors du changement de dimension, tous les enregistrements sont conservés.


## Exemple {#example}

Ce cas pratique se concentre sur l’envoi d’un SMS aux profils qui ont créé une liste de souhaits au cours du dernier mois.

Commencez par une activité de ciblage **[!UICONTROL Créer une audience]**, en utilisant la dimension de ciblage **[!UICONTROL Liste de souhaits]** pour identifier toutes les listes de souhaits pertinentes.

Ajoutez ensuite une activité **[!UICONTROL Modifier la dimension]** pour basculer la dimension de ciblage de **[!UICONTROL Liste de souhaits]** à **[!UICONTROL Destinataire].** Cette étape permet de s’assurer que la campagne orchestrée cible les profils corrects associés à ces listes de souhaits, ce qui permet d’envoyer le SMS aux profils prévus.

![](../assets/orchestrated-change-dimension-example.png)
