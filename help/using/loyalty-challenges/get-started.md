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
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
source-git-commit: 17d7cf7ae18ff987b7a9c9bebdec44b354ed11da
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 2%

---

# Prise en main des défis de fidélité {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* **Prise en main des défis de fidélité** ◀︎ **Vous êtes ici**
* [Accéder aux défis et aux tâches et les gérer](access-loyalty-challenges.md)
* [Créer des défis](create-challenges.md)
* [Création de tâches](create-tasks.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **privée**. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Vue d’ensemble {#overview}

Les défis de fidélité vous permettent de créer des programmes de fidélité attrayants et ludiques qui stimulent le comportement des clients et approfondissent les relations de la marque. Créez des défis qui récompensent les clients pour des actions spécifiques, qu’il s’agisse d’acheter ou de rédiger des avis, de communiquer sur les médias sociaux ou de recommander des amis.

Grâce aux défis de fidélité, vous pouvez :

* **Concevez des types de défis flexibles** : créez des défis standard, en série ou séquentiels pour répondre aux objectifs de votre entreprise
* **Configurer les récompenses de manière stratégique** : attribuez des points aux jalons de la tâche ou à l’achèvement complet pour maintenir l’engagement
* **Personnaliser l’expérience** : utilisez des cartes de contenu et la messagerie multicanale pour créer des expériences immersives de marque
* **Intégration transparente** : entrez en contact avec vos fournisseurs de fidélité existants et exploitez les données Experience Platform
* **Suivi automatique** : surveiller les progrès des clients par le biais de parcours générés automatiquement sans développement personnalisé

![](assets/challenges-gs.png)

Vous pouvez créer trois types d’expériences de défi :

* **Défis standard** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre. Utilisez ce type lorsque vous souhaitez de la flexibilité et que vous souhaitez terminer plusieurs chemins d’accès.\
  *Exemple : « Summer Wellness Challenge » - Effectuez 3 des 5 tâches suivantes : acheter des produits de santé, partager sur les médias sociaux, recommander un ami, écrire un commentaire ou assister à un événement virtuel*

* **Défis de Streak** : les clients effectuent la même tâche plusieurs fois de suite. Utilisez ce type pour encourager un comportement cohérent et répété au fil du temps.\
  *Exemple : « Semaine des amoureux du café » - Achetez des produits de café pendant 7 jours consécutifs pour débloquer une récompense de boisson gratuite*

* **Défis séquentiels** : les clients exécutent des tâches dans un ordre défini. Utilisez ce type pour guider les clients tout au long d’un processus d’intégration ou de parcours spécifique.\
  *Exemple : « Nouveau Parcours membre » - Inscrivez-vous aux e-mails → Effectuez votre premier achat → Rédiger un avis sur le produit → Recommander un ami (dans cet ordre exact)*

## Fonctionnement {#how-it-works}

La création et le lancement d’un défi de fidélité suivent ce workflow :

1. **Créer un défi** - Définissez les propriétés de base du défi, y compris le nom, le type (Standard, Streak ou Séquentiel) et la période.

1. **Ajouter des tâches** - Définissez les actions spécifiques que les clients doivent effectuer, y compris les types de tâches (achat, dépenses), les quantités, les filtres de produit et les récompenses.

1. **Conception de cartes de contenu** - Créez la représentation visuelle de votre défi à l’aide de cartes de contenu Journey Optimizer qui s’affichent sur les appareils des clients. Les cartes de contenu affichent les informations sur le défi, la progression et les récompenses.

1. **Configurer la messagerie** (facultatif) - Configurez des messages multicanaux (in-app, e-mail, push) pour les étapes clés du cycle de vie : lancement, en cours et achèvement.

1. **Sélectionner une audience cible** - Définissez quels clients peuvent participer à votre défi en sélectionnant une audience depuis Adobe Experience Platform.

1. **Lancer le défi** - Publiez le défi, puis générez un parcours. Journey Optimizer crée automatiquement le parcours pour votre défi. Publiez le parcours généré automatiquement pour mettre le défi à la disposition des clients.

Pour obtenir des instructions détaillées, voir [Créer des défis](create-challenges.md).

## Conditions préalables {#prerequisites}

Avant d’utiliser les défis de fidélité, vérifiez que vous disposez des éléments suivants :

+++Autorisations nécessaires

Pour utiliser les défis de fidélité, vous avez besoin des autorisations appropriées dans Journey Optimizer et Adobe Experience Platform.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

Contactez votre administrateur si vous ne pouvez pas accéder à la fonctionnalité ou si vous avez besoin d’autorisations supplémentaires.

+++

+++Audience cible

Assurez-vous que l’audience cible dont vous avez besoin existe dans Adobe Experience Platform avant de créer votre défi. Lors de la configuration du défi, vous sélectionnerez l’audience qui définit les clients éligibles à participer. [Découvrez comment utiliser les audiences](../audience/about-audiences.md).

+++

## Explorons plus en détail. {#lets-dive-deeper}

Maintenant que vous connaissez les défis de fidélité et leur fonctionnement, il est temps d’entrer dans les détails. Explorez les rubriques suivantes pour accéder à l’interface, créer votre premier défi et définir les tâches que vos clients effectueront.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="Accès" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Accéder aux défis et aux tâches et les gérer</strong></a>
    </div>
    <p>
    <em>Découvrez comment accéder à l’inventaire et gérer les défis et les tâches</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Créer" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong>Créer des défis</strong></a>
    </div>
    <p>
    <em>Découvrez comment créer et configurer votre premier défi de fidélité</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="Tâches" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>Créer des tâches</strong></a>
    </div>
    <p>
    <em>Découvrez comment définir les tâches que les clients effectuent pour relever les défis</em>
    </p>
  </td>
</tr>
</table>
