---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal WhatsApp
description: Découvrez comment configurer votre environnement pour envoyer des messages WhatsApp avec Journey Optimizer.
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: d71dfb4f791c48997e448147b414fede49023b91
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 65%

---

# Commencer la configuration WhatsApp  {#whatsapp-config}

>[!BEGINSHADEBOX]

**Table des matières**

* [Commencer avec les messages WhatsApp](get-started-whatsapp.md)
* **[Commencer la configuration de WhatsApp](whatsapp-configuration.md)**
* [Créer un message WhatsApp](create-whatsapp.md)
* [Vérifier et envoyer vos messages WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Avant d’envoyer un message WhatsApp, vous devez configurer votre environnement Adobe Journey Optimizer et l’associer à votre compte WhatsApp. Pour ce faire, procédez comme suit :

1. [Créez vos informations d’identification d’API WhatsApp.](#WhatsApp-credentials)
1. [Créer vos Webhooks WhatsApp](#WhatsApp-webhook)
1. [Créez une configuration de WhatsApp.](#WhatsApp-configuration)

Ces étapes doivent être exécutées par un [Administrateur ou une Administratrice système](../start/path/administrator.md) Adobe Journey Optimizer.

## Créer des informations d’identification d’API WhatsApp {#whatsapp-credentials}

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification dʼAPI comme indiqué ci-dessous :

   * **Jeton API** : saisissez votre jeton API. Pour en savoir plus, consultez la [documentation Meta](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/).
   * **ID de compte professionnel** : saisissez le numéro unique associé à votre porfolio professionnel. Pour en savoir plus, consultez la [documentation Meta](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Cliquez sur **[!UICONTROL Continuer]**.

1. Choisissez le **Compte professionnel** que vous souhaitez connecter à vos informations d’identification d’API WhatsApp.

   ![](assets/whatsapp-api-2.png)

1. Sélectionnez le **Nom de l’expéditeur** utilisé pour envoyer vos messages Whatsapp.

1. Les paramètres de votre numéro de téléphone sont automatiquement renseignés :

   * **Évaluation de la qualité** : reflète les commentaires de la clientèle sur les messages envoyés au cours des dernières 24 heures.
      * Vert : haute qualité
      * Jaune : qualité moyenne
      * Rouge : faible qualité

     En savoir plus sur l’[évaluation de la qualité](https://www.facebook.com/business/help/766346674749731#).

   * **Débit** : indique la vitesse à laquelle votre numéro de téléphone peut envoyer des messages.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

Après avoir créé et configuré vos informations d’identification d’API, vous devez créer une configuration des canaux pour les messages WhatsApp. [En savoir plus](#whatsapp-configuration)

## Créer un webhook {#WhatsApp-webhook}

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword_category"
>title="Catégorie de mots-clés entrants"
>abstract="<br/><b>Opt-in</b> : envoie votre réponse automatique définie lorsqu’un utilisateur s’abonne. <br/><b>Opt-out</b> : envoie votre réponse automatique définie lorsqu’un utilisateur se désabonne. <br/><b>Aide</b> : envoie votre réponse automatique définie lorsqu’un utilisateur demande de l’aide ou de l’assistance. <br/><b>Par défaut</b> : envoie votre réponse automatique de secours lorsqu’aucun mot-clé ne correspond."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword"
>title="Entrez vos mots-clés"
>abstract= "You can define keywords to trigger specific auto-responses, such as for Opt-In, Opt-Out, Help, or Default, based on what users text. Keywords are not case-sensitive, e.g., "stop" and "STOP" are treated the same."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_webhook_url"
>title=" URL de rappel"
>abstract="La demande de validation et les notifications webhook pour cet objet sont envoyées à l’URL spécifiée."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_verify_token"
>title="Vérifier le jeton"
>abstract="Jeton renvoyé par Meta pour confirmer et vérifier l’URL de rappel pendant le processus de vérification."

>[!NOTE]
>
>Sans mots-clés de souscription ou d’exclusion spécifiés, les messages de consentement standard ne sont pas activés.

Une fois vos identifiants d&#39;API WhatsApp et vos Webhooks [Meta](https://developers.facebook.com/docs/whatsapp/webhooks/) créés, l&#39;étape suivante consiste à créer un webhook et à configurer vos paramètres entrants.

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]**, sélectionnez le menu **[!UICONTROL WhatsApp Webhooks]** sous **[!UICONTROL Paramètres de WhatsApp]**, puis cliquez sur le bouton **[!UICONTROL Créer Webhook]**.

1. Saisissez un [!UICONTROL Nom] pour votre webhook.

1. Dans la liste déroulante, sélectionnez les [ Informations d’identification de l’API ](#whatsapp-credentials) vous avez créées précédemment.

1. Cliquez sur ![ajouter](assets/do-not-localize/Smock_AddCircle_18_N.svg) pour commencer à configurer une **[!UICONTROL catégorie de mots-clés entrante]** telle que :

   * **[!UICONTROL Mots-clés d’accord préalable]**
   * **[!UICONTROL Mots-clés de droit d’opposition]**
   * **[!UICONTROL Mots-clés d’aide]**

1. Saisissez votre **[!UICONTROL Mot-clé]**.

   Pour ajouter plusieurs mots-clés, cliquez sur ![ajouter](assets/do-not-localize/Smock_AddCircle_18_N.svg).

1. Spécifiez le **[!UICONTROL Message de réponse]** envoyer lorsqu’un mot-clé configuré est reçu.

<!--
1. Click **[!UICONTROL View payload editor]** to validate and customize your request payloads. 
    
    You can dynamically personalize your payload using profile attributes, and ensure accurate data is sent for processing and response generation with the help of built-in helper functions.
-->

1. Cliquez sur **[!UICONTROL Soumettre]** lorsque vous avez terminé la configuration de votre Webhook WhatsApp.

1. Dans le menu **[!UICONTROL Webhooks]**, cliquez sur l&#39;icône ![bin](assets/do-not-localize/Smock_Delete_18_N.svg) pour supprimer votre Webhook WhatsApp.

1. Pour modifier la configuration existante, recherchez le webhook souhaité et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

1. Accédez à votre nouvelle **[!UICONTROL URL Webhook]** et copiez-la à partir de votre **[!UICONTROL Webhook WhatsApp]** précédemment envoyé.

Maintenant que votre Webhook est configuré, vous pouvez créer votre configuration WhatsApp.

## Créer une configuration WhatsApp {#whatsapp-configuration}

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Configurations de canal]**. Cliquez sur le bouton **[!UICONTROL Créer une configuration de canal]**.

   ![](assets/whatsapp-config-1.png)

1. Saisissez un nom et une description (facultatif) pour la configuration, puis sélectionnez le canal WhatsApp.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Sélectionnez **[!DNL WhatsApp]** en tant que canal.

   ![](assets/whatsapp-config-2.png)

1. Sélectionnez une ou plusieurs **[!UICONTROL actions marketing]** pour associer des politiques de consentement aux messages qui utilisent cette configuration. Toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. En savoir plus

1. Sélectionnez la **[!UICONTROL configuration de l’API WhatsApp]** créée précédemment.

   ![](assets/whatsapp-config-3.png)

1. Saisissez le **[!UICONTROL Numéro dʼexpéditeur]** à utiliser lors de vos communications.

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer la configuration de canal en tant que brouillon et reprendre son paramétrage ultérieurement.

1. Une fois la configuration de canal créée, elle s’affiche dans la liste avec le statut **[!UICONTROL En cours de traitement]**.

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](../configuration/channel-surfaces.md).

1. Une fois les contrôles réussis, la configuration de canal obtient le statut **[!UICONTROL Actif]**. Elle est prête à être utilisée pour diffuser des messages.

Une fois qu’il est configuré, vous pouvez tirer parti de toutes les fonctionnalités d’origine des canaux, telles que la création de messages, la personnalisation, le suivi des liens et la création de rapports.

Vous pouvez maintenant commencer à envoyer des messages WhatsApp avec Journey Optimizer.