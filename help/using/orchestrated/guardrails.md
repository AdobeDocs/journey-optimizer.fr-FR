---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations des campagnes orchestrées
description: En savoir plus sur les mécanismes de sécurisation et les limitations des campagnes orchestrées
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 10%

---

# Mécanismes de sécurisation et limitations {#guardrails}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancement de votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Commencer avec les activités](activities/about-activities.md)<br/><br/>Activités :<br/>[Rendez-vous](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Changement de dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combiner](activities/combine.md) - [Déduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Branchement](activities/fork.md) - [Réconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Partage](activities/split.md) - [Attente](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limites d’un flux de données à un jeu de données

Chaque jeu de données dans Adobe Experience Platform ne peut être associé qu’à un seul flux de données actif à la fois. Cette cardinalité 1:1 est strictement appliquée par la plateforme.

Si vous devez changer de source de données (par exemple, d’Amazon S3 vers Salesforce) :

Vous devez supprimer le flux de données existant connecté au jeu de données.

Créez ensuite un flux de données avec la nouvelle source mappée au même jeu de données.

Cela garantit une ingestion de données fiable et est essentiel lors de l’utilisation de la capture de données modifiées (CDC), qui dépend d’une clé primaire et d’un attribut de version définis (par exemple, last modified) pour les mises à jour incrémentielles.


## Schémas relationnels/limites d’ingestion des données

* Jusqu’à 200 schémas relationnels (tables) sont pris en charge dans le magasin de données relationnelles.

* La taille totale d’un schéma relationnel utilisé pour l’orchestration des campagnes ne doit pas dépasser 100 Go.

* L’ingestion par lots pour l’orchestration des campagnes ne doit pas avoir lieu plus d’une fois toutes les 15 minutes.

* Les modifications quotidiennes apportées à un schéma relationnel doivent rester inférieures à 20 % du nombre total d’enregistrements.

## Modélisation des données

* Le descripteur de version est obligatoire sur tous les schémas, y compris les tables de faits.

* Une clé primaire est requise pour chaque table.

* Le nom_table attribué lors de la création du jeu de données est utilisé dans l’interface utilisateur de segmentation et les fonctionnalités de personnalisation.

  Ce nom est permanent et ne peut pas être modifié après sa création.

* Les groupes de champs ne sont actuellement pas pris en charge.

## Ingestion des données

* Profil + ingestion de données relationnelles requise.

* Un champ de type de modification est requis pour l’ingestion basée sur des fichiers, tandis que la journalisation des tables doit être activée pour l’ingestion de la base de données Cloud. Cela est nécessaire pour la capture des données modifiées (CDC).

* La latence entre l’ingestion et la disponibilité des données dans Snowflake varie de 15 minutes à 2 heures, selon le volume de données, la simultanéité et le type d’opérations (les insertions sont plus rapides que les mises à jour).

* La surveillance des données dans Snowflake est en cours de développement. Il n’existe actuellement aucune confirmation native de réussite de l’ingestion.

* Les mises à jour directes de Snowflake ou du jeu de données ne sont pas prises en charge. Toutes les modifications doivent transiter par les sources CDC.

  Le service de requête est en lecture seule.

* ETL n’est pas pris en charge : les clients doivent fournir les données au format requis.

* Les mises à jour partielles ne sont pas autorisées. Chaque ligne doit être fournie en tant qu’enregistrement complet.

* L’ingestion repose sur Query Service et Data Distiller.

## Segmentation

* La liste de valeurs et les énumérations sont actuellement disponibles.

* Les audiences enregistrées sont des listes statiques dont le contenu reflète les données disponibles au moment de l’exécution de la campagne.

* L’ajout à une audience enregistrée n’est pas pris en charge. Les mises à jour nécessitent un remplacement complet.

* Les audiences doivent consister uniquement en attributs scalaires ; les mappages et les tableaux ne sont pas pris en charge.

* La segmentation prend principalement en charge les données relationnelles. Bien que le mélange avec des données de profil soit autorisé, l’ajout de jeux de données de profil volumineux peut affecter les performances. Pour éviter cela :

* Des mécanismes de sécurisation sont en place, comme la limitation du nombre d’attributs de profil sélectionnés dans les audiences par lots ou en flux continu.

* Les audiences de lecture ne sont pas mises en cache : chaque exécution de campagne déclenche une lecture complète.

  L’optimisation est nécessaire pour les audiences volumineuses ou complexes.