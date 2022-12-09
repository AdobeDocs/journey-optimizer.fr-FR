---
title: Configuration de la sélection des offres dans les décisions
description: Découvrez comment gérer la sélection des offres dans les décisions
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: b890d7dc2e1508bb68d45a162236483ac6fc76bd
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---

# Configuration de la sélection des offres dans les décisions {#offers-selection-in-decisions}

Si plusieurs offres sont éligibles pour un emplacement donné, vous pouvez choisir la méthode qui sélectionnera la meilleure offre pour chaque profil lors de la configuration d&#39;une décision. Vous pouvez classer les offres par :
* Priorité des offres
* Formule de classement
* [Classement AI](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Priorité des offres {#offer-priority}

Par défaut, lorsque plusieurs offres sont éligibles pour un emplacement donné dans une décision, les offres présentant le niveau le plus élevé **priority** sera d’abord livré aux clients.

![](../assets/offer-priority.png)

Les scores de priorité des offres sont attribués lors de la création d’une offre. Découvrez comment créer une offre personnalisée dans [cette section](../offer-library/creating-personalized-offers.md).

## Formule de classement {#assign-ranking-formula}

Outre la priorité des offres, Journey Optimizer vous permet de créer des **formules de classement**. Il s’agit de formules qui déterminent quelle offre doit être présentée en premier pour un emplacement donné, plutôt que de prendre en compte les scores de priorité des offres.

Par exemple, vous pouvez augmenter la priorité de toutes les offres dont la date de fin est inférieure à 24 heures, ou augmenter les offres de la catégorie &quot;en cours&quot; si le point ciblé du profil est &quot;en cours&quot;.

Découvrez comment créer une formule de classement dans [cette section](../ranking/create-ranking-formulas.md).

Une fois qu’une formule de classement a été créée, vous pouvez l’affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

1. Créez une décision ou modifiez une décision existante. Voir [Créer des décisions](../offer-activities/create-offer-activities.md).

1. Ajoutez les emplacements qui contiendront vos offres. Voir [Créer des emplacements](../offer-library/creating-placements.md).

1. Pour chaque emplacement, ajoutez une collection. Voir [Création de collections](../offer-library/creating-collections.md).

1. Sélectionner **[!UICONTROL Ranking formula]** comme méthode de classement, puis cliquez sur **[!UICONTROL Add ranking]**.

   ![](../assets/offer-activity-ranking.png)

1. Sélectionnez la formule de classement souhaitée, puis cliquez sur **[!UICONTROL Select]**.

   ![](../assets/ranking-selection.png)

La formule de classement est désormais associée à l’emplacement.

Si plusieurs offres peuvent être présentées à cet emplacement, la décision utilisera la formule de la formule de classement pour calculer la première offre à diffuser.

## Classement AI {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Vous pouvez également utiliser un système de modèles formé qui classe automatiquement les offres à afficher pour un profil donné en sélectionnant une stratégie de classement. Découvrez comment créer une stratégie de classement dans [cette section](../ranking/create-ranking-strategies.md).

Une fois une stratégie de classement créée, vous pouvez l’affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

1. Créez une décision ou modifiez une décision existante. Voir [Créer des décisions](../offer-activities/create-offer-activities.md).

1. Ajoutez les emplacements qui contiendront vos offres. Voir [Créer des emplacements](../offer-library/creating-placements.md).

1. Pour chaque emplacement, ajoutez une collection. Voir [Création de collections](../offer-library/creating-collections.md).

1. Choisir de classer les offres par **[!UICONTROL AI ranking]** dans la liste déroulante, puis cliquez sur **[!UICONTROL Add ranking]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Sélectionnez la stratégie de classement que vous avez créée. Tous les détails de la stratégie de classement s’affichent.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Cliquez sur **[!UICONTROL Select]**. La stratégie de classement est désormais associée à l’emplacement.

Si plusieurs offres sont éligibles, le système de modèle formé détermine l’offre qui doit être présentée en premier pour un emplacement donné.

