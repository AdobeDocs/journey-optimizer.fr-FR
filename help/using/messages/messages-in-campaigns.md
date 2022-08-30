---
title: Ajout de messages dans les campagnes
description: Découvrez comment ajouter des messages dans une campagne
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 81%

---


# Ajout de messages dans les campagnes{#messages-in- campaigns}

Dans vos campagnes, sélectionnez le canal pour concevoir et personnaliser le message que vous souhaitez envoyer à votre audience. Lorsque vous ajoutez un email, un SMS ou une notification push à votre campagne, vous pouvez l&#39;envoyer immédiatement ou planifier le message.

>[!NOTE]
>Vous pouvez également créer des parcours pour envoyer des messages déclenchés. En savoir plus dans [cette section](messages-in-journeys.md).

Découvrez comment ajouter et configurer des messages dans une campagne [dans cette section](../campaigns/create-campaign.md)

Découvrez les étapes détaillées pour créer le contenu de votre message dans la page suivante :

* [Création d&#39;un e-mail](create-email.md)
* [Créer des notification push](create-push.md)
* [Créer un SMS](create-sms.md)

## Activer l’optimisation de l’heure d’envoi{#sto-in-journeys}

Pour les notifications push et les e-mails, vous pouvez activer l’**[!UICONTROL optimisation de l’heure d’envoi]**.

Utilisez l’**[!UICONTROL optimisation de l’heure d’envoi]** pour planifier des heures d’envoi personnalisées pour chaque utilisateur afin d’augmenter les taux d’ouverture et de clic de vos messages. [En savoir plus](../messages/send-time-optimization.md).

## Paramètres avancés{#adv-settings}

Les paramètres avancés sont en lecture seule et masqués par défaut.

Pour accéder aux paramètres avancés, cliquez sur l’icône **[!UICONTROL Afficher les champs en lecture seule]** en haut du volet des messages.

![](assets/show-read-only.png)

Les paramètres avancés sont affichés au bas du volet des messages. Ces paramètres sont définis par l’[administrateur système](../start/path/administrator.md) dans la [surface de canal](../configuration/channel-surfaces.md) (c’est-à-dire le préréglage du message) associée au message.

Pour les notifications push, vous pouvez afficher les paramètres suivants : Jeton, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Pour les e-mails, vous pouvez afficher l’adresse e-mail principale.

Pour une utilisation particulière, vous pouvez remplacer ces valeurs dans des contextes spécifiques. Pour forcer une valeur, cliquez sur l’icône **Activer la substitution de paramètre** à droite du champ. Par exemple, cette option peut être utile pour :

* Tester un e-mail. Vous pouvez ajouter votre adresse e-mail. Une fois le parcours publié, l’e-mail vous est envoyé.
* Se référer à l’adresse e-mail des abonnés d’une liste. En savoir plus sur [ce cas d’utilisation](../building-journeys/message-to-subscribers-uc.md).

Cliquez sur la même icône pour masquer les paramètres avancés.

## Parcourir les messages{#browse-message}

Lorsque plusieurs messages sont utilisés dans un parcours, vous pouvez passer de l’un à l’autre à partir de l’écran **Modifier le contenu**.

![](assets/inline-messages-multi-content.png)

Vous pouvez alors [vérifier les alertes](alerts.md) et [simuler](../design/preview.md) chaque contenu depuis une seule vue.

## Dupliquer un message {#duplicate-message}

Vous pouvez copier un message existant à partir de la zone de travail du parcours.

Pour ce faire, suivez les étapes ci-après :

1. Sélectionnez le message que vous souhaitez copier.

1. Utilisez le bouton **[!UICONTROL Copier]** à partir du volet **[!UICONTROL Action]**.

   ![](assets/message-duplicate.png)

1. Appuyez sur **Ctrl+V** pour coller le message.

   Le message est ajouté à la zone de travail du parcours. Tous les paramètres et la configuration sont copiés dans le nouveau message.

   ![](assets/message-duplicated.png)

1. Renommez le message pour pouvoir différencier le message initial de la copie, par exemple lors de l’édition des messages, comme ci-dessous :

   ![](assets/multi-message.png)


>[!NOTE]
>
>Pour les e-mails, vous pouvez également transformer un message existant en modèle. [En savoir plus](../design/email-templates.md).

## Supprimer un message{#delete-message}

Pour supprimer un message, utilisez l’icône de corbeille située en haut du volet de l’activité d’action du canal.

![](assets/delete-message.png)

Utilisez le bouton **[!UICONTROL Confirmer]** pour valider.
