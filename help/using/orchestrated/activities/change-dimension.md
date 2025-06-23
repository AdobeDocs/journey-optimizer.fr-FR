---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Changement de dimension
description: Découvrir comment utiliser l’activité « Changement de dimension »
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 38b65200435e0b997e79aefbb66549b9168188fd
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 26%

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
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](../gs-campaign-creation.md) | [Créer une campagne orchestrée](../create-orchestrated-campaign.md)<br/><br/>[Orchestrer des activités](../orchestrate-activities.md)<br/><br/>[Envoyer des messages avec des campagnes orchestrées](../send-messages.md)<br/><br/>[Démarrer et surveiller la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser la requête Modeler](../orchestrated-rule-builder.md)<br/><br/>[créer votre première requête](../build-query.md)<br/><br/>[modifier des expressions](../edit-expressions.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Combiner](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

En tant que spécialiste marketing, vous pouvez affiner le ciblage des audiences en passant d’une entité de données à une autre entité liée au sein d’une campagne orchestrée. Vous pouvez ainsi passer du ciblage des profils utilisateur à des actions spécifiques, telles que des achats, des réservations ou d’autres interactions.

Pour ce faire, utilisez l’activité **[!UICONTROL Modifier la dimension]**. Elle permet de modifier la dimension de ciblage au cours de la campagne orchestrée, en fonction de la structure de votre modèle de données et de la dimension de saisie.

Par exemple, vous pouvez déplacer la dimension de ciblage de **&#x200B;**&#x200B;[!UICONTROL Profil] **&#x200B; vers &#x200B;**&#x200B;**[!UICONTROL Contrats]** afin d’envoyer des messages directement aux propriétaires de contrat associés à l’audience sélectionnée.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **&#x200B;**&#x200B;[!UICONTROL Modifier la dimension]**, procédez comme suit :

1. Ajoutez une activité **&#x200B;**&#x200B;[!UICONTROL Modifier la dimension]** à votre campagne orchestrée.

   ![](../assets/change-dimension.png)

1. Définissez la **&#x200B;**&#x200B;[!UICONTROL Nouvelle dimension cible]**. Lors du changement de dimension, tous les enregistrements sont conservés.

1. Exécutez la campagne orchestrée pour afficher le résultat. Comparez les données dans les tables avant et après l’activité de changement de dimension, et comparez la structure des tables de la campagne orchestrée.

## Exemple {#example}

Ce cas pratique implique l’envoi d’un SMS aux profils qui ont créé une liste de souhaits au cours du dernier mois.

Commencez par une activité de ciblage **[!UICONTROL Créer une audience]** à l’aide de la dimension de ciblage **&#x200B;**&#x200B;[!UICONTROL Liste de souhaits]** pour sélectionner toutes les listes de souhaits pertinentes.

Insérez ensuite une activité **[!UICONTROL Modifier la dimension]** pour basculer la dimension de ciblage de **&#x200B;**&#x200B;[!UICONTROL Liste de souhaits &#x200B;]&#x200B;**à &#x200B;**&#x200B;**[!UICONTROL Destinataire]**. Cela permet à la campagne orchestrée d’envoyer les SMS aux profils associés à ces listes de souhaits.

![](../assets/change-dimension-example.png)
