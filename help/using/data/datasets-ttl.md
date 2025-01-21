---
solution: Journey Optimizer
product: journey optimizer
title: À propos des modifications de la segmentation du streaming et de la durée de vie (TTL)
description: Modifications de la segmentation du streaming et de la durée de vie dans Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: platform, lac de données, créer, lac, jeux de données, profil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: f5df65a0225754ab66fb2ffa33c5130f7137b644
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 100%

---

# Modifications de la segmentation du streaming et de la durée de vie {#ttl-guardrail}

## Mises à jour de la segmentation du streaming {#segmentation-update}

Dès le 1er novembre 2024, la segmentation du streaming ne prendra plus en charge l’utilisation des événements d’envoi et d’ouverture provenant des jeux de données de tracking et de commentaires dans Journey Optimizer. Cette modification s’applique à tous les sandbox et toutes les organisations des clientes et des clients. Vous trouverez des informations sur les raisons pour lesquelles cette pratique a été découragée par le passé [ici](../audience/about-audiences.md#streaming-segmentation-events-guardrails).

**Questions fréquentes**

+++ Ces modifications auront-elles une incidence sur l’utilisation des clics ou d’autres événements de tracking ?

Cette modification n’affecte que l’utilisation des événements d’envoi et d’ouverture ; les clics et autres événements de tracking peuvent toujours être utilisés dans un segment de streaming.

+++

+++ La segmentation par lots sera-t-elle affectée par cette modification ?

Cette modification n’affecte que la segmentation du streaming. Les événements d’envoi et d’ouverture peuvent toujours être utilisés dans un segment par lots. S’ils sont utilisés dans un segment de streaming, ils sont évalués par lots.

+++

+++ Cette modification aura-t-elle une incidence sur la collecte des données de tracking ?

Cette modification n’a aucune incidence sur la collecte des données de tracking. Les événements d’envoi et d’ouverture continueront à être collectés.

+++


+++ Les événements de réaction sont-ils affectés par ce changement ?

Les événements de réaction dans les parcours ne sont pas affectés par cette modification.

+++


+++ Cette modification s’appliquera-t-elle uniquement aux sandbox de production ou s’appliquera-t-elle également aux sandbox de développement ?

Cette modification s’applique à tous les types de sandbox.

+++

+++ Les événements de retour résultant de l’événement d’envoi sont-ils également affectés par la modification ?

Cette modification s’applique également aux événements d’exclusion et aux événements de rebond/retard résultant de l’envoi.

+++

## Mise à jour de la durée de vie (TTL) par phases {#ttl}

Dès février 2025, un mécanisme de sécurisation de la durée de vie (TTL) sera déployé dans les jeux de données générés par le système Journey Optimizer dans **les nouveaux sandbox et les nouvelles organisations** comme suit :

* 90 jours pour les données dans la banque de profils
* 13 mois pour les données du lac de données

Cette modification sera déployée sur les **sandbox client existants** dans une phase ultérieure.

**Questions fréquentes**

+++ Cette modification s’appliquera-t-elle uniquement aux sandbox de production ou s’appliquera-t-elle également aux sandbox de développement ?

Cette modification s’applique à tous les types de sandbox.

+++

+++ Pour la durée de vie de 90 jours dans la banque de profils, les profils eux-mêmes sont-ils affectés ?

Les données du jeu de données généré par le système dans le profil sont ignorées au bout de 90 jours, et non pas les profils eux-mêmes.

+++

+++ Si les données d’un jeu de données généré par le système sont transmises à Customer Journey Analytics (CJA), les données de CJA seront-elles également affectées par la durée de vie ?

Les données de CJA restent synchronisées avec Experience Platform. Par conséquent, la suppression de données en raison d’une durée de vie sur les données de jeu de données générées par le système aura également un impact sur les données dans CJA.

+++
