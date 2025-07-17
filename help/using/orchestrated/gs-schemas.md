---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment créer un schéma relationnel dans Adobe Experience Platform en chargeant un fichier DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 5%

---

# Prise en main des schémas et des éléments associés {#file-upload-schema}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul><br/><br/>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

Ce guide vous guide tout au long du processus de création d’un schéma relationnel, de configuration d’un jeu de données pour des campagnes orchestrées, d’ingestion de données via une source S3 et d’interrogation des données ingérées dans la plateforme AP.

Dans cet exemple, la configuration comprend l’intégration de deux entités clés, **Transactions de fidélité** et **Récompenses de fidélité**, et leur liaison à des entités de base existantes **Destinataires** et **Marques**.

![](assets/do-not-localize/schema_admin.png)

1. [Création d’un schéma relationnel et d’un jeu de données associé](#schema)

   Définissez le modèle de données relationnel pour les campagnes orchestrées, y compris les entités **Loyalty Memberships**, **Loyalty Transactions** et **Loyalty Rewards**, ainsi que les clés et attributs de contrôle de version requis.

1. [Schéma du lien](#link-schema)

   Liez l’entité **Transactions de fidélité** à **Destinataires** et **Récompenses de fidélité** à **Marques**, afin de créer un modèle de données connecté prenant en charge les parcours client personnalisés.

1. [Ingérer des données](#ingest)

   Insérez des données dans Adobe Experience Platform à partir de sources prises en charge telles que SFTP, l’espace de stockage dans le cloud ou des bases de données.


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
