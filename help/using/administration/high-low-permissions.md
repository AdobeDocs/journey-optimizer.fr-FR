---
title: Niveaux d’autorisation
description: En savoir plus sur les autorisations générales et de bas niveau
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
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Populations témoins
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Niveaux d’autorisation {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Chaque profil de produit est constitué d’autorisations permettant aux utilisateurs d’accéder aux différentes fonctionnalités.
Elles peuvent être divisées en deux types :

* **Autorisation** de haut niveau : représente les différentes autorisations qui peuvent être affectées au  **[!UICONTROL profil de]** produit dans  [!DNL Admin console], telles que  **[!UICONTROL Publier les]** parcours et  **[!UICONTROL Gérer la délégation des sous-domaines]**. Les autorisations de haut niveau englobent les autorisations de bas niveau.

* **Autorisation** de bas niveau : représente les différentes autorisations qui proviennent de l’autorisation de niveau supérieur.

Par exemple, le profil de produit **[!UICONTROL Administrateur de Parcours]** se voit attribuer l’autorisation **[!UICONTROL Gérer les parcours]**. À partir de cette autorisation, les autorisations de bas niveau permettent à l’administrateur de Parcours d’écrire, de lire et de supprimer des parcours.

## Fonction parcours {#journey-capability}

### Autorisation Gérer les parcours {#manage-journeys}

L’autorisation de haut niveau **[!UICONTROL Gérer les parcours]** permet aux utilisateurs de créer et de modifier/supprimer des Parcours existants, ainsi que d’accéder aux objets utilisés dans le canevas de parcours pour créer le flux de parcours.

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

### Autorisation de publication des parcours {#publish-journeys}

L’autorisation de haut niveau **[!UICONTROL Publier les parcours]** permet aux utilisateurs de publier des parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys.publish
   * journeys.read

### Autorisation d’affichage des parcours {#view-journeys}

L’autorisation de haut niveau **[!UICONTROL Afficher les parcours]** permet aux utilisateurs de parcourir et d’afficher les parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * journeys.read

* Spécifique à Adobe Experience Platform :
   * segments.read
   * profiles.read

### Gérer les événements parcours, les sources de données et les autorisations d’actions {#manage-journeys-events}

L’autorisation de haut niveau **[!UICONTROL Gérer les événements de parcours, les sources de données et les actions]** permet aux utilisateurs de configurer les configurations d’événement et de données.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * parcours_events.read
   * parcours_events.write
   * parcours_events.delete
   * parcours_data_sources.read
   * parcours_data_sources.write
   * parcours_data_sources.delete
   * parcours_actions.read
   * parcours_actions.write
   * parcours_actions.delete
* Spécifique à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Affichage des événements de parcours, des sources de données et des autorisations d’actions {#view-journeys-event}

L’autorisation de haut niveau **[!UICONTROL Afficher les événements de parcours, les sources de données et les actions]** permet aux utilisateurs d’utiliser l’événement et les données dans le flux de parcours.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * parcours_events.read
   * parcours_data_sources.read
   * parcours_actions.read

* Spécifique à Adobe Experience Platform :
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Autorisation d’affichage des rapports de parcours {#view-journeys-report}

L’autorisation de niveau supérieur **[!UICONTROL Afficher les parcours permet aux utilisateurs de consulter un rapport de parcours en lecture seule.]**

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * parcours_report.read
   * messages_report.read

* Spécifique à Adobe Experience Platform :
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Fonction des messages {#message-capability}

### Autorisation de gestion des messages {#manage-messages}

L’autorisation de haut niveau **[!UICONTROL Gérer les messages]** permet aux utilisateurs de créer et modifier/supprimer des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Spécifique à Adobe Experience Platform :
   * segments.read
   * schemas.read

### Gérer l’aperçu des messages et l’autorisation de test {#mange-messages-preview}

L’autorisation de haut niveau **[!UICONTROL Gérer l’aperçu et le test des messages]** permet aux utilisateurs de prévisualiser un message personnalisé.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Spécifique à Adobe Experience Platform :
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### Autorisation de publication des messages {#publish-messages}

L’autorisation de haut niveau **[!UICONTROL Publier les messages]** permet aux utilisateurs de publier des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages.publish

* Spécifique à Adobe Experience Platform :
   * profiles.read
   * schemas.read
   * datasets.read

### Autorisation d’affichage des messages {#view-messages}

L’autorisation de haut niveau **[!UICONTROL Afficher les messages]** permet aux utilisateurs de lire uniquement les messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages.read
   * messages_presets.read

* Spécifique à Adobe Experience Platform :
   * schemas.read
   * segments.read

### Afficher l’autorisation du rapport des messages {#view-message-reports}

L’autorisation de haut niveau **[!UICONTROL Afficher les messages permet aux utilisateurs d’envoyer des messages électroniques et des rapports push en lecture seule.]**

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Fonctionnalité de gestion des décisions {#decisions-permissions}

### Autorisation de gestion des décisions {#manage-decisioning}

L’autorisation de haut niveau **[!UICONTROL Gérer les décisions]** permet aux utilisateurs de créer et de modifier/supprimer des **[!UICONTROL entités d’activité]** existantes, ainsi que de gérer les objets utilisés dans ces activités pour prendre les décisions.

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

### Autorisation d’affichage des décisions {#view-decisions}

L’autorisation de haut niveau **[!UICONTROL Afficher les décisions]** permet aux utilisateurs d’utiliser une activité existante et les objets commerciaux associés pour prendre les décisions.

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

### Publier l’autorisation de prise de décision des offres {#publish-decisions}

L’autorisation de haut niveau **[!UICONTROL Publier les offres permet aux utilisateurs d’accéder à l’approbation/l’annulation de l’approbation des activités d’offre.]**

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

### Gérer l’autorisation des stratégies de classement {#manage-decisions}

L’autorisation de haut niveau **[!UICONTROL Gérer les stratégies de classement]** permet aux utilisateurs de lire, créer, modifier et supprimer un rapport de messages personnalisés et d’utiliser des fonctionnalités d’action.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à la gestion des décisions :
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Fonctionnalité d’administration {#administration-permissions}

### Gérer l’autorisation de délégation des sous-domaines {#manage-subdomain}

L’autorisation de haut niveau **[!UICONTROL Gérer la délégation des sous-domaines]** permet aux utilisateurs de créer, modifier et supprimer la délégation des sous-domaines (y compris le pool d’adresses IP).

Elle comprend les autorisations de bas niveau suivantes :

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### Afficher l’autorisation des enregistrements PTR {#view-ptr}

L’autorisation de haut niveau **[!UICONTROL Afficher les enregistrements PTR]** permet aux utilisateurs d’afficher les enregistrements PTR qui ont été configurés en fonction du sous-domaine et inclut les autorisations de bas niveau suivantes :

* PTR_records.read
* subdomains_delegation.read

### Gérer l’autorisation des pools d’adresses IP {#manage-ip-pools}

L’autorisation de haut niveau **[!UICONTROL Gérer les pools d’adresses IP]** permet aux utilisateurs de créer, modifier et supprimer la définition des affinités.

Elle comprend les autorisations de bas niveau suivantes :

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Autorisation de gestion des paramètres généraux des messages {#manage-message-settings}

L’autorisation de haut niveau **[!UICONTROL Gérer les paramètres généraux des messages]** permet aux utilisateurs de créer, modifier et supprimer des paramètres globaux au niveau de l’environnement de test.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* Spécifique à Adobe Experience Platform :
   * schemas.read

### Autorisation d’affichage des paramètres généraux des messages {#view-message-settings}

L’autorisation de haut niveau **[!UICONTROL Afficher les paramètres généraux des messages]** permet aux utilisateurs d’afficher les paramètres généraux des messages, tels que les règles de suppression ou l’adresse d’exécution.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages_general_settings.read
* Spécifique à Adobe Experience Platform :
   * schemas.read

### Autorisation de gestion des messages prédéfinis {#manage-message-presets}

L’autorisation de haut niveau **[!UICONTROL Gérer les paramètres prédéfinis de message]** permet aux utilisateurs de créer, modifier et supprimer des paramètres prédéfinis de message sur les canaux au niveau de l’environnement de test.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (à partir d’Adobe Experience Platform Launch)

### Autorisation d’affichage des messages prédéfinis {#view-message-presets}

L’autorisation de haut niveau **[!UICONTROL Afficher les paramètres prédéfinis de message]** permet aux utilisateurs d’afficher les paramètres prédéfinis de message afin de savoir quels paramètres prédéfinis de message utiliser lors de la création d’un message.

Elle comprend les autorisations de bas niveau suivantes :

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (à partir d’Adobe Experience Platform Launch)

### Gérer l’autorisation des règles de suppression {#manage-suppression-rules}

L’autorisation de haut niveau **[!UICONTROL Gérer les règles de suppression]** permet aux utilisateurs de définir le nombre de rebonds avant l’ajout de l’adresse électronique de l’utilisateur à la liste de suppression.

Elle comprend les autorisations de bas niveau suivantes :

* delete_rules.read
* delete_rules.write
* delete_rules.delete

### Autorisation d’affichage de liste de suppression {#view-suppresion-list}

L’autorisation de haut niveau **[!UICONTROL Afficher la liste de suppression]** permet aux utilisateurs d’afficher les configurations des messages, y compris les paramètres prédéfinis des messages et les paramètres généraux des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Journey Optimizer :
   * delete_list.view
* Spécifique à Adobe Experience Platform :
   * profiles.read
   * datasets.read

### Exporter l’autorisation de liste de suppression {#export-suppression-list}

L’autorisation de haut niveau **[!UICONTROL Exporter la liste de suppression]** permet aux utilisateurs de configurer les configurations des messages, y compris les paramètres prédéfinis des messages et les paramètres généraux des messages.

Elle comprend les autorisations de bas niveau suivantes :

* Spécifique à Adobe Experience Platform :
   * profiles.read
   * datasets.read
