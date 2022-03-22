---
title: Profils de produit intégrés
description: En savoir plus sur les profils de produit intégrés
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: f5627a23ceb0d00dd01db8766e72fed1b5d652a3
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 97%

---

# Profils de produit intégrés {#ootb-product-profiles}

## [!DNL Journey Administrator] {#journey-administrator}

Le profil de produit **[!DNL Journey Administrator]** permet dʼavoir accès aux menus dʼadministration avec la possibilité de gérer et de publier des parcours, des messages et la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li> **[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL Publish journeys]** : la publication des parcours.</li><li>**[!DNL Manage journeys events, data sources and actions]** : la lecture, la création, la modification et la suppression des événements, des sources ou des actions.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul>|
|Messages|<ul><li> **[!DNL Manage messages]** : la lecture, la création et la modification de lʼaperçu du message et lʼenvoi du test/BAT.</li><li>**[!DNL Manage messages preview and test]** : la publication des messages.</li><li>**[!DNL Publish messages]** : la lecture, la création et la modification de lʼaperçu du message et lʼenvoi du test/BAT.</li><li>**[!DNL View messages report]** : la lecture et la modification du rapport de messages.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li><li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li><li>**[!DNL View PTR records]** : accès en lecture seule aux enregistrements PTR.</li><li> **[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li><li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li><li>**[!DNL Manage suppression rules]** : accès à la lecture, la création, la modification et la suppression des règles de suppression.</li><li>**[!DNL View suppression list]** : la lecture et lʼexportation de la liste de suppression locale.</li><li>**[!DNL Manage alerts]** : lʼactivation/la désactivation des alertes pour les parcours, les messages et les droits.</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]**: lire, créer, modifier et supprimer des stratégies de classement.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]** : octroi de lʼaccès aux environnements sandbox.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Bibliothèque Journey Optimizer|<ul><li>**[!DNL Manage Library Items]**: ajouter et supprimer des expressions enregistrées dans [!DNL Journey Optimizer] Bibliothèque.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Le profil de produit **[!DNL Journey Approver]** permet aux utilisateurs dʼapprouver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec les rapports **[!DNL Message]** et **[!DNL Journey]**.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL Publish journey]** : la publication des parcours.</li><li>**[!DNL View journeys events, data sources and actions]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification des rapports de parcours.</li></ul>| |Messages| <ul><li>**[!DNL Manage messages]** : la lecture, la création, la modification et la suppression des messages.</li><li>**[!DNL Publish messages]** : la publication des messages.</li><li>**[!DNL Manage messages preview and test]** : la lecture, la création et la modification de lʼaperçu du message et lʼenvoi du test/BAT.</li><li>**[!DNL View messages report]** : la lecture, la création, la modification et la suppression du rapport de messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Le profil de produit **[!DNL Journey Manager]** permet aux utilisateurs de créer et de modifier des **[!UICONTROL parcours]** ainsi que toutes les fonctionnalités liées aux **[!UICONTROL parcours]**. Cependant, ils ne pourront pas publier de parcours.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL View journeys events]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul>| |Messages| <ul><li>**[!DNL Manage messages]** : la lecture, la création, la modification et la suppression des messages.</li><li> **[!DNL Manage messages preview and test]** : la lecture, la création et la modification de lʼaperçu du message et lʼenvoi du test/BAT.</li><li>**[!DNL View messages report]** : la lecture, la création, la modification et la suppression du rapport de messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Journey viewer] {#journey-viewer}

Le profil de produit **[!DNL Journey viewer]** permet un accès en lecture seule aux **[!UICONTROL parcours]**, **[!UICONTROL objectifs]**, **[!UICONTROL messages]** et fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les utilisateurs affectés à ce profil de produit ne pourront effectuer ni modification, ni publication.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL View journeys]** : accès en lecture seule aux parcours.</li><li>**[!DNL View journeys event, data sources, actions]** : accès en lecture seule aux événements de parcours et aux sources de données.</li><li>**[!DNL View journeys report]** : accès en lecture seule aux rapports de parcours.</li></ul>| |Messages| <ul><li>**[!DNL View messages]** : accès en lecture seule aux messages.</li><li>**[!DNL View messages report]** : accès en lecture seule aux rapports de messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul>|

## [!DNL Message Manager] {#message-manager}

Le profil de produit **[!DNL Message Manager]** permet aux utilisateurs de créer et de modifier des **[!UICONTROL messages]** et la **[!UICONTROL gestion des décisions]**. Cependant, ils ne pourront effectuer aucune publication.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL View journeys]** : accès en lecture seule aux parcours.</li><li>**[!DNL View Journeys events, data sources and actions]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li></ul>| |Messages| <ul><li>**[!DNL Manage messages]** : la lecture, la création, la modification et la suppression des messages.</li><li>**[!DNL Manage messages preview and test]** : la lecture, la création et la modification de lʼaperçu du message et lʼenvoi du test/BAT.</li><li> **[!DNL View messages report]** : la lecture, la création, la modification et la suppression des rapports de messages.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Read profiles]** : accès en lecture seule au profil pour la prévisualisation et le test.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Le profil de produit **[!DNL Decisioning manager]** permet uniquement dʼaccéder au menu **[!UICONTROL Gestion des décisions]**. Les utilisateurs affectés à ce profil de produit ne pourront gérer, afficher et publier que les décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li><li>**[!DNL Publish decisions]** : lʼactivation ou la désactivation des activités de prise de décision.</li></ul>|
