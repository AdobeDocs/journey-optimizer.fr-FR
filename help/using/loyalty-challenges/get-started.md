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
source-git-commit: bd98e4dc77a0adde83df6251af749aa6da8c058d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 4%

---


# Prise en main des défis de fidélité {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* **Prise en main des défis de fidélité** ◀︎ **Vous êtes ici** - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité](access-loyalty-challenges.md) - Inventaire et filtrage
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Créer des tâches](create-tasks.md) - Définir des tâches de défi
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Vue d’ensemble {#overview}

Les défis de fidélité offrent une solution complète pour créer des programmes de fidélité à grande échelle, de la définition de tâches et de jalons à la diffusion de contenu et au suivi des performances sur l’ensemble des canaux.

Vous pouvez créer trois types d’expériences de défi :

* **Défis standard** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre
* **Défis en série** : les clients effectuent la même tâche plusieurs fois de suite
* **Défis séquentiels** : les clients exécutent des tâches dans un ordre défini

Grâce aux défis de fidélité, vous pouvez configurer des récompenses, envoyer des notifications multicanaux à des étapes clés du cycle de vie et surveiller les performances par le biais de parcours générés automatiquement, tout en conservant l’intégration à votre système de gestion de la fidélité externe.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## Fonctionnement {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

La création et le lancement d’un défi de fidélité suivent ce workflow :

1. **Configurer l’ingestion des données** - Configurez les connecteurs source Experience Platform (tels que le connecteur capillaire) pour ingérer des données d’événement de fidélité qui effectuent le suivi des actions et de la progression des clients. Ces données alimentent le suivi des défis et l’achèvement des tâches.

1. **Créer un défi** - Définissez les propriétés de base du défi, y compris le nom, le type (Standard, Streak ou Séquentiel), l’audience et la période. Voir [Créer des défis](create-challenges.md) pour obtenir des instructions détaillées.

1. **Ajouter des tâches** - Définissez les actions spécifiques que les clients doivent effectuer, y compris les types de tâche (achat, dépense, visite, engagement, événements personnalisés), les quantités, les filtres de produit et les récompenses. Voir [Créer des tâches](create-tasks.md) pour obtenir des instructions détaillées.

1. **Conception de cartes de contenu** - Créez la représentation visuelle de votre défi à l’aide de Journey Optimizer [cartes de contenu](../content-card/create-content-card.md) qui s’affichent sur les appareils des clients. Les cartes de contenu affichent les informations sur le défi, la progression et les récompenses.

1. **Configurer la messagerie** (facultatif) - Configurez des messages multicanaux ([in-app](../in-app/get-started-in-app.md), [e-mail](../email/get-started-email.md), [push](../push/get-started-push.md)) pour les étapes clés du cycle de vie : lancement, en cours et achèvement.

1. **Réviser et publier** - Testez votre défi avec des [profils de test](../test-approve/test-profiles.md), puis publiez-le pour le rendre disponible auprès de votre audience cible.

1. **Activer le parcours** - Lorsque vous publiez un défi, Journey Optimizer crée automatiquement un [parcours ](../building-journeys/journey-gs.md) à l’état de brouillon qui orchestre la diffusion et la messagerie des cartes de contenu. Accédez à l’inventaire des Parcours, localisez le parcours généré automatiquement (nommé « Défi : [Nom du défi] ») et [activez-le](../building-journeys/publishing-the-journey.md) pour mettre le défi à la disposition de vos clients.

1. **Surveiller les performances** - Suivez la participation, les taux d’achèvement, la distribution des récompenses et l’engagement des messages au moyen de rapports intégrés et de la zone de travail de parcours. Voir [Gérer les défis](manage-challenges.md) pour plus d’informations sur la surveillance.

## Conditions préalables {#prerequisites}

Avant d’utiliser les défis de fidélité, vérifiez que vous disposez des éléments suivants :

+++Configuration de l’ingestion des données

Les défis de fidélité reposent sur des données ingérées par le biais des connecteurs source Experience Platform pour suivre la progression des clients et l’achèvement des tâches.

1. **Configuration d&#39;un connecteur source pris en charge** : actuellement, le connecteur capillaire est généralement disponible. D’autres connecteurs sont prévus pour les prochaines versions.

1. **Valider l’ingestion des données** : assurez-vous que les événements de fidélité et les données client circulent dans Experience Platform et sont disponibles dans Journey Optimizer. Vérifiez que le schéma de données comprend les champs nécessaires pour effectuer le suivi des actions et de la progression des clients.

Pour obtenir des instructions détaillées, voir :

* [Documentation sur les sources Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configuration des connecteurs source dans Journey Optimizer](../start/get-started-sources.md)

+++

+++Autorisations nécessaires

Pour utiliser les défis de fidélité, vous avez besoin des autorisations appropriées dans Journey Optimizer. Les autorisations requises sont les suivantes :

* Accès à la fonctionnalité **[!UICONTROL Défis de fidélité]**
* Autorisations de création et de gestion des parcours
* Autorisations pour créer et gérer des cartes de contenu
* Autorisations pour créer et gérer des audiences

Contactez votre administrateur si vous ne pouvez pas accéder à la fonctionnalité ou si vous avez besoin d’autorisations supplémentaires.

+++

+++Audiences cibles

Créez des audiences cibles dans Experience Platform avant de créer des défis. Ces audiences définissent les clients éligibles pour participer à vos défis de fidélité. Pour plus d’informations sur la création d’audiences, consultez la section [Prise en main des audiences](../audience/about-audiences.md).

+++

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
    </p>
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
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>Créer des tâches</strong></a>
    </div>
    <p>
    <em>Définir les actions et les récompenses pour les défis</em>
    </p>
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
    </p>
  </td>
</tr>
</table>
