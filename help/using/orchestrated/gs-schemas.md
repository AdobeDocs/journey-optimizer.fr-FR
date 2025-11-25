---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment créer un schéma relationnel dans Adobe Experience Platform en chargeant un fichier DDL.
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 059670c143595b9cacdf7e82a8a5c3efda78f30b
workflow-type: ht
source-wordcount: '470'
ht-degree: 100%

---


# Commencer avec les schémas relationnels et les jeux de données{#gs-schemas}

Ce guide explique le processus de création d’un schéma relationnel, de configuration d’un jeu de données pour les campagnes orchestrées et d’ingestion de données.

![schéma](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## Principaux concepts

Dans le contexte des campagnes orchestrées, un **jeu de données** est une structure de stockage et de gestion pour une collection de données, généralement une table, contenant un schéma (des lignes) et des champs (des colonnes). Les données correctement ingérées dans Experience Platform sont conservées sous forme de jeux de données dans le lac de données.

Un **schéma** représente et valide la structure et le format des données. Il fournit une définition abstraite d’un objet du monde réel (comme une personne) et décrit les données à inclure dans chaque instance de cet objet (nom, anniversaire, etc.).

Un **modèle de données** est le plan conceptuel de la normalisation de vos données.

Il décrit :

* Les entités (par exemple, client, campagne, segment)
* Les attributs de ces entités (par exemple, Nom du client ou de la cliente, Date de début de la campagne)
* Les relations entre les entités (par exemple, les clients et clientes appartiennent à des segments, les campagnes ciblent des segments)

Un modèle de données est logique et conceptuel, et n’est pas lié à une mise en œuvre physique dans les campagnes orchestrées.

Dans un **modèle de données relationnel**, les données sont organisées en tables liées à d’autres tables.

* Chaque table comporte des lignes (enregistrements) et des colonnes (attributs).
* Chaque table possède une clé primaire pour identifier de manière unique les lignes.
* Les relations entre les tables sont exprimées à l’aide de clés étrangères.

Un **schéma relationnel** est la définition formelle du modèle de données relationnel.

Il précise :

* L’ensemble de tables
* Les colonnes de chaque table
* Les contraintes
* Les relations entre les tables

L’organisation des schémas ou des tables dans un modèle de données relationnel consiste à structurer vos données en plusieurs tables. Assurez-vous que chaque table stocke un type d’entité/des schémas.

➡️ [Pour en savoir plus sur les schémas, consultez la documentation d’Adobe Experience Platform.](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/ui/resources/schemas#create-model-based-schema)

## Étapes dʼimplémentation {#implementation}

Pour ingérer des données et créer un schéma relationnel, procédez comme suit :

1. Créer [un schéma relationnel manuellement](manual-schema.md) ou [à l’aide d’un fichier DDL](file-upload-schema.md)

   Définissez la structure de votre modèle de données, y compris les tables, les attributs et les relations. Choisissez de créer le schéma manuellement dans l’interface utilisateur ou de charger un fichier DDL pour une configuration plus rapide.

   Lors de la création manuelle du schéma, le jeu de données doit également être créé et activé manuellement. Lors de l’utilisation d’un fichier DDL, la création et l’activation d’un jeu de données sont automatiques.

1. [Lier des schémas](file-upload-schema.md)

   Établissez des relations entre vos schémas pour garantir la cohérence des données et activer les requêtes entre entités. Par exemple, liez les transactions de fidélité aux destinataires ou les récompenses aux marques.

1. [Créer un jeu de données](manual-schema.md#dataset)

   Après avoir défini votre schéma, vous devez créer un jeu de données basé sur celui-ci. Ce jeu de données sert de stockage des données ingérées.

1. [Activer des campagnes orchestrées](manual-schema.md#enable)

   Ce jeu de données stocke vos données ingérées et doit être activé pour les campagnes orchestrées afin de le rendre accessible dans Adobe Journey Optimizer.

1. [Ingérer des données](ingest-data.md)

   Insérez des données dans Adobe Experience Platform à partir de sources prises en charge telles que SFTP, l’espace de stockage dans le cloud ou des bases de données.

