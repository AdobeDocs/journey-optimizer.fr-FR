---
title: Configurer la sélection des offres dans les décisions
description: Découvrez comment gérer la sélection des offres dans les décisions.
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: ht
source-wordcount: '255'
ht-degree: 100%

---

# Configurer la sélection des offres dans les décisions {#offers-selection-in-activities}

## À propos de la priorité des offres {#about-offers-priority}

Par défaut, lorsque plusieurs offres sont éligibles pour un emplacement donné dans une décision (auparavant « activité d’offre »), les offres présentant la **priorité** la plus élevée sont diffusées en premier aux clients. Les scores de priorité des offres sont attribués lors de la création d’une offre (voir [Création d’une offre personnalisée](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

De plus, Journey Optimizer vous permet de créer des **formules de classement**. Ces formules déterminent quelle offre doit être présentée en premier pour un placement donné au lieu de prendre en compte les scores de priorité des offres. Par exemple, vous pouvez augmenter la priorité de toutes les offres dont la date de fin est inférieure à 24 heures, ou remonter les offres de la catégorie « en cours » si le point ciblé du profil est « en cours ».

Pour plus d’informations sur la création d’une formule de classement, reportez-vous à [cette section](../offer-library/create-ranking-formulas.md).

## Affectation d’une formule de classement à un placement {#assign-ranking-formula}

Après avoir créé une formule de classement, vous pouvez l’affecter à un emplacement dans une décision. Pour ce faire, procédez comme suit :

* Créez une décision ou modifiez-en une, puis créez les emplacements qui contiendront vos offres (voir [Création de décisions](../offer-activities/create-offer-activities.md)).

* Pour chaque placement, sélectionnez **[!UICONTROL Classement]** dans la liste déroulante, puis cliquez sur **[!UICONTROL Ajouter un classement]**.

   ![](../../assets/offer-activity-ranking.png)

* Sélectionnez la formule de classement souhaitée, puis cliquez sur **[!UICONTROL Sélectionner]**.

   ![](../../assets/ranking-selection.png)

La formule de classement est désormais associée au placement. Si plusieurs offres sont éligibles à la présentation dans cet emplacement, la décision utilise la formule de classement pour calculer l’offre à diffuser en premier.
