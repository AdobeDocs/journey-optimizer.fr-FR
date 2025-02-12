---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter une action de canal intégrée à un parcours
description: Découvrir comment ajouter une action de canal intégrée à un parcours
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: parcours, message, notification push, sms, e-mail, in-app, web, carte de contenu, expérience basée sur du code
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 56a1ef1ba256d1aac3593d8a61e67bdc42c17d32
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 83%

---

# Utiliser des actions de canal intégrées {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Action de canal intégrée"
>abstract="Journey Optimizer est fourni avec des fonctionnalités d’actions de canal intégrées. Vous pouvez simplement ajouter à votre parcours une activité sortante (e-mail, message texte (SMS/MMS), notification push) ou entrante (in-app, web, expérience basée sur du code, carte de contenu) et définir les paramètres et le contenu. Elle est ensuite exécutée et envoyée dans le contexte du parcours."

[!DNL Journey Optimizer] est fourni avec des fonctionnalités d’actions de canal intégrées. Vous pouvez simplement ajouter à votre parcours une activité sortante (e-mail, message texte (SMS/MMS), notification push) ou entrante (in-app, web, expérience basée sur du code, carte de contenu) et définir les paramètres et le contenu. Elle est ensuite exécutée et envoyée dans le contexte du parcours.

>[!NOTE]
>
>Vous pouvez également configurer des actions spécifiques pour envoyer vos messages. [En savoir plus](#recommendation)

Pour ajouter une action de canal intégrée à un parcours, procédez comme suit :

1. Débutez votre parcours avec une activité [Événement](general-events.md) ou [Lecture d’audience](read-audience.md).

1. Dans la section **Actions** de la palette, effectuez un glisser-déposer d’une activité sortante (**e-mail**, **notification push**, **SMS**) ou entrante (**in-app**, **web**, **expérience basée sur du code**, **carte de contenu**) dans la zone de travail.

   ![](assets/journey-web-activity.png)

1. Configurez votre activité.

   * Découvrez ci-dessous les étapes détaillées pour créer le contenu de votre message :

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

     >[!NOTE]
     >
     >Pour les e-mails et les notifications push, vous pouvez activer l’optimisation de l’heure d’envoi. [En savoir plus](send-time-optimization.md)

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
     >Chaque activité de message entrant est accompagnée d’une activité **Attente** de 3 jours. [En savoir plus](wait-activity.md#auto-wait-node)


## Mettre à jour le contenu dynamique {#update-live-content}

Vous pouvez mettre à jour le contenu d’une action de canal intégrée dans un parcours dynamique.

Pour ce faire, ouvrez votre parcours dynamique, sélectionnez l’activité de canal et cliquez sur **Modifier le contenu**.

![](assets/add-a-message2.png)

Cependant, vous ne pouvez pas modifier les attributs utilisés dans la personnalisation, qu’il s’agisse d’attributs de profil ou de données contextuelles (à partir des propriétés d’événement ou de parcours).

Si vous avez modifié des données contextuelles, le message d’erreur suivant s’affiche : `ERR_AUTHORING_JOURNEYVERSION_201`

Si vous avez modifié les attributs de profil, le message d’erreur suivant s’affiche : `ERR_AUTHORING_JOURNEYVERSION_202`

Notez que pour l’activité in-app, des modifications peuvent être apportées au contenu pendant que le parcours est actif, mais les triggers in-app ne peuvent pas être modifiés.

## Envoyer avec des actions personnalisées {#recommendation}

Au lieu d&#39;utiliser les fonctionnalités de message intégrées, vous pouvez utiliser des actions personnalisées pour configurer la connexion d&#39;un système tiers afin d&#39;envoyer des messages ou des appels d&#39;API.

* Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. [En savoir plus](../action/action.md)

* Si vous utilisez Adobe Campaign, reportez-vous aux sections suivantes :

   * [[!DNL Journey Optimizer] et Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] et Campaign Standard](../action/acs-action.md)