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
source-git-commit: bb988dbc3aa8b70081c9f3de595d49904cc699b4
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 100%

---

# Niveaux d’autorisation {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Chaque rôle est constitué d’autorisations permettant aux utilisateurs et utilisatrices d’accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau** : représente les différentes autorisations qui peuvent être attribuées au **[!UICONTROL rôle]** dans [!DNL Admin console], tels que **[!DNL Publish journeys]** et **[!DNL Manage subdomains delegation]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation de bas niveau** : représente les différentes autorisations qui proviennent de l&#39;autorisation de haut niveau.

Par exemple, le rôle **[!DNL Journey administrator]** se voit attribuer lʼautorisation **[!DNL Manage journeys]**. À partir de cette autorisation, les autorisations de bas niveau permettent à lʼadministrateur ou l’adminnistratrice de parcours dʼécrire, de lire et de supprimer des parcours.

## Ressource de parcours {#journey-capability}

* Lʼautorisation de haut niveau **[!DNL Manage journeys]** permet aux utilisateurs et utilisatrices de créer des parcours et de modifier/supprimer des parcours existants, ainsi que dʼaccéder aux objets utilisés dans la zone de travail de parcours pour concevoir le flux du parcours.

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

* Lʼautorisation de haut niveau **[!DNL Publish journeys]** permet aux utilisateurs et utilisatrices de publier des parcours.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :
      * journeys.publish
      * journeys.read

+++

* Lʼautorisation de haut niveau **[!DNL View journeys]** permet aux utilisateurs et utilisatrices de parcourir et dʼafficher les parcours.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * journeys.read

   * Spécifiques à Adobe Experience Platform :
      * segments.read
      * profiles.read

+++

* Lʼautorisation de haut niveau **[!DNL Manage journeys events, data sources and actions]** permet aux utilisateurs et utilisatrices de configurer des configurations d’événement et de données.

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

* L’autorisation de haut niveau **[!DNL View journeys events, data sources and actions]** permet aux utilisateurs et utilisatrices d’utiliser lʼévénement et les données dans le flux du parcours.

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

* L’autorisation de haut niveau **[!DNL View journeys report]** permet aux utilisateurs et utilisatrices dʼafficher en lecture seule un rapport sur le parcours.

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

## Ressource des règles Journey Optimizer {#journey-rules-capability}

* L’autorisation de haut niveau **[!DNL Manage frequency rules]** permet aux utilisateurs et utilisatrices de lire, créer, modifier, supprimer et activer/désactiver les règles de fréquence.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* L’autorisation de haut niveau **[!DNL View frequency rules]** permet aux utilisateurs et utilisatrices d’afficher les règles de fréquence.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * frequency_rules.read

+++

## Ressource Campaign {#campaign-capability}

* L’autorisation de haut niveau **[!DNL Export suppression list]** permet aux utilisateurs et utilisatrices de télécharger la liste de suppression sous forme de fichier CSV.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * suppression_list.export

   * Spécifiques à Adobe Experience Platform :
      * profiles.read
      * datasets.read

+++

* Lʼautorisation de haut niveau **[!DNL Manage campaigns]** permet aux utilisateurs et utilisatrices de créer et modifier/supprimer des campagnes.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* Lʼautorisation de haut niveau **[!DNL Publish campaigns]** permet aux utilisateurs et utilisatrices de publier des campagnes.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

+++

* L’autorisation de haut niveau **[!DNL View campaigns report]** permet aux utilisateurs et utilisatrices de lire et de modifier des rapports de campagne.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Ressource de gestion des décisions {#decisions-permissions}

* Lʼautorisation de haut niveau **[!DNL Manage decisions]** permet aux utilisateurs et utilisatrices de créer et de modifier/supprimer des **[!DNL Activity entities]** existantes, ainsi que de gérer les objets utilisés dans ces activités pour prendre des décisions.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à la gestion des décisions :
      * activities.read
      * activities.write
      * activities.delete
      * offer.read
      * offers.write
      * offers.delete
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

* Lʼautorisation de haut niveau **[!DNL View decisions]** permet aux utilisateurs et utilisatrices dʼutiliser une activité existante et les objets métier associés pour prendre des décisions.

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

* L’autorisation de haut niveau **[!DNL Manage offers]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer toutes les offres et tous les composants, ainsi que de lire les décisions et les collections.

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

* L’autorisation de haut niveau **[!DNL Manage ranking strategies]** permet aux utilisateurs et utilisatrices de lire, créer, modifier et supprimer des stratégies de classement.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à la gestion des décisions :
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offer.read
      * placements.read

+++

## Ressource des configurations de canal {#administration-permissions}

* Lʼautorisation de haut niveau **[!DNL Manage channel surface]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer des surfaces de canaux sur les canaux au niveau du sandbox.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
      * mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

+++

* Lʼautorisation de haut niveau **[!DNL Manage IP pools]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer la définition des affinités.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* Lʼautorisation de haut niveau **[!DNL Manage landing page settings]** permet aux utilisateurs et utilisatrices de lire, créer et modifier les sous-domaines et les préréglages des pages de destination.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* Lʼautorisation de haut niveau **[!DNL Manage messages general settings]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer des paramètres globaux au niveau du sandbox.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Spécifiques à Adobe Experience Platform :
      * schemas.read

+++

* L’autorisation de haut niveau **[!DNL Manage messages presets]** permet aux utilisateurs et utilisatrices de lire, créer, modifier et supprimer du branding de contenu.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Spécifique à la collecte de données :
      * Mobile_setting.read

+++

* L’autorisation de haut niveau **[!DNL Manage PTR records]** permet aux utilisateurs et utilisatrices de lire et de modifier les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* L&#39;autorisation de haut niveau **[!DNL Manage Seedlist]** permet de lire, créer, modifier et supprimer des listes de contrôle.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* L&#39;autorisation de haut niveau **[!DNL Manage SMS subdomains]** permet aux utilisateurs et utilisatrices de lire, créer, modifier et supprimer des sous-domaines de SMS.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* Lʼautorisation de haut niveau **[!DNL Manage subdomains delegation]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer les délégations de sous-domaines (y compris le groupe dʼadresses IP).

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* L’autorisation de haut niveau **[!DNL Manage suppression]** permet aux utilisateurs et utilisatrices de définir le nombre de bounces avant l’ajout d’une adresse e-mail à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans la liste de suppression.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* Lʼautorisation de haut niveau **[!DNL View PTR records]** permet aux utilisateurs et utilisatrices dʼafficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

+++ Elle comprend les autorisations de bas niveau suivantes :
   * Spécifiques à Journey Optimizer :

      * PTR_records.read
      * subdomains_delegation.read

+++

* Lʼautorisation de haut niveau **[!DNL View messages general settings]** permet aux utilisateurs et utilisatrices dʼafficher les paramètres généraux des messages, tels que lʼadresse dʼexécution.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_general_settings.read

   * Spécifiques à Adobe Experience Platform :
      * schemas.read

+++

* L’autorisation de haut niveau **[!DNL View messages presets]** permet aux utilisateurs et utilisatrices d’afficher les préréglages de message.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Spécifique à la collecte de données :
      * Mobile_setting.read

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


* L’autorisation de haut niveau **[!DNL View suppression list]** permet aux utilisateurs et utilisatrices d’afficher le contenu et les paramètres de la liste de suppression.

+++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :
      * suppression_list.view

   * Spécifiques à Adobe Experience Platform :
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

