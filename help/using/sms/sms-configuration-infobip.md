---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Infobip
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS et MMS avec Journey Optimizer avec Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 604af3a0ac9febb62f2e2b1705e2751b2c476e04
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 62%

---

# Configurer le fournisseur Infobip {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Si les mots-clés relatifs à l’opt-in ou à l’opt-out ne sont pas fournis, des messages de consentement standard sont utilisés pour respecter la confidentialité des personnes. L’ajout de mots-clés personnalisés remplace automatiquement les valeurs par défaut.

**Mots-clés par défaut :**

* **Opt-in** : SUBSCRIBE (s’abonner), YES (oui), UNSTOP (redémarrer), START (démarrer), CONTINUE (continuer), RESUME (reprendre), BEGIN (commencer).
* **Opt-out** : STOP (arrêter), QUIT (quitter), CANCEL (annuler), END (terminer), UNSUBSCRIBE (se désabonner), NO (non).
* **Aide** : HELP (aide).

>[!ENDSHADEBOX]

## Configuration des informations d’identification d’API pour les SMS

Pour configurer Infobip avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez les informations d’identification pour l’API SMS, comme indiqué ci-dessous :

+++ Liste des informations d’identification SMS pour la configuration

   | Champs de configuration | Description |
   |---|---|    
   | Fournisseur SMS | Infobip |
   | Nom | Saisissez un nom pour vos informations d’identification API. |
   | URL de base et clé API | Accédez à la page d’accueil de votre interface web ou à la page de gestion des clés API pour trouver vos informations d’identification. En savoir plus dans la [documentation Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | Mots-clés d’opt-in | Saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre message d’opt-in. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. |
   | Message d’opt-in | Saisissez la réponse personnalisée qui est automatiquement envoyée en tant que message d’opt-in. |
   | Mots-clés d’opt-out | Saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre message d’opt-out. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. |
   | Message d’opt-out | Saisissez la réponse personnalisée qui est automatiquement envoyée en tant que message d’opt-out. |
   | Mots-clés d’aide | Saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **message d’aide**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. |
   | Message d’aide | Saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **message d’aide**. |
   | Mots-clés de double opt-in | Saisissez les mots-clés qui déclenchent le processus de double opt-in. Si un profil d’utilisateur ou d’utilisatrice n’existe pas, il est créé lors de la confirmation. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules. [En savoir plus sur le double opt-in des SMS](https://video.tv.adobe.com/v/3440276/?learn=on&captions=fre_fr). |
   | Message de double opt-in | Saisissez la réponse personnalisée qui est automatiquement envoyée en réponse à la confirmation de double opt-in. |
   | ID d’entité principale | Saisissez l’ID d’entité principale DLT qui vous a été attribué. |
   | Identifiant du modèle de contenu | Saisissez votre identifiant de modèle de contenu DLT enregistré. |
   | Période de validité | Saisissez la période de validité du message en heures. Si les messages ne peuvent pas être livrés dans ce délai, le système effectue d’autres tentatives pour les renvoyer. La période de validité par défaut est définie sur 48 heures. |
   | Données de rappel | Saisissez les données client supplémentaires qui seront envoyées sur l’URL de notification. |
   | Numéro entrant | Ajoutez votre numéro entrant unique. Cela vous permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun ayant son propre numéro entrant. |
   | Mots-clés entrants personnalisés | Définissez des mots-clés uniques pour des actions spécifiques, par exemple REMISE, OFFRES, INSCRIRE. Ces mots-clés sont capturés et stockés en tant qu’attributs dans le profil, ce qui vous permet de déclencher une qualification de segment en continu dans le parcours et de fournir une réponse ou une action personnalisée. |
   | Message de réponse entrant par défaut | Saisissez la réponse par défaut envoyée lorsqu’un utilisateur final ou une utilisatrice finale envoie un SMS entrant qui ne correspond à aucun des mots-clés définis. |

+++

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une configuration de canal pour les messages SMS et MMS. [En savoir plus](sms-configuration-surface.md)

## Configuration des informations d’identification d’API pour RCS

La messagerie RCS est prise en charge dans Adobe Journey Optimizer via Infobip à l’aide de la fonctionnalité [Fournisseur de SMS personnalisé](sms-configuration-custom.md). Cela permet de diffuser des messages riches et interactifs par le biais de profils professionnels vérifiés, en incorporant des éléments tels que des carrousels, des boutons et du contenu multimédia.

➡️ [Découvrez comment Infobip prend en charge RCS dans la documentation Infobip](https://www.infobip.com/docs/api/channels/rcs)

Pour activer la messagerie RCS avec Infobip, les nouvelles informations d’identification d’API doivent être configurées via un fournisseur de SMS personnalisé. Les informations d’identification SMS Infobip existantes ne sont pas compatibles, car RCS nécessite un format de payload distinct.

Pour configurer RCS avec Infobip :

1. **Enregistrez votre entreprise pour RCS via Infobip**

   Commencez par terminer le processus d’intégration et d’enregistrement RCS dans la plateforme Infobip. Cela implique de configurer votre profil d’expéditeur RCS et de vous assurer que votre compte est compatible RCS. En savoir plus dans la [documentation Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Créer un Webhook SMS**

   [Configurez un webhook SMS personnalisé](sms-configuration-custom.md#webhook) dans Journey Optimizer. Ce webhook sera chargé de gérer les accusés de réception de diffusion, les messages RCS entrants et les mises à jour de statut de la plateforme d&#39;Infobip.

1. **Créer des informations d’identification d’API à l’aide de Personnalisé en tant que fournisseur SMS**

   [Créez des informations d’identification d’API](sms-configuration-custom.md#api-credential) dans Journey Optimizer, en sélectionnant « Personnalisé » comme fournisseur SMS. Utilisez la méthode d’authentification de point d’entrée RCS appropriée, l’URL de base et les en-têtes.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une configuration de canal pour vos messages RCS. [En savoir plus](sms-configuration-surface.md)
