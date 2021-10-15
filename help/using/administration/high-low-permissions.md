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
source-git-commit: da885bd5e29ff3454fef1c6b362f0e646fe8c39a
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 100%

---

# Niveaux d&#39;autorisation {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Chaque profil de produit est constitué d&#39;autorisations permettant aux utilisateurs d&#39;accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation de haut niveau** : représente les différentes autorisations qui peuvent être affectées au **[!UICONTROL profil de produit]** dans [!DNL Admin console], telles que **[!UICONTROL Publier les parcours]** et **[!UICONTROL Gérer la délégation des sous-domaines]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation de bas niveau** : représente les différentes autorisations qui proviennent de l&#39;autorisation de haut niveau.

Par exemple, le profil de produit **[!UICONTROL Administrateur de parcours]** se voit attribuer l&#39;autorisation **[!UICONTROL Gérer les parcours]**. À partir de cette autorisation, les autorisations de bas niveau permettent à l&#39;administrateur de parcours d&#39;écrire, de lire et de supprimer des parcours.

## Fonction de parcours {#journey-capability}

### Autorisation Gérer les parcours {#manage-journeys}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les parcours]** permet aux utilisateurs de créer des parcours et de modifier/supprimer des parcours existants, ainsi que d&#39;accéder aux objets utilisés dans la zone de travail de parcours pour concevoir le flux du parcours.

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

### Autorisation Publier les parcours {#publish-journeys}

L&#39;autorisation de haut niveau **[!UICONTROL Publier les parcours]** permet aux utilisateurs de publier des parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys.publish
   * journeys.read

### Autorisation Afficher les parcours {#view-journeys}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les parcours]** permet aux utilisateurs de parcourir et d&#39;afficher les parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * journeys.read

* Spécifiques à Adobe Experience Platform :
   * segments.read
   * profiles.read

### Autorisation Gérer les événements de parcours, les sources de données et les actions {#manage-journeys-events}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les événements de parcours, les sources de données et les actions]** permet aux utilisateurs de configurer les configurations d&#39;événement et de données.

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

### Autorisation Afficher les événements de parcours, les sources de données et les actions {#view-journeys-event}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les événements de parcours, les sources de données et les actions]** permet aux utilisateurs d&#39;utiliser l&#39;événement et les données dans le flux du parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * parcours_events.read
   * parcours_data_sources.read
   * parcours_actions.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Autorisation Afficher le rapport de parcours {#view-journeys-report}

L&#39;autorisation de niveau supérieur **[!UICONTROL Afficher le rapport de parcours]** permet aux utilisateurs de consulter un rapport de parcours en lecture seule.

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

### Autorisation Gérer les messages {#manage-messages}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les messages]** permet aux utilisateurs de créer et modifier/supprimer des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Spécifiques à Adobe Experience Platform :
   * segments.read
   * schemas.read

### Autorisation Gérer l&#39;aperçu et le test des messages {#mange-messages-preview}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer l&#39;aperçu et le test des messages]** permet aux utilisateurs de prévisualiser un message personnalisé.

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

### Autorisation Publier les messages {#publish-messages}

L&#39;autorisation de haut niveau **[!UICONTROL Publier les messages]** permet aux utilisateurs de publier des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.publish

* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * schemas.read
   * datasets.read

### Autorisation Afficher les messages {#view-messages}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les messages]** permet aux utilisateurs de lire uniquement les messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages.read
   * messages_presets.read

* Spécifiques à Adobe Experience Platform :
   * schemas.read
   * segments.read

### Autorisation Afficher le rapport des messages {#view-message-reports}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher le rapport des messages]** permet aux utilisateurs d&#39;afficher en lecture seule un rapport sur les e-mails et les notifications push.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Fonction de gestion des décisions {#decisions-permissions}

### Autorisation Gérer les décisions {#manage-decisioning}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les décisions]** permet aux utilisateurs de créer des rapports et de modifier/supprimer des **[!UICONTROL entités d&#39;activité]** existantes, ainsi que de gérer les objets utilisés dans ces activités pour prendre des décisions.

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

### Autorisation Afficher les décisions {#view-decisions}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les décisions]** permet aux utilisateurs d&#39;utiliser une activité existante et les objets métier associés pour prendre des décisions.

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

### Autorisation Publier la prise de décision des offres {#publish-decisions}

L&#39;autorisation de haut niveau **[!UICONTROL Publier la prise de décision des offres]** permet aux utilisateurs d&#39;obtenir un accès pour approuver/annuler l&#39;approbation des activités d&#39;offre.

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

### Autorisation Gérer les stratégies de classement {#manage-decisions}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les stratégies de classement]** permet aux utilisateurs de lire, de créer, de modifier et de supprimer un rapport de messages personnalisé et d&#39;utiliser des fonctionnalités d&#39;action.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à la gestion des décisions :
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Fonction d&#39;administration {#administration-permissions}

### Autorisation Gérer la délégation des sous-domaines {#manage-subdomain}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer la délégation des sous-domaines]** permet aux utilisateurs de créer, de modifier et de supprimer la délégation des sous-domaines (y compris le pool d&#39;adresses IP).

Elle comprend les autorisations de bas niveau suivantes :

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### Autorisation Afficher les enregistrements PTR {#view-ptr}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les enregistrements PTR]** permet aux utilisateurs d&#39;afficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine.

Elle comprend les autorisations de bas niveau suivantes :

* PTR_records.read
* subdomains_delegation.read

### Autorisation Gérer les pools d&#39;adresses IP {#manage-ip-pools}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les pools d&#39;adresses IP]** permet aux utilisateurs de créer, de modifier et de supprimer la définition des affinités.

Elle comprend les autorisations de bas niveau suivantes :

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Autorisation Gérer les paramètres généraux des messages {#manage-message-settings}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les paramètres généraux des messages]** permet aux utilisateurs de créer,de  modifier et de supprimer des paramètres globaux au niveau de l&#39;environnement sandbox.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Spécifiques à Adobe Experience Platform :
   * schemas.read

### Autorisation Afficher les paramètres généraux des messages {#view-message-settings}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les paramètres généraux des messages]** permet aux utilisateurs d&#39;afficher les paramètres généraux des messages, tels que l&#39;adresse d&#39;exécution.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_general_settings.read
* Spécifiques à Adobe Experience Platform :
   * schemas.read

### Autorisation Gérer les préréglages de message {#manage-message-presets}

L&#39;autorisation de haut niveau **[!UICONTROL Gérer les préréglages de message]** permet aux utilisateurs de créer, de modifier et de supprimer des préréglages de message sur les canaux au niveau de l&#39;environnement sandbox.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

### Autorisation Afficher les préréglages de message {#view-message-presets}

L&#39;autorisation de haut niveau **[!UICONTROL Afficher les préréglages de message]** permet aux utilisateurs d&#39;afficher les préréglages de message afin de savoir quels préréglages de message utiliser lors de la création d&#39;un message.

Elle comprend les autorisations de bas niveau suivantes :

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (à partir d&#39;Adobe Experience Platform Launch)

### Autorisation Gérer la suppression {#manage-suppression}

L’autorisation de haut niveau **[!UICONTROL Gérer la suppression]** permet aux utilisateurs de définir le nombre de bounces avant l’ajout d’une adresse e-mail à la liste de suppression, ainsi que d’ajouter et de supprimer des entrées dans la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Autorisation Afficher la liste de suppression {#view-suppresion-list}

L’autorisation de haut niveau **[!UICONTROL Afficher la liste de suppression]** permet aux utilisateurs d’afficher le contenu et les paramètres de la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * suppression_list.view
* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### Autorisation Exporter la liste de suppression {#export-suppression-list}

L’autorisation de haut niveau **[!UICONTROL Exporter la liste de suppression]** permet aux utilisateurs de télécharger la liste de suppression sous forme de fichier CSV.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifiques à Journey Optimizer :
   * suppression_list.export
* Spécifiques à Adobe Experience Platform :
   * profiles.read
   * datasets.read
