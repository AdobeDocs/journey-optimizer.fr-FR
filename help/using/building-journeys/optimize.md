---
solution: Journey Optimizer
product: journey optimizer
title: Activité Optimiser
description: En savoir plus sur l’activité Optimiser
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: activité, condition, zone de travail, parcours, optimisation
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 496
ht-degree: 44%

---

# Prise en main de l’activité Optimisation {#journey-path-optimization}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser l’activité Optimiser pour créer plusieurs chemins de parcours en fonction de l’expérimentation, du ciblage et des conditions, en remplaçant l’ancienne activité de condition.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Activité Optimiser"
>abstract="L’activité **Optimiser** vous permet de définir la progression des individus dans votre parcours en créant plusieurs chemins en fonction de critères spécifiques, y compris l’expérimentation, le ciblage et des conditions spécifiques. Notez que l’activité **Optimiser** est le nouveau moyen de créer des chemins conditionnels dans les parcours. Elle remplace l’ancienne activité **Condition**."

>[!IMPORTANT]
>
>L’activité **Optimiser** est le nouveau moyen de créer des chemins conditionnels dans les parcours. Elle remplace l’ancienne activité **Condition**, qui a été supprimée de l’interface d’utilisation. Toute la logique conditionnelle est conservée et est désormais gérée via les [conditions](conditions.md) de l’activité **Optimize**.
>
>Si des parcours existants utilisent des activités **[!UICONTROL Condition]**, vous pouvez continuer à les utiliser comme auparavant. Elles s’affichent désormais avec une nouvelle icône en tant qu’activités **[!UICONTROL Optimiser]** à l’aide de la méthode **[!UICONTROL Condition]**, mais le comportement reste inchangé. Toute étiquette personnalisée que vous avez définie sur le nœud est conservée.

L’activité **Optimiser** vous permet de définir la progression des individus dans votre parcours en créant plusieurs **chemins** en fonction de critères spécifiques, notamment l’expérimentation, le ciblage et des conditions spécifiques, garantissant ainsi un engagement et un succès optimaux pour créer des parcours hautement personnalisés et efficaces.

![Bouton Optimiser dans la palette d’activités du parcours](assets/journey-optimize.png)

## Qu’est-ce qu’un chemin de parcours ? {#journey-path}

Un **chemin** de parcours peut être constitué de l’un des éléments suivants : séquencement des communications, intervalle entre celles-ci, nombre de communications ou toute combinaison de ces trois variables.

Par exemple, un chemin peut contenir un e-mail, un autre peut contenir deux SMS et un troisième peut contenir un e-mail, un nœud d’attente de deux heures, puis un SMS.

## Trois façons d’optimiser vos parcours {#optimization-methods}

Grâce à l’activité **Optimiser**, vous pouvez effectuer les actions suivantes sur vos chemins de parcours :

* [Exécuter des expériences de chemin](path-experimentation.md) - Testez différents chemins en fonction de divisions aléatoires afin de déterminer celui qui fonctionne le mieux en fonction des mesures de succès prédéfinies (par exemple : taux de conversion, chiffre d’affaires, engagement).

* [Tirer parti des règles de ciblage](path-targeting.md) - Définissez des règles spécifiques qui doivent être respectées pour qu’un client puisse accéder à l’un des chemins de parcours, en fonction des segments d’audience, des attributs de profil ou des données contextuelles. Cela permet de s’assurer que l’audience appropriée entre dans le chemin spécifié.

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est actuellement en disponibilité limitée. Pour obtenir l’accès, contactez votre représentant ou représentante Adobe.

* [Appliquer des conditions](conditions.md) - Créez des chemins d’accès conditionnels en fonction de critères spécifiques tels que les sources de données, l’heure, la date, les divisions en pourcentage ou les limites de profil. Il s’agit de l’équivalent de l’ancienne activité Condition .

## Fonctionnement {#how-it-works}

Une fois le parcours actif, les profils sont évalués en fonction des critères définis. Puis, en fonction des critères correspondants, ils sont envoyés vers le chemin approprié du parcours.

## Étapes suivantes {#next-steps}

Sélectionnez la méthode d’optimisation qui correspond le mieux à votre cas d’utilisation :

* Vous souhaitez tester et savoir quel chemin est le plus performant ? → Accéder à [Expérimentation de chemin](path-experimentation.md)
* Vous souhaitez envoyer différentes audiences sur des chemins spécifiques ? → Accéder au [Ciblage des chemins](path-targeting.md)
* Vous souhaitez créer une logique conditionnelle (scénarios if/then) ? → Accéder à [&#x200B; Conditions &#x200B;](conditions.md)
