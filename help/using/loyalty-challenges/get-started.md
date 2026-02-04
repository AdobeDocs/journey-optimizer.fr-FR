---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des défis de fidélité
description: Découvrez comment créer et gérer des défis de fidélité dans Adobe Journey Optimizer pour créer des programmes de fidélité attrayants.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 4%

---


# Prise en main des défis de fidélité {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* **Prise en main des défis de fidélité** ◀︎ **Vous êtes ici** - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité](access-loyalty-challenges.md) - Inventaire et filtrage
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="À propos des défis de fidélité"
>abstract="Les défis de fidélité vous permettent de créer des offres d’engagement personnalisées qui motivent les clients à effectuer des actions spécifiques et à gagner des récompenses."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Contactez votre représentant ou représentante Adobe pour en bénéficier.

## Vue d’ensemble {#overview}

Les défis de fidélité offrent une solution complète pour créer des programmes de fidélité à grande échelle, de la définition de tâches et de jalons à la diffusion de contenu et au suivi des performances sur l’ensemble des canaux. Vous pouvez créer trois types d’expériences de défi, configurer des récompenses, envoyer des notifications multicanaux à des étapes clés du cycle de vie et surveiller les performances par le biais de parcours générés automatiquement, tout en conservant l’intégration à votre système de gestion de la fidélité externe.

## Fonctionnalités principales {#key-capabilities}

Utilisez les défis de fidélité pour :

* **Créez trois types de défis** :
   * **Standard** : les clients effectuent un nombre illimité de tâches dans n’importe quel ordre pour gagner des récompenses
   * **Streak** : les clients effectuent la même tâche plusieurs fois de suite
   * **Séquentiel** : les clients exécutent des tâches dans un ordre spécifique

* **Conception du contenu du défi** : utilisez des cartes de contenu Journey Optimizer pour créer la représentation visuelle de votre défi sur les appareils des clients. Les cartes de contenu affichent les informations sur le défi, la progression et les récompenses.

* **Configurer les exigences de tâche** : définissez ce que les clients doivent faire pour gagner des récompenses, notamment :
   * Types de tâches (achat, montant des dépenses, visite, engagement, événements personnalisés)
   * Exigences de quantité
   * Inclusions/exclusions de produits à l’aide de SKU, de catégories ou d’attributs
   * Attributs et conditions personnalisés

* **Configurer les récompenses** : définissez les récompenses que les clients gagnent à l’achèvement de la tâche (récompenses progressives) ou après avoir terminé l’ensemble du défi (récompenses finales).

* **Envoyer des notifications multicanaux** : diffusez des messages sur plusieurs canaux (in-app, e-mail, push) à des étapes clés :
   * **Launch** : quand le défi commence
   * **En cours** : lorsque les clients sont à mi-chemin
   * **Terminé** : lorsque les clients terminent le défi

* **Suivi des performances** : surveillez les parcours générés automatiquement et passez en revue les performances des défis au moyen de rapports intégrés.

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

## Conditions préalables {#prerequisites}

Avant d’utiliser les défis de fidélité, vérifiez que vous disposez des éléments suivants :

### Configuration de l’ingestion des données {#data-ingestion}

Les défis de fidélité reposent sur des données ingérées par le biais des connecteurs source Experience Platform pour suivre la progression des clients et l’achèvement des tâches.

1. **Configuration d&#39;un connecteur source pris en charge** : actuellement, le connecteur capillaire est généralement disponible. Des connecteurs supplémentaires sont prévus.

2. **Valider l’ingestion des données** : assurez-vous que les événements de fidélité et les données client circulent dans Experience Platform et sont disponibles dans Journey Optimizer.

Pour obtenir des instructions détaillées, voir :

* [Documentation sur les sources Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/home)
* [Configuration des connecteurs source dans Journey Optimizer](../start/get-started-sources.md)

### Autorisations nécessaires {#required-permissions}

Pour utiliser les défis de fidélité, vous avez besoin des autorisations appropriées dans Journey Optimizer. Contactez votre administrateur si vous ne pouvez pas accéder à la fonctionnalité.

### Audiences cibles {#target-audiences}

Créez des audiences cibles dans Experience Platform avant de créer des défis. Vous pouvez sélectionner des audiences existantes, mais ne pouvez pas créer de nouvelles audiences dans l’interface utilisateur Défis de fidélité .

## Limites importantes {#limitations}

* **Aucun système comptable** : Loyalty Challenges ne suit pas les valeurs monétaires ou les soldes en points. Lorsque les clients relèvent un défi et gagnent une récompense, Journey Optimizer appelle votre système de gestion de la fidélité externe pour gérer l’affectation des points.

* **Sélection d’audience uniquement** : vous pouvez sélectionner des audiences existantes, mais ne pouvez pas créer de nouvelles audiences à partir de l’interface utilisateur des défis de fidélité.

## Étapes suivantes {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Accéder aux défis de fidélité</strong></a>
    </div>
    <p>
    <em>Découvrez comment accéder à l’inventaire et filtrer les défis</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Créer des défis</strong></a>
    </div>
    <p>
    <em>Créer et configurer votre premier défi de fidélité</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Gérer les défis</strong></a>
    </div>
    <p>
    <em>Modification, surveillance et optimisation des défis</em>
    <p>
  </td>
</tr>
</table>
