---
title: Profils de produits natifs
description: En savoir plus sur les profils de produit intégrés
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
exl-id: null
feature: Populations témoins
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 8%

---

# Profils de produits natifs {#ootb-product-profiles}

## Administrateur de parcours {#journey-administrator}

Le profil de produit **[!UICONTROL Administrateur de Parcours]** permet aux menus d’administration de gérer et de publier des Parcours, des messages et de la gestion des décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li> **Gestion des parcours** : lecture, création, modification et suppression de parcours.</li><li>**Parcours** de publication : publier des parcours.</li><li>**Gérer les événements parcours, les sources de données et les actions** : lire, créer, modifier et supprimer des événements, des sources ou des actions.</li><li>**Afficher le rapport** parcours : lire et modifier le rapport parcours.</li></ul>|
|Messages|<ul><li> **Gérer les messages** : lire, créer, modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**Gérer l&#39;aperçu et le test des messages** : publier des messages.</li><li>**Publier les messages** : lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**Afficher le rapport** des messages : rapport lire et modifier les messages .</li></ul>|
|Administration|<ul><li>**Gérer la délégation des sous-domaines** : lire, créer, modifier et supprimer la délégation de sous-domaine.</li><li>**Gérer les pools** d’adresses IP : lire, créer, modifier et supprimer le pool ip.</li><li>**Afficher les enregistrements** PTR : accès en lecture seule aux enregistrements PTR.</li><li> **Gérer les paramètres** généraux des messages : lire, créer, modifier et supprimer les paramètres généraux des messages.</li><li>**Gérer les paramètres de message prédéfinis** : lire, créer, modifier et supprimer l’identité graphique du contenu.</li><li>**Gestion des règles** de suppression : accéder aux règles de suppression de lecture, création, modification et suppression ;</li><li>**Afficher la liste** de suppression : lire et exporter la liste de suppression locale.</li><li>**Gérer les alertes** : activer/désactiver des alertes pour les parcours, les messages et les droits ;</li></ul>|
|Decision Management|<ul><li>**Gérer les décisions** : lire, créer, modifier et supprimer des décisions.</li><li>**Gérer les stratégies** de classement : lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>|
|Adobe Experience Platform|<ul><li>**Sandbox** : Accordez l’accès aux environnements de test.</li><li>**Gestion des segments** : lire, créer, modifier et supprimer des segments.</li><li>**Gérer les profils** : lire, créer, modifier et supprimer des profils.</li><li>**Lire les jeux de données** : accès en lecture seule aux jeux de données.</li><li>**Lecture des schémas** : accès en lecture seule aux schémas.</li><li>**Lire l’espace de noms** d’identité : accès en lecture seule à l’espace de noms d’identité.</li><li>**Gestion des stratégies de fusion** : lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>|

## Approbateur de parcours {#journey-approver}

Le profil de produit **[!UICONTROL Approbateur de Parcours]** permet aux utilisateurs d’approuver les diffusions et de les publier. Ils peuvent ensuite vérifier le succès de leurs diffusions avec les rapports **[!UICONTROL Message]** et **[!UICONTROL Parcours]**.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**Gestion des parcours** : lecture, création, modification et suppression de parcours.</li><li>**Parcours** de publication : publier des parcours.</li><li>**Affichage des événements de parcours, des sources de données et des actions** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**Afficher le rapport** parcours : lire, modifier des rapports de parcours.</li></ul>|
|Messages| <ul><li>**Gérer les messages** : lire, créer, modifier et supprimer des messages.</li><li>**Publier des** messages, publier des messages.</li><li>**Gérer l&#39;aperçu et le test des messages** : lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**Afficher le rapport** des messages : lire, créer, modifier et supprimer le rapport des messages.</li></ul>|
|Decision Management| <ul><li>**Gérer les décisions** : lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**Gérer les stratégies** de classement : lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>|
|Adobe Experience Platform| <ul><li>**Gestion des segments** : lire, créer, modifier et supprimer des segments.</li><li>**Gérer les profils** : lire, créer, modifier et supprimer des profils.</li><li>**Lire les jeux de données** : accès en lecture seule aux jeux de données.</li><li>**Lecture des schémas** : accès en lecture seule aux schémas.</li><li>**Gestion des stratégies de fusion** : lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>|
|Administration| <ul><li>**Afficher les paramètres prédéfinis** des messages : accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## Gestionnaire de parcours {#journey-manager}

Le profil de produit **[!UICONTROL Gestionnaire de Parcours]** permet aux utilisateurs de créer et de modifier des **[!UICONTROL Parcours]** ainsi que toutes les fonctionnalités liées à **[!UICONTROL Parcours]**, mais ils ne pourront pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**Gestion des parcours** : lecture, création, modification et suppression de parcours.</li><li>**Affichage des événements de parcours** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li><li>**Afficher le rapport** parcours : lire, modifier le rapport parcours.</li></ul>|
|Messages| <ul><li>**Gérer les messages** : lire, créer, modifier et supprimer des messages.</li><li> **Gérer l&#39;aperçu et le test des messages** : lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li>**Afficher le rapport** des messages : lire, créer, modifier et supprimer le rapport des messages.</li></ul>|
|Decision Management| <ul><li>**Gérer les décisions** : lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**Gérer les stratégies** de classement : lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li></ul>|
|Adobe Experience Platform| <ul><li> **Gestion des segments** : lire, créer, modifier et supprimer des segments.</li><li>**Gérer les profils** : lire, créer, modifier et supprimer des profils.</li><li>**Lire les jeux de données** : accès en lecture seule aux jeux de données.</li><li>**Lecture des schémas** : accès en lecture seule aux schémas.</li><li>**Gestion des stratégies de fusion** : lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>|
|Administration| <ul><li>**Afficher les paramètres prédéfinis** des messages : accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## Visionneuse par parcours {#journey-viewer}

Le profil de produit **[!UICONTROL Visionneuse de Parcours]** permet un accès en lecture seule aux **[!UICONTROL Parcours]**, **[!UICONTROL Objectifs]**, **[!UICONTROL Messages]** et aux fonctionnalités **[!UICONTROL Gestion des décisions]**.

Les utilisateurs affectés à ce profil de produit ne pourront pas modifier ni publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**Afficher les parcours** : accès en lecture seule à parcours.</li><li>**Afficher les événements parcours, les sources de données, les actions** : accès en lecture seule aux événements parcours et aux sources de données.</li><li>**Afficher le rapport** parcours : accès en lecture seule aux rapports parcours.</li></ul>|
|Messages| <ul><li>**Afficher les messages** : accès en lecture seule aux messages.</li><li>**Afficher le rapport** des messages : accès en lecture seule aux rapports sur les messages.</li></ul>|
|Decision Management| <ul><li>**Afficher les décisions** : accès en lecture seule aux entités de décision.</li></ul>|

## Message Manager {#message-manager}

Le profil de produit **[!UICONTROL Message Manager]** permet aux utilisateurs de créer et de modifier des **[!UICONTROL messages]** et **[!UICONTROL Gestion des décisions]**, mais ne pourra pas les publier.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Parcours| <ul><li>**Afficher les parcours** : accès en lecture seule à parcours.</li><li>**Affichage des événements de Parcours, des sources de données et des actions** : accès en lecture seule aux événements de parcours, aux actions personnalisées de parcours et aux sources de données de parcours.</li></ul>|
|Messages| <ul><li>**Gérer les messages** : lire, créer, modifier et supprimer des messages.</li><li>**Gérer l&#39;aperçu et le test des messages** : lire, créer et modifier l&#39;aperçu du message et envoyer test/BAT.</li><li> **Afficher le rapport** des messages : lire, créer, modifier et supprimer des rapports de messages.</li></ul>|
|Decision Management| <ul><li>**Gérer les décisions** : lire, créer, modifier et supprimer des entités de prise de décision.</li></ul>|
|Adobe Experience Platform| <ul><li>**Lecture de profils** : accès en lecture seule au profil pour la prévisualisation et le test.</li><li>**Lire les jeux de données** : accès en lecture seule aux jeux de données.</li><li>**Lecture des schémas** : accès en lecture seule aux schémas.</li><li>**Gestion des stratégies de fusion** : lire, créer, modifier et supprimer des stratégies de fusion.</li></ul>|
|Administration| <ul><li>**Afficher les paramètres prédéfinis** des messages : accès en lecture seule aux paramètres prédéfinis des messages.</li></ul>|

## Gestionnaire de prise de décision {#decisioning-manager}

Le profil de produit **[!UICONTROL Gestionnaire de prise de décision]** permet uniquement le menu **[!UICONTROL Gestion des décisions]**. Les utilisateurs affectés à ce profil de produit ne pourront gérer, afficher et publier que les décisions.

Ce profil de produit comprend les autorisations suivantes :

| Fonctionnalité | Autorisations|
|-|-|
|Gestion des décisions| <ul><li>**Gérer les décisions** : lire, créer, modifier et supprimer des entités de prise de décision.</li><li>**Afficher les décisions** : accès en lecture seule aux entités de prise de décision.</li><li>**Gérer les stratégies** de classement : lire, créer, modifier et supprimer des rapports de messages personnalisés et utiliser des fonctions d’action.</li><li>**Publier les décisions** : approuver ou annuler l’approbation des activités de prise de décision.</li></ul>|