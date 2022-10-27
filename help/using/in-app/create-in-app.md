---
title: Créer une notification In-App
description: Découvrez comment créer un message in-app dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 74f24c4ccdecd5afe52706e1ecb2d323c3200152
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 16%

---


# Création d’un message in-app {#create-in-app}

## Créer une campagne et un message in-app{#create-in-app-in-a-campaign}

Pour créer un message In-App, procédez comme suit :

1. Accédez au menu **[!UICONTROL Campagnes]**, puis cliquez sur **[!UICONTROL Créer une campagne]**.

1. Dans le **[!UICONTROL Propriétés]** , indiquez quand exécuter la campagne.

1. Dans le **[!UICONTROL Actions]** , choisissez la **[!UICONTROL Message in-app]** et le **[!UICONTROL Surface de l’application]** précédemment configuré pour votre message in-app. Cliquez ensuite sur **[!UICONTROL Créer]**.

   [En savoir plus sur la configuration In-App](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Dans la **[!UICONTROL Propriétés]** , modifiez la section de votre campagne **[!UICONTROL Titre]** et **[!UICONTROL Description]**.

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la page de destination, sélectionnez **[!UICONTROL Gérer l’accès]**. [En savoir plus](../administration/object-based-access.md).

1. Cliquez sur le bouton **[!UICONTROL Sélection de l’audience]** pour définir l’audience à cibler à partir de la liste des segments Adobe Experience Platform disponibles. [En savoir plus](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné. [En savoir plus](../event/about-creating.md#select-the-namespace).

1. Sélectionnez la fréquence de votre trigger lorsque votre message in-app est principal :

   * **[!UICONTROL Afficher à chaque fois]**: Toujours afficher le message lorsque les événements sélectionnés dans la variable **[!UICONTROL Déclencheur d’application mobile]** s’affiche.
   * **[!UICONTROL Afficher une fois]**: N’afficher ce message que la première fois que les événements sont sélectionnés dans la variable **[!UICONTROL Déclencheur d’application mobile]** s’affiche.
   * **[!UICONTROL Afficher jusqu’à ce que clic]**: Afficher ce message lorsque les événements sélectionnés dans la variable **[!UICONTROL Déclencheur d’application mobile]** se produit jusqu’à ce qu’un événement d’interaction soit envoyé par le SDK avec une action &quot;clicked&quot;.

1. Dans la **[!UICONTROL Déclencheur d’application mobile]** , choisissez le ou les événements et les critères qui déclencheront votre message :

   1. Dans la liste déroulante de gauche, sélectionnez l’événement nécessaire pour déclencher le message.
   1. Dans la liste déroulante de droite, sélectionnez la validation requise pour l’événement sélectionné.
   1. Cliquez sur le bouton **[!UICONTROL Ajouter]** si vous souhaitez que le déclencheur prenne en compte plusieurs événements ou critères. Répétez ensuite les étapes ci-dessus.
   1. Sélectionnez le mode de liaison de vos événements, par exemple **[!UICONTROL Et]** si vous voulez **both** se déclenche pour que le message s’affiche et **[!UICONTROL Ou]** si vous souhaitez que le message s’affiche **both** des déclencheurs sont vrais.

   ![](assets/in_app_create_3.png)

1. Sélectionnez l’événement qui déclenche votre message dans la **[!UICONTROL Déclencheur d’application mobile]**
menu déroulant.

   En choisissant un déclencheur, vous choisissez l’action de l’utilisateur qui entraîne l’affichage du message in-app.

   ![](assets/in_app_create_3.png)

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planification]** de votre campagne dans [cette section](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Vous pouvez maintenant commencer à concevoir votre contenu à l’aide de la méthode **[!UICONTROL Modifier le contenu]** bouton .

   ![](assets/in_app_create_4.png)

## Envoyer vos messages In-App{#in-app-send}

### Aperçu sur l’appareil {#preview-device}

Vous pouvez prévisualiser la notification In-App sur un appareil spécifique.

1. Cliquez sur **[!UICONTROL Aperçu sur l’appareil]**.

   ![](assets/in_app_create_6.png)

1. Dans la **[!UICONTROL Connexion à l’appareil]** fenêtre, cliquez sur **[!UICONTROL Début]**.

1. Saisissez dans la variable **[!UICONTROL URL de base]** de votre application, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/in_app_create_7.png)

1. Analysez le code QR avec votre appareil et saisissez le code PIN affiché.

Votre message in-app peut maintenant être déclenché directement sur votre appareil, ce qui vous permet de prévisualiser et de revoir votre message sur un appareil réel.

### Vérifier et activer votre notification In-App{#in-app-review}

Une fois votre message In-App créé et son contenu défini et personnalisé, vous pouvez le consulter et l&#39;activer.

Pour ce faire, suivez les étapes ci-après :

1. Utilisez la variable **[!UICONTROL Réviser pour activer]** pour afficher un résumé de votre message.

   Le résumé vous permet de modifier votre campagne si nécessaire et de vérifier si un paramètre est incorrect ou manquant.

   ![](assets/in_app_create_5.png)

1. Vérifiez que votre campagne est correctement configurée, puis cliquez sur **[!UICONTROL Activer]**.

Votre campagne est maintenant activée. La notification In-App configurée dans la campagne est envoyée immédiatement ou à la date spécifiée.

Une fois envoyés, vous pouvez mesurer l’impact de vos messages In-App dans le rapport Campaign. Pour plus d’informations sur le reporting, consultez [cette section](inapp-report.md).

**Rubriques connexes :**

* [Concevoir un message in-app](design-in-app.md)
* [Rapport in-app](inapp-report.md)
* [Configuration In-App](inapp-configuration.md)
