---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment créer des schémas relationnels directement via l’interface utilisateur.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 4%

---

# Configurer un schéma relationnel manuel {#manual-schema}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br><ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

Les schémas relationnels peuvent être créés directement via l’interface utilisateur, ce qui permet une configuration détaillée des attributs, des clés primaires, des champs de contrôle de version et des relations.

L’exemple suivant définit manuellement le schéma **Loyalty Memberships** pour illustrer la structure requise pour les campagnes orchestrées.

1. [Création manuelle d’un schéma relationnel](#schema) à l’aide de l’interface Adobe Experience Platform.

1. [Ajoutez des attributs](#schema-attributes) tels que l’ID de client, le niveau d’abonnement et les champs de statut.

1. [Liez votre schéma](#link-schema) à des schémas intégrés tels que les destinataires pour le ciblage de la campagne.

1. [Créez un jeu de données](#dataset) basé sur votre schéma et activez-le pour l’utiliser dans des campagnes orchestrées.

1. [Ingérez des données](ingest-data.md) dans votre jeu de données à partir de sources prises en charge.

## Création de votre schéma {#schema}

Commencez par créer manuellement un nouveau schéma relationnel dans Adobe Experience Platform. Ce processus vous permet de définir la structure du schéma à partir de zéro, y compris son nom et son comportement.

1. Connectez-vous à Adobe Experience Platform.

1. Accédez au menu **[!UICONTROL Gestion des données]** > **[!UICONTROL Schéma]**.

1. Cliquez sur **[!UICONTROL Créer un schéma]**.

1. Sélectionnez **[!UICONTROL Relationnel]** comme **Type de schéma**.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Choisissez **[!UICONTROL Créer manuellement]** pour créer un schéma en ajoutant manuellement des champs.

1. Saisissez votre **[!UICONTROL nom d’affichage du schéma]**.

1. Choisissez **[!UICONTROL Enregistrement]** comme **[!UICONTROL comportement du schéma]**.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Cliquez sur **Terminer** pour procéder à la création de votre schéma.

Vous pouvez maintenant commencer à ajouter des attributs à votre schéma pour définir sa structure.

## Ajouter des attributs à votre schéma {#schema-attributes}

Ajoutez ensuite des attributs pour définir la structure de votre schéma. Ces champs représentent les points de données clés utilisés dans les campagnes orchestrées, tels que les identifiants des clients, les détails d’abonnement et les dates d’activité. Leur définition précise garantit une personnalisation, une segmentation et un suivi fiables.

1. Dans la zone de travail, cliquez sur ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) en regard de votre **nom du schéma** pour commencer à ajouter des attributs.

   ![](assets/schema_manual_1.png){zoomable="yes"}

1. Saisissez votre attribut **[!UICONTROL Nom du champ]**, **[!UICONTROL Nom d’affichage]** et **[!UICONTROL Type]**.

   Dans cet exemple, nous avons ajouté les attributs présentés dans le tableau ci-dessous au schéma **Abonnements aux programmes de fidélité**.

+++ Exemples d’attributs

   | Nom de l’attribut | Type de données | Attributs supplémentaires |
   |-|-|-|
   | client ou cliente | CHAÎNE | Clé primaire |
   | membership_level | CHAÎNE | Obligatoire |
   | points_balance | NOMBRE ENTIER | Obligatoire |
   | enrollment_date | DATE | Obligatoire |
   | last_status_change | DATE | Obligatoire |
   | expiration_date | DATE | - |
   | is_active | BOOLEAN | Obligatoire |
   | lastmodified | DATETIME | Obligatoire |

+++

1. Attribuez les champs appropriés comme clé de Principal **** et **[!UICONTROL descripteur de version]**.

   La clé de Principal **** garantit que chaque enregistrement est identifié de manière unique, tandis que le descripteur de version **[!UICONTROL Version]** capture les mises à jour au fil du temps, permettant la capture des données modifiées et la mise en miroir des données.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Une fois les attributs créés, vous devez lier le schéma que vous venez de créer à un schéma intégré.

## Lier les schémas {#link-schema}

La création d’une relation entre deux schémas permet d’enrichir vos campagnes orchestrées avec des données stockées en dehors du schéma de profil principal.

1. Dans le schéma que vous venez de créer, sélectionnez l’attribut à utiliser comme lien et cliquez sur **[!UICONTROL Ajouter une relation]**.

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Choisissez les champs **[!UICONTROL Schéma de référence]** et **[!UICONTROL Champ de référence]** avec lesquels établir la relation.

   Dans cet exemple, l’attribut `customer` est lié au schéma `recipients`.

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Saisissez un Nom de la relation à partir du schéma actuel et du schéma de référence.

1. Cliquez sur **[!UICONTROL Appliquer]** une fois la configuration terminée.

Une fois la relation établie, vous devez créer un jeu de données basé sur votre schéma.

## Création d’un jeu de données pour le schéma {#dataset}

Après avoir défini votre schéma, l’étape suivante consiste à créer un jeu de données basé sur celui-ci. Ce jeu de données stocke vos données ingérées et doit être activé pour les campagnes orchestrées afin de le rendre accessible dans Adobe Journey Optimizer. L’activation de cette option garantit que le jeu de données est reconnu pour une utilisation dans les workflows d’orchestration et de personnalisation en temps réel.

1. Accédez au menu **[!UICONTROL Data Management]** > **[!UICONTROL Datasets]** et cliquez sur **[!UICONTROL Créer un jeu de données]**.

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Sélectionnez **[!UICONTROL Créer un jeu de données à partir d&#39;un schéma]**.

1. Sélectionnez le schéma créé précédemment, ici **Abonnements de fidélité**, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Saisissez un **[!UICONTROL Nom]** pour votre **[!UICONTROL Jeu de données]** puis cliquez sur **[!UICONTROL Terminer]**.

1. Activez l’option **Campagnes orchestrées** pour rendre le jeu de données disponible pour une utilisation dans vos campagnes AJO.

   L’activation peut prendre quelques minutes. L’ingestion de données n’est possible qu’une fois l’option entièrement activée.

   ![](assets/schema_manual_7.png){zoomable="yes"}

Vous pouvez maintenant commencer à ingérer des données dans votre schéma à l’aide de la source de votre choix.

➡️ [Découvrez comment ingérer des données](ingest-data.md)
