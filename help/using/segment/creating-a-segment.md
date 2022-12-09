---
solution: Journey Optimizer
product: journey optimizer
title: Création d’un segment
description: Découvrez comment créer des segments
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Création de segments {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Création d’une règle"
>abstract="La méthode de création de règles Build vous permet de créer une définition de segment à l’aide d’Adobe Experience Platform Segmentation Service."

Dans cet exemple, nous allons créer un segment afin de cibler tous les clients qui vivent à Atlanta, San Francisco ou Seattle et qui sont nés après 1980. Tous ces clients auraient dû ouvrir l’application Luma au cours des 7 derniers jours, puis effectuer un achat dans les 2 heures suivant l’ouverture de l’application.

➡️ [Découvrez comment créer des segments dans cette vidéo](#video-segment)

1. Accédez au **[!UICONTROL Segments]** , puis cliquez sur **[!UICONTROL Create segment]** bouton .

   ![](assets/create-segment.png)

   L’écran de définition de segment vous permet de configurer tous les champs requis pour définir votre segment. Découvrez comment configurer des segments dans le [Documentation de Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}.

   ![](assets/segment-builder.png)

1. Dans le **[!UICONTROL Segment properties]** , indiquez un nom et une description (facultatif) pour le segment.

   ![](assets/segment-properties.png)

1. Faites glisser les champs de votre choix depuis le volet de gauche vers l’espace de travail central, puis configurez-les selon vos besoins.

   >[!NOTE]
   >
   >Notez que les champs disponibles dans le volet de gauche varient en fonction de la manière dont la variable **XDM Individual Profile** et **XDM ExperienceEvent** des schémas ont été configurés pour votre organisation.  En savoir plus dans la section [Documentation du modèle de données d’expérience (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

   ![](assets/drag-fields.png)

   Dans cet exemple, nous devons nous fier à **Attributs** et **Événements** champs pour créer le segment :

   * **Attributs**: profils habitant Atlanta, San Francisco ou Seattle, nés après 1980

      ![](assets/add-attributes.png)

   * **Événements**: profils ayant ouvert l’application Luma au cours des 7 derniers jours, puis effectué un achat dans les 2 heures suivant l’ouverture de l’application.

      ![](assets/add-events.png)

1. À mesure que vous ajoutez et configurez de nouveaux champs dans l’espace de travail, la variable **[!UICONTROL Segment Properties]** Le volet est automatiquement mis à jour avec des informations sur l’estimation des profils appartenant au segment.

   ![](assets/segment-estimate.png)

1. Une fois que le segment est prêt, cliquez sur **[!UICONTROL Save]**. Il s’affiche dans la liste des segments Adobe Experience Platform. Notez qu’une barre de recherche est disponible pour vous aider à rechercher un segment spécifique dans la liste.

Le segment peut désormais être utilisé dans vos parcours. Voir à ce sujet la section [cette section](../segment/about-segments.md).

## Vidéo pratique{#video-segment}

Découvrez comment créer des segments.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
