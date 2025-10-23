---
solution: Journey Optimizer
product: journey optimizer
title: Niveaux d’autorisation
description: Découvrez les autorisations de haut niveau et de bas niveau qui permettent aux utilisateurs et aux utilisatrices d’accéder aux différentes fonctionnalités.
topic: Administration
feature: Access Management
role: Admin, Developer
level: Experienced
keywords: autorisation, haut niveau, bas niveau, profil, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '1303'
ht-degree: 100%

---

# Niveaux d’autorisation {#high-low-permissions}


Chaque rôle comprend des autorisations permettant aux utilisateurs et aux utilisatrices d’accéder aux différentes fonctionnalités.

Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau** : représente les différentes autorisations qui peuvent être attribuées au **[!UICONTROL rôle]**, telles que **[!DNL Publish journeys]** et **[!DNL Manage subdomains delegation]**. Les autorisations de haut niveau englobent les autorisations de bas niveau. Les autorisations de haut niveau sont présentées dans [cette page](ootb-permissions.md).

* **Autorisation de bas niveau** : il s’agit des différentes autorisations qui découlent de l’autorisation de haut niveau.

Par exemple, le rôle **[!DNL Journey administrator]** se voit attribuer lʼautorisation **[!DNL Manage journeys]**. À partir de cette autorisation, les autorisations de bas niveau permettent à lʼadministrateur ou l’adminnistratrice de parcours dʼécrire, de lire et de supprimer des parcours.

![](assets/do-not-localize/permissions.png){width="70%"}


## Ressource de parcours {#journey-capability}

* Lʼautorisation de haut niveau **[!DNL Manage journeys]** permet aux utilisateurs et utilisatrices de créer des parcours et de modifier/supprimer/arrêter/mettre en pause des parcours existants, ainsi que dʼaccéder aux objets utilisés dans la zone de travail de parcours pour concevoir le flux du parcours.

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

* L’autorisation de haut niveau **[!DNL Export suppression list]** permet aux utilisateurs et aux utilisatrices de télécharger la liste de suppression sous forme de fichier CSV.

  +++ Elle comprend les autorisations de bas niveau suivantes : 

   * Spécifiques à Journey Optimizer :
      * suppression_list.export

   * Spécifiques à Adobe Experience Platform :
      * profiles.read
      * datasets.read

  +++

* Lʼautorisation de haut niveau **[!DNL Manage campaigns]** permet aux utilisateurs et aux utilisatrices de créer et de modifier/supprimer des campagnes.

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
      * offers.read
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
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Spécifiques à Adobe Experience Platform :
      * schemas.read
      * segment.read
      * datasets.read

  +++

* L’autorisation de haut niveau **[!DNL Manage offers]** permet aux utilisateurs et aux utilisatrices de créer, de modifier et de supprimer toutes les offres et tous les composants, ainsi que de lire les décisions et les collections.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à la gestion des décisions :
      * offers_activity.read
      * offers.read
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
      * offers.read
      * placements.read

  +++

## Ressource des configurations de canal {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ This permission includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* Lʼautorisation de haut niveau **[!DNL Manage file routing]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer les configuration des routages.

  +++ Elle comprend les autorisations de bas niveau suivantes :  
   * Spécifiques à Journey Optimizer :

      * file_routing.read
      * file_routing.write
      * file_routing.delete

  +++

* Lʼautorisation de haut niveau **[!DNL Manage IP pools]** permet aux utilisateurs et aux utilisatrices de créer, de modifier et de supprimer la définition des affinités.

  +++ Elle comprend les autorisations de bas niveau suivantes :  
   * Spécifiques à Journey Optimizer :
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

  +++

* Lʼautorisation de niveau supérieur **[!DNL Manage landing page settings]** permet aux utilisateurs et aux utilisatrices de lire, de créer et de modifier les sous-domaines et les préréglages des pages de destination.

  +++ Elle comprend les autorisations de bas niveau suivantes : 

   * Spécifiques à Journey Optimizer :

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

  +++

* Lʼautorisation de niveau supérieur **[!DNL Manage messages general settings]** permet aux utilisateurs et aux utilisatrices de créer, de modifier et de supprimer des paramètres globaux au niveau du sandbox.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Spécifiques à Adobe Experience Platform :
      * schemas.read

  +++

* Lʼautorisation de haut niveau **[!DNL Manage messages presets]** permet aux utilisateurs et utilisatrices de créer, modifier et supprimer des configurations de canaux sur les canaux au niveau du sandbox.

  +++ Elle comprend les autorisations de bas niveau suivantes : 

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Spécifique à la collecte de données :
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

  +++

* L’autorisation de haut niveau **[!DNL Manage PTR records]** permet aux utilisateurs et aux utilisatrices de lire et de modifier les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

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

* L&#39;autorisation de haut niveau **[!DNL Manage SMS subdomains]** permet aux utilisateurs et aux utilisatrices de lire, de créer, de modifier et de supprimer des sous-domaines de SMS.

  +++ Elle comprend les autorisations de bas niveau suivantes : 

   * Spécifiques à Journey Optimizer :
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

  +++

* Lʼautorisation de haut niveau **[!DNL Manage subdomains delegations]** permet aux utilisateurs et aux utilisatrices de créer, de modifier et de supprimer des délégations de sous-domaines (y compris le groupe dʼadresses IP).

  +++ Elle comprend les autorisations de bas niveau suivantes :  
   * Spécifiques à Journey Optimizer :

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

  +++

* L’autorisation de haut niveau **[!DNL Manage suppression]** permet aux utilisateurs et aux utilisatrices de définir le nombre de rebonds avant l’ajout d’une adresse e-mail à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans la liste de suppression.

  +++ Elle comprend les autorisations de bas niveau suivantes :  
   * Spécifiques à Journey Optimizer :
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

  +++

* L’autorisation de haut niveau **[!DNL View file routing]** permet aux utilisateurs et utilisatrices d’afficher les configurations de routage de fichiers.

  +++ Elle comprend les autorisations de bas niveau suivantes :  
   * Spécifiques à Journey Optimizer :

      * file_routing.read

  +++

* Lʼautorisation de haut niveau **[!DNL View messages general settings]** permet aux utilisateurs et aux utilisatrices dʼafficher les paramètres généraux des messages, tels que lʼadresse dʼexécution.

  +++ Elle comprend les autorisations de bas niveau suivantes : 

   * Spécifiques à Journey Optimizer :
      * messages_general_settings.read

   * Spécifiques à Adobe Experience Platform :
      * schemas.read

  +++

* L’autorisation de haut niveau **[!DNL View messages presets]** permet aux utilisateurs et aux utilisatrices d’afficher les préréglages de message.

  +++ Elle comprend les autorisations de bas niveau suivantes : 

   * Spécifiques à Journey Optimizer :
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Spécifique à la collecte de données :
      * Mobile_setting.read

  +++

* Lʼautorisation de haut niveau **[!DNL View PTR records]** permet aux utilisateurs et aux utilisatrices dʼafficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

  +++ Elle comprend les autorisations de bas niveau suivantes : 
   * Spécifiques à Journey Optimizer :

      * PTR_records.read
      * subdomains_delegation.read

  +++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ This permission includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* L’autorisation de haut niveau **[!DNL View suppression list]** permet aux utilisateurs et aux utilisatrices d’afficher le contenu et les paramètres de la liste de suppression.

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

  +++ This permission includes the following low-level permissions: 
-->

## Ressource pour l’assistant IA {#ai-permissions}

* L’autorisation de haut niveau **[!DNL Generate content]** permet aux utilisateurs et aux utilisatrices d’accéder à l’Assistant IA dans Journey Optimizer.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :
      * ai-assistant-generated-content.generate

  +++

## Ressource des campagnes orchestrées {#ai-orchestrated-campaign}

* Lʼautorisation de haut niveau **[!DNL Manage orchestrated campaigns]** permet aux utilisateurs et aux utilisatrices de créer et de modifier/supprimer des campagnes orchestrées.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :

      * orchestrated_campaigns.read
      * orchestrated_campaigns.write
      * orchestrated_campaigns.delete
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.write
      * cjm-message.delete
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * cjm-message-preview-test.write
      * experiment.read
      * experiment.write
      * experiment.delete

   * Spécifiques à Adobe Experience Platform :

      * identity-graph.read
      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read
      * sandboxes.view

  +++

* L’autorisation de haut niveau **[!DNL Manage orchestrated campaigns admin]** permet aux utilisateurs et aux utilisatrices de créer et de modifier/supprimer des liens et des réconciliations entre les profils Adobe Experience Platform et les entités de stockage relationnel.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :

      * cjm-orchestrated-campaign-admin.read
      * cjm-orchestrated-campaign-admin.write
      * cjm-orchestrated-campaign-admin.delete

  +++

* Lʼautorisation de haut niveau **[!DNL Publish orchestrated campaigns]** permet aux utilisateurs et aux utilisatrices de publier des campagnes orchestrées.

  +++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * cjm-orchestrated-campaign.read
      * cjm-orchestrated-campaign.publish
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.publish
      * cjm-library-item.read

   * Spécifiques à Adobe Experience Platform :

      * sandboxes.view

  +++

* L’autorisation de haut niveau **[!DNL View orchestrated campaigns]** permet aux utilisateurs et aux utilisatrices d’afficher la campagne orchestrée et son contenu.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :

      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * experiment.read

   * Spécifiques à Adobe Experience Platform :

      * sandboxes.view
      * segments.read
      * profiles.read

  +++

* L’autorisation de haut niveau **[!DNL View orchestrated campaigns admin]** permet aux utilisateurs et aux utilisatrices d’afficher les paramètres d’administration, mais sans pouvoir les modifier.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :

      * cjm-orchestrated-campaign-admin.read

  +++

* L’autorisation de haut niveau **[!DNL View orchestrated campaigns report]** permet aux utilisateurs et aux utilisatrices d’afficher les performances des campagnes orchestrées dans les rapports dynamiques et professionnels.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :

      * cjm-orchestrated-campaign-reports.read
      * cjm-message-report.read
      * cjm-channel-report.read
      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * experiment.read
      * experiment-report.read

   * Spécifiques à Adobe Experience Platform :

      * sandboxes.view
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++
