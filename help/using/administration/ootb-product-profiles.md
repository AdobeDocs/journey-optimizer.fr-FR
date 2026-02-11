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
source-git-commit: a91d5c6a22f81411d7a9acbe2bbc8e86c1a4da13
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 96%

---

# Rôles intégrés {#ootb-product-profiles}

Les rôles intégrés sont un ensemble de droits unitaires qui permet aux utilisateurs et utilisatrices d’accéder à certaines fonctionnalités ou à certains objets dans l’interface. Consultez [cette page](ootb-permissions.md) pour obtenir la liste des autorisations disponibles pour créer votre rôle.


## [!DNL Campaign Administrator] {#campaign-administrator}

Le rôle **[!DNL Campaign Administrator]** permet dʼaccéder aux menus dʼadministration avec la possibilité de gérer et de publier des campagnes et d’avoir accès à la gestion des décisions.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li> <li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li> <li>**[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li> <li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li> <li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li> <li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li> <li>**[!DNL Sandbox]** : octroi de lʼaccès aux sandbox.</li> </ul> |
| Campagnes | <ul><li> **[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez les campagnes.</li><li>**[!DNL View campaigns report]** : lisez et modifiez le rapport des campagnes.</li></ul> |
| Configurations de canal | <ul> <li>**[!DNL Export suppression list]** : l’accès à la liste de suppression des exports en tant que fichier CSV.</li> <li>**[!DNL Manage alerts]** : activation/désactivation des alertes pour les campagnes, les messages et les droits.</li> <li>**[!DNL Manage IP pools]** : lecture, création, modification et suppression des groupes dʼadresses IP.</li> <li>**[!DNL Manage landing page settings]** : lecture, création, modification et suppression des paramètres de page de destination.</li> <li>**[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li> <li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li> <li>**[!DNL Manage PTR records]** : lecture et modification des enregistrements PTR.</li> <li>**[!DNL Manage SMS settings]** : lecture, création, modification et suppressions des paramètres des SMS.</li> <li>**[!DNL Manage subdomains delegation]** : lecture, création, modification et suppression de la délégation de sous-domaine.</li> <li>**[!DNL Manage suppression rules]** : accès, lecture, création, modification et suppression des règles de suppression.</li> <li>**[!DNL View PTR records]** : l’accès en lecture seule aux enregistrements PTR.</li> <li>**[!DNL View suppression list]** : la lecture et lʼexport de la liste de suppression locale.</li> </ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Le rôle **[!DNL Campaign Approver]** permet aux utilisateurs et utilisatrices dʼapprouver les diffusions et de les publier. Il est ensuite possible vérifier le succès des diffusions avec les rapports **[!DNL Campaigns]**.

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li><li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Campagnes | <ul><li>**[!DNL Manage campaigns]** : lisez, créez, modifiez et supprimez des campagnes.</li><li>**[!DNL Publish campaigns]** : publiez les campagnes.</li><li>**[!DNL View campaigns report]** : lecture et modification des rapports de campagne.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

Le rôle **[!DNL Campaign Manager]** permet aux utilisateurs et utilisatrices de créer et de modifier des **[!UICONTROL campagnes]**, ainsi que toutes les fonctionnalités liées aux **[!UICONTROL campagnes]**. Cependant, leur publication ne sera pas possible.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li><li> **[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Campagnes | <ul><li>**[!DNL Manage campaigns]** : lire, créer, modifier et supprimer des campagnes.</li><li>**[!DNL View campaigns report]** : lecture et modification du rapport de parcours.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Le rôle **[!DNL Campaign Viewer]** permet un accès en lecture seule aux **[!UICONTROL campagnes]** et aux fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les personnes affectées à ce rôle ne pourront effectuer ni modification, ni publication.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]** : accès en lecture seule aux campagnes.</li><li>**[!DNL View campaigns report]** : accès en lecture seule aux rapports de campagne.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Le rôle **[!DNL Content Library Manager]** permet uniquement d’accéder au menu **[!UICONTROL Modèles de contenu]**. Les personnes affectées à ce rôle ne pourront accéder à la bibliothèque de modèles que pour créer du contenu sans accéder aux parcours ou aux campagnes.

Cette autorisation inclut les autorisations suivantes :

| Fonctionnalité | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li><li> **[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul> |
| Bibliothèque Journey Optimizer | <ul><li>**[!DNL Manage library items]** : lire, créer, modifier et supprimer des éléments de la bibliothèque Journey Optimizer, y compris des modèles de contenu et des fragments.</li><li>**[!DNL Manage simulate content]** : accéder à l’option **[!UICONTROL Simuler du contenu]** pour l’aperçu et le BAT.</li><li>**[!DNL Publish Fragment]** : publiez des fragments de contenu.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Le rôle **[!DNL Decisioning manager]** permet uniquement d’accéder au menu **[!UICONTROL Gestion des décisions]**. Les personnes affectées à ce rôle ne pourront gérer, afficher et publier que les décisions.

Cette autorisation inclut les autorisations suivantes :

| Fonctionnalité | Autorisations |
|-|-|
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li><li>**[!DNL Publish decisions]** : activation ou désactivation des activités de prise de décision.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Le rôle **[!DNL Journey Administrator]** permet dʼavoir accès aux menus dʼadministration avec la possibilité de gérer et de publier des parcours et d’avoir accès à la gestion des décisions.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li> <li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li> <li>**[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li> <li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li> <li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li> <li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li> <li>**[!DNL Sandbox]** : octroi de lʼaccès aux sandbox.</li> </ul> |
| Configurations de canal | <ul> <li>**[!DNL Manage alerts]** : activation/désactivation des alertes pour les parcours et les droits.</li> <li>**[!DNL Manage IP pools]** : lecture, création, modification et suppression des groupes dʼadresses IP.</li> <li>**[!DNL Manage Landing page settings]** : créer, modifier et supprimer des sous-domaines de page de destination et des paramètres prédéfinis de page de destination.</li> <li>**[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li> <li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li> <li>**[!DNL Manage PTR records]** : lecture et modification des enregistrements PTR.</li> <li>**[!DNL Manage SMS settings]** : création, modification et suppression des informations d’identification d’API et des configurations de canal SMS requises pour activer le canal SMS.</li> <li>**[!DNL Manage subdomains delegation]** : lecture, création, modification et suppression de la délégation de sous-domaine.</li> <li>**[!DNL Manage suppression rules]** : accès, lecture, création, modification et suppression des règles de suppression.</li> <li>**[!DNL View PTR records]** : l’accès en lecture seule aux enregistrements PTR.</li> <li>**[!DNL View suppression list]** : la lecture et lʼexport de la liste de suppression locale.</li> </ul> |
| Gouvernance des données | <ul> <li>**[!DNL Manage data usage policies]** : la lecture, la ccréation, la modification et la suppression des politiques dʼutilisation des données.</li> <li>**[!DNL Manage usage label]** : lecture, création et suppression des libellés d’utilisation.</li> <li>**[!DNL View data usage policies]** : accès en lecture seule aux politiques d’utilisation des données.</li> <li>**[!DNL View user activity log]** : accès en lecture seule aux journaux d’audit enregistrés des activités d’Experience Platform.</li> </ul> |
| Gestion des décisions | <ul> <li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li> <li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li> </ul> |
| Parcours | <ul> <li>**[!DNL Manage journeys]** : la lecture, la création, la modification, l’arrêt (en direct, en mode test et essai) et la suppression des parcours. </li> <li>**[!DNL Manage journeys events, data sources and actions]** : lecture, création, modification et suppression des événements, des sources ou des actions.</li> <li>**[!DNL Publish journeys]** : publication, démarrage du mode test, démarrage de l’exécution d’essai, pause et reprise des parcours. </li> <li>**[!DNL View journeys report]** : lecture et modification du rapport de parcours.</li> </ul> |
| Bibliothèque Journey Optimizer | <ul> <li>**[!DNL Manage Library Items]** : ajout et suppression des expressions enregistrées dans la bibliothèque [!DNL Journey Optimizer].</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Le rôle **[!DNL Journey Approver]** permet aux utilisateurs et utilisatrices dʼapprouver les diffusions et de les publier. Il est ensuite possible de vérifier le succès des diffusions avec les rapports **[!DNL Journey]**.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li><li>**[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View channel configurations]** : accès en lecture seule aux configurations de canaux.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul> |
| Parcours | <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification, l’arrêt (en direct, en mode test et essai) et la suppression des parcours. </li><li>**[!DNL Publish journey]** : publication, démarrage du mode test, démarrage de l’exécution d’essai, pause et reprise des parcours. </li><li>**[!DNL View journeys events, data sources and actions]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification des rapports de parcours.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Le rôle **[!DNL Journey Manager]** permet aux utilisateurs et utilisatrices de créer et de modifier des **[!UICONTROL parcours]** ainsi que toutes les fonctionnalités liées aux **[!UICONTROL parcours]**. Cependant, il sera impossible de les publier.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li><li> **[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View channel configurations]** : accès en lecture seule aux configurations de canaux.</li></ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des rapports personnalisés et lʼutilisation des fonctionnalités dʼaction.</li></ul> |
| Parcours | <ul><li>**[!DNL Manage journeys]** : la lecture, la création, la modification, l’arrêt (en direct, en mode test et essai) et la suppression des parcours.</li><li>**[!DNL View journeys events]** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**[!DNL View journeys report]** : la lecture et la modification du rapport de parcours.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Le rôle **[!DNL Journey viewer]** permet un accès en lecture seule aux **[!UICONTROL campagnes]** et aux fonctionnalités de **[!UICONTROL gestion des décisions]**.

Les personnes affectées à ce rôle ne pourront effectuer ni modification, ni publication.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Gestion des décisions | <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul> |
| Parcours | <ul><li>**[!DNL View journeys]** : accès en lecture seule aux parcours.</li><li>**[!DNL View journeys event, data sources, actions]** : accès en lecture seule aux événements de parcours et aux sources de données.</li><li>**[!DNL View journeys report]** : accès en lecture seule aux rapports de parcours.</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

Le rôle **[!DNL Orchestrated Campaign Administrator]** permet dʼavoir accès aux menus dʼadministration avec la possibilité de gérer et de publier des campagnes orchestrées.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]** : activation des fonctionnalités de campagne et d’audience optimisées par l’IA ou accès à celles-ci.</li> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li> <li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li> <li>**[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li> <li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li> <li>**[!DNL Read Identity namespace]** : accès en lecture seule à lʼespace de noms d’identité.</li> <li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li> <li>**[!DNL Sandbox]** : octroi de lʼaccès aux sandbox.</li> <li>**[!DNL View operational insights]** : accès en lecture seule aux informations système et aux tableaux de bord de surveillance.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL Export suppression list]** : l’accès à la liste de suppression des exports en tant que fichier CSV.</li> <li>**[!DNL Manage alerts]** : activation/désactivation des alertes pour les campagnes, les messages et les droits.</li> <li>**[!DNL Manage custom dashboards]** : lecture, création, modification et suppression des tableaux de bord personnalisés.</li><li>**[!DNL Manage IP pools]** : lecture, création, modification et suppression des groupes dʼadresses IP.</li> <li>**[!DNL Manage landing page settings]** : lecture, création, modification et suppression des paramètres de page de destination.</li> <li>**[!DNL Manage messages general settings]** : la lecture, la création, la modification et la suppression des paramètres généraux du message.</li> <li>**[!DNL Manage messages presets]** : la lecture, la création, la modification et la suppression du branding de contenu.</li><li>**[!DNL Manage PTR records]** : lecture et modification des enregistrements PTR.</li> <li>**[!DNL Manage SMS settings]** : lecture, création, modification et suppressions des paramètres des SMS.</li> <li>**[!DNL Manage subdomains delegation]** : lecture, création, modification et suppression de la délégation de sous-domaine.</li> <li>**[!DNL Manage suppression rules]** : accès, lecture, création, modification et suppression des règles de suppression.</li> <li>**[!DNL View PTR records]** : l’accès en lecture seule aux enregistrements PTR.</li> <li>**[!DNL View suppression list]** : la lecture et lʼexport de la liste de suppression locale.</li> </ul> |
| Tableau de bord | <ul> <li>**[!DNL Manage standard dashboard]** : lecture, création, modification et suppression des widgets personnalisés et du schéma de widget par le biais de la bibliothèque de widgets.</li> </ul> |
| Gouvernance des données | <ul> <li>**[!DNL View user activity log]** : accès en lecture seule aux journaux d’audit enregistrés des activités d’Experience Platform. </li> </ul> |
| Ingestion de données | <ul> <li>**[!DNL Manage sources]** : lecture, création, modification et désactivation de sources.</li> </ul> |
| Gestion des données | <ul> <li>**[!DNL Manage datasets]** : lecture, création, modification et suppression des jeux de données.</li> </ul> |
| Modélisation des données | <ul> <li>**[!DNL Manage schemas]** : lecture, création, modification et suppression des schémas et des ressources associées.</li> </ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : la lecture, la création, la modification et la suppression des décisions.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression des stratégies de classement.</li></ul> |
| Règles Journey Optimizer | <ul> <li>**[!DNL View frequency rules]** : accès en lecture seule aux règles de fréquence.</li><li>**[!DNL Manage frequency rules]** : lecture, création, modification ou suppression des règles de fréquence.</li> </ul> |
| Messages | <ul><li> **[!DNL Manage Messages]** : lecture, création, modification et suppression des messages. </li> **[!DNL Manage Messages Preview and Test]** : approbation et publication de messages lorsqu’une politique est appliquée.</li><li>**[!DNL Publish Messages]** : publication des messages. </li><li>**[!DNL View Messages Report]** : lecture et modification des rapports sur les messages. <li></ul> |
| Campagnes orchestrées | <ul><li> **[!DNL Manage orchestrated campaigns]** : lecture, création, modification et suppression des campagnes orchestrées.</li> <li>**[!DNL Manage orchestrated campaigns admin]** : lecture, création, modification et suppression des liens et des réconciliations entre les profils Adobe Experience Platform et les entités de stockage relationnel.</li><li>**[!DNL Publish orchestrated campaigns]** : publication de campagnes orchestrées.</li><li>**[!DNL View orchestrated campaigns report]** : lecture et modification du rapport sur les campagnes orchestrées.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

Le rôle **[!DNL Orchestrated Campaign Approver]** permet aux utilisateurs et aux utilisatrices de publier des campagnes orchestrées.

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]** : la lecture, la création, la modification et la suppression des définitions de segments.</li> <li>**[!DNL Manage profiles]** : la lecture, la création, la modification et la suppression des profils.</li> <li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li> <li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li> <li>**[!DNL Enable AI Assistant]** : activation des fonctionnalités de campagne et d’audience optimisées par l’IA ou accès à celles-ci.</li>  <li>**[!DNL View operational insights]** : accès en lecture seule aux informations système et aux tableaux de bord de surveillance.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li> <li>**[!DNL Manage custom dashboards]** : création, modification et suppression des tableaux de bord personnalisés.</li></ul> |
| Tableau de bord | <ul> <li>**[!DNL Manage standard dashboard]** : lecture, création, modification et suppression des widgets personnalisés et du schéma de widget par le biais de la bibliothèque de widgets.</li> </ul> |
| Gouvernance des données | <ul> <li>**[!DNL View user activity log]** : accès en lecture seule aux journaux d’audit enregistrés des activités d’Experience Platform.</li> </ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul> |
| Règles Journey Optimizer | <ul> <li>**[!DNL View frequency rules]** : accès en lecture seule aux règles de fréquence.</li></ul> |
| Messages | <ul><li> **[!DNL Manage Messages]** : lecture, création, modification et suppression des messages. </li> **[!DNL Manage Messages Preview and Test]** : approbation et publication de messages lorsqu’une politique est appliquée.</li><li>**[!DNL Publish Messages]** : publication des messages. </li><li>**[!DNL View Messages Report]** : lecture et modification des rapports sur les messages. <li></ul> |
| Campagnes orchestrées | <ul><li>**[!DNL Manage orchestrated campaigns]** : lecture, création, modification et suppression des campagnes orchestrées.</li><li>**[!DNL Publish orchestrated campaigns]** : publication de campagnes orchestrées.</li><li>**[!DNL View orchestrated campaigns admin]** : accès en lecture seule aux liens et aux réconciliations entre les profils Adobe Experience Platform et les entités de stockage relationnel.</li><li>**[!DNL View orchestrated campaigns report]** : lecture et modification des rapports sur les campagnes orchestrées.</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

Le rôle **[!DNL Orchestrated Campaign Manager]** permet aux utilisateurs et aux utilisatrices de créer et de modifier des **[!UICONTROL campagnes orchestrées]**, ainsi que toutes les fonctionnalités liées aux **[!UICONTROL campagnes orchestrées]**. Cependant, leur publication ne sera pas possible.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]** : activation des fonctionnalités de campagne et d’audience optimisées par l’IA ou accès à celles-ci.</li> <li>**[!DNL Manage merge policies]** : lecture, création, modification et suppression des politiques de fusion.</li><li>**[!DNL Manage profiles]** : lecture, création, modification et suppression des profils.</li><li> **[!DNL Manage segments]** : lecture, création, modification et suppression des définitions de segments.</li><li>**[!DNL View datasets]** : accès en lecture seule aux jeux de données.</li>  <li>**[!DNL View operational insights]** : accès en lecture seule aux informations système et aux tableaux de bord de surveillance.</li><li>**[!DNL View schemas]** : accès en lecture seule aux schémas.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL Manage custom dashboards]** : création, modification et suppression des tableaux de bord personnalisés.</li><li>**[!DNL View messages presets]** : accès en lecture seule aux préréglages des messages.</li></ul> |
| Tableau de bord | <ul> <li>**[!DNL Manage standard dashboard]** : lecture, création, modification et suppression des widgets personnalisés et du schéma de widget par le biais de la bibliothèque de widgets.</li> </ul> |
| Gouvernance des données | <ul> <li>**[!DNL View user activity log]** : accès en lecture seule aux journaux d’audit enregistrés des activités d’Experience Platform.</li> </ul> |
| Gestion des décisions | <ul><li>**[!DNL Manage decisions]** : lecture, création, modification et suppression des entités de prise de décision.</li><li>**[!DNL Manage ranking strategies]** : la lecture, la création, la modification et la suppression de rapports de messages personnalisés et lʼutilisation des fonctions dʼaction.</li></ul> |
| Règles Journey Optimizer | <ul> <li>**[!DNL View frequency rules]** : accès en lecture seule aux règles de fréquence. </li></ul> |
| Messages | <ul><li> **[!DNL Manage Messages]** : lecture, création, modification et suppression des messages. </li> **[!DNL Manage Messages Preview and Test]** : approbation et publication de messages lorsqu’une politique est appliquée.</li><li>**[!DNL View Messages Report]** : lecture et modification des rapports sur les messages. </li></ul> |
| Campagnes orchestrées | <ul><li>**[!DNL Manage orchestrated campaigns]** : lecture, création, modification et suppression des campagnes orchestrées.</li><li>**[!DNL View orchestrated campaigns report]** : lecture et modification des campagnes orchestrées.</li><li>**[!DNL View orchestrated campaigns admin]** : accès en lecture seule aux liens et aux réconciliations entre les profils Adobe Experience Platform et les entités de stockage relationnel.</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

Le rôle **[!DNL Campaign Viewer]** permet d’accéder en lecture seule aux fonctionnalités des **[!UICONTROL campagnes orchestrées]**.

Les personnes affectées à ce rôle ne pourront effectuer ni modification, ni publication.

Ce rôle comprend les autorisations suivantes :

| Ressources | Autorisations |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]** : activation des fonctionnalités de campagne et d’audience optimisées par l’IA ou accès à celles-ci.</li> <li>**[!DNL View operational insights]** : accès en lecture seule aux informations système et aux tableaux de bord de surveillance.</li></ul> |
| Configurations de canal | <ul><li>**[!DNL Manage custom dashboards]** : création, modification et suppression des tableaux de bord personnalisés.</li></ul> |
| Tableau de bord | <ul> <li>**[!DNL Manage standard dashboard]** : lecture, création, modification et suppression des widgets personnalisés et du schéma de widget par le biais de la bibliothèque de widgets.</li> </ul> |
| Gouvernance des données | <ul> <li>**[!DNL View user activity log]** : accès en lecture seule aux journaux d’audit enregistrés des activités d’Experience Platform.</li> </ul> |
| Gestion des décisions | <ul><li>**[!DNL View decisions]** : accès en lecture seule aux entités de prise de décision.</li></ul> |
| Règles Journey Optimizer | <ul> <li>**[!DNL View frequency rules]** : accès en lecture seule aux règles de fréquence.</li></ul> |
| Campagnes orchestrées | <ul><li>**[!DNL View orchestrated campaigns]** : accès en lecture seule aux campagnes orchestrées.</li><li>**[!DNL View orchestrated campaigns report]** : accès en lecture seule aux rapports sur les campagnes orchestrées.</li></ul> |




