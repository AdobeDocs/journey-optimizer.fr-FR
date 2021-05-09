---
title: Créer des décisions
description: Découvrez comment créer des décisions
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Créer des décisions {#create-offer-activities}

Les décisions (précédemment connues sous le nom d&#39;activités d&#39;offre) sont des conteneurs pour vos offres qui exploiteront le moteur de décision d&#39;Offre afin de choisir la meilleure offre à fournir, selon la cible de la diffusion.

![](../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité dans la vidéo](#video)

La liste des décisions est accessible dans l&#39;onglet **[!UICONTROL Offres]** menu / **[!UICONTROL Décisions]**. Des filtres sont disponibles pour vous aider à récupérer les décisions en fonction de leur statut ou de leur début et de leurs dates de fin.

![](../assets/activities-list.png)

Avant de créer une décision, assurez-vous que les composants ci-dessous ont été créés dans la bibliothèque d’Offres :

* [Emplacements](../offer-library/creating-placements.md),
* [Collections](../offer-library/creating-collections.md),
* [Offres](../offer-library/creating-personalized-offers.md) personnalisées,
* [Offres](../offer-library/creating-fallback-offers.md) de secours.

## Créer la décision {#create-activity}

1. Accédez à la liste de décisions, puis cliquez sur **[!UICONTROL Créer une activité]**.

1. Indiquez le nom de la décision ainsi que son début et sa date et heure de fin, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](../assets/activities-name.png)

## Décisions d&#39;Ajoute {#add-decisions}

1. Faites glisser un emplacement de la liste pour l’ajouter à la décision, puis cliquez sur **[!UICONTROL Ajouter la collection]**.

   ![](../assets/activities-placement.png)

1. Sélectionnez la collection qui contient les offres à prendre en compte, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![](../assets/activities-collection.png)

1. Les offres sélectionnées sont ajoutées au placement. Dans cet exemple, nous avons sélectionné deux offres qui s’afficheront dans un emplacement de type JSON destiné à présenter des offres dans une solution de centre d’appels.

   ![](../assets/offers-added.png)

1. Par défaut, si plusieurs offres sont éligibles à cet emplacement, les offres ayant le score de priorité le plus élevé sont remises au client.

   Si vous souhaitez utiliser une formule spécifique pour choisir l’offre éligible à livrer, sélectionnez une formule de classement dans la liste déroulante **[!UICONTROL Classement des offres par]**. Pour plus d&#39;informations à ce sujet, consultez [cette section](../offer-activities/configure-offer-selection.md).

1. Le champ **[!UICONTROL Contrainte]** limite la sélection des offres pour cet emplacement. Cette contrainte peut être appliquée en utilisant une règle de décision ou un ou plusieurs segments Adobe Experience Platform.

   Pour limiter la sélection des offres aux membres d’un segment Adobe Experience Platform, sélectionnez **[!UICONTROL Segments]**, puis cliquez sur **[!UICONTROL Ajouter des segments]**.

   ![](../assets/activity_constraint_segment.png)

   Ajoutez un ou plusieurs segments dans le volet de gauche, combinez-les à l’aide des opérateurs logiques **[!UICONTROL Et]** / **[!UICONTROL Ou]**, puis cliquez sur **[!UICONTROL Sélectionner]** pour confirmer.

   Pour plus d’informations sur la façon d’utiliser les segments, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../assets/activity_constraint_segment2.png)

   Si vous souhaitez ajouter une contrainte de sélection pour cet emplacement à l&#39;aide d&#39;une règle de décision, sélectionnez l&#39;option **[!UICONTROL Règle de décision]**, puis faites glisser la règle de votre choix depuis le volet de gauche vers la zone **[!UICONTROL Règle de décision]**. Pour plus d&#39;informations sur la création d&#39;une règle de décision, consultez [cette section](../offer-library/creating-decision-rules.md).

   ![](../assets/activity_constraint_rule.png)

## Ajouter une offre de secours {#add-fallback}

Sélectionnez l’offre de secours qui sera présentée en dernier recours aux clients qui ne correspondent pas aux règles d&#39;éligibilité et contraintes des offres, puis cliquez sur **[!UICONTROL Suivant]**.

![](../assets/add-fallback-offer.png)

## Examiner et enregistrer la décision {#review}

Si tout est configuré correctement et que votre décision est prête à être utilisée pour présenter des offres aux clients, cliquez sur **[!UICONTROL Terminer]**, puis sélectionnez **[!UICONTROL Enregistrer et activer]**.

Vous pouvez également enregistrer la décision en tant que brouillon, afin de la modifier et de l’activer ultérieurement.

![](../assets/save-activities.png)

La décision s’affiche dans la liste avec l’état **[!UICONTROL Live]** ou **[!UICONTROL Brouillon]**, selon que vous l’avez activé ou non à l’étape précédente.

Il est maintenant prêt à être utilisé pour fournir des offres aux clients. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

Pour plus d’informations sur la diffusion des offres, reportez-vous aux sections suivantes :

* [Ajouter des offres personnalisées dans les messages](../../deliver-personalized-offers.md)
* [Fourniture d’offres à l’aide d’API](../api-reference/decisions-api/deliver-offers.md)

![](../assets/activities-created.png)

>[!NOTE]
>
>Une fois une décision créée, vous pouvez cliquer sur son nom dans la liste pour accéder à des informations détaillées et visualiser toutes les modifications qui y ont été apportées à l&#39;aide de l&#39;onglet **[!UICONTROL Journal des modifications]** (voir [Journal des modifications des Offres et décisions](../get-started/user-interface.md#changes-log)).

## Vidéo didactique {#video}

>[!NOTE]
>
>Cette vidéo s’applique au service d’applications d’Offer decisioning créé sur Adobe Experience Platform. Toutefois, il fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
