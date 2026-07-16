---
title: Test de votre canal personnalisé
description: Découvrez comment tester la connexion, simuler le contenu et tester vos messages de canal personnalisés dans Adobe Journey Optimizer avant l’activation.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---


# Test de votre canal personnalisé {#test-custom-channel}

Avant d’activer un parcours ou une campagne qui utilise un canal personnalisé, vérifiez que votre point d’entrée est accessible, que l’authentification fonctionne et que les jetons de personnalisation sont résolus correctement pour vos profils cibles.

## Tester la connexion à partir du créateur de canaux {#test-connection}

Lorsqu’un canal personnalisé est à l’état **[!UICONTROL Brouillon]**, utilisez le bouton **[!UICONTROL Test]** dans le Créateur de canaux pour envoyer une requête de test à votre point d’entrée et valider la connexion de bout en bout avant l’activation. [En savoir plus](create-custom-channel.md#test-connection)

Ce test confirme :

* Le point d’entrée est accessible à partir des adresses IP sortantes de [!DNL Journey Optimizer].
* Vérifiez que les informations d’authentification configurées sont valides.
* Le point d’entrée renvoie une réponse HTTP 2xx.

Vérifiez les journaux de votre système externe pour vous assurer que la demande de test a été reçue avec les en-têtes et la structure de payload attendus.

## Simuler du contenu avec des profils de test {#simulate-content}

La fonctionnalité **[!UICONTROL Simuler du contenu]** résout les expressions de personnalisation par rapport aux profils de test afin que vous puissiez examiner la payload exacte qui serait envoyée avant qu’un message réel ne soit diffusé.

1. Dans l’action de parcours ou l’écran d’édition de la campagne, cliquez sur **[!UICONTROL Simuler du contenu]**.

1. Cliquez sur **[!UICONTROL Ajouter un profil de test]** et sélectionnez un ou plusieurs profils. [En savoir plus sur la création de profils de test](../audience/creating-test-profiles.md)

1. Examinez la payload résolue dans le panneau d’aperçu. Pour chaque profil de test, vérifiez les points suivants :

   * Tous les jetons de personnalisation (par exemple, `{{profile.person.name.firstName}}`) ont été remplacés par les valeurs attendues du profil.
   * Il ne reste aucun jeton non résolu (affiché sous la forme de chaînes vides ou de syntaxe de `{{...}}` littérale).
   * Les champs de payload obligatoires sont renseignés.
   * Les fonctions d’assistance produisent la sortie formatée attendue.

>[!TIP]
>
>Testez plusieurs profils représentant différents segments d’audience pour détecter les cas de périphérie, par exemple, les profils comportant des attributs facultatifs manquants, des jeux de caractères non latins ou des valeurs nulles dans des champs personnalisés.

## Envoi d&#39;un BAT {#send-proof}

Pour valider une diffusion de bout en bout avant l’activation, envoyez un BAT à un ensemble de destinataires test :

1. Dans le panneau **[!UICONTROL Simuler du contenu]**, passez à l’onglet **[!UICONTROL Envoyer un BAT]**.

1. Ajoutez les profils que vous souhaitez utiliser. Vous pouvez charger un fichier CSV avec des profils qui ne sont pas définis comme des profils de test dans [!DNL Journey Optimizer].

1. Cliquez sur **[!UICONTROL Envoyer un BAT]**. [!DNL Journey Optimizer] appelle votre point d’entrée externe avec la payload personnalisée pour chaque profil sélectionné.

1. Vérifiez votre système externe pour vous assurer que les payloads du BAT ont bien été reçues. Pour les canaux de messagerie (par exemple, WeChat ou Kakao Talk), vérifiez que le message s’affiche sur l’appareil ou l’application de messagerie cible.

Le résultat du BAT s’affiche en utilisant les mêmes modèles de validation que la relecture des e-mails : les champs obligatoires, les incohérences de type et les erreurs de validation de schéma sont affichés avant l’envoi du BAT.

En savoir plus sur l’envoi de BAT dans [campagnes](../campaigns/create-campaign.md#send-proof) et [parcours &#x200B;](../building-journeys/testing-the-journey.md).

## Test en mode parcours {#test-journey}

Pour une validation de parcours de bout en bout, activez le parcours en **[!UICONTROL mode Test]** :

1. Dans la zone de travail de parcours, cliquez sur **[!UICONTROL Tester]** dans la zone supérieure droite.

1. Configurez l’événement déclencheur ou sélectionnez un profil de test pour un parcours déclenché par une audience.

1. Cliquez sur **[!UICONTROL Déclencher un événement]** ou laissez le profil rejoindre une activité **[!UICONTROL Lecture d’audience]**.

1. Observez le flux dans la zone de travail. Lorsqu’un profil atteint le nœud d’action de canal personnalisé, [!DNL Journey Optimizer] appelle votre point d’entrée externe avec la payload personnalisée.

1. Vérifiez les journaux de votre système externe pour vous assurer que la demande a été correctement reçue.

1. Cliquez sur **[!UICONTROL Arrêter le test]** lorsque vous avez terminé.

En savoir plus sur le test de parcours en [mode test](../building-journeys/testing-the-journey.md).

## Simulation d’un parcours {#simulate-journey}

Le mode **Simulation** de [!DNL Journey Optimizer] vous permet de valider votre parcours de bout en bout à l’aide d’utilisateurs simulés (des entités temporaires de type profil qui ne sont pas conservées dans Adobe Experience Platform) sans avoir à créer de profils de test au préalable.

Pour les canaux personnalisés, la simulation résout les expressions de personnalisation et effectue le rendu de l’aperçu de la payload pour chaque utilisateur simulé, afin que vous puissiez vérifier que le contenu correct sera diffusé avant la mise en ligne.

Pour simuler un parcours à l’aide d’un canal personnalisé :

1. Dans la zone de travail de parcours, cliquez sur **[!UICONTROL Simuler]** dans la zone supérieure droite.

1. Ajoutez manuellement des utilisateurs simulés ou générez-les à l’aide de l’option **[!UICONTROL Simulation rapide]** optimisée par IA.

1. Configurez les événements d’entrée requis, puis déclenchez les utilisateurs simulés via le parcours.

1. Lorsqu’un utilisateur simulé atteint le nœud d’action de canal personnalisé, inspectez la payload résolue dans le panneau d’aperçu pour confirmer que les jetons de personnalisation et la structure de la payload sont corrects.

>[!NOTE]
>
>La simulation est disponible pour les parcours en version brouillon et en direct et utilise des utilisateurs simulés temporaires qui ne sont pas pris en compte dans les quotas de profil ou les appels de point d’entrée réels.

[En savoir plus sur la simulation de parcours](../building-journeys/simulate-journey-gs.md)

## Liste de contrôle de pré-activation {#checklist}

Avant d’activer votre parcours ou votre campagne, vérifiez les points suivants :

* Le test de la connexion du Channel Builder a réussi (point d’entrée atteignable, authentification valide).
* Les payloads simulées affichent les valeurs attendues pour tous les profils de test.
* Il ne reste aucun jeton de personnalisation non résolu dans la payload.
* Tous les champs de payload obligatoires sont renseignés.
* Un BAT a été envoyé et reçu correctement par votre système externe.
* Les chemins d’erreur de l’activité d’action de parcours (s’ils sont configurés) gèrent les scénarios d’échec comme prévu.

Une fois le test terminé, passez à l’activation. [Voici comment procéder](create-custom-experience.md#activate)
