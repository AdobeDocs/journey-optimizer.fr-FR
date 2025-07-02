---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Branchement
description: Découvrez comment utiliser l’activité Branchement dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 7de878c316e966129e7dede37f132938d2abbdf8
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 35%

---

# Branchement {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Activité Branchement"
>abstract="L’activité **Branchement** permet de créer des transitions sortantes afin de lancer plusieurs activités en parallèle."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transitions de l’activité Branchement"
>abstract="Par défaut, deux transitions sont créées avec une activité **Branchement**. Cliquez sur le bouton **Ajouter une transition** pour définir une transition sortante supplémentaire, puis renseignez son libellé."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](../gs-campaign-creation.md) | [Créer une campagne orchestrée](../create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](../orchestrate-activities.md)<br/><br/><br/>[Démarrer et surveiller la campagne](../start-monitor-campaigns.md)<br/><br/>[le reporting](../reporting-campaigns.md) | [Utiliser la requête Modeler](../orchestrated-rule-builder.md)<br/><br/>[créer votre première requête](../build-query.md)<br/><br/>[modifier des expressions](../edit-expressions.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Activités de canal](channels.md) - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L’activité **[!UICONTROL Branchement]** est un composant **[!UICONTROL Contrôle de flux]** qui permet de créer plusieurs transitions sortantes et d’exécuter plusieurs activités en parallèle.

## Configurer l’activité Branchement{#fork-configuration}

Pour configurer l’activité **[!UICONTROL Branchement]**, procédez comme suit :

![](../assets/workflow-fork.png)

1. Ajoutez une activité **[!UICONTROL Branchement]** à votre campagne orchestrée.

1. Définissez un **[!UICONTROL libellé]**.

1. Attribuez un libellé à chaque transition sortante. Par défaut, deux transitions sont fournies.

1. Pour supprimer une transition, cliquez sur l’icône ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Si nécessaire, cliquez sur **[!UICONTROL Ajouter une transition]** pour ajouter une transition sortante supplémentaire.
