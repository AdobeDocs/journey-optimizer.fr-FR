---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment importer des données dans Adobe Experience Platform à partir de sources prises en charge telles que le protocole SFTP, l’espace de stockage dans le cloud ou les bases de données.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 38%

---

# Ingérer des données {#ingest-data}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Commencer avec les activités](activities/about-activities.md)<br/><br/>Activités :<br/>[Rendez-vous](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Changement de dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combiner](activities/combine.md) - [Déduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Branchement](activities/fork.md) - [Réconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Partage](activities/split.md) - [Attente](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Pour modifier la source de données d’un jeu de données, vous devez d’abord supprimer le flux de données existant avant d’en créer un nouveau qui référence le même jeu de données et la nouvelle source.
>
>Adobe Experience Platform applique une relation stricte et individuelle entre les flux de données et les jeux de données. Cela vous permet de maintenir la synchronisation entre la source et le jeu de données pour une ingestion incrémentielle précise.

Adobe Experience Platform permet d’ingérer des données à partir de sources externes tout en vous offrant la possibilité de structurer, d’étiqueter et d’améliorer les données entrantes à l’aide des services d’Experience Platform. Vous pouvez ingérer des données provenant de diverses sources telles que les applications Adobe, les stockages dans le cloud, les bases de données, etc.

## Sources prises en charge pour les campagnes orchestrées {#supported}

Les sources suivantes sont prises en charge pour une utilisation avec des campagnes orchestrées :

<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Stockage dans le cloud</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Entrepôts de données cloud</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Zone d’atterrissage des données<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Chargements Basés Sur Des Fichiers</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Chargement de fichier local<a></td>
    </tr>

</tbody>
</table>

## Configurer un flux de données

Cet exemple montre comment configurer un flux de données qui ingère des données structurées dans Adobe Experience Platform. Le flux de données configuré prend en charge l’ingestion automatisée et planifiée et permet des mises à jour en temps réel.

1. Dans le menu **[!UICONTROL Connexions]**, accédez au menu **[!UICONTROL Sources]**.

1. Choisissez votre source en fonction de la [Sources prises en charge pour les campagnes orchestrées](#supported).

   ![](assets/admin_sources_1.png)

1. Connectez votre compte d’espace de stockage ou d’espace de stockage Google si vous avez choisi des sources basées sur le cloud.

   ![](assets/admin_sources_2.png)

1. Sélectionnez les données que vous souhaitez ingérer dans Adobe Experience Platform.

   ![](assets/S3_config_1.png)

1. Sur la page **[!UICONTROL Détails du jeu de données]**, cochez la case **[!UICONTROL Activer la capture de données Modifier]** pour afficher uniquement les jeux de données mappés à des schémas relationnels et incluant une clé primaire et un descripteur de version.

   >[!IMPORTANT]
   >
   > Pour les **sources basées sur des fichiers uniquement**, chaque ligne du fichier de données doit inclure une colonne `_change_request_type` avec des valeurs `U` (upsert) ou `D` (delete). Sans cette colonne, le système ne reconnaît pas les données comme prenant en charge le suivi des modifications et le bouton Campagne orchestrée n’apparaît pas, empêchant le jeu de données d’être sélectionné pour le ciblage.

   ![](assets/S3_config_6.png)

1. Sélectionnez le jeu de données créé précédemment et cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/S3_config_3.png)

1. Si vous utilisez uniquement des sources basées sur des fichiers, dans la fenêtre **[!UICONTROL Sélectionner les données]**, chargez vos fichiers locaux et prévisualisez leur structure et leur contenu.

   Notez que la taille maximale prise en charge est de 100MB.

1. Dans la fenêtre **[!UICONTROL Mappage]**, vérifiez que chaque attribut de fichier source est correctement mappé avec les champs correspondants dans le schéma cible.

   Cliquez sur **[!UICONTROL Suivant]** une fois l’opération terminée.

   ![](assets/S3_config_4.png)

1. Configurez le **[!UICONTROL Planning]** du flux de données en fonction de la fréquence souhaitée.

1. Cliquez sur **[!UICONTROL Terminer]** pour créer le flux de données. Il s’exécute automatiquement selon le planning défini.

1. Dans le menu **[!UICONTROL Connexions]**, sélectionnez **[!UICONTROL Sources]** et accédez à l’onglet **[!UICONTROL Flux de données]** pour suivre l’exécution du flux, vérifier les enregistrements ingérés et résoudre les erreurs.

   ![](assets/S3_config_5.png)

