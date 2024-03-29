---
title: Étapes clés de la création d’une offre
description: Découvrez les étapes clés nécessaires à la création dʼune offre.
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 100%

---

# Étapes clés de création et de gestion des offres {#key-steps-to-manage-offers}

Les principales étapes de création, de configuration et de gestion des offres, ainsi que de leur utilisation dans une décision, sont présentées ci-dessous.

![](../assets/offer-create-manage-process.png)

Pour obtenir un exemple complet montrant comment configurer des offres, les utiliser dans une décision et exploiter cette décision dans un e-mail, consultez [cette page](../offers-e2e.md).

## Création de composants {#create-components}

Avant de commencer à créer des offres, vous devez définir plusieurs composants que vous utiliserez dans vos offres.

1. **Créez des emplacements** qui sont des conteneurs utilisés pour présenter vos offres. Vous pouvez, par exemple, créer un emplacement réservé aux offres au format d&#39;image uniquement, et situé en haut de vos messages.

1. **Créez des règles de décision** qui spécifient les conditions dans lesquelles les offres sont présentées.

1. **Créez des qualificateurs de collection** (auparavant appelés « balises ») et associez-les aux offres pour un classement et une recherche faciles dans la bibliothèque.

1. Si vous souhaitez définir des règles qui déterminent quelle offre doit être présentée en premier pour un emplacement donné (plutôt que de prendre en compte les scores de priorité des offres), vous pouvez **créer une formule de classement**.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Création d’emplacements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Création de règles de décision</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Création de balises</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Création de formules de classement</a>
</div>
<p>
</td>
</tr>
</table>

## Création et gestion des offres {#create-and-manage-offers}

1. **Créez des offres** et configurez leur contenu et leurs propriétés.

1. **Créez des offres de secours**, qui sont les dernières offres de recours à afficher si les clients ne sont éligibles à aucune des offres sélectionnées.

1. **Créez une collection** afin d&#39;inclure les offres personnalisées que vous avez créées et de les utiliser dans une décision.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Création d’offres</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Création d’offres de secours</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Création de collections</a>
</div>
<p>
</td>
</tr>
</table>

## Création et configuration des décisions {#create-and-configure-decisions}

1. **Créez une décision** qui combine des emplacements avec des offres personnalisées et des offres de secours. Cette combinaison sera utilisée par le moteur de décision pour trouver la meilleure offre pour un profil spécifique.

1. **Configurez la décision**. Pour ce faire, sélectionnez les emplacements, puis, pour chaque emplacement, sélectionnez une collection et une offre de secours.

1. Si nécessaire, vous pouvez **attribuer une formule de classement** à un emplacement lors de la configuration de la décision.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Création de décisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configuration des décisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Attribution d’un classement</a>
</div>
<p>
</td>
</tr>
</table>
