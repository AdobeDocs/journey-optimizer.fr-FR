---
title: Configuration de la sélection des offres dans les décisions
description: Découvrez comment gérer la sélection des offres dans les décisions.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 89%

---

# Configuration de la sélection des offres dans les décisions {#offers-selection-in-activities}

## À propos de la priorité des offres {#about-offers-priority}

Par défaut, lorsque plusieurs offres sont éligibles pour un emplacement donné dans une décision (auparavant « activité d’offre »), les offres présentant la **priorité** la plus élevée sont diffusées en premier aux clients. Les scores de priorité des offres sont attribués lors de la création d’une offre (voir [Création d’une offre personnalisée](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

De plus, Journey Optimizer vous permet de créer des **formules de classement**. Ces formules déterminent quelle offre doit être présentée en premier pour un emplacement donné au lieu de prendre en compte les scores de priorité des offres.

Par exemple, vous pouvez augmenter la priorité de toutes les offres dont la date de fin est inférieure à 24 heures, ou remonter les offres de la catégorie « en cours » si le point ciblé du profil est « en cours ».

Pour plus d&#39;informations sur la création d&#39;une formule de classement, reportez-vous à [cette section](../offer-library/create-ranking-formulas.md).

## Affectation d&#39;une formule de classement à un emplacement {#assign-ranking-formula}

Après avoir créé une formule de classement, vous pouvez l’affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

1. Créez une décision ou modifiez une décision existante, puis créez les emplacements qui contiendront vos offres (voir [Création de décisions](../offer-activities/create-offer-activities.md)).

1. Pour chaque emplacement, sélectionnez **[!UICONTROL Classement]** dans la liste déroulante.

1. Cliquez sur **[!UICONTROL Ajouter un classement]**.

   ![](../../assets/offer-activity-ranking.png)

1. Sélectionnez la formule de classement souhaitée, puis cliquez sur **[!UICONTROL Sélectionner]**.

   ![](../../assets/ranking-selection.png)

La formule de classement est désormais associée à l&#39;emplacement.

Si plusieurs offres peuvent être présentées à cet emplacement, la décision utilisera la formule de la formule de classement pour calculer la première offre à diffuser.
