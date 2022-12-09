---
title: Créer des offres de secours
description: Découvrez comment créer des offres de secours à afficher pour les clients qui ne sont éligibles à aucune offre
topic: Integrations
role: User
level: Intermediate
exl-id: 9ba16ad9-a5e7-4ce7-8ed6-7707d37178c6
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Créer des offres de secours {#create-fallback-offers}

L’offre de secours est envoyée aux clients s’ils ne sont pas éligibles pour d’autres offres. Les étapes de création d’une offre de secours consistent à créer une ou plusieurs représentations, comme lors de la création d’une offre.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

La liste des offres de secours est accessible dans la variable **[!UICONTROL Offers]** .

![](../assets/offers_list.png)

Pour créer une offre de secours, procédez comme suit :

>[!NOTE]
>
>Notez que, contrairement aux offres personnalisées, les offres de secours n’ont pas de règles d’éligibilité ni de paramètres de contrainte, car elles sont présentées aux clients en dernier recours sans condition.

1. Cliquez sur **[!UICONTROL Create offer]**, puis sélectionnez **[!UICONTROL Fallback offer]**.

   ![](../assets/create_fallback.png)

1. Indiquez le nom de l’offre de secours. Vous pouvez également y associer une ou plusieurs balises existantes, ce qui vous permet de rechercher et d’organiser plus facilement la bibliothèque des offres.

   ![](../assets/fallback_details.png)

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à l’offre, sélectionnez **[!UICONTROL Manage access]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../../administration/object-based-access.md)

1. Créez une ou plusieurs représentations pour l’offre de secours. Pour ce faire, faites glisser des emplacements depuis le volet de gauche, comme lors de la création d’une offre personnalisée. Voir [Créer des offres personnalisées](../offer-library/creating-personalized-offers.md).

   ![](../assets/fallback_content.png)

1. Une fois les représentations de l’offre de secours ajoutées, un résumé s’affiche. Si tout est configuré correctement et que votre offre de secours est prête à être présentée aux clients, cliquez sur **[!UICONTROL Finish]**, puis sélectionnez **[!UICONTROL Save and approve]**.

   Vous pouvez également enregistrer l’offre de secours en tant que version préliminaire afin de la modifier et de l’approuver ultérieurement.

   ![](../assets/fallback_review.png)

1. L’offre de secours s’affiche dans la liste avec la variable **[!UICONTROL Live]** ou **[!UICONTROL Draft]** selon que vous l’avez approuvée ou non à l’étape précédente.

   Elle est maintenant prête à être diffusée aux clients. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier. <!-- no suppression? -->

   ![](../assets/fallback_created.png)

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329383?quality=12)

