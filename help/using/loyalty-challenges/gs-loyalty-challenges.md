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
source-git-commit: 7b075996eebd03f0aa812da3ece9cfebef8c65fc
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 7%

---


# Prise en main des défis de fidélité {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

Les défis de fidélité vous permettent de créer des offres d’engagement personnalisées pour vos clients et d’orchestrer des programmes de fidélité à grande échelle. Vous pouvez concevoir des défis avec des tâches et des jalons spécifiques, récompenser les clients qui les ont réalisés et leur offrir une expérience via les canaux Adobe Journey Optimizer.

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* **Prise en main des défis de fidélité** ◀︎ **Vous êtes ici** - Aperçu rapide et étapes suivantes
* [Présentation des défis de fidélité](get-started.md) - Fonctionnalités, workflow, conditions préalables
* [Créer des défis](create-challenges.md) - Créez et configurez des défis
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

## Aperçu rapide {#quick-overview}

Utilisez les défis de fidélité pour :

* **Créez trois types de défis** : standard (toutes les tâches), en flux continu (tâches répétées) ou séquentiel (tâches ordonnées)
* **Conception du contenu du défi** : utilisez des cartes de contenu pour afficher les défis sur les appareils des clients
* **Configurer les exigences de tâche** : définissez des actions telles que des achats, des visites ou des événements personnalisés avec des récompenses
* **Envoyer des notifications multicanaux** : diffusez des messages via in-app, par e-mail et push à des étapes clés.
* **Suivi des performances** : surveillez-les au moyen de parcours générés automatiquement et de rapports intégrés

## Fonctionnement {#how-it-works-overview}

Le workflow suivant permet de créer un défi de fidélité :

1. **Configurer l’ingestion des données** - Configurer les connecteurs source pour effectuer le suivi des actions des clients
2. **Créer un défi** - Définissez le type, l’audience et les dates
3. **Ajouter des tâches** - Configuration des actions et des récompenses
4. **Conception de contenu** - Créez des cartes de contenu et des messages facultatifs
5. **Publication** - Journey Optimizer génère et active automatiquement un parcours
6. **Surveiller** - Suivre la participation et les performances

>[!NOTE]
>
>Le parcours généré automatiquement apparaît dans votre inventaire de parcours et peut être personnalisé si nécessaire. Toutefois, les modifications apportées directement au parcours ne sont pas resynchronisées avec la configuration de défi.

## Conditions préalables {#prerequisites-overview}

Avant d’utiliser les défis de fidélité :

* Configurez les connecteurs source Experience Platform (par exemple, Capillaire) pour ingérer les données d’événement de fidélité
* Vérifiez que vous disposez des autorisations appropriées dans Journey Optimizer
* Création d’audiences cibles dans Experience Platform

Pour obtenir des conditions préalables détaillées, voir [Présentation des défis de fidélité](get-started.md#prerequisites).

## Limites importantes {#limitations-overview}

* **Aucun système comptable** : Loyalty Challenges ne suit pas les valeurs monétaires ou les soldes en points. Journey Optimizer appelle votre système de gestion de la fidélité externe pour gérer l’affectation de points.
* **Sélection d’audience uniquement** : vous pouvez sélectionner des audiences existantes, mais ne pouvez pas créer de nouvelles audiences à partir de l’interface utilisateur des défis de fidélité.

## Étapes suivantes {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="get-started.md">
    <img alt="Comprendre" src="../assets/do-not-localize/learn-more-button.svg">
    </a>
    <div>
    <a href="get-started.md"><strong>Comprendre les défis de fidélité</strong></a>
    </div>
    <p>
    <em>En savoir plus sur les fonctionnalités, le workflow et les fonctions</em>
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
