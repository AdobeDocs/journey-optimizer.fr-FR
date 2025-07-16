---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Twilio
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer avec Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 604af3a0ac9febb62f2e2b1705e2751b2c476e04
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 49%

---

# Configurer le fournisseur Twilio {#sms-configuration-twilio}

## Configurer les informations d’identification d’API pour SMS/MMS

Pour configurer Twilio avec Journey Optimizer, vous devez créer des informations d’identification de l’API utilisées pour Twilio :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** `>`**[!UICONTROL Paramètres des SMS]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez les informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : Twilio.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL SID du compte]** et **[!UICONTROL Jeton d’authentification]** : accédez au volet **Informations du compte** de la page Tableau de bord de la console Twilio pour trouver vos informations d’identification.

   * **[!UICONTROL SID du message]** : saisissez l’identifiant unique attribué à chaque message créé par l’API de Twilio. En savoir plus dans la [Documentation Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Numéro entrant]** : ajoutez votre numéro entrant unique. Cela vous permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun ayant son propre numéro entrant.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une configuration de canal pour les messages SMS et MMS. [En savoir plus](sms-configuration-surface.md)

## Configuration des informations d’identification d’API pour RCS

La messagerie RCS est prise en charge dans Adobe Journey Optimizer via Twilio à l’aide de la fonctionnalité [Fournisseur de SMS personnalisé](sms-configuration-custom.md). Cela permet de diffuser des messages riches et interactifs par le biais de profils professionnels vérifiés, en incorporant des éléments tels que des carrousels, des boutons et du contenu multimédia.

➡️ [Découvrez comment Twilio prend en charge RCS dans la documentation Twilio](https://www.twilio.com/docs/rcs)

Pour activer la messagerie RCS avec Twilio, les nouvelles informations d’identification d’API doivent être configurées via un fournisseur de SMS personnalisé. Les informations d’identification SMS Twilio existantes ne sont pas compatibles, car RCS nécessite un format de payload distinct.

Pour configurer RCS avec Twilio :

1. **S&#39;inscrire aux messages RCS dans Twilio**

   Commencez par terminer le processus d’enregistrement RCS sur la plateforme Twilio. Cela inclut la configuration de votre profil d’entreprise et l’activation des fonctionnalités RCS pour votre compte.

1. **Créer un Webhook SMS**

   [Configurez un Webhook SMS](sms-configuration-custom.md#webhook) qui peut recevoir les réponses aux messages RCS entrants ou les mises à jour de diffusion. Ce webhook doit être correctement lié à votre configuration Twilio pour une communication bidirectionnelle.

1. **Créer des informations d’identification d’API à l’aide de Personnalisé en tant que fournisseur SMS**

   Dans Journey Optimizer, [définissez de nouvelles informations d’identification d’API](sms-configuration-custom.md#api-credential) spécifiquement pour RCS en utilisant « Personnalisé » comme fournisseur de SMS. Utilisez la méthode d’authentification de point d’entrée RCS appropriée, l’URL de base et les en-têtes.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une configuration de canal pour vos messages RCS. [En savoir plus](sms-configuration-surface.md)







