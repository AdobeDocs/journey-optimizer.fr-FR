---
title: Création de préréglages de message
description: Découvrez comment configurer et surveiller les préréglages de message
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: f52f73b1d7f2ad5a7ebd2e8b23b7c68c4dc99212
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 70%

---


# Création de préréglages de message

Avec [!DNL Journey Optimizer], vous pouvez configurer des préréglages de message qui définissent tous les paramètres techniques requis pour les messages de notification par e-mail et push : type d&#39;e-mail, nom et adresse e-mail de l&#39;expéditeur, applications mobiles, etc.

>[!CAUTION]
>
> * La configuration des préréglages de message est limitée aux administrateurs de parcours. [En savoir plus](../administration/ootb-product-profiles.md#journey-administrator)
>
> * Vous devez effectuer les étapes de configuration E-mail et Push avant de créer des préréglages de message.


Une fois les préréglages de message configurés, vous pourrez les sélectionner dans la liste **[!UICONTROL Préréglages]** lors de la création de messages.

➡️ [Découvrez comment créer et utiliser des préréglages d’e-mail dans cette vidéo](#video-presets)

## Création d&#39;un préréglage de message {#create-message-preset}

Pour créer un préréglage de message, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Préréglages de message]**, puis cliquez sur **[!UICONTROL Créer un préréglage de message]**.

   ![](../assets/preset-create.png)

1. Saisissez un nom et une description (facultatif) pour le paramètre prédéfini, puis sélectionnez le ou les canaux à configurer.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Configurez les paramètres **email**.

   ![](../assets/preset-email.png)

   * Sélectionnez le type de message qui sera envoyé avec le paramètre prédéfini : **Transactionnel** ou **Marketing**.

      >[!CAUTION]
      >
      > Les messages **transactionnels** peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques, tels que la réinitialisation du mot de passe, le statut de la commande, la notification de diffusion, par exemple.

   * Sélectionnez le sous-domaine à utiliser pour envoyer les e-mails. [En savoir plus](about-subdomain-delegation.md)
   * Sélectionnez le pool d&#39;adresses IP à associer au paramètre prédéfini. [En savoir plus](ip-pools.md)
   * Saisissez les paramètres d’en-tête des emails envoyés à l’aide de ce paramètre prédéfini.

      >[!CAUTION]
      >
      >À l&#39;exception du champ **Répondre à (transférer l&#39;e-mail)**, le domaine des adresses e-mails doit utiliser le [sous-domaine délégué](about-subdomain-delegation.md).

      * **[!UICONTROL Nom de l&#39;expéditeur]** : nom de l&#39;expéditeur, tel que le nom de votre marque.

      * **[!UICONTROL E-mail de l&#39;expéditeur]** : adresse e-mail que vous souhaitez utiliser pour vos communications. Par exemple, si le sous-domaine délégué est *marketing.luma.com*, vous pouvez utiliser *contact@marketing.luma.com*.

      * **[!UICONTROL Répondre à (nom)]** : le nom qui sera utilisé lorsque le destinataire clique sur le bouton **Répondre** de son logiciel de messagerie.

      * **[!UICONTROL Répondre à (e-mail)]** : adresse e-mail qui sera utilisée lorsque le destinataire clique sur le bouton **Répondre** de son logiciel de messagerie. Les e-mails envoyés à cette adresse seront transférés à l&#39;adresse **[!UICONTROL Répondre à (transférer l&#39;e-mail)]** fournie ci-dessous. Vous devez utiliser une adresse définie sur le sous-domaine délégué (par exemple, *reply@marketing.luma.com*), sinon les e-mails seront ignorés.

      * **[!UICONTROL Répondre à (transférer l&#39;email)]** : tous les e-mails reçus par [!DNL Journey Optimizer] pour le sous-domaine délégué seront transférés vers cette adresse e-mail. Vous pouvez spécifier n&#39;importe quelle adresse, à l&#39;exception d&#39;une adresse e-mail définie sur le sous-domaine délégué. Par exemple, si le sous-domaine délégué est *marketing.luma.com*, toute adresse telle que *abc@marketing.luma.com* est interdite.

      * **[!UICONTROL Message d&#39;erreur]** : toutes les erreurs générées par les FAI après quelques jours de diffusion de l&#39;e-mail (bounces asynchrones) sont reçues sur cette adresse.

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

   * Configurez les **paramètres de reprise d’email**. Par défaut, la [période de reprise](retries.md#retry-duration) est définie sur 84 heures, mais vous pouvez ajuster ce paramètre pour mieux l’adapter à vos besoins.

      ![](../assets/preset-retry-paramaters.png)

      Vous devez saisir une valeur entière (en heures ou minutes) dans la plage suivante :
      * Pour le type d&#39;email marketing, la période de reprise minimale est de 6 heures.
      * Pour le type d’email transactionnel, la période de reprise minimale est de 10 minutes.
      * Pour les deux types d’email, la période de reprise maximale est de 84 heures (soit 5 040 minutes).


1. Configurez les paramètres **notification push** .

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

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](#monitor-message-presets).

1. Une fois les vérifications effectuées, le préréglage de message obtient le statut **[!UICONTROL Actif]**. Il est prêt à être utilisé pour diffuser des messages.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Surveillance des préréglages de message {#monitor-message-presets}

Tous vos préréglages de message s&#39;affichent dans le menu **[!UICONTROL Canaux]**/**[!UICONTROL Préréglages de message]**. Des filtres sont disponibles pour vous aider à parcourir la liste (type de canal, utilisateur, statut).

![](../assets/preset-filters.png)

Les préréglages de message peuvent avoir les statuts suivants :

* **[!UICONTROL Version préliminaire]** : le préréglage de message a été enregistré en tant que version préliminaire et n&#39;a pas encore été envoyé. Ouvrez-le pour reprendre la configuration.
* **[!UICONTROL Traitement]** : le préréglage de message a été envoyé et passe par plusieurs étapes de vérification.
* **[!UICONTROL Actif]** : le préréglage de message a été vérifié et peut être sélectionné pour créer des messages.
* **[!UICONTROL Échec]** : une ou plusieurs vérifications ont échoué lors de la vérification du préréglage de message.
* **[!UICONTROL Désactivé]** : le préréglage de message est désactivé. Il ne peut pas être utilisé pour créer de nouveaux messages.

En cas d’échec de la création d’un paramètre prédéfini de message, les détails de chaque raison d’échec possible sont décrits ci-dessous.

Si l’une de ces erreurs se produit, contactez l’[équipe d’assistance clientèle Adobe](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} pour obtenir de l’aide.

* **Échec** de la validation SPF : SPF (Sender Policy Framework) est un protocole d’authentification d’email qui permet de spécifier des adresses IP autorisées pouvant envoyer des emails à partir d’un sous-domaine donné.
L’échec de validation SPF signifie que les adresses IP contenues dans l’enregistrement SPF ne correspondent pas aux adresses IP utilisées pour envoyer les emails aux fournisseurs de messagerie.

* **Échec** de la validation DKIM : DKIM permet au serveur destinataire de vérifier que le message reçu a été envoyé par l&#39;expéditeur véritable du domaine associé et que le contenu du message d&#39;origine n&#39;a pas été modifié en cours de route.
L&#39;échec de validation DKIM signifie que les serveurs de messagerie de réception ne peuvent pas vérifier l&#39;authenticité du contenu du message et son association avec le domaine d&#39;envoi.

* **Échec** de la validation des enregistrements MX : L’échec de validation des enregistrements MX signifie que les serveurs de messagerie chargés d’accepter les emails entrants pour le compte d’un sous-domaine donné ne sont pas correctement configurés.

* **Les configurations de délivrabilité ont échoué** : L’échec des configurations de délivrabilité peut être dû à l’une des raisons suivantes :
   * Placer sur la liste bloquée les adresses IP allouées
   * Nom `helo` non valide
   * Emails envoyés à partir d’adresses IP autres que celles spécifiées dans le pool IP du paramètre prédéfini correspondant
   * Impossible de diffuser des emails vers les boîtes de réception des principaux FAI tels que Gmail et Yahoo

## Modifier les préréglages de message

Pour modifier un préréglage de message, vous devez d&#39;abord le désactiver afin de le rendre indisponible pour créer de nouveaux messages (les messages publiés l&#39;utilisant ne seront pas affectés et continueront à fonctionner). Vous devez ensuite dupliquer le préréglage de message pour créer une version que vous utiliserez pour créer de nouveaux messages :

1. Accédez à la liste des paramètres prédéfinis de message, puis désactivez le paramètre prédéfini de message que vous souhaitez modifier.

   ![](../assets/preset-deactivate.png)

1. Dupliquez le préréglage de message désactivé. Une copie avec le statut **[!UICONTROL Version préliminaire]** est automatiquement ajoutée à la liste.

   ![](../assets/preset-duplicated.png)

1. Ouvrez le préréglage de message dupliqué, modifiez-le selon vos besoins, puis soumettez vos modifications. Le préréglage de message passe par le même cycle de validation que lors de l&#39;[étape de création](#create-message-preset).

1. Une fois validé, il obtient le statut **[!UICONTROL Actif]** et est prêt à être utilisé pour créer de nouveaux messages.

   >[!NOTE]
   >
   >Les paramètres prédéfinis de message désactivés ne peuvent pas être supprimés pour éviter tout problème dans les parcours utilisant ces paramètres prédéfinis pour envoyer des messages.

## Vidéo pratique{#video-presets}

Découvrez comment créer des préréglages de message et les utiliser. Apprenez également comment déléguer un sous-domaine et créer un pool d’adresses IP.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
