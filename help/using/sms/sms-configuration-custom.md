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
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: ht
source-wordcount: '376'
ht-degree: 100%

---

# Configurer un fournisseur personnalisé {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL du fournisseur"
>abstract="Spécifiez l’URL de l’API externe à laquelle vous prévoyez de vous connecter. Cette URL sert de point d’entrée pour accéder aux fonctionnalités de l’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Type d’authentification"
>abstract="Spécifiez la méthode d’authentification nécessaire pour accéder à l’API, telle que les jetons OAuth ou porteurs. Cela garantit une communication sécurisée et autorisée avec le service externe."

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
>
>Notez que cette version bêta ne prend pas en charge les messages entrants pour la gestion du consentement opt-in/opt-out et la création de rapports de diffusion.

Pour envoyer des messages dans Journey Optimizer à l’aide d’un fournisseur personnalisé non disponible chez Adobe (par exemple, Sinch, Infobip, Twilio), procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**.

1. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

   ![](assets/sms_byo_1.png)

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : personnalisé.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL AppId du fournisseur]** : saisissez l’ID de l’application fourni par votre fournisseur de SMS.

   * **[!UICONTROL Nom du fournisseur]** : saisissez le nom de votre fournisseur de SMS.

   * **[!UICONTROL URL du fournisseur]** : saisissez l’URL de votre fournisseur de SMS.

   * **[!UICONTROL Type d’authentification]** : sélectionnez votre type d’autorisation. Les types d’autorisation pris en charge sont **Bearer App** ou **Basic**.

   * **[!UICONTROL Jeton API]** : saisissez le jeton API fourni par votre fournisseur de SMS.

   * **[!UICONTROL Payload du fournisseur]** : ajoutez le payload de votre fournisseur, par exemple `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Assurez-vous que le payload inclut `{{toNumber}}`, `{{fromNumber}}`, `{{message}}`.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

Une fois qu’il est configuré, vous pouvez tirer parti de toutes les fonctionnalités d’origine des canaux, telles que la création de messages, la personnalisation, le suivi des liens et la création de rapports.

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3443608?captions=fre_fr)
