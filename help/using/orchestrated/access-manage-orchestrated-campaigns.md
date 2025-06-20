---
solution: Journey Optimizer
product: journey optimizer
title: Accéder à une campagne orchestrée et la gérer
description: Découvrez les principes fondamentaux de la création de campagnes orchestrées avec Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: cd42bca1a36344f688b2d90e1c0b96a9ef2a53ce
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 22%

---

# Accéder à une campagne orchestrée et la gérer {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagne orchestrée"
>abstract="Dans cet écran, vous pouvez accéder à la liste complète des campagnes orchestrées, vérifier leur statut actuel, les dates de dernière exécution et de prochaine exécution, et créer une campagne orchestrée."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Action"
>abstract="Cette section répertorie toutes les actions utilisées dans la campagne orchestrée."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/><b>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md)</b> | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](orchestrate-activities.md)<br/><br/>[Envoyez des messages avec des campagnes orchestrées](send-messages.md)<br/><br/>[Lancez et surveillez la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Combiner](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Accès aux campagnes orchestrées

Accédez au menu **[!UICONTROL Campagnes]** et sélectionnez l’onglet **[!UICONTROL Orchestration]** pour accéder à la liste complète des campagnes orchestrées.

![image montrant l’inventaire des campagnes orchestrées](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Chaque campagne orchestrée figurant dans la liste affiche des informations telles que le [statut](#status) actuel de la campagne, le canal et les balises associés ou la dernière fois qu’elle a été modifiée. Vous pouvez personnaliser les colonnes affichées en cliquant sur le bouton ![Configurer la disposition](assets/do-not-localize/inventory-configure-layout.svg).

Une barre de recherche et des filtres sont également disponibles pour faciliter la recherche dans la liste. Vous pouvez, par exemple, filtrer les campagnes orchestrées afin de n’afficher que celles associées à un canal ou à une balise donnée, ou celles créées au cours d’une période spécifique.

## Que contient une campagne orchestrée ? {#gs-ms-campaign-inside}

La zone de travail de campagne orchestrée est une représentation de ce qui est censé se produire. Il décrit les différentes tâches à effectuer et la manière dont elles sont liées.

![image montrant une zone de travail de campagne orchestrée](assets/canvas-example.png){zoomable="yes"}{zoomable="yes"}

Chaque campagne orchestrée contient :

* des **Activités** : une activité est une tâche à effectuer. Les différentes activités disponibles sont représentées sur le diagramme par des icônes. Chaque activité possède des propriétés spécifiques et d’autres propriétés communes à toutes les activités.

  Dans un diagramme de campagne orchestré, une même activité peut générer plusieurs tâches, notamment en cas de boucle ou d&#39;actions récurrentes.

* **Transitions** : les transitions relient une activité source à une activité de destination et définissent leur ordre.

* **Tables de travail** : la table de travail contient toutes les informations véhiculées par la transition. Chaque campagne orchestrée utilise plusieurs tables de travail. Les données transmises dans ces tableaux peuvent être utilisées tout au long du cycle de vie de la campagne orchestrée.

## Statuts des campagnes {#status}

Les campagnes orchestrées peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la campagne orchestrée a été créée. Il n’a pas encore été publié.
* **[!UICONTROL Publication]** : la campagne orchestrée est en cours de publication.
* **[!UICONTROL En direct]** : la campagne orchestrée a été publiée et est en cours d’exécution.
* **[!UICONTROL Planifié]** : l’exécution de la campagne orchestrée a été planifiée.
* **[!UICONTROL Terminé]** : l’exécution de la campagne orchestrée est terminée. Le statut Terminé est automatiquement attribué jusqu’à 3 jours après qu’une campagne a terminé l’envoi des messages sans erreur.
* **[!UICONTROL Fermé]** : ce statut s’affiche lorsqu’une campagne récurrente a été arrêtée.
<!--Comment une campaign devient Closed?
[CPR] : A vérifier avec Fred si cette fonctionalité est toujours d'actualité. Normalement c'est sur action de l'utilisateur sur une campaine récurrente only
= pas trouvé-->
* **[!UICONTROL Archivé]** : la campagne orchestrée a été archivée. Toutes les campagnes archivées sont supprimées selon un nouveau planning progressif 30 jours après la date de la dernière modification. Vous pouvez dupliquer une campagne archivée si nécessaire pour continuer à travailler dessus.
<!--Comment une campaign devient Archived?
[CPR] : Soit par action manuel sur une campagne en statut "final" (Completed, Closed, Stopped, etc. ...)
= pas trouvé -->
* **[!UICONTROL Arrêté]** : l&#39;exécution de la campagne orchestrée a été arrêtée. Pour redémarrer la campagne, vous devez la dupliquer.

## Dupliquer et supprimer des campagnes orchestrées {#duplicate-delete}

Dans certains cas, vous devrez peut-être dupliquer une campagne orchestrée, par exemple pour exécuter une campagne qui a été arrêtée, ou pour modifier la fréquence d’exécution d’une campagne planifiée. Pour ce faire, cliquez sur le bouton ![image illustrant le bouton Autres actions](assets/do-not-localize/rule-builder-icon-more.svg) de l’inventaire des campagnes, puis sélectionnez **[!UICONTROL Dupliquer]**

<!--Une fois une campaign Scheduled, on ne peut plus changer l'execution frequency = la solution est de dupliquer la campaign ?
[CPR] : Actuellement oui, mais on est en discussion pour pouvoir revenir en mode "draft" et quelles seraient les actions à nouveau disponibles. A vérifier avec Fred-->

Pour supprimer une campagne, cliquez sur l’image ![bouton Autres actions](assets/do-not-localize/rule-builder-icon-more.svg) puis sélectionnez **[!UICONTROL Supprimer]**.

>[!NOTE]
>
>Seules les campagnes **[!UICONTROL Brouillon]** peuvent être supprimées.
