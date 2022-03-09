---
title: Niveaux d'autorisation
description: En savoir plus sur les autorisations de haut et de bas niveau
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2a27c19766c84d8c65e8b21ba381754758d60cae
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 96%

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
   * parcours_events.read
   * parcours_data_sources.read
   * parcours_actions.read

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

## Fonction de messages {#message-capability}

### Autorisation [!DNL Manage messages] {#manage-messages}

Lʼautorisation de haut niveau **[!DNL Manage messages]** permet aux utilisateurs de créer et modifier/supprimer un message.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Spécifiques à Adobe Experience Platform :
   * segments.read
   * schemas.read

### Autorisation [!DNL Manage messages preview and test] {#mange-messages-preview}

L’autorisation de haut niveau **[!DNL Manage messages preview and test]** permet aux utilisateurs de prévisualiser un message personnalisé.

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

### Autorisation [!DNL Publish messages] {#publish-messages}

Lʼautorisation de haut niveau **[!DNL Publish messages]** permet aux utilisateurs de publier des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.publish

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * schemas.read
   * datasets.read

### Autorisation [!DNL View messages] {#view-messages}

Lʼautorisation de haut niveau **[!DNL View messages]** permet aux utilisateurs de lire uniquement les messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.read
   * messages_presets.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * segments.read

### Autorisation [!DNL View messages report] {#view-message-reports}

Lʼautorisation de haut niveau **[!DNL View messages report]** permet aux utilisateurs dʼafficher en lecture seule un rapport sur les e-mails et les notifications push.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

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
   * offers.read
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

### Autorisation [!DNL Manage ranking strategies] {#manage-decisions}

Lʼautorisation de haut niveau **[!DNL Manage ranking strategies]** permet aux utilisateurs de lire, de créer, de modifier et de supprimer un rapport de messages personnalisé et dʼutiliser des fonctionnalités dʼaction.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
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

### Autorisation [!DNL Manage messages general settings] {#manage-message-settings}

Lʼautorisation de haut niveau **[!DNL Manage messages general settings]** permet aux utilisateurs de créer, de modifier et de supprimer des paramètres globaux au niveau de lʼenvironnement sandbox.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Spécifiques à Adobe Experience Platform :
   * schemas.read

### Autorisation [!DNL View messages general settings] {#view-message-settings}

Lʼautorisation de haut niveau **[!DNL View messages general settings]** permet aux utilisateurs dʼafficher les paramètres généraux des messages, tels que lʼadresse dʼexécution.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_general_settings.read
* Spécifiques à Adobe Experience Platform :
   * schemas.read

### Autorisation [!DNL Manage messages presets] {#manage-message-presets}

Lʼautorisation de haut niveau **[!DNL Manage messages presets]** permet aux utilisateurs de créer, de modifier et de supprimer des préréglages de message sur les canaux au niveau de lʼenvironnement sandbox.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

### Autorisation [!DNL View messages presets] {#view-message-presets}

Lʼautorisation de haut niveau **[!DNL View messages presets]** permet aux utilisateurs dʼafficher les préréglages de message afin de savoir lesquels utiliser lors de la création dʼun message.

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

Le **[!DNL Manage landing page settings]** l’autorisation de haut niveau permet aux utilisateurs de lire, créer et modifier des sous-domaines de landing page et des paramètres prédéfinis.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete
