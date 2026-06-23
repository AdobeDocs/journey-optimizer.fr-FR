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
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1094
ht-degree: 20%

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

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page présente l’activité Optimiser , qui remplace l’ancienne activité Condition , ce qui permet aux utilisateurs de créer plusieurs chemins de parcours à l’aide de l’expérimentation, des règles de ciblage ou d’une logique conditionnelle.

**Intentions:**

* Découvrez la fonction de l’activité Optimiser et comment elle remplace l’ancienne activité Condition
* Création de plusieurs chemins de parcours à l’aide de l’expérimentation de chemins (test A/B)
* Définissez des règles de ciblage pour acheminer des segments d’audience ou des attributs de profil spécifiques vers des chemins distincts
* Appliquez une logique conditionnelle (if/then) à l’aide de la méthode Conditions dans l’activité Optimiser .
* Migrez les parcours existants qui utilisaient l’activité Condition vers la nouvelle activité Optimiser .

**Glossaire:**

* **Activité d’optimisation** : activité de zone de travail de parcours qui remplace l’ancienne activité Condition et permet la création de plusieurs chemins d’accès par le biais d’expérimentations, de ciblages ou de conditions. *(spécifique au produit)*
* **Chemin d&#39;accès au Parcours** : séquence au sein d&#39;un parcours pouvant consister en des communications, des temps d&#39;attente, un nombre de messages ou toute combinaison de plusieurs éléments. Les profils sont acheminés vers un chemin d&#39;accès en fonction de critères définis dans l&#39;activité Optimiser . *(spécifique au produit)*
* **Expérimentation de chemin d’accès** : méthode Optimize qui divise de manière aléatoire les profils sur les chemins d’accès afin de déterminer celui qui fonctionne le mieux par rapport aux mesures de succès prédéfinies telles que le taux de conversion ou le chiffre d’affaires. *(spécifique au produit)*
* **Ciblage des chemins d’accès** : méthode Optimize (actuellement à disponibilité limitée) qui achemine les profils vers des chemins d’accès en fonction des segments d’audience, des attributs de profil ou des données contextuelles. *(spécifique au produit)*
* **Conditions** : méthode Optimize équivalente à l’ancienne activité Condition, qui crée des chemins d’accès conditionnels en fonction des sources de données, de l’heure, de la date, des divisions en pourcentage ou des limites de profil. *(spécifique au produit)*

**Mécanismes de sécurisation :**

* Le ciblage des chemins est actuellement à disponibilité limitée. Contactez votre représentant Adobe pour demander l’accès.
* L’ancienne activité Condition a été supprimée de l’interface utilisateur. Les parcours qui l’utilisaient continuent à fonctionner et s’affichent désormais avec une nouvelle icône en tant qu’activités Optimiser à l’aide de la méthode Conditions
* Les libellés personnalisés définis sur les anciens nœuds de condition sont conservés après la migration vers Optimize

**Terminologie:**

* Nom canonique : Optimiser l’activité — Acronyme : aucune — variantes : optimisation du chemin de parcours, nœud Optimiser
* Synonymes : « Optimiser l’activité (méthode Conditions) » = « ancienne activité de condition »
* Ne pas confondre : « Expérimentation de chemin » ≠ « Ciblage de chemin » — L’expérimentation de chemin utilise des divisions aléatoires pour tester le chemin le plus performant ; le ciblage de chemin utilise des règles définies pour acheminer des audiences spécifiques vers des chemins spécifiques

**FAQ:**

* **Q : Qu’est-il advenu de l’activité Condition ?** — Elle a été remplacée par l&#39;activité Optimiser et supprimée de l&#39;interface utilisateur. Les parcours existants qui utilisaient des activités Condition continuent à fonctionner sans modification. Ils s’affichent désormais avec une nouvelle icône en tant qu’activités Optimiser à l’aide de la méthode Conditions .
* **Q : Quelles sont les trois méthodes disponibles dans l’activité Optimiser ?** — Expérimentation des chemins (fractionnements A/B aléatoires pour trouver le chemin le plus performant), ciblage des chemins (routage basé sur des règles par attribut d’audience ou de profil, actuellement en disponibilité limitée) et Conditions (si/puis logique conditionnelle équivalente à l’ancienne activité de condition).
* **Q : En quoi l’expérimentation de chemin diffère-t-elle du ciblage de chemin ?** — L’expérimentation de chemins divise les profils de manière aléatoire pour tester et comparer les performances des chemins par rapport aux mesures de succès ; le ciblage de chemins achemine des audiences ou des types de profils spécifiques vers des chemins désignés en fonction de critères définis.
* **Q : Le ciblage de chemin d’accès est-il généralement disponible ?** — Non ; il est actuellement en disponibilité limitée. Contactez votre représentant Adobe pour demander l’accès.
* **Q : Qu’est-ce qu’un chemin de parcours ?** — Un chemin d’accès est une séquence au sein d’un parcours qui peut inclure une combinaison de communications, de périodes d’attente et de nombres de messages ; les profils sont évalués et acheminés vers le chemin d’accès approprié selon les critères d’activité Optimiser .

+++
