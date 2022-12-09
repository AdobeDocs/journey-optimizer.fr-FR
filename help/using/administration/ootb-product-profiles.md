---
solution: Journey Optimizer
product: journey optimizer
title: Profils de produit intégrés
description: En savoir plus sur les profils de produit intégrés
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Profils de produit intégrés {#ootb-product-profiles}


## A propos des permissions liées aux messages{#message-permissions}

Adobe Journey Optimizer a publié de nouvelles fonctionnalités de création intégrées qui vous permettent de créer et de créer vos messages directement à partir d’un parcours ou d’une campagne.

Cette fonctionnalité aura un impact sur les autorisations comme suit :

| Nom de l’autorisation | Sera inclus dans |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Après le 25 juillet**, autorisations liées à **Messages** sont toujours disponibles, car les messages sont toujours accessibles pour activer la transition et vous pouvez les enregistrer en tant que modèle.

**À partir du 6 septembre**, autorisations liées à **Messages** sera supprimé et les messages ne seront plus accessibles.

>[!WARNING]
>
>Si des utilisateurs sont affectés à la variable **[!DNL Message Manager]** profil de produit uniquement, sans **[!DNL Journey manager]** profil de produit, vous devez lui attribuer un nouveau profil de produit pour pouvoir continuer à modifier le contenu.


## [!DNL Campaign Administrator] {#campaign-administrator}

Le **[!DNL Campaign Administrator]** Le profil de produit permet aux menus d’administration de gérer et de publier les campagnes et la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Campagnes| <ul><li> **[!DNL Manage campaigns]**: lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL Publish campaigns]**: publier des campagnes.</li><li>**[!DNL View campaigns report]**: lire et modifier le rapport campagnes.</li></ul>| |Administration|<ul><li>**[!DNL Manage subdomains delegation]**: lire, créer, modifier et supprimer la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]**: lire, créer, modifier et supprimer le pool ip.</li><li>**[!DNL Manage PTR records]**: lire et modifier des enregistrements PTR.</li><li>**[!DNL View PTR records]**: accès en lecture seule aux enregistrements PTR.</li><li> **[!DNL Manage messages general settings]**: lire, créer, modifier et supprimer les paramètres généraux des messages.</li><li>**[!DNL Manage messages presets]**: lire, créer, modifier et supprimer l’identité graphique du contenu.</li><li>**[!DNL Manage suppression rules]**: accéder aux règles de suppression de lecture, création, modification et suppression ;</li><li>**[!DNL Export suppression list]**: accès à la liste de suppression des exportations au format CSV.</li><li>**[!DNL View suppression list]**: lire et exporter la liste de suppression locale.</li><li>**[!DNL Manage alerts]**: activer/désactiver des alertes pour les campagnes, les messages et les droits ;</li><li>**[!DNL Manage landing page settings]**: lire, créer, modifier et supprimer les paramètres de la landing page.</li><li>**[!DNL Manage SMS settings]**: lire, créer, modifier et supprimer les paramètres SMS.</li></ul>| |Gestion des décisions|<ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des décisions.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des stratégies de classement.</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Accordez l’accès aux environnements de test.</li><li>**[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]**: accès en lecture seule à l’espace de noms d’identité.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

Le **[!DNL Campaign Approver]** le profil de produit permet aux utilisateurs d’approuver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec la variable **[!DNL Campaigns]** rapports.

| Fonctionnalité | Autorisations| |-|-| |Campagnes| <ul><li>**[!DNL Manage campaigns]**: lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL Publish campaigns]**: publier des campagnes.</li><li>**[!DNL View Campaigns report]**: lire, modifier des rapports de parcours.</li></ul>| |Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

Le **[!DNL Campaign Manager]** le profil de produit permet aux utilisateurs de créer et de modifier des **[!UICONTROL Campaigns]** et chaque fonctionnalité liée à **[!UICONTROL Campaigns]** mais ne pourront pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Campagnes| <ul><li>**[!DNL Manage campaigns]**: lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL View campaigns report]**: lire, modifier le rapport de parcours.</li></ul>| |Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

Le **[!DNL Campaign Viewer]** le profil de produit permet d’accéder en lecture seule à la variable **[!UICONTROL Campaigns]** et **[!UICONTROL Decision management]** fonctionnalités.

Les utilisateurs affectés à ce profil de produit ne pourront pas modifier ni publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Campagnes| <ul><li>**[!DNL View campaigns]**: accès en lecture seule aux campagnes.</li><li>**[!DNL View campaigns report]**: accès en lecture seule aux rapports des campagnes.</li></ul>| |Gestion des décisions| <ul><li>**[!DNL View decisions]**: accès en lecture seule aux entités de décision.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

Le **[!DNL Journey Administrator]** Le profil de produit permet aux menus d’administration de gérer et de publier les parcours et la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Parcours| <ul><li> **[!DNL Manage journeys]**: lire, créer, modifier et supprimer des parcours.</li><li>**[!DNL Publish journeys]**: publier les parcours.</li><li>**[!DNL Manage journeys events, data sources and actions]**: lire, créer, modifier et supprimer des événements, des sources ou des actions.</li><li>**[!DNL View journeys report]**: lire et modifier le rapport parcours.</li></ul>| |Administration|<ul><li>**[!DNL Manage subdomains delegation]**: lire, créer, modifier et supprimer la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]**: lire, créer, modifier et supprimer le pool ip.</li><li>**[!DNL Manage PTR records]**: lire et modifier des enregistrements PTR.</li><li>**[!DNL View PTR records]**: accès en lecture seule aux enregistrements PTR.</li><li>**[!DNL Manage channel surfaces]**: lire, créer, modifier et supprimer l’identité graphique du contenu.</li><li>**[!DNL Manage Landing page settings]**: créer, modifier et supprimer des sous-domaines de landing page et des paramètres prédéfinis de landing page.</li><li> **[!DNL Manage messages general settings]**: lire, créer, modifier et supprimer les paramètres généraux des messages.</li><li>**[!DNL Manage SMS settings]**: créer, modifier et supprimer les informations d’identification d’API et les surfaces de canal SMS requises pour activer le canal SMS.</li><li>**[!DNL Manage suppression rules]**: accéder aux règles de suppression de lecture, création, modification et suppression ;</li><li>**[!DNL View suppression list]**: lire et exporter la liste de suppression locale.</li><li>**[!DNL Manage alerts]**: activer/désactiver des alertes pour les parcours et les droits ;</li></ul>| |Gestion des décisions|<ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des décisions.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des stratégies de classement.</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Accordez l’accès aux environnements de test.</li><li>**[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]**: accès en lecture seule à l’espace de noms d’identité.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Bibliothèque Journey Optimizer|<ul><li>**[!DNL Manage Library Items]**: ajouter et supprimer des expressions enregistrées dans [!DNL Journey Optimizer] Bibliothèque.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Le **[!DNL Journey Approver]** le profil de produit permet aux utilisateurs d’approuver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec la variable **[!DNL Journey]** rapports.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Parcours| <ul><li>**[!DNL Manage journeys]**: lire, créer, modifier et supprimer des parcours.</li><li>**[!DNL Publish journey]**: publier les parcours.</li><li>**[!DNL View journeys events, data sources and actions]**: accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]**: lire, modifier des rapports de parcours.</li></ul>| |Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports personnalisés et utiliser des fonctions d’action.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: accès en lecture seule aux surfaces des canaux.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Le **[!DNL Journey Manager]** le profil de produit permet aux utilisateurs de créer et de modifier des **[!UICONTROL Journeys]** et chaque fonctionnalité liée à **[!UICONTROL Journeys]** mais ne pourront pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Parcours| <ul><li>**[!DNL Manage journeys]**: lire, créer, modifier et supprimer des parcours.</li><li>**[!DNL View journeys events]**: accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]**: lire, modifier le rapport de parcours.</li></ul>| |Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports personnalisés et utiliser des fonctions d’action.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: lire, créer, modifier et supprimer des segments.</li><li>**[!DNL Manage profiles]**: lire, créer, modifier et supprimer des profils.</li><li>**[!DNL Read datasets]**: accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]**: accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]**: lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: accès en lecture seule aux surfaces des canaux.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

Le **[!DNL Journey viewer]** le profil de produit permet d’accéder en lecture seule à la variable **[!UICONTROL Journeys]** et **[!UICONTROL Decision management]** fonctionnalités.

Les utilisateurs affectés à ce profil de produit ne pourront pas modifier ni publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Parcours| <ul><li>**[!DNL View journeys]**: accès en lecture seule aux parcours.</li><li>**[!DNL View journeys event, data sources, actions]**: accès en lecture seule aux événements de parcours et aux sources de données.</li><li>**[!DNL View journeys report]**: accès en lecture seule aux rapports de parcours.</li></ul>| |Gestion des décisions| <ul><li>**[!DNL View decisions]**: accès en lecture seule aux entités de décision.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Le **[!DNL Decisioning manager]** le profil de produit autorise uniquement la variable **[!UICONTROL Decision management]** . Les utilisateurs affectés à ce profil de produit ne pourront gérer, afficher et publier que les décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations| |-|-| |Gestion des décisions| <ul><li>**[!DNL Manage decisions]**: lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**[!DNL View decisions]**: accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des rapports personnalisés et utiliser des fonctions d’action.</li><li>**[!DNL Publish decisions]**: activer ou désactiver les activités de prise de décision.</li></ul>|
