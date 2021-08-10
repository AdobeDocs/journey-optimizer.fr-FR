---
title: Ajout d'un message dans un parcours
description: Ajout d'un message dans un parcours
feature: Parcours
topic: Gestion de contenu
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3530a600a4c842ff99bc23354b2d158c6d41f902
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 100%

---


# Ajout d&#39;un message dans un parcours

Les fonctionnalités de message [!DNL Journey Optimizer] sont intégrées, il vous suffit de concevoir votre contenu et de publier votre message. Consultez [cette section](../get-started-content.md). Ensuite, vous ajoutez simplement, dans votre parcours, un message push ou e-mail conçu à l&#39;aide de Journey Optimizer.

Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. En savoir plus dans cette [section](../action/action.md).

## Ajout d&#39;une activité de message

1. Comme toujours, débutez votre parcours avec un événement ou une activité **Lecture de segment**.

   ![](../assets/jo-message0.png)

1. Dans la section **Actions** de la palette, faites glisser-déposer une activité **Message** dans la zone de travail.

   ![](../assets/jo-message1.png)

1. Ajoutez un libellé et une description.

   ![](../assets/jo-message2.png)

1. Cliquez dans le champ **Message**. La liste des messages disponibles conçus dans Journey Optimizer s&#39;affiche. Vous pouvez filtrer la liste par état.

   ![](../assets/jo-message3.png)

1. Choisissez un message et cliquez sur **Sélectionner**. Vous pouvez également créer un nouveau message directement à partir de cet écran en cliquant sur **Créer un message**.

   ![](../assets/jo-message4-ter.png)

   Si vous souhaitez vérifier votre message, vous pouvez cliquer sur l&#39;icône **Ouvrir le message** dans le champ **Message**. Le message s&#39;ouvre dans un nouvel onglet.

   ![](../assets/jo-message4-bis.png)

1. Ajoutez les étapes suivantes à votre parcours.

## Paramètres de l&#39;e-mail et paramètres Push

Les sections **[!UICONTROL Paramètres de l&#39;e-mail]** et **[!UICONTROL Paramètres Push]** affichent des champs en lecture seule. Cette configuration est généralement effectuée lors de la création du message. Consultez [cette section](../get-started-content.md).

![](../assets/jo-message4.png)

Pour forcer une valeur spécifique, vous pouvez utiliser l’icône **Activer la substitution de paramètre** à droite du champ. Cette option peut être utile à des fins de test. Par exemple, pour un e-mail, vous pouvez ajouter votre adresse e-mail. Une fois le parcours publié, l&#39;e-mail vous est envoyé.

## Optimisation de l&#39;heure d&#39;envoi{#send-time-optimization}

### À propos de l&#39;optimisation de l&#39;heure d&#39;envoi{#about-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="À propos de l&#39;optimisation de l&#39;heure d&#39;envoi"
>abstract="La fonctionnalité d&#39;optimisation de l&#39;heure d&#39;envoi d&#39;Adobe Journey Optimizer, optimisée par les services d&#39;IA d&#39;Adobe, peut prévoir le meilleur moment pour envoyer un e-mail ou un message push afin de maximiser l&#39;engagement en fonction des taux d&#39;ouverture et de clic historiques."

La fonctionnalité d&#39;optimisation de l&#39;heure d&#39;envoi d&#39;Adobe Journey Optimizer, optimisée par les services d&#39;IA d&#39;Adobe, peut prévoir le meilleur moment pour envoyer un e-mail ou un message push afin de maximiser l&#39;engagement en fonction des taux d&#39;ouverture et de clic historiques. Utilisez notre modèle d&#39;apprentissage automatique pour planifier des heures d&#39;envoi personnalisées afin que chaque utilisateur augmente les taux d&#39;ouverture et de clic de vos messages.

Le modèle d&#39;optimisation de l&#39;heure d&#39;envoi ingère vos données Adobe Journey Optimizer et examine les taux d&#39;ouverture au niveau de l&#39;utilisateur (pour les e-mails et les notifications push) et de clics (pour les e-mails) afin de déterminer à quel moment vos clients sont les plus susceptibles d&#39;interagir avec vos messages. L&#39;optimisation de l&#39;heure d&#39;envoi nécessite au moins un mois de données de suivi des messages pour formuler des recommandations éclairées. Pour chaque utilisateur, le modèle génère les données prédictives suivantes :

* La meilleure heure de chaque jour de la semaine pour optimiser l&#39;engagement
* Le meilleur jour de la semaine pour optimiser l&#39;engagement
* La meilleure heure du meilleur jour de la semaine pour optimiser l&#39;engagement

Le modèle varie selon que vous parlez de notation ou de formation. La formation est dispensée une fois par semaine, puis une fois par trimestre. La notation est d&#39;abord hebdomadaire, puis mensuelle.

* Formation : développement de l&#39;algorithme utilisé pour calculer le score.
* Notation : application d&#39;un score à des profils individuels en fonction du modèle formé.

Ces informations sont stockées avec le profil de l&#39;utilisateur et sont référencées lors de l&#39;exécution du parcours pour indiquer à Adobe Journey Optimizer quand envoyer votre message.

## Remarques importantes{#send-time-optimization-notes}

* Cette fonctionnalité est uniquement disponible pour les messages mono-canal sur les e-mails et les notifications push avec le suivi activé.
* Le message doit être publié.
* Cette fonctionnalité n&#39;est pas compatible avec le mode rafale.

## Activation de l&#39;optimisation de l&#39;heure d&#39;envoi{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Activation de l&#39;optimisation de l&#39;heure d&#39;envoi"
>abstract="Choisissez si vous souhaitez optimiser les ouvertures d&#39;e-mail ou les clics sur e-mail en sélectionnant le bouton radio approprié. Vous pouvez également choisir de mettre entre crochets les heures d&#39;envoi utilisées par le système en saisissant une valeur pour l&#39;option Envoyer pendant."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Activation de l&#39;optimisation de l&#39;heure d&#39;envoi"
>abstract="Les messages push sont définis par défaut sur l&#39;option d&#39;ouverture, car les clics ne s&#39;appliquent pas à la messagerie push. Vous pouvez également choisir de mettre entre crochets les heures d&#39;envoi utilisées par le système en saisissant une valeur pour l&#39;option Envoyer pendant."

Activez l&#39;optimisation de l&#39;heure d&#39;envoi sur un e-mail ou un message push en sélectionnant le commutateur **Optimisation de l&#39;heure d&#39;envoi** dans les paramètres de l&#39;activité Message.

![](../assets/jo-message5.png)

Pour les e-mails, choisissez si vous souhaitez optimiser les ouvertures d&#39;e-mail ou les clics sur e-mail en sélectionnant le bouton radio approprié. Les messages push sont définis par défaut sur l&#39;option d&#39;ouverture, car les clics ne s&#39;appliquent pas à la messagerie push.

Vous pouvez également choisir de mettre entre crochets les heures d&#39;envoi utilisées par le système en saisissant une valeur pour l&#39;option **Envoyer pendant**. Si vous choisissez « six heures » comme valeur, Adobe Journey Optimizer vérifie chaque profil utilisateur pour déterminer si l&#39;heure d&#39;envoi optimale se produit dans les six heures suivant l&#39;heure d&#39;exécution du parcours et sélectionnez l&#39;heure déterminée pour l&#39;optimisation de l&#39;heure d&#39;envoi. Si ce délai n&#39;est pas compris dans les six heures suivantes, Adobe Journey Optimizer enverra le message par défaut au moment de l&#39;exécution du parcours.
