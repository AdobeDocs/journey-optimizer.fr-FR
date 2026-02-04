---
solution: Journey Optimizer
product: journey optimizer
title: Créer des défis de fidélité
description: Découvrez comment créer et configurer des défis de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: 5120eb51311348b8561b0a20f982576f6c945921
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 2%

---


# Créer des défis {#create-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité](access-loyalty-challenges.md) - Inventaire et filtrage
* **Créer des défis** ◀︎ **Vous êtes ici** - Créez et configurez des défis
* [Créer des tâches](create-tasks.md) - Définir des tâches de défi
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Fonctionnement {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

La création et le lancement d’un défi de fidélité suivent ce workflow :

1. **Créer un défi** - Définissez les propriétés de base du défi, y compris le nom, le type (Standard, Streak ou Séquentiel), l’audience et la période.

1. **Ajouter des tâches** - Définissez les actions spécifiques que les clients doivent effectuer, y compris les types de tâches (achat, dépenses, visite, etc.), les quantités, les filtres de produit et les récompenses.

1. **Conception de cartes de contenu** - Créez la représentation visuelle de votre défi à l’aide de cartes de contenu Journey Optimizer qui s’affichent sur les appareils des clients.

1. **Configurer la messagerie** (facultatif) - Configurez des messages multicanaux (in-app, e-mail, push, SMS) pour les étapes clés : lancement, en cours et achèvement.

1. **Réviser et publier** - Testez votre défi avec des profils de test, puis publiez-le pour le rendre disponible auprès de votre audience cible.

## Créer le défi {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

Pour créer un nouveau défi de fidélité :

1. Accédez à **[!UICONTROL Défis de fidélité]** dans Journey Optimizer.

1. Sélectionnez l’onglet **[!UICONTROL Défis]**.

1. Sélectionnez **[!UICONTROL Créer un défi]**.

1. Configurez les propriétés du défi :

   **Nom du défi** : saisissez un nom explicite pour votre défi. Ce nom apparaît dans l’inventaire des défis et vous aide à identifier le défi.

   **Type de défi** : sélectionnez l’un des types suivants :
   * **[!UICONTROL Standard]** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre
   * **[!UICONTROL Streak]** : les clients effectuent la même tâche plusieurs fois de suite
   * **[!UICONTROL Séquentiel]** : les clients exécutent des tâches dans un ordre défini

   **Audience cible** : sélectionnez le segment d’audience qui définit les personnes pouvant participer à ce défi. Vous devez créer des audiences dans Experience Platform avant de créer des défis. Pour plus d’informations, voir [Prise en main des audiences](../audience/about-audiences.md).

   **Date de début** : définie au moment où le défi devient disponible pour les clients.

   **Date de fin** : définie lorsque le défi expire et n’accepte plus de nouvelles fins de cours.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### Ajouter des tâches {#add-tasks}

Les tâches définissent les actions ou jalons spécifiques que les clients doivent effectuer pour gagner des récompenses. Vous configurez les types de tâches (achat, dépenses, visite, engagement, événements personnalisés), les quantités, les filtres de produit et les récompenses.

Selon votre type de défi, les clients exécutent les tâches différemment :

* **Défis standard** : effectuez le nombre spécifié de tâches dans n’importe quel ordre
* **Défis de Streak** : effectuez la même tâche plusieurs fois de suite
* **Défis séquentiels** : exécutez les tâches dans un ordre défini

Pour ajouter des tâches à votre défi, sélectionnez **[!UICONTROL Ajouter une tâche]** dans la section Tâches et configurez les propriétés de la tâche.

Pour obtenir des instructions détaillées sur la création et la configuration de tâches, voir [Créer des tâches](create-tasks.md).

### Configuration des cartes de contenu {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

Les cartes de contenu fournissent la représentation visuelle de votre défi sur les appareils des clients, affichant les informations sur le défi, la progression et les récompenses. En savoir plus sur les [cartes de contenu](../content-card/create-content-card.md).

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

Pour configurer les cartes de contenu en fonction de votre défi :

1. Dans l’éditeur de défis, accédez à la section **[!UICONTROL Cartes de contenu]**.

1. Sélectionnez **[!UICONTROL Créer une carte de contenu]** ou choisissez un modèle existant.

1. Concevez votre carte de contenu :
   * Ajouter des images, du texte et des éléments de branding
   * Incluez [&#x200B; jetons de personnalisation &#x200B;](../personalization/personalization-syntax.md) pour afficher les informations spécifiques au client ou à la cliente
   * Afficher les indicateurs de progression des défis
   * Afficher les récompenses et les incentives

1. Configurez le moment où la carte de contenu s’affiche :
   * **Début du défi** : afficher le moment où le défi est disponible
   * **En cours** : afficher lorsque les clients participent activement
   * **Achèvement** : afficher une fois que les clients ont terminé toutes les tâches

1. Prévisualisez la carte de contenu sur différents appareils pour garantir un affichage correct.

1. Enregistrez la configuration de la carte de contenu.

Pour plus d’informations sur la conception et la personnalisation des cartes de contenu, voir [Conception de cartes de contenu](../content-card/design-content-card.md).

### Configurer la messagerie {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

Configurez des messages multicanaux pour impliquer les clients aux étapes clés du cycle de vie du défi.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

Pour configurer la messagerie en fonction de votre défi :

1. Dans l’éditeur de défis, accédez à la section **[!UICONTROL Messagerie]**.

1. Configurez les messages pour chaque étape du cycle de vie :

   **Messages Launch** - Avertissez les clients lorsque le défi commence :
   * Sélectionnez les canaux : [in-app](../in-app/get-started-in-app.md), [e-mail](../email/get-started-email.md), [notification push](../push/get-started-push.md) ou [SMS](../sms/get-started-sms.md)
   * Concevoir le message avec des détails de défi et call-to-action
   * Définir le timing : envoyer immédiatement lorsque le défi est lancé ou planifié pour une heure spécifique

   **Messages en cours** - Maintenez l’engagement des clients pendant le défi :
   * Définir des conditions de déclenchement (par exemple, 50 % d’achèvement, tâche spécifique terminée)
   * Créer des messages de rappel pour encourager la participation continue
   * Inclure les mises à jour de progression et les étapes suivantes

   **Messages d’achèvement** - Célébrez le succès et offrez des récompenses :
   * Félicitez les clients d’avoir relevé ce défi
   * Confirmer l’attribution de la récompense
   * Fournir des instructions pour la demande de récompenses
   * Proposer les prochains défis ou actions

Pour plus d’informations sur la création de messages pour des canaux spécifiques, voir :

* [Documentation sur les messages in-app](../in-app/get-started-in-app.md)
* [Documentation sur les e-mails](../email/get-started-email.md)
* [Documentation sur les notifications push](../push/get-started-push.md)
* [Documentation sur les messages SMS](../sms/get-started-sms.md)

## Examiner et publier le défi {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

Avant de publier votre défi :

1. **Examiner tous les composants** : vérifier les propriétés du défi, les tâches, les récompenses, les cartes de contenu et les configurations de messagerie.

1. **Tester l’expérience** : utilisez des [profils de test](../content-management/test-profiles.md) pour valider l’affichage de la carte de contenu et le comportement du déclencheur de tâche.

1. **Publier** : sélectionnez **[!UICONTROL Publier]** pour que le défi soit disponible pour votre audience cible.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

Lorsque vous publiez un défi, Journey Optimizer crée automatiquement un parcours [&#128279;](../building-journeys/journey-gs.md) au statut Brouillon . Le parcours généré automatiquement apparaît dans votre inventaire de parcours avec le format de nom « Défi : [Nom du défi] ».

Pour mettre le défi à la disposition des clients :

1. Accédez à l’inventaire **[!UICONTROL Parcours]** dans Journey Optimizer.

1. Recherchez le parcours généré automatiquement (son nom contiendra le préfixe « Défi : »).

1. [&#x200B; Activer le parcours &#x200B;](../building-journeys/publish-journey.md).

Le parcours démarre automatiquement à la date de début du défi que vous avez spécifiée.

>[!NOTE]
>
>Le parcours généré automatiquement apparaît dans votre inventaire de parcours et peut être personnalisé si nécessaire. Toutefois, les modifications apportées directement au parcours ne sont pas resynchronisées avec la configuration de défi.

## Étapes suivantes {#next-steps}

* [Gérer les défis](manage-challenges.md) - Découvrez comment modifier, surveiller et optimiser les défis
* [Comprendre les défis de la fidélité](get-started.md) - Examinez les fonctionnalités et capacités

