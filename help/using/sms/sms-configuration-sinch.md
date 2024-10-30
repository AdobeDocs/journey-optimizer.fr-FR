---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Sinch
description: Découvrir comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer avec Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 81%

---

# Configurer le fournisseur Sinch {#sms-configuration-sinch}

Lorsque vous utilisez le fournisseur Sinch avec Journey Optimizer, vous pouvez trouver deux options distinctes :

* **Configuration des SMS** : configurez vos informations d’identification d’API Sinch pour envoyer des messages SMS de manière transparente.

* **Configuration des MMS** : pour la messagerie multimédia (MMS), configurez vos informations d’identification d’API MMS Sinch. Notez que le suivi et la réponse aux messages entrants sont gérés par la configuration des SMS. La configuration des MMS concerne uniquement la diffusion sortante des messages MMS.

## Informations d’identification de l’API Sinch{#create-api}

Pour configurer votre fournisseur Sinch pour envoyer des SMS et des MMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** `>` **[!UICONTROL Paramètres des SMS]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : Sinch.

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

   * **[!UICONTROL Numéro entrant]** : ajoutez votre numéro entrant unique ou votre code court. Cela permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun ayant son propre numéro entrant ou code court.

   * **[!UICONTROL Mots-clés entrants personnalisés]** : définissez des mots-clés uniques pour des actions spécifiques, par exemple DISCOUNT, OFFERS, ENROLL. Ces mots-clés sont capturés et stockés en tant qu’attributs dans le profil, ce qui vous permet de déclencher une qualification de segment en continu dans le parcours et de fournir une réponse ou une action personnalisée.

   * **[!UICONTROL Message de réponse entrante par défaut]** : saisissez la réponse par défaut envoyée lorsqu’un utilisateur final envoie un SMS entrant qui ne correspond à aucun des mots-clés définis.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

1. Dans le menu **[!UICONTROL Informations d’identification de l’API]**, cliquez sur l’icône de la corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification de l’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une configuration des canaux pour les messages SMS. [En savoir plus](sms-configuration-surface.md)

## Informations d’identification de l’API MMS Sinch {#sinch-mms}

>[!IMPORTANT]
>
> Avec la configuration des MMS, vous devez également créer des informations d’identification de l’API Sinch spécifiques pour le suivi des messages entrants et la gestion des demandes de consentement.

Pour configurer Sinch MMS avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** `>` **[!UICONTROL Paramètres des SMS]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification pour l’API MMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : Sinch MMS.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL Identifiant de projet]**, **[!UICONTROL Identifiant d’application]** et **[!UICONTROL Jeton API]** : suivez les étapes ci-dessous pour collecter vos informations d’identification d’API MMS.

      * Pour l’**[!UICONTROL Identifiant de projet]** et l’**[!UICONTROL Identifiant d’application]** : accédez à la page [Vue d’ensemble de l’API de conversation](https://dashboard.sinch.com/convapi/overview) de votre projet Sinch sur votre tableau de bord Sinch.
      * Pour le **[!UICONTROL Jeton API]** : obtenez les [Clés d’accès](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) pour votre projet Sinch et générez un **Jeton API Base64** à partir des **Clés d’accès** de votre projet Sinch.

   * **[!UICONTROL Identifiant de plan de service]** et **[!UICONTROL Jeton d’API SMS]** : votre **[!UICONTROL Identifiant de plan de service]** et votre **[!UICONTROL Jeton d’API SMS]** se trouvent dans l’onglet SMS de la page des API.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

1. Dans le menu **[!UICONTROL Informations d’identification de l’API]**, cliquez sur l’icône de la corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification de l’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une configuration des canaux pour les messages MMS. [En savoir plus](sms-configuration-surface.md)
