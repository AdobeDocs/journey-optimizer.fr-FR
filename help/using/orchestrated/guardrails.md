---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations des campagnes orchestrées
description: En savoir plus sur les mécanismes de sécurisation et les limitations des campagnes orchestrées
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 4f262d4cbbe2241ec8356333d9a3191081f58a6a
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Mécanismes de sécurisation et limitations {#guardrails}

Vous trouverez ci-dessous des mécanismes de sécurisation et des limitations supplémentaires lors de l’utilisation de campagnes orchestrées.

## Limites des flux de données

### Conception et stockage des données

* Le magasin de données relationnel prend en charge **maximum 200 tables** (schémas).

* Pour les campagnes orchestrées, la taille totale d’un schéma individuel **ne doit pas dépasser 100 Go**.

* Les mises à jour quotidiennes d’un schéma doivent être **limitées à moins de 20 %** du nombre total d’enregistrements pour maintenir les performances et la stabilité.

* Les données relationnelles sont le modèle principal pris en charge pour l’ingestion, la modélisation des données et les cas d’utilisation de segmentation.

* Les schémas utilisés pour le ciblage doivent contenir au moins **un champ d’identité de type`String`**, mappé à un espace de noms d’identité défini.

### Ingestion de données

* Profil + ingestion de données relationnelles requise.

* Toute ingestion doit se faire via les sources **Modifier la capture de données** :

   * Pour **Basé sur des fichiers** : `_change_request_type` champ est obligatoire.

   * Pour **basé sur le cloud** : la journalisation des tables doit être activée.

* **Les mises à jour directes de Snowflake ou de jeux de données ne sont pas prises en charge**. Le système est en lecture seule, toutes les modifications doivent être appliquées via la capture de données de modification.

* **Les processus ETL ne sont pas pris en charge**. Les données doivent être entièrement transformées au format requis avant l’ingestion.

* **Les mises à jour partielles ne sont pas autorisées**, chaque ligne doit être fournie en tant qu’enregistrement complet.

* L’ingestion par lots pour l’orchestration des campagnes est limitée à **toutes les 15 minutes**.

* La latence d’ingestion, le temps écoulé entre l’ingestion et la disponibilité dans Snowflake, varie généralement **de 15 minutes à 2 heures**, selon :

   * Volume des données

   * Simultanéité du système

   * Type d’opération : les insertions sont plus rapides que les mises à jour, par exemple.

### Modélisation des données

* Tous les schémas, y compris les tableaux de faits, doivent inclure **un descripteur de version** pour garantir un contrôle et une traçabilité appropriés des versions.

* Chaque table doit disposer d&#39;une **clé primaire** définie pour prendre en charge l&#39;intégrité des données et les opérations en aval.

* Le `table_name` affecté lors de la création du jeu de données est permanent et est utilisé dans toutes les fonctionnalités de segmentation et de personnalisation.

* **Les groupes de champs ne sont pas pris en charge** dans le framework de modélisation des données actuel.

## Limites des activités

* Seuls les attributs **scalaires) sont pris en charge** dans les définitions d’audience. Les **mappages et tableaux ne sont pas autorisés**.

* **Les activités de segmentation reposent principalement sur des données relationnelles**. Bien que les données de profil puissent être incluses, l’utilisation de jeux de données de profil volumineux peut avoir un impact sur les performances.

* **Des limites sont appliquées au nombre d’attributs de profil** qui peuvent être utilisés dans les audiences par lots et en flux continu pour maintenir l’efficacité du système.

* Les **listes de valeurs (LOV)** et **énumérations** sont entièrement prises en charge.

* **Les audiences de lecture ne sont pas mises en cache**, chaque exécution de campagne déclenche une évaluation complète de l’audience à partir des données sous-jacentes.

* **L’optimisation est vivement recommandée** lorsque vous utilisez des définitions d’audience volumineuses ou complexes afin d’assurer les performances.

* **Les activités des audiences enregistrées sont statiques** elles reflètent les données disponibles au moment de l’exécution de la campagne.

* **L’ajout à une activité Audience enregistrée n’est pas pris en charge**. Toute modification nécessite un remplacement complet de l’audience.

## Limites de canal

Seuls les canaux SMS, Push et E-mail sont pris en charge dans les campagnes orchestrées.
