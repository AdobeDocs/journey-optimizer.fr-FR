---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Réconciliation
description: Découvrez comment utiliser l’activité Réconciliation dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 61%

---

# Réconciliation {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Activité Réconciliation"
>abstract="L’activité **Réconciliation** est une activité de **Ciblage** vous permettant de définir le lien entre Adobe Journey Optimizer et les données dans une table de travail."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Champ de sélection de la réconciliation"
>abstract="Champ de sélection de la réconciliation"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Condition de création de réconciliation"
>abstract="Condition de création de réconciliation"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Complément de génération de réconciliation"
>abstract="Complément de génération de réconciliation"

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interrogation de la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](../gs-campaign-creation.md) | [Créer une campagne orchestrée](../create-orchestrated-campaign.md)<br/><br/>[Orchestrer des activités](../orchestrate-activities.md)<br/><br/>[Envoyer des messages avec des campagnes orchestrées](../send-messages.md)<br/><br/>[Démarrer et surveiller la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser la requête Modeler](../orchestrated-rule-builder.md)<br/><br/>[créer votre première requête](../build-query.md)<br/><br/>[modifier des expressions](../edit-expressions.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - [Combiner](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L&#39;activité **Réconciliation** est une activité de **Ciblage** qui permet de définir le lien entre les données de Adobe Journey Optimizer et les données d&#39;une table de travail, par exemple les données chargées depuis un fichier externe.

L’activité Enrichissement vous permet d’ajouter des données supplémentaires à votre campagne orchestrée, par exemple, en combinant des données provenant de plusieurs sources ou en les liant à une ressource temporaire. En revanche, l’activité Réconciliation est utilisée pour mettre en correspondance des données non identifiées ou externes avec des ressources existantes dans la base de données.

Le rapprochement nécessite que les enregistrements associés existent déjà dans le système. Par exemple, si vous importez un fichier d’achat répertoriant les produits, les horodatages et les informations client, les produits et les clients doivent déjà être présents dans la base de données pour établir la liaison.

## Configurer l’activité Réconciliation {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimension de ciblage"
>abstract="Sélectionnez la nouvelle dimension de ciblage. Une dimension vous permet de définir la population ciblée : destinataires, personnes abonnées à l’application, opérateurs et opératrices, personnes eabonnés, etc. Par défaut, la dimension de ciblage actuelle est sélectionnée."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Règles de réconciliation"
>abstract="Sélectionnez les règles de réconciliation à utiliser pour la déduplication. Pour utiliser des attributs, sélectionnez l’option **Attributs simples** et choisissez les champs source et de destination. Pour créer votre propre condition de réconciliation à l’aide du concepteur de requête, sélectionnez l’option **Conditions de réconciliation avancées**."
>additional-url="https://experienceleague.adobe.com/fr/docs/campaign-web/v8/query-database/query-modeler-overview" text="Utiliser le concepteur de requête"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Sélectionner la dimension de ciblage"
>abstract="Sélectionnez la dimension de ciblage de vos données entrantes avec lesquelles vous souhaitez effectuer la réconciliation."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=fr#targeting-dimensions" text="Dimensions de ciblage"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Conserver les données non réconciliées"
>abstract="Par défaut, les données non réconciliées sont conservées dans la transition sortante et disponibles dans la table de travail pour une utilisation ultérieure. Pour supprimer les données non réconciliées, désactivez l’option **Conserver les données non réconciliées**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Attribut de réconciliation"
>abstract="Sélectionnez l’attribut à utiliser pour réconcilier les données, puis cliquez sur Confirmer."

Pour configurer l’activité **Réconciliation**, procédez comme suit :

1. Ajoutez une activité **Réconciliation** dans votre campagne orchestrée.

1. Sélectionnez la nouvelle dimension de ciblage. Une dimension vous permet de définir la population ciblée : destinataires, abonnés de l’application, opérateurs, abonnés, etc.

1. Sélectionnez le ou les champs à utiliser pour la réconciliation. Vous pouvez utiliser un ou plusieurs critères de réconciliation.

   1. Pour utiliser des attributs afin de réconcilier des données, sélectionnez l’option **Attributs simples**. Le champ **Source** répertorie les champs disponibles dans la transition d’entrée, qui doivent être réconciliés. Le champ **Destination** correspond aux champs de la dimension de ciblage sélectionnée. Les données sont réconciliées lorsque la source et la destination sont égales. Par exemple, sélectionnez les champs **E-mail** pour dédupliquer des profils en fonction de leur adresse e-mail.

      Pour ajouter un autre critère de réconciliation, cliquez sur le bouton **Ajouter une règle**. Si plusieurs conditions de jointure sont indiquées, elles doivent TOUTES être vérifiées pour que le lien entre les données puisse se faire.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Pour utiliser d’autres attributs afin de réconcilier des données, sélectionnez l’option **Conditions avancées de réconciliation**. Vous pouvez ensuite créer votre propre condition de réconciliation à l&#39;aide du modéliseur de requêtes.

1. Vous pouvez filtrer les données à réconcilier à l’aide du bouton **Créer un filtre**. Vous pouvez ainsi créer une condition personnalisée à l’aide du concepteur de requête.

Par défaut, les données non réconciliées sont conservées dans la transition sortante et disponibles dans la table de travail pour une utilisation ultérieure. Pour supprimer les données non réconciliées, désactivez l’option **Conserver les données non réconciliées**.
