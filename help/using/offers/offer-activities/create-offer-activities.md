---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Créer des décisions
description: Découvrez comment créer des décisions
badge: label="Hérité" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '2566'
ht-degree: 100%

---

# Créer des décisions {#create-offer-activities}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

Les décisions sont des conteneurs pour vos offres qui s’appuient sur le moteur de décision d’offre pour choisir la meilleure offre à diffuser en fonction de la cible de la diffusion.

➡️[Découvrez comment créer des activités d’offre dans cette vidéo.](#video)

La liste des décisions est accessible dans le menu **[!UICONTROL Offres]**> onglet **[!UICONTROL Décisions]**. Des filtres sont disponibles pour vous aider à récupérer les décisions en fonction de leurs statuts ou de leurs dates de début ou de fin.

![](../assets/activities-list.png)

Avant de créer une décision, vérifiez que les composants suivants ont été créés dans la bibliothèque des offres :

* [Emplacements](../offer-library/creating-placements.md)
* [Collections](../offer-library/creating-collections.md)
* [Offres personnalisées](../offer-library/creating-personalized-offers.md)
* [Offres de secours](../offer-library/creating-fallback-offers.md)

## Création de la décision {#create-activity}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_details"
>title="Détails de la décision d’offres"
>abstract="Indiquez le nom de la décision et définissez une date et une heure de début et de fin si nécessaire. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la décision, sélectionnez **[!UICONTROL Gérer l’accès]**."

1. Accédez à la liste des décisions, puis cliquez sur **[!UICONTROL Créer une décision]**.

1. Indiquez le nom de la décision.

1. Définissez une date et une heure de début et de fin si nécessaire, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](../assets/activities-name.png)

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la décision, sélectionnez **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../../administration/object-based-access.md)

## Définir des portées de décision {#add-decision-scopes}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_scopes"
>title="Portées de décision"
>abstract="Configurez une ou plusieurs portées pour la décision d’offres afin de déterminer les offres à afficher. Pour ce faire, sélectionnez un emplacement et un critère d’évaluation associé à cet emplacement."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_placement"
>title="Emplacement"
>abstract="Sélectionnez l’emplacement où les offres seront diffusées."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_evaluation"
>title="Critères d’évaluation"
>abstract="Les critères d’évaluation consistent en une collection d’offres associée à une contrainte d’éligibilité et à une méthode de classement permettant de déterminer les offres à afficher dans l’emplacement. La séquence de critères d’évaluation détermine la collection qui sera évaluée en premier. Au moins un critère d’évaluation est requis."

1. Sélectionnez un emplacement dans la liste déroulante. Il sera ajouté à la première portée de décision de votre décision.

   ![](../assets/activities-placement.png)

1. Cliquez sur **[!UICONTROL Ajouter]** pour sélectionner les critères d’évaluation de cet emplacement.

   ![](../assets/activities-evaluation-criteria.png)

   Chaque critère consiste en une collection d’offres associée à une contrainte d’éligibilité et à une méthode de classement permettant de déterminer les offres à afficher dans l’emplacement.

   >[!NOTE]
   >
   >Au moins un critère d’évaluation est requis.

1. Sélectionnez la collection d’offres qui contient les offres à prendre en compte, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >Vous pouvez cliquer sur le lien **[!UICONTROL Ouvrir les collections d’offres]** pour afficher la liste des collections dans un nouvel onglet, qui permet de parcourir les collections et les offres qu’elles contiennent.

   La collection sélectionnée est ajoutée au critère.

   ![](../assets/activities-collection-added.png)

1. Utilisez le champ **[!UICONTROL Éligibilité]** pour restreindre la sélection des offres pour cet emplacement.

   Cette contrainte peut être appliquée en utilisant une **règle de décision** ou une ou plusieurs **audiences Adobe Experience Platform**. Celles-ci sont présentées dans [cette section](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * Pour limiter la sélection des offres aux membres d’une audience Experience Platform, sélectionnez **[!UICONTROL Audiences]**, puis cliquez sur **[!UICONTROL Ajouter des audiences]**.

     ![](../assets/activity_constraint_segment.png)

     Ajoutez une ou plusieurs audiences depuis le volet de gauche, puis combinez-les à l’aide des opérateurs logiques **[!UICONTROL Et]**/**[!UICONTROL Ou]**.

     ![](../assets/activity_constraint_segment2.png)

     Découvrez comment utiliser des audiences dans [cette section](../../audience/about-audiences.md).

   * Si vous souhaitez ajouter une contrainte de sélection avec une règle de décision, utilisez l’option **[!UICONTROL Règle de décision]** et sélectionnez la règle de votre choix.

     ![](../assets/activity_constraint_rule.png)

     Découvrez comment créer une règle de décision dans [cette section](../offer-library/creating-decision-rules.md).

1. Lorsque vous sélectionnez des audiences ou des règles de décision, vous pouvez afficher des informations sur les profils qualifiés estimés. Cliquez sur **[!UICONTROL Actualiser]** pour mettre à jour les données.

   >[!NOTE]
   >
   >Les estimations de profil ne sont pas disponibles lorsque les paramètres de règle incluent des données qui ne figurent pas dans le profil, telles que des données contextuelles. Par exemple, une règle d’éligibilité qui exige que la météo actuelle soit de ≥80 degrés.

   ![](../assets/activity_constraint-estimate.png)

1. Définissez la méthode de classement à utiliser pour sélectionner la meilleure offre pour chaque profil. [En savoir plus](../offer-activities/configure-offer-selection.md).

   ![](../assets/activity_ranking-method.png)

   * Par défaut, si plusieurs offres sont éligibles pour cet emplacement, la méthode **[!UICONTROL Priorité des offres]** utilise la valeur définie dans les offres : l’offre ayant le score de priorité le plus élevé sera présentée à l’utilisateur ou l’utilisatrice.

   * Si vous souhaitez utiliser un score calculé spécifique pour choisir l’offre éligible à présenter, sélectionnez **[!UICONTROL Formule]** ou **[!UICONTROL Modèle d’IA]**. [En savoir plus](../offer-activities/configure-offer-selection.md).

1. Cliquez sur **[!UICONTROL Ajouter]** pour définir d’autres critères pour le même emplacement.

   ![](../assets/activity_add-collection.png)

1. Lorsque vous ajoutez plusieurs critères, ils sont évalués dans un ordre spécifique. La première collection ajoutée à la séquence sera évaluée en premier, etc. [En savoir plus](#evaluation-criteria-order).

   Pour modifier la séquence par défaut, vous pouvez faire glisser et déposer les collections afin de les réorganiser selon vos besoins.

   ![](../assets/activity_reorder-collections.png)

1. Vous pouvez également évaluer plusieurs critères en même temps. Pour ce faire, glissez et déposez la collection au-dessus d’une autre.

   ![](../assets/activity_move-collection.png)

   Ils possèdent désormais le même rang et seront donc évalués en même temps. [En savoir plus](#evaluation-criteria-order).

   ![](../assets/activity_same-rank-collections.png)

   >[!CAUTION]
   >
   >* Si le [modèle d’IA](../ranking/ai-models.md) est utilisé dans un groupe de critères d’évaluation, tous les critères d’évaluation de ce groupe doivent utiliser la méthode de classement AI et le même modèle d’AI spécifique.
   >
   >* Un seul groupe de critères d’évaluation peut utiliser le modèle d’IA. Tous les autres groupes d’une portée de décision doivent utiliser d’autres méthodes de classement (priorité ou formule). [En savoir plus sur les méthodes de classement](../offer-activities/configure-offer-selection.md)

1. Pour ajouter un emplacement supplémentaire pour vos offres dans le cadre de cette décision, cliquez sur le bouton **[!UICONTROL Nouvelle portée]**. Répétez les étapes ci-dessus pour chaque portée de décision.

   ![](../assets/activity_new-scope.png)

   >[!NOTE]
   >
   >L’ajout de plusieurs portées de décision modifie l’ordre des critères d’évaluation. [En savoir plus](#multiple-scopes).

### Ordre des critères d’évaluation {#evaluation-criteria-order}

Comme décrit ci-dessus, un critère d’évaluation se compose d’une collection, de contraintes d’éligibilité et d’une méthode de classement. Vous pouvez définir l’ordre séquentiel dans lequel les critères d’évaluation s’appliquent, mais vous pouvez également combiner plusieurs critères d’évaluation afin de les appliquer ensemble et non séparément.

#### Avec une portée unique {#one-scope}

Dans une portée de décision unique, différents critères et leur regroupement déterminent la priorité des critères et le classement des offres éligibles. Le premier critère a la priorité la plus élevée et les critères combinés au sein d’un même « groupe » ont la même priorité.

Prenons l’exemple suivant : vous disposez de deux collections, l’une dans le critère d’évaluation A et l’autre dans le critère d’évaluation B. La demande concerne le renvoi de deux offres. Deux offres répondent au critère d’évaluation A et trois offres au critère d’évaluation B.

* Si les deux critères d’évaluation ne sont **pas combinés** et/ou dans l’ordre séquentiel (1 et 2), les deux meilleures offres éligibles selon les critères d’évaluation seront renvoyées dans la première ligne. S’il n’y a pas deux offres éligibles pour le premier critère d’évaluation, le moteur de décision passera au critère d’évaluation suivant dans l’ordre pour trouver autant d’offres que nécessaire, et renverra finalement une offre de secours si nécessaire.

  ![](../assets/activity_consecutive-rank-collections.png)

* Si les deux collections sont **évaluées en même temps**, puisque deux offres répondent au critère d’évaluation A et trois offres au critère d’évaluation B, les cinq offres sont regroupées et classées dans l’ordre de leurs méthodes de classement respectives. Comme deux offres sont demandées, les deux meilleures offres éligibles parmi ces cinq offres seront renvoyées.

  ![](../assets/activity_same-rank-collections.png)

+++ **Exemple avec plusieurs critères**

Prenons maintenant un exemple où plusieurs critères pour une même portée sont divisés en différents groupes.

Vous avez défini trois critères. Les critères 1 et 2 sont combinés dans le groupe 1 et le critère 3 est indépendant (groupe 2).

Les offres éligibles pour chaque critère et leur priorité (utilisée dans l’évaluation de la fonction de classement) sont les suivantes :

* Groupe 1 :
   * Critère 1 - (offre 1, offre 2 et offre 3) - Priorité 1
   * Critère 2 - (offre 3, offre 4 et offre 5) - Priorité 1

* Groupe 2 :
   * Critère 3 - (offre 5 et offre 6) - Priorité 0

Les offres répondant aux critères de priorité les plus élevés sont évaluées en premier et ajoutées à la liste des offres classées.

**Itération 1 :**

Les offres des critères 1 et 2 sont évaluées ensemble (offre 1, offre 2, offre 3, offre 4 et offre 5). Nous arrivons au résultat suivant :

Offre 1 - 10
Offre 2 - 20
Offre 3 - 30 pour le critère 1, 45 pour le critère 2. Le critère le plus élevé des deux sera pris en compte (45).
Offre 4 - 40
Offre 5 - 50

L’offre classée se présente désormais comme suit : offre 5, offre 3, offre 4, offre 2 et offre 1.

**Itération 2 :**

Les offres du critère 3 sont évaluées (offre 5 et offre 6). Nous arrivons au résultat suivant :

* Offre 5 : non évaluée, car elle existe déjà dans le résultat ci-dessus.
* Offre 6 - 60

Les offres classées sont désormais les suivantes : offre 5 , offre 3, offre 4, offre 2, offre 1 et offre 6.

+++

#### Avec plusieurs portées {#multiple-scopes}

**Si la duplication est désactivée**

Lorsque vous ajoutez plusieurs portées de décision à une décision et si la duplication n’est pas autorisée entre les emplacements, les offres éligibles sont sélectionnées de manière séquentielle dans l’ordre des portées de décision de la requête.

>[!NOTE]
>
>Le paramètre **[!UICONTROL Autoriser les doublons dans les emplacements]** est défini au niveau de l’emplacement. Si la duplication est définie sur « false » dans un emplacement d’une requête de prise de décision, tous les emplacements de la requête hériteront du paramètre « false ». [En savoir plus sur le paramètre de duplication](../offer-library/creating-placements.md)

Prenons un exemple où vous avez ajouté deux portées de décision, telles que :

* Portée 1 : il existe quatre offres éligibles (offre 1, offre 2, offre 3 et offre 4) et la requête porte sur le renvoi de deux offres.
* Portée 2 : il existe quatre offres éligibles (offre 1, offre 2, offre 3 et offre 4) et la requête porte sur le renvoi de deux offres.

+++ **Exemple 1**

La sélection se présente comme suit :

1. Les deux meilleures offres éligibles de la portée 1 sont renvoyées (offre 1 et offre 2).
1. Les deux autres meilleures offres éligibles de la portée 2 sont renvoyées (offre 3 et offre 4).

+++

+++ **Exemple 2**

Dans cet exemple, l’offre1 a atteint sa limite de fréquence maximale. [En savoir plus sur le capping de la fréquence](../offer-library/add-constraints.md#capping)

La sélection se présente comme suit :

1. Les deux autres meilleures offres éligibles de la portée 1 sont renvoyées (offre 2 et offre 3).
1. L’offre éligible restante de la portée 2 est renvoyée (offre 4).

+++

+++ **Exemple 3**

Dans cet exemple, les offres 1 et 3 ont atteint leur limite de fréquence maximale. [En savoir plus sur le capping de la fréquence](../offer-library/add-constraints.md#capping)

La sélection se présente comme suit :

1. Les deux autres meilleures offres éligibles de la portée 1 sont renvoyées (offre 2 et offre 4).
1. Il n’existe aucune autre offre éligible pour la portée 2. Par conséquent, l’[offre de secours](#add-fallback) est renvoyée.

+++

**Si la duplication est activée**

Lorsque la duplication est autorisée entre tous les emplacements, la même offre peut être proposée plusieurs fois à différents emplacements. Si cette option est activée, le système accepte de placer la même offre dans plusieurs emplacements. [En savoir plus sur le paramètre de duplication](../offer-library/creating-placements.md)

Prenons le même exemple que ci-dessus, dans lequel vous avez ajouté deux portées de décision, telles que :

* Portée 1 : il existe quatre offres éligibles (offre 1, offre 2, offre 3 et offre 4) et la requête porte sur le renvoi de deux offres.
* Portée 2 : il existe quatre offres éligibles (offre 1, offre 2, offre 3 et offre 4) et la requête porte sur le renvoi de deux offres.

+++ **Exemple 1**

La sélection se présente comme suit :

1. Les deux meilleures offres éligibles de la portée 1 sont renvoyées (offre 1 et offre 2).
1. Les deux mêmes meilleures offres éligibles de la portée 2 sont renvoyées (offre 1 et offre 2).

+++

+++ **Exemple 2**

Dans cet exemple, l’offre1 a atteint sa limite de fréquence maximale. [En savoir plus sur le capping de la fréquence](../offer-library/add-constraints.md#capping)

La sélection se présente comme suit :

1. Les deux autres meilleures offres éligibles de la portée 1 sont renvoyées (offre 2 et offre 3).

1. De même, les deux autres meilleures offres éligibles de la portée 2 sont renvoyées (offre 2 et offre 3).

+++

+++ **Exemple 3**

Dans cet exemple, les offres 1 et 3 ont atteint leur limite de fréquence maximale. [En savoir plus sur le capping de la fréquence](../offer-library/add-constraints.md#capping)

La sélection se présente comme suit :

1. Les deux autres meilleures offres éligibles de la portée 1 sont renvoyées (offre 2 et offre 4).

1. De même, les deux autres meilleures offres éligibles de la portée 2 sont renvoyées (offre 2 et offre 4).

+++

## Ajouter une offre de secours {#add-fallback}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_fallback"
>title="Ajouter une offre de secours"
>abstract="Une fois que vous avez défini les portées de décision, définissez l’offre de secours qui sera présentée en dernier recours aux clients qui ne correspondent pas aux règles d’éligibilité et contraintes des offres."

Une fois que vous avez défini les portées de décision, définissez l’[offre de secours](../offer-library/creating-fallback-offers.md) qui sera présentée en dernier recours aux clientes et clients qui ne répondent pas aux règles d’éligibilité et contraintes des offres.

Pour ce faire, sélectionnez-la dans la liste des offres de secours disponibles pour les emplacements définis dans la décision.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>Les offres de secours doivent contenir toutes les représentations utilisées dans une décision. Par exemple, si une décision comporte 5 offres et que chacune d’elles a une représentation différente, 5 représentations doivent être incluses dans l’offre de secours.

Une fois la sélection effectuée, cliquez sur **[!UICONTROL Suivant]**.

Vous pouvez cliquer sur le lien **[!UICONTROL Ouvrir la bibliothèque des offres]** pour afficher la liste des offres dans un nouvel onglet.

## Examiner et enregistrer la décision {#review}

Si tout est configuré correctement, un résumé des propriétés de la décision s&#39;affiche.

1. Assurez-vous que la décision est prête à être utilisée pour présenter des offres aux clients. Toutes les portées de décision et l’offre de secours qu’elle contient s’affichent.

   ![](../assets/review-decision.png)

1. Vous pouvez développer ou réduire chaque emplacement. Vous pouvez prévisualiser les offres disponibles, les détails d’éligibilité et de classement pour chaque emplacement. Vous pouvez également afficher des informations sur les profils qualifiés estimés. Cliquez sur **[!UICONTROL Actualiser]** pour mettre à jour les données.

   ![](../assets/review-decision-details.png)

1. Cliquez sur **[!UICONTROL Terminer]**.
1. Sélectionnez **[!UICONTROL Enregistrer et activer]**.

   ![](../assets/save-activities.png)

   Vous pouvez également enregistrer la décision en tant que brouillon afin de la modifier et de l&#39;activer ultérieurement.

La décision s&#39;affiche dans la liste avec l&#39;état **[!UICONTROL Actif]** ou **[!UICONTROL Brouillon]**, selon que vous l&#39;avez activée ou non à l&#39;étape précédente.

Elle est maintenant prête à être utilisée pour diffuser des offres vers les clients.

## Liste des décisions {#decision-list}

Dans la liste des décisions, vous pouvez sélectionner la décision afin d&#39;afficher ses propriétés. Depuis cet emplacement, vous pouvez également la modifier, modifier son statut (**Brouillon**, **Actif**, **Terminé**, **Archivé**), la dupliquer ou la supprimer.

![](../assets/decision_created.png)

Sélectionnez le bouton **[!UICONTROL Modifier]** pour revenir au mode d&#39;édition de la décision, où vous pouvez modifier ses [détails](#create-activity), les [portées de décision](#add-decision-scopes) et l&#39;[offre de secours](#add-fallback).

>[!IMPORTANT]
>
>Si des modifications sont apportées à une décision d’offres qui est utilisée dans le message d’un parcours, vous devez dépublier le parcours et le republier. Cela permet de s’assurer que les modifications sont intégrées au message du parcours et que le message est cohérent avec les dernières mises à jour.

Sélectionnez une décision active et cliquez sur **[!UICONTROL Désactiver]** pour redéfinir le statut de la décision sur **[!UICONTROL Brouillon]**.

Pour définir à nouveau le statut sur **[!UICONTROL Actif]**, cliquez sur le bouton **[!UICONTROL Activer]** qui s&#39;affiche désormais.

![](../assets/decision_activate.png)

Le bouton **[!UICONTROL Autres actions]** active les actions décrites ci-dessous.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Terminé]** : définit le statut de la décision sur **[!UICONTROL Terminé]**, ce qui signifie que la décision ne peut plus être appelée. Cette action n&#39;est disponible que pour les décisions activées. La décision est toujours disponible dans la liste, mais vous ne pouvez pas redéfinir son statut sur **[!UICONTROL Brouillon]** ou **[!UICONTROL Approuvé]**. Vous pouvez uniquement la dupliquer, la supprimer ou l&#39;archiver.

* **[!UICONTROL Dupliquer]** : crée une décision avec les mêmes propriétés, portées de décision et offre de secours. Par défaut, la nouvelle décision a le statut **[!UICONTROL Brouillon]**.

* **[!UICONTROL Supprimer]** : supprime la décision de la liste.

  >[!CAUTION]
  >
  >La décision et son contenu ne seront plus accessibles. Cette action ne peut pas être annulée.
  >
  >Si la décision est utilisée dans un autre objet, elle ne peut pas être supprimée.

* **[!UICONTROL Archiver]** : définit le statut de la décision sur **[!UICONTROL Archivé]**. La décision est toujours disponible dans la liste, mais vous ne pouvez pas redéfinir son statut sur **[!UICONTROL Brouillon]** ou **[!UICONTROL Approuvé]**. Vous pouvez uniquement la dupliquer ou la supprimer.

Vous pouvez également supprimer ou modifier le statut de plusieurs décisions en même temps en cochant les cases correspondantes.

![](../assets/decision_multiple-selection.png)

Si vous souhaitez modifier le statut de plusieurs décisions dont les statuts sont différents, seuls les statuts correspondants seront modifiés.

![](../assets/decision_change-status.png)

Une fois une décision créée, vous pouvez cliquer sur son nom dans la liste.

![](../assets/decision_click-name.png)

Vous pouvez ainsi accéder à des informations détaillées sur cette décision. Sélectionnez l&#39;onglet **[!UICONTROL Log des modifications]** pour [surveiller toutes les modifications](../get-started/user-interface.md#changes-logs) qui ont été apportées à la décision.

![](../assets/decision_information.png)

## Vidéo pratique{#video}

Découvrez comment créer des activités d’offre dans la gestion de décisions.

>[!VIDEO](https://video.tv.adobe.com/v/346693?captions=fre_fr&quality=12)


