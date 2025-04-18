---
solution: Journey Optimizer
product: journey optimizer
title: Principes clés de la création de campagnes orchestrée
description: Découvrez les principes fondamentaux des campagnes orchestrées avec Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 26%

---

# Principes de base {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagne orchestrée"
>abstract="Dans cet écran, vous pouvez accéder à la liste complète des campagnes orchestrées, vérifier leur statut actuel, les dates de dernière exécution et de prochaine exécution, et créer une nouvelle campagne orchestrée."

Avec Adobe Journey Optimizer, vous pouvez créer des campagnes orchestrées dans une zone de travail visuelle afin de concevoir des processus cross-canal tels que la segmentation, l’exécution de campagnes ou le traitement de fichiers.

## Que contient une campagne orchestrée ? {#gs-ms-campaign-inside}

La zone de travail de campagne orchestrée est une représentation de ce qui est censé se produire. Il décrit les différentes tâches à effectuer et la manière dont elles sont liées.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Chaque campagne orchestrée contient :

* des **Activités** : une activité est une tâche à effectuer. Les différentes activités disponibles sont représentées sur le diagramme par des icônes. Chaque activité possède des propriétés spécifiques et d’autres propriétés communes à toutes les activités.

  Dans un diagramme de campagne orchestré, une même activité peut générer plusieurs tâches, notamment en cas de boucle ou d&#39;actions récurrentes.

* **Transitions** : les transitions relient une activité source à une activité de destination et définissent leur ordre.

* **Tables de travail** : la table de travail contient toutes les informations véhiculées par la transition. Chaque campagne orchestrée utilise plusieurs tables de travail. Les données transmises dans ces tableaux peuvent être utilisées tout au long du cycle de vie de la campagne orchestrée.

## Étapes clés de création d’une campagne orchestrée {#gs-ms-campaign-steps}

Les étapes clés de création d’une campagne orchestrée sont les suivantes :

![](assets/workflow-creation-process.png){zoomable="yes"}

## Accès aux campagnes orchestrées

Dans le menu **[!UICONTROL Campagnes]**, accédez à l’onglet À plusieurs étapes pour accéder à la liste complète des campagnes orchestrées.

Chaque campagne orchestrée figurant dans la liste affiche des informations sur son [statut](#status) en cours, la dernière fois qu’elle a été exécutée ou modifiée, ainsi que la date et l’heure de la prochaine exécution planifiée.

Vous pouvez personnaliser les colonnes affichées en cliquant sur l’icône **[!UICONTROL Configurer la colonne pour une disposition personnalisée]**, située dans le coin supérieur droit de la liste. Vous pouvez ainsi ajouter des informations supplémentaires à la liste, telles que la dernière activité à avoir rencontré une erreur pour chaque campagne orchestrée ou la dimension de ciblage appliquée.

Une barre de recherche et des filtres sont également disponibles pour faciliter la recherche dans la liste. Vous pouvez, par exemple, filtrer les campagnes orchestrées afin de n’afficher que celles appartenant à une campagne ou celles traitées au cours d’une période spécifique.

Pour dupliquer ou supprimer une campagne orchestrée, cliquez sur le bouton représentant des points de suspension, puis sélectionnez **[!UICONTROL Dupliquer]** ou **[!UICONTROL Supprimer]**.

>[!NOTE]
>
>Lorsqu’une campagne orchestrée est en cours, vous pouvez la dupliquer, mais vous ne pouvez pas la supprimer.

## Statuts et cycle de vie {#status}

Les campagnes peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la campagne orchestrée a été créée et enregistrée.
* **[!UICONTROL En cours]** : la campagne orchestrée est en cours d’exécution.
* **[!UICONTROL Terminé]** : l’exécution de la campagne orchestrée est terminée.
* **[!UICONTROL En pause]** : la campagne orchestrée a été suspendue.
* **[!UICONTROL Avec erreur]** : la campagne orchestrée a rencontré une erreur. Ouvrez la campagne orchestrée et accédez aux logs et aux tâches pour identifier l’erreur et la résoudre.


## Création d’une requête

## Instructions relatives à Personalization
