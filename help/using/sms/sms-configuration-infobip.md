---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Infobip
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS et MMS avec Journey Optimizer avec Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: ea2753bd9ce7372e53fefc7816d19a7a3c73b87d
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 83%

---

# Configurer le fournisseur Infobip {#sms-configuration-infobip}

En intégrant Infobip à Adobe Journey Optimizer, vous pouvez diffuser des SMS à vos profils dans le cadre de vos parcours et campagnes.

Pour configurer Infobip en tant que fournisseur SMS, procédez comme suit :

1. [Créer des informations d’identification d’API](#api-credential)
1. [Créer un webhook](sms-webhook.md)
1. [Créer une configuration des canaux](sms-configuration-surface.md)
1. [Créer un parcours ou une campagne avec une action de canal SMS](create-sms.md)

## Configurer les informations d’identification d’API pour les SMS {#api-credential}

Pour configurer Infobip avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez les informations d’identification pour l’API SMS, comme indiqué ci-dessous :

   +++ Liste des informations d’identification SMS pour la configuration

   | Champs de configuration | Description |
   |---|---|
   | Fournisseur SMS | Infobip |
   | Nom | Saisissez un nom pour vos informations d’identification API. |
   | URL de base et clé API | Accédez à la page d’accueil de votre interface web ou à la page de gestion des clés API pour trouver vos informations d’identification. Pour les points d’entrée de domaine régionaux ou alternatifs, par exemple `api-ny2.infobip.com`, spécifiez l’URL de base complète et vérifiez votre jeton d’autorisation auprès de l’assistance d’Infobip. </br>En savoir plus dans la [documentation Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | Identifiant d’entité principale | Saisissez l’identifiant d’entité principale DLT qui vous a été attribué. |
   | Identifiant du modèle de contenu | Saisissez votre identifiant de modèle de contenu DLT enregistré. |
   | Période de validité | Saisissez la période de validité du message en heures. Si les messages ne peuvent pas être livrés dans ce délai, le système effectue d’autres tentatives pour les renvoyer. La période de validité par défaut est définie sur 48 heures. |
   | Données de rappel | Saisissez les données clients supplémentaires qui seront envoyées à l’URL de notification. |
   | Numéro entrant | Ajoutez votre numéro entrant unique. Cela permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun possédant son propre numéro entrant. |

   +++

1. Activez l’option **[!UICONTROL Opt-out en logique floue]** pour détecter les messages ressemblant à des mots-clés d’opt-out (par exemple, « CANCIL ») et personnalisez la réponse de confirmation dans le champ **[!UICONTROL Réponse automatique en logique floue]**.

   L’option **[!UICONTROL Opt-out en logique floue]** identifie les SMS indiquant qu’une personne souhaite se désabonner, même si le message ne correspond pas exactement à un mot-clé d’opt-out défini. Les expressions de désabonnement courantes et certains termes offensants peuvent être détectés, ce qui permet de s’assurer que vos campagnes respectent les préférences des utilisateurs et utilisatrices et qu’elles restent conformes.

1. Sélectionnez **[!UICONTROL Utiliser un jeu de données personnalisé pour le trafic entrant]** pour acheminer le SMS entrant de ces informations d’identification vers un jeu de données précréé que vous sélectionnez dans la liste déroulante. [En savoir plus sur la création de jeux de données](../experience-decisioning/data-collection/create-dataset.md)

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

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une configuration de canal pour les messages SMS et MMS. [En savoir plus](sms-configuration-surface.md)

## Configurer des informations d’identification d’API pour RCS

Les messages RCS sont pris en charge dans Adobe Journey Optimizer via Infobip à l’aide de la fonctionnalité [Fournisseur de SMS personnalisé](sms-configuration-custom.md). Cela permet de diffuser des messages riches et interactifs par le biais de profils professionnels vérifiés, en incorporant des éléments tels que des carrousels, des boutons et du contenu multimédia.

➡️ [Découvrez dans la documentation Infobip comment Infobip prend en charge RCS](https://www.infobip.com/docs/api/channels/rcs).

Pour activer la messagerie RCS avec Infobip, les nouvelles informations d’identification d’API doivent être configurées via un fournisseur de SMS personnalisé. Les informations d’identification SMS Infobip existantes ne sont pas compatibles, car RCS nécessite un format de payload distinct.

Pour configurer RCS avec Infobip :

1. **Inscrire votre entreprise à RCS via Infobip**

   Commencez par terminer le processus d’intégration et d’enregistrement RCS sur la plateforme Infobip. Cela implique de configurer votre profil d’expédition RCS et de vous assurer que votre compte est compatible avec RCS. Pour plus d’informations, consultez la [documentation d’Infobip](https://www.infobip.com/docs/rcs/get-started).

1. **Créer un webhook SMS**

   [Configurez un webhook SMS personnalisé](sms-configuration-custom.md#webhook) dans Journey Optimizer. Ce webhook sera chargé de gérer les accusés de réception de diffusion, les messages RCS entrants et les mises à jour de statut provenant de la plateforme d’Infobip.

1. **Créer des informations d’identification d’API en définissant le fournisseur de SMS sur Personnalisé**

   [Créez des informations d’identification d’API](sms-configuration-custom.md#api-credential) dans Journey Optimizer, en sélectionnant « Personnalisé » comme fournisseur SMS. Utilisez la méthode d’authentification de point d’entrée RCS, l’URL de base et les en-têtes appropriés.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer [votre Webhook](sms-webhook.md) et une configuration de canal pour vos messages RCS. [En savoir plus](sms-configuration-surface.md)
