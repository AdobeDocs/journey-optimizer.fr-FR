---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Action
description: Découvrez comment ajouter une activité Action générique pour configurer des actions uniques et des groupes d’actions entrants multi-actions dans la zone de travail de parcours et comment ajouter des actions de canal intégrées.
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: parcours, message, notification push, sms, e-mail, in-app, web, carte de contenu, expérience basée sur du code
exl-id: 0ed97ffa-8efc-45a2-99ae-7bcb872148d5
version: Journey Orchestration
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 86%

---

# Utiliser l’activité Action {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_action_activity"
>title="Activité Action"
>abstract="L’activité **Action** vous permet de configurer une action de canal native unique et plusieurs activités entrantes, tout en ajoutant une optimisation à toute action de canal intégrée."

[!DNL Journey Optimizer] est fourni avec une nouvelle activité **Action** générique qui permet de configurer une action de canal intégrée unique, ainsi que plusieurs activités entrantes.

L&#39;activité Action offre les avantages suivants :

* Configuration d’action native simplifiée dans la zone de travail de parcours
* Création de groupes d’actions entrantes multi-actions
* Ajout d’une optimisation à toute action de canal intégrée

Pour ajouter une action de canal intégrée à votre parcours, utilisez l’activité **Action**. Cette activité unifiée regroupe toutes les actions de canal (e-mail, notification push, SMS, in-app, web, expérience basée sur le code et carte de contenu) en un seul type d’activité, remplaçant les activités de canal individuelles précédentes.

>[!IMPORTANT]
>
>Tous les canaux natifs étant désormais accessibles par le biais de l’activité Action , les activités de canal natives héritées seront abandonnées avec la version de mars. Les parcours existants qui incluent des actions héritées continueront à fonctionner en l’état. Aucune migration n’est requise.

Vous pouvez également configurer des actions personnalisées pour envoyer vos messages dans [!DNL Journey Optimizer]. [En savoir plus](#recommendation)

## Ajouter une action de canal intégrée à un parcours  {#add-action}

Pour ajouter une action de canal intégrée à votre parcours à l’aide de l’activité **[!UICONTROL Action]**, procédez comme suit.

Pour plus d’informations sur les canaux disponibles dans les parcours, reportez-vous au tableau de cette section : [Canaux dans les parcours et les campagnes](../channels/gs-channels.md#channels).

1. Débutez votre parcours avec une activité [Événement](general-events.md) ou [Lecture d’audience](read-audience.md).

1. Dans la section **[!UICONTROL Actions]** de la palette, placez une activité **[!UICONTROL Action]** dans la zone de travail.

1. Sélectionnez l’activité de canal intégrée que vous souhaitez utiliser dans votre parcours.

   ![Liste déroulante Type d’action affichant l’action du canal et les options d’action personnalisée](assets/journey-action-type-cbe.png)

1. Ajoutez un libellé à votre action et sélectionnez **[!UICONTROL Configurer l’action]**.

   ![Volet de configuration de l’activité d’action avec les champs de libellé et de description](assets/journey-action-configure.png){width="80%"}

1. Vous accédez à l’onglet **[!UICONTROL Actions]** de l’écran de configuration de l’action de parcours.

   Sélectionnez la configuration à utiliser pour le canal sélectionné.

   ![Onglet Actions du menu Administration affichant les actions personnalisées et Adobe](assets/journey-action-actions-tab.png)

1. Si vous avez sélectionné un canal entrant, vous pouvez ajouter plusieurs actions. [En savoir plus](#multi-action)

1. Configurez votre activité en fonction du canal sélectionné. Des instructions de configuration détaillées sont disponibles dans les liens ci-dessous.

   * Découvrez ci-dessous les étapes détaillées pour créer votre action sortante :

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="Lead" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong>Créer des e-mails</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="Peu fréquent" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong>Créer des notifications push<strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="Validation" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong>Créer des messages texte (SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * Découvrez ci-dessous les étapes détaillées pour créer votre action entrante :

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>Créer des messages in-app</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="Lead" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>Créer des expériences web</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="Lead" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>Créer des cartes de contenu</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="Peu fréquent" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>Créer des expériences basées sur le code<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   >[!NOTE]
   >
   >* Chaque action d’expérience entrante est fournie avec une activité **Attente** de 3 jours. [En savoir plus](wait-activity.md#auto-wait-node)
   >
   >* Pour les notifications push et les e-mails, vous pouvez activer l’optimisation de l’heure d’envoi. [En savoir plus](send-time-optimization.md)

1. Selon l’activité, vous pouvez afficher des paramètres avancés spécifiques au canal sélectionné et remplacer certaines valeurs par défaut telles que l’adresse d’exécution. [En savoir plus](about-journey-activities.md#advanced-parameters)

   >[!NOTE]
   >
   >Si les paramètres avancés sont masqués, cliquez sur le bouton **[!UICONTROL Afficher les champs en lecture seule]** en haut du volet de droite.

1. Utilisez la section **[!UICONTROL Optimisation]** pour exécuter des expériences de contenu, tirer parti des règles de ciblage ou utiliser des combinaisons avancées d’expérimentation et de ciblage.

   Ces différentes options et les étapes à suivre sont présentées dans [cette section](../content-management/gs-message-optimization.md).

1. Utilisez la section **[!UICONTROL Langues]** pour créer du contenu dans plusieurs langues au sein de votre action de parcours. Pour ce faire, cliquez sur le bouton **[!UICONTROL Ajouter des langues]** et sélectionnez les **[!UICONTROL paramètres de langue]** souhaités.

   Vous trouverez des informations détaillées sur la configuration et l’utilisation des fonctionnalités multilingues dans [cette section](../content-management/multilingual-gs.md).

Des paramètres supplémentaires sont disponibles en fonction du canal de communication sélectionné. Pour plus d’informations, développez les sections ci-dessous.

+++**Appliquer des règles de limitation** (e-mail, notification push ou SMS)

Dans la liste déroulante **[!UICONTROL Règles métier]**, sélectionnez un jeu de règles pour appliquer des règles de limitation à votre action de parcours.

L’utilisation des jeux de règles de canal vous permet de définir un capping de fréquence par type de communication afin d’éviter d’envoyer trop de messages similaires aux clientes et aux clients.

[Découvrir comment utiliser les jeux de règles](../conflict-prioritization/rule-sets.md)

+++

+++**Suivre l’engagement** (e-mail, SMS).

Utilisez la section **[!UICONTROL Suivi des actions]** pour suivre la réaction des personnes destinataires à vos diffusions e-mail ou SMS.

Les résultats du suivi sont accessibles dans le rapport du parcours, une fois celui-ci exécuté.

[En savoir plus sur les rapports de parcours](../reports/journey-global-report-cja.md)

+++

+++**Activer le mode de diffusion rapide** (notifications push).

Le mode de diffusion rapide est un module complémentaire de [!DNL Journey Optimizer] qui permet d’envoyer très rapidement des messages push en grande quantité dans le cadre d’une campagne.

La diffusion rapide est utilisée lorsque le retard dans la diffusion des messages est critique pour l’entreprise, quand vous souhaitez envoyer une alerte push urgente sur les téléphones mobiles, par exemple une nouvelle de dernière minute aux personnes qui ont installé votre application d&#39;actualités.

Découvrez comment activer le mode de diffusion rapide pour les notifications push [sur cette page](../push/create-push.md#rapid-delivery).

Pour plus d’informations sur les performances lors de l’utilisation du mode de diffusion rapide, consultez la section [[!DNL Adobe Journey Optimizer] description du produit](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++**Attribuer des scores de priorité** (web, in-app, basé sur du code)

Dans la section **[!UICONTROL Gestion des conflits]**, attribuez un score de priorité à l’action de parcours, ce qui vous permet de donner la priorité à une action entrante lorsque plusieurs actions de parcours ou campagnes utilisent la même configuration des canaux.

Par défaut, le score de priorité de l’action est hérité du score de priorité global du parcours.

[Découvrir comment attribuer des scores de priorité aux actions de canal](../conflict-prioritization/priority-scores.md#priority-action)

+++

+++**Définir des règles de diffusion supplémentaires** (cartes de contenu)

Pour les parcours de cartes de contenu, vous pouvez activer des règles de diffusion supplémentaires afin de choisir les événements et critères qui déclenchent votre message.

[Découvrir comment créer des cartes de contenu](../content-card/create-content-card.md)

+++

+++**Définir des déclencheurs** (in-app)

Pour les messages in-app, vous pouvez utiliser le bouton **[!UICONTROL Modifier les déclencheurs]** pour choisir les événements et les critères qui déclenchent votre message.

[Découvrir comment créer un message in-app](../in-app/create-in-app.md)

+++

## Ajouter plusieurs actions entrantes {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action_journey"
>title="Ajouter plusieurs actions entrantes"
>abstract="Vous pouvez sélectionner plusieurs actions entrantes au sein d’un même parcours. Cette fonctionnalité permet de diffuser plusieurs expériences basées sur du code, messages in-app, cartes de contenu ou actions web à différents emplacements en même temps, chaque action comportant du contenu spécifique."

Pour simplifier votre orchestration de parcours, vous pouvez définir plusieurs actions entrantes dans une seule action de parcours.

>[!NOTE]
>
>Cette fonctionnalité est uniquement disponible pour les canaux entrants. Actuellement, les canaux sortants comme l’E-mail ne sont pas pris en charge.

Cette fonctionnalité permet de diffuser plusieurs expériences basées sur du code, messages in-app, cartes de contenu ou actions web à différents emplacements en même temps, sans avoir besoin de créer plusieurs actions de parcours. Le déploiement de votre parcours en est facilité et les rapports sont plus fluides, toutes les données étant consolidées dans un seul parcours.

Par exemple, vous pouvez envoyer une expérience basée sur du code à plusieurs points d’entrée avec des contenus légèrement différents. Pour ce faire, créez plusieurs actions basées sur du code dans la même action de parcours, chacune avec une configuration de point d’entrée différente.

Pour définir plusieurs actions entrantes dans une action de parcours, procédez comme suit.

1. Débutez votre parcours avec une activité [Événement](general-events.md) ou [Lecture d’audience](read-audience.md).

1. Dans la section **[!UICONTROL Actions]** de la palette, placez une activité **[!UICONTROL Action]** dans la zone de travail.

1. Sélectionnez **[!UICONTROL Action multiple]** comme type d’action.

   ![Activité multi-action dans la palette de parcours sous Orchestration](assets/journey-multi-action.png)

1. Ajoutez un libellé si nécessaire et sélectionnez **[!UICONTROL Configurer l’action]**.

   ![Volet de configuration multi-action avec les champs de libellé et de description](assets/journey-multi-action-configure.png){width="60%"}

1. Vous accédez à l’onglet **[!UICONTROL Actions]** de l’écran de configuration de l’action de parcours.

   ![Configuration multi-action affichant la liste des actions à exécuter](assets/journey-multi-action-configuration.png){width="70%"}

1. Sélectionnez une action entrante (**Expérience basée sur du code**, **message in-app**, **carte de contenu** ou **web**) dans la section **[!UICONTROL Actions]**.

1. Sélectionnez la configuration des canaux et définissez un contenu spécifique pour cette action.

1. Utilisez le bouton **[!UICONTROL Ajouter une action]** pour sélectionner une autre action entrante dans la liste déroulante.

   ![Ajouter un bouton d’action pour inclure des actions supplémentaires dans l’activité multi-action](assets/journey-multi-action-add.png){width="80%"}

1. Procédez de la même manière pour ajouter d’autres actions. Vous pouvez ajouter jusqu’à 10 actions entrantes dans un groupe d’actions de parcours.

Une fois le parcours [actif](publish-journey.md), toutes les actions sont activées simultanément.

## Mise à jour du contenu dynamique {#update-live-content}

Vous pouvez mettre à jour le contenu d’une action de canal intégrée dans un parcours dynamique.

Les modifications apportées au contenu ne sont pas répercutées dans le parcours tant que vous n’avez pas enregistré les propriétés de l’action. [En savoir plus](about-journey-activities.md#advanced-parameters)

Pour ce faire, ouvrez votre parcours dynamique, sélectionnez l’activité de canal et cliquez sur **Modifier le contenu**.

![Bouton Modifier l’activité de canal dans le parcours en direct](assets/email-action-edit-content.png)

Cependant, vous ne pouvez pas modifier les attributs utilisés dans la personnalisation, qu’il s’agisse d’attributs de profil ou de données contextuelles (à partir des propriétés d’événement ou de parcours).

* Si vous avez modifié des données contextuelles, le message d’erreur suivant s’affiche : `ERR_AUTHORING_JOURNEYVERSION_201`.

* Si vous avez modifié des attributs de profil, le message d’erreur suivant s’affiche : `ERR_AUTHORING_JOURNEYVERSION_202`.

Notez que pour l’activité in-app, des modifications peuvent être apportées au contenu pendant que le parcours est actif, mais les déclencheurs in-app ne peuvent pas être modifiés.

## Envoi avec des actions personnalisées {#recommendation}

Au lieu d’utiliser les fonctionnalités de message intégrées, vous pouvez utiliser des actions personnalisées pour configurer la connexion d’un système tiers afin d’envoyer des messages ou des appels API.

* Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. [En savoir plus](../action/action.md)

* Si vous utilisez Adobe Campaign, reportez-vous aux sections suivantes :

   * [[!DNL Journey Optimizer] et Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] et Campaign Standard](../action/acs-action.md)
