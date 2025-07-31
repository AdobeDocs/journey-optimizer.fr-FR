---
solution: Journey Optimizer
product: journey optimizer
title: Rôles intégrés à Journey Optimizer
description: En savoir plus sur les rôles intégrés
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: autorisations, création, messages
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: ee2e07353762a81aadd3d63580c528f617599623
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 99%

---

# Rôles intégrés {#ootb-product-profiles}

Les rôles intégrés sont un ensemble de droits unitaires qui permet aux utilisateurs et utilisatrices d’accéder à certaines fonctionnalités ou à certains objets dans l’interface. Consultez [cette page](ootb-permissions.md) pour obtenir la liste des autorisations disponibles pour créer votre rôle.

## [!DNL Content Library Manager] {#content-library-manager}

Le rôle **[!DNL Content Library Manager]** permet uniquement d’accéder au menu **[!UICONTROL Modèles de contenu]**. Les personnes affectées à ce rôle ne pourront accéder à la bibliothèque de modèles que pour créer du contenu sans accéder aux parcours ou aux campagnes.

Ce rôle inclut les autorisations suivantes :

| Fonctionnalité | Autorisations |
|-|-|
| Bibliothèque Journey Optimizer | <ul><li>**[!DNL Manage library items]** : lire, créer, modifier et supprimer des éléments de la bibliothèque Journey Optimizer, y compris des modèles de contenu et des fragments.</li><li>**[!DNL Manage simulate content]** : accéder à l’option **[!UICONTROL Simuler du contenu]** pour l’aperçu et le BAT.</li><li>**[!DNL Publish Fragment]** : publiez des fragments de contenu.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Le rôle **[!DNL Decisioning manager]** permet uniquement d’accéder au menu **[!UICONTROL Gestion des décisions]**. Les personnes affectées à ce rôle ne pourront gérer, afficher et publier que les décisions.

Ce rôle inclut les autorisations suivantes :

| Fonctionnalité | Autorisations |
|-|-|
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Publish decisions]** : lʼactivation ou la désactivation des activités de prise de décision.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

Le rôle **[!DNL Campaign Administrator]** permet dʼaccéder aux menus dʼadministration avec la possibilité de gérer et de publier des campagnes et d’avoir accès à la gestion des décisions.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Campagnes | <ul><li> **[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez les campagnes.</li><li>**[!DNL View campaigns report]** : lisez et modifiez le rapport des campagnes.</li></ul> |
| Configurations de canal | <ul> <li>**[!DNL Export suppression list]** : l’accès à la liste de suppression des exports en tant que fichier CSV.</li> <li>**[!DNL Manage alerts]** : activez/désactivez les alertes pour les campagnes, les messages et les droits.</li> <li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li> <li>**[!DNL Manage landing page settings]** : lisez, créez, modifiez et la supprimez les paramètres de la page de destination.</li> <li>**[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li> <li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li> <li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li> <li>**[!DNL Manage SMS settings]** : lisez, créez, modifiez et supprimez des paramètres des SMS.</li> <li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li> <li>**[!DNL Manage suppression rules]** : l’accès à la lecture, la création, la modification et la suppression des règles de suppression.</li> <li>**[!DNL View PTR records]** : l’accès en lecture seule aux enregistrements PTR.</li> <li>**[!DNL View suppression list]** : la lecture et lʼexport de la liste de suppression locale.</li> </ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li> <li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li> <li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li> <li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li> <li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li> <li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li> <li>**[!DNL Sandbox]** : l’octroi de lʼaccès aux sandbox.</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Le rôle **[!DNL Campaign Approver]** permet aux utilisateurs et utilisatrices dʼapprouver les diffusions et de les publier. Il est ensuite possible vérifier le succès des diffusions avec les rapports **[!DNL Campaigns]**.

| Ressources | Autorisations |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez les campagnes.</li><li>**[!DNL View campaigns report]** : lire et modifier des rapports de campagne.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Le rôle **[!DNL Campaign Manager]** permet aux utilisateurs et aux utilisatrices de créer et de modifier des **[!UICONTROL campagnes]**, ainsi que toutes les fonctionnalités liées aux **[!UICONTROL campagnes]**. Cependant, leur publication ne sera pas possible.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]** : lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL View campaigns report]** : lecture et modification du rapport de parcours.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Le rôle **[!DNL Campaign Viewer]** permet un accès en lecture seule aux **[!UICONTROL campagnes]** et aux fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les personnes affectées à ce rôle ne pourront effectuer ni modification, ni publication.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]** : accès en lecture seule aux campagnes.</li><li>**[!DNL View campaigns report]** : accès en lecture seule aux rapports de campagne.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Le rôle **[!DNL Journey Administrator]** permet dʼavoir accès aux menus dʼadministration avec la possibilité de gérer et de publier des parcours et d’avoir accès à la gestion des décisions.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Parcours | <ul> <li>**[!DNL Manage journeys]** : lecture, création, modification et suppression des parcours.</li> <li>**[!DNL Manage journeys events, data sources and actions]** : lecture, création, modification et suppression des événements, des sources ou des actions.</li> <li>**[!DNL Publish journeys]** : publication des parcours.</li> <li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li> </ul> |
| Configurations de canal | <ul> <li>**[!DNL Manage alerts]** : lʼactivation/la désactivation des alertes pour les parcours et les droits.</li> <li>**[!DNL Manage IP pools]** : la lecture, la création, la modification et la suppression du groupe dʼadresses IP.</li> <li>**[!DNL Manage Landing page settings]** : créer, modifier et supprimer des sous-domaines de page de destination et des paramètres prédéfinis de page de destination.</li> <li>**[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li> <li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li> <li>**[!DNL Manage PTR records]** : lire et modifier les enregistrements PTR.</li> <li>**[!DNL Manage SMS settings]** : créer, modifier et supprimer les informations d’identification d’API et les configurations de canal SMS requises pour activer le canal SMS.</li> <li>**[!DNL Manage subdomains delegation]** : la lecture, la création, la modification et la suppression de la délégation de sous-domaine.</li> <li>**[!DNL Manage suppression rules]** : l’accès à la lecture, la création, la modification et la suppression des règles de suppression.</li> <li>**[!DNL View PTR records]** : l’accès en lecture seule aux enregistrements PTR.</li> <li>**[!DNL View suppression list]** : la lecture et lʼexport de la liste de suppression locale.</li> </ul> |
| Gestion des décisions | <ul> <li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li> <li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li> <li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li> <li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li> <li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li> <li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li> <li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li> <li>**[!DNL Sandbox]** : l’octroi de lʼaccès aux sandbox.</li> </ul> |
| Bibliothèque Journey Optimizer | <ul> <li>**[!DNL Manage Library Items]** : ajoutez et supprimez des expressions enregistrées dans la bibliothèque [!DNL Journey Optimizer].</li> </ul> |
| Gouvernance des données | <ul> <li>**[!DNL Manage data usage policies]** : la lecture, la ccréation, la modification et la suppression des politiques dʼutilisation des données.</li> <li>**[!DNL Manage usage label]** : lire, créer et supprimer des libellés d’utilisation.</li> <li>**[!DNL View data usage policies]** : accéder en lecture seule aux politiques d’utilisation des données.</li> <li>**[!DNL View user activity log]** : lire et exporter les journaux d’audit.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Le rôle **[!DNL Journey Approver]** permet aux utilisateurs et utilisatrices dʼapprouver les diffusions et de les publier. Il est ensuite possible de vérifier le succès des diffusions avec les rapports **[!DNL Journey]**.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Parcours | <ul><li>**[!DNL Manage journeys]** : lecture, création, modification et suppression des parcours.</li><li>**[!DNL Publish journey]** : la publication des parcours.</li><li>**[!DNL View journeys events, data sources and actions]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification des rapports de parcours.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View channel configurations]** : accès en lecture seule aux configurations de canaux.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Le rôle **[!DNL Journey Manager]** permet aux utilisateurs et aux utilisatrices de créer et de modifier des **[!UICONTROL parcours]** ainsi que toutes les fonctionnalités liées aux **[!UICONTROL parcours]**. Cependant, il sera impossible de les publier.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Parcours | <ul><li>**[!DNL Manage journeys]** : lecture, création, modification et suppression des parcours.</li><li>**[!DNL View journeys events]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : lecture et modification du rapport de parcours.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li> **[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View channel configurations]** : accès en lecture seule aux configurations de canaux.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Le rôle **[!DNL Journey viewer]** permet un accès en lecture seule aux **[!UICONTROL campagnes]** et aux fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les personnes affectées à ce rôle ne pourront effectuer ni modification, ni publication.

Ce rôle inclut les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Parcours | <ul><li>**[!DNL View journeys]** : accès en lecture seule aux parcours.</li><li>**[!DNL View journeys event, data sources, actions]** : accès en lecture seule aux événements de parcours et aux sources de données.</li><li>**[!DNL View journeys report]** : accès en lecture seule aux rapports de parcours.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Orchestrated Campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: read, create, edit, and delete custom dashboards.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: Read, create, edit and delete links and reconciliations between Adobe Experience Platform Profiles and Relational store entities.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL View sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to publish Orchestrated campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaign reports.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li> </ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Orchestrated campaigns]** and every capability linked to **[!UICONTROL Orchestrated campaigns]** but will not be able to publish them.

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Orchestrated campaigns]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Messages|<ul><li>**[!DNL View messages]**: view messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

-->