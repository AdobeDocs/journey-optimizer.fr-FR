---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment insérer des données dans Adobe Experience Platform à partir de sources prises en charge telles que SFTP, l’espace de stockage dans le cloud ou des bases de données.
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
version: Campaign Orchestration
source-git-commit: 059670c143595b9cacdf7e82a8a5c3efda78f30b
workflow-type: ht
source-wordcount: '699'
ht-degree: 100%

---


# Ingérer des données {#ingest-data}

>[!IMPORTANT]
>
>Pour modifier la source de données d’un jeu de données, vous devez d’abord supprimer le flux de données existant avant d’en créer un nouveau qui référence le même jeu de données et la nouvelle source.
>
>Adobe Experience Platform applique une relation stricte de un-à-un entre les flux de données et les jeux de données. Cela vous permet de maintenir la synchronisation entre la source et le jeu de données pour une ingestion incrémentielle précise.

Adobe Experience Platform permet d’ingérer des données à partir de sources externes tout en vous offrant la possibilité de structurer, d’étiqueter et d’améliorer les données entrantes à l’aide des services d’Experience Platform. Vous pouvez ingérer des données provenant de diverses sources telles que les applications Adobe, les stockages dans le cloud, les bases de données, etc.

Un jeu de données est une structure de stockage et de gestion pour une collection de données, généralement sous la forme d’une table, qui contient un schéma (des colonnes) et des champs (des lignes). Les données correctement ingérées par Experience Platform sont conservées sous forme de jeux de données dans le lac de données.

## Sources prises en charge pour les campagnes orchestrées {#supported}

Les sources suivantes sont prises en charge pour une utilisation dans des campagnes orchestrées :

<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Espace de stockage dans le cloud</td>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Entrepôts de données cloud</td>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Zone d’atterrissage des données<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Chargements basés sur des fichiers</td>
      <td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Chargement de fichiers locaux<a></td>
    </tr>

</tbody>
</table>

## Instructions relatives à l’hygiène des données des schémas relationnels {#cdc}

Pour les jeux de données avec l’option **[!UICONTROL Capture des données modifiées]** activée, toutes les modifications de données, y compris les suppressions, sont automatiquement répliquées dans Adobe Experience Platform à partir du système source.

Étant donné que les campagnes Adobe Journey Optimizer nécessitent que tous les jeux de données intégrés aient l’option **[!UICONTROL Capture des données modifiées]** activée, il est de la responsabilité du client ou de la cliente de gérer les suppressions à la source. Tout enregistrement supprimé dans le système source est automatiquement supprimé du jeu de données correspondant dans Adobe Experience Platform.

Pour supprimer des enregistrements par ingestion basée sur des fichiers, le fichier de données du client ou de la cliente doit marquer l’enregistrement à l’aide d’une valeur `D` dans le champ `Change Request Type`. Celle-ci indique que l’enregistrement doit être supprimé dans Adobe Experience Platform, reflétant ainsi le système source.

Si le client ou la cliente souhaite supprimer uniquement des enregistrements dans Adobe Experience Platform sans affecter les données source d’origine, les options suivantes peuvent être utilisées :

* **Table proxy ou table assainie pour la réplication de la capture des données modifiées**

  Le client ou la cliente peut créer une table source proxy ou assainie pour contrôler quels enregistrements seront répliqués dans Adobe Experience Platform. Les suppressions peuvent ensuite être gérées de manière sélective à partir de cette table intermédiaire.

* **Suppression via Data Distiller**

  Si une licence est disponible, **Data Distiller** peut être utilisé pour prendre en charge les opérations de suppression directement dans Adobe Experience Platform, indépendamment du système source.

  [En savoir plus sur Data Distiller](https://experienceleague.adobe.com/fr/docs/experience-platform/query/data-distiller/overview)

## Configurer un flux de données

Cet exemple montre comment configurer un flux de données qui ingère des données structurées dans Adobe Experience Platform. Le flux de données configuré prend en charge l’ingestion automatisée et planifiée et permet des mises à jour en temps réel.

1. Dans le menu **[!UICONTROL Connexions]**, accédez au menu **[!UICONTROL Sources]**.

1. Choisissez votre source en fonction des [Sources prises en charge pour les campagnes orchestrées](#supported).

   ![](assets/admin_sources_1.png)

1. Connectez votre compte d’espace de stockage dans le cloud ou d’espace de stockage dans le cloud Google si vous avez choisi des sources basées sur le cloud.

   ![](assets/admin_sources_2.png)

1. Sélectionnez les données à ingérer dans Adobe Experience Platform.

   ![](assets/S3_config_1.png)

1. Depuis la page **[!UICONTROL Détails du jeu de données]**, cochez **[!UICONTROL Activer la capture des données modifiées]** pour afficher uniquement les jeux de données mappés à des schémas relationnels et contenant à la fois une clé primaire et un descripteur de version.

[En savoir plus sur les directives relatives à l’hygiène des données des schémas relationnels](#cdc)

   >[!IMPORTANT]
   >
   > Pour les **sources basées sur des fichiers uniquement**, chaque ligne du fichier de données doit inclure une colonne `_change_request_type` avec des valeurs `U` (upsert) ou `D` (delete). Sans cette colonne, le système ne reconnaît pas les données comme prenant en charge le suivi des modifications et le bouton Campagne orchestrée n’apparaît pas, empêchant le jeu de données d’être sélectionné pour le ciblage.

   ![](assets/S3_config_6.png)

1. Sélectionnez le jeu de données créé précédemment et cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/S3_config_3.png)

1. Si vous utilisez uniquement des sources basées sur des fichiers, dans la fenêtre **[!UICONTROL Sélectionner les données]**, chargez vos fichiers locaux et prévisualisez leur structure et leur contenu.

   Notez que la taille maximale prise en charge est de 100 Mo.

1. Dans la fenêtre **[!UICONTROL Mappage]**, vérifiez que chaque attribut de fichier source est correctement mappé avec les champs correspondants dans le schéma cible. [Découvrez les dimensions de ciblage](target-dimension.md).

   Cliquez sur **[!UICONTROL Suivant]** une fois l’opération terminée.

   ![](assets/S3_config_4.png)

1. Configurez le **[!UICONTROL Planning]** du flux de données en fonction de la fréquence souhaitée.

1. Cliquez sur **[!UICONTROL Terminer]** pour créer le flux de données. Il s’exécute automatiquement selon le planning défini.

1. Dans le menu **[!UICONTROL Connexions]**, sélectionnez **[!UICONTROL Sources]** et accédez à l’onglet **[!UICONTROL Flux de données]** pour suivre l’exécution du flux, vérifier les enregistrements ingérés et résoudre les erreurs.

   ![](assets/S3_config_5.png)


