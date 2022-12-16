---
solution: Journey Optimizer
product: journey optimizer
title: Niveaux d'autorisation
description: En savoir plus sur les autorisations de haut et de bas niveau
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 100%

---

# Niveaux d&#39;autorisation {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Chaque profil de produit est constitué d&#39;autorisations permettant aux utilisateurs d&#39;accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau** : représente les différentes autorisations qui peuvent être attribuées au **[!UICONTROL profil de produit]** dans [!DNL Admin console], telles que **[!DNL Publish journeys]** et **[!DNL Manage subdomains delegation]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation de bas niveau** : représente les différentes autorisations qui proviennent de l&#39;autorisation de haut niveau.

Par exemple, le profil de produit **[!DNL Journey administrator]** se voit attribuer lʼautorisation **[!DNL Manage journeys]**. À partir de cette autorisation, les autorisations de bas niveau permettent à lʼadministrateur de parcours dʼécrire, de lire et de supprimer des parcours.

## Fonction de parcours {#journey-capability}

### Autorisation [!DNL Manage journeys] {#manage-journeys}

Lʼautorisation de haut niveau **[!DNL Manage journeys]** permet aux utilisateurs de créer des parcours et de modifier/supprimer des parcours existants, ainsi que dʼaccéder aux objets utilisés dans la zone de travail de parcours pour concevoir le flux du parcours.

Elle comprend les autorisations de bas niveau suivantes :

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

### Autorisation [!DNL Publish journeys] {#publish-journeys}

Lʼautorisation de haut niveau **[!DNL Publish journeys]** permet aux utilisateurs de publier des parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys.publish
   * journeys.read

### Autorisation [!DNL View journeys] {#view-journeys}

Lʼautorisation de haut niveau **[!DNL View journeys]** permet aux utilisateurs de parcourir et dʼafficher les parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys.read

* Spécifiques à Adobe Experience Platform :
   * segments.read
   * profiles.read

### Autorisation [!DNL Manage journeys events, data sources and actions] {#manage-journeys-events}

Lʼautorisation de haut niveau **[!DNL Manage journeys events, data sources and actions]** permet aux utilisateurs de configurer des configurations d’événement et de données.

Elle comprend les autorisations de bas niveau suivantes :

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

### Autorisation [!DNL View journeys events, data sources and actions] {#view-journeys-event}

L’autorisation de haut niveau **[!DNL View journeys events, data sources and actions]** permet aux utilisateurs d’utiliser lʼévénement et les données dans le flux du parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Autorisation [!DNL View journeys report] {#view-journeys-report}

L’autorisation de haut niveau **[!DNL View journeys report]** permet aux utilisateurs dʼafficher en lecture seule un rapport sur le parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys_report.read
   * messages_report.read

* Spécifiques à Adobe Experience Platform :
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Fonction de gestion des décisions {#decisions-permissions}

### Autorisation [!DNL Manage decisions] {#manage-decisioning}

Lʼautorisation de haut niveau **[!DNL Manage decisions]** permet aux utilisateurs de créer et de modifier/supprimer des **[!DNL Activity entities]** existantes, ainsi que de gérer les objets utilisés dans ces activités pour prendre des décisions.

Elle comprend les autorisations de bas niveau suivantes :

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

### Autorisation [!DNL View decisions] {#view-decisions}

Lʼautorisation de haut niveau **[!DNL View decisions]** permet aux utilisateurs dʼutiliser une activité existante et les objets métier associés pour prendre des décisions.

Elle comprend les autorisations de bas niveau suivantes :

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

### Autorisation [!DNL Publish offers decisioning] {#publish-decisions}

Lʼautorisation de haut niveau **[!DNL Publish offers decisioning]** permet aux utilisateurs dʼobtenir un accès pour approuver/annuler lʼapprobation des activités dʼoffre.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * offer_activity.read
   * offer.read
   * offer.write
   * offer.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### Autorisation [!DNL Manage ranking strategies] {#manage-ranking-strategies}

L&#39;autorisation **[!DNL Manage ranking strategies]** de haut niveau permet aux utilisateurs de lire, créer, modifier et supprimer des stratégies de classement.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offer.read
   * placements.read

## Fonction d&#39;administration {#administration-permissions}

### Autorisation [!DNL Manage subdomains delegation] {#manage-subdomain}

Lʼautorisation de haut niveau **[!DNL Manage subdomains delegation]** permet aux utilisateurs de créer, de modifier et de supprimer les délégations de sous-domaines (y compris le groupe dʼadresses IP).

Elle comprend les autorisations de bas niveau suivantes :

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### Autorisation [!DNL Manage PTR records] {#manage-ptr}

L’autorisation de haut niveau **[!DNL Manage PTR records]** permet aux utilisateurs de lire et de modifier les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### Autorisation [!DNL View PTR records] {#view-ptr}

Lʼautorisation de haut niveau **[!DNL View PTR records]** permet aux utilisateurs dʼafficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* subdomains_delegation.read

### Autorisation [!DNL Manage IP pools] {#manage-ip-pools}

Lʼautorisation de haut niveau **[!DNL Manage IP pools]** permet aux utilisateurs de créer, de modifier et de supprimer la définition des affinités.

Elle comprend les autorisations de bas niveau suivantes :

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

### Autorisation [!DNL Manage channel surface] {#manage-channel-surface}

Lʼautorisation de haut niveau **[!DNL Manage channel surface]** permet aux utilisateurs de créer, de modifier et de supprimer des surfaces de canaux sur les canaux au niveau de la sandbox.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

### Autorisation [!DNL View channel surface] {#view-channel-surface}

L’autorisation de haut niveau **[!DNL View channel surface]** permet aux utilisateurs d’afficher les surfaces des canaux afin de connaître celles à utiliser.

Elle comprend les autorisations de bas niveau suivantes :

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (à partir de la collecte de données dʼAdobe Experience Platform)

### Autorisation [!DNL Manage suppression] {#manage-suppression}

L’autorisation de haut niveau **[!DNL Manage suppression]** permet aux utilisateurs de définir le nombre de bounces avant l’ajout d’une adresse e-mail à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Autorisation [!DNL View suppression list] {#view-suppression-list}

L’autorisation de haut niveau **[!DNL View suppression list]** permet aux utilisateurs d’afficher le contenu et les paramètres de la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * suppression_list.view

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### Autorisation [!DNL Export suppression list] {#export-suppression-list}

L’autorisation de haut niveau **[!DNL Export suppression list]** permet aux utilisateurs de télécharger la liste de suppression sous forme de fichier CSV.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * suppression_list.export

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### Autorisation [!DNL Manage landing page settings] {#manage-landing-page-settings}

Lʼautorisation de haut niveau **[!DNL Manage landing page settings]** permet aux utilisateurs de lire, créer et modifier les sous-domaines et les préréglages des pages de destination.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### Autorisation [!DNL Manage frequency rules] {#manage-frequency-rules}

L’autorisation de haut niveau **[!DNL Manage frequency rules]** permet aux utilisateurs de lire, de créer, de modifier, de supprimer et d’activer/désactiver les règles de fréquence.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### Autorisation [!DNL View frequency rules] {#view-frequency-rules}

L’autorisation de haut niveau **[!DNL View frequency rules]** permet aux utilisateurs d’afficher les règles de fréquence.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * frequency_rules.read
