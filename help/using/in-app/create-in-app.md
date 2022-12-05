---
title: Créer une notification in-app
description: Découvrez comment créer un message in-app dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 100%

---

# Créer un message in-app {#create-in-app}

## Créer une campagne et un message in-app{#create-in-app-in-a-campaign}

Pour créer un message in-app, suivez les étapes ci-dessous :

1. Accédez au menu **[!UICONTROL Campagnes]**, puis cliquez sur **[!UICONTROL Créer une campagne]**.

1. Dans la section **[!UICONTROL Propriétés]**, indiquez quand exécuter la campagne.

1. Dans la section **[!UICONTROL Actions]**, choisissez le **[!UICONTROL Message in-app]** et la **[!UICONTROL Surface d’application]** précédemment configurée pour votre message in-app. Cliquez ensuite sur **[!UICONTROL Créer]**.

   [En savoir plus sur la configuration in-app](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la page de destination, sélectionnez **[!UICONTROL Gérer l’accès]**. [En savoir plus](../administration/object-based-access.md).

1. Cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour définir l’audience à cibler à partir de la liste des segments Adobe Experience Platform disponibles. [En savoir plus](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné. [En savoir plus](../event/about-creating.md#select-the-namespace).

1. Sélectionnez la fréquence de votre déclencheur lorsque votre message in-app est actif :

   * **[!UICONTROL Afficher à chaque fois]** : toujours afficher le message lorsque les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent.
   * **[!UICONTROL Afficher une fois]** : n’afficher ce message que la première fois que les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent.
   * **[!UICONTROL Afficher jusqu’au clic]** : afficher ce message lorsque les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent jusqu’à ce qu’un événement d’interaction soit envoyé par le SDK avec une action « faisant l’objet d’un clic ».

1. Dans le ou les menus déroulants **[!UICONTROL Déclencheur d’application mobile]**, choisissez le ou les événements et les critères qui déclencheront votre message :

   1. Dans le menu déroulant de gauche, sélectionnez l’événement nécessaire pour déclencher le message.
   1. Dans le menu déroulant de droite, sélectionnez la validation requise pour l’événement sélectionné.
   1. Cliquez sur le bouton **[!UICONTROL Ajouter]** si vous souhaitez que le déclencheur prenne en compte plusieurs événements ou critères. Répétez ensuite les étapes ci-dessus.
   1. Sélectionnez le mode de liaison de vos événements, par exemple choisissez **[!UICONTROL And]** si vous voulez que les déclencheurs soient **tous les deux** vérifiés pour que le message s’affiche ou choisissez **[!UICONTROL Or]** si vous souhaitez que le message ne s’affiche que si **l’un ou l’autre** des déclencheurs est vérifié.

   ![](assets/in_app_create_3.png)

1. Sélectionnez l’événement qui déclenche votre message dans le
menu déroulant **[!UICONTROL Déclencheur d’application mobile]**.

   En choisissant un déclencheur, vous choisissez l’action de l’utilisateur qui entraîne l’affichage du message in-app.

   ![](assets/in_app_create_3.png)

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planning]** de votre campagne dans [cette section](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Vous pouvez maintenant commencer à concevoir votre contenu à l’aide du bouton **[!UICONTROL Modifier le contenu]**.

   ![](assets/in_app_create_4.png)

## Envoyer vos messages in-app{#in-app-send}

### Aperçu sur l’appareil {#preview-device}

Vous pouvez prévisualiser la notification in-app sur un appareil spécifique.

1. Cliquez sur **[!UICONTROL Aperçu sur l’appareil]**.

   ![](assets/in_app_create_6.png)

1. Dans la fenêtre **[!UICONTROL Connexion à l’appareil]**, cliquez sur **[!UICONTROL Commencer]**.

1. Saisissez l’**[!UICONTROL URL de base]** de votre application, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/in_app_create_7.png)

1. Scannez le code QR avec votre appareil et saisissez le code PIN affiché.

Votre message in-app peut maintenant être déclenché directement sur votre appareil, ce qui vous permet de prévisualiser et de vérifier votre message sur un appareil réel.

### Vérifier et activer votre notification in-app{#in-app-review}

Une fois votre message in-app créé et son contenu défini et personnalisé, vous pouvez le vérifier et l’activer.

Pour ce faire, suivez les étapes ci-après :

1. Utilisez le bouton **[!UICONTROL Examiner pour activer]** pour afficher un résumé de votre message.

   Le résumé vous permet de modifier votre campagne si nécessaire et de vérifier si un paramètre est incorrect ou manquant.

   ![](assets/in_app_create_5.png)

1. Vérifiez que votre campagne est correctement configurée, puis cliquez sur **[!UICONTROL Activer]**.

Votre campagne est maintenant activée. La notification in-app configurée dans la campagne est envoyée immédiatement ou le sera à la date indiquée.

Une fois envoyés, vous pouvez mesurer l’impact de vos messages in-app dans le rapport Campaign. Pour plus d’informations sur le reporting, consultez [cette section](inapp-report.md).

**Rubriques connexes :**

* [Concevoir un message in-app](design-in-app.md)
* [Rapport in-app](inapp-report.md)
* [Configuration in-app](inapp-configuration.md)
