---
title: Configurer la sélection des offres dans les décisions
description: Découvrez comment gérer la sélection des offres dans les décisions.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 52%

---

# Configurer la sélection des offres dans les décisions {#offers-selection-in-activities}

## À propos de la priorité des offres {#about-offers-priority}

Par défaut, lorsque plusieurs offres sont éligibles pour un placement donné dans une décision (précédemment connue sous le nom d&#39;activité d&#39;offre), les offres ayant la priorité la plus élevée **** sont livrées en premier aux clients. Les scores de priorité des offres sont attribués lors de la création d’une offre (voir [Création d’une offre personnalisée](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

De plus, Journey Optimizer vous permet de créer des **formules de classement**. Ces formules déterminent quelle offre doit être présentée en premier pour un placement donné au lieu de prendre en compte les scores de priorité des offres. Par exemple, vous pouvez augmenter la priorité de toutes les offres dont la date de fin est inférieure à 24 heures, ou remonter les offres de la catégorie « en cours » si le point ciblé du profil est « en cours ».

Pour plus d’informations sur la création d’une formule de classement, reportez-vous à [cette section](../offer-library/create-ranking-formulas.md).

## Affectation d’une formule de classement à un placement {#assign-ranking-formula}

Une fois qu&#39;une formule de classement a été créée, vous pouvez l&#39;affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

* Créez une décision ou modifiez une décision existante, puis créez les emplacements qui contiendront vos offres (voir [Créer des décisions](../offer-activities/create-offer-activities.md)).

* Pour chaque placement, sélectionnez **[!UICONTROL Classement]** dans la liste déroulante, puis cliquez sur **[!UICONTROL Ajouter un classement]**.

   ![](../../assets/offer-activity-ranking.png)

* Sélectionnez la formule de classement souhaitée, puis cliquez sur **[!UICONTROL Sélectionner]**.

   ![](../../assets/ranking-selection.png)

La formule de classement est désormais associée au placement. Si plusieurs offres sont admissibles à ce placement, la décision utilisera la formule de classement pour calculer l&#39;offre à livrer en premier.
