---
title: Prise en main des messages
description: Découvrez comment créer et diffuser des messages personnalisés dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 8%

---

# Prise en main des actions de canal {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Actions des canaux"
>abstract="Utilisez les actions de canal pour envoyer un message push, un SMS ou un email."

Utilisation [!DNL Journey Optimizer] pour créer et diffuser des notifications push, des SMS et des emails personnalisés. Tous les messages sont modifiables en ligne dans le cadre d’une action sur le canevas de Parcours.  Utilisez la fonctionnalité Enregistrer comme modèle pour réutiliser facilement votre contenu. Vous pouvez :

* Utilisation [!DNL Journey Optimizer] **fonctionnalités de conception d&#39;email** pour créer ou importer des emails réactifs.

* Utilisation **Adobe Experience Manager Assets Essentials** pour enrichir vos emails, créez et gérez votre propre base de données de ressources.

* Rechercher **Photos Adobe Stock** pour créer votre contenu et améliorer votre conception d&#39;email.

* Améliorez l’expérience des clients en créant des **notifications push, SMS et emails** en fonction de leurs attributs de profil.

* **Envoi de diffusions** en fonction de ces contenus et effectuez le suivi du comportement des clients.

>[!NOTE]
>
>Les utilisateurs peuvent accéder aux parcours, les créer, les modifier et/ou les publier en fonction de leur profil de produit. En savoir plus sur les autorisations utilisateur [dans cette section](../administration/permissions.md).


## Ajout de messages dans vos parcours{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Catégorie de message"
>abstract="Choisissez Marketing pour les messages commerciaux ou Transactionnel pour les messages non commerciaux tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion."

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Surface du canal"
>abstract="Une surface de canal est une instance de ce canal qui possède tous les paramètres pour diffuser une action avec succès via une campagne ou un parcours. Il est défini par un administrateur système."

Pour ajouter des messages dans vos parcours, ajoutez simplement une activité push, SMS ou email dans les canevas de parcours.

1. Commencez votre parcours par une [Événement](../building-journeys/general-events.md) ou [Lecture de segment](../building-journeys/read-segment.md) activité.

1. Dans la **Actions** de la palette, effectuez un glisser-déposer d’une **email**, un **SMS** ou **Push** dans la zone de travail.

   ![](assets/add-a-message.png)

1. Saisissez un libellé et une description.

1. Sélectionner le message **[!UICONTROL Catégorie]**: select **Marketing** pour les messages commerciaux, ou **Transactionnel** pour les messages non commerciaux tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion.

   >[!NOTE]
   >
   >Si vous avez défini [règles de fréquence](../configuration/frequency-rules.md) pour un canal et une catégorie spécifiques, ils sont automatiquement appliqués au message lors de la sélection de ce canal et de cette catégorie. Actuellement, seule la variable **[!UICONTROL Marketing]** est disponible pour les règles de fréquence.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >Les messages de type marketing doivent inclure une [lien d’exclusion](../messages/consent.md#opt-out-management). Cela n’est pas nécessaire pour les messages transactionnels, car ces messages peuvent être envoyés aux profils qui se sont désabonnés des communications marketing.

1. Sélectionner le canal **[!UICONTROL Surface]** (c’est-à-dire le paramètre prédéfini du message) à utiliser pour envoyer votre message.

   Une surface est une configuration définie par une [Administrateur système](../start/path/administrator.md). Il contient tous les paramètres techniques pour l’envoi du message, tels que les paramètres d’en-tête, le sous-domaine, les applications mobiles, etc. [En savoir plus](../configuration/message-presets.md).

   >[!CAUTION]
   >
   >Vous devez choisir une surface de canal valide pour la catégorie et le canal de message sélectionnés.

   Vous pouvez à tout moment accéder au libellé, à la description et à la surface du message et le modifier à l&#39;aide de la fonction **[!UICONTROL Propriétés]** dans l’interface des messages.

1. Création du contenu du message.

   Découvrez les étapes détaillées pour créer le contenu de votre message dans la page suivante :

   * [Création d&#39;un e-mail](create-email.md)
   * [Créer des notification push](create-push.md)
   * [Création dʼun SMS](create-sms.md)

## Activation de l’optimisation du temps d’envoi{#sto-in-journeys}

Pour les notifications par e-mail et push, vous pouvez activer **[!UICONTROL Optimisation de l’heure d’envoi]**.

Utilisation **[!UICONTROL Optimisation de l’heure d’envoi]** pour planifier des heures d’envoi personnalisées pour que chaque utilisateur augmente les taux d’ouverture et de clic de vos messages. [En savoir plus](../messages/send-time-optimization.md).


## Paramètres avancés{#adv-settings}

Les paramètres avancés sont en lecture seule et masqués par défaut.

Pour accéder aux paramètres avancés, cliquez sur le bouton **[!UICONTROL Afficher les champs en lecture seule]** en haut du volet des messages.

![](assets/show-read-only.png)

Les paramètres avancés sont affichés au bas du volet des messages. Ces paramètres sont définis par la variable [administrateur système](../start/path/administrator.md) dans le [surface du canal](../configuration/message-presets.md) (c’est-à-dire le paramètre prédéfini du message) associé au message.

Pour les notifications push, vous pouvez afficher les paramètres suivants : Jeton, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Pour les emails, vous pouvez afficher l’Principale adresse email.

Pour une utilisation spécifique, vous pouvez remplacer ces valeurs dans des contextes spécifiques. Pour forcer une valeur, cliquez sur le bouton **Activer le remplacement de paramètre** à droite du champ. Cette option peut s’avérer utile, par exemple pour :

* Testez un email, vous pouvez ajouter votre adresse email. Une fois le parcours publié, l’e-mail vous est envoyé. 
* Reportez-vous à l&#39;adresse email des abonnés d&#39;une liste. En savoir plus dans [ce cas pratique ;](../building-journeys/message-to-subscribers-uc.md).

Cliquez sur la même icône pour rétablir le paramètre par défaut.


## Parcourir les messages{#browse-message}

Lorsque plusieurs messages sont utilisés dans un parcours, vous pouvez passer de l’un à l’autre à partir de la variable **Modifier le contenu** écran.

![](assets/inline-messages-multi-content.png)

Vous pouvez alors [alertes de vérification](alerts.md) et [simuler](../design/preview.md) chaque contenu depuis une seule vue.

## Dupliquer un message {#duplicate-message}

Vous pouvez copier un message existant à partir du canevas de parcours.

Pour ce faire, suivez les étapes ci-après :

1. Sélectionnez le message à copier.

1. Utilisez la variable **[!UICONTROL Copier]** à partir du bouton **[!UICONTROL Action]** volet.

   ![](assets/message-duplicate.png)

1. Entrée **crtl+V** pour coller le message.

   Le message est ajouté aux canevas de parcours. Tous les paramètres et la configuration seront copiés dans le nouveau message.

   ![](assets/message-duplicated.png)

1. Renommez le message pour pouvoir différencier le message initial de la copie, par exemple lors de l&#39;édition des messages, comme ci-dessous :

   ![](assets/multi-message.png)


>[!NOTE]
>
>Pour les emails, vous pouvez également transformer un message existant en modèle. [En savoir plus](../design/email-templates.md).

## Supprimer un message

Pour supprimer un message, utilisez l’icône de corbeille située en haut du volet de l’activité d’action du canal.

![](assets/delete-message.png)

Utilisez la variable **[!UICONTROL Confirmer]** pour valider.
