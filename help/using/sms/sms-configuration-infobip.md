---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le fournisseur Infobip
description: Découvrir comment configurer votre environnement pour envoyer des messages SMS et MMS avec Journey Optimizer avec Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: ht
source-wordcount: '485'
ht-degree: 100%

---

# Configurer le fournisseur Infobip {#sms-configuration-infobip}

Pour configurer Infobip avec Journey Optimizer, procédez comme suit :

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations dʼidentification de lʼAPI, comme indiqué ci-dessous.

   * **[!UICONTROL Fournisseur de SMS]** : Infobip.

   * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

   * **[!UICONTROL URL de base de l’API]** et **[!UICONTROL Clé API]** : accédez à la page d’accueil de votre interface web ou à la page de gestion des clés d’API pour trouver vos informations d’identification. En savoir plus dans la [Documentation Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Mots-clés d’opt-in]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **[!UICONTROL message d’opt-in]**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’opt-in]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **[!UICONTROL message d’opt-in]**.

   * **[!UICONTROL Mots-clés d’opt-out]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **[!UICONTROL message d’opt-out]**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’opt-out]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **[!UICONTROL message d’opt-out]**.

   * **[!UICONTROL Mots-clés d’aide]** : saisissez les mots-clés par défaut ou personnalisés qui déclencheront automatiquement votre **message d’aide**. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message d’aide]** : saisissez la réponse personnalisée qui est automatiquement envoyée en tant que **message d’aide**.

   * **[!UICONTROL Mots-clés de double opt-in]** : saisissez les mots-clés qui déclenchent le processus de double opt-in. Si un profil de personne n’existe pas, il est créé lors de la confirmation. Pour plusieurs mots-clés, utilisez des valeurs séparées par des virgules.

   * **[!UICONTROL Message de double opt-in]** : saisissez la réponse personnalisée qui est automatiquement envoyée en réponse à la confirmation de double opt-in.

   * **[!UICONTROL ID d’entité principale]** : saisissez l’ID d’entité principale DLT qui vous a été attribué.

   * **[!UICONTROL ID de modèle de contenu]** : saisissez l’ID de modèle de contenu DLT enregistré.

   * **[!UICONTROL Période de validité]** : saisissez la période de validité du message en heures. Si les messages ne peuvent pas être livrés dans ce délai, le système effectue d’autres tentatives pour les renvoyer. La période de validité par défaut est définie sur 48 heures.

   * **[!UICONTROL Données de rappel]** : saisissez les données clientes supplémentaires qui seront envoyées à l’URL de notification.

   * **[!UICONTROL Numéro entrant]** : ajoutez votre numéro entrant unique. Cela vous permet d’utiliser les mêmes informations d’identification d’API dans différents sandbox, chacun ayant son propre numéro entrant.

   * **[!UICONTROL Mots-clés entrants personnalisés]** : définissez des mots-clés uniques pour des actions spécifiques, par exemple REMISE, OFFRES, INSCRIRE. Ces mots-clés sont capturés et stockés en tant qu’attributs dans le profil, ce qui vous permet de déclencher une qualification de segment en continu dans le parcours et de fournir une réponse ou une action personnalisée.

   * **[!UICONTROL Message de réponse entrant par défaut]** : saisissez la réponse par défaut envoyée lorsqu’un utilisateur final ou une utilisatrice finale envoie un SMS entrant qui ne correspond à aucun des mots-clés définis.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

1. Dans le menu **[!UICONTROL Informations d’identification d’API]**, cliquez sur l’icône de corbeille pour supprimer vos informations d’identification d’API.

1. Pour modifier les informations d’identification existantes, recherchez les informations d’identification d’API souhaitées et cliquez sur l’option **[!UICONTROL Modifier]** pour apporter les modifications nécessaires.

Après avoir créé et configuré vos informations d’identification de l’API, vous devez maintenant créer une configuration de canal pour les messages SMS et MMS. [En savoir plus](sms-configuration-surface.md)
