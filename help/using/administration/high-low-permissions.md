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
TQID: https://experienceleague.adobe.com/JmWqA2lkS0vWlssVYWycq-gvC6IRrrmAokJj1AGINxc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 1995
ht-degree: 73%

---

# Niveaux d’autorisation {#high-low-permissions}

>[!BEGINSHADEBOX]

**Sur cette page :** comprenez comment les autorisations de haut niveau regroupent les autorisations de bas niveau sous-jacentes pour chaque ressource, afin que vous puissiez accorder aux rôles l’accès à la fonctionnalité dont vos utilisateurs ont besoin.

>[!ENDSHADEBOX]

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
     <!--
      * experiments.read
      * experiments.write
      * experiments.delete
-->

+++

* Lʼautorisation de haut niveau **[!DNL Publish campaigns]** permet aux utilisateurs et utilisatrices de publier des campagnes.

  +++ Elle comprend les autorisations de bas niveau suivantes :

   * Spécifiques à Journey Optimizer :

      * campaign-read
      * campaign-publish
     <!--
      * experiments.activate    
      -->

  +++

* L’autorisation de haut niveau **[!DNL View campaigns report]** permet aux utilisateurs et utilisatrices de lire et de modifier des rapports de campagne.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :
      * campaign.read
      * campaign-report.read
     <!--
      * experiments.read
      * experiments_report.read
      -->

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

* **[!DNL Manage key registry]** autorisation de haut niveau permet aux utilisateurs d’afficher, de créer, de faire pivoter et de révoquer des clés dans le registre des clés.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :
      * key-registry.read
      * key-registry.write

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

* **[!DNL Manage seed lists]** autorisation de haut niveau permet aux utilisateurs et utilisatrices de lire, créer, modifier et supprimer des listes de contrôle.

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

* **[!DNL View key registry]** autorisation de haut niveau permet aux utilisateurs d’afficher la liste du registre des clés et les détails des clés.

  +++ Elle comprend les autorisations de bas niveau suivantes :  

   * Spécifiques à Journey Optimizer :
      * key-registry.read

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

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Les rôles Journey Optimizer sont créés à partir d’autorisations de haut niveau, chacune d’elles regroupant les droits spécifiques de bas niveau sur l’API dont les utilisateurs ont besoin pour lire, écrire, publier ou supprimer des ressources dans les parcours, les campagnes, les décisions, les configurations de canal, etc.

**Intentions:**

* Comprendre la distinction entre les autorisations de haut niveau et de bas niveau
* Identifier les autorisations de bas niveau accordées par chaque autorisation de haut niveau
* Configurez des rôles précisément pour les parcours, les campagnes, la gestion des décisions, les configurations de canal et les campagnes orchestrées
* Accorder l’accès à l’assistant AI pour la génération de contenu
* Comprenez ce que permet l’autorisation Publier des parcours par rapport à l’autorisation Gérer les parcours .

**Glossaire:**

* **Autorisation de haut niveau** : autorisation nommée attribuée à un rôle (par exemple, Gérer les parcours, Publier les parcours) qui englobe une ou plusieurs autorisations de bas niveau *(spécifiques au produit)*
* **Autorisation de bas niveau** : droit granulaire au niveau de l’API (par exemple, parcours.read, parcours.write) dérivé de et inclus dans une *d’autorisation de haut niveau (spécifique au produit)*
* **Rôle** : ensemble d’utilisateurs partageant les mêmes autorisations et sandbox au sein de l’organisation *(spécifique au produit)*

**Terminologie:**

* Ne les confondez pas : « Autorisation de haut niveau » (droit nommé assignable à un rôle) ≠ « Autorisation de bas niveau » (droit API granulaire sous-jacent, non directement assignable)
* Ne les confondez pas : « Gérer les parcours » (permet la création, la modification, la suppression, l’arrêt, y compris l’exécution en direct, le mode test et l’essai) ≠ « Publier les parcours » (permet la publication, le démarrage du mode test, le démarrage de l’essai, la mise en pause et la reprise des parcours)
* Ne les confondez pas : « Gérer les événements parcours, les sources de données et les actions » (CRUD complet sur les événements, les sources, les actions) ≠ « Afficher les événements parcours, les sources de données et les actions » (accès en lecture seule à ces objets)
* Ne les confondez pas : « Générer le contenu » (accès à l’assistant AI dans Journey Optimizer) ≠ d’autres autorisations de parcours ou de campagne
* Ne les confondez pas : « Mode test » (référencé dans Publication de parcours et Gestion des parcours en tant que mode d’exécution de parcours pouvant être démarré ou arrêté) ≠ « Exécution d’essai » (un mode d’exécution de parcours distinct également référencé dans ces mêmes autorisations)

**FAQ:**

* **Q : L’autorisation Gérer les parcours permet-elle à un utilisateur de publier des parcours ?** — Non ; la publication de parcours nécessite l’autorisation de haut niveau Publier les parcours .
* **Q : Qu’accorde l’autorisation Générer du contenu** — Accès à l’assistant AI dans Journey Optimizer.
* **Q : Un utilisateur peut-il configurer des événements de parcours sans l’autorisation Gestion des parcours ?** — Oui ; la gestion des événements parcours, des sources de données et des actions est une autorisation de haut niveau distincte couvrant la configuration des événements, des sources de données et des actions.
* **Q : Quelles autorisations de bas niveau sont incluses dans le rapport Affichage des parcours ?** — parcours_report.read et messages_report.read, plus datasets.read, queries.read, queries.write et queries.delete de Adobe Experience Platform.

+++
<!-- ai-accordion-version: 1 | source-hash: d1d9ebf9 -->
