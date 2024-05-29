---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Twilio
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer avec Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 98%

---

# Configurer le fournisseur Twilio {#sms-configuration-twilio}

Pour configurer Twilio avec Journey Optimizer, vous devez créer des informations d’identification de l’API utilisées pour Twilio :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL fournisseur de SMS]**: Twilio.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL SID du compte]** et **[!UICONTROL Jeton d’authentification]** : accédez au volet **Informations du compte** de la page Tableau de bord de la console Twilio pour trouver vos informations d’identification.

   * **[!UICONTROL SID du message]** : saisissez l’identifiant unique attribué à chaque message créé par l’API de Twilio. En savoir plus dans la [Documentation Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une surface de canal pour les messages SMS et MMS. [En savoir plus](sms-configuration-surface.md)
