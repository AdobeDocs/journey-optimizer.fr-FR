---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Changement de dimension
description: Découvrir comment utiliser l’activité « Changement de dimension »
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: ht
source-wordcount: '260'
ht-degree: 100%

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

En tant que responsable marketing, vous pouvez améliorer le ciblage des audiences en passant d’une entité de données à une entité associée au sein d’une campagne orchestrée. Vous pouvez ainsi aller au-delà des profils d’utilisation et vous concentrer sur des comportements spécifiques, tels que les achats, les réservations ou d’autres interactions.

Pour ce faire, utilisez l’activité **[!UICONTROL Changement de dimension]**. Elle permet d’ajuster la dimension du ciblage au cours de la campagne orchestrée.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **[!UICONTROL Changement de dimension]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Changement de dimension]** à votre campagne orchestrée.

   ![](../assets/orchestrated-change-dimension.png)

1. Définissez la **[!UICONTROL Nouvelle dimension cible]**. Lors du changement de dimension, tous les enregistrements sont conservés.


## Exemple {#example}

Ce cas d’utilisation se concentre sur l’envoi d’un SMS aux profils qui ont créé une liste de souhaits au cours du dernier mois.

Commencez par une activité **[!UICONTROL Créer une audience]**, en utilisant la dimension de ciblage **[!UICONTROL Liste de souhaits]** pour identifier toutes les listes de souhaits pertinentes.

Ajoutez ensuite une activité **[!UICONTROL Changement de dimension]** pour basculer la dimension de ciblage de **[!UICONTROL Liste de souhaits]** à **[!UICONTROL Destinataire].** Cette étape permet de s’assurer que la campagne orchestrée cible les bons profils associés à ces listes de souhaits, ce qui permet d’envoyer le SMS aux profils prévus.

![](../assets/orchestrated-change-dimension-example.png)
