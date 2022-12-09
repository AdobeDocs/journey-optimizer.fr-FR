---
solution: Journey Optimizer
product: journey optimizer
title: Niveaux d’autorisation
description: En savoir plus sur les autorisations générales et de bas niveau
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Niveaux d’autorisation {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Chaque profil de produit est constitué d’autorisations permettant aux utilisateurs d’accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau**: représente les différentes autorisations qui peuvent être affectées à **[!UICONTROL Product profile]** dans le [!DNL Admin console], par exemple **[!DNL Publish journeys]** et **[!DNL Manage subdomains delegation]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation de bas niveau**: représente les différentes autorisations qui proviennent de l’autorisation de niveau supérieur.

Par exemple, la variable **[!DNL Journey administrator]** le profil de produit se voit attribuer la valeur **[!DNL Manage journeys]** autorisation. Grâce à cette autorisation, les autorisations de bas niveau permettent à l’administrateur du parcours d’écrire, de lire et de supprimer des parcours.

## Fonctionnalité de parcours {#journey-capability}

### [!DNL Manage journeys] autorisation {#manage-journeys}

Le **[!DNL Manage journeys]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des parcours existants, ainsi que d’accéder aux objets utilisés dans la zone de travail du parcours pour créer le flux du parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Spécifique à Adobe Experience Platform :

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] autorisation {#publish-journeys}

Le **[!DNL Publish journeys]** l’autorisation de haut niveau permet aux utilisateurs de publier des parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys.publish
   * journeys.read

### [!DNL View journeys] autorisation {#view-journeys}

Le **[!DNL View journeys]** l’autorisation de haut niveau permet aux utilisateurs de parcourir et d’afficher les parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys.read

* Spécifique à Adobe Experience Platform :
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] autorisation {#manage-journeys-events}

Le **[!DNL Manage journeys events, data sources and actions]** l’autorisation de haut niveau permet aux utilisateurs de configurer des configurations d’événement et de données.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys_events.read
   * journeys_events.write
   * journeys_events.delete
   * journeys_data_sources.read
   * journeys_data_sources.write
   * journeys_data_sources.delete
   * journeys_actions.read
   * journeys_actions.write
   * journeys_actions.delete

* Spécifique à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] autorisation {#view-journeys-event}

Le **[!DNL View journeys events, data sources and actions]** l’autorisation de haut niveau permet aux utilisateurs d’utiliser l’événement et les données dans le flux de parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Spécifique à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] autorisation {#view-journeys-report}

Le **[!DNL View journeys report]** l’autorisation de haut niveau permet aux utilisateurs de créer un rapport de parcours en lecture seule.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys_report.read
   * messages_report.read

* Spécifique à Adobe Experience Platform :
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Fonctionnalité de gestion des décisions {#decisions-permissions}

### [!DNL Manage decisions] autorisation {#manage-decisioning}

Le **[!DNL Manage decisions]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des **[!DNL Activity entities]**, ainsi que de gérer les objets utilisés dans ces activités pour prendre des décisions.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à la gestion des décisions :
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

* Spécifique à Adobe Experience Platform :
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] autorisation {#view-decisions}

Le **[!DNL View decisions]** l’autorisation de haut niveau permet aux utilisateurs d’utiliser une activité existante et les objets commerciaux associés pour prendre des décisions.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à la gestion des décisions :
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Spécifique à Adobe Experience Platform :
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] autorisation {#publish-decisions}

Le **[!DNL Publish offers decisioning]** l’autorisation de haut niveau permet aux utilisateurs d’accéder à l’approbation/l’annulation de l’approbation des activités d’offre.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à la gestion des décisions :
   * offer_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Spécifique à Adobe Experience Platform :
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] autorisation {#manage-ranking-strategies}

Le **[!DNL Manage ranking strategies]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier et supprimer des stratégies de classement.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à la gestion des décisions :
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Fonctionnalité d&#39;administration {#administration-permissions}

### [!DNL Manage subdomains delegation] autorisation {#manage-subdomain}

Le **[!DNL Manage subdomains delegation]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des délégations de sous-domaines (y compris le pool d’adresses IP).

Elle comprend les autorisations de bas niveau suivantes :

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] autorisation {#manage-ptr}

Le **[!DNL Manage PTR records]** l’autorisation de haut niveau permet aux utilisateurs de lire et de modifier les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] autorisation {#view-ptr}

Le **[!DNL View PTR records]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] autorisation {#manage-ip-pools}

Le **[!DNL Manage IP pools]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer la définition d’affinité.

Elle comprend les autorisations de bas niveau suivantes :

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### [!DNL Manage channel surface] autorisation {#manage-channel-surface}

Le **[!DNL Manage channel surface]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des surfaces de canal sur les canaux au niveau de l’environnement de test.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (à partir d’Adobe Experience Platform Launch)

### [!DNL View channel surface] autorisation {#view-channel-surface}

Le **[!DNL View channel surface]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les surfaces des canaux afin de connaître les surfaces des canaux à utiliser.

Elle comprend les autorisations de bas niveau suivantes :

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (à partir de la collecte de données Adobe Experience Platform)

### [!DNL Manage suppression] autorisation {#manage-suppression}

Le **[!DNL Manage suppression]** l’autorisation de haut niveau permet aux utilisateurs de définir le nombre de rebonds avant l’ajout d’une adresse électronique à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans/depuis la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* delete_rules.read
* delete_rules.write
* delete_rules.delete
* delete_list.write
* delete_list.delete

### [!DNL View suppression list] autorisation {#view-suppression-list}

Le **[!DNL View suppression list]** l’autorisation de haut niveau permet aux utilisateurs d’afficher le contenu et les paramètres de la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * delete_list.view

* Spécifique à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] autorisation {#export-suppression-list}

Le **[!DNL Export suppression list]** l’autorisation de haut niveau permet aux utilisateurs de télécharger la liste de suppression sous la forme d’un fichier CSV.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * delete_list.export

* Spécifique à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] autorisation {#manage-landing-page-settings}

Le **[!DNL Manage landing page settings]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer et modifier des sous-domaines de landing page et des paramètres prédéfinis.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] autorisation {#manage-frequency-rules}

Le **[!DNL Manage frequency rules]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier, supprimer et activer/désactiver les règles de fréquence.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] autorisation {#view-frequency-rules}

Le **[!DNL View frequency rules]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les règles de fréquence.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * frequency_rules.read
