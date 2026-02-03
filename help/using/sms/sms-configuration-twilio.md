---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Twilio
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer avec Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 93%

---

# Configurer le fournisseur Twilio {#sms-configuration-twilio}

En intégrant Twilio à Adobe Journey Optimizer, vous pouvez diffuser des SMS à vos profils dans le cadre de vos parcours et campagnes.

Pour configurer Twilio en tant que fournisseur de SMS, procédez comme suit :

1. [Créer des informations d’identification d’API](#api-credential)
1. [Créer un webhook](sms-webhook.md)
1. [Créer une configuration des canaux](sms-configuration-surface.md)
1. [Créer un parcours ou une campagne avec une action de canal SMS](create-sms.md)

## Configurer les informations d’identification d’API pour les SMS/MMS {#api-credential}

Pour configurer Twilio avec Journey Optimizer, vous devez créer des informations d’identification d’API pour Twilio :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** `>`**[!UICONTROL Paramètres des SMS]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez les informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : Twilio.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL SID du compte]** et **[!UICONTROL Jeton d’authentification]** : accédez au volet **Informations du compte** de la page Tableau de bord de la console Twilio pour trouver vos informations d’identification.

   * **[!UICONTROL SID du message]** : saisissez l’identifiant unique attribué à chaque message créé par l’API de Twilio. En savoir plus dans la [Documentation de Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Numéro entrant]** : ajoutez votre numéro entrant unique. Cela permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun possédant son propre numéro entrant.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

1. Cliquez sur **[!UICONTROL Vérifier la connexion SMS]**, à partir de vos informations d’identification d’API existantes, pour tester et vérifier vos informations d’identification d’API SMS en envoyant un exemple de message à un appareil désigné.

1. Renseignez les champs **Numéro** et **Message**, puis cliquez sur **[!UICONTROL Vérifier la connexion]**.

   >[!IMPORTANT]
   >
   >Le message doit être structuré de manière à s’aligner sur le format de payload du fournisseur.

   ![](assets/verify-connection.png)

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une configuration de canal pour les messages SMS et MMS. [En savoir plus](sms-configuration-surface.md)

## Configurer des informations d’identification d’API pour RCS

Les messages RCS sont pris en charge dans Adobe Journey Optimizer via Twilio à l’aide de la fonctionnalité [Fournisseur de SMS personnalisé](sms-configuration-custom.md). Cela permet de diffuser des messages riches et interactifs par le biais de profils professionnels vérifiés, en incorporant des éléments tels que des carrousels, des boutons et du contenu multimédia.

➡️ [Découvrez dans la documentation Twilio comment Twilio prend en charge RCS](https://www.twilio.com/docs/rcs)

Pour activer la messagerie RCS avec Twilio, les nouvelles informations d’identification d’API doivent être configurées via un fournisseur de SMS personnalisé. Les informations d’identification SMS Twilio existantes ne sont pas compatibles, car RCS nécessite un format de payload distinct.

Pour configurer RCS avec Twilio :

1. **S’inscrire à la messagerie RCS dans Twilio**

   Commencez par terminer le processus d’enregistrement RCS sur la plateforme Twilio. Cela comprend la configuration de votre profil d’entreprise et l’activation des fonctionnalités RCS pour votre compte.

1. **Créer un webhook SMS**

   [Configurez un webhook SMS](sms-configuration-custom.md#webhook) qui peut recevoir les réponses aux messages RCS entrants ou les mises à jour des diffusions. Ce webhook doit être correctement lié à votre configuration Twilio pour disposer d’une communication bidirectionnelle.

1. **Créer des informations d’identification d’API en définissant le fournisseur de SMS sur Personnalisé**

   Dans Journey Optimizer, [définissez de nouvelles informations d’identification d’API](sms-configuration-custom.md#api-credential) spécifiquement pour RCS en utilisant « Personnalisé » comme fournisseur de SMS. Utilisez la méthode d’authentification de point d’entrée RCS, l’URL de base et les en-têtes appropriés.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une configuration de canal pour les messages RCS. [En savoir plus](sms-configuration-surface.md)







