---
solution: Journey Optimizer
product: journey optimizer
title: Principes clés de la création de campagnes en plusieurs étapes
description: Découvrez les principes fondamentaux des campagnes à plusieurs étapes avec Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 271c4739a5537a99da981913606bc9eb099b5139
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 28%

---

# Principes clés d’une campagne orchestrée {#ms-campaign-creation}

Avec Adobe Journey Optimizer, vous pouvez créer des campagnes à plusieurs étapes dans une zone de travail visuelle afin de concevoir des processus cross-canal tels que la segmentation, l’exécution de campagnes ou le traitement de fichiers.

## Création d’une requête

## Instructions relatives à Personalization

## Que contient une campagne à plusieurs étapes ? {#gs-ms-campaign-inside}

La zone de travail de campagne à plusieurs étapes est une représentation de ce qui est censé se produire. Il décrit les différentes tâches à effectuer et la manière dont elles sont liées.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Chaque campagne à plusieurs étapes contient les éléments suivants :

* des **Activités** : une activité est une tâche à effectuer. Les différentes activités disponibles sont représentées sur le diagramme par des icônes. Chaque activité possède des propriétés spécifiques et d’autres propriétés communes à toutes les activités.

  Dans un diagramme de campagne à plusieurs étapes, une même activité peut générer plusieurs tâches, notamment en cas de boucle ou d&#39;actions récurrentes.

* **Transitions** : les transitions relient une activité source à une activité de destination et définissent leur ordre.

* **Tables de travail** : la table de travail contient toutes les informations véhiculées par la transition. Chaque campagne à plusieurs étapes utilise plusieurs tables de travail. Les données transmises dans ces tableaux peuvent être utilisées tout au long du cycle de vie de la campagne à plusieurs étapes.

## Étapes clés de création d’une campagne à plusieurs étapes {#gs-ms-campaign-steps}

Les étapes clés de création d’une campagne à plusieurs étapes sont les suivantes :

![](assets/workflow-creation-process.png){zoomable="yes"}

## Statuts et cycle de vie

Les campagnes peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la campagne à plusieurs étapes a été créée et enregistrée.
* **[!UICONTROL En cours]** : la campagne à plusieurs étapes est en cours d’exécution.
* **[!UICONTROL Terminé]** : l’exécution de la campagne en plusieurs étapes est terminée.
* **[!UICONTROL En pause]** : la campagne à plusieurs étapes a été suspendue.
* **[!UICONTROL Avec erreur]** : une erreur s’est produite lors de la campagne à plusieurs étapes. Ouvrez la campagne à plusieurs étapes et accédez aux journaux et aux tâches pour identifier l’erreur et la résoudre.

