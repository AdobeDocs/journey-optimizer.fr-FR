---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment créer des schémas relationnels directement via l’interface utilisateur.
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 4f262d4cbbe2241ec8356333d9a3191081f58a6a
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 5%

---


# Configurer un schéma relationnel manuel {#manual-schema}

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

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Cliquez sur **Terminer** pour procéder à la création de votre schéma.

Vous pouvez maintenant commencer à ajouter des attributs à votre schéma pour définir sa structure.

## Ajouter des attributs à votre schéma {#schema-attributes}

Ajoutez ensuite des attributs pour définir la structure de votre schéma. Ces champs représentent les points de données clés utilisés dans les campagnes orchestrées, tels que les identifiants des clients, les détails d’abonnement et les dates d’activité. Leur définition précise garantit une personnalisation, une segmentation et un suivi fiables.

Tout schéma utilisé pour le ciblage doit inclure au moins un champ d’identité de type `String` avec un espace de noms d’identité associé. Cela garantit la compatibilité avec les fonctionnalités de ciblage et de résolution d’identité de Adobe Journey Optimizer.

+++Les fonctions suivantes sont prises en charge lors de la création de schémas relationnels dans Adobe Experience Platform

* **ENUM**\
  Les champs ENUM sont pris en charge lors de la création de schémas manuelle et basée sur DDL, ce qui vous permet de définir des attributs avec un ensemble fixe de valeurs autorisées.

* **libellé de schéma pour la gouvernance des données**\
  L’étiquetage est pris en charge au niveau du champ de schéma pour appliquer des politiques de gouvernance des données telles que le contrôle d’accès et les restrictions d’utilisation. Pour plus d’informations, consultez la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr).

* **Clé composite**\
  Les clés primaires composites sont prises en charge dans les définitions de schéma relationnel, ce qui permet d’utiliser plusieurs champs ensemble pour identifier les enregistrements de manière unique.

+++

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

1. Attribuez les champs appropriés comme clé de Principal **&#x200B;**&#x200B;et **[!UICONTROL descripteur de version]**.

   Lors de la création d’un schéma manuel, assurez-vous que les champs essentiels suivants sont inclus :

   * Au moins une clé primaire
   * Un identifiant de version, tel qu’un champ `lastmodified` de type `datetime` ou `number`.
   * Pour l’ingestion Change Data Capture (CDC), une colonne spéciale nommée `_change_request_type` de type `String`, qui indique le type de modification des données (par exemple, insertion, mise à jour, suppression) et permet un traitement incrémentiel. Notez que le `_change_request_type` ne doit pas faire partie du schéma de la table, il doit uniquement être ajouté au fichier de données lors de l’ingestion.

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

Vous devez maintenant activer votre jeu de données pour orchestrer des campagnes.

## Activer le jeu de données pour les campagnes orchestrées {#enable}

Après avoir créé votre jeu de données, vous devez l’activer explicitement pour les campagnes orchestrées. Cette étape permet de s’assurer que votre jeu de données est disponible pour l’orchestration et la personnalisation en temps réel dans Adobe Journey Optimizer.

1. Recherchez votre jeu de données dans la liste **[!UICONTROL Jeux de données]**.

1. Dans les paramètres **[!UICONTROL Jeux de données]**, activez l’option **Campagnes orchestrées** pour rendre le jeu de données disponible pour une utilisation dans vos campagnes orchestrées.

   ![](assets/schema_manual_7.png){zoomable="yes"}

1. Patientez quelques minutes pour que le processus d’activation se termine. Notez que l’ingestion de données et l’utilisation de campagnes ne seront possibles qu’une fois ce paramètre entièrement activé.

Vous pouvez maintenant commencer à ingérer des données dans votre schéma à l’aide de la source de votre choix.

➡️ [Découvrez comment ingérer des données](ingest-data.md)
