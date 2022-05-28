---
title: Configurer la sélection des offres dans les décisions
description: Découvrez comment gérer la sélection des offres dans les décisions
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: b890d7dc2e1508bb68d45a162236483ac6fc76bd
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 100%

---

# Configurer la sélection des offres dans les décisions {#offers-selection-in-decisions}

Si plusieurs offres sont éligibles pour un emplacement donné, vous pouvez choisir la méthode qui sélectionnera la meilleure offre pour chaque profil lors de la configuration d’une décision. Vous pouvez classer les offres par :
* Priorité des offres
* Formule de classement
* [Classement par l&#39;IA](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Priorité des offres {#offer-priority}

Par défaut, lorsque plusieurs offres sont éligibles pour un emplacement donné dans une décision, les offres avec la **priorité** la plus élevée sont diffusées en premier aux clients.

![](../assets/offer-priority.png)

Les scores de priorité d&#39;une offre sont attribués lors de sa création. Découvrez comment créer une offre personnalisée dans [cette section](../offer-library/creating-personalized-offers.md).

## Formule de classement {#assign-ranking-formula}

En plus de la priorité d’offre, Journey Optimizer vous permet de créer des **formules de classement**. Ces formules déterminent quelle offre doit être présentée en premier pour un emplacement donné au lieu de prendre en compte les scores de priorité des offres.

Par exemple, vous pouvez augmenter la priorité de toutes les offres dont la date de fin est inférieure à 24 heures, ou remonter les offres de la catégorie « en cours » si le point ciblé du profil est « en cours ».

Découvrez comment créer une formule de classement dans [cette section](../ranking/create-ranking-formulas.md).

Après avoir créé une formule de classement, vous pouvez l’affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

1. Créez une décision ou modifiez une décision existante. Voir la section [Créer des décisions](../offer-activities/create-offer-activities.md).

1. Ajoutez les emplacements qui contiendront vos offres. Voir [Créer des emplacements](../offer-library/creating-placements.md).

1. Pour chaque emplacement, ajoutez une collection. Voir [Créer des collections](../offer-library/creating-collections.md).

1. Sélectionnez **[!UICONTROL Formule de classement]** comme méthode de classement, puis cliquez sur **[!UICONTROL Ajouter un classement]**. 

   ![](../assets/offer-activity-ranking.png)

1. Sélectionnez la formule de classement souhaitée, puis cliquez sur **[!UICONTROL Sélectionner]**.

   ![](../assets/ranking-selection.png)

La formule de classement est désormais associée à l&#39;emplacement.

Si plusieurs offres sont éligibles à la présentation dans cet emplacement, la décision utilisera la formule de classement pour calculer l&#39;offre à diffuser en premier.

## Classement par l&#39;IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Vous pouvez également utiliser un système de modèles entraînés qui classe automatiquement les offres à afficher pour un profil donné en sélectionnant une stratégie de classement. Découvrez comment créer une stratégie de classement dans [cette section](../ranking/create-ranking-strategies.md).

Après avoir créé une stratégie de classement, vous pouvez l’affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

1. Créez une décision ou modifiez une décision existante. Voir la section [Créer des décisions](../offer-activities/create-offer-activities.md).

1. Ajoutez les emplacements qui contiendront vos offres. Voir [Créer des emplacements](../offer-library/creating-placements.md).

1. Pour chaque emplacement, ajoutez une collection. Voir [Créer des collections](../offer-library/creating-collections.md).

1. Choisissez de classer les offres par **[!UICONTROL classement AI]** dans la liste déroulante, puis cliquez sur **[!UICONTROL Ajouter un classement]**. 

   ![](../assets/ranking-selection-ai-ranking.png)

1. Sélectionnez la stratégie de classement que vous avez créée. Tous les détails de la stratégie de classement s&#39;affichent.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Cliquez sur **[!UICONTROL Sélectionner]**. La stratégie de classement est désormais associée à l&#39;emplacement.

Si plusieurs offres sont éligibles, le système de modèles formés détermine l&#39;offre qui doit être présentée en premier pour un emplacement donné.

