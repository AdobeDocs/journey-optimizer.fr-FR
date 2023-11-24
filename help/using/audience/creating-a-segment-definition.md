---
solution: Journey Optimizer
product: journey optimizer
title: Créer des définitions de segment
description: Découvrez comment créer des audiences à l’aide de définitions de segment.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 3de42084d849047f218cf8dca2ad7e510759fb1c
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 88%

---

# Créer des définitions de segment {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Créer une règle"
>abstract="La méthode de création Créer une règle vous permet de créer une définition d’audience à l’aide du service d’audiences d’Adobe Experience Platform."

Dans cet exemple, nous allons créer une audience pour cibler tous les clientes et clients résidant à Atlanta, San Francisco ou Seattle et nés après 1980. Tous ces clientes et clients doivent avoir ouvert l’application Luma dans les 7 derniers jours, puis fait un achat dans les 2 heures suivant l’ouverture de l’application.

➡️ [Découvrez comment créer des audiences dans cette vidéo](#video-segment).

1. Dans la **[!UICONTROL Audiences]** , cliquez sur **[!UICONTROL Créer une audience]** et sélectionnez **[!UICONTROL Créer une règle]**.

   ![](assets/create-segment.png)

   L’écran de définition de segment vous permet de configurer tous les champs requis pour définir votre audience. Découvrez comment configurer des audiences dans la [documentation de service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr){target="_blank"}.

   ![](assets/segment-builder.png)

1. Dans le volet **[!UICONTROL Propriétés d’audience]**, indiquez un nom et une description (facultatif) pour l’audience.

   ![](assets/segment-properties.png)

1. Réalisez un glisser-déposer dans les champs de votre choix depuis le volet de gauche vers l’espace de travail central, puis configurez-les en fonction de vos besoins.

   >[!NOTE]
   >
   >Notez que les champs disponibles dans le volet de gauche varient selon la configuration des schémas **profil individuel XDM** et **XDM ExperienceEvent** pour votre organisation.  Pour en savoir plus, consultez la [documentation Modèle de données d’expérience (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.

   ![](assets/drag-fields.png)

   Dans cet exemple, nous devons nous baser sur les champs **Attributs** et **Événements** pour créer l’audience :

   * **Attributs** : profils qui vivent à Atlanta, San Francisco ou Seattle, nés après 1980

     ![](assets/add-attributes.png)

   * **Événements** : profils qui ont ouvert l’application Luma au cours des 7 derniers jours, puis effectué un achat dans les 2 heures suivant l’ouverture de l’application.

     ![](assets/add-events.png)

     >[!NOTE]
     >
     >Adobe recommande de ne pas utiliser les événements d’ouverture et d’envoi avec la segmentation par flux. Utilisez plutôt des signaux d’activité utilisateur réels tels que des clics, des achats ou des données de balise. Pour la logique de fréquence ou de suppression, utilisez des règles métier plutôt que d’envoyer des événements. [En savoir plus](about-audiences.md#open-and-send-event-guardrails)

1. À mesure que vous ajoutez et configurez de nouveaux champs dans l’espace de travail, le volet **[!UICONTROL Propriétés d’audience]** est automatiquement mis à jour avec des informations sur l’estimation des profils appartenant à l’audience.

   ![](assets/segment-estimate.png)

1. Une fois l’audience prête, cliquez sur **[!UICONTROL Enregistrer]**. Elle s’affiche dans la liste des audiences Adobe Experience Platform. Notez qu’une barre de recherche est disponible pour vous aider à rechercher une audience spécifique dans la liste.

L’audience peut désormais être utilisée dans vos parcours. Voir à ce propos [cette section](../audience/about-audiences.md).

## Vidéo pratique{#video-segment}

Découvrez comment Journey Optimizer utilise des règles pour générer une audience. Apprenez à utiliser des attributs, des événements et des audiences existantes pour créer une audience.

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)
