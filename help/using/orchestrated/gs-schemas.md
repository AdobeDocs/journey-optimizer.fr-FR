---
solution: Journey Optimizer
product: journey optimizer
title: Étapes de configuration
description: Découvrez comment créer un schéma relationnel dans Adobe Experience Platform en chargeant un fichier DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 7fc03d15c63789a2c35e3d517ca0c63f93545d4c
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# Prise en main des schémas relationnels et des jeux de données{#gs-schemas}

Ce guide vous guide tout au long du processus de création d’un schéma relationnel, de configuration d’un jeu de données pour les campagnes orchestrées et d’ingestion de données.

![](assets/do-not-localize/schema_admin.png)

1. Créez [un schéma relationnel manuellement](manual-schema.md) ou [à l’aide d’un fichier DDL](file-upload-schema.md)

   Définissez la structure de votre modèle de données, y compris les tables, les attributs et les relations. Choisissez de créer le schéma manuellement dans l’interface utilisateur ou de charger un fichier DDL pour une configuration plus rapide.

   Lors de la création manuelle du schéma, le jeu de données doit également être créé et activé manuellement. Lors de l’utilisation d’un fichier DDL, la création et l’activation du jeu de données sont automatiques.

1. [Lier le schéma](file-upload-schema.md)

   Établissez des relations entre vos schémas pour garantir la cohérence des données et activer les requêtes entre entités. Par exemple, liez les transactions de fidélité aux destinataires ou les récompenses aux marques.

1. [Ingérer des données](ingest-data.md)

   Insérez des données dans Adobe Experience Platform à partir de sources prises en charge telles que le SFTP, l’espace de stockage dans le cloud ou les bases de données.

