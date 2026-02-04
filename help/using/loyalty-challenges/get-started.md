---
solution: Journey Optimizer
product: journey optimizer
title: Comprendre les défis de fidélité
description: Découvrez les fonctionnalités, le workflow et les défis de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 2%

---


# Comprendre les défis de fidélité {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="À propos des défis de fidélité"
>abstract="Les défis de fidélité vous permettent de créer des offres d’engagement personnalisées qui motivent les clients à effectuer des actions spécifiques et à gagner des récompenses."

Les défis de fidélité vous permettent de concevoir et de déployer des offres d’engagement personnalisées qui motivent les clients à effectuer des actions spécifiques et à gagner des récompenses.

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](gs-loyalty-challenges.md) - Aperçu rapide et étapes suivantes
* **Présentation des défis de fidélité** ◀︎ **Vous êtes ici** - Fonctionnalités, workflow, conditions préalables
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

## Vue d’ensemble {#overview}

Les défis de fidélité offrent une solution complète pour créer des programmes de fidélité à grande échelle, de la définition de tâches et de jalons à la diffusion de contenu et au suivi des performances sur l’ensemble des canaux. Vous pouvez créer trois types d’expériences de défi, configurer des récompenses, envoyer des notifications multicanaux à des étapes clés du cycle de vie et surveiller les performances par le biais de parcours générés automatiquement, tout en conservant l’intégration à votre système de gestion de la fidélité externe.

## Fonctionnement {#how-it-works}

La création et le lancement d’un défi de fidélité suivent ce workflow :

1. **Configurer l’ingestion des données** - Configurez les connecteurs source Experience Platform (tels que Capillaire) pour ingérer des données d’événement de fidélité qui effectuent le suivi des actions et de la progression des clients.

2. **Créer un défi** - Définissez les propriétés de base du défi, y compris le nom, le type (Standard, Streak ou Séquentiel), l’audience et la période.

3. **Ajouter des tâches** - Définissez les actions spécifiques que les clients doivent effectuer, y compris les types de tâches (achat, dépenses, visite, etc.), les quantités, les filtres de produit et les récompenses.

4. **Conception de cartes de contenu** - Créez la représentation visuelle de votre défi à l’aide de cartes de contenu Journey Optimizer qui s’affichent sur les appareils des clients.

5. **Configurer la messagerie** (facultatif) - Configurez des messages multicanaux (in-app, e-mail, push) pour les étapes clés : lancement, en cours et achèvement.

6. **Réviser et publier** - Testez votre défi avec des profils de test, puis publiez-le pour le rendre disponible auprès de votre audience cible.

7. **parcours généré automatiquement** - Lorsque vous publiez, Journey Optimizer crée automatiquement un parcours qui orchestre la diffusion et la messagerie des cartes de contenu.

8. **Activer le parcours** - Le parcours généré automatiquement est activé à la date de début de votre défi et gère toutes les interactions des clients.

9. **Surveiller les performances** - Suivez la participation, les taux d’achèvement, la distribution des récompenses et l’engagement des messages au moyen de rapports intégrés et de la zone de travail de parcours.

>[!NOTE]
>
>Le parcours généré automatiquement apparaît dans votre inventaire de parcours et peut être personnalisé si nécessaire. Toutefois, les modifications apportées directement au parcours ne sont pas resynchronisées avec la configuration de défi.

## Fonctionnalités principales {#key-capabilities}

Utilisez les défis de fidélité pour :

* **Créez trois types de défis** :
   * **Standard** : les clients effectuent un certain nombre de tâches pour gagner des récompenses.
   * **Streak** : les clients effectuent la même tâche plusieurs fois.
   * **Séquentiel** : les clients exécutent des tâches dans un ordre spécifique.

* **Conception du contenu du défi** : utilisez des cartes de contenu Journey Optimizer pour créer la représentation visuelle de votre défi sur les appareils des clients. Les cartes de contenu affichent les informations sur le défi, la progression et les récompenses sur l’appareil du client.

* **Configurer les exigences de tâche** : définissez ce que les clients doivent faire pour gagner des récompenses, notamment :
   * Types de tâches (achat, montant des dépenses, visite, etc.)
   * Exigences de quantité
   * Inclusions/exclusions de produits à l’aide de SKU
   * Attributs et conditions personnalisés

* **Configurer les récompenses** : définissez les récompenses que les clients gagnent à l’achèvement de la tâche ou après avoir relevé l’ensemble du défi

* **Envoyer des notifications** : diffusez des messages sur plusieurs canaux (in-app, e-mail, push) à des étapes clés :
   * **Launch** : quand le défi commence
   * **En cours** : lorsque les clients sont à mi-chemin
   * **Terminé** : lorsque les clients terminent le défi

* **Suivre les performances** : surveiller les parcours générés automatiquement et examiner les performances des défis

### Limites importantes {#limitations}

* **Aucun système comptable** : Loyalty Challenges ne suit pas les valeurs monétaires ou les soldes en points. Lorsque les clients relèvent un défi et gagnent une récompense, Journey Optimizer appelle votre système de gestion de la fidélité externe pour gérer l’affectation des points.

* **Sélection d’audience uniquement** : vous pouvez sélectionner des audiences existantes, mais ne pouvez pas créer de nouvelles audiences à partir de l’interface utilisateur des défis de fidélité.

## Conditions préalables {#prerequisites}

Avant d’utiliser les défis de fidélité, vérifiez que vous disposez des éléments suivants :

### Configuration de l’ingestion des données {#data-ingestion}

Les défis de fidélité reposent sur des données ingérées par le biais des connecteurs source Experience Platform pour suivre la progression des clients et l’achèvement des tâches.

1. **Configuration d&#39;un connecteur source pris en charge** : actuellement, le connecteur capillaire est généralement disponible. Des connecteurs supplémentaires sont prévus.

2. **Valider l’ingestion des données** : assurez-vous que les événements de fidélité et les données client circulent dans Experience Platform et sont disponibles dans Journey Optimizer.

Pour obtenir des instructions détaillées, voir :

* [Documentation sur les sources Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configuration des connecteurs source dans Journey Optimizer](../start/get-started-sources.md)

### Autorisations nécessaires {#required-permissions}

Pour utiliser les défis de fidélité, vous avez besoin des autorisations appropriées dans Journey Optimizer. Contactez votre administrateur si vous ne pouvez pas accéder à la fonctionnalité.

## Accès aux défis de fidélité {#access}

Pour accéder aux défis de fidélité :

1. Dans Adobe Journey Optimizer, sélectionnez **[!UICONTROL Défis de fidélité]** dans le menu de navigation de gauche.

2. L’inventaire des défis de fidélité répertorie tous les défis existants avec des informations telles que :
   * Nom et description du défi
   * Statut (brouillon, actif, arrêté, etc.)
   * Type de défi (Standard, Séquentiel, Séquentiel)
   * Dates de début et de fin
   * Date de la dernière modification

3. Sélectionnez **[!UICONTROL Créer un défi]** pour commencer à créer un nouveau défi.

### Défis liés à la recherche et au filtrage {#search-filter}

Utilisez les fonctionnalités de recherche et de filtrage pour trouver rapidement des défis spécifiques :

* **Rechercher** : saisissez le nom du défi ou les mots-clés dans le champ Rechercher
* **Filtrer par statut** : brouillon, planifié, actif, terminé, arrêté ou archivé
* **Filtrer par type** : défis standard, en traînée ou séquentiels
* **Filtrer par date** : défis au sein d’une période spécifique
* **Filtrer par balises** : défis associés à l’application de balises spécifiques

## Étapes suivantes {#next-steps}

Maintenant que vous comprenez les défis de fidélité, apprenez à créer votre premier défi :

* [Créer des défis](create-challenges.md)
* [Gestion des défis](manage-challenges.md)
