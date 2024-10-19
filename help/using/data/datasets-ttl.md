---
solution: Journey Optimizer
product: journey optimizer
title: À propos des modifications de la segmentation par flux et de la durée de vie (TTL)
description: Modifications de la segmentation par flux et de la durée de vie dans Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: platform, lac de données, créer, lac, jeux de données, profil
source-git-commit: 1be920fb8b3ea825e38084f459523ccde0ad979b
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 7%

---


# Modifications de la segmentation par flux et du temps d’activation {#ttl-guardrail}

## Barrière de sécurité de la durée de vie (TTL) {#ttl}

À compter du 1er novembre 2024, un garde-fou de durée de vie (TTL) sera déployé dans les jeux de données générés par le système Journey Optimizer dans **de nouveaux environnements de test et de nouvelles organisations** comme suit :

* 90 jours pour les données dans la banque de profils
* 13 mois pour les données du lac de données

Cette modification sera déployée par la suite vers les **environnements de test client existants** dans une phase ultérieure.

**Questions fréquentes**

+++ Cette modification s’appliquera-t-elle uniquement aux environnements de test de production ou s’appliquera-t-elle également aux environnements de test de développement ?

Cette modification s’applique à tous les types d’environnements de test.

+++


+++ Pour la durée de vie de 90 jours dans la banque de profils, les profils eux-mêmes sont-ils affectés ?

Les données du jeu de données généré par le système dans le profil sont ignorées au bout de 90 jours, et non pas les profils eux-mêmes.

+++

+++ Si les données d’un jeu de données généré par le système sont transmises à Customer Journey Analytics (CJA), les données de CJA seront-elles également affectées par le TTL ?

Les données de CJA sont conservées synchronisées avec l’Experience Platform. Par conséquent, la suppression de données en raison d’un TTL sur les données de jeu de données générées par le système aura également un impact sur les données dans CJA.

+++

## Mises à jour de la segmentation par flux {#segmentation-update}

En outre, le 1er novembre, la segmentation par flux ne prendra plus en charge l’utilisation des événements d’envoi et de retour des jeux de données de suivi et de retour.  Vous trouverez des informations sur les raisons pour lesquelles cette pratique a été découragée par le passé [ici](../audience/about-audiences.md#streaming-segmentation-events-guardrails).


**Questions fréquentes**

+++ Ces modifications auront-elles une incidence sur l’utilisation des clics ou d’autres événements de suivi ?

Cette modification n’affecte que l’utilisation des événements d’envoi et d’ouverture ; les clics et autres événements de suivi peuvent toujours être utilisés dans un segment de diffusion en continu.

+++

+++ La segmentation par lots sera-t-elle affectée par cette modification ?

Cette modification n’affecte que la segmentation par flux. Les événements d’envoi et d’ouverture peuvent toujours être utilisés dans un segment par lot. S’ils sont utilisés dans un segment en continu, ils sont évalués par lots.

+++

+++ Cette modification aura-t-elle une incidence sur la collecte des données de suivi ?

Cette modification n’a aucune incidence sur la collecte des données de suivi. Les événements d’envoi et d’ouverture continueront à être collectés.

+++


+++ Les événements de réaction sont-ils affectés par ce changement ?

Les événements de réaction dans les Parcours ne sont pas affectés par cette modification.

+++


+++ Cette modification s’appliquera-t-elle uniquement aux environnements de test de production ou s’appliquera-t-elle également aux environnements de test de développement ?

Cette modification s’applique à tous les types d’environnements de test.

+++