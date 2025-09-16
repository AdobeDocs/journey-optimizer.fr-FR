---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment créer un schéma relationnel dans Adobe Experience Platform en chargeant un fichier DDL.
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 69644e85d9c453f34fe8c5d40e0c1e8dce2891a5
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 95%

---


# Commencer avec les schémas et les jeux de données{#gs-schemas}

Ce guide explique le processus de création d’un schéma relationnel, de configuration d’un jeu de données pour les campagnes orchestrées et d’ingestion de données.

![](assets/do-not-localize/schema_admin.png)

Un jeu de données est une structure de stockage et de gestion pour une collection de données, généralement sous la forme d’une table, qui contient un schéma (des colonnes) et des champs (des lignes). Les données correctement ingérées par Experience Platform sont conservées sous forme de jeux de données dans le lac de données.

Un schéma représente et valide la structure et le format des données. Il fournit une définition abstraite d’un objet du monde réel (comme une personne) et décrit les données à inclure dans chaque instance de cet objet (nom, anniversaire, etc.).


1. Créer [un schéma relationnel manuellement](manual-schema.md) ou [à l’aide d’un fichier DDL](file-upload-schema.md)

   Définissez la structure de votre modèle de données, y compris les tables, les attributs et les relations. Choisissez de créer le schéma manuellement dans l’interface utilisateur ou de charger un fichier DDL pour une configuration plus rapide.

   Lors de la création manuelle du schéma, le jeu de données doit également être créé et activé manuellement. Lors de l’utilisation d’un fichier DDL, la création et l’activation du jeu de données sont automatiques.

1. [Lier le schéma](file-upload-schema.md)

   Établissez des relations entre vos schémas pour garantir la cohérence des données et activer les requêtes entre entités. Par exemple, liez les transactions de fidélité aux destinataires ou les récompenses aux marques.

1. [Ingérer des données](ingest-data.md)

   Insérez des données dans Adobe Experience Platform à partir de sources prises en charge telles que SFTP, l’espace de stockage dans le cloud ou des bases de données.

