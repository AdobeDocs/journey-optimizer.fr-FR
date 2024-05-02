---
solution: Journey Optimizer
product: journey optimizer
title: Configuration du fournisseur Sinch
description: Découvrez comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer avec Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 65%

---

# Configuration du fournisseur Sinch {#sms-configuration-sinch}

Lorsque vous utilisez le fournisseur Sinch avec Journey Optimizer, vous pouvez trouver deux options distinctes :

* **Configuration des SMS**: configurez vos informations d’identification d’API Sinch pour envoyer des messages SMS de manière transparente.

* **Configuration MMS**: pour la messagerie multimédia (MMS), configurez vos informations d’identification d’API MMS Sinch. Notez que le tracking et la réponse aux messages entrants sont gérés par la configuration SMS. La configuration MMS est uniquement destinée à la diffusion sortante du message MMS.

## Informations d’identification de l’API Sinch{#create-api}

Pour configurer votre fournisseur Sinch pour envoyer des SMS et des MMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

   ![](assets/sms_6.png)

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]** : accédez à la page des API, puis à vos informations d’identification sous l’onglet SMS. En savoir plus dans la [Documentation Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Mots-clés d’opt-in]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **[!UICONTROL message d’opt-in]**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’opt-in]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **[!UICONTROL message d’opt-in]**.

   * **[!UICONTROL Mots-clés d’opt-out]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **[!UICONTROL message d’opt-out]**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’opt-out]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **[!UICONTROL message d’opt-out]**.

   * **[!UICONTROL Mots-clés d’aide]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **message d’aide**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’aide]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **message d’aide**.

   * **[!UICONTROL Mots-clés de double opt-in]** : saisissez les mots-clés qui déclenchent le processus de double opt-in. Si un profil de personne n’existe pas, il est créé lors de la confirmation. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. [En savoir plus sur le double opt-in SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Message de double opt-in]** : saisissez la réponse personnalisée qui est automatiquement envoyée en réponse à la confirmation de double opt-in.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une surface de canal pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

## Informations d’identification de l’API MMS Sinch {#sinch-mms}

>[!IMPORTANT]
>
> Avec la configuration MMS, vous devez également créer des informations d’identification d’API Sinch spécifiques pour le suivi des messages entrants et la gestion des demandes de consentement.

Pour configurer Sinch MMS pour envoyer MMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

   ![](assets/sms_6.png)

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL ID de projet]**, **[!UICONTROL ID de l’application]** et **[!UICONTROL Jeton API]** : à partir du menu API de conversation, vous trouverez vos informations d’identification dans le menu Application. En savoir plus dans la [Documentation Sinch](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * **[!UICONTROL ID de plan de service]** et **[!UICONTROL Jeton d’API SMS]** : votre **[!UICONTROL ID de plan de service]** et votre **[!UICONTROL Jeton d’API SMS]** se trouvent dans l’onglet SMS de la page API.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une surface de canal pour les messages MMS. [En savoir plus](sms-configuration-surface.md)
