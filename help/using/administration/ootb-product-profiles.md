---
title: Profils de produit natifs
description: En savoir plus sur les profils de produit intégrés
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: e5aa7fbce348c9da00b3f5c8624237c76128a61b
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 18%

---

# Profils de produit natifs {#ootb-product-profiles}

## [!DNL Journey Administrator] {#journey-administrator}

Le **[!DNL Journey Administrator]** Le profil de produit permet aux menus d’administration de gérer et de publier des Parcours, des messages et de la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li> **[!DNL Manage journeys]**: lecture, création, modification et suppression de parcours.</li><li>**[!DNL Publish journeys]**: publier des parcours.</li><li>**[!DNL Manage journeys events, data sources and actions]**: lire, créer, modifier et supprimer des événements, des sources ou des actions.</li><li>**[!DNL View journeys report]**: lire et modifier le rapport parcours.</li></ul>|
|Messages|<ul><li> **[!DNL Manage messages]**: lire, créer, modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**[!DNL Manage messages preview and test]**: publier des messages.</li><li>**[!DNL Publish messages]**: lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**[!DNL View messages report]**: rapport lire et modifier les messages .</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: lire, créer, modifier et supprimer la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]**: lire, créer, modifier et supprimer le pool ip.</li><li>**[!DNL Manage PTR records]**: lire et modifier des enregistrements PTR.</li><li>**[!DNL View PTR records]**: accès en lecture seule aux enregistrements PTR.</li><li> **[!DNL Manage messages general settings]**: lire, créer, modifier et supprimer les paramètres généraux des messages.</li><li>**[!DNL Manage messages presets]**: lire, créer, modifier et supprimer l’identité graphique du contenu.</li><li>**[!DNL Manage suppression rules]**: accéder aux règles de suppression de lecture, création, modification et suppression ;</li><li>**[!DNL View suppression list]**: lire et exporter la liste de suppression locale.</li><li>**[!DNL Manage alerts]**: activer/désactiver des alertes pour les parcours, les messages et les droits ;</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des décisions.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Accordez l’accès aux environnements de test.</li><li>**[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]**: accès en lecture seule à l’espace de noms d’identité.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Le **[!DNL Journey Approver]** le profil de produit permet aux utilisateurs d’approuver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec la variable **[!DNL Message]** et **[!DNL Journey]** rapports.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL Manage journeys]**: lecture, création, modification et suppression de parcours.</li><li>**[!DNL Publish journey]**: publier des parcours.</li><li>**[!DNL View journeys events, data sources and actions]**: accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]**: lire, modifier des rapports de parcours.</li></ul>| |Messages| <ul><li>**[!DNL Manage messages]**: lire, créer, modifier et supprimer des messages.</li><li>**[!DNL Publish messages]** publier des messages.</li><li>**[!DNL Manage messages preview and test]**: lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**[!DNL View messages report]**: lire, créer, modifier et supprimer le rapport des messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Le **[!DNL Journey Manager]** le profil de produit permet aux utilisateurs de créer et de modifier des **[!UICONTROL Parcours]** et chaque fonctionnalité liée à **[!UICONTROL Parcours]** mais ne pourront pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL Manage journeys]**: lecture, création, modification et suppression de parcours.</li><li>**[!DNL View journeys events]**: accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]**: lire, modifier le rapport parcours.</li></ul>| |Messages| <ul><li>**[!DNL Manage messages]**: lire, créer, modifier et supprimer des messages.</li><li> **[!DNL Manage messages preview and test]**: lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**[!DNL View messages report]**: lire, créer, modifier et supprimer le rapport des messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## [!DNL Journey viewer] {#journey-viewer}

Le **[!DNL Journey viewer]** le profil de produit permet d’accéder en lecture seule à la variable **[!UICONTROL Parcours]**, **[!UICONTROL Objectifs]**, **[!UICONTROL Messages]** et **[!UICONTROL Gestion des décisions]** fonctionnalités.

Les utilisateurs affectés à ce profil de produit ne pourront effectuer ni modification, ni publication.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL View journeys]**: accès en lecture seule à parcours.</li><li>**[!DNL View journeys event, data sources, actions]**: accès en lecture seule aux événements parcours et aux sources de données.</li><li>**[!DNL View journeys report]**: accès en lecture seule aux rapports parcours.</li></ul>| |Messages| <ul><li>**[!DNL View messages]**: accès en lecture seule aux messages.</li><li>**[!DNL View messages report]**: accès en lecture seule aux rapports sur les messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL View decisions]**: accès en lecture seule aux entités de décision.</li></ul>|

## [!DNL Message Manager] {#message-manager}

Le **[!DNL Message Manager]** le profil de produit permet aux utilisateurs de créer et de modifier des **[!UICONTROL Messages]** et **[!UICONTROL Gestion des décisions]** mais ne pourront pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL View journeys]**: accès en lecture seule à parcours.</li><li>**[!DNL View Journeys events, data sources and actions]**: accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li></ul>| |Messages| <ul><li>**[!DNL Manage messages]**: lire, créer, modifier et supprimer des messages.</li><li>**[!DNL Manage messages preview and test]**: lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li> **[!DNL View messages report]**: lire, créer, modifier et supprimer des rapports de messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Read profiles]**: accès en lecture seule au profil pour la prévisualisation et le test.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Le **[!DNL Decisioning manager]** le profil de produit autorise uniquement la variable **[!UICONTROL Gestion des décisions]** . Les utilisateurs affectés à ce profil de produit ne pourront gérer, afficher et publier que les décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL View decisions]**: accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li><li>**[!DNL Publish decisions]**: activer ou désactiver les activités de prise de décision.</li></ul>|
