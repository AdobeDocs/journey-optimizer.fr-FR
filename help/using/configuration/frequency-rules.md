---
solution: Journey Optimizer
product: journey optimizer
title: Règles de fréquence
description: Découvrez comment définir des règles de fréquence
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 100%

---

# Règles de fréquence des messages {#frequency-rules}

[!DNL Journey Optimizer] vous permet de contrôler la fréquence à laquelle les utilisateurs recevront un message ou entreront dans un parcours en définissant des règles cross-canal qui excluront automatiquement les profils sur-sollicités des messages et actions.

Par exemple, vous ne voulez pas que votre marque envoie plus de 3 messages marketing par mois à ses clients.

Pour cela, vous pouvez utiliser une règle de fréquence qui limite le nombre de messages envoyés sur un ou plusieurs canaux au cours d&#39;une période calendaire mensuelle.

>[!NOTE]
>
>Les règles de fréquence des messages sont différentes de la gestion des désabonnements, qui permet aux utilisateurs de se désabonner de la réception des communications de la part d&#39;une marque. [En savoir plus](../privacy/opt-out.md#opt-out-management)

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Règles d&#39;accès {#access-rules}

Les règles sont disponibles à partir du menu **[!UICONTROL Administration]** > **[!UICONTROL Règles]**. Toutes les règles sont répertoriées, triées par date de modification.

Utilisez l&#39;icône de filtre pour filtrer par catégorie, statut et/ou canal. Vous pouvez également effectuer une recherche sur le libellé du message.

![](assets/message-rules-filter.png)

### Autorisations{#permissions-frequency-rules}

Pour accéder aux règles de fréquence des messages, en créer, les modifier ou les supprimer, vous devez disposer de l’autorisation **[!UICONTROL Gestion des règles de fréquence]**.

Les utilisateurs avec l’autorisation **[!UICONTROL Afficher les règles de fréquence]** peuvent afficher les règles, mais pas les modifier ni les supprimer.

![](assets/message-rules-access.png)

Pour en savoir plus sur les autorisations, consultez [cette section](../administration/high-low-permissions.md).

## Création d&#39;une règle {#create-new-rule}

Pour créer une nouvelle règle, procédez comme suit.

1. Accédez à la liste **[!UICONTROL Règles de fréquence des messages]**, puis cliquez sur **[!UICONTROL Créer une règle]**.

   ![](assets/message-rules-create.png)

1. Définissez le nom de la règle.

   ![](assets/message-rules-details.png)

1. Sélectionnez la catégorie de règle du message.

   >[!NOTE]
   >
   >Actuellement, seule la catégorie **[!UICONTROL Marketing]** est disponible.

1. Définissez la limitation de votre règle, c&#39;est-à-dire le nombre maximum de messages qui peuvent être envoyés à un profil utilisateur individuel chaque mois.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >La limite de fréquence est basée sur une période calendaire mensuelle. Elle est réinitialisée au début de chaque mois.

1. Sélectionnez le canal à utiliser pour cette règle : **[!UICONTROL E-mail]** ou **[!UICONTROL Notification push]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Vous devez sélectionner au moins un canal pour pouvoir créer la règle.

1. Sélectionnez plusieurs canaux si vous souhaitez appliquer une limitation sur tous les canaux sélectionnés en tant que nombre total.

   Par exemple, définissez la limitation sur 15 et sélectionnez les canaux e-mail et push. Si un profil a déjà reçu 10 e-mails marketing et 5 notifications push marketing, ce profil sera exclu de la prochaine diffusion de tout e-mail ou notification push marketing.

1. Cliquez sur **[!UICONTROL Enregistrer comme brouillon]** pour confirmer la création de la règle. Votre message est ajouté à la liste de règles, dans l&#39;état **[!UICONTROL Brouillon]**.

   ![](assets/message-rules-created.png)

## Activer une règle {#activate-rule}

Une fois créée, une règle de fréquence des messages affiche le statut **[!UICONTROL Brouillon]** et n’a encore aucune incidence sur le message. Pour l’activer, cliquez sur les points de suspension en regard de la règle et sélectionnez **[!UICONTROL Activer]**.

![](assets/message-rules-activate.png)

L&#39;activation d&#39;une règle aura un impact sur tous les messages auxquels elle s&#39;applique lors de leur exécution suivante. Découvrez comment [appliquer une règle de fréquence à un message](#apply-frequency-rule).

>[!NOTE]
>
>L’activation complète d’une règle peut prendre jusqu’à 10 minutes. Vous n’avez pas besoin de modifier des messages ou de republier des parcours pour qu’une règle prenne effet.

Pour désactiver une règle de fréquence des messages, cliquez sur les points de suspension en regard de la règle et sélectionnez **[!UICONTROL Désactiver]**.

![](assets/message-rules-deactivate.png)

L&#39;état de la règle devient **[!UICONTROL Inactif]** et la règle ne s&#39;appliquera pas aux futures exécutions de messages. Les messages en cours d&#39;exécution ne seront pas affectés.

>[!NOTE]
>
>La désactivation d&#39;une règle n&#39;affecte ou ne réinitialise aucun comptage sur les profils individuels.

## Appliquer une règle de fréquence à un message {#apply-frequency-rule}

Pour appliquer une règle de fréquence à un message, procédez comme suit.

1. [Créez un message](../messages/get-started-content.md#create-new-message) en sélectionnant l’un des canaux que vous avez définis pour votre règle.

1. Sélectionnez la catégorie que vous avez définie pour la [règle que vous avez créée](#create-new-rule).

   ![](assets/inline-message-category.png)

   >[!NOTE]
   >
   >Actuellement, seule la variable **[!UICONTROL Marketing]** est disponible pour les règles de fréquence des messages.

   <!--
   1. You can click the **[!UICONTROL Frequency rule]** link to view the frequency rules that will apply for the selected category and channel(s). A new tab will open to display the matching message frequency rules.-->

1. Toutes les règles de fréquence correspondant à la catégorie et aux canaux sélectionnés seront automatiquement appliquées à ce message.

   >[!NOTE]
   >
   >Les messages <!--that do not have any selected category or messages -->où la catégorie sélectionnée est **[!UICONTROL Transactionnel]** ne seront pas évalués par rapport aux règles de fréquence.

   <!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

1. Vous pouvez visualiser le nombre de profils exclus de la diffusion dans le [rapport global](../reports/global-report.md) et dans le [rapport dynamique](../reports/live-report.md), où les règles de fréquence seront répertoriées comme une raison possible pour les utilisateurs exclus de la diffusion.

>[!NOTE]
>
>Plusieurs règles peuvent s’appliquer au même canal, mais une fois la limite inférieure atteinte, le profil sera exclu des prochaines diffusions.

## Exemple : combiner plusieurs règles {#frequency-rule-example}

Vous pouvez combiner plusieurs règles de fréquence des messages, comme décrit dans l’exemple ci-dessous.

1. [Créez une règle](#create-new-rule) appelée *Limitation marketing globale :*

   * Sélectionnez les canaux E-mail et Push.
   * Définissez la limitation sur 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Pour limiter davantage le nombre de notifications push marketing envoyées à un utilisateur, créez une deuxième règle appelée *Limitation Push marketing* :

   * Sélectionnez le canal push.
   * Définissez la limitation sur 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Enregistrez et [activez](#activate-rule) la règle.

1. Créez un e-mail et sélectionnez la catégorie **[!UICONTROL Marketing]** pour ce message. [En savoir plus](../messages/get-started-content.md#create-new-message)

1. Créez une notification push et sélectionnez la catégorie **[!UICONTROL Marketing]** pour ce message. [En savoir plus](../messages/get-started-content.md#create-new-message)

Dans ce scénario, un profil individuel :
* peut recevoir jusqu’à 12 messages marketing par mois ;
* mais sera exclu des notifications push marketing après avoir reçu 4 notifications push.

>[!NOTE]
>
>Lors du test des règles de fréquence, il est recommandé d’utiliser un nouveau [profil de test](../segment/creating-test-profiles.md), car une fois la limitation de fréquence d’un profil atteinte, il n’est pas possible de réinitialiser le compteur avant le mois suivant. La désactivation d’une règle permet aux profils limités de recevoir des messages, mais elle ne supprime pas les incréments de compteur.

## Vidéo pratique {#video}

Découvrez comment créer, activer, tester et générer des rapports sur les règles de fréquence.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
