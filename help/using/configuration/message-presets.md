---
title: Création de préréglages de message
description: Découvrez comment configurer et surveiller les préréglages de message
feature: Paramétrage de l’application
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 71%

---


# Création de préréglages de message

Avec [!DNL Journey Optimizer], vous pouvez configurer des préréglages de message qui définissent tous les paramètres techniques requis pour les messages de notification par e-mail et push : type d&#39;e-mail, nom et adresse e-mail de l&#39;expéditeur, applications mobiles, etc.

>[!CAUTION]
>
> * La configuration des préréglages de message est limitée aux administrateurs de parcours. [En savoir plus](../administration/ootb-product-profiles.md#journey-administrator)
   >
   > 
* Vous devez effectuer les étapes de configuration Email et Push avant de créer des paramètres prédéfinis de message.


Une fois les préréglages de message configurés, vous pourrez les sélectionner dans la liste **[!UICONTROL Paramètres prédéfinis]** lors de la création de messages.

![](../assets/do-not-localize/how-to-video.png) [Découvrez comment créer et utiliser des paramètres prédéfinis d’email dans cette vidéo](#video-presets)

## Création d&#39;un préréglage de message {#create-message-preset}

Pour créer un préréglage de message, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Préréglages de message]**, puis cliquez sur **[!UICONTROL Créer un préréglage de message]**.

   ![](../assets/preset-create.png)

1. Saisissez un nom et une description (facultatif) pour le paramètre prédéfini, puis sélectionnez le ou les canaux à configurer.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Configurez les paramètres d&#39;**e-mail**.

   ![](../assets/preset-email.png)

   * Sélectionnez le type de message qui sera envoyé avec le paramètre prédéfini : **Transactionnel** ou **Marketing**.

      >[!CAUTION]
      >
      > Les messages **transactionnels** peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques, tels que la réinitialisation du mot de passe, le statut de la commande, la notification de diffusion, par exemple.

   * Sélectionnez le sous-domaine à utiliser pour envoyer les e-mails. [En savoir plus](about-subdomain-delegation.md)
   * Sélectionnez le pool d&#39;adresses IP à associer au paramètre prédéfini. [En savoir plus](ip-pools.md)
   * Renseignez les paramètres d&#39;en-tête des e-mails envoyés à l&#39;aide du paramètre prédéfini.

      >[!CAUTION]
      >
      >À l’exception du champ **Répondre à (courrier électronique de transfert)** , le domaine des adresses électroniques doit utiliser le [sous-domaine délégué](about-subdomain-delegation.md) sélectionné actuellement.

      * **[!UICONTROL Nom]** de l&#39;expéditeur : Nom de l’expéditeur, tel que le nom de votre marque.

      * **[!UICONTROL Email de l&#39;expéditeur]** : Adresse électronique que vous souhaitez utiliser pour vos communications. Par exemple, si le sous-domaine délégué est *marketing.luma.com*, vous pouvez utiliser *contact@marketing.luma.com*.

      * **[!UICONTROL Réponse (nom)]** : Nom qui sera utilisé lorsque le destinataire clique sur le bouton  **** Répondre de son logiciel de messagerie.

      * **[!UICONTROL Répondre à (email)]** : Adresse électronique qui sera utilisée lorsque le destinataire clique sur le bouton  **** Répondre de son logiciel de messagerie. Les emails envoyés à cette adresse seront transférés à l&#39;adresse **[!UICONTROL Réponse (email de transfert)]** fournie ci-dessous. Vous devez utiliser une adresse définie sur le sous-domaine délégué (par exemple, *reply@marketing.luma.com*), sinon les emails seront ignorés.

      * **[!UICONTROL Répondre à (transférer l&#39;email)]** : Tous les emails reçus par  [!DNL Journey Optimizer] pour le sous-domaine délégué seront transférés vers cette adresse email. Vous pouvez spécifier n’importe quelle adresse, à l’exception d’une adresse électronique définie sur le sous-domaine délégué. Par exemple, si le sous-domaine délégué est *marketing.luma.com*, toute adresse telle que *abc@marketing.luma.com* est interdite.

      * **[!UICONTROL Message d’erreur]** : Toutes les erreurs générées par les FAI après quelques jours de diffusion du courrier (bounces asynchrones) sont reçues sur cette adresse.

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.


1. Configurez les paramètres de **notification push**.

   ![](../assets/preset-push.png)

   * Sélectionnez au moins une plateforme : **iOS** et/ou **Android**.

   * Sélectionnez les applications mobiles à utiliser pour chaque plateforme.

      Pour plus d&#39;informations sur la configuration de votre environnement pour envoyer des notifications push, consultez [cette section](../push-gs.md).

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer le préréglage de message en tant que version préliminaire et reprendre sa configuration ultérieurement.

   ![](../assets/preset-submit.png)

1. Une fois le préréglage de message créé, il s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**.

   Au cours de cette étape, plusieurs vérifications seront effectuées afin de vérifier qu&#39;il a été correctement configuré. Le temps de traitement est d&#39;environ **48 h-72 h** et peut prendre jusqu&#39;à **7-10 jours**.

   Ces contrôles incluent les tests de délivrabilité effectués par l&#39;équipe chargée de la délivrabilité d&#39;Adobe :

   * Validation SPF
   * Validation DKIM
   * Validation des enregistrements MX
   * Vérification de la liste bloquée des adresses IP
   * Vérification de l&#39;hôte Helo
   * Vérification du pool d&#39;adresses IP
   * Enregistrement A/PTR, vérification du sous-domaine t/m/res

1. Une fois les vérifications effectuées, le paramètre de message prédéfini obtient le statut **[!UICONTROL Principal]**. Il est prêt à être utilisé pour diffuser des messages.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Surveillance des préréglages de message

Tous vos préréglages de message s&#39;affichent dans le menu **[!UICONTROL Canaux]**/**[!UICONTROL Préréglages de message]**. Des filtres sont disponibles pour vous aider à parcourir la liste (type de canal, utilisateur, statut).

![](../assets/preset-filters.png)

Les préréglages de message peuvent avoir les statuts suivants :

* **[!UICONTROL Version préliminaire]** : le préréglage de message a été enregistré en tant que version préliminaire et n&#39;a pas encore été envoyé. Ouvrez-le pour reprendre la configuration.
* **[!UICONTROL Traitement]** : le préréglage de message a été envoyé et passe par plusieurs étapes de vérification.
* **[!UICONTROL Actif]** : le préréglage de message a été vérifié et peut être sélectionné pour créer des messages.
* **[!UICONTROL Échec]** : une ou plusieurs vérifications ont échoué lors de la vérification du préréglage de message.
* **[!UICONTROL Désactivé]** : le préréglage de message est désactivé. Il ne peut pas être utilisé pour créer de nouveaux messages.

## Modifier les préréglages de message

Pour modifier un préréglage de message, vous devez d&#39;abord le désactiver afin de le rendre indisponible pour créer de nouveaux messages (les messages publiés l&#39;utilisant ne seront pas affectés et continueront à fonctionner). Vous devez ensuite dupliquer le préréglage de message pour créer une version que vous utiliserez pour créer de nouveaux messages :

1. Accédez à la liste des préréglages de message, puis désactivez le préréglage de message que vous souhaitez modifier.

   ![](../assets/preset-deactivate.png)

1. Dupliquez le préréglage de message désactivé. Une copie avec le statut **[!UICONTROL Version préliminaire]** est automatiquement ajoutée à la liste.

   ![](../assets/preset-duplicated.png)

1. Ouvrez le préréglage de message dupliqué, modifiez-le selon vos besoins, puis soumettez vos modifications. Le préréglage de message passe par le même cycle de validation que lors de l&#39;[étape de création](#create-message-preset).

1. Une fois validé, il obtient le statut **[!UICONTROL Actif]** et est prêt à être utilisé pour créer de nouveaux messages.

   >[!NOTE]
   >
   >Les préréglages de message désactivés ne peuvent pas être supprimés afin d&#39;éviter tout problème dans les parcours les utilisant pour envoyer des messages.

## Vidéo pratique{#video-presets}

Découvrez comment créer des paramètres prédéfinis de message, comment les utiliser et comment déléguer un sous-domaine et créer un pool d’adresses IP.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
