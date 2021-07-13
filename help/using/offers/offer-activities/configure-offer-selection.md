---
title: Configuration de la sélection des offres dans les décisions
description: Découvrez comment gérer la sélection des offres dans les décisions.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: 807157d4d6fc1dba018bbe796c8bd213504589dc
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 51%

---

# Configuration de la sélection des offres dans les décisions {#offers-selection-in-activities}

Si plusieurs offres sont éligibles pour un emplacement donné, vous pouvez choisir la méthode qui sélectionnera la meilleure offre pour chaque profil lors de la configuration d’une décision (précédemment appelée activité d’offre). Vous pouvez classer les offres par :
* Priorité des offres
* Formule de classement

## Priorité des offres {#about-offers-priority}

Par défaut, lorsque plusieurs offres sont éligibles pour un emplacement donné dans une décision (auparavant « activité d’offre »), les offres présentant la **priorité** la plus élevée sont diffusées en premier aux clients.

![](../../assets/offer-priority.png)

Les scores de priorité des offres sont attribués lors de la création d’une offre. Découvrez comment créer une offre personnalisée dans [cette section](../offer-library/creating-personalized-offers.md)).

## Formule de classement {#assign-ranking-formula}

En plus de la priorité des offres, Journey Optimizer vous permet de créer des **formules de classement**. Ces formules déterminent quelle offre doit être présentée en premier pour un emplacement donné au lieu de prendre en compte les scores de priorité des offres.

Par exemple, vous pouvez augmenter la priorité de toutes les offres dont la date de fin est inférieure à 24 heures, ou remonter les offres de la catégorie « en cours » si le point ciblé du profil est « en cours ».

Découvrez comment créer une formule de classement dans [cette section](../offer-library/create-ranking-formulas.md).

Après avoir créé une formule de classement, vous pouvez l&#39;affecter à un emplacement dans une décision (auparavant appelée activité d&#39;offre). Pour ce faire, procédez comme suit :

1. Créez une décision ou modifiez une décision existante. Voir [Créer des décisions](../offer-activities/create-offer-activities.md).

1. Ajoutez les emplacements qui contiendront vos offres. Voir [Créer des emplacements](../offer-library/creating-placements.md).

1. Pour chaque emplacement, ajoutez une collection. Voir [Créer des collections](../offer-library/creating-collections.md).

1. Choisissez de classer les offres par **[!UICONTROL Classement]** dans la liste déroulante, puis cliquez sur **[!UICONTROL Ajouter un classement]**.

   ![](../../assets/offer-activity-ranking.png)

1. Sélectionnez la formule de classement souhaitée, puis cliquez sur **[!UICONTROL Sélectionner]**.

   ![](../../assets/ranking-selection.png)

La formule de classement est désormais associée à l&#39;emplacement.

Si plusieurs offres peuvent être présentées à cet emplacement, la décision utilisera la formule de la formule de classement pour calculer la première offre à diffuser.
