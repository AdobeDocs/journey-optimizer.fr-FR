---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Partage
description: Découvrez comment utiliser l’activité Partage dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 54%

---

# Partage {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Activité Partage"
>abstract="L’activité **Partage** permet de segmenter les populations entrantes en plusieurs sous-ensembles selon différents critères de sélection, tels que les règles de filtrage ou la taille de la population."


+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](../access-manage-orchestrated-campaigns.md) | [Étapes clés de création d’une campagne orchestrée](../gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](../orchestrate-activities.md)<br/><br/>[Lancez et surveillez la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser le créateur de règles](../orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](../build-query.md)<br/><br/>[Modifier les expressions](../edit-expressions.md)<br/><br/>[Reciblage](../retarget.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Activités de canal](channels.md) - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Enregistrer l’audience](save-audience.md) - <b>[Split](split.md)</b> - [Wait](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

L&#39;activité **[!UICONTROL Partage]** est une activité **[!UICONTROL Ciblage]** qui segmente la population entrante en plusieurs sous-ensembles en fonction de critères de sélection définis, tels que les règles de filtrage ou la taille de la population.

## Configurer l’activité Partage {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segments de l’activité de partage"
>abstract="Ajoutez autant de sous-ensembles que vous le souhaitez pour segmenter la population entrante.<br/></br>Lorsque l’activité **Partage** est exécutée, la population est segmentée entre les différents sous-ensembles dans l’ordre dans lequel ils sont ajoutés à l’activité. Avant de démarrer votre campagne orchestrée, assurez-vous d’avoir trié les sous-ensembles dans l’ordre qui vous convient à l’aide des boutons fléchés."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Filtre de l’activité Partage"
>abstract="Pour appliquer une condition de filtrage au sous-ensemble, cliquez sur **[!UICONTROL Créer un filtre]** et configurez la règle de filtrage souhaitée à l’aide du concepteur de requête. Par exemple, incluez les profils de la population entrante dont l’adresse e-mail existe dans la base de données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="Limite de l’activité Partage"
>abstract="Pour limiter le nombre de profils sélectionnés par le sous-ensemble, activez la fonction **[!UICONTROL Activer la limite]** et indiquez le nombre ou les pourcentages de la population à inclure."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="Tri de l’activité Partage"
>abstract="Lorsque vous définissez une limite de population pour un sous-ensemble, vous pouvez classer les profils sélectionnés en fonction d’un attribut de profil spécifique, dans un ordre croissant ou décroissant. Pour ce faire, activez l’option **Activer le tri**. Par exemple, vous pouvez restreindre un sous-ensemble afin de n’inclure que les 50 premiers profils qui ont le montant d’achat le plus élevé."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="Générer un complément pour l’activité Partage"
>abstract="Une fois que vous avez paramétré tous les sous-ensembles, vous pouvez sélectionner la population restante qui ne correspond à aucun des sous-ensembles et les inclure dans une transition sortante supplémentaire. Pour ce faire, activez l’option **Générer un complément**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="Générer tous les sous-ensembles dans le même tableau"
>abstract="Activez cette option pour regrouper tous les sous-ensembles dans une seule transition sortante."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="Ignorer la transition vide"
>abstract="Activez l’option **[!UICONTROL Ignorer la transition vide]** pour désactiver la transition sortante pour ce sous-ensemble si la population entrante est vide."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="Permettre le chevauchement des populations de sortie"
>abstract=" L’option **[!UICONTROL Permettre le chevauchement des populations de sortie]** permet de gérer les populations qui appartiennent à plusieurs sous-ensembles. Lorsque la case n’est pas cochée, l’activité de partage fait en sorte qu’une personne destinataire ne puisse pas apparaître dans plusieurs transitions de sortie, même si elle répond aux critères de plusieurs sous-ensembles. Elles apparaissent ainsi dans la cible du premier onglet avec les critères correspondants. Lorsque la case est activée, les destinataires se trouvent dans plusieurs sous-ensembles s’ils ou elles répondent à leurs critères de filtre."

Pour configurer l’activité **[!UICONTROL Partage]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Partage]** à votre campagne orchestrée.

1. Le volet de configuration des activités s’ouvre avec un sous-ensemble par défaut. Cliquez sur le bouton **[!UICONTROL Ajouter un segment]** pour ajouter autant de sous-ensembles que vous le souhaitez pour segmenter la population entrante.

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >L&#39;activité **Partage** traite les sous-ensembles dans l&#39;ordre dans lequel ils sont ajoutés. Par exemple, si le premier sous-ensemble capture 70 % de la population, le suivant applique ses critères aux 30 % restants.
   >
   >Avant d’exécuter votre campagne orchestrée, assurez-vous que les sous-ensembles sont triés comme prévu. Utilisez les boutons fléchés pour ajuster leur position.

1. Une fois les sous-ensembles ajoutés, l’activité propose autant de transitions en sortie que de sous-ensembles : Nous vous recommandons vivement de modifier le libellé de chaque sous-ensemble pour les identifier facilement dans la zone de travail de campagne orchestrée.

1. Configurez les filtres pour chaque sous-ensemble :

   1. Cliquez sur un sous-ensemble pour en ouvrir les paramètres.

   1. Cliquez sur **[!UICONTROL Créer un filtre]** pour définir des règles de filtrage à l’aide du modéliseur de requêtes, par exemple, pour sélectionner des profils avec une adresse e-mail valide.

      ![](../assets/orchestrated-split-1.png)

   1. Pour limiter le nombre de profils sélectionnés, activez **[!UICONTROL Activer la limite]** et spécifiez un nombre ou un pourcentage.

   1. Pour ignorer une transition lorsque le sous-ensemble est vide, activez **[!UICONTROL Ignorer la transition vide].**

1. Pour inclure des profils qui ne correspondent à aucun sous-ensemble, activez **[!UICONTROL Générer le complémentaire]**. Cela crée une transition sortante supplémentaire pour la population restante.

   >[!NOTE]
   >
   >Activez l&#39;option **[!UICONTROL Générer tous les sous-ensembles dans la même table]** pour regrouper tous les sous-ensembles en une seule transition.

1. Utilisez **[!UICONTROL Permettre le chevauchement des populations de sortie]** pour autoriser les profils à apparaître dans plusieurs sous-ensembles :

   * **Si cette option n’est pas cochée** chaque profil est affecté à un seul sous-ensemble, le premier dont il correspond aux critères, même s’il est admissible pour d’autres sous-ensembles.

   * **Si cette case est cochée** les profils peuvent être inclus dans plusieurs sous-ensembles s’ils répondent aux critères de chacun d’eux.

L’activité est désormais configurée. Lors de l&#39;exécution de la campagne orchestrée, la population sera segmentée en différents sous-ensembles, dans l&#39;ordre dans lequel ils ont été ajoutés à l&#39;activité.

## Exemple{#split-example}

Dans l’exemple suivant, l’activité **[!UICONTROL Partage]** sert à segmenter une audience en sous-ensembles distincts en fonction du canal de communication que nous voulons utiliser :

* **Sous-ensemble 1 « e-mail »** : inclut les profils qui ont fourni un numéro de téléphone.

* **Sous-ensemble 2 « sms »** : cible les profils dont le numéro de téléphone mobile est stocké dans la base de données.

* **Transition complémentaire** : capture les profils restants qui ne répondent aux critères d’aucun des sous-ensembles.

![](../assets/orchestrated-split-3.png)
