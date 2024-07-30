---
solution: Journey Optimizer
product: journey optimizer
title: Configuration de votre fournisseur personnalisé
description: Découvrez comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer avec un fournisseur personnalisé
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 24%

---

# Configurer un fournisseur personnalisé (Beta) {#sms-configuration-custom}

>[!AVAILABILITY]
>
>Les fournisseurs personnalisés sont actuellement disponibles en version bêta uniquement pour les utilisateurs sélectionnés. Contactez votre représentant ou représentante Adobe pour accéder à la version bêta.
>
>Notez que ce Beta ne prend pas en charge les messages entrants pour la gestion du consentement d’opt-in/opt-out et la création de rapports de diffusion.

Pour envoyer des messages dans Journey Optimizer à l’aide d’un fournisseur personnalisé non disponible par Adobe (par exemple, Sinch, Infobip, Twilio), procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]** .

1. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

   ![](assets/sms_byo_1.png)

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : personnalisé.

   * **[!UICONTROL Nom]** : saisissez un nom pour vos informations d’identification API.

   * **[!UICONTROL Provider AppId]** : saisissez l&#39;ID d&#39;application fourni par votre fournisseur SMS.

   * **[!UICONTROL Nom du fournisseur]** : saisissez le nom de votre fournisseur SMS.

   * **[!UICONTROL URL du fournisseur]** : saisissez l&#39;URL de votre fournisseur SMS.

   * **[!UICONTROL Type d’authentification &#x200B;]** : sélectionnez votre type d’autorisation. Les types d’autorisation pris en charge sont **Bearer App** ou **Basic**.

   * **[!UICONTROL Jeton API]** : saisissez le jeton API fourni par votre fournisseur SMS.

   * **[!UICONTROL Charge utile du fournisseur]** : ajoutez la charge utile de votre fournisseur, par exemple `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Assurez-vous que la charge utile inclut `{{toNumber}}`, `{{fromNumber}}`, `{{message}}`.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

Une fois configurée, vous pouvez tirer parti de toutes les fonctionnalités de canal d’usine, telles que la création de messages, la personnalisation, le suivi des liens et la création de rapports.

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
