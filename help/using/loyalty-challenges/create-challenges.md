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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 1%

---


# Créer des défis {#create-challenges}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md) - Présentation, workflow, conditions préalables
* [Accéder aux défis de fidélité et les gérer](access-loyalty-challenges.md) - Inventaire, défis et gestion des tâches
* **Créer des défis** ◀︎ **Vous êtes ici** - Créez et configurez des défis
* [Créer des tâches](create-tasks.md) - Définir des tâches de défi

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

## Créer le défi {#create-the-challenge}

1. Accédez à **[!UICONTROL Défis de fidélité (Beta)]** dans Journey Optimizer.

1. Sélectionnez l’onglet **[!UICONTROL Défis]** et sélectionnez **[!UICONTROL Créer un défi]**.

   ![](assets/challenge-create.png)

1. Choisissez le type de défi :

   * **[!UICONTROL Standard]** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre\
     *Exemple : effectuez 3 des 5 tâches disponibles*

   * **[!UICONTROL Streak]** : les clients effectuent la même tâche plusieurs fois de suite\
     *Exemple : effectuez un achat sur 7 jours consécutifs*

   * **[!UICONTROL Séquentiel]** : les clients exécutent des tâches dans un ordre défini\
     *Exemple : achat → révision → partage (doit être effectué dans cet ordre)*

## Configurer la structure de défi {#structure}

Dans l’onglet **[!UICONTROL Structure]**, définissez l’organisation de votre défi : ses propriétés, son planning, les tâches à effectuer et les récompenses à diffuser.

### Définir les propriétés du défi et utiliser des métadonnées personnalisées {#properties}

1. Dans le volet **[!UICONTROL Propriétés du défi]**, définissez les paramètres globaux du défi :

   * **[!UICONTROL Nom]** : saisissez un nom explicite pour votre défi. Ce nom apparaît dans l’inventaire des défis.
   * **[!UICONTROL Description]** : saisissez une description qui explique l’objectif et les objectifs du défi.

   ![](assets/challenge-create-properties.png)

1. Utilisez la section **[!UICONTROL Métadonnées personnalisées]** pour ajouter des métadonnées personnalisées à l’aide de paires clé/valeur. Ces métadonnées peuvent être utilisées pour le suivi ou l’intégration à des systèmes externes.

### Planifier le défi {#schedule}

Configurez le moment où votre défi s’exécute en sélectionnant l’icône ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Ouvrir le planning]** :

![](assets/challenge-create-properties.png)

* **[!UICONTROL Date et heure de début]** : à définir lorsque le défi est disponible pour les clients.
* **[!UICONTROL Date et heure de fin]** : défini lorsque le défi expire et n’accepte plus de nouvelles tâches terminées.
   * **[!UICONTROL Fuseau horaire]** : le défi utilise par défaut le fuseau horaire local du destinataire.
* **[!UICONTROL Les tâches doivent être terminées]** : choisissez le moment où les clients peuvent terminer les tâches :

   * **[!UICONTROL À tout moment pendant le défi]** : les clients peuvent effectuer des tâches à tout moment entre les dates de début et de fin du défi.
   * **[!UICONTROL À des heures spécifiques de la journée]** : limitez la fin de la tâche à des heures quotidiennes spécifiques en définissant les paramètres **[!UICONTROL Heure de début]** et **[!UICONTROL Heure de fin]**.

Le planning du défi est maintenant configuré. Ajoutez ensuite les tâches que les clients doivent effectuer.

### Ajouter des tâches {#add-tasks}

Les tâches définissent les actions spécifiques que les clients doivent effectuer pour gagner des récompenses. Vous pouvez configurer les types de tâches (achat, dépenses), les quantités, les filtres de produit et d’autres attributs.

Selon votre type de défi, les clients exécutent les tâches différemment :

* **Défis standard** : effectuez le nombre spécifié de tâches dans n’importe quel ordre\
  *Exemple : effectuez 3 tâches sur 5 - effectuez un achat, rédigez une évaluation, recommandez un ami, partagez sur les médias sociaux ou mettez à jour un profil*

* **Défis de Streak** : effectuez la même tâche plusieurs fois de suite\
  *Exemple : effectuez un achat pendant 7 jours consécutifs pour gagner des primes*

* **Défis séquentiels** : exécutez les tâches dans un ordre défini\
  *Exemple : effectuez d’abord un achat, puis rédigez une révision, puis partagez-la sur les médias sociaux. Les tâches doivent être effectuées dans cet ordre exact*

Pour ajouter des tâches à votre défi, procédez comme suit :

1. Dans la section **[!UICONTROL Tâches]**, sélectionnez **[!UICONTROL Ajouter une tâche]**.

   ![](assets/challenge-create-add-task.png)

1. L’**[!UICONTROL Inventaire des tâches]** s’ouvre. Sélectionnez une ou plusieurs tâches dans la liste, puis sélectionnez **[!UICONTROL Ajouter]**. Pour créer une nouvelle tâche, sélectionnez **[!UICONTROL Nouveau]**. [Découvrez comment créer et configurer des tâches](create-tasks.md).

1. Dans la section **[!UICONTROL Exigence d’achèvement de la tâche]**, indiquez à quel moment le défi est considéré comme terminé :

   * **[!UICONTROL Le client choisit 1 tâche à effectuer]** : les clients peuvent sélectionner et exécuter n’importe quelle tâche pour gagner des récompenses.
   * **[!UICONTROL Le client effectue un nombre spécifique de tâches]** : les clients doivent effectuer un nombre défini de tâches.

1. Par défaut, les défis permettent aux clients d’effectuer des tâches sur plusieurs transactions. Pour exiger que toutes les tâches soient effectuées dans une seule transaction, sélectionnez l’icône ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Paramètres]** et activez l’option ci-dessous.

   ![](assets/challenge-create-single-transaction.png)

Après avoir ajouté des tâches à votre défi, configurez les récompenses que les clients obtiendront pour les avoir effectuées.

### Configurer les récompenses {#rewards}

Les récompenses sont les points de fidélité ou les avantages que les clients reçoivent pour relever les défis. Configurez quand et comment les récompenses sont diffusées.

1. Dans le menu déroulant **[!UICONTROL Diffusion de récompenses]**, choisissez quand diffuser les récompenses :

   * **[!UICONTROL Remettre des récompenses lorsque le défi est terminé]** : récompensez les clients lorsqu’ils relèvent l’ensemble du défi\
     *Exemple : Attribuez 100 points après avoir effectué les 5 tâches*

   * **[!UICONTROL Offrir des récompenses aux jalons d’achèvement de tâche au fur et à mesure de la progression du défi]** : récompensez progressivement les clients lorsqu’ils effectuent des tâches individuelles (uniquement pour les défis nécessitant plus d’une tâche)\
     *Exemple : Attribuer 10 points après la tâche 1, 20 points après la tâche 2 et 50 points après la tâche 3*

1. Sélectionnez votre fournisseur de récompense. Il s’agit de votre solution de fidélité qui gère les points et les récompenses des clients.

1. Configurez les montants de récompense en fonction de la méthode de diffusion sélectionnée :

   +++Diffuser des récompenses lorsque le défi est terminé

   Spécifiez le montant total de récompense à accorder lorsque les clients relèvent l’ensemble du défi.

   ![](assets/challenge-create-reward-total.png)

   **Exemple** : les clients obtiennent 100 points pour relever le défi.

   +++

   +++Diffuser des récompenses aux jalons d’achèvement de la tâche

   Spécifiez les montants de récompense pour les jalons d’achèvement de la tâche. Cette option vous permet de créer des récompenses progressives qui augmentent la motivation du client au fur et à mesure qu’il relève le défi.

   Pour toute tâche pour laquelle vous souhaitez offrir une récompense, activez l’option Récompense et indiquez le nombre de points à accorder lorsque les clients effectuent cette tâche spécifique. Vous pouvez choisir de ne récompenser que certaines tâches terminées ; par exemple, si vous avez 10 tâches, vous pouvez récompenser uniquement les tâches 1, 5 et 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Exemple** : les clients obtiennent 10 points lorsqu’ils terminent la première tâche, puis 50 points supplémentaires après avoir terminé la deuxième tâche, pour un total de 60 points lorsque le défi est terminé.

   >[!TIP]
   >
   >Envisagez d’augmenter les valeurs de récompense pour les tâches ultérieures afin de maintenir l’engagement client tout au long du défi.

   +++

Après avoir configuré la structure du défi avec des tâches et des récompenses, concevez les cartes de contenu pour afficher le défi aux clients.

## Configuration des cartes de contenu {#configure-content-cards}

Les cartes de contenu représentent visuellement votre défi sur les appareils des clients, en affichant les informations sur le défi, la progression et les récompenses. [En savoir plus sur les cartes de contenu](../content-card/create-content-card.md).

Pour configurer les cartes de contenu en fonction de votre défi :

1. Accédez à l’onglet **[!UICONTROL Contenu]** et saisissez un **[!UICONTROL Nom]** pour la carte de contenu.

1. Sélectionnez la **[!UICONTROL Configuration du canal]**. Les configurations de canal contiennent tous les paramètres techniques relatifs à l’envoi de messages, tels que les paramètres d’en-tête, le sous-domaine, les applications mobiles, etc. [En savoir plus sur les configurations de canal](../configuration/channel-surfaces.md).

1. Sélectionnez **[!UICONTROL Modifier le contenu]** pour concevoir votre carte de contenu. [Découvrez comment concevoir et personnaliser des cartes de contenu](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Après avoir configuré la carte de contenu, configurez la messagerie pour impliquer les clients tout au long du cycle de vie du défi.

### Configurer la messagerie {#configure-messaging}

Configurez des messages multicanaux pour impliquer les clients aux étapes clés du cycle de vie du défi. La messagerie est facultative, mais recommandée pour optimiser l’engagement du client.

1. Accédez à l’onglet **[!UICONTROL Messagerie]** et configurez les messages pour chaque étape du cycle de vie :

   * Message **Launch** : avertissez les clients lorsque le défi commence
   * Message **En cours** : pour que les clients restent engagés dans les rappels et les mises à jour de progression
   * Message **Achèvement** : célébrer le succès et confirmer l’attribution de la récompense

1. Pour chaque étape, sélectionnez **[!UICONTROL Ajouter [étape] message]** (où [étape] représente le lancement, la progression ou la fin) pour créer un message pour cette étape.

1. Choisissez le canal de votre choix : **[!UICONTROL In-app]**, **[!UICONTROL Email]** ou **[!UICONTROL Notification push]** et sélectionnez la configuration de canal associée.

1. Sélectionnez l’icône ![](assets/do-not-localize/Smock_More_18_N.svg) et choisissez **[!UICONTROL Modifier]** pour concevoir le contenu de votre message.

   ![](assets/challenge-create-messaging.png)

Découvrez comment créer des messages pour des canaux spécifiques :

* [Messages in-app](../in-app/get-started-in-app.md)
* [Canal Email](../email/get-started-email.md)
* [Notifications push](../push/get-started-push.md)

Une fois la configuration de la messagerie terminée, définissez les clients éligibles pour participer au défi.

## Sélectionner l’audience du défi {#audience}

Définir quels clients peuvent participer à votre défi de fidélité.

1. Accédez à l’onglet **[!UICONTROL Audience]** et sélectionnez le bouton **[!UICONTROL Sélectionner une audience]**.

   ![](assets/challenge-create-audience.png)

1. Sélectionnez votre audience cible dans la liste des audiences Adobe Experience Platform disponibles. [Découvrez comment utiliser les audiences](../audience/about-audiences.md).

1. Sélectionnez **[!UICONTROL Ajouter une audience]**.

Votre défi est maintenant entièrement configuré avec sa structure, son contenu, sa messagerie et son audience cible. La dernière étape consiste à générer et publier le parcours.

## Générer et publier le parcours {#review-and-publish}

Générez le parcours qui orchestrera votre diffusion de défi et les interactions des clients. Pour ce faire, sélectionnez **[!UICONTROL Générer le Parcours]**.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer crée automatiquement un parcours [&#128279;](../building-journeys/journey-gs.md) au statut Brouillon . Le parcours généré automatiquement apparaît dans votre inventaire de parcours avec le format de nom « Défi : [Nom du défi] ».

![](assets/challenge-create-journey.png)

Passez en revue la configuration du parcours si nécessaire, puis publiez le parcours pour mettre le défi à la disposition des clients. [Découvrez comment publier un parcours &#x200B;](../building-journeys/publish-journey.md).

Le parcours démarrera automatiquement à la date de début du défi que vous avez spécifiée et diffusera le contenu et les messages en fonction de votre configuration.

>[!NOTE]
>
>Le parcours généré automatiquement peut être personnalisé pour ajouter une logique ou un message supplémentaire. Toutefois, les modifications apportées directement au parcours ne sont pas resynchronisées avec la configuration de défi. Si vous modifiez le défi ultérieurement, toutes les personnalisations de parcours seront perdues lorsque le parcours sera régénéré.
