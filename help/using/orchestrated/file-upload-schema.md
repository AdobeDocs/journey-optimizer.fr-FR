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
source-wordcount: '804'
ht-degree: 27%

---

# Chargement des fichiers {#file-upload-schema}

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

Définissez le modèle de données relationnelles requis pour les campagnes orchestrées en créant des schémas tels que **Loyalty Memberships**, **Loyalty Transactions** et **Loyalty Rewards**. Chaque schéma doit inclure une clé primaire, un attribut de contrôle de version et des relations appropriées pour référencer des entités telles que **Destinataires** ou **Marques**.

Les schémas peuvent être créés manuellement par le biais de l’interface ou importés en bloc à l’aide d’un fichier DDL.

Cette section fournit des instructions détaillées sur la création d’un schéma relationnel dans Adobe Experience Platform en chargeant un fichier DDL (Data Definition Language). L’utilisation d’un fichier DDL vous permet de définir à l’avance la structure de votre modèle de données, y compris les tables, les attributs, les clés et les relations.

## Chargement du fichier DDL {#ddl-upload}

1. Connectez-vous à Adobe Experience Platform.

1. Accédez à **Gestion des données** > **Schéma**.

1. Cliquez sur **Créer un schéma**.

1. Vous êtes invité à choisir entre deux types de schéma :

   * **Standard**
   * **Relationnel**, utilisé spécifiquement pour les campagnes orchestrées

   ![](assets/admin_schema_1.png)

1. Sélectionnez **Télécharger le fichier DDL** pour définir un diagramme de relation d’entité et créer des schémas.

   La structure du tableau doit contenir :
   * Au moins une clé primaire
   * Identifiant de version, tel qu’un champ de `lastmodified` de type `datetime` ou `number`.

1. Faites glisser et déposez votre fichier DDL, puis cliquez sur **[!UICONTROL Suivant]**.

1. Saisissez votre **[!UICONTROL nom du schéma]**.

1. Configurez chaque schéma et ses colonnes en veillant à ce qu’une clé primaire soit spécifiée.

   Un attribut, tel que `lastmodified`, doit être désigné comme descripteur de version. Cet attribut, généralement de type `datetime`, `long` ou `int`, est essentiel pour que les processus d’ingestion garantissent que le jeu de données est mis à jour avec la dernière version des données.

   ![](assets/admin_schema_2.png)

1. Cliquez sur **[!UICONTROL Terminé]** une fois l’opération terminée.

Vous pouvez maintenant vérifier les définitions de table et de champ dans la zone de travail. [En savoir plus dans la section ci-dessous](#entities)

## Définition des relations {#relationships}

Pour définir des connexions logiques entre les tables de votre schéma, procédez comme suit.

1. Accédez à la vue Zone de travail de votre modèle de données et sélectionnez les deux tables à lier

1. Cliquez sur le bouton ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) en regard de la jointure Source, puis faites glisser la flèche vers la jointure cible pour établir la connexion.

   ![](assets/admin_schema_5.png)

1. Remplissez le formulaire donné pour définir le lien et cliquez sur **Appliquer** une fois configuré.

   ![](assets/admin_schema_3.png)

   **Cardinalité** :

   * **1-N** : à une occurrence du tableau source peuvent correspondre plusieurs occurrences du tableau cible, mais à une occurrence du tableau cible peut correspondre au plus une occurrence du tableau source.

   * **N-1** : à une occurrence du tableau cible peuvent correspondre plusieurs occurrences du tableau source, mais à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

   * **1-1** : à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

1. Tous les liens définis dans votre modèle de données sont représentés par des flèches dans la vue Zone de travail. Cliquez sur une flèche entre deux tableaux pour afficher les détails, apporter des modifications ou supprimer le lien selon les besoins.

   ![](assets/admin_schema_6.png)

1. Utilisez la barre d’outils pour personnaliser et ajuster la zone de travail.

   ![](assets/toolbar.png)

   * **Zoom avant** : agrandissez la zone de travail pour afficher plus clairement les détails de votre modèle de données.

   * **Zoom arrière** : réduisez la taille de la zone de travail pour obtenir une vue plus large de votre modèle de données.

   * **Ajuster la vue** : ajustez le zoom pour qu’il s’adapte à tous les schémas dans la zone visible.

   * **Filtre** : choisissez le schéma à afficher dans la zone de travail.

   * **Forcer la disposition automatique** : organiser automatiquement les schémas pour une meilleure organisation.

   * **Afficher la carte** : basculez sur une superposition minimale pour parcourir plus facilement les dispositions de schémas volumineuses ou complexes.

1. Cliquez sur **Enregistrer** une fois l’opération terminée. Cette action crée les schémas et les jeux de données associés et permet au jeu de données d’être utilisé dans des campagnes orchestrées.

1. Cliquez sur **[!UICONTROL Ouvrir les tâches]** pour surveiller la progression de la tâche de création. Ce processus peut prendre quelques minutes, selon le nombre de tables définies dans le fichier DDL.

   ![](assets/admin_schema_4.png)

## Schéma du lien {#link-schema}

Établissez une relation entre le schéma **transactions de fidélité** et le schéma **Destinataires** pour associer chaque transaction à l’enregistrement client correct.

1. Accédez à **[!UICONTROL Schémas]** et ouvrez vos **transactions de fidélité** créées précédemment.

1. Cliquez sur **[!UICONTROL Ajouter une relation]** dans le champ Client **[!UICONTROL Propriétés du champ]**.

   ![](assets/schema_1.png)

1. Sélectionnez **[!UICONTROL Plusieurs-à-un]** comme relation **[!UICONTROL Type]**.

1. Lien vers le schéma **Destinataires** existant.

   ![](assets/schema_2.png)

1. Saisissez un **[!UICONTROL Nom de la relation à partir du schéma actuel]** et un **[!UICONTROL Nom de la relation à partir du schéma de référence]**.

1. Cliquez sur **[!UICONTROL Appliquer]** pour enregistrer vos modifications.

Continuez en créant une relation entre le schéma **récompenses de fidélité** et le schéma **Marques** pour associer chaque entrée de récompense à la marque appropriée.

![](assets/schema_3.png)

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