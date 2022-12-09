---
title: Créer des décisions
description: Découvrez comment créer des décisions
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%

---

# Créer des décisions {#create-offer-activities}

Les décisions sont des conteneurs pour vos offres qui exploiteront le moteur de décision d’offre afin de sélectionner la meilleure offre à diffuser, en fonction de la cible de la diffusion.

➡️ [Découvrez comment créer des activités d’offre dans cette vidéo](#video)

La liste des décisions est accessible dans le **[!UICONTROL Offers]** menu > **[!UICONTROL Decisions]** . Des filtres sont disponibles pour vous aider à récupérer les décisions en fonction de leur état ou de leurs dates de début et de fin.

![](../assets/activities-list.png)

Avant de créer une décision, assurez-vous que les composants ci-dessous ont été créés dans la bibliothèque des offres :

* [Emplacements](../offer-library/creating-placements.md)
* [Collections](../offer-library/creating-collections.md)
* [Offres personnalisées](../offer-library/creating-personalized-offers.md)
* [Offres de secours](../offer-library/creating-fallback-offers.md)

## Créer la décision {#create-activity}

1. Accédez à la liste de décisions, puis cliquez sur **[!UICONTROL Create decision]**.

1. Indiquez le nom de la décision.

1. Si nécessaire, définissez une date et une heure de début et de fin, puis cliquez sur **[!UICONTROL Next]**.

   ![](../assets/activities-name.png)

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la décision, sélectionnez **[!UICONTROL Manage access]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../../administration/object-based-access.md)

## Définition des portées de décision {#add-decision-scopes}

1. Sélectionnez un emplacement dans la liste déroulante. Il sera ajouté à la première portée de décision de votre décision.

   ![](../assets/activities-placement.png)

1. Cliquez sur **[!UICONTROL Add]** pour sélectionner les critères d’évaluation de cet emplacement.

   ![](../assets/activities-evaluation-criteria.png)

   Chaque critère consiste en une collection d’offres associée à une contrainte d’éligibilité et à une méthode de classement permettant de déterminer les offres à afficher dans l’emplacement.

   >[!NOTE]
   >
   >Au moins un critère d’évaluation est requis.

1. Sélectionnez la collection d’offres qui contient les offres à prendre en compte, puis cliquez sur **[!UICONTROL Add]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >Vous pouvez cliquer sur le bouton **[!UICONTROL Open offer collections]** lien pour afficher la liste des collections dans un nouvel onglet, qui permet de parcourir les collections et les offres qu’elles contiennent.

   La collection sélectionnée est ajoutée au critère.

   ![](../assets/activities-collection-added.png)

1. Utilisez la variable **[!UICONTROL Eligibility]** pour restreindre la sélection des offres pour cet emplacement.

   Cette contrainte peut être appliquée en utilisant une **règle de décision** ou un ou plusieurs **Segments Adobe Experience Platform**. Les deux sont présentés dans la section [cette section](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * Pour restreindre la sélection des offres aux membres d’un segment Experience Platform, sélectionnez **[!UICONTROL Segments]**, puis cliquez sur **[!UICONTROL Add segments]**.

      ![](../assets/activity_constraint_segment.png)

      Ajoutez un ou plusieurs segments depuis le volet de gauche, puis combinez-les à l’aide de la fonction **[!UICONTROL And]** / **[!UICONTROL Or]** opérateurs logiques.

      ![](../assets/activity_constraint_segment2.png)

      Découvrez comment utiliser les segments dans [cette section](../../segment/about-segments.md).

   * Si vous souhaitez ajouter une contrainte de sélection à une règle de décision, utilisez la variable **[!UICONTROL Decision rule]** et sélectionnez la règle de votre choix.

      ![](../assets/activity_constraint_rule.png)

      Découvrez comment créer une règle de décision dans [cette section](../offer-library/creating-decision-rules.md).

1. Lorsque vous sélectionnez des segments ou des règles de décision, vous pouvez afficher des informations sur les profils qualifiés estimés. Cliquez sur **[!UICONTROL Refresh]** pour mettre à jour les données.

   >[!NOTE]
   >
   >Les estimations de profil ne sont pas disponibles lorsque les paramètres de règle incluent des données qui ne figurent pas dans le profil, telles que des données contextuelles. Par exemple, une règle d’éligibilité qui exige que la météo actuelle soit de ≥80 degrés.

   ![](../assets/activity_constraint-estimate.png)

1. Définissez la méthode de classement à utiliser pour sélectionner la meilleure offre pour chaque profil.

   ![](../assets/activity_ranking-method.png)

   * Par défaut, si plusieurs offres sont éligibles pour cet emplacement, l’offre ayant le score de priorité le plus élevé est diffusée au client.

   * Si vous souhaitez utiliser une formule spécifique pour choisir l’offre éligible à diffuser, sélectionnez **[!UICONTROL Ranking formula]**. Découvrez comment classer les offres dans [cette section](../offer-activities/configure-offer-selection.md).

1. Cliquez sur **[!UICONTROL Add]** pour définir d’autres critères pour le même emplacement.

   ![](../assets/activity_add-collection.png)

1. Lorsque vous ajoutez plusieurs critères, ils sont évalués dans un ordre spécifique. La première collection ajoutée à la séquence sera évaluée en premier, etc.

   Pour modifier la séquence par défaut, vous pouvez faire glisser et déposer les collections afin de les réorganiser selon vos besoins.

   ![](../assets/activity_reorder-collections.png)

1. Vous pouvez également évaluer plusieurs critères en même temps. Pour ce faire, faites glisser la collection au-dessus d’une autre.

   ![](../assets/activity_move-collection.png)

   Ils ont maintenant le même rang et seront donc évalués en même temps.

   ![](../assets/activity_same-rank-collections.png)

1. Pour ajouter un autre emplacement pour vos offres dans le cadre de cette décision, utilisez la variable **[!UICONTROL New scope]** bouton . Répétez les étapes ci-dessus pour chaque portée de décision.

   ![](../assets/activity_new-scope.png)

## Ajouter une offre de secours {#add-fallback}

Une fois que vous avez défini les portées de décision, définissez l’offre de secours qui sera présentée en dernier recours aux clients qui ne correspondent pas aux règles d’éligibilité et contraintes des offres.

Pour ce faire, sélectionnez-le dans la liste des offres de secours disponibles pour les emplacements définis dans la décision, puis cliquez sur **[!UICONTROL Next]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>Vous pouvez cliquer sur le bouton **[!UICONTROL Open offer library]** lien pour afficher la liste des offres dans un nouvel onglet.

## Vérifier et enregistrer la décision {#review}

Si tout est configuré correctement, un résumé des propriétés de décision s’affiche.

1. Assurez-vous que la décision est prête à être utilisée pour présenter des offres aux clients. Toutes les portées de décision et l’offre de secours qu’elle contient s’affichent.

   ![](../assets/review-decision.png)

1. Vous pouvez développer ou réduire chaque emplacement. Vous pouvez prévisualiser les offres disponibles, ainsi que les détails d’éligibilité et de classement pour chaque emplacement. Vous pouvez également afficher des informations sur les profils qualifiés estimés. Cliquez sur **[!UICONTROL Refresh]** pour mettre à jour les données.

   ![](../assets/review-decision-details.png)

1. Cliquez sur **[!UICONTROL Finish]**.
1. Sélectionner **[!UICONTROL Save and activate]**.

   ![](../assets/save-activities.png)

   Vous pouvez également enregistrer la décision en tant que brouillon afin de la modifier et de l’activer ultérieurement.

La décision s’affiche dans la liste avec le **[!UICONTROL Live]** ou **[!UICONTROL Draft]** selon que vous l’avez activée ou non à l’étape précédente.

Il est maintenant prêt à être utilisé pour diffuser des offres aux clients.

## Liste de décisions {#decision-list}

Dans la liste de décisions, vous pouvez sélectionner la décision d’afficher ses propriétés. De là, vous pouvez également la modifier, modifier son état (**Version préliminaire**, **En direct**, **Terminer**, **Archivé**), dupliquez la décision ou supprimez-la.

![](../assets/decision_created.png)

Sélectionnez la **[!UICONTROL Edit]** pour revenir au mode d’édition de la décision, où vous pouvez modifier le [détails](#create-activity), [portées de décision](#add-decision-scopes) et [offre de secours](#add-fallback).

Sélectionnez une décision en direct et cliquez sur **[!UICONTROL Deactivate]** pour rétablir l’état de décision sur **[!UICONTROL Draft]**.

Pour définir à nouveau l’état sur **[!UICONTROL Live]**, sélectionnez la variable **[!UICONTROL Activate]** qui s’affiche maintenant.

![](../assets/decision_activate.png)

Le **[!UICONTROL More actions]** active les actions décrites ci-dessous.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**: définit l’état de la décision sur **[!UICONTROL Complete]**, ce qui signifie que la décision ne peut plus être appelée. Cette action n’est disponible que pour les décisions activées. La décision est toujours disponible dans la liste, mais vous ne pouvez pas rétablir son état sur **[!UICONTROL Draft]** ou **[!UICONTROL Approved]**. Vous pouvez uniquement le dupliquer, le supprimer ou l’archiver.

* **[!UICONTROL Duplicate]**: crée une décision avec les mêmes propriétés, portées de décision et offre de secours. Par défaut, la nouvelle décision a la valeur **[!UICONTROL Draft]** statut.

* **[!UICONTROL Delete]**: supprime la décision de la liste.

   >[!CAUTION]
   >
   >La décision et son contenu ne seront plus accessibles. Cette action ne peut pas être annulée.
   >
   >Si la décision est utilisée dans un autre objet, elle ne peut pas être supprimée.

* **[!UICONTROL Archive]**: définit l’état de décision sur **[!UICONTROL Archived]**. La décision est toujours disponible dans la liste, mais vous ne pouvez pas rétablir son état sur **[!UICONTROL Draft]** ou **[!UICONTROL Approved]**. Vous pouvez uniquement le dupliquer ou le supprimer.

Vous pouvez également supprimer ou modifier l’état de plusieurs décisions en même temps en cochant les cases correspondantes.

![](../assets/decision_multiple-selection.png)

Si vous souhaitez modifier l’état de plusieurs décisions dont les statuts sont différents, seuls les états pertinents seront modifiés.

![](../assets/decision_change-status.png)

Une fois une décision créée, vous pouvez cliquer sur son nom dans la liste.

![](../assets/decision_click-name.png)

Vous pouvez ainsi accéder à des informations détaillées sur cette décision. Sélectionnez la **[!UICONTROL Change log]** à [surveiller toutes les modifications ;](../get-started/user-interface.md#changes-log) qui ont été pris à la décision.

![](../assets/decision_information.png)

## Vidéo pratique{#video}

Découvrez comment créer des activités d’offre dans la gestion de la décision.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


