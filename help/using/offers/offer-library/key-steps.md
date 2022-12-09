---
title: Étapes clés de création d’une offre
description: Découvrez les étapes clés nécessaires à la création d’une offre
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Étapes clés de création et de gestion des offres {#key-steps-to-manage-offers}

Les principales étapes de création, de configuration et de gestion des offres, ainsi que de leur utilisation dans une décision, sont présentées ci-dessous.

![](../assets/offer-create-manage-process.png)

Pour un exemple complet de bout en bout montrant comment configurer des offres, utilisez-les dans une décision et exploitez cette décision dans un email, extrayez-les. [cette page](../offers-e2e.md).

## Création de composants {#create-components}

Avant de commencer à créer des offres, vous devez définir plusieurs composants que vous utiliserez dans vos offres.

1. **Créer des emplacements**, qui sont des conteneurs qui seront utilisés pour présenter vos offres. Vous pouvez, par exemple, créer un emplacement qui sera dédié aux offres au format d’image uniquement et situé en haut de vos messages.

1. **Créer des règles de décision** qui spécifient les conditions dans lesquelles les offres seront présentées.

1. **Créer des balises** que vous associerez aux offres, ce qui vous permet de les organiser et de les rechercher facilement dans la bibliothèque.

1. Si vous souhaitez définir des règles qui déterminent la première offre à présenter pour un emplacement donné (plutôt que de prendre en compte les scores de priorité des offres), vous pouvez **créer une formule de classement**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Créer des emplacements</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Créer des règles de décision</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Créer des balises</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">Création de formules de classement</a></p></td>
</table>

## Créer et gérer des offres {#create-and-manage-offers}

1. **Créer des offres** et configurez leur contenu et leurs propriétés.

1. **Créer des offres de secours**, qui sont les dernières offres de recours à afficher si les clients ne sont éligibles à aucune des offres sélectionnées.

1. **Création d’une collection** pour inclure les offres personnalisées que vous avez créées et les utiliser dans une décision.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Créer des offres</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Créer des offres de secours</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Création de collections</a></p></td></tr>
</table>

## Créer et configurer des décisions {#create-and-configure-decisions}

1. **Créer une décision** qui combinera des emplacements avec les offres personnalisées et les offres de secours. Cette combinaison sera utilisée par le moteur de prise de décision pour trouver la meilleure offre pour un profil spécifique.

1. **Configurer la décision**. Pour ce faire, sélectionnez les emplacements, puis, pour chaque emplacement, sélectionnez une collection et un secours.

1. Si nécessaire, vous pouvez **attribuer une formule de classement** à un emplacement lors de la configuration de la décision.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Créer des décisions</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Configuration des décisions</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Attribuer un classement</a></p></td>
</tr>
</table>
