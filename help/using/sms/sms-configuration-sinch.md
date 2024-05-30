---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Sinch
description: Découvrir comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer avec Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 81%

---

# Configurer le fournisseur Sinch {#sms-configuration-sinch}

Lorsque vous utilisez le fournisseur Sinch avec Journey Optimizer, vous pouvez trouver deux options distinctes :

* **Configuration des SMS** : configurez vos informations d’identification d’API Sinch pour envoyer des messages SMS de manière transparente.

* **Configuration des MMS** : pour la messagerie multimédia (MMS), configurez vos informations d’identification d’API MMS Sinch. Notez que le suivi et la réponse aux messages entrants sont gérés par la configuration des SMS. La configuration des MMS concerne uniquement la diffusion sortante des messages MMS.

## Informations d’identification de l’API Sinch{#create-api}

Pour configurer votre fournisseur Sinch pour envoyer des SMS et des MMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL fournisseur de SMS]**: Sinch.

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

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

## Informations d’identification de l’API MMS Sinch {#sinch-mms}

>[!IMPORTANT]
>
> Avec la configuration des MMS, vous devez également créer des informations d’identification de l’API Sinch spécifiques pour le suivi des messages entrants et la gestion des demandes de consentement.

Pour configurer Sinch MMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification d’API MMS, comme indiqué ci-dessous :

   * **[!UICONTROL fournisseur de SMS]**: Sinch MMS.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL Identifiant de projet]**, **[!UICONTROL ID de l’application]** et **[!UICONTROL Jeton API]**: suivez les étapes ci-dessous pour rassembler vos informations d’identification d’API MMS.

      * Pour **[!UICONTROL Identifiant de projet]** et **[!UICONTROL ID de l’application]**: accédez au [Présentation de l’API de conversation](https://dashboard.sinch.com/convapi/overview) page de votre projet Sinch sur votre tableau de bord Sinch.
      * Pour **[!UICONTROL Jeton API]**: obtenez la variable [Clés d’accès](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) pour votre projet Sinch et générez une **Jeton API Base64** de votre projet Sinch **Clés d’accès**.

   * **[!UICONTROL Identifiant du plan de service]** et **[!UICONTROL Jeton d’API SMS]**: votre **[!UICONTROL Identifiant du plan de service]** et **[!UICONTROL Jeton d’API SMS]** se trouvent dans l’onglet SMS de la page API.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une surface de canal pour les messages MMS. [En savoir plus](sms-configuration-surface.md)
