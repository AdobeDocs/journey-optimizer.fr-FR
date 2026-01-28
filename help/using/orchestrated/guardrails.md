---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations des campagnes orchestrées
description: En savoir plus sur les mécanismes de sécurisation et les limitations des campagnes orchestrées
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: 266bf3afde663b17aedce5fb51e7c5f424fee9ad
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 97%

---


# Mécanismes de sécurisation et limitations {#guardrails}

Vous trouverez ci-dessous les mécanismes de sécurisation et les limitations lors de l’utilisation de campagnes orchestrées.

## Limitations des flux de données

### Conception et stockage des données

* Le magasin de données relationnelles prend en charge un **maximum de 200 tables** (schémas).

* Pour les campagnes orchestrées, la taille totale d’un schéma individuel **ne doit pas dépasser 100 Go**.

* Les mises à jour quotidiennes d’un schéma doivent être **limitées à moins de 20 %** du nombre total d’enregistrements afin de maintenir les performances et la stabilité.

* Les données relationnelles constituent le modèle principal pris en charge pour l’ingestion, la modélisation des données et les cas d’utilisation de segmentation.

* Les schémas utilisés pour le ciblage doivent contenir au moins **un champ d’identité de type`String`**, mappé à un espace de noms d’identité défini.

* Le nombre moyen d’attributs par schéma **ne doit pas dépasser 50 colonnes** afin de maintenir la facilité de gestion et les performances.

* Les schémas relationnels ne peuvent pas être activés pour les **profils** Adobe Experience Platform. Seuls les schémas XDM standard sont pris en charge pour les **profils** Adobe Experience Platform. Les schémas relationnels peuvent être activés pour les campagnes orchestrées ou les campagnes d’action. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Ingestion de données

* L’ingestion de données de profil et relationnelles est requise.

* Toute ingestion doit se faire via des sources **Capture des données modifiées** :

   * Pour **Basé sur des fichiers** : le champ `_change_request_type` est requis. Les valeurs prises en charge sont `U` (upsert) ou `D` (delete).

   * Pour **basé sur le cloud**, la journalisation des tables doit être activée.

* **Les mises à jour partielles des enregistrements ne sont pas autorisées**, chaque ligne doit être fournie en tant qu’enregistrement complet.

* L’ingestion par lots pour l’orchestration de campagne est limitée à **une fois toutes les 15 minutes**.

* La latence d’ingestion, dans le stockage relationnel, varie généralement **de 15 minutes à 2 heures**, selon :

   * Le volume des données

   * La concurrence du système

   * Le type d’opération, par ex. les insertions sont plus rapides que les mises à jour

* **La relation entre le flux de données et le jeu de données est 1-1**. Cela signifie qu’une seule source peut alimenter un jeu de données à un moment donné. Pour changer de source, il faut supprimer le flux de données existant et en créer un autre avec la nouvelle source.

### Modélisation des données

* Tous les schémas, y compris les tableaux de faits, doivent inclure **un descripteur de version** pour garantir un gestion et une traçabilité appropriés des versions.

* Chaque table doit comporter une **clé primaire** définie afin de garantir l’intégrité des données et les opérations en aval.

* Le `table_name` affecté lors de la création du jeu de données est permanent et est utilisé dans toutes les fonctionnalités de segmentation et de personnalisation.

* **Les groupes de champs ne sont pas pris en charge** dans le cadre actuel de modélisation des données.

* La prise en charge des clés primaires composites avec les flux de chargement de fichier n’est pas disponible pour le moment.

## Limitations des activités

* Seuls **les attributs scalaires sont pris en charge** dans les définitions d’audience ; **les mappages et les tableaux ne sont pas autorisés**.

* **Les activités de segmentation reposent principalement sur des données relationnelles**. Bien que les données de profil puissent être incluses, l’utilisation de jeux de données de profil volumineux peut avoir un impact sur les performances.

* **Des limites sont appliquées au nombre d’attributs de profil** pouvant être utilisés dans les audiences par lots et en streaming afin de maintenir l’efficacité du système.

* Les **énumérations** sont entièrement prises en charge.

* **Les audiences en lecture ne sont pas mises en cache** ; chaque exécution de campagne déclenche une évaluation complète de l’audience à partir des données sous-jacentes.

* **L’optimisation est fortement recommandée** lors de l’utilisation de définitions d’audience volumineuses ou complexes afin de garantir les performances.

* **Les activités d’audiences enregistrées sont statiques** ; elles reflètent les données disponibles au moment de l’exécution de la campagne.

* **L’ajout à une activité d’audience enregistrée n’est pas pris en charge**. Toute modification nécessite un remplacement complet de l’audience.

## Limitations des canaux

Seuls les canaux SMS, Push, E-mail et Courrier sont pris en charge dans les campagnes orchestrées.
