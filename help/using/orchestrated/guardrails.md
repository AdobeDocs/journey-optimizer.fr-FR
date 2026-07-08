---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations des campagnes orchestrées
description: En savoir plus sur les mécanismes de sécurisation et les limitations des campagnes orchestrées
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ViPJaOPo-AT-naQqq-PaPw-BI5YupYuYAEy56AUEp2A
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: b364e9038ac9dc2de884c32bc39d4cb20e8bd90a
workflow-type: tm+mt
source-wordcount: 763
ht-degree: 12%

---

# Mécanismes de sécurisation et limitations {#guardrails}

>[!BEGINSHADEBOX]

**Sur cette page :** passez en revue les mécanismes de sécurisation et les limitations qui s’appliquent au stockage des données, à l’ingestion, à la modélisation des données, aux activités et aux canaux dans les campagnes orchestrées.

>[!ENDSHADEBOX]

Vous trouverez ci-dessous les mécanismes de sécurisation et les limitations lors de l’utilisation de campagnes orchestrées.

## Limitations des flux de données

### Conception et stockage des données

* **Tables maximum** - Le magasin de données relationnel prend en charge un maximum de 200 tables (schémas).

* **Taille du schéma** - Pour les campagnes orchestrées, la taille totale d’un schéma individuel ne doit pas dépasser 100 Go.

* **Volume de mises à jour quotidiennes** - Les mises à jour quotidiennes d’un schéma doivent être limitées à moins de 20 % de son nombre total d’enregistrements pour maintenir les performances et la stabilité.

* **Modèle de données relationnel** - Les données relationnelles sont le modèle principal pris en charge pour les cas d’utilisation d’ingestion, de modélisation des données et de segmentation.

* **Champ d’identité** - Les schémas utilisés pour le ciblage doivent contenir au moins un champ d’identité de type `String`, mappé à un espace de noms d’identité défini.

* **Attributs par schéma** - Le nombre moyen d’attributs par schéma ne doit pas dépasser 50 colonnes pour garantir la facilité de gestion et les performances.

* **Activation des profils** - Les schémas relationnels ne peuvent pas être activés pour les profils Adobe Experience Platform. Seuls les schémas XDM standard sont pris en charge pour les profils Adobe Experience Platform. Les schémas relationnels peuvent être activés pour les campagnes orchestrées ou les campagnes d’action. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Ingestion des données {#data-ingestion}

* **Ingestion de profil et relationnelle** - L’ingestion de données de profil + relationnelle est requise.

* **Modifier les sources de capture de données** - Toute ingestion doit se produire via l’option Modifier les sources de capture de données :

   * **Sources basées sur des fichiers** - Le champ `_change_request_type` est obligatoire. Les valeurs prises en charge sont `u` (upsert) ou `d` (delete). Ces valeurs doivent être `u` et `d` en minuscules, et non `U` et `D` en majuscules.

   * **Sources basées sur le cloud** - La journalisation des tables doit être activée.

* **Enregistrements complets uniquement** - Les mises à jour partielles des enregistrements ne sont pas autorisées. Chaque ligne doit être fournie en tant qu’enregistrement complet.

* **Fréquence d’ingestion par lots** - L’ingestion par lots pour l’orchestration des campagnes est limitée à une fois toutes les 15 minutes.

* **Latence d’ingestion** - La latence d’ingestion dans la boutique relationnelle est généralement comprise entre 15 minutes et 2 heures, selon :

   * Le volume des données

   * La concurrence du système

   * Type d&#39;opération (par exemple, les insertions sont plus rapides que les mises à jour)

* **Relation entre le flux de données et le jeu de données** - La relation entre le flux de données et le jeu de données est 1-1. Une seule source peut alimenter un jeu de données à la fois. Pour changer de source, supprimez le flux de données existant, puis créez un flux de données avec la nouvelle source.

### Modélisation des données

* **Descripteur de version** - Tous les schémas, y compris les tables de faits, doivent inclure un descripteur de version pour garantir un contrôle et une traçabilité appropriés des versions.

* **Clé de Principal** - Chaque table doit avoir une clé primaire définie pour prendre en charge l&#39;intégrité des données et les opérations en aval.

* **Nom de table permanent** - Le `table_name` attribué lors de la création du jeu de données est permanent et est utilisé dans toutes les fonctionnalités de segmentation et de personnalisation.

* **Groupes de champs** - Les groupes de champs ne sont pas pris en charge dans le cadre de modélisation des données actuel.

* **Clés primaires composites** - La prise en charge des clés primaires composites avec les flux de chargement de fichiers n’est pas disponible pour le moment.

## Audiences

* **Attributs scalaires uniquement** - Seuls les attributs scalaires sont pris en charge dans les définitions d’audience. Les mappages et les tableaux ne sont pas autorisés.

* **Données relationnelles pour la segmentation** - Les activités de segmentation reposent principalement sur des données relationnelles. Bien que les données de profil puissent être incluses, l’utilisation de jeux de données de profil volumineux peut avoir un impact sur les performances.

* **Limites d’attributs de profil** - Des limites sont appliquées au nombre d’attributs de profil qui peuvent être utilisés dans les audiences par lots et en flux continu pour maintenir l’efficacité du système.

* **Enumérations** - Les énumérations sont entièrement prises en charge.

* **Lecture d’audiences non mises en cache** - Les audiences lues ne sont pas mises en cache ; chaque exécution de campagne déclenche une évaluation complète de l’audience à partir des données sous-jacentes.

* **Optimisation de l’audience** - L’optimisation est vivement recommandée lorsque vous travaillez avec des définitions d’audience volumineuses ou complexes afin d’assurer les performances.

* **Audiences enregistrées**

   * **Les audiences enregistrées sont statiques** - Les activités d’audience enregistrées sont statiques ; elles reflètent les données disponibles au moment de l’exécution de la campagne.

* **Aucun ajout à une audience enregistrée** - L’ajout à une activité Audience enregistrée n’est pas pris en charge. Toute modification nécessite un remplacement complet de l’audience.

## Limitations des activités {#activities-limitations}

* **Limite des activités de canal** - Une campagne orchestrée prend en charge un maximum de 10 activités de canal (e-mail, SMS, notification push ou courrier). Seules les activités de canal sont prises en compte dans cette limite. Les activités de ciblage, de gestion des données et de contrôle de flux ne sont pas comptabilisées (par exemple, création d’audience, chargement de fichier, attente, partage, enrichissement, réconciliation, branchement, fin ou test).

  Si vous dépassez la limite lors de l’enregistrement ou de la publication, l’opération échoue. Pour respecter la limite, réduisez le nombre d’activités de canal ou répartissez la diffusion des messages sur plusieurs campagnes orchestrées.

* **Limite des activités du canevas** - Le nombre d’activités sur un canevas de campagne orchestré est limité à 500. Cette limite s’applique à tous les types d’activité sur la zone de travail. Il est distinct de la limite des activités de canal appliquée lors de la publication. Pour des raisons de maintenabilité et de performances, maintenez les workflows de moins de 100 activités en pratique.

## Limitations des canaux

Seuls les canaux SMS, Push, E-mail et Courrier sont pris en charge dans les campagnes orchestrées.
