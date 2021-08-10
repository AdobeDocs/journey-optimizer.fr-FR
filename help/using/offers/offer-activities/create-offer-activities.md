---
title: Création de décisions
description: Découvrez comment créer des décisions
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: 80451fcd012257c8648e751076ed668aa05c44c7
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 100%

---

# Création de décisions {#create-offer-activities}

Les décisions (précédemment appelées activités d’offre) sont des conteneurs qui s’appuient sur le moteur de décision pour choisir la meilleure offre à diffuser en fonction de la cible de la diffusion.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

La liste des décisions est accessible dans le menu **[!UICONTROL Offres]**/onglet **[!UICONTROL Décisions]**. Des filtres sont disponibles pour vous aider à récupérer les décisions en fonction de leurs statuts ou de leurs dates de début ou de fin.

![](../../assets/activities-list.png)

Avant de créer une décision, vérifiez que les composants suivants ont été créés dans la bibliothèque des offres :

* [Emplacements](../offer-library/creating-placements.md)
* [Collections](../offer-library/creating-collections.md)
* [Offres personnalisées](../offer-library/creating-personalized-offers.md)
* [Offres de secours](../offer-library/creating-fallback-offers.md)

## Création de la décision {#create-activity}

1. Accédez à la liste des décisions, puis cliquez sur **[!UICONTROL Créer une décision]**.

1. Indiquez le nom de la décision, ainsi que ses dates et heures de début et de fin, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](../../assets/activities-name.png)

## Ajout des portées de décision {#add-decision-scopes}

1. Effectuez un glisser-déposer d&#39;un emplacement de la liste pour l&#39;ajouter à la décision, puis cliquez sur **[!UICONTROL Ajouter une collection]**.

   ![](../../assets/activities-placement.png)

   >[!NOTE]
   >
   >Un même emplacement peut être sélectionné plusieurs fois dans la décision.

1. Sélectionnez la collection qui contient les offres à prendre en compte, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![](../../assets/activities-collection.png)

1. Les offres sélectionnées sont ajoutées à l&#39;emplacement. Dans cet exemple, nous avons sélectionné deux offres qui s&#39;afficheront dans un emplacement de type JSON destiné à présenter des offres dans une solution de centre d&#39;appels.

   ![](../../assets/offers-added.png)

1. Par défaut, si plusieurs offres sont éligibles pour cet emplacement, ce sont les offres ayant le score de priorité le plus élevé qui sont diffusées au client.

   Si vous souhaitez utiliser une formule spécifique pour choisir l&#39;offre éligible à diffuser, sélectionnez une formule de classement dans la liste déroulante **[!UICONTROL Classer les offres par]**. Voir à ce propos [cette section](../offer-activities/configure-offer-selection.md).

1. Le champ **[!UICONTROL Contrainte]** limite la sélection des offres pour cet emplacement. Cette contrainte peut être appliquée en utilisant une règle de décision ou un ou plusieurs segments Adobe Experience Platform.

   Pour limiter la sélection des offres aux membres d&#39;un segment Adobe Experience Platform, sélectionnez **[!UICONTROL Segments]**, puis cliquez sur **[!UICONTROL Ajouter des segments]**.

   ![](../../assets/activity_constraint_segment.png)

   Ajoutez un ou plusieurs segments du volet de gauche, combinez-les à l&#39;aide des opérateurs logiques **[!UICONTROL Et]** / **[!UICONTROL Ou]**, puis cliquez sur **[!UICONTROL Sélectionner]** pour confirmer.

   Pour plus d’informations sur l’utilisation des segments, consultez [cette page](../../segment/about-segments.md).

   ![](../../assets/activity_constraint_segment2.png)

   Si vous souhaitez ajouter une contrainte de sélection pour cet emplacement à l&#39;aide d&#39;une règle de décision, sélectionnez l&#39;option **[!UICONTROL Règle de décision]**, puis faites glisser la règle de votre choix depuis le volet de gauche vers la zone **[!UICONTROL Règle de décision]**. Pour plus d&#39;informations sur la façon de créer une règle de décision, reportez-vous à [cette section](../offer-library/creating-decision-rules.md).

   ![](../../assets/activity_constraint_rule.png)

## Ajout d&#39;une offre de secours {#add-fallback}

Sélectionnez l&#39;offre de secours qui sera présentée en dernier recours aux clients qui ne correspondent pas aux règles d&#39;éligibilité et contraintes des offres, puis cliquez sur **[!UICONTROL Suivant]**.

![](../../assets/add-fallback-offer.png)

## Examen et enregistrement de la décision {#review}

Si tout est configuré correctement, un résumé des propriétés de la décision s&#39;affiche.

1. Vérifiez que la décision est prête à être utilisée pour présenter des offres aux clients.
1. Cliquez sur **[!UICONTROL Terminer]**.
1. Sélectionnez ensuite **[!UICONTROL Enregistrer et activer]**.

   ![](../../assets/save-activities.png)

   Vous pouvez également enregistrer la décision en tant que version préliminaire afin de la modifier et de l&#39;activer ultérieurement.

La décision s&#39;affiche dans la liste avec l&#39;état **[!UICONTROL Actif]** ou **[!UICONTROL Version préliminaire]**, selon que vous l&#39;avez activée ou non à l&#39;étape précédente.

Elle est maintenant prête à être utilisée pour diffuser des offres vers les clients.

## Liste des décisions {#decision-list}

Dans la liste des décisions, vous pouvez sélectionner la décision afin d&#39;afficher ses propriétés. Depuis cet emplacement, vous pouvez également la modifier, modifier son statut (**Version préliminaire**, **Actif**, **Terminé**, **Archivé**), la dupliquer ou la supprimer.

![](../../assets/decision_created.png)

Sélectionnez le bouton **[!UICONTROL Modifier]** pour revenir au mode d&#39;édition de la décision, où vous pouvez modifier ses [détails](#create-activity), les [portées de décision](#add-decision-scopes) et l&#39;[offre de secours](#add-fallback).

Sélectionnez une décision active et cliquez sur **[!UICONTROL Désactiver]** pour redéfinir le statut de la décision sur **[!UICONTROL Version préliminaire]**.

Pour définir à nouveau le statut sur **[!UICONTROL Actif]**, cliquez sur le bouton **[!UICONTROL Activer]** qui s&#39;affiche désormais.

![](../../assets/decision_activate.png)

Le bouton **[!UICONTROL Autres actions]** active les actions décrites ci-dessous.

![](../../assets/decision_more-actions.png)

* **[!UICONTROL Terminé]** : définit le statut de la décision sur **[!UICONTROL Terminé]**, ce qui signifie que la décision ne peut plus être appelée. Cette action n&#39;est disponible que pour les décisions activées. La décision est toujours disponible dans la liste, mais vous ne pouvez pas redéfinir son statut sur **[!UICONTROL Version préliminaire]** ou **[!UICONTROL Approuvé]**. Vous pouvez uniquement la dupliquer, la supprimer ou l&#39;archiver.

* **[!UICONTROL Dupliquer]** : crée une décision avec les mêmes propriétés, portées de décision et offre de secours. Par défaut, la nouvelle décision a le statut **[!UICONTROL Version préliminaire]**.

* **[!UICONTROL Supprimer]** : supprime la décision de la liste.

   >[!CAUTION]
   >
   >La décision et son contenu ne seront plus accessibles. Cette action ne peut pas être annulée.
   >
   >Si la décision est utilisée dans un autre objet, elle ne peut pas être supprimée.

* **[!UICONTROL Archiver]** : définit le statut de la décision sur **[!UICONTROL Archivé]**. La décision est toujours disponible dans la liste, mais vous ne pouvez pas redéfinir son statut sur **[!UICONTROL Version préliminaire]** ou **[!UICONTROL Approuvé]**. Vous pouvez uniquement la dupliquer ou la supprimer.

Vous pouvez également supprimer ou modifier le statut de plusieurs décisions en même temps en cochant les cases correspondantes.

![](../../assets/decision_multiple-selection.png)

Si vous souhaitez modifier le statut de plusieurs décisions dont les statuts sont différents, seuls les statuts correspondants seront modifiés.

![](../../assets/decision_change-status.png)

Une fois une décision créée, vous pouvez cliquer sur son nom dans la liste.

![](../../assets/decision_click-name.png)

Vous pouvez ainsi accéder à des informations détaillées sur cette décision. Sélectionnez l&#39;onglet **[!UICONTROL Log des modifications]** pour [surveiller toutes les modifications](../get-started/user-interface.md#changes-log) qui ont été apportées à la décision.

![](../../assets/decision_information.png)

## Tutoriel vidéo {#video}

>[!NOTE]
>
>Cette vidéo s&#39;applique au service applicatif d&#39;Offer Decisioning basé sur Adobe Experience Platform. Elle fournit toutefois des orientations générales pour l&#39;utilisation d&#39;Offer dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
