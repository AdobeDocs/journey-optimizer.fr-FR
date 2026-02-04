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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 1%

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

La création et le lancement d’un défi de fidélité suivent ce workflow :

1. **[Créer le défi](#create-the-challenge)** - Choisissez le type de défi (Standard, Streak ou Séquentiel) qui correspond le mieux aux objectifs de votre programme de fidélité.

1. **[Configurer la structure du défi](#structure)** - Définissez les propriétés du défi, le planning, les tâches que les clients doivent effectuer et les récompenses qu’ils vont gagner.

1. **[Configurer des cartes de contenu](#configure-content-cards)** - Concevez des cartes de contenu pour représenter visuellement votre défi sur les appareils des clients, en affichant les informations sur le défi, la progression et les récompenses.

1. **[Configurer la messagerie](#configure-messaging)** (facultatif) - Configurez des messages multicanaux (in-app, e-mail, push) pour les étapes clés : lancement, en cours et achèvement.

1. **[Sélectionner l’audience du défi](#audience)** - Définir quels clients sont éligibles pour participer au défi.

1. **[Générer et activer le parcours](#review-and-publish)** - Générez le parcours associé et activez-le pour mettre le défi à la disposition de votre audience cible.

## Créer le défi {#create-the-challenge}

1. Accédez à **[!UICONTROL Défis de fidélité (Beta)]** dans Journey Optimizer.

1. Sélectionnez l’onglet **[!UICONTROL Défis]** et sélectionnez **[!UICONTROL Créer un défi]**.

   ![](assets/challenge-create.png)

1. Choisissez le type de défi :

   * **[!UICONTROL Standard]** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre
   * **[!UICONTROL Streak]** : les clients effectuent la même tâche plusieurs fois de suite
   * **[!UICONTROL Séquentiel]** : les clients exécutent des tâches dans un ordre défini

## Configurer la structure de défi {#structure}

C’est dans l’onglet Structure que vous définissez l’organisation de votre défi : ses propriétés, son planning, les tâches à effectuer et les récompenses à accorder.

### Définir les propriétés du défi et utiliser des métadonnées personnalisées {#properties}

1. Dans le volet Propriétés du défi , configurez les propriétés du défi :

   ![](assets/challenge-create-properties.png)

   **Nom** : saisissez un nom explicite pour votre défi. Ce nom apparaît dans l’inventaire des défis et vous aide à identifier le défi.

   **Description** : saisissez une description pour votre défi.

1. Utilisez la section **[!UICONTROL Métadonnées personnalisées]** pour ajouter des métadonnées personnalisées à l’aide de paires clé/valeur. Ces métadonnées peuvent être utilisées pour le suivi, la segmentation ou l’intégration à des systèmes externes.

### Planifier le défi {#schedule}

Planifiez le défi en sélectionnant l’icône ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Ouvrir le planning]**.

* **Date et heure de début** : indiquez le moment où le défi sera disponible pour les clients (format : jj/mm/aaaa, — : matin/après-midi).

* **Date et heure de fin** : indiquez le moment où le défi expire et où vous n’acceptez plus de nouvelles formations (format : mm/jj/aaaa, —:— matin/après-midi).

* **Fuseau horaire** : le défi utilise par défaut le fuseau horaire local du destinataire.

* **Les tâches doivent être terminées** : choisissez le moment où les clients peuvent terminer les tâches :

   * **[!UICONTROL À tout moment pendant le défi]** : les clients peuvent terminer des tâches à tout moment entre les dates de début et de fin du défi
   * **[!UICONTROL À des heures spécifiques de la journée]** : limitez la fin de la tâche à des heures quotidiennes spécifiques en définissant les paramètres **[!UICONTROL Heure de début]** et **[!UICONTROL Heure de fin]**

Le planning du défi est maintenant configuré. Vous pouvez maintenant ajouter les tâches que les clients doivent effectuer.

### Ajouter des tâches {#add-tasks}

Les tâches définissent les actions ou jalons spécifiques que les clients doivent effectuer pour gagner des récompenses. Vous configurez les types de tâches (achat, dépenses, visite, engagement, événements personnalisés), les quantités, les filtres de produit et les récompenses.

Selon votre type de défi, les clients exécutent les tâches différemment :

* **Défis standard** : effectuez le nombre spécifié de tâches dans n’importe quel ordre
* **Défis de Streak** : effectuez la même tâche plusieurs fois de suite
* **Défis séquentiels** : exécutez les tâches dans un ordre défini

Pour ajouter des tâches à votre défi, procédez comme suit :

1. Dans la section **[!UICONTROL Tâches]**, sélectionnez **[!UICONTROL Ajouter une tâche]**.

   ![](assets/challenge-create-add-task.png)

1. L’inventaire des tâches s’ouvre. Sélectionnez une ou plusieurs tâches dans la liste, puis sélectionnez **[!UICONTROL Ajouter]**. Pour créer une nouvelle tâche, sélectionnez **[!UICONTROL Nouveau]**.

   Pour obtenir des instructions détaillées sur la création et la configuration de tâches, voir [Créer des tâches](create-tasks.md).

1. Dans la section **[!UICONTROL Exigence d’achèvement de la tâche]**, indiquez à quel moment le défi doit être considéré comme terminé :

   * **[!UICONTROL Le client choisit 1 tâche à effectuer]** : Le client peut sélectionner et exécuter n’importe quelle tâche du défi pour gagner des récompenses
   * **[!UICONTROL Le client effectue un nombre spécifique de tâches]** : Le client doit effectuer un nombre défini de tâches. Saisissez le nombre requis de tâches terminées.

1. Par défaut, les défis permettent aux clients d’effectuer des tâches sur plusieurs transactions. Pour exiger que toutes les tâches soient effectuées dans une seule transaction, sélectionnez l’icône ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Paramètres]** et activez/désactivez l’option **[!UICONTROL Une seule transaction]**.

   ![](assets/challenge-create-single-transaction.png)

### Configurer les récompenses {#rewards}

Les récompenses sont les points de fidélité ou les avantages que les clients reçoivent pour relever les défis. Configurez comment et quand les récompenses sont distribuées pour motiver la participation du client.

1. Dans le menu déroulant **[!UICONTROL Diffusion de récompenses]**, choisissez quand les récompenses doivent être diffusées :

   * **[!UICONTROL Remettre des récompenses lorsque le défi est terminé]** : récompensez toutes les récompenses lorsque le client termine l’ensemble du défi
   * **[!UICONTROL Offrir des récompenses aux jalons d’achèvement de tâche au fur et à mesure de la progression du défi]** : récompensez de manière incrémentielle les clients qui effectuent des tâches individuelles (uniquement disponible lorsque le défi nécessite l’accomplissement de plusieurs tâches)

1. Sélectionnez votre fournisseur de récompense dans la liste déroulante. Il s’agit de votre solution de fidélité qui gère les points et les récompenses des clients.

1. Configurez les montants de récompense en fonction de la méthode de diffusion sélectionnée :

   +++Diffuser des récompenses lorsque le défi est terminé

   Dans le champ **Nombre de [points de fidélité] à l’issue du défi**, indiquez le montant total de récompense à accorder lorsque le client termine l’ensemble du défi.

   Le nom du champ affiche le nom de vos points de fidélité tel que défini dans le fournisseur sélectionné. Par exemple, si votre fournisseur utilise « Points Luma », le champ affiche « Nombre de points Luma à l’issue du défi ».

   ![](assets/challenge-create-reward-total.png)

   **Exemple** : dans la capture d’écran ci-dessus, les clients reçoivent 100 points pour relever le défi.

   +++

   +++Diffuser des récompenses aux jalons d’achèvement de la tâche

   Spécifiez les montants de récompense pour les jalons d’achèvement de la tâche. Cette option vous permet de créer des récompenses progressives qui augmentent la motivation du client au fur et à mesure qu’il relève le défi.

   Pour toute tâche pour laquelle vous souhaitez offrir une récompense, activez l’option Récompense et indiquez le nombre de points à accorder lorsque les clients effectuent cette tâche spécifique. Vous pouvez choisir de ne récompenser que certaines tâches terminées ; par exemple, si vous avez 10 tâches, vous pouvez récompenser uniquement les tâches 1, 5 et 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Exemple** : dans la capture d’écran ci-dessus, les clients obtiennent 10 points lorsqu’ils terminent la première tâche, puis 50 points supplémentaires après avoir terminé la seconde tâche, pour un total de 60 points lorsque le défi est terminé.

   >[!TIP]
   >
   >Envisagez d’augmenter les valeurs de récompense pour les tâches ultérieures afin de maintenir l’engagement client tout au long du défi.

   +++

La structure de défi est désormais configurée avec des tâches et des récompenses. Vous pouvez maintenant concevoir les cartes de contenu pour présenter le défi aux clients.

## Configuration des cartes de contenu {#configure-content-cards}

Les cartes de contenu fournissent la représentation visuelle de votre défi sur les appareils des clients, affichant les informations sur le défi, la progression et les récompenses. En savoir plus sur les [cartes de contenu](../content-card/create-content-card.md).

Pour configurer les cartes de contenu en fonction de votre défi :

1. Dans l’éditeur de défis, accédez à l’onglet **[!UICONTROL Contenu]**.

1. Saisissez un **[!UICONTROL Nom]** pour la carte de contenu.

1. Sélectionnez la **[!UICONTROL configuration du canal]** associée. Les configurations de canal définissent comment et où votre contenu est diffusé aux clients. Pour plus d’informations, voir [Configurations de canal](../configuration/channel-surfaces.md).

1. Sélectionnez **[!UICONTROL Modifier le contenu]** pour concevoir votre carte de contenu.

   ![](assets/challenge-create-content.png)

Pour plus d’informations sur la conception et la personnalisation des cartes de contenu, voir [Conception de cartes de contenu](../content-card/design-content-card.md).

La carte de contenu est maintenant configurée. Vous pouvez désormais configurer la messagerie pour impliquer les clients tout au long du cycle de vie du défi.

### Configurer la messagerie {#configure-messaging}

Configurez des messages multicanaux pour impliquer les clients aux étapes clés du cycle de vie du défi.

1. Accédez à l’onglet **[!UICONTROL Messagerie]**.

1. Configurez les messages pour chaque étape du cycle de vie :

   ![](assets/challenge-create-messaging.png)

   * **Messages Launch** : avertissez les clients lorsque le défi commence et fournissez les détails initiaux
   * **Messages en cours** : maintenez l’engagement des clients pendant le défi avec des rappels, des mises à jour sur la progression et des encouragements pour continuer
   * **Messages d’achèvement** : célébrez le succès, confirmez l’attribution de récompenses et suggérez les prochains défis ou actions

1. Pour chaque étape, sélectionnez **[!UICONTROL Ajouter *étape* message]** pour créer un message pour cette étape.

1. Choisissez le canal de votre choix : **[!UICONTROL In-app]**, **[!UICONTROL Email]** ou **[!UICONTROL Notification push]** et sélectionnez la configuration de canal associée.

1. Sélectionnez l’icône ![](assets/do-not-localize/Smock_More_18_N.svg) et choisissez **[!UICONTROL Modifier]** pour concevoir le contenu de votre message.

   Pour plus d’informations sur la création de messages pour des canaux spécifiques, voir :

   * [Documentation sur les messages in-app](../in-app/get-started-in-app.md)
   * [Documentation sur les e-mails](../email/get-started-email.md)
   * [Documentation sur les notifications push](../push/get-started-push.md)

1. Répétez ces étapes pour chaque étape et canal selon les besoins.

La configuration de la messagerie est maintenant terminée. Vous pouvez maintenant définir les clients éligibles pour participer au défi.

## Sélectionner l’audience du défi {#audience}

Définissez les clients éligibles pour participer à votre défi de fidélité.

1. Accédez à l’onglet **[!UICONTROL Audience]** et cliquez sur le bouton **[!UICONTROL Sélectionner une audience]**.

   ![](assets/challenge-create-audience.png)

1. Toutes les audiences Adobe Experience Platform disponibles s’affichent. Sélectionnez l’audience souhaitée dans la liste.

1. Sélectionnez **[!UICONTROL Ajouter une audience]** pour confirmer votre sélection.

Votre configuration de défi est maintenant terminée. Vous pouvez maintenant générer le parcours qui orchestre la diffusion de défi.

## Génération et activation du parcours {#review-and-publish}

Une fois la configuration de votre défi terminée, générez le parcours associé qui orchestrera la diffusion du défi et les interactions des clients. Pour ce faire, sélectionnez **[!UICONTROL Générer le Parcours]**.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer crée automatiquement un parcours [](../building-journeys/journey-gs.md) au statut Brouillon . Le parcours généré automatiquement apparaît dans votre inventaire de parcours avec le format de nom « Défi : [Nom du défi] ».

Vérifiez la configuration du parcours si nécessaire, puis [activez le parcours ](../building-journeys/publish-journey.md) pour mettre le défi à la disposition des clients.

Le parcours démarrera automatiquement à la date de début du défi que vous avez spécifiée et diffusera le contenu et les messages en fonction de votre configuration.

>[!NOTE]
>
>Le parcours généré automatiquement peut être personnalisé si nécessaire pour ajouter une logique ou un message supplémentaire. Toutefois, les modifications apportées directement au parcours ne sont pas resynchronisées avec la configuration de défi. Si vous modifiez le défi ultérieurement, toutes les personnalisations de parcours seront perdues lorsque le parcours sera régénéré.

## Étapes suivantes {#next-steps}

* [Gérer les défis](manage-challenges.md) - Découvrez comment modifier, surveiller et optimiser les défis
* [Comprendre les défis de la fidélité](get-started.md) - Examinez les fonctionnalités et capacités
