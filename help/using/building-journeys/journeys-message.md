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
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: ht
source-wordcount: '1268'
ht-degree: 100%

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
     >Chaque activité de message entrant est accompagnée d’une activité **Attente** de 3 jours. [En savoir plus](../building-journeys/wait-activity.md#auto-wait-node)

## Recommandation {#recommendation}

[!DNL Journey Optimizer] est fourni avec une fonctionnalité de message intégrée. Cependant, les actions personnalisées vous permettent de configurer la connexion d’un système tiers pour envoyer des messages ou des appels d’API.

* Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. [En savoir plus](../action/action.md)

* Si vous utilisez Campaign et Journey Optimizer, reportez-vous aux sections suivantes :

   * [[!DNL Journey Optimizer] et Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] et Campaign Standard](../action/acs-action.md)

## Mettre à jour le contenu dynamique{#update-live-content}

Vous pouvez mettre à jour le contenu d’une action de canal intégrée dans un parcours dynamique.

Pour ce faire, ouvrez votre parcours dynamique, sélectionnez l’activité de canal et cliquez sur **Modifier le contenu**.

![](assets/add-a-message2.png)

Cependant, vous ne pouvez pas modifier les attributs utilisés dans la personnalisation, qu’il s’agisse d’attributs de profil ou de données contextuelles (à partir des propriétés d’événement ou de parcours).

Si vous avez modifié des données contextuelles, le message d’erreur suivant s’affiche : ERR_AUTHORING_JOURNEYVERSION_201.

Si vous avez modifié des attributs de profil, le message d’erreur suivant s’affiche : ERR_AUTHORING_JOURNEYVERSION_202.

Notez que pour l’activité in-app, des modifications peuvent être apportées au contenu pendant que le parcours est actif, mais les triggers in-app ne peuvent pas être modifiés.

## Optimisation de l’heure d’envoi{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="À propos de l&#39;optimisation de l&#39;heure d&#39;envoi"
>abstract="La fonctionnalité d’optimisation de l’heure d&#39;envoi d’Adobe Journey Optimizer, proposée par les services d’IA d’Adobe, peut prévoir le meilleur moment pour envoyer un e-mail ou un message push afin d’optimiser l’engagement en fonction des taux historiques d’ouverture et de clic."

>[!NOTE]
>
>Cette fonctionnalité n&#39;est pas activée par défaut. Vous pouvez contacter votre représentant ou représentante Adobe pour l’activer.
>
>La fonctionnalité d’optimisation de l’heure d’envoi s’applique uniquement aux canaux d’e-mail et de notification push.

### À propos de l’optimisation de l’heure d’envoi {#about-send-time}

La fonctionnalité d’optimisation de l’heure d’envoi d’Adobe Journey Optimizer, proposée par les services d’IA d’Adobe, peut prévoir le meilleur moment pour envoyer un **e-mail** ou un **message push** afin d’optimiser l’engagement en fonction des taux historiques d’ouvertures et de clics. Utilisez notre modèle d&#39;apprentissage automatique pour planifier des heures d&#39;envoi personnalisées afin que chaque utilisateur augmente les taux d&#39;ouverture et de clic de vos messages.

Le modèle d&#39;optimisation de l&#39;heure d&#39;envoi ingère vos données Adobe Journey Optimizer et examine les taux d&#39;ouverture au niveau de l&#39;utilisateur (pour les e-mails et les notifications push) et de clics (pour les e-mails) afin de déterminer à quel moment vos clients sont les plus susceptibles d&#39;interagir avec vos messages. L&#39;optimisation de l&#39;heure d&#39;envoi nécessite au moins un mois de données de suivi des messages pour formuler des recommandations éclairées. Pour chaque utilisateur, le système sélectionne automatiquement la meilleure heure à l’aide des scores suivants :

* La meilleure heure de chaque jour de la semaine pour optimiser l&#39;engagement
* Le meilleur jour de la semaine pour optimiser l&#39;engagement
* La meilleure heure du meilleur jour de la semaine pour optimiser l&#39;engagement

Le modèle varie selon que vous parlez de notation ou de formation. La formation est dispensée une fois par semaine, puis une fois par trimestre. La notation est d&#39;abord hebdomadaire, puis mensuelle.

* Formation : développement de l&#39;algorithme utilisé pour calculer le score.
* Notation : application d&#39;un score à des profils individuels en fonction du modèle formé.

Ces informations sont stockées avec le profil de l&#39;utilisateur et sont référencées lors de l&#39;exécution du parcours pour indiquer à Adobe Journey Optimizer quand envoyer votre message.

### Questions fréquentes {#faq-send-time}

+++ Que peut faire l’optimisation de l’heure d’envoi ? Comment sont gérés les nouveaux profils ? L’envoi est-il étendu sur une fenêtre de 6/12/24 heures ?

L’optimisation de l’heure d’envoi tente de prévoir le meilleur moment pour interagir avec la clientèle et d’optimiser les taux d’ouverture/de clics des e-mails. Le score prend un format d’attributs `3*7*24` pour chaque profil. Les attributs `7*24` décrivent le classement du meilleur moment prédit pour envoyer des e-mails au destinataire ; 3 est destiné à optimiser le taux d’ouverture des e-mails, le taux de clics sur les e-mails et le taux d’ouverture des notifications push.

+++

+++Où puis-je consulter l’heure d’envoi prévue pour chaque profil ?

Vous pouvez voir le score global dans l’interface **Profils**. Pour chacun des trois ensembles de 168 scores, les classements vont de -83 à 84. Plus le classement est élevé, plus le moment choisi pour l’interaction avec le ou la destinataire est bon. Puisque vous pouvez définir le début et la durée d’un parcours, il est possible que le meilleur classement (84) ne tombe pas dans cette fenêtre temporelle. Dans ce cas, nous vous recommandons de choisir une heure ayant la valeur de classement la plus élevée.

+++


+++Quels sont les rapports disponibles ?

Accédez à votre parcours, cliquez sur le bouton **Afficher le rapport** en haut à droite et sélectionnez l’onglet **Parcours** de gauche. [En savoir plus](../reports/journey-global-report-cja.md)

+++

+++Comment les données d’optimisation de l’heure d’envoi affectent-elles la richesse des profils ?

L’optimisation de l’heure d’envoi ajoute le score/les attributs à chaque profil, mais aucun nouveau profil n’est créé.

+++

### Activer l’optimisation de l’heure d’envoi{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Activer l’optimisation de l’heure d’envoi"
>abstract="Choisissez si vous souhaitez optimiser les ouvertures d&#39;e-mail ou les clics sur e-mail en sélectionnant le bouton radio approprié. Vous pouvez également choisir de mettre entre crochets les heures d&#39;envoi utilisées par le système en saisissant une valeur pour l&#39;option Envoyer pendant."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Activer l’optimisation de l’heure d’envoi"
>abstract="Les messages push sont définis par défaut sur l&#39;option d&#39;ouverture, car les clics ne s&#39;appliquent pas à la messagerie push. Vous pouvez également choisir de mettre entre crochets les heures d&#39;envoi utilisées par le système en saisissant une valeur pour l&#39;option Envoyer pendant."

Activez l’optimisation de l’heure d’envoi sur un e-mail ou une notification push en sélectionnant le commutateur **Optimisation de l’heure d’envoi** dans les paramètres d’activité.

![](../building-journeys/assets/jo-message5.png)

Pour les e-mails, choisissez si vous souhaitez optimiser les ouvertures d&#39;e-mail ou les clics sur e-mail en sélectionnant le bouton radio approprié. Les messages push sont définis par défaut sur l&#39;option d&#39;ouverture, car les clics ne s&#39;appliquent pas à la messagerie push.

Vous pouvez également choisir de mettre entre crochets les heures d&#39;envoi utilisées par le système en saisissant une valeur pour l&#39;option **Envoyer pendant**. Si vous choisissez « six heures » comme valeur, [!DNL Journey Optimizer] vérifie chaque profil utilisateur et sélectionne l’heure d’envoi optimale dans les six heures suivant l’heure d’exécution du parcours.

**Que se passe-t-il si le temps optimal se situe à l’extérieur de l’intervalle ?**

Prenons un exemple avec la configuration suivante :

* Optimiser avec les clics
* L’action est censée commencer à 10 heures
* L’intervalle est de 3 heures

Un profil peut avoir un temps d’ouverture optimal en dehors de l’intervalle. Par exemple, l’ouverture optimale des clics pour John est à 17 heures.

Au niveau du profil, il y a des scores pour chaque heure de la semaine. Dans cet exemple, l’e-mail sera toujours envoyé pendant l’intervalle. Au moment de l’exécution, le système vérifie la liste des scores dans cet intervalle (intervalle de 3 heures commençant à 10 heures). Le système compare ensuite les scores pour 10 h, 11 h et midi et sélectionne le meilleur. L’e-mail est envoyé à ce moment-là.
