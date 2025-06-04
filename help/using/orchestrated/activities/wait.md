---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité d’attente dans des campagnes orchestrées
description: Découvrez comment utiliser l’activité Attente dans les campagnes orchestrées
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 52226a4374fa6321b31ac2d57f76a48594df1c51
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 11%

---

# Attente {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Activité Attente"
>abstract="L’activité **Attente** est utilisée pour retarder la transition d’une activité à une autre."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interrogation de la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](../gs-campaign-creation.md) | [Créer une campagne orchestrée](../create-orchestrated-campaign.md)<br/><br/>[Orchestrer des activités](../orchestrate-activities.md)<br/><br/>[Envoyer des messages avec des campagnes orchestrées](../send-messages.md)<br/><br/>[Démarrer et surveiller la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser la requête Modeler](../orchestrated-query-modeler.md)<br/><br/>[créer votre première requête](../build-query.md)<br/><br/>[modifier des expressions](../edit-expressions.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Combiner](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L’activité **Attente** est un composant **Contrôle de flux** utilisé pour introduire un délai entre deux activités dans une campagne orchestrée. Cela permet de vous assurer que vos activités de suivi arrivent à un meilleur moment et sont plus pertinentes par rapport à l’interaction client.

Par exemple, vous pouvez attendre quelques jours après une diffusion e-mail pour suivre les ouvertures et les clics avant d’envoyer un message de relance.

## Configuration{#wait-configuration}

Pour configurer l’activité d’**attente**, procédez comme suit :

1. Ajoutez une activité **Attente** dans votre campagne orchestrée.

1. Sélectionnez le Type d’attente qui correspond le mieux à vos besoins :

   * **Durée** : indiquez un délai en secondes, minutes, heures ou jours avant de passer à l’activité suivante.

   * **Heure fixe** : définissez une date et une heure spécifiques après lesquelles l’activité suivante commencera.

   ![](../assets/wait_activity.png)

## Exemple{#wait-example}

L’exemple suivant illustre l’activité **Attente** dans un cas d’utilisation standard.  Un e-mail avec un code de promotion est envoyé aux profils qui célèbrent leur anniversaire. Après 29 jours, un SMS est envoyé au même groupe pour leur rappeler que leur code de promotion d’anniversaire va expirer.

![](../assets/wait-example.png)
