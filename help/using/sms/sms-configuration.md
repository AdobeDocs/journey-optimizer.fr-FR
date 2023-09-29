---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal SMS
description: Découvrez comment configurer votre environnement pour envoyer des SMS avec Journey Optimizer.
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: b657f4380026988ac324ee87c96375734a9b3961
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 96%

---

# Configurer le canal SMS {#sms-configuration}

[!DNL Journey Optimizer] vous permet de créer vos parcours et dʼenvoyer des messages à une audience ciblée.

Avant d’envoyer des SMS, configurez votre instance. Vous devez [intégrer les paramètres du fournisseur](#create-api) avec Journey Optimizer et [créer une surface SMS](#message-preset-sms) (c.-à-d. un préréglage de SMS). Ces étapes doivent être exécutées par un [Administrateur système Adobe Journey Optimizer](../start/path/administrator.md).

## Conditions préalables{#sms-prerequisites}

Adobe Journey Optimizer s’intègre actuellement à des fournisseurs tiers tels que Sinch, Twilio et Infobip, qui offrent des services SMS indépendants d’Adobe Journey Optimizer.

Avant la configuration des SMS, vous devez créer un compte auprès de l’un de ces fournisseurs SMS afin de recevoir le jeton API et l’ID de service qui vous permettront d’établir la connexion entre Adobe Journey Optimizer et le fournisseur SMS approprié.

Votre utilisation des services SMS sera soumise aux conditions générales supplémentaires de la part du fournisseur de SMS concerné. Étant donné que Sinch et Twilio sont des produits tiers disponibles pour les utilisateurs d’Adobe Journey Optimizer via une intégration, pour tout problème ou toute demande liée aux services SMS, les utilisateurs de Sinch ou Twilio devront contacter le fournisseur de SMS approprié pour obtenir de l’aide. Adobe ne contrôle pas et n’est pas responsable des produits tiers.

>[!CAUTION]
>
>Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gestion des sous-domaines SMS]** dans le sandbox de production.

## Création d’informations d’identification API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurer votre fournisseur de SMS avec Journey Optimizer"
>abstract="Sélectionnez votre fournisseur et renseignez vos informations d’identification d’API SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurer votre fournisseur de SMS avec Journey Optimizer"
>abstract="Avant d’envoyer des SMS, vous devez intégrer les paramètres du fournisseur à Journey Optimizer. Une fois cette opération terminée, vous devrez créer une surface SMS. Ces étapes doivent être exécutées par un Administrateur système Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=fr#message-preset-sms" text="Création d’une surface de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Sélectionnez la configuration du fournisseur de SMS."
>abstract="Sélectionnez les informations d’identification d’API configurées pour votre fournisseur SMS."

Pour configurer votre fournisseur de SMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

   ![](assets/sms_6.png)

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

   * Pour **[!DNL Sinch]** :

      * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

      * **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]** : accédez à la page des API, puis à vos informations d’identification sous l’onglet SMS.  [En savoir plus](https://developers.sinch.com/docs/sms/getting-started/).

      * **[!UICONTROL Message d’inclusion]**: saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **[!UICONTROL Message d’inclusion]**.

      * **[!UICONTROL Message d’aide]**: saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **[!UICONTROL Message d’aide]**.

   * Pour **[!DNL Twilio]** :

      * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

      * **[!UICONTROL SID du compte]** et **[!UICONTROL Jeton d’authentification]** : accédez au volet Informations du compte de la page Tableau de bord de la console Twilio pour trouver vos informations d’identification.

      * **[!UICONTROL SID du message]** : saisissez l’identifiant unique attribué à chaque message créé par l’API de Twilio. [En savoir plus](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-).

   * Pour **[!DNL Infobip]** :

      * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

      * **[!UICONTROL URL de base de l’API]** et **[!UICONTROL Jeton API]** : accédez à la page d’accueil de votre interface web ou à la page de gestion des clés d’API pour trouver vos informations d’identification. [En savoir plus](https://www.infobip.com/docs/api).

   ![](assets/sms_7.png)

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal (c’est-à-dire un préréglage de message) pour les messages SMS.

## Créer une surface SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Définissez la catégorie de SMS."
>abstract="Sélectionnez le type de SMS utilisant cette surface : marketing pour les SMS promotionnels, qui nécessitent le consentement de l’utilisateur ou de l’utilisatrice, ou transactionnel pour les SMS non commerciaux, tels que la réinitialisation du mot de passe."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=fr#sms-opt-out-management" text="Se désinscrire dans les SMS de marketing"

Une fois votre canal SMS configuré, vous devez créer une surface de canal afin de pouvoir envoyer des SMS depuis **[!DNL Journey Optimizer]**.

Pour créer une surface de canal, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez **[!UICONTROL Branding]** > **[!UICONTROL Surfaces de canal]**. Cliquez sur le bouton **[!UICONTROL Créer une surface de canal]**.

   ![](assets/preset-create.png)

1. Saisissez un nom et une description (facultatif) pour la surface, puis sélectionnez le canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Définissez les **paramètres SMS**.

   ![](assets/preset-sms.png)

   * Sélectionnez le **[!UICONTROL Type de SMS]** qui sera envoyé avec la surface : **[!UICONTROL Transactionnel]** ou **[!UICONTROL Marketing]**.

      * Choisissez **Marketing** pour les SMS promotionnels : ces messages nécessitent le consentement de l’utilisateur ou de l’utilisatrice.
      * Choisissez **Transactionnel** pour les messages non commerciaux tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion, par exemple.

     >[!CAUTION]
     >
     >Les SMS **transactionnels** peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques.

     Lors de la création d’un SMS, vous devez choisir une surface de canal valide correspondant à la catégorie que vous avez sélectionnée pour votre message.

   * Sélectionnez la **[!UICONTROL Configuration SMS]** à associer à la surface.

     Pour plus dʼinformations sur la configuration de votre environnement pour envoyer des messages SMS, consultez [cette section](#create-api).

   * Saisissez le **[!UICONTROL Numéro dʼexpéditeur]** à utiliser lors de vos communications.

   * Sélectionnez votre **[!UICONTROL Champ d’exécution SMS]** pour sélectionner l’**[!UICONTROL Attribut de profil]** associé aux numéros de téléphone des profils.

1. Si vous souhaitez utiliser la fonction de raccourcissement des URL dans vos SMS, sélectionnez un élément de la liste **[!UICONTROL Sous-domaine]**.

   >[!NOTE]
   >
   >Avant de pouvoir sélectionner un sous-domaine, vous devez avoir configuré au moins un sous-domaine SMS. [Voici comment procéder.](sms-subdomains.md)

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer la surface de canal en tant que brouillon et reprendre sa configuration ultérieurement.

   ![](assets/sms_preset_2.png)
<!--
1. **[!UICONTROL Opt-out number]** But what we need to call out is that the opt-out is no longer at a channel level. Previously on receiving the opt-out keyword we used to opt-out the profile at the channel level. Now, we have made it short code specific. So if the customer is using multiple short codes within AJO to send out SMSs, they can continue to send messages to users from other shortcodes if the end user unsubscribes from 1.-->

1. Une fois la surface de canal créée, elle s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**.

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](#monitor-channel-surfaces).

1. Une fois les vérifications effectuées, la surface de canal obtient le statut **[!UICONTROL Actif]**. Elle est prête à être utilisée pour diffuser des messages.

   ![](assets/preset-active.png)

Vous êtes maintenant prêt à envoyer des messages SMS avec Journey Optimizer.

**Rubriques connexes**

* [Création d’un SMS](create-sms.md)
* [Ajouter un message dans un parcours](../building-journeys/journeys-message.md)
* [Ajouter un message dans une campagne](../campaigns/create-campaign.md)

