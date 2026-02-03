---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Infobip
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS et MMS avec Journey Optimizer avec Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 70%

---

# Configurer le fournisseur Infobip {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Si les mots-clés relatifs à l’opt-in ou à l’opt-out ne sont pas fournis, des messages de consentement standard sont utilisés pour respecter la confidentialité des personnes. L’ajout de mots-clés personnalisés remplace automatiquement les valeurs par défaut.

**Mots-clés par défaut :**

* **Opt-in** : SUBSCRIBE (s’abonner), YES (oui), UNSTOP (redémarrer), START (démarrer), CONTINUE (continuer), RESUME (reprendre), BEGIN (commencer).
* **Opt-out** : STOP (arrêter), QUIT (quitter), CANCEL (annuler), END (terminer), UNSUBSCRIBE (se désabonner), NO (non).
* **Aide** : HELP (aide).

>[!ENDSHADEBOX]

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
   | Mots-clés d’opt-in | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br>Saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre message d’accord préalable. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. |
   | Message d’opt-in | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br> Saisissez la réponse personnalisée qui est automatiquement envoyée en tant que message d’accord préalable. |
   | Mots-clés d’opt-out | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br> Entrez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre message d&#39;opt-out. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. |
   | Message d’opt-out | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br>Saisissez la réponse personnalisée qui est automatiquement envoyée en tant que message d’opt-out. |
   | Mots-clés d’aide | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br>Saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **message d’aide**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. |
   | Message d’aide | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br>Saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **message d’aide**. |
   | Mots-clés de double opt-in | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br>Saisissez les mots-clés qui déclenchent le processus de double opt-in. Si un profil d’utilisateur ou d’utilisatrice n’existe pas, il est créé lors de la confirmation. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. [En savoir plus sur le double opt-in des SMS](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | Message de double opt-in | **Pour les nouvelles configurations SMS, utilisez le menu [Webhooks](sms-webhook.md) pour configurer les mots-clés de consentement. Les configurations existantes peuvent continuer à utiliser des mots-clés de consentement dans cette section.** </br>Saisissez la réponse personnalisée qui est automatiquement envoyée en réponse à la confirmation de double opt-in. |
   | Identifiant d’entité principale | Saisissez l’identifiant d’entité principale DLT qui vous a été attribué. |
   | Identifiant du modèle de contenu | Saisissez votre identifiant de modèle de contenu DLT enregistré. |
   | Période de validité | Saisissez la période de validité du message en heures. Si les messages ne peuvent pas être livrés dans ce délai, le système effectue d’autres tentatives pour les renvoyer. La période de validité par défaut est définie sur 48 heures. |
   | Données de rappel | Saisissez les données clients supplémentaires qui seront envoyées à l’URL de notification. |
   | Numéro entrant | Ajoutez votre numéro entrant unique. Cela permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun possédant son propre numéro entrant. |
   | Mots-clés entrants personnalisés | Définissez des mots-clés uniques et non liés au consentement pour des actions par lots, par exemple REMISE, OFFRES, INSCRIRE. Ces mots-clés sont capturés et stockés en tant qu’attributs dans le profil, ce qui vous permet de déclencher une qualification de segment par lots dans le parcours et de fournir une réponse ou une action personnalisée. |
   | Message de réponse entrant par défaut | Saisissez la réponse par défaut envoyée lorsqu’un utilisateur final ou une utilisatrice finale envoie un SMS entrant qui ne correspond à aucun des mots-clés définis. |

   +++

1. Activez l’option **[!UICONTROL Opt-out en logique floue]** pour détecter les messages ressemblant à des mots-clés d’opt-out (par exemple, « CANCIL ») et personnalisez la réponse de confirmation dans le champ **[!UICONTROL Réponse automatique en logique floue]**.

   L’option **[!UICONTROL Opt-out en logique floue]** identifie les SMS indiquant qu’une personne souhaite se désabonner, même si le message ne correspond pas exactement à un mot-clé d’opt-out défini. Les expressions de désabonnement courantes et certains termes offensants peuvent être détectés, ce qui permet de s’assurer que vos campagnes respectent les préférences des utilisateurs et utilisatrices et qu’elles restent conformes.

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
