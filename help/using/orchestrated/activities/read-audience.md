---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Lecture d’audience
description: Découvrez comment utiliser l’activité Lecture d’audience dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 19%

---

# Lecture d’audience {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Lire l’audience** permet de sélectionner l’audience qui va entrer dans la campagne orchestrée. Il peut s’agir d’une audience Adobe Experience Platform existante ou d’une audience extraite d’un fichier CSV. Lors de l’envoi de messages dans le cadre d’une campagne orchestrée, l’audience du message n’est pas définie dans l’activité de canal, mais dans une activité **Lire l’audience** ou **Créer une audience**."


+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Prise en main des schémas et des jeux de données](../gs-schemas.md)</li><li>[Schéma manuel](../manual-schema.md)</li><li>[Schéma de chargement de fichier](../file-upload-schema.md)</li><li>[ Ingérer des données ](../ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](../access-manage-orchestrated-campaigns.md) | [Étapes clés de création d’une campagne orchestrée](../gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](../orchestrate-activities.md)<br/><br/>[Lancez et surveillez la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser le créateur de règles](../orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](../build-query.md)<br/><br/>[Modifier les expressions](../edit-expressions.md)<br/><br/>[Reciblage](../retarget.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Activités de canal](channels.md) - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

L&#39;activité **[!UICONTROL Lecture d&#39;audience]** vous permet de récupérer une audience existante, précédemment enregistrée ou importée, et de la réutiliser dans une campagne orchestrée. Cette activité est particulièrement utile pour cibler un ensemble prédéfini de profils sans avoir à exécuter un nouveau processus de segmentation.

Une fois l’audience chargée, vous pouvez éventuellement l’affiner en sélectionnant un champ d’identité unique et en enrichissant l’audience avec des attributs de profil supplémentaires à des fins de ciblage, de personnalisation ou de création de rapports.

## Configuration de l&#39;activité Lecture d&#39;audience {#read-audience-configuration}

Pour configurer l’activité **[!UICONTROL Lecture d’audience]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Lecture d’audience]** à votre campagne orchestrée.

   ![](../assets/read-audience-1.png)

1. Saisissez un **[!UICONTROL libellé]** pour votre activité.

1. Cliquez sur ![icône de recherche de dossier](../assets/do-not-localize/folder-search.svg) pour sélectionner l’audience que vous souhaitez cibler pour votre campagne orchestrée.

   ![](../assets/read-audience-2.png)

1. Sélectionnez l’**[!UICONTROL Entité]** utilisée pour identifier de manière unique les profils de votre audience.

   ![](../assets/read-audience-3.png)

1. Sélectionnez **[!UICONTROL Ajouter un attribut de profil]** pour enrichir votre audience sélectionnée avec des données supplémentaires. L’audience obtenue contient une liste de destinataires, enrichie chacun des attributs de profil sélectionnés.

1. Sélectionnez les **[!UICONTROL Attributs]** à ajouter à votre audience.

   ![](../assets/read-audience-4.png)

## Exemple

Dans l’exemple ci-dessous, l’activité **[!UICONTROL Lecture d’audience]** permet de récupérer une audience créée et enregistrée précédemment pour les profils s’étant abonnés à la newsletter. L’audience est ensuite enrichie de l’attribut **Loyalty membership** pour permettre le ciblage des utilisateurs qui sont membres inscrits au programme de fidélité.

![](../assets/read-audience-5.png)
