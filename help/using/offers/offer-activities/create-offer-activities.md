---
title: Création de décisions
description: Découvrez comment créer des décisions
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 7f8871fdaf5bb543ce8dc894f3a7dc7304eccf36
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 100%

---

# Création de décisions {#create-offer-activities}

Les décisions (précédemment appelées activités d’offre) sont des conteneurs qui s’appuient sur le moteur de décision pour choisir la meilleure offre à diffuser en fonction de la cible de la diffusion.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

La liste des décisions est accessible dans le menu **[!UICONTROL Offres]**> onglet **[!UICONTROL Décisions]**. Des filtres sont disponibles pour vous aider à récupérer les décisions en fonction de leurs statuts ou de leurs dates de début ou de fin.

![](../../assets/activities-list.png)

Avant de créer une décision, vérifiez que les composants suivants ont été créés dans la bibliothèque des offres :

* [Emplacements](../offer-library/creating-placements.md)
* [Collections](../offer-library/creating-collections.md)
* [Offres personnalisées](../offer-library/creating-personalized-offers.md)
* [Offres de secours](../offer-library/creating-fallback-offers.md)

## Création de la décision {#create-activity}

1. Accédez à la liste des décisions, puis cliquez sur **[!UICONTROL Créer une décision]**. 

1. Indiquez le nom de la décision. 

1. Définissez une date et une heure de début et de fin si nécessaire, puis cliquez sur **[!UICONTROL Suivant]**. 

   ![](../../assets/activities-name.png)

## Définir des portées de décision {#add-decision-scopes}

1. Sélectionnez un emplacement dans la liste déroulante. Il sera ajouté à la première portée de décision de votre décision. 

   ![](../../assets/activities-placement.png)

1. Cliquez sur **[!UICONTROL Ajouter]** pour sélectionner les critères d’évaluation de cet emplacement. 

   ![](../../assets/activities-evaluation-criteria.png)

   Chaque critère consiste en une collection d’offres associée à une contrainte d’éligibilité et à une méthode de classement permettant de déterminer les offres à afficher dans l’emplacement. 

   >[!NOTE]
   >
   >Au moins un critère d’évaluation est requis. 

1. Sélectionnez la collection d’offres qui contient les offres à prendre en compte, puis cliquez sur **[!UICONTROL Ajouter]**. 

   ![](../../assets/activities-collection.png)

   >[!NOTE]
   >
   >Vous pouvez cliquer sur le lien **[!UICONTROL Ouvrir les collections d’offres]** pour afficher la liste des collections dans un nouvel onglet, qui permet de parcourir les collections et les offres qu’elles contiennent. 

   La collection sélectionnée est ajoutée au critère. 

   ![](../../assets/activities-collection-added.png)

1. Utilisez le champ **[!UICONTROL Éligibilité]** pour restreindre la sélection des offres pour cet emplacement. 

   Cette contrainte peut être appliquée en utilisant une **règle de décision** ou un ou plusieurs **segments Adobe Experience Platform**. Ceux-ci sont présentés dans [cette section](#segments-vs-decision-rules).

   * Pour limiter la sélection des offres aux membres d’un segment Experience Platform, sélectionnez **[!UICONTROL Segments]**, puis cliquez sur **[!UICONTROL Ajouter des segments]**. 

      ![](../../assets/activity_constraint_segment.png)

      Ajoutez un ou plusieurs segments depuis le volet de gauche, puis combinez-les à l’aide des opérateurs logiques **[!UICONTROL Et]**/**[!UICONTROL Ou]**. 

      ![](../../assets/activity_constraint_segment2.png)

      Découvrez comment utiliser des segments dans [cette section](../../segment/about-segments.md). 

   * Si vous souhaitez ajouter une contrainte de sélection avec une règle de décision, utilisez l’option **[!UICONTROL Règle de décision]** et sélectionnez la règle de votre choix. 

      ![](../../assets/activity_constraint_rule.png)

      Découvrez comment créer une règle de décision dans [cette section](../offer-library/creating-decision-rules.md). 

1. Définissez la méthode de classement à utiliser pour sélectionner la meilleure offre pour chaque profil. 

   ![](../../assets/activity_ranking-method.png)

   * Par défaut, si plusieurs offres sont éligibles pour cet emplacement, l’offre ayant le score de priorité le plus élevé sera diffusée au client. 

   * Si vous souhaitez utiliser une formule spécifique pour choisir l’offre éligible à diffuser, sélectionnez **[!UICONTROL Formule de classement]**. Découvrez comment classer les offres dans [cette section](../offer-activities/configure-offer-selection.md). 

1. Cliquez sur **[!UICONTROL Ajouter]** pour définir d’autres critères pour le même emplacement. 

   ![](../../assets/activity_add-collection.png)

1. Lorsque vous ajoutez plusieurs critères, ils sont évalués dans un ordre spécifique. La première collection ajoutée à la séquence sera évaluée en premier, etc. 

   Pour modifier la séquence par défaut, vous pouvez faire glisser et déposer les collections afin de les réorganiser selon vos besoins. 

   ![](../../assets/activity_reorder-collections.png)

1. Vous pouvez également évaluer plusieurs critères en même temps. Pour ce faire, glissez et déposez la collection au-dessus d’une autre. 

   ![](../../assets/activity_move-collection.png)

   Elles possèdent désormais le même rang et seront donc évaluées en même temps. 

   ![](../../assets/activity_same-rank-collections.png)

1. Pour ajouter un emplacement supplémentaire pour vos offres dans le cadre de cette décision, cliquez sur le bouton **[!UICONTROL Nouvelle portée]**. Répétez les étapes ci-dessus pour chaque portée de décision. 

   ![](../../assets/activity_new-scope.png)

### Utilisation des segments par rapport aux règles de décision {#segments-vs-decision-rules}

<!--to move to create-offers?-->

Pour appliquer une contrainte, vous pouvez restreindre la sélection des offres aux membres d’un ou de plusieurs **segments Adobe Experience Platform**, ou vous pouvez utiliser une **règle de décision**, les deux solutions correspondant à des utilisations différentes.

Pour faire simple, la sortie d’un segment est une liste de profils, tandis qu’une règle de décision est une fonction exécutée à la demande sur un seul profil pendant le processus de prise de décision. La différence entre ces deux usages est présentée ci-dessous.

* **Segments**

   D’une part, les segments sont un groupe de profils Adobe Experience Platform qui correspondent à une certaine logique basée sur les attributs de profil et les événements d’expérience. Cependant, la gestion des offres ne recalcule pas le segment, qui peut ne pas être à jour lors de la présentation de l’offre.

   En savoir plus sur les segments dans [cette section](../../segment/about-segments.md).

* **Règles de décision**

   D’un autre côté, une règle de décision est basée sur les données disponibles dans Adobe Experience Platform et détermine à qui une offre peut être montrée. Une fois sélectionnée dans une offre ou une décision pour un emplacement donné, la règle est exécutée chaque fois qu’une décision est prise, ce qui garantit que chaque profil obtient la dernière et la meilleure offre.

   Pour en savoir plus sur les règles de décision, consultez [cette section](../offer-library/creating-decision-rules.md).

## Ajouter une offre de secours {#add-fallback}

Une fois que vous avez défini les portées de décision, définissez l’offre de secours qui sera présentée en dernier recours aux clients qui ne correspondent pas aux règles d’éligibilité et contraintes des offres. 

Pour ce faire, sélectionnez-la dans la liste des offres de secours disponibles pour les emplacements définis dans la décision, puis cliquez sur **[!UICONTROL Suivant]**.

![](../../assets/add-fallback-offer.png)

>[!NOTE]
>
>Vous pouvez cliquer sur le lien **[!UICONTROL Ouvrir la bibliothèque des offres]** pour afficher la liste des offres dans un nouvel onglet. 

## Examiner et enregistrer la décision {#review}

Si tout est configuré correctement, un résumé des propriétés de la décision s&#39;affiche.

1. Assurez-vous que la décision est prête à être utilisée pour présenter des offres aux clients. Toutes les portées de décision et l’offre de secours qu’elle contient s’affichent. 

   ![](../../assets/review-decision.png)

   Vous pouvez développer ou réduire chaque emplacement. Vous pouvez également prévisualiser les offres disponibles, les détails d’éligibilité et de classement pour chaque emplacement. 

   ![](../../assets/review-decision-details.png)

1. Cliquez sur **[!UICONTROL Terminer]**.
1. Sélectionnez **[!UICONTROL Enregistrer et activer]**. 

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
>Cette vidéo s’applique au service applicatif Offer Decisioning intégré à Adobe Experience Platform. Toutefois, elle fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
