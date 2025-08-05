---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Enregistrer l’audience
description: Découvrez comment utiliser l’activité Enregistrer l’audience dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 458e0b19725147e0a3ad34891ca55b61f1ac44a8
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 39%

---

# Enregistrer l’audience {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Activité Enregistrer l’audience"
>abstract="L’activité **Enregistrer l’audience** est une activité de **Ciblage** qui permet de mettre à jour une audience existante ou d’en créer une nouvelle à partir de la population générée précédemment dans la campagne orchestrée. Une fois créées, ces audiences sont ajoutées à la liste des audiences de l’application. Vous pouvez y accéder à partir du menu **Audiences**."


+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Commencer avec des schémas et des jeux de données](../gs-schemas.md)</li><li>[Schéma manuel](../manual-schema.md)</li><li>[Schéma de chargement de fichier](../file-upload-schema.md)</li><li>[Ingérer des données](../ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](../access-manage-orchestrated-campaigns.md) | [Étapes clés de création d’une campagne orchestrée](../gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](../orchestrate-activities.md)<br/><br/>[Lancez et surveillez la campagne](../start-monitor-campaigns.md)<br/><br/>[Créez des rapports](../reporting-campaigns.md) | [Utiliser le créateur de règles](../orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](../build-query.md)<br/><br/>[Modifier les expressions](../edit-expressions.md)<br/><br/>[Reciblage](../retarget.md) | [Commencer avec les activités](about-activities.md)<br/><br/>Activités :<br/>[Rendez-vous](and-join.md) - [Créer une audience](build-audience.md) - [Changement de dimension](change-dimension.md) - [Activités de canal](channels.md) - [Combiner](combine.md) - [Déduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Branchement](fork.md) - [Réconciliation](reconciliation.md) - <b>[Enregistrer l’audience](save-audience.md)</b> - [Partage](split.md) - [Attente](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et est susceptible d’être modifié.

>[!ENDSHADEBOX]

L&#39;activité **[!UICONTROL Sauvegarde d&#39;audience]** est une activité **[!UICONTROL Ciblage]** utilisée pour créer une nouvelle audience ou mettre à jour une audience existante en fonction de la population générée précédemment dans la campagne orchestrée. Une fois enregistrée, l’audience est ajoutée à la liste des audiences de l’application et devient accessible à partir du menu **[!UICONTROL Audiences]**.

Elle est généralement utilisée pour capturer des segments d’audience créés dans la même campagne, ce qui les rend disponibles pour réutilisation dans de futures campagnes. En règle générale, il est connecté à d’autres activités de ciblage, telles que **[!UICONTROL Créer une audience]** ou **[!UICONTROL Combiner]**, pour enregistrer la population ciblée finale.

## Configurer l’activité Enregistrer l’audience {#save-audience-configuration}

Pour configurer l’activité **[!UICONTROL Enregistrer l’audience]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Enregistrer l’audience]** à votre campagne orchestrée.

1. Saisissez un **[!UICONTROL libellé d’audience]** qui identifiera l’audience enregistrée.

1. Choisissez un **[!UICONTROL champ de mappage de profil&#x200B;]** à partir de votre dimension de ciblage de campagne.

   ➡️ [Suivez les étapes présentées sur cette page pour créer votre dimension de ciblage de campagne](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Cliquez sur **[!UICONTROL Ajouter des mappages d’audience]** si vous souhaitez associer l’audience enregistrée à des champs d’identité supplémentaires.

   ![](../assets/save-audience-2.png)

1. Finalisez votre configuration en enregistrant et en publiant la campagne orchestrée. Cette opération génère et stocke votre audience.

Le contenu de l’audience enregistrée est alors disponible dans la vue détaillée de l’audience. Elle est accessible à partir du menu **[!UICONTROL Audiences]** ou peut être sélectionnée lors du ciblage d’une audience, par exemple avec une activité **[!UICONTROL Lecture d’audience]**.

![](../assets/save-audience-4.png)


## Exemple {#save-audience-example}

L’exemple suivant montre comment créer une audience simple à l’aide du ciblage. Une requête identifie tous les destinataires qui ont réservé un voyage au cours des 30 derniers jours en filtrant cette population dans votre campagne orchestrée. En choisissant **Destinataires - CRMID** comme **Dimension de ciblage**, l’audience cible chaque événement de réservation individuel plutôt que le destinataire dans son ensemble. L’activité **[!UICONTROL Enregistrer l’audience]** capture ensuite ces profils afin de créer une audience réutilisable des acheteurs et acheteuses récents.

![](../assets/save-audience-3.png)
