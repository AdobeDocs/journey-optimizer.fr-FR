---
solution: Journey Optimizer
product: journey optimizer
title: Règles commerciales
description: Découvrir comment définir des règles de fréquence
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: message, fréquence, règles, pression
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 100%

---

# Règles commerciales {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="Règles commerciales"
>abstract="Les règles de fréquence des messages sont un type de règle commerciale qui limite le nombre de fois où les utilisateurs et les utilisatrices reçoivent des messages ou entrent dans des parcours via un ou plusieurs canaux. Ces règles cross-canal excluent automatiquement des messages et des actions les profils sur-sollicités."

[!DNL Journey Optimizer] vous permet de contrôler la fréquence à laquelle les utilisateurs et les utilisatrices reçoivent un message ou entrent dans un parcours via un ou plusieurs canaux. Règles de fréquence des messages qui excluent automatiquement des messages et des actions les profils sur-sollicités.

Par exemple, pour une marque, une règle peut être de ne pas envoyer plus de 4 messages marketing par mois à sa clientèle. Pour cela, vous pouvez utiliser une règle commerciale qui limite le nombre de messages envoyés sur un ou plusieurs canaux au cours d’une période calendaire mensuelle.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>Les règles métier sont différentes de la gestion des désinscriptions, qui permet aux utilisateurs et utilisatrices de se désinscrire de la réception des communications de la part d’une marque. [En savoir plus](../privacy/opt-out.md#opt-out-management)

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Accéder aux règles commerciales {#access-rules}

Les règles commerciales sont disponibles à partir du menu **[!UICONTROL Administration]** > **[!UICONTROL Règles commerciales]**. Toutes les règles sont répertoriées, triées par date de modification. Utilisez l&#39;icône de filtre pour filtrer par catégorie, statut et/ou canal. Vous pouvez également effectuer une recherche sur le libellé du message.

![](assets/message-rules-filter.png)

### Autorisations{#permissions-frequency-rules}

Pour accéder aux règles commerciales, en créer, les modifier ou les supprimer, vous devez disposer de l’autorisation **[!UICONTROL Gérer les règles commerciales]**.

Les utilisateurs avec l’autorisation **[!UICONTROL Afficher les règles de fréquence]** peuvent afficher les règles, mais pas les modifier ni les supprimer.

![](assets/message-rules-access.png)

Pour en savoir plus sur les autorisations, consultez [cette section](../administration/high-low-permissions.md).

## Créer une règle commerciale {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Sélectionner la catégorie de règle relative aux messages"
>abstract="Lorsqu’elle sont activées et appliquées à un message, toutes les règles commerciales correspondant à la catégorie sélectionnée seront automatiquement appliquées à ce message. Actuellement, seule la catégorie Marketing est disponible."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Définir la limitation de votre règle commerciale"
>abstract="Spécifiez le nombre maximal de messages envoyés à un profil client au cours de la période choisie. La limite de fréquence sera basée sur la période calendaire sélectionnée et sera réinitialisée au début de la période correspondante."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Définissez le ou les canaux auxquels la règle commerciale s’applique."
>abstract="Sélectionnez au moins un canal. Le plafond est calculé sur l’ensemble des canaux."

Pour créer une règle commerciale, procédez comme suit.

1. Accédez à la liste **[!UICONTROL Règles commerciales]**, puis cliquez sur **[!UICONTROL Créer une règle]**.

   ![](assets/message-rules-create.png)

1. Définissez le nom de la règle et sélectionnez la catégorie de la règle relative aux messages.

   >[!NOTE]
   >
   >Seule la catégorie **[!UICONTROL Marketing]** est disponible.

   ![](assets/message-rules-details.png)

1. Dans la liste déroulante **[!UICONTROL Durée]**, sélectionnez une période pour la limitation à appliquer. [En savoir plus](#frequency-cap)

1. Définissez la limitation de votre règle, c’est-à-dire le nombre maximum de messages qui peuvent être envoyés à un profil individuel chaque mois ou chaque semaine <!--or day-->, en fonction de votre sélection ci-dessous.

   <!--![](assets/message-rules-capping.png)-->

1. Sélectionnez le canal à utiliser pour cette règle : **[!UICONTROL E-mail]**, **[!UICONTROL Notification push]**, **[!UICONTROL SMS]** ou **[!UICONTROL Courrier]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Vous devez sélectionner au moins un canal pour pouvoir créer la règle.

1. Sélectionnez plusieurs canaux si vous souhaitez appliquer une limitation sur tous les canaux sélectionnés en tant que nombre total.

   Par exemple, définissez la limitation sur 15 et sélectionnez les canaux e-mail et push. Si un profil a déjà reçu 10 e-mails marketing et 5 notifications push marketing pour la période sélectionnée, ce profil sera exclu de la prochaine diffusion de tout e-mail ou notification push marketing.

1. Cliquez sur **[!UICONTROL Enregistrer comme brouillon]** pour confirmer la création de la règle. Votre message est ajouté à la liste de règles, dans l&#39;état **[!UICONTROL Brouillon]**.

   ![](assets/message-rules-created.png)

### Limite de fréquence {#frequency-cap}

Dans la liste déroulante **[!UICONTROL Durée]**, sélectionnez si vous souhaitez que la limitation soit appliquée tous les mois ou toutes les semaines.

>[!NOTE]
>
>Une limite de fréquence quotidienne est également disponible à la demande. [En savoir plus](#daily-frequency-cap)

La limite de fréquence est basée sur la période calendaire sélectionnée. Elle est réinitialisée au début de la période correspondante.

![](assets/message-rules-capping-duration.png)

L’expiration du compteur pour chaque période se présente comme suit :

* **[!UICONTROL Mensuelle]** : la limite de fréquence est valable jusqu’au dernier jour du mois à 23:59:59 UTC. Par exemple, la date d’expiration mensuelle pour janvier est le 31 janvier à 23:59:59 UTC.

* **[!UICONTROL Hebdomadaire]** : la limite de fréquence est valable jusqu’au samedi à 23:59:59 UTC de cette semaine, car la semaine calendaire commence le dimanche. L’expiration est indépendante de la création de la règle. Par exemple, si la règle est créée le jeudi, cette règle est valide jusqu’au samedi à 23:59:59.

### Limite de fréquence quotidienne {#daily-frequency-cap}

Outre les fréquences mensuelle et hebdomadaire, un limite de fréquence quotidienne est également disponible à la demande. Pour en savoir plus sur celle-ci, contactez votre représentant ou représentante Adobe.

La limite de fréquence quotidienne est valable pour la journée jusqu’à 23:59:59 UTC et est réinitialisée à 0 au début de la journée suivante.

>[!NOTE]
>
>Pour garantir la précision des règles de capping de la fréquence quotidienne, nous vous recommandons d’utiliser la méthode [Segmentation en streaming](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=fr){target="_blank"}. En savoir plus sur les méthodes d’évaluation de l’audience dans [cette section](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Activer une règle commerciale {#activate-rule}

Une fois créée, la règle commerciale affiche le statut **[!UICONTROL Brouillon]** et n’a encore aucune incidence sur le message. Pour l’activer, cliquez sur les points de suspension en regard de la règle et sélectionnez **[!UICONTROL Activer]**.

![](assets/message-rules-activate.png)

L&#39;activation d&#39;une règle aura un impact sur tous les messages auxquels elle s&#39;applique lors de leur exécution suivante. Découvrez comment [appliquer une règle commerciale à un message](#apply-frequency-rule).

>[!NOTE]
>
>L’activation complète d’une règle peut prendre jusqu’à 10 minutes. Vous n’avez pas besoin de modifier des messages ou de republier des parcours pour qu’une règle prenne effet.

Pour désactiver une règle commerciale, cliquez sur les points de suspension en regard de la règle et sélectionnez **[!UICONTROL Désactiver]**.

![](assets/message-rules-deactivate.png)

L&#39;état de la règle devient **[!UICONTROL Inactif]** et la règle ne s&#39;appliquera pas aux futures exécutions de messages. Les messages en cours d&#39;exécution ne seront pas affectés.

>[!NOTE]
>
>La désactivation d&#39;une règle n&#39;affecte ou ne réinitialise aucun comptage sur les profils individuels.

## Appliquer une règle commerciale à un message {#apply-frequency-rule}

Pour appliquer une règle commerciale à un message, procédez comme suit.

1. Lors de la création d’un [parcours](../building-journeys/journey-gs.md), ajoutez un message en sélectionnant l’un des canaux que vous avez définis pour votre règle.

1. Sélectionnez la catégorie que vous avez définie pour la [règle que vous avez créée](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Actuellement, seule la catégorie **[!UICONTROL Marketing]** est disponible pour les règles commerciales.

1. Cliquez sur le lien **[!UICONTROL Règle de fréquence]** pour ouvrir l’écran des règles de fréquence dans un nouvel onglet. [En savoir plus](#access-rules).

   Toutes les règles commerciales correspondant à la catégorie et aux canaux sélectionnés seront automatiquement appliquées à ce message.

   >[!NOTE]
   >
   >Les messages pour lesquels la catégorie sélectionnée est **[!UICONTROL Transactionnel]** ne seront pas évalués par rapport aux règles de fréquence.

1. Vous pouvez visualiser le nombre de profils exclus de la diffusion dans le [rapport Customer Journey Analytics](../reports/report-gs-cja.md) et dans le [rapport dynamique](../reports/live-report.md), où les règles de fréquence seront répertoriées comme une raison possible pour les personnes exclues de la diffusion.

>[!NOTE]
>
>Plusieurs règles peuvent s’appliquer au même canal, mais une fois la limite inférieure atteinte, le profil sera exclu des prochaines diffusions.

## Exemple : combiner plusieurs règles {#frequency-rule-example}

Vous pouvez combiner plusieurs règles commerciales, comme décrit dans l’exemple ci-dessous.

1. [Créez une règle commerciale](#create-new-rule) appelée *Limitation marketing globale* :

   * Sélectionnez tous les canaux.
   * Définissez la limitation mensuelle sur 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Pour limiter davantage le nombre de notifications push marketing envoyées à un utilisateur, créez une deuxième règle appelée *Limitation Push marketing* :

   * Sélectionnez le canal push.
   * Définissez la limitation mensuelle sur 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Enregistrez et [activez](#activate-rule) la règle.

1. [Créez un message](../building-journeys/journeys-message.md) pour chaque canal par lequel vous souhaitez communiquer et sélectionnez la catégorie **[!UICONTROL Marketing]** pour chaque message. [Découvrir comment appliquer une règle commerciale](#apply-frequency-rule)

   ![](assets/journey-message-category.png)


<!--
Learn how to create a message for the different channels in the following sections:
* [Create an email](../email/create-email.md)
* [Create a push notification](../push/create-push.md)
* [Create an SMS](../sms/create-sms.md)
* [Create a direct mail](../direct-mail/create-direct-mail.md)

Create an email and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../email/create-email.md)

Create a push notification and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../push/create-push.md)

Create an SMS and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../sms/create-sms.md)

Create a direct mail and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../direct-mail/create-direct-mail.md)
-->

Dans ce scénario, un profil individuel :
* peut recevoir jusqu’à 12 messages marketing par mois ;
* mais sera exclu des notifications push marketing après avoir reçu 4 notifications push.

>[!NOTE]
>
>Lors du test des règles commerciales, il est recommandé d’utiliser un nouveau [profil de test](../audience/creating-test-profiles.md), car une fois la limitation de fréquence d’un profil atteinte, il n’est pas possible de réinitialiser le compteur avant le mois suivant. La désactivation d’une règle permet aux profils limités de recevoir des messages, mais elle ne supprime pas les incréments de compteur.

## Vidéo pratique {#video}

Découvrez comment créer, activer, tester et générer des rapports sur les règles commerciales.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
