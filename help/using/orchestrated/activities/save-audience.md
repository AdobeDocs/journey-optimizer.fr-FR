---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Enregistrer l’audience
description: Découvrez comment utiliser l’activité Enregistrer l’audience dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 48%

---

# Enregistrer l’audience {#save-audience}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](orchestrate-activities.md)<br/><br/><b>[Lancez et surveillez la campagne](start-monitor-campaigns.md)</b><br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

L&#39;activité **[!UICONTROL Sauvegarde d&#39;audience]** est une activité **[!UICONTROL Ciblage]** qui permet de mettre à jour une audience existante ou d&#39;en créer une nouvelle à partir de la population générée précédemment dans la campagne orchestrée. Une fois créées, ces audiences sont ajoutées à la liste des audiences de l’application. Vous pouvez y accéder à partir du menu **[!UICONTROL Audiences]**.

Cette activité est particulièrement utile pour conserver les segments d’audience calculés dans la même campagne orchestrée, et les rendre disponibles pour réutilisation dans les futures campagnes. Il est généralement connecté à d’autres activités de ciblage, telles que **[!UICONTROL Créer une audience]** ou **[!UICONTROL Combiner]**, pour capturer et enregistrer la population résultante.

## Configurer l’activité Enregistrer l’audience {#save-audience-configuration}

Pour configurer l’activité **Enregistrer l’audience**, procédez comme suit :

1. Ajoutez une activité **Enregistrer l’audience** à votre campagne orchestrée.

1. Dans la liste déroulante **Mode**, sélectionnez l’action à effectuer :

   * **Créer ou mettre à jour une audience existante** : définissez un **libellé d’audience**. Si l’audience existe déjà, elle est mise à jour, sinon une nouvelle audience est créée.

   * **Mettre à jour une audience existante** : sélectionnez l’**Audience** que vous souhaitez mettre à jour parmi la liste des audiences existantes.

1. Sélectionnez le **mode de mise à jour** qui s’applique aux audiences existantes :

   * **Remplacer le contenu de l’audience par les nouvelles données** : tout le contenu de l’audience est remplacé et les anciennes données sont perdues. Seules les données issues de la transition entrante de l’activité **Enregistrer l’audience** sont conservées. Cette option écrase le type et la dimension de ciblage de l’audience mise à jour.

   * **Compléter l’audience avec les nouvelles données** : l’ancien contenu de l’audience est conservé et les données sont complétées avec celles issues de la transition entrante de l’activité **Enregister l’audience**.

1. Cochez l’option **Générer une transition sortante** si vous souhaitez ajouter une transition après l’activité **Enregistrer l’audience**.

Le contenu de l’audience enregistrée est ensuite disponible dans la vue détaillée de l’audience, accessible depuis le menu **Audiences**. Les colonnes disponibles dans cette vue correspondent aux colonnes de la transition entrante de l’activité de campagne orchestrée **Sauvegarde d’audience**.

## Exemple {#save-audience-example}

L’exemple suivant illustre une mise à jour simple de l’audience à partir du ciblage. Un planificateur exécute la campagne orchestrée une fois par mois. Une requête récupère tous les profils abonnés aux différentes applications disponibles. L’activité **Enregistrer l’audience** met à jour l’audience en supprimant les profils qui se sont désabonnés du service depuis la dernière exécution de campagne orchestrée et en ajoutant les profils nouvellement abonnés.
