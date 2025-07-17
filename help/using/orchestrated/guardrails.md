---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations des campagnes orchestrées
description: En savoir plus sur les mécanismes de sécurisation et les limitations des campagnes orchestrées
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 5%

---

# Mécanismes de sécurisation et limitations {#guardrails}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul><br/><br/>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limites d’un flux de données à un jeu de données

Chaque jeu de données dans Adobe Experience Platform ne peut être associé qu’à un seul flux de données actif à la fois. Cette cardinalité 1:1 est strictement appliquée par la plateforme.

Si vous devez changer de source de données (par exemple, d’Amazon S3 vers Salesforce) :

Vous devez supprimer le flux de données existant connecté au jeu de données.

Créez ensuite un flux de données avec la nouvelle source mappée au même jeu de données.

Cela garantit une ingestion de données fiable et est essentiel lors de l’utilisation de la capture de données modifiées (CDC), qui dépend d’une clé primaire et d’un attribut de version définis (par exemple, last modified) pour les mises à jour incrémentielles.


## Schémas relationnels/limites d’ingestion des données

* Nombre de schémas - Le nombre maximal de schémas relationnels (tables dans le magasin de données relationnelles) est de 200
* Taille du schéma relationnel : la taille maximale du schéma relationnel pour l’orchestration des campagnes est 100GB.
* Fréquence d’ingestion des données : la fréquence d’ingestion des données par lots pour l’orchestration des campagnes ne doit pas dépasser une toutes les quinze minutes.
* Modifications/Mises à jour : les mises à jour/modifications quotidiennes doivent représenter moins de 20 % du total des enregistrements pour un schéma relationnel donné
