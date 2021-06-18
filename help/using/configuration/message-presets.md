---
title: Création de préréglages de message
description: Découvrez comment configurer et surveiller les paramètres prédéfinis de message
feature: Paramétrage de l’application
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: 705aa4c238eb1d6d6ce46b68f8690f639124a090
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 1%

---


# Création de préréglages de message

Avec [!DNL Journey Optimizer], vous pouvez configurer des paramètres prédéfinis de message qui définissent tous les paramètres techniques requis pour les messages de notification électronique et push : type de courrier électronique, nom et adresse électronique de l’expéditeur, applications mobiles, etc.

>[!CAUTION]
>
> * La configuration des paramètres de message prédéfinis est limitée aux administrateurs de Parcours. [En savoir plus](../administration/ootb-product-profiles.md#journey-administrator)
   >
   > 
* Vous devez effectuer les étapes de configuration Email et Push avant de créer des paramètres prédéfinis de message.


Une fois les paramètres prédéfinis de message configurés, vous pouvez les sélectionner lors de la création de messages à partir de la liste **[!UICONTROL Paramètres prédéfinis]**.

## Créer un paramètre prédéfini de message {#create-message-preset}

Pour créer un paramètre prédéfini de message, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]** / **[!UICONTROL Paramètres de message prédéfinis]**, puis cliquez sur **[!UICONTROL Créer un paramètre de message prédéfini]**.

   ![](../assets/preset-create.png)

1. Saisissez un nom et une description (facultatif) pour le paramètre prédéfini, puis sélectionnez le ou les canaux à configurer.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Elle ne peut contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d’union `-`.

1. Configurez les paramètres **email**.

   ![](../assets/preset-email.png)

   * Sélectionnez le type de message qui sera envoyé avec le paramètre prédéfini : **Transactionnel** ou **Marketing**

      >[!CAUTION]
      >
      > **** Les messages transactionnels peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques, tels que la réinitialisation du mot de passe, l’état de la commande, la notification de diffusion, par exemple.

   * Sélectionnez le sous-domaine à utiliser pour envoyer les emails. [En savoir plus](about-subdomain-delegation.md)
   * Sélectionnez le pool d’adresses IP à associer au paramètre prédéfini. [En savoir plus](ip-pools.md)
   * Renseignez les paramètres d&#39;en-tête des emails envoyés à l&#39;aide du paramètre prédéfini.

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
      >Les noms doivent commencer par une lettre (A-Z). Elle ne peut contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d’union `-`.


1. Configurez les paramètres **notification push**.

   ![](../assets/preset-push.png)

   * Sélectionnez au moins une plateforme : **iOS** et/ou **Android**

   * Sélectionnez les applications mobiles à utiliser pour chaque plateforme.

      Pour plus d&#39;informations sur la configuration de votre environnement pour envoyer des notifications push, consultez [cette section](../push-gs.md).

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer le paramètre prédéfini de message en tant que brouillon et reprendre sa configuration ultérieurement.

   ![](../assets/preset-submit.png)

1. Une fois le paramètre prédéfini de message créé, il s’affiche dans la liste avec l’état **[!UICONTROL Traitement]**.

   Au cours de cette étape, plusieurs vérifications seront effectuées afin de vérifier qu’il a été correctement configuré. Le temps de traitement est d’environ **48h-72h** et peut prendre jusqu’à **7-10 jours**.

   Ces contrôles incluent les tests de délivrabilité effectués par l’équipe de délivrabilité d’Adobe :

   * Validation SPF
   * Validation DKIM
   * Validation des enregistrements MX
   * Vérifier l’liste bloquée des adresses IP
   * Vérification de l’hôte Helo
   * Vérification du pool d’adresses IP
   * Enregistrement A/PTR, vérification du sous-domaine t/m/res

1. Une fois les vérifications effectuées, le paramètre prédéfini du message obtient le statut **[!UICONTROL Principal]**. Il est prêt à être utilisé pour diffuser des messages.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Surveillance des paramètres prédéfinis de message

Tous vos paramètres prédéfinis de message s’affichent dans le menu **[!UICONTROL Canaux]** / **[!UICONTROL Paramètres prédéfinis de message]** . Des filtres sont disponibles pour vous aider à parcourir la liste (type de canal, utilisateur, statut).

![](../assets/preset-filters.png)

Les paramètres de message prédéfinis peuvent avoir les états suivants :

* **[!UICONTROL Version préliminaire]** : Le paramètre prédéfini du message a été enregistré en tant que brouillon et n’a pas encore été envoyé. Ouvrez-le pour reprendre la configuration.
* **[!UICONTROL Traitement]** : Le paramètre prédéfini du message a été envoyé et passe par plusieurs étapes de vérification.
* **[!UICONTROL Principal]** : Le paramètre prédéfini du message a été vérifié et peut être sélectionné pour créer des messages.
* **[!UICONTROL Échec]** : Une ou plusieurs vérifications ont échoué lors de la vérification du paramètre prédéfini du message.
* **[!UICONTROL Désactivé]** : Le paramètre prédéfini du message est désactivé. Il ne peut pas être utilisé pour créer de nouveaux messages.

## Modifier les paramètres prédéfinis de message

Pour modifier un paramètre prédéfini de message, vous devez d’abord le désactiver afin de le rendre indisponible pour créer de nouveaux messages (les messages publiés utilisant ce paramètre prédéfini ne seront pas affectés et continueront à fonctionner). Vous devez ensuite dupliquer le paramètre prédéfini de message pour créer une version que vous utiliserez pour créer de nouveaux messages :

1. Accédez à la liste des paramètres prédéfinis de message, puis désactivez le paramètre prédéfini de message que vous souhaitez modifier.

   ![](../assets/preset-deactivate.png)

1. Dupliquez le paramètre prédéfini de message désactivé. Une copie avec le statut **[!UICONTROL Brouillon]** est automatiquement ajoutée à la liste.

   ![](../assets/preset-duplicated.png)

1. Ouvrez le paramètre prédéfini de message dupliqué, modifiez-le selon vos besoins, puis soumettez vos modifications. Le paramètre prédéfini de message passe par le même cycle de validation que lors de l’[étape de création](#create-message-preset).

1. Une fois validé, il obtient le statut **[!UICONTROL Principal]** et est prêt à être utilisé pour créer de nouveaux messages.

   >[!NOTE]
   >
   >Les paramètres prédéfinis de message désactivés ne peuvent pas être supprimés pour éviter tout problème dans les parcours utilisant ces paramètres prédéfinis pour envoyer des messages.

