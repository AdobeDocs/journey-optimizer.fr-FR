---
title: Optimisation de l'heure d'envoi
description: Découvrez comment paramétrer l’optimisation de l’heure d’envoi dans vos messages
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 100%

---

## Optimisation de l’heure d’envoi{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="À propos de l&#39;optimisation de l&#39;heure d&#39;envoi"
>abstract="La fonctionnalité d&#39;optimisation de l&#39;heure d&#39;envoi d&#39;Adobe Journey Optimizer, optimisée par les services d&#39;IA d&#39;Adobe, peut prévoir le meilleur moment pour envoyer un e-mail ou un message push afin de maximiser l&#39;engagement en fonction des taux d&#39;ouverture et de clic historiques."

La fonctionnalité d&#39;optimisation de l&#39;heure d&#39;envoi d&#39;Adobe Journey Optimizer, optimisée par les services d&#39;IA d&#39;Adobe, peut prévoir le meilleur moment pour envoyer un e-mail ou un message push afin de maximiser l&#39;engagement en fonction des taux d&#39;ouverture et de clic historiques. Utilisez notre modèle d&#39;apprentissage automatique pour planifier des heures d&#39;envoi personnalisées afin que chaque utilisateur augmente les taux d&#39;ouverture et de clic de vos messages.

Le modèle d&#39;optimisation de l&#39;heure d&#39;envoi ingère vos données Adobe Journey Optimizer et examine les taux d&#39;ouverture au niveau de l&#39;utilisateur (pour les e-mails et les notifications push) et de clics (pour les e-mails) afin de déterminer à quel moment vos clients sont les plus susceptibles d&#39;interagir avec vos messages. L&#39;optimisation de l&#39;heure d&#39;envoi nécessite au moins un mois de données de suivi des messages pour formuler des recommandations éclairées. Pour chaque utilisateur, le système sélectionne automatiquement la meilleure heure à l’aide des scores suivants :

* La meilleure heure de chaque jour de la semaine pour optimiser l&#39;engagement
* Le meilleur jour de la semaine pour optimiser l&#39;engagement
* La meilleure heure du meilleur jour de la semaine pour optimiser l&#39;engagement

Le modèle varie selon que vous parlez de notation ou de formation. La formation est dispensée une fois par semaine, puis une fois par trimestre. La notation est d&#39;abord hebdomadaire, puis mensuelle.

* Formation : développement de l&#39;algorithme utilisé pour calculer le score.
* Notation : application d&#39;un score à des profils individuels en fonction du modèle formé.

Ces informations sont stockées avec le profil de l&#39;utilisateur et sont référencées lors de l&#39;exécution du parcours pour indiquer à Adobe Journey Optimizer quand envoyer votre message.

>[!CAUTION]
>
>Cette fonctionnalité n&#39;est pas compatible avec le mode rafale.

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
