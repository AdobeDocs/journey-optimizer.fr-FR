---
solution: Journey Optimizer
product: journey optimizer
title: Principes clés de la création de campagnes en plusieurs étapes
description: Découvrez les principes fondamentaux des campagnes à plusieurs étapes avec Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 3ecb1691cc8a1c429d9bd9919b06ddc5a316eff7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 31%

---

# Principes clés {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagne à étapes multiples"
>abstract="Dans cet écran, vous pouvez accéder à la liste complète des campagnes à étapes multiples, vérifier leur statut actuel, les dates de dernière exécution et de prochaine exécution, et créer une campagne à étapes multiples."

Avec Adobe Journey Optimizer, vous pouvez créer des campagnes à plusieurs étapes dans une zone de travail visuelle afin de concevoir des processus cross-canal tels que la segmentation, l’exécution de campagnes ou le traitement de fichiers.

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

## Accès aux campagnes à plusieurs étapes

Dans le menu **[!UICONTROL Campagnes]**, accédez à l’onglet À plusieurs étapes pour accéder à la liste complète des campagnes à plusieurs étapes.

Chaque campagne à plusieurs étapes de la liste affiche des informations sur son [statut](#status) en cours, la dernière fois qu’elle a été exécutée ou modifiée, ainsi que la date et l’heure de la prochaine exécution planifiée.

Vous pouvez personnaliser les colonnes affichées en cliquant sur l’icône **[!UICONTROL Configurer la colonne pour une disposition personnalisée]**, située dans le coin supérieur droit de la liste. Vous pouvez ainsi ajouter des informations supplémentaires à la liste, telles que la dernière activité en erreur pour chaque campagne à plusieurs étapes ou la dimension de ciblage appliquée.

Une barre de recherche et des filtres sont également disponibles pour faciliter la recherche dans la liste. Vous pouvez, par exemple, filtrer les campagnes à plusieurs étapes afin d’afficher uniquement celles appartenant à une campagne ou celles traitées au cours d’une période spécifique.

Pour dupliquer ou supprimer une campagne à plusieurs étapes, cliquez sur le bouton représentant des points de suspension, puis sélectionnez **[!UICONTROL Dupliquer]** ou **[!UICONTROL Supprimer]**.

>[!NOTE]
>
>Lorsqu’une campagne à plusieurs étapes est en cours, vous pouvez la dupliquer, mais vous ne pouvez pas la supprimer.

## Statuts et cycle de vie {#status}

Les campagnes peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la campagne à plusieurs étapes a été créée et enregistrée.
* **[!UICONTROL En cours]** : la campagne à plusieurs étapes est en cours d’exécution.
* **[!UICONTROL Terminé]** : l’exécution de la campagne en plusieurs étapes est terminée.
* **[!UICONTROL En pause]** : la campagne à plusieurs étapes a été suspendue.
* **[!UICONTROL Avec erreur]** : une erreur s’est produite lors de la campagne à plusieurs étapes. Ouvrez la campagne à plusieurs étapes et accédez aux journaux et aux tâches pour identifier l’erreur et la résoudre.


## Création d’une requête

## Instructions relatives à Personalization
