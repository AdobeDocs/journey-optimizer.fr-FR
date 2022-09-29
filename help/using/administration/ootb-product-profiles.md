---
title: Profils de produit intégrés
description: En savoir plus sur les profils de produit intégrés
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 8ca0d2bbd01451de613d8ae985e10a711fcc6316
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 100%

---

# Profils de produit intégrés {#ootb-product-profiles}


## À propos des autorisations liées aux messages{#message-permissions}

Adobe Journey Optimizer a publié de nouvelles fonctionnalités de création intégrées qui vous permettent de créer vos messages directement à partir d’un parcours ou d’une campagne.

Cette fonctionnalité aura un impact sur les autorisations comme suit :

| Nom de l’autorisation | Sera inclus dans |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Après le 25 juillet**, les autorisations liées aux **messages** seront toujours disponibles, car les messages restent accessibles pour permettre la transition et vous pouvez toujours les enregistrer comme modèle.

**À partir du 6 septembre**, les autorisations liées aux **messages** seront supprimées et les messages ne seront plus accessibles.

>[!WARNING]
>
>Si des utilisateurs sont affectés au profil de produit **[!DNL Message Manager]** uniquement, sans le profil de produit **[!DNL Journey manager]**, vous devez leur attribuer un nouveau profil de produit pour pouvoir continuer à modifier le contenu.


## [!DNL Campaign Administrator] {#campaign-administrator}

Le profil de produit **[!DNL Campaign Administrator]** permet dʼaccéder aux menus dʼadministration avec la possibilité de gérer et de publier des campagnes et d’avoir accès à la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Campagnes| <ul><li> **[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez les campagnes.</li><li>**[!DNL View campaigns report]** : lisez et modifiez le rapport des campagnes.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li><li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li><li>**[!DNL View PTR records]** : accès en lecture seule aux enregistrements PTR.</li><li> **[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li><li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li><li>**[!DNL Manage suppression rules]** : accès à la lecture, la création, la modification et la suppression des règles de suppression.</li><li>**[!DNL Export suppression list]** : accédez à la liste de suppression des exportations au format CSV.</li><li>**[!DNL View suppression list]** : la lecture et lʼexportation de la liste de suppression locale.</li><li>**[!DNL Manage alerts]** : activez/désactivez les alertes pour les campagnes, les messages et les droits.</li><li>**[!DNL Manage landing page settings]** : lisez, créez, modifiez et la supprimez les paramètres de la page de destination.</li><li>**[!DNL Manage SMS settings]** : lisez, créez, modifiez et supprimez des paramètres des SMS.</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]** : octroi de lʼaccès aux environnements sandbox.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

Le profil de produit **[!DNL Campaign Approver]** permet aux utilisateurs dʼapprouver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec les rapports **[!DNL Campaigns]**.

| Fonctionnalité | Autorisations|
|-|-|
|Campagnes| <ul><li>**[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez des campagnes.</li><li>**[!DNL View Campaigns report]** : la lecture et la modification des rapports de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

Le profil de produit **[!DNL Campaign Manager]** permet aux utilisateurs de créer et de modifier des **[!UICONTROL campagnes]** ainsi que toutes les fonctionnalités liées aux **[!UICONTROL campagnes]**. Cependant, ils ne pourront pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Campagnes| <ul><li>**[!DNL Manage campaigns]** : lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL View campaigns report]** : la lecture et la modification du rapport de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

Le profil de produit **[!DNL Campaign Viewer]** permet un accès en lecture seule aux **[!UICONTROL campagnes]** et aux fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les utilisateurs affectés à ce profil de produit ne pourront effectuer ni modification, ni publication.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Campagnes| <ul><li>**[!DNL View campaigns]** : accès en lecture seule aux campagnes.</li><li>**[!DNL View campaigns report]** : accès en lecture seule aux rapports de campagne.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

Le profil de produit **[!DNL Journey Administrator]** permet dʼavoir accès aux menus dʼadministration avec la possibilité de gérer et de publier des parcours et d’avoir accès à la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li> **[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL Publish journeys]** : la publication des parcours.</li><li>**[!DNL Manage journeys events, data sources and actions]** : la lecture, la création, la modification et la suppression des événements, des sources ou des actions.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul>| |Administration|<ul><li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li><li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li><li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li><li>**[!DNL View PTR records]** : accès en lecture seule aux enregistrements PTR.</li><li>**[!DNL Manage channel surfaces]** : la lecture, la création, la modification et la suppression du branding de contenu.</li><li>**[!DNL Manage Landing page settings]** : créer, modifier et supprimer des sous-domaines de page de destination et des paramètres prédéfinis de page de destination.</li><li> **[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li><li>**[!DNL Manage SMS settings]** : créer, modifier et supprimer les informations d’identification d’API et les surfaces de canal SMS requises pour activer le canal SMS.</li><li>**[!DNL Manage suppression rules]** : accès à la lecture, la création, la modification et la suppression des règles de suppression.</li><li>**[!DNL View suppression list]** : la lecture et lʼexportation de la liste de suppression locale.</li><li>**[!DNL Manage alerts]** : lʼactivation/la désactivation des alertes pour les parcours et les droits.</li></ul>|
|Gestion des décisions|<ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]** : octroi de lʼaccès aux environnements sandbox.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>|
|Bibliothèque Journey Optimizer|<ul><li>**[!DNL Manage Library Items]** : ajoutez et supprimez des expressions enregistrées dans la bibliothèque [!DNL Journey Optimizer].</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Le profil de produit **[!DNL Journey Approver]** permet aux utilisateurs dʼapprouver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec les rapports **[!DNL Journey]**.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL Publish journey]** : la publication des parcours.</li><li>**[!DNL View journeys events, data sources and actions]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification des rapports de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]** : accès en lecture seule aux surfaces des canaux.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Le profil de produit **[!DNL Journey Manager]** permet aux utilisateurs de créer et de modifier des **[!UICONTROL parcours]** ainsi que toutes les fonctionnalités liées aux **[!UICONTROL parcours]**. Cependant, ils ne pourront pas publier de parcours.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification et la suppression des parcours.</li><li>**[!DNL View journeys events]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Read datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL Read schemas]** : accès en lecture seule aux schémas.</li><li>**[!DNL Manage merge policies]** : la lecture, la création, la modification et la suppression des stratégies de fusion.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]** : accès en lecture seule aux surfaces des canaux.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

Le profil de produit **[!DNL Journey viewer]** permet un accès en lecture seule aux **[!UICONTROL parcours]** et aux fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les utilisateurs affectés à ce profil de produit ne pourront effectuer ni modification, ni publication.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**[!DNL View journeys]** : accès en lecture seule aux parcours.</li><li>**[!DNL View journeys event, data sources, actions]** : accès en lecture seule aux événements de parcours et aux sources de données.</li><li>**[!DNL View journeys report]** : accès en lecture seule aux rapports de parcours.</li></ul>|
|Gestion des décisions| <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Le profil de produit **[!DNL Decisioning manager]** permet uniquement dʼaccéder au menu **[!UICONTROL Gestion des décisions]**. Les utilisateurs affectés à ce profil de produit ne pourront gérer, afficher et publier que les décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Gestion des décisions| <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des entités de prise de décision.</li><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li><li>**[!DNL Publish decisions]** : lʼactivation ou la désactivation des activités de prise de décision.</li></ul>|
