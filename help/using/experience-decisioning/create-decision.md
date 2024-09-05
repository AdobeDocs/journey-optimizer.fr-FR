---
title: Créer des politiques de décisions
description: Découvrir comment créer des politiques de décisions
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilité limitée"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 100%

---

# Créer des politiques de décision {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Qu’est-ce qu’une décision ?"
>abstract="Les politiques de décision contiennent toute la logique de sélection afin que le moteur de prise de décision choisisse le meilleur contenu. Les politiques de décision sont spécifiques aux campagnes. Leur objectif est de sélectionner les meilleures offres pour chaque profil, tandis que la création de campagne vous permet d’indiquer comment les éléments de décision sélectionnés doivent être présentés, y compris les attributs d’élément à inclure dans le message."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="À propos de la prise de décision basée sur l’expérience"

Les politiques de décision sont des conteneurs pour vos offres qui utilisent le moteur de prise de décision basée sur l’expérience afin de choisir le meilleur contenu à diffuser, en fonction de l’audience.

Les politiques de décision contiennent toute la logique de sélection afin que le moteur de prise de décision choisisse le meilleur contenu. Les politiques de décision sont spécifiques aux campagnes. Leur objectif est de sélectionner les meilleures offres pour chaque profil, tandis que la création de campagne vous permet d’indiquer comment les éléments de décision sélectionnés doivent être présentés, y compris les attributs d’élément à inclure dans le message.

>[!NOTE]
>
>Dans l’interface utilisateur [!DNL Journey Optimizer], les politiques de décision sont étiquetées comme étant des décisions<!--but they are decision policies. TBC if this note is needed-->.

## Ajouter une politique de décision à une campagne basée sur du code {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Définir le nombre d’éléments à renvoyer"
>abstract="Sélectionnez le nombre d’éléments de décision à renvoyer. Par exemple, si vous sélectionnez 2, les 2 meilleures offres éligibles seront présentées pour la configuration actuelle."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Sélectionner une offre de secours"
>abstract="Un élément d’offre de secours s’affiche pour l’utilisateur ou l’utilisatrice lorsqu’aucune des stratégies de sélection définies pour cette politique de décision n’est qualifiée."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Qu’est-ce qu’une stratégie ?"
>abstract="La séquence de stratégies de sélection détermine la stratégie qui sera évaluée en premier. Au moins une stratégie est requise. Les éléments de décision des stratégies combinées seront évalués ensemble."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Créer des stratégies"
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Ordre d’évaluation"

Pour présenter la meilleure offre et expérience dynamique aux visiteurs et visiteuses de votre site Web ou de votre application mobile, ajoutez une politique de décision à une campagne basée sur du code. Pour ce faire, procédez comme suit.

1. Créez une campagne et sélectionnez l’action **[!UICONTROL Expérience basée sur le code]**. [En savoir plus](../code-based/create-code-based.md)

1. Dans l’[éditeur de code](../code-based/create-code-based.md#edit-code), sélectionnez l’icône **[!UICONTROL Politique de décision]**, et cliquez sur **[!UICONTROL Ajouter une politique de décision]**.

   ![](assets/decision-code-based-create.png)

1. Renseignez les détails de votre politique de décision : ajoutez un nom et sélectionnez un catalogue.

   >[!NOTE]
   >
   >Actuellement, seul le catalogue par défaut **[!UICONTROL Offres]** est disponible.

   ![](assets/decision-code-based-details.png)

1. Sélectionnez le nombre d’éléments à renvoyer. Par exemple, si vous sélectionnez 2, les 2 meilleures offres éligibles seront présentées pour la configuration actuelle. Cliquez sur **[!UICONTROL Suivant]**.

1. Utilisez le bouton **[!UICONTROL Ajouter une stratégie]** pour définir les stratégies de sélection de votre politique de décision. Chaque stratégie consiste en une collection d’offres associée à une contrainte d’éligibilité et à une méthode de classement permettant de déterminer les offres à afficher. [En savoir plus](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >Au moins une stratégie est requise. Vous ne pouvez pas ajouter plus de 10 stratégies.

1. Dans l’écran **[!UICONTROL Ajouter une stratégie]**, vous pouvez également créer une stratégie. Le bouton **[!UICONTROL Créer une stratégie de sélection]** vous redirige vers le menu **[!UICONTROL Prise de décision basée sur l’expérience]** > **[!UICONTROL Configuration de la stratégie]**. [En savoir plus](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. Lorsque vous ajoutez plusieurs stratégies, elles sont évaluées dans un ordre spécifique. La première stratégie ajoutée à la séquence sera évaluée en premier, etc. [En savoir plus](#evaluation-order)

   Pour modifier la séquence par défaut, vous pouvez faire glisser et déposer les stratégies et/ou les groupes afin de les réorganiser selon vos besoins.

   ![](assets/decision-code-based-strategy-groups.png)

1. Ajoutez une offre secours. Un élément d’offre de secours s’affiche pour l’utilisateur ou l’utilisatrice si aucune des stratégies de sélection ci-dessus n’est qualifiée.

   ![](assets/decision-code-based-strategy-fallback.png)

   Vous pouvez sélectionner n’importe quel élément de la liste, qui affiche tous les éléments de décision créés dans le sandbox actuel. Si aucune stratégie de sélection n’est qualifiée, l’offre de secours est affichée pour l’utilisateur ou utilisatrice, quelles que soient les dates et les contraintes d’éligibilité appliquées à l’élément sélectionné.<!--nor frequency capping when available - TO CLARIFY-->.

   >[!NOTE]
   >
   >Une offre de secours est facultative. Si aucune offre de secours n’est sélectionnée et qu’aucune stratégie n’est qualifiée, rien ne sera affiché par [!DNL Journey Optimizer].

1. Enregistrez votre sélection et cliquez sur **[!UICONTROL Créer]**. Maintenant que la politique de décision est créée, vous pouvez utiliser les attributs de décision dans votre contenu d’expérience basée sur le code. [En savoir plus](#use-decision-policy)

   ![](assets/decision-code-based-decision-added.png)

## Ordre d’évaluation {#evaluation-order}

Comme décrit ci-dessus, une stratégie se compose d’une collection, d’une méthode de classement et de contraintes d’éligibilité.

Vous pouvez :

* définir l’ordre séquentiel souhaité pour l’évaluation des stratégies ;
* combiner plusieurs stratégies afin qu’elles soient évaluées ensemble et non séparément.

Plusieurs stratégies et leur regroupement déterminent la priorité des stratégies et le classement des offres éligibles. La première stratégie a la priorité la plus élevée et les stratégies combinées au sein d’un même groupe ont la même priorité.

Prenons l’exemple suivant : vous disposez de deux collections, l’une dans la stratégie A et l’autre dans la stratégie B. La demande concerne le renvoi de deux éléments de décision. Supposons qu&#39;il y ait deux offres éligibles pour la stratégie A et trois offres éligibles pour la stratégie B.

* Si les deux stratégies ne sont **pas combinées** ni dans l’ordre séquentiel (1 et 2), les deux meilleures offres éligibles de la première stratégie seront renvoyées dans la première ligne. S’il n’y a pas deux offres éligibles pour la première stratégie, le moteur de décision passera à la stratégie suivante dans la séquence pour trouver autant d’offres que nécessaire, et renverra finalement une offre de secours si nécessaire.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Si les deux collections sont **évaluées en même temps**, étant donné qu’il y a deux offres éligibles pour la stratégie A et trois offres éligibles pour la stratégie B, les cinq offres seront regroupées et classées selon la valeur déterminée par leurs méthodes de classement respectives. Comme deux offres sont demandées, les deux meilleures offres éligibles parmi ces cinq offres seront renvoyées.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **Exemple avec plusieurs stratégies**

Prenons un exemple où plusieurs stratégies sont divisées en différents groupes.

Vous avez défini trois stratégies. Les stratégies 1 et 2 sont combinées dans le groupe 1 et la stratégie 3 est indépendante (groupe 2).

Les offres éligibles pour chaque stratégie et leur priorité (utilisée dans l’évaluation de la fonction de classement) sont les suivantes :

* Groupe 1 :
   * Stratégie 1 - (offre 1, offre 2 et offre 3) - Priorité 1
   * Stratégie 2 - (offre 3, offre 4 et offre 5) - Priorité 1

* Groupe 2 :
   * Stratégie 3 - (offre 5 et offre 6) - Priorité 0

Les offres de stratégie ayant la priorité la plus élevée sont évaluées en premier et ajoutées à la liste des offres classées.

**Itération 1 :**

Les offres des stratégies 1 et 2 sont évaluées ensemble (offre 1, offre 2, offre 3, offre 4 et offre 5). Nous arrivons au résultat suivant :

Offre 1 - 10
Offre 2 - 20
Offre 3 - 30 pour la stratégie 1, 45 pour la stratégie 2. Le critère le plus élevé des deux sera pris en compte (45).
Offre 4 - 40
Offre 5 - 50

Les offres classées se présentent désormais comme suit : offre 5, offre 3, offre 4, offre 2 et offre 1.

**Itération 2 :**

Les offres de la stratégie 3 sont évaluées (offre 5 et offre 6). Nous arrivons au résultat suivant :

* Offre 5 : non évaluée, car elle existe déjà dans le résultat ci-dessus.
* Offre 6 - 60

Les offres classées sont désormais les suivantes : offre 5 , offre 3, offre 4, offre 2, offre 1 et offre 6.

+++

## Utiliser la politique de décision dans l’éditeur de code {#use-decision-policy}

Une fois créée, la politique de décision peut être utilisée dans l’[éditeur de personnalisation](../code-based/create-code-based.md#edit-code). Pour ce faire, procédez comme suit.

>[!NOTE]
>
>L’expérience basée sur le code tire parti de l’éditeur de personnalisation de [!DNL Journey Optimizer] et de toutes ses fonctionnalités de personnalisation et de création. [En savoir plus](../personalization/personalization-build-expressions.md)

1. Cliquez sur le bouton **[!UICONTROL Insérer une politique]**. Le code correspondant à la politique de décision est ajouté.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Cette séquence sera répétée selon le nombre de renvoi de la politique de décision que vous choisissez. Par exemple, si vous avez choisi de renvoyer 2 éléments lors de la [création de la décision](#add-decision), la même séquence sera répétée deux fois.

1. Vous pouvez désormais ajouter tous les attributs de décision que vous souhaitez dans ce code. Les attributs disponibles sont stockés dans le schéma du catalogue **[!UICONTROL Offres]**. Les attributs personnalisés sont stockés dans le dossier **`_<imsOrg`>**, et les attributs standard dans le dossier **`_experience`**. [En savoir plus sur le schéma du catalogue Offres](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >Pour le suivi des éléments de la politique de décision, l’attribut `trackingToken` doit être ajouté comme suit pour le contenu de la politique de décision :
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Cliquez sur chaque dossier pour le développer. Placez le curseur de votre souris à l’emplacement souhaité, puis cliquez sur l’icône + en regard de l’attribut à ajouter. Vous pouvez ajouter au code autant d’attributs que vous le souhaitez.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Vous pouvez également ajouter tout autre attribut disponible dans l’éditeur de personnalisation, tel que des attributs de profil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

## Rapports dans Customer Journey Analytics {#cja}

Si vous utilisez Customer Journey Analytics, vous pouvez créer des tableaux de bord de rapports personnalisés pour vos campagnes basées sur du code en tirant parti d’Experience Decisioning

Suivez les étapes principales ci-dessous : Vous trouverez des informations détaillées sur l’utilisation de Customer Journey Analytics dans la [documentation de Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Créez et configurez une **connexion** dans Customer Journey Analytics. Vous pouvez ainsi vous connecter au jeu de données pour lequel vous souhaitez établir des rapports. [Découvrir comment créer une connexion](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Créez une **vue des données** et associez-la à la connexion créée précédemment. Sous l’onglet **[!UICONTROL Composants]**, sélectionnez les champs de schéma appropriés que vous souhaitez afficher dans les rapports. Pour Experience Decisioning, veillez à inclure les champs **propositioninteract** et **propositiondisplay**. [Découvrir comment créer et configurer des vues de données](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combinez des composants de données, des tableaux et des visualisations dans des **projets Workspace** pour créer et partager des rapports pour votre campagne basée sur du code.[Découvrir comment créer des projets Workspace](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
