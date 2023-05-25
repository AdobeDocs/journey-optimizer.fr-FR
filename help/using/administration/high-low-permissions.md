---
solution: Journey Optimizer
product: journey optimizer
title: Niveaux d'autorisation
description: En savoir plus sur les autorisations de haut et de bas niveau permettant aux utilisateurs et utilisatrices d’accéder aux différentes fonctionnalités.
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: autorisation, haut niveau, bas niveau, profil, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 7ac2ae714f2d11d2559b6195af37e2dece35b17c
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 54%

---

# Niveaux d&#39;autorisation {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Chaque rôle se compose d’autorisations permettant aux utilisateurs d’accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau**: représente les différentes autorisations qui peuvent être affectées à **[!UICONTROL Rôle]** dans le [!DNL Admin console], par exemple **[!DNL Publish journeys]** et **[!DNL Manage subdomains delegation]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation de bas niveau** : représente les différentes autorisations qui proviennent de l&#39;autorisation de haut niveau.

Par exemple, la variable **[!DNL Journey administrator]** se voit attribuer le rôle **[!DNL Manage journeys]** autorisation. À partir de cette autorisation, les autorisations de bas niveau permettent à lʼadministrateur de parcours dʼécrire, de lire et de supprimer des parcours.

## Ressource de parcours {#journey-capability}

* **[!DNL Manage journeys]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des Parcours existants, ainsi que d’accéder aux objets utilisés dans la zone de travail du parcours pour créer le flux de parcours.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * journeys.read
      * journeys.write
      * journeys.delete
      * messages.read
   * Spécifiques à Adobe Experience Platform :

      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read

+++

* **[!DNL Publish journeys]** l’autorisation de haut niveau permet aux utilisateurs de publier des parcours.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** l’autorisation de haut niveau permet aux utilisateurs de parcourir et d’afficher des parcours.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * journeys.read
   * Spécifiques à Adobe Experience Platform :
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** l’autorisation de haut niveau permet aux utilisateurs de configurer des configurations d’événement et de données.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * journeys_events.read
      * journeys_events.write
      * journeys_events.delete
      * journeys_data_sources.read
      * journeys_data_sources.write
      * journeys_data_sources.delete
      * journeys_actions.read
      * journeys_actions.write
      * journeys_actions.delete
   * Spécifiques à Adobe Experience Platform :
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys events, data sources and actions]** l’autorisation de haut niveau permet aux utilisateurs d’utiliser l’événement et les données dans le flux de parcours.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * journeys_events.read
      * journeys_data_sources.read
      * journeys_actions.read
   * Spécifiques à Adobe Experience Platform :
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** l’autorisation de haut niveau permet aux utilisateurs de créer des rapports de parcours en lecture seule.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * journeys_report.read
      * messages_report.read
   * Spécifiques à Adobe Experience Platform :
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## Ressource de règles Journey Optimizer {#journey-rules-capability}

* **[!DNL Manage frequency rules]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier, supprimer et activer/désactiver les règles de fréquence.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les règles de fréquence.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * frequency_rules.read

+++

## Ressource de campagne {#campaign-capability}

* **[!DNL Manage campaigns]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des campagnes.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * campaign.read
      * campaign.write
      * campaign.delete

      <!--* experiments.read
      * experiments.write
      * experiments.delete-->
+++

* **[!DNL Publish campaigns]** l’autorisation de haut niveau permet aux utilisateurs de publier des campagnes.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * campaign-read
      * campaign-publish
         <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** l’autorisation de niveau supérieur permet aux utilisateurs de lire et de modifier le rapport des campagnes.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * campaign.read
      * campaign-report.read

      <!--* experiments.read
      * experiments_report.read-->
+++

## Ressource de gestion des décisions {#decisions-permissions}

* **[!DNL Manage decisions]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des **[!DNL Activity entities]**, ainsi que de gérer les objets utilisés dans ces activités pour prendre des décisions.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à la gestion des décisions :
      * activities.read
      * activities.write
      * activities.delete
      * offer.read
      * offer.write
      * offer.delete
      * placements.read
      * placements.write
      * placements.delete
      * ranking_strategy.read
   * Spécifiques à Adobe Experience Platform :
      * datasets.read
      * datasets.write
      * datasets.delete
      * schemas.read
      * profile.read
      * segments.read

+++

* **[!DNL View decisions]** l’autorisation de haut niveau permet aux utilisateurs d’utiliser une activité existante et les objets commerciaux associés pour prendre des décisions.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à la gestion des décisions :
      * activities.read
      * offer.read
      * placements.read
      * ranking_strategy.read
   * Spécifiques à Adobe Experience Platform :
      * schemas.read
      * segment.read
      * datasets.read
      * datasets.write
      * datasets.delete

+++

* **[!DNL Manage offers]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer toutes les offres, tous les composants, ainsi que de lire les décisions et les collections.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à la gestion des décisions :
      * offer_activity.read
      * offer.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read
   * Spécifiques à Adobe Experience Platform :
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier et supprimer des stratégies de classement.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à la gestion des décisions :
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offer.read
      * placements.read

+++

## Ressource de configuration de canal {#administration-permissions}

* **[!DNL Manage subdomains delegation]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des délégations de sous-domaines (y compris le pool d’adresses IP).

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage PTR records]** l’autorisation de haut niveau permet aux utilisateurs de lire et de modifier les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL View PTR records]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :

      * PTR_records.read
      * subdomains_delegation.read

+++

* **[!DNL Manage IP pools]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer la définition d’affinité.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage messages general settings]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des paramètres globaux au niveau de l’environnement de test.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete
   * Spécifiques à Adobe Experience Platform :
      * schemas.read

+++

* **[!DNL View messages general settings]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les paramètres généraux des messages, tels que l’adresse d’exécution.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_general_settings.read
   * Spécifiques à Adobe Experience Platform :
      * schemas.read

+++

* **[!DNL Manage channel surface]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des surfaces de canal sur les canaux au niveau de l’environnement de test.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
      * mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

+++

<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->

* **[!DNL Manage suppression]** l’autorisation de haut niveau permet aux utilisateurs de définir le nombre de rebonds avant l’ajout d’une adresse électronique à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans/depuis la liste de suppression.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View suppression list]** l’autorisation de haut niveau permet aux utilisateurs d’afficher le contenu et les paramètres de la liste de suppression.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * suppression_list.view
   * Spécifiques à Adobe Experience Platform :
      * profiles.read
      * datasets.read

+++

* **[!DNL Export suppression list]** l’autorisation de haut niveau permet aux utilisateurs de télécharger la liste de suppression sous la forme d’un fichier CSV.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * suppression_list.export
   * Spécifiques à Adobe Experience Platform :
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage landing page settings]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer et modifier des sous-domaines de landing page et des paramètres prédéfinis.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

* **[!DNL Manage messages presets]** l’autorisation de niveau supérieur permet aux utilisateurs de lire, créer, modifier et supprimer la marque de contenu.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
   * Collecte de données spécifique :
      * Mobile_setting.read

+++

* **[!DNL View messages presets]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les paramètres prédéfinis de message.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read
   * Collecte de données spécifique :
      * Mobile_setting.read

+++

* **[!DNL Manage SMS subdomains]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier et supprimer des sous-domaines SMS.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete
+++
