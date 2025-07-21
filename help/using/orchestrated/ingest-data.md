---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment importer des données dans Adobe Experience Platform à partir de sources prises en charge telles que le protocole SFTP, l’espace de stockage dans le cloud ou les bases de données.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 8%

---

# Ingestion de données {#ingest-data}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

Adobe Experience Platform permet d’ingérer des données à partir de sources externes tout en vous offrant la possibilité de structurer, d’étiqueter et d’améliorer les données entrantes à l’aide des services d’Experience Platform. Vous pouvez ingérer des données provenant de diverses sources telles que les applications Adobe, les stockages dans le cloud, des bases de données, etc.

## Avec le stockage dans le cloud {#ingest}


>[!IMPORTANT]
>
>Chaque jeu de données de Adobe Experience Platform ne prend en charge qu’un seul flux de données actif à la fois. Pour obtenir des instructions de configuration détaillées sur le changement de source de données, consultez cette [section](#cdc-ingestion).


Vous pouvez configurer un flux de données pour ingérer des données d’une source Amazon S3 dans Adobe Experience Platform. Une fois configuré, le flux de données permet l’ingestion automatisée et planifiée de données structurées et prend en charge les mises à jour en temps réel.

1. Dans le menu **[!UICONTROL Connexions]**, accédez au menu **[!UICONTROL Sources]**.

1. Sélectionnez la catégorie **[!UICONTROL Espace de stockage]** puis Amazon S3 et cliquez sur **[!UICONTROL Ajouter des données]**.

   ![](assets/admin_sources_1.png)

1. Connectez votre compte S3 :

   * Avec un compte existant

   * Avec un nouveau compte

   [En savoir plus dans la documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. Choisissez votre dossier **[!UICONTROL Format des données]**, **[!UICONTROL Délimiteur]** et **[!UICONTROL Type de compression]**.

1. Parcourez la source S3 connectée jusqu’à localiser les dossiers souhaités, par exemple **récompenses de fidélité** et **transactions de fidélité**.

1. Sélectionnez le dossier contenant vos données.

   La sélection d’un dossier garantit que tous les fichiers actuels et futurs avec la même structure sont automatiquement traités. Toutefois, la sélection d’un seul fichier nécessite de charger manuellement chaque nouvel incrément de données.

   ![](assets/S3_config_2.png)

1. Choisissez votre dossier **[!UICONTROL Format des données]**, **[!UICONTROL Délimiteur]** et **[!UICONTROL Type de compression]**. Vérifiez l’exactitude de vos données d’exemple, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/S3_config_1.png)

1. Cochez **[!UICONTROL Activer la capture de données Modifier]** pour effectuer une sélection parmi les jeux de données mappés aux schémas relationnels et pour lesquels une clé primaire et un descripteur de version sont définis.

1. Sélectionnez le [jeu de données créé précédemment](file-upload-schema.md) et cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/S3_config_3.png)

1. Dans la fenêtre **[!UICONTROL Mappage]**, vérifiez que chaque attribut de fichier source est correctement mappé avec les champs correspondants dans le schéma cible.

   Cliquez sur **[!UICONTROL Suivant]** une fois l’opération terminée.

   ![](assets/S3_config_4.png)

1. Configurez le flux de données **[!UICONTROL Planifier]** en fonction de la fréquence souhaitée.

1. Cliquez sur **[!UICONTROL Terminer]** pour créer le flux de données. Il s’exécute automatiquement selon le planning défini.

1. Dans le menu **[!UICONTROL Connexions]**, sélectionnez **[!UICONTROL Sources]** et accédez à l’onglet **[!UICONTROL Flux de données]** pour suivre l’exécution du flux, passer en revue les enregistrements ingérés et résoudre les erreurs.

   ![](assets/S3_config_5.png)

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
