---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Branchement
description: Découvrez comment utiliser l’activité Branchement dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: c46c202d68613f08e2d2b23ea882fb6561669b08
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 62%

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

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interrogation de la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](../gs-campaign-creation.md) | [Créer une campagne orchestrée](../create-orchestrated-campaign.md)<br/><br/>[Orchestrer des activités](../orchestrate-activities.md)<br/><br/>[Envoyer des messages avec des campagnes orchestrées](../send-messages.md)<br/><br/>[Démarrer et surveiller la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser la requête Modeler](../orchestrated-query-modeler.md)<br/><br/>[créer votre première requête](../build-query.md)<br/><br/>[modifier des expressions](../edit-expressions.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Combiner](combine.md) - [Deduplication](/deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

L’activité **Branchement** est une activité de **contrôle de flux**. Elle permet de créer des transitions sortantes afin de démarrer plusieurs activités en parallèle.

## Configurer l’activité Branchement{#fork-configuration}

Pour configurer l’activité **Branchement**, procédez comme suit :

![](../assets/workflow-fork.png)

1. Ajoutez une activité **Branchement** à votre campagne orchestrée.
1. Cliquez sur **Ajouter une transition** pour ajouter une nouvelle transition sortante. Par défaut, deux transitions sont définies.
1. Ajoutez un libellé à chacune de vos transitions.

## Exemple{#fork-example}

Dans l’exemple suivant, nous utilisons deux activités **Branchement** :

* Une avant les deux requêtes, pour les exécuter en même temps.
* Une après l’intersection, pour envoyer simultanément un e-mail et un SMS à la population ciblée.

![](../assets/workflow-fork-example.png)
