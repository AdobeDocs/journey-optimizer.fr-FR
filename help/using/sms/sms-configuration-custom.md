---
solution: Journey Optimizer
product: journey optimizer
title: Configurer votre fournisseur personnalisé
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer par le biais d’un fournisseur personnalisé
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: fc78fcfb0f2ce3616cb8b1df44dda2cfd66262fe
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 38%

---

# Configurer un fournisseur de SMS personnalisé {#sms-configuration-custom}

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

>[!AVAILABILITY]
>
>Les fournisseurs personnalisés sont actuellement disponibles en version bêta pour certains utilisateurs et utilisatrices uniquement. Contactez votre représentant ou représentante Adobe pour accéder à la version bêta.
>Notez que cette version bêta ne prend pas en charge les messages entrants pour la gestion du consentement opt-in/opt-out et la création de rapports de diffusion.


Cette fonctionnalité vous permet d’intégrer et de configurer vos propres fournisseurs SMS, offrant ainsi une flexibilité au-delà des fournisseurs par défaut (Sinch, Twilio et Infobip). Cela permet la création, la diffusion, le reporting et la gestion du consentement des SMS en toute transparence.

Avec la configuration de fournisseur personnalisée pour les SMS, vous pouvez :

* Configurez les fournisseurs SMS personnalisés directement dans Journey Optimizer.
* Utilisez la personnalisation avancée de la payload pour la messagerie dynamique.
* Gérer les préférences de consentement (opt-in/opt-out) pour garantir la conformité.

## Création de vos informations d’identification API {#api-credential}

Pour envoyer des messages dans Journey Optimizer à l’aide d’un fournisseur personnalisé non disponible chez Adobe (par exemple, Sinch, Infobip, Twilio), procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]**, sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**, puis cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification de l’API]**.

   ![](assets/sms_byo_1.png)

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : personnalisé.

   * **[!UICONTROL Nom]** : saisissez un nom pour vos informations d’identification API.

   * **[!UICONTROL AppId du fournisseur]** : saisissez l’ID d’application fourni par votre fournisseur SMS.

   * **[!UICONTROL Nom du fournisseur]** : saisissez le nom de votre fournisseur SMS.

   * **[!UICONTROL URL du fournisseur]** : saisissez l’URL de votre fournisseur SMS.

   * **[!UICONTROL Type d’authentification&#x200B;]** : sélectionnez votre type d’autorisation et [renseignez les champs correspondants](#auth-options) en fonction de la méthode d’authentification choisie.

     ![](assets/sms-byop.png)

1. Dans la section **[!UICONTROL En-têtes]**, cliquez sur **[!UICONTROL Ajouter un nouveau paramètre]** pour spécifier les en-têtes HTTP du message de requête qui sera envoyé au service externe.

   Les champs d’en-tête **Content-Type** et **Charset** sont définis par défaut et ne peuvent pas être supprimés.

   ![](assets/sms_byo_2.png)

1. Ajoutez votre **[!UICONTROL payload de fournisseur]** pour valider et personnaliser les payloads de votre requête.

   Vous pouvez personnaliser votre payload de manière dynamique à l’aide d’attributs de profil, et vous assurer que des données précises sont envoyées pour le traitement et la génération de réponse à l’aide de fonctions d’assistance intégrées.
<!--
1. Add your **Inbound settings** to determine how your system handles incoming messages and subscriber preferences: 

    * **[!UICONTROL Inbound Webhook URL]**: Specify the endpoint URL where inbound messages (e.g. replies or new messages from users) are sent.
    * **[!UICONTROL Opt-in Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-In Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-in Message]**: Enter the custom response that is automatically sent as your Opt-In Message.
    * **[!UICONTROL Opt-out Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-Out Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-out Message]**: Enter the custom response that is automatically sent as your Opt-Out Message.
-->

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

   ![](assets/sms_byo_3.png)

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

   ![](assets/sms_byo_4.png)

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

Une fois qu’il est configuré, vous pouvez tirer parti de toutes les fonctionnalités d’origine des canaux, telles que la création de messages, la personnalisation, le suivi des liens et la création de rapports.

### Options d’authentification pour les fournisseurs de SMS personnalisés {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Type d’authentification"
>abstract="Indiquez la méthode d’authentification nécessaire pour accéder à l’API, afin de garantir une communication sécurisée et autorisée avec le service externe."

>[!BEGINTABS]

>[!TAB Clé API]

Une fois vos informations d’identification API créées, renseignez les champs requis pour l’authentification par clé API :

* **[!UICONTROL Nom]**&#x200B; : saisissez un nom pour la configuration de votre clé API.
* **[!UICONTROL Jeton API]**&#x200B; : saisissez le jeton API fourni par votre fournisseur SMS.

![](assets/sms-byop-api-key.png)

>[!TAB Authentification MAC]

Une fois vos informations d’identification d’API créées, renseignez les champs requis pour l’authentification MAC :

* **[!UICONTROL Nom]**&#x200B; : saisissez un nom pour votre configuration d’authentification MAC.
* **[!UICONTROL Jeton API]**&#x200B; : saisissez le jeton API fourni par votre fournisseur SMS.
* **[!UICONTROL Clé secrète API]** : saisissez la clé secrète API fournie par votre fournisseur SMS. Cette clé est utilisée pour générer le code d’authentification du message (MAC, Message Authentication Code) pour une communication sécurisée.
* **[!UICONTROL Format de hachage d’autorisation Mac]** : sélectionnez le format de hachage pour l’authentification MAC.

![](assets/sms-byop-mac.png)

>[!TAB  Authentification OAuth ]

Une fois vos informations d’identification d’API créées, renseignez les champs requis pour l’authentification OAuth :

* **[!UICONTROL Nom]**&#x200B; : saisissez un nom pour votre configuration d’authentification OAuth.

* **[!UICONTROL Jeton API]**&#x200B; : saisissez le jeton API fourni par votre fournisseur SMS.

* **[!UICONTROL URL OAuth]**&#x200B; : saisissez l’URL pour obtenir le jeton OAuth.

* **[!UICONTROL Corps OAuth]**&#x200B; : indiquez le corps de la requête OAuth au format JSON, y compris les paramètres tels que `grant_type`, `client_id` et `client_secret`.

![](assets/sms-byop-oauth.png)

>[!TAB  Authentification JWT ]

Une fois vos informations d’identification d’API créées, renseignez les champs requis pour l’authentification JWT :

* **[!UICONTROL Nom]**&#x200B; : saisissez un nom pour votre configuration d’authentification JWT.

* **[!UICONTROL Jeton API]**&#x200B; : saisissez le jeton API fourni par votre fournisseur SMS.

* **[!UICONTROL Payload JWT]**&#x200B; : saisissez la payload JSON contenant les revendications requises pour JWT, telles que l’émetteur, l’objet, l’audience et l’expiration.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
