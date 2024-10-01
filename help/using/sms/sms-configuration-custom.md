---
solution: Journey Optimizer
product: journey optimizer
title: Configurer votre fournisseur personnalisé
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer par le biais d’un fournisseur personnalisé
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 100%

---

# Configurer un fournisseur personnalisé (version bêta) {#sms-configuration-custom}

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

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

Une fois qu’il est configuré, vous pouvez tirer parti de toutes les fonctionnalités d’origine des canaux, telles que la création de messages, la personnalisation, le suivi des liens et la création de rapports.

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
