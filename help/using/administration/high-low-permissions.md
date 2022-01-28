---
title: Niveaux d'autorisation
description: En savoir plus sur les autorisations de haut et de bas niveau
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: bbeecbacb4838dfb0794d5625eb2774cf4b983ef
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 55%

---

# Niveaux d&#39;autorisation {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Chaque profil de produit est constitué d&#39;autorisations permettant aux utilisateurs d&#39;accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau**: représente les différentes autorisations qui peuvent être affectées à **[!UICONTROL Profil de produit]** dans le [!DNL Admin console], par exemple **[!DNL Publish journeys]** et **[!DNL Manage subdomains delegation]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation de bas niveau** : représente les différentes autorisations qui proviennent de l&#39;autorisation de haut niveau.

Par exemple, la variable **[!DNL Journey administrator]** le profil de produit se voit attribuer la valeur **[!DNL Manage journeys]** autorisation. À partir de cette autorisation, les autorisations de bas niveau permettent à l&#39;administrateur de parcours d&#39;écrire, de lire et de supprimer des parcours.

## Fonction de parcours {#journey-capability}

### [!DNL Manage journeys] autorisation {#manage-journeys}

Le **[!DNL Manage journeys]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des Parcours existants, ainsi que d’accéder aux objets utilisés dans la zone de travail du parcours pour créer le flux de parcours.

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

### [!DNL Publish journeys] autorisation {#publish-journeys}

Le **[!DNL Publish journeys]** l’autorisation de haut niveau permet aux utilisateurs de publier des parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys.publish
   * journeys.read

### [!DNL View journeys] autorisation {#view-journeys}

Le **[!DNL View journeys]** l’autorisation de haut niveau permet aux utilisateurs de parcourir et d’afficher des parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys.read

* Spécifiques à Adobe Experience Platform :
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] autorisation {#manage-journeys-events}

Le **[!DNL Manage journeys events, data sources and actions]** l’autorisation de haut niveau permet aux utilisateurs de configurer des configurations d’événement et de données.

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

### [!DNL View journeys events, data sources and actions] autorisation {#view-journeys-event}

Le **[!DNL View journeys events, data sources and actions]** l’autorisation de haut niveau permet aux utilisateurs d’utiliser l’événement et les données dans le flux de parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * parcours_events.read
   * parcours_data_sources.read
   * parcours_actions.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] autorisation {#view-journeys-report}

Le **[!DNL View journeys report]** l’autorisation de haut niveau permet aux utilisateurs de créer des rapports de parcours en lecture seule.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys_report.read
   * messages_report.read

* Spécifiques à Adobe Experience Platform :
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Fonction de messages {#message-capability}

### [!DNL Manage messages] autorisation {#manage-messages}

Le **[!DNL Manage messages]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Spécifiques à Adobe Experience Platform :
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] autorisation {#mange-messages-preview}

Le **[!DNL Manage messages preview and test]** l’autorisation de haut niveau permet aux utilisateurs de prévisualiser un message personnalisé.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### [!DNL Publish messages] autorisation {#publish-messages}

Le **[!DNL Publish messages]** l’autorisation de haut niveau permet aux utilisateurs de publier des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.publish

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] autorisation {#view-messages}

Le **[!DNL View messages]** l’autorisation de haut niveau permet aux utilisateurs de lire uniquement les messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.read
   * messages_presets.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * segments.read

### [!DNL View messages report] autorisation {#view-message-reports}

Le **[!DNL View messages report]** l’autorisation de haut niveau permet aux utilisateurs d’envoyer des rapports push et des e-mails en lecture seule.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Fonction de gestion des décisions {#decisions-permissions}

### [!DNL Manage decisions] autorisation {#manage-decisioning}

Le **[!DNL Manage decisions]** l’autorisation de haut niveau permet aux utilisateurs de créer et de modifier/supprimer des **[!DNL Activity entities]**, ainsi que de gérer les objets utilisés dans ces activités pour prendre des décisions.

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

### [!DNL View decisions] autorisation {#view-decisions}

Le **[!DNL View decisions]** l’autorisation de haut niveau permet aux utilisateurs d’utiliser une activité existante et les objets commerciaux associés pour prendre des décisions.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] autorisation {#publish-decisions}

Le **[!DNL Publish offers decisioning]** l’autorisation de haut niveau permet aux utilisateurs d’accéder à l’approbation/l’annulation de l’approbation des activités d’offre.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * offer_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] autorisation {#manage-decisions}

Le **[!DNL Manage ranking strategies]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier et supprimer un rapport de messages personnalisés et d’utiliser des fonctions d’action.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Fonction d&#39;administration {#administration-permissions}

### [!DNL Manage subdomains delegation] autorisation {#manage-subdomain}

Le **[!DNL Manage subdomains delegation]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des délégations de sous-domaines (y compris le pool d’adresses IP).

Elle comprend les autorisations de bas niveau suivantes :

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] autorisation {#manage-ptr}

Le **[!DNL Manage PTR records]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer, modifier et supprimer des enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] autorisation {#view-ptr}

Le **[!DNL View PTR records]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] autorisation {#manage-ip-pools}

Le **[!DNL Manage IP pools]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer la définition d’affinité.

Elle comprend les autorisations de bas niveau suivantes :

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] autorisation {#manage-message-settings}

Le **[!DNL Manage messages general settings]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des paramètres globaux au niveau de l’environnement de test.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Spécifiques à Adobe Experience Platform :
   * schemas.read

### [!DNL View messages general settings] autorisation {#view-message-settings}

Le **[!DNL View messages general settings]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les paramètres généraux des messages, tels que l’adresse d’exécution.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_general_settings.read
* Spécifiques à Adobe Experience Platform :
   * schemas.read

### [!DNL Manage messages presets] autorisation {#manage-message-presets}

Le **[!DNL Manage messages presets]** l’autorisation de haut niveau permet aux utilisateurs de créer, modifier et supprimer des paramètres prédéfinis de message sur plusieurs canaux au niveau de l’environnement de test.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

### [!DNL View messages presets] autorisation {#view-message-presets}

Le **[!DNL View messages presets]** l’autorisation de haut niveau permet aux utilisateurs d’afficher les paramètres prédéfinis de message afin de connaître les paramètres prédéfinis de message à utiliser lors de la création d’un message.

Elle comprend les autorisations de bas niveau suivantes :

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (à partir de la collecte de données Adobe Experience Platform)

### [!DNL Manage suppression] autorisation {#manage-suppression}

Le **[!DNL Manage suppression]** l’autorisation de haut niveau permet aux utilisateurs de définir le nombre de rebonds avant l’ajout d’une adresse électronique à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans/depuis la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] autorisation {#view-suppression-list}

Le **[!DNL View suppression list]** l’autorisation de haut niveau permet aux utilisateurs d’afficher le contenu et les paramètres de la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * suppression_list.view

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] autorisation {#export-suppression-list}

Le **[!DNL Export suppression list]** l’autorisation de haut niveau permet aux utilisateurs de télécharger la liste de suppression sous la forme d’un fichier CSV.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * suppression_list.export

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * datasets.read
