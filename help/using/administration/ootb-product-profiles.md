---
solution: Journey Optimizer
product: journey optimizer
title: Rôles intégrés à Journey Optimizer
description: En savoir plus sur les rôles intégrés
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: autorisations, création, messages
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 92ecaffe6e16ff4f3ac2221e3d69dfbb23d930b4
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 72%

---

# Rôles intégrés {#ootb-product-profiles}

## [!DNL Campaign Administrator] {#campaign-administrator}

Le **[!DNL Campaign Administrator]** Le rôle permet aux menus d’administration de gérer et de publier les campagnes et la gestion des décisions.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations| |-|-| |Campagnes| <ul><li> **[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez les campagnes.</li><li>**[!DNL View campaigns report]** : lisez et modifiez le rapport des campagnes.</li></ul>| |Configurations de canal|<ul><li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li><li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li><li>**[!DNL View PTR records]** : accès en lecture seule aux enregistrements PTR.</li><li> **[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li><li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li><li>**[!DNL Manage suppression rules]** : accès à la lecture, la création, la modification et la suppression des règles de suppression.</li><li>**[!DNL Export suppression list]** : accédez à la liste de suppression des exportations au format CSV.</li><li>**[!DNL View suppression list]** : la lecture et lʼexportation de la liste de suppression locale.</li><li>**[!DNL Manage alerts]** : activez/désactivez les alertes pour les campagnes, les messages et les droits.</li><li>**[!DNL Manage landing page settings]** : lisez, créez, modifiez et la supprimez les paramètres de la page de destination.</li><li>**[!DNL Manage SMS settings]** : lisez, créez, modifiez et supprimez des paramètres des SMS.</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]** : octroi de lʼaccès aux sandbox.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

Le **[!DNL Campaign Approver]** permet aux utilisateurs d’approuver des diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec les rapports **[!DNL Campaigns]**.

| Ressources | Autorisations| |-|-| |Campagnes| <ul><li>**[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez des campagnes.</li><li>**[!DNL View Campaigns report]** : la lecture et la modification des rapports de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>| |Configurations de canal| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

Le **[!DNL Campaign Manager]** rôle permet aux utilisateurs de créer et de modifier **[!UICONTROL Campagnes]** et chaque fonctionnalité liée à **[!UICONTROL Campagnes]** mais ne pourront pas les publier.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations| |-|-| |Campagnes| <ul><li>**[!DNL Manage campaigns]** : lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL View campaigns report]** : la lecture et la modification du rapport de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>| |Configurations de canal| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

Le **[!DNL Campaign Viewer]** permet d’accéder en lecture seule à la fonction **[!UICONTROL Campagnes]** et **[!UICONTROL Gestion des décisions]** fonctionnalités.

Les utilisateurs affectés à ce rôle ne pourront pas modifier ni publier.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations| |-|-| |Campagnes| <ul><li>**[!DNL View campaigns]** : accès en lecture seule aux campagnes.</li><li>**[!DNL View campaigns report]** : accès en lecture seule aux rapports de campagne.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

Le **[!DNL Journey Administrator]** Le rôle permet aux menus d’administration de gérer et de publier des Parcours et la gestion des décisions.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations| |-|-| |Parcours| <ul><li> **[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL Publish journeys]** : la publication des parcours.</li><li>**[!DNL Manage journeys events, data sources and actions]** : la lecture, la création, la modification et la suppression des événements, des sources ou des actions.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul>| |Configurations de canal|<ul><li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li><li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li><li>**[!DNL View PTR records]** : accès en lecture seule aux enregistrements PTR.</li><li>**[!DNL Manage channel surfaces]** : la lecture, la création, la modification et la suppression du branding de contenu.</li><li>**[!DNL Manage Landing page settings]** : créer, modifier et supprimer des sous-domaines de page de destination et des paramètres prédéfinis de page de destination.</li><li> **[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li><li>**[!DNL Manage SMS settings]** : créer, modifier et supprimer les informations d’identification d’API et les surfaces de canal SMS requises pour activer le canal SMS.</li><li>**[!DNL Manage suppression rules]** : accès à la lecture, la création, la modification et la suppression des règles de suppression.</li><li>**[!DNL View suppression list]** : la lecture et lʼexportation de la liste de suppression locale.</li><li>**[!DNL Manage alerts]** : lʼactivation/la désactivation des alertes pour les parcours et les droits.</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]** : octroi de lʼaccès aux sandbox.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>|
|Bibliothèque Journey Optimizer|<ul><li>**[!DNL Manage Library Items]** : ajoutez et supprimez des expressions enregistrées dans la bibliothèque [!DNL Journey Optimizer].</li></ul>|
|Gouvernance des données|<ul><li>**[!DNL Manage usage label]** : lire, créer et supprimer des libellés d’utilisation.</li><li>**[!DNL Manage data usage policies]** : lire, créer, modifier et supprimer des politiques dʼutilisation des données.</li><li>**[!DNL View data usage policies]** : accéder en lecture seule aux politiques d’utilisation des données.</li><li>**[!DNL View user activity log]** : lire et exporter les journaux d’audit.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Le **[!DNL Journey Approver]** permet aux utilisateurs d’approuver des diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec les rapports **[!DNL Journey]**.

Ce rôle inclut les autorisations suivantes :

| Ressources| Autorisations| |-|-| |Parcours| <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL Publish journey]** : la publication des parcours.</li><li>**[!DNL View journeys events, data sources and actions]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification des rapports de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>| |Configurations de canal| <ul><li>**[!DNL View channel surfaces]** : accès en lecture seule aux surfaces des canaux.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Le **[!DNL Journey Manager]** rôle permet aux utilisateurs de créer et de modifier **[!UICONTROL Parcours]** et chaque fonctionnalité liée à **[!UICONTROL Parcours]** mais ne pourront pas les publier.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations| |-|-| |Parcours| <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL View journeys events]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>| |Configurations de canal| <ul><li>**[!DNL View channel surfaces]** : accès en lecture seule aux surfaces des canaux.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

Le **[!DNL Journey viewer]** permet d’accéder en lecture seule à la fonction **[!UICONTROL Parcours]** et **[!UICONTROL Gestion des décisions]** fonctionnalités.

Les utilisateurs affectés à ce rôle ne pourront pas modifier ni publier.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations| |-|-| |Parcours| <ul><li>**[!DNL View journeys]** : accès en lecture seule aux parcours.</li><li>**[!DNL View journeys event, data sources, actions]** : accès en lecture seule aux événements de parcours et aux sources de données.</li><li>**[!DNL View journeys report]** : accès en lecture seule aux rapports de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Le **[!DNL Decisioning manager]** uniquement permet d’accéder à la fonction **[!UICONTROL Gestion des décisions]** . Les utilisateurs affectés à ce rôle pourront uniquement gérer, afficher et publier les décisions.

Ce rôle inclut les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li><li>**[!DNL Publish decisions]** : lʼactivation ou la désactivation des activités de prise de décision.</li></ul>|

## [!DNL Content Library Manager] {#content-library-manager}

Le **[!DNL Content Library Manager]** uniquement permet d’accéder à la fonction **[!UICONTROL Modèles de contenu]** . Les utilisateurs affectés à ce rôle ne pourront accéder à la bibliothèque de modèles que pour créer du contenu sans accéder aux parcours ou aux campagnes.

Ce rôle inclut les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Bibliothèque Journey Optimizer| <ul><li>**[!DNL Manage library items]** : lire, créer, modifier et supprimer des éléments de la bibliothèque Journey Optimizer.</li><li>**[!DNL Manage simulate content]** : accéder à l’option **[!UICONTROL Simuler du contenu]** pour l’aperçu et le BAT.</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des politiques de fusion.</li></ul>|
