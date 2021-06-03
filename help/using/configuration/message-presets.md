---
title: Création de paramètres de message prédéfinis
description: Découvrez comment créer des paramètres prédéfinis de message de notification push et par email
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Création de paramètres de message prédéfinis

Avec [!DNL Journey Optimizer], vous pouvez configurer des paramètres prédéfinis de message qui définissent tous les paramètres techniques requis pour les emails et les notifications push (type d’email, nom et adresse email de l’expéditeur, applications mobiles, etc.).

Vous pouvez configurer autant de paramètres prédéfinis de message que vous le souhaitez, en fonction des différentes marques pour lesquelles vous devez communiquer.

Une fois les paramètres prédéfinis de message configurés, vous pouvez les sélectionner lors de la création de messages à partir de la liste **[!UICONTROL Paramètres prédéfinis]**.

## Créer un paramètre prédéfini de message {#create-message-preset}

Pour créer un paramètre prédéfini de message, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]** / **[!UICONTROL Paramètres de message prédéfinis]**, puis cliquez sur **[!UICONTROL Créer un paramètre de message prédéfini]**.

   ![](../assets/preset-create.png)

1. Attribuez un nom et une description (facultatif) au paramètre prédéfini, puis spécifiez le ou les canaux à configurer.

   ![](../assets/preset-general.png)

1. Configurez les paramètres de l&#39;email et de la notification push :

   Pour le canal Email, spécifiez :

   * le type de communication qui sera envoyé avec le paramètre prédéfini (messages transactionnels ou marketing),
   * Le [sous-domaine](about-subdomain-delegation.md) à utiliser pour envoyer les emails,
   * Le [pool IP](ip-pools.md) à associer au paramètre prédéfini,
   * Paramètres d’en-tête à utiliser pour les emails envoyés à l’aide du paramètre prédéfini.

   ![](../assets/preset-email.png)

   Pour le canal Notification push, spécifiez les applications mobiles IOS et/ou Android à utiliser pour vos messages. Pour plus d&#39;informations sur la configuration de votre environnement pour envoyer des notifications push, consultez [cette section](../push-configuration.md).

   ![](../assets/preset-push.png)

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer le paramètre prédéfini de message en tant que brouillon et reprendre sa configuration ultérieurement.

   ![](../assets/preset-submit.png)

1. Une fois le paramètre prédéfini de message créé, il s’affiche dans la liste avec l’état **[!UICONTROL Traitement]**.

   Au cours de cette étape, plusieurs vérifications seront effectuées afin de vérifier qu’il a été correctement configuré. Le temps de traitement est d’environ 48h à 72h, et peut prendre jusqu’à 7 à 10 jours.

   Ces contrôles incluent les tests de délivrabilité effectués par l’équipe de délivrabilité d’Adobe :

   * validation SPF,
   * Validation DKIM,
   * Validation des enregistrements MX,
   * Vérifier la placée sur la liste bloquée des adresses IP,
   * Vérification de l’hôte Helo,
   * vérification du pool d’adresses IP,
   * Enregistrement A/PTR, vérification du sous-domaine t/m/res.

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