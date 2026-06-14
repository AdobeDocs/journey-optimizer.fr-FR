---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Twilio
description: Découvrez comment configurer votre environnement pour envoyer des messages mobiles avec Journey Optimizer avec Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
TQID: https://experienceleague.adobe.com/EbPWXkbbXG4zazPUQsqaEeXx5wUi6VzFGrEeYmlAASY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 640
ht-degree: 74%

---

# Configurer le fournisseur Twilio {#sms-configuration-twilio}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment intégrer Twilio à Adobe Journey Optimizer en créant des informations d’identification d’API pour les SMS, les MMS et les messages RCS afin de diffuser des messages mobiles dans vos parcours et campagnes.

>[!ENDSHADEBOX]

En intégrant Twilio à Adobe Journey Optimizer, vous pouvez diffuser des messages mobiles à vos profils dans le cadre de vos parcours et campagnes.

Pour configurer Twilio en tant que fournisseur de SMS, procédez comme suit :

1. [Créer des informations d’identification d’API](#api-credential)
1. [Créer un webhook](mobile-webhook.md)
1. [Créer une configuration des canaux](mobile-configuration-surface.md)
1. [Créer un parcours ou une campagne avec une action de canal SMS](create-mobile-message.md)

## Configurer les informations d’identification d’API pour SMS/RCS/MMS {#api-credential}

Pour configurer Twilio avec Journey Optimizer, vous devez créer des informations d’identification d’API pour Twilio :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** `>` **[!UICONTROL Paramètres des SMS]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez les informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   * **[!UICONTROL Fournisseur de SMS]** : Twilio.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL SID du compte]** et **[!UICONTROL Jeton d’authentification]** : accédez au volet **Informations du compte** de la page Tableau de bord de la console Twilio pour trouver vos informations d’identification.

   * **[!UICONTROL SID du message]** : saisissez l’identifiant unique attribué à chaque message créé par l’API de Twilio. En savoir plus dans la [Documentation de Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Numéro entrant]** : ajoutez votre numéro entrant unique. Cela permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun possédant son propre numéro entrant.

1. Sélectionnez **[!UICONTROL Utiliser un jeu de données personnalisé pour le trafic entrant]** pour acheminer le SMS entrant de ces informations d’identification vers un jeu de données précréé que vous sélectionnez dans la liste déroulante. [En savoir plus sur l’utilisation d’un jeu de données personnalisé pour les mots-clés entrants](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >Le schéma du jeu de données doit être **[!UICONTROL XDM ExperienceEvent]** et inclure au moins les groupes de champs suivants :
   >* Adobe CJM ExperienceEvent - Informations sur l’interaction du message
   >* ExperienceEvent Adobe CJM - Détails d’exécution du message
   >* ExperienceEvent Adobe CJM - Détails du profil de message
   >
   >Le schéma et le jeu de données doivent être activés pour Profil.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

1. Cliquez sur **[!UICONTROL Vérifier la connexion SMS]**, à partir de vos informations d’identification d’API existantes, pour tester et vérifier vos informations d’identification d’API SMS en envoyant un exemple de message à un appareil désigné.

1. Renseignez les champs **Numéro** et **Message**, puis cliquez sur **[!UICONTROL Vérifier la connexion]**.

   >[!IMPORTANT]
   >
   >Le message doit être structuré de manière à s’aligner sur le format de payload du fournisseur.

   ![](assets/verify-connection.png)

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une configuration de canal pour les messages SMS et MMS. [En savoir plus](mobile-configuration-surface.md)

## Configurer des informations d’identification d’API pour RCS

Les messages RCS sont pris en charge dans Adobe Journey Optimizer via Twilio à l’aide de la fonctionnalité [Fournisseur de SMS personnalisé](mobile-configuration-custom.md). Cela permet de diffuser des messages riches et interactifs par le biais de profils professionnels vérifiés, en incorporant des éléments tels que des carrousels, des boutons et du contenu multimédia.

➡️ [Découvrez dans la documentation Twilio comment Twilio prend en charge RCS](https://www.twilio.com/docs/rcs)

Pour activer la messagerie RCS avec Twilio, les nouvelles informations d’identification d’API doivent être configurées via un fournisseur de SMS personnalisé. Les informations d’identification SMS Twilio existantes ne sont pas compatibles, car RCS nécessite un format de payload distinct.

Pour configurer RCS avec Twilio :

1. **S’inscrire à la messagerie RCS dans Twilio**

   Commencez par terminer le processus d’enregistrement RCS sur la plateforme Twilio. Cela comprend la configuration de votre profil d’entreprise et l’activation des fonctionnalités RCS pour votre compte.

1. **Créer un webhook SMS**

   [Configurez un webhook SMS](mobile-configuration-custom.md#webhook) qui peut recevoir les réponses aux messages RCS entrants ou les mises à jour des diffusions. Ce webhook doit être correctement lié à votre configuration Twilio pour disposer d’une communication bidirectionnelle.

1. **Créer des informations d’identification d’API en définissant le fournisseur de SMS sur Personnalisé**

   Dans Journey Optimizer, [définissez de nouvelles informations d’identification d’API](mobile-configuration-custom.md#api-credential) spécifiquement pour RCS en utilisant « Personnalisé » comme fournisseur de SMS. Utilisez la méthode d’authentification de point d’entrée RCS, l’URL de base et les en-têtes appropriés.

Après avoir créé et configuré vos informations d’identification d’API, vous devez maintenant créer une configuration de canal pour les messages RCS. [En savoir plus](mobile-configuration-surface.md)







