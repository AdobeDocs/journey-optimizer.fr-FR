---
solution: Journey Optimizer
product: journey optimizer
title: Configurer votre fournisseur personnalisé
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer par le biais d’un fournisseur personnalisé
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 88%

---

# Configurer un fournisseur personnalisé {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL du fournisseur"
>abstract="Spécifiez l’URL de l’API externe à laquelle vous prévoyez de vous connecter. Cette URL sert de point d’entrée pour accéder aux fonctionnalités de l’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Paramètres d’en-tête"
>abstract="Spécifiez le libellé, le type et la valeur des en-têtes supplémentaires pour que l’authentification, la mise en forme du contenu et la communication avec l’API soient efficaces. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Payload du fournisseur"
>abstract="Fournissez le payload de la requête pour vous assurer que les bonnes données sont envoyées pour le traitement et la génération de la réponse."

Cette fonctionnalité vous permet d’intégrer et de configurer vos propres fournisseurs de messagerie, offrant ainsi une flexibilité au-delà des options par défaut (Sinch, Twilio et Infobip). Cela permet une création, une diffusion, un reporting et une gestion du consentement transparents pour les SMS et les messages RCS.

Grâce à la configuration personnalisée du fournisseur, vous pouvez connecter des services de messagerie tiers directement dans Journey Optimizer, personnaliser les payloads des messages pour le contenu dynamique et gérer les préférences de souscription/désinscription pour assurer la conformité sur les canaux SMS et RCS.

Pour configurer votre fournisseur personnalisé, procédez comme suit :

1. [Créer des informations d’identification d’API](#api-credential)
1. [Créer un webhook](#webhook)
1. [Créer une configuration des canaux](sms-configuration-surface.md)
1. [Créer un parcours ou une campagne avec une action de canal SMS](create-sms.md)

## Créer vos informations d’identification d’API {#api-credential}

Pour envoyer des SMS et des messages RCS dans Journey Optimizer à l’aide d’un fournisseur personnalisé qui n’est pas prêt à l’emploi par Adobe (par exemple Sinch, Infobip, Twilio), procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]**, sélectionnez le menu **[!UICONTROL Informations d’identification d’API]** sous **[!UICONTROL Paramètres SMS]**, puis cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification d’API]**.

   ![](assets/sms_byo_1.png)

1. Configurez les informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : personnalisé.

   * **[!UICONTROL Nom]** : saisissez un nom pour les informations d’identification d’API.

   * **[!UICONTROL AppId du fournisseur]** : saisissez l’ID de l’application fourni par votre fournisseur de SMS.

   * **[!UICONTROL Nom du fournisseur]** : saisissez le nom du fournisseur de SMS.

   * **[!UICONTROL URL du fournisseur]** : saisissez l’URL du fournisseur de SMS.

   * **[!UICONTROL Type d’authentification]** : sélectionnez le type d’autorisation et [renseignez les champs correspondants](#auth-options) en fonction de la méthode d’authentification choisie.

     ![](assets/sms-byop.png)

1. Dans la section **[!UICONTROL En-têtes]**, cliquez sur **[!UICONTROL Ajouter un nouveau paramètre]** pour définir les en-têtes HTTP du message de requête à envoyer au service externe.

   Les champs d’en-tête **Content-Type** et **Charset** sont définis par défaut et ne peuvent pas être supprimés.

   ![](assets/sms_byo_2.png)

1. Ajoutez la **[!UICONTROL payload du fournisseur]** pour valider et personnaliser les payloads de votre requête.

   Pour les messages RCS, cette payload est ensuite utilisée lors de la [conception de contenu](create-sms.md#sms-content).

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’![icône de corbeille](assets/do-not-localize/Smock_Delete_18_N.svg) pour supprimer vos informations d’identification d’API.

   ![](assets/sms_byo_3.png)

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

   ![](assets/sms_byo_4.png)

Une fois vos informations d’identification d’API créées et configurées, vous devez configurer [les paramètres entrants du webhook](#webhook) pour les SMS.

### Options d’authentification pour les fournisseurs de SMS personnalisés {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Type d’authentification"
>abstract="Indiquez la méthode d’authentification nécessaire pour accéder à l’API, afin de garantir une communication sécurisée et autorisée avec le service externe."

>[!BEGINTABS]

>[!TAB Clé d’API]

Une fois vos informations d’identification d’API créées, renseignez les champs obligatoires relatifs à l’authentification par clé API :

* **[!UICONTROL Nom]** : saisissez un nom pour votre configuration de clé d’API.
* **[!UICONTROL Jeton API]** : saisissez le jeton API fourni par votre fournisseur de SMS.

![](assets/sms-byop-api-key.png)

>[!TAB Authentification MAC]

Une fois vos informations d’identification d’API créées, renseignez les champs obligatoires relatifs à l’authentification MAC :

* **[!UICONTROL Nom]** : saisissez un nom pour votre configuration d’authentification MAC.
* **[!UICONTROL Jeton API]** : saisissez le jeton API fourni par votre fournisseur de SMS.
* **[!UICONTROL Clé secrète d’API]** : saisissez la clé secrète d’API fournie par votre fournisseur de SMS. Cette clé est utilisée pour générer la balise MAC (code d’authentification de message) pour une communication sécurisée.
* **[!UICONTROL Format de hachage d’autorisation Mac]** : sélectionnez le format de hachage pour l’authentification MAC.

![](assets/sms-byop-mac.png)

>[!TAB Authentification OAuth]

Une fois vos informations d’identification d’API créées, renseignez les champs obligatoires relatifs à l’authentification OAuth :

* **[!UICONTROL Nom]** : saisissez un nom pour votre configuration d’authentification OAuth.

* **[!UICONTROL Jeton API]** : saisissez le jeton API fourni par votre fournisseur de SMS.

* **[!UICONTROL URL OAuth]** : saisissez l’URL permettant d’obtenir le jeton OAuth.

* **[!UICONTROL Corps OAuth]** : indiquez le corps de la requête OAuth au format JSON, y compris les paramètres tels que `grant_type`, `client_id` et `client_secret`.

![](assets/sms-byop-oauth.png)

>[!TAB Authentification JWT]

Une fois vos informations d’identification d’API créées, renseignez les champs obligatoires relatifs à l’authentification JWT :

* **[!UICONTROL Nom]** : saisissez un nom pour votre configuration d’authentification JWT.

* **[!UICONTROL Jeton API]** : saisissez le jeton API fourni par votre fournisseur de SMS.

* **[!UICONTROL Payload JWT]** : saisissez la payload JSON contenant les revendications requises pour JWT, telles que l’émetteur, l’objet, l’audience et l’expiration.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## Créer un webhook {#webhook}

>[!BEGINSHADEBOX]

Si les mots-clés relatifs à l’opt-in ou à l’opt-out ne sont pas fournis, des messages de consentement standard sont utilisés pour respecter la confidentialité des personnes. L’ajout de mots-clés personnalisés remplace automatiquement les valeurs par défaut.

**Mots-clés par défaut :**

* **Opt-in** : SUBSCRIBE (s’abonner), YES (oui), UNSTOP (redémarrer), START (démarrer), CONTINUE (continuer), RESUME (reprendre), BEGIN (commencer).
* **Opt-out** : STOP (arrêter), QUIT (quitter), CANCEL (annuler), END (terminer), UNSUBSCRIBE (se désabonner), NO (non).
* **Aide** : HELP (aide).

>[!ENDSHADEBOX]

Une fois vos informations d’identification d’API créées, l’étape suivante consiste à créer un webhook et à configurer vos paramètres entrants. Cette configuration garantit que votre système peut recevoir et traiter correctement les données ou messages entrants.

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]**, sélectionnez le menu **[!UICONTROL Webhooks SMS]** sous **[!UICONTROL Paramètres SMS]**, puis cliquez sur le bouton **[!UICONTROL Créer un webhook]**.

   ![](assets/sms_byo_5.png)

1. Configurez vos paramètres de webhook comme indiqué ci-dessous :

   * **[!UICONTROL Nom]** : saisissez un nom pour votre webhook.

   * **[!UICONTROL Sélectionner le fournisseur de SMS]** : personnalisé.

   * **[!UICONTROL Sélectionner les informations d’identification d’API]** : choisissez dans la liste déroulante les [informations d’identification d’API configurées précédemment](#api-credential).

   * **[!UICONTROL Mots-clés d’opt-in]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre message d’opt-in. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’opt-in]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que message d’opt-in.

   * **[!UICONTROL Mots-clés d’opt-out]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre message d’opt-out. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’opt-out]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que message d’opt-out.

   ![](assets/sms_byo_6.png)

1. Cliquez sur **[!UICONTROL Afficher l’éditeur de payload]** pour valider et personnaliser les payloads de votre requête.

   Vous pouvez personnaliser votre payload de manière dynamique à l’aide d’attributs de profil, et veiller à ce que des données précises sont envoyées pour le traitement et la génération de réponse à l’aide de fonctions d’assistance intégrées.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de votre webhook.

1. Dans le menu **[!UICONTROL Webhooks]**, cliquez sur l’![icône de corbeille](assets/do-not-localize/Smock_Delete_18_N.svg) pour supprimer votre webhook.

1. Pour modifier la configuration existante, recherchez le webhook souhaité et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

1. Accédez à la nouvelle **[!UICONTROL URL du webhook]** et copiez-la à partir du **[!UICONTROL webhook]** précédemment envoyé.

   ![](assets/sms_byo_7.png)

Après avoir créé et configuré les paramètres entrants pour le webhook, vous devez créer une [configuration des canaux](sms-configuration-surface.md) pour les messages SMS.

Une fois qu’il est configuré, vous pouvez tirer parti de toutes les fonctionnalités d’origine des canaux, telles que la création de messages, la personnalisation, le suivi des liens et la création de rapports.

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

