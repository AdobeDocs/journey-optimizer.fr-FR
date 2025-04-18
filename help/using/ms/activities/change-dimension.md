---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Changement de dimension
description: Découvrir comment utiliser l’activité « Changement de dimension »
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: f0213f1270e9821b61a5dc396e39f5707f8f4b42
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 60%

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

L’activité **Changement de dimension** est une activité de **ciblage**. Cette activité permet de modifier la dimension de ciblage au fur et à mesure que vous créez votre campagne orchestrée. Il déplace l’axe en fonction du modèle de données et de la dimension d’entrée.

Par exemple, vous pouvez basculer la dimension de ciblage d’une campagne orchestrée de « Profil » vers « Contrats » afin d’envoyer des messages au propriétaire du contrat ciblé.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **Changement de dimension**, procédez comme suit :

1. Ajoutez une activité **Modifier la dimension** à votre campagne orchestrée.

   ![](assets/change-dimension.png)

1. Définissez la **Nouvelle dimension cible**. Lors du changement de dimension, tous les enregistrements sont conservés.

1. Exécutez la campagne orchestrée pour afficher le résultat. Comparez les données dans les tables avant et après l’activité de changement de dimension, et comparez la structure des tables de la campagne orchestrée.

## Exemple {#example}

Dans cet exemple, nous souhaitons envoyer une diffusion SMS à tous les profils ayant effectué un achat. Pour ce faire, nous utilisons d’abord une activité **[!UICONTROL Créer une audience]** liée à une dimension de ciblage « Achat » personnalisée pour cibler tous les achats qui se sont produits.

Nous utilisons ensuite une activité **[!UICONTROL Modifier la dimension]** pour basculer la dimension de ciblage de la campagne orchestrée sur « Destinataires ». Cela nous permet de cibler les personnes destinataires qui correspondent à la requête.

![](assets/change-dimension-example.png)
