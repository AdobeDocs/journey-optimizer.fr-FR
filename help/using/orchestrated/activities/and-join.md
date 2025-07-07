---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Rendez-vous
description: Découvrez comment utiliser l’activité Rendez-vous dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 38%

---

# Rendez-vous {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Activité Rendez-vous"
>abstract="L’activité **Rendez-vous** vous permet de synchroniser plusieurs branches d’exécution d’une campagne orchestrée. Elle est déclenchée une fois toutes les activités précédentes terminées. Vous pouvez ainsi vous assurer que certaines activités sont terminées avant de continuer à exécuter la campagne orchestrée."


+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](../access-manage-orchestrated-campaigns.md) | [Étapes clés de création d’une campagne orchestrée](../gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](../orchestrate-activities.md)<br/><br/>[Lancez et surveillez la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser le créateur de règles](../orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](../build-query.md)<br/><br/>[Modifier les expressions](../edit-expressions.md)<br/><br/>[Reciblage](../retarget.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/><b>[Et-joindre](and-join.md)</b> - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Activités de canal](channels.md) - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L’activité **[!UICONTROL Rendez-vous]** est une activité de **[!UICONTROL contrôle de flux]**. Elle permet de synchroniser plusieurs branches d’exécution d’une campagne orchestrée.

L’activité Rendez-vous ne déclenche sa transition sortante qu’une fois toutes les transitions entrantes activées, c’est-à-dire quand toutes les activités précédentes sont terminées. Vous pouvez ainsi vous assurer que certaines activités sont terminées avant de continuer à exécuter la campagne orchestrée.

## Configurer l’activité Rendez-vous{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Options de fusion"
>abstract="Sélectionnez les activités auxquelles vous souhaitez adhérer. Dans l’**Ensemble principal**, choisissez la population de transition entrante à conserver."

Pour configurer l’activité **[!UICONTROL Rendez-vous]**, procédez comme suit :

![](../assets/workflow-andjoin.png)

1. Ajoutez plusieurs activités, telles que des activités de canal, pour créer au moins deux branches d’exécution distinctes.

1. Insérez une activité **[!UICONTROL Rendez-vous]** dans l’une des branches.

1. Sous la section **[!UICONTROL Options de fusion]**, sélectionnez toutes les activités précédentes à joindre.

1. Dans le menu déroulant Ensemble de Principal **&#x200B;**, choisissez la population de transition entrante que vous souhaitez conserver.

## Exemple{#and-join-example}

Cet exemple illustre deux branches de campagne coordonnée, chacune disposant d’une diffusion e-mail, l’une ciblant les membres Gold et l’autre les membres Silver. La **[!UICONTROL Rendez-vous]** s’active une fois les deux transitions entrantes déclenchées. Le SMS ne sera envoyé qu’une fois les deux diffusions par e-mail terminées, après un délai de 7 jours.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
