---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Créer une audience
description: Découvrez comment utiliser l’activité Créer une audience dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 31%

---

# Créer une audience {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Créer une audience** vous permet de définir l’audience qui va entrer dans la campagne orchestrée. Lors de l’envoi de messages dans le cadre d’une campagne orchestrée, l’audience du message n’est pas définie dans l’activité de canal, mais dans une activité **Créer une audience**."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](orchestrate-activities.md)<br/><br/><b>[Lancez et surveillez la campagne](start-monitor-campaigns.md)</b><br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

En tant que spécialiste marketing, vous pouvez créer des segments d’audience complexes par le biais d’une interface intuitive, ce qui vous permet de cibler les utilisateurs et les utilisatrices en fonction d’un large éventail de critères et de comportements, afin d’adapter plus efficacement vos campagnes.

Pour ce faire, utilisez l’activité de ciblage **[!UICONTROL Créer une audience]**. Cette activité définit l’audience qui entre dans la campagne orchestrée. Lors de l’envoi de messages dans le cadre d’une campagne orchestrée, l’audience est définie dans l’activité **[!UICONTROL Créer une audience]** et non dans la campagne orchestrée.

## Configurer l’activité Créer une audience {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="Sélectionnez votre audience de la même manière que vous utilisez une audience lors de la conception d’une nouvelle diffusion."

Pour configurer l’activité **[!UICONTROL Créer une audience]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Créer une audience]**.

   ![](../assets/build-audience.png)

1. Définissez un **[!UICONTROL libellé]**.

1. Configurez votre audience en suivant les étapes présentées dans les onglets ci-dessous.

1. Choisissez la **[!UICONTROL dimension de ciblage]**. La dimension de ciblage permet de définir la population ciblée par l’opération : personnes destinataires, personnes bénéficiaires d’un contrat, opérateurs et opératrices, personnes abonnées, etc. Par défaut, la cible est sélectionnée parmi les destinataires.

1. Cliquez sur **[!UICONTROL Continuer]**.

1. Utilisez le modéliseur de requête pour définir votre requête. [En savoir plus sur Query Modeler dans cette section](../orchestrated-rule-builder.md)

1. Indiquez si une transition sortante doit être générée lorsque l’audience est vide.

## Exemples{#build-audience-examples}

Voici un exemple de campagne orchestrée avec deux activités **[!UICONTROL Créer une audience]**. La première cible les profils qui ont des articles dans leur panier, suivie d’une diffusion par e-mail. La seconde cible les profils avec une liste de souhaits, suivie d’une diffusion par SMS.

![](../assets/build-audience-2.png)
