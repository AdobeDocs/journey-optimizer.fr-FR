---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Déduplication
description: Découvrir comment utiliser l’activité Déduplication
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 88%

---

# Déduplication {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Champs pour identifier les doublons"
>abstract="Dans la section **Champs pour identifier des doublons**, cliquez sur le bouton **Ajouter un attribut** pour indiquer les champs pour lesquels des valeurs identiques permettent d’identifier les doublons, par exemple : adresse e-mail, prénom, nom, etc. L’ordre des champs vous permet de spécifier ceux à traiter en premier."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Activité Déduplication"
>abstract="L’activité **Déduplication** permet de supprimer les doublons dans le ou les résultats des activités entrantes. Elle est principalement utilisée à la suite des activités de ciblage et avant les activités permettant l’utilisation des données ciblées."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Générer un complément"
>abstract="Vous pouvez générer une transition sortante supplémentaire avec la population restante, qui a été exclue en tant que doublon. Pour ce faire, activez l’option **Générer un complément**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Paramètres de déduplication"
>abstract="Pour supprimer des doublons dans les données entrantes, définissez la méthode de déduplication dans les champs ci-dessous. Par défaut, un seul enregistrement est conservé. Vous devez également sélectionner le mode de déduplication en fonction d’une expression ou d’un attribut. Par défaut, l’enregistrement à conserver en dehors des doublons est sélectionné de manière aléatoire."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interrogation de la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](gs-campaign-creation.md) | [Créer une campagne orchestrée](create-orchestrated-campaign.md)<br/><br/>[Orchestrer des activités](orchestrate-activities.md)<br/><br/>[Envoyer des messages avec des campagnes orchestrées](send-messages.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser la requête Modeler](orchestrated-query-modeler.md)<br/><br/>[créer votre première requête](build-query.md)<br/><br/>[modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Combiner](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

L’activité **Déduplication** est une activité de **ciblage**. Cette activité permet de supprimer les doublons dans le ou les résultats des activités entrantes, par exemple les profils dupliqués dans la liste des profils destinataires. L’activité **Déduplication** est généralement utilisée à la suite des activités de ciblage et avant les activités permettant d’utiliser les données ciblées.

## Configurer l’activité Déduplication{#deduplication-configuration}

Pour configurer l’activité **Déduplication**, procédez comme suit :

![](../assets/workflow-deduplication.png)

1. Ajoutez une activité **Déduplication** à votre campagne orchestrée.

1. Dans la section **Champs pour identifier des doublons**, cliquez sur le bouton **Ajouter un attribut** pour indiquer les champs pour lesquels des valeurs identiques permettent d’identifier les doublons, par exemple : adresse e-mail, prénom, nom, etc. L’ordre des champs vous permet de spécifier ceux à traiter en premier.

1. Dans la section **Paramètres de déduplication**, sélectionnez le nombre de **Doublons à conserver** uniques. La valeur par défaut de champ est 1. La valeur 0 permet de conserver tous les doublons.

   Par exemple, si les enregistrements A et B sont considérés comme des doublons de l’enregistrement Y et qu’un enregistrement C est considéré comme un doublon de l’enregistrement Z :

   * Si la valeur du champ est 1 : seuls les enregistrements Y et Z sont conservés.
   * Si la valeur du champ est 0 : tous les enregistrements sont conservés.
   * Si la valeur du champ est 2 : les enregistrements C et Z sont conservés et deux enregistrements parmi A, B et Y sont conservés, par hasard ou selon la méthode de déduplication sélectionnée par la suite.

1. Sélectionnez la **méthode de déduplication** à utiliser :

   * **Sélection aléatoire** : sélectionne au hasard l’enregistrement à conserver parmi les doublons.
   * **À partir d’une expression** : permet de conserver les enregistrements dont la valeur de l’expression renseignée est la plus petite ou la plus grande.
   * **Valeurs non vides** : conserve les enregistrements pour lesquels l’expression n’est pas vide.
   * **Par ordonnancement de valeurs** : définit un ordre de priorité des valeurs pour un ou plusieurs champs. Pour définir les valeurs, cliquez sur **Attributs** pour sélectionner un champ ou créez une expression, puis ajoutez la ou les valeurs dans le tableau correspondant. Pour définir un nouveau champ, cliquez sur le bouton **Ajouter** situé au-dessus de la liste des valeurs.

1. Cochez l’option **Générer le complément** si vous souhaitez exploiter la population restante. Le complément est constitué de tous les doublons. Une transition supplémentaire sera alors ajoutée à l’activité.

## Exemple{#deduplication-example}

Dans l’exemple suivant, utilisez une activité Déduplication pour exclure les doublons de la cible avant l’envoi d’une diffusion. Les profils dupliqués identifiés sont ajoutés à une audience dédiée qui peut être réutilisée si nécessaire. Choisissez l’adresse **e-mail** pour identifier les doublons. Conservez une entrée et sélectionnez la méthode de déduplication **aléatoire**.

![](../assets/workflow-deduplication-example.png)
