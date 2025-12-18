---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Collecte de données
description: En savoir plus sur la collecte de données des commentaires sur la gestion des décisions
badge: label="Hérité" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 100%

---

# Collecte de données sur la gestion des décisions {#data-collection}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

## Présentation de la collecte de données

Vous pouvez collecter des commentaires concernant la prise de décisions sur les offres dans Adobe Experience Platform, notamment par rapport aux offres présentées et à la manière dont les utilisateurs et utilisatrices interagissent avec elles. Tirez ensuite parti de ces données dans les scénarios suivants :

* élaborer des [rapports de gestion des décisions](../reports/get-started-events.md),
* utiliser des règles de [limitation de la fréquence](../offer-library/add-constraints.md#capping),
* créer des [modèles d’IA](../ranking/create-ranking-strategies.md) qui peuvent être utilisés comme méthode de classement.

## Types d’événements

Le mode de collecte de données varie en fonction du type d’événement que vous souhaitez capturer.

### Événements de décision

Chaque fois que la gestion des décisions prend une décision, les informations relatives à cet événement de décision sont **automatiquement** envoyées à Adobe Experience Platform, et ce pour tous les canaux. [En savoir plus](../reports/get-started-events.md).

### Événements d’impression et de clic

Les impressions et les clics de la gestion des décisions sont définis comme suit :

* un événement d’**impression** se produit lorsqu’une offre est présentée à un utilisateur ou une utilisatrice,

* un événement de **clic** survient lorsqu’un utilisateur ou une utilisatrice clique ou interagit avec une offre.

Le mode de capture des commentaires sur les impressions et les clics dépend du canal [!DNL Journey Optimizer] emprunté.

Les **e-mails** créés par [!DNL Journey Optimizer] effectuent **automatiquement** le suivi des impressions et des clics.

Cependant, pour la **plupart des canaux**, les données relatives aux impressions et aux clics doivent être transmises à Adobe Experience Platform en tant qu’**événement d’expérience**. Cela inclut :

* Les pages web utilisant le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com//docs/experience-platform/edge/home.html?lang=fr){target="_blank"} pour afficher les offres

* Les applications mobiles utilisant le [SDK mobile Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=fr){target="_blank"} pour afficher les offres - [En savoir plus](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* les kiosques,
* les messages envoyés par le biais d’applications tierces.
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Les canaux qui utilisent une requête d’API de prise de décision pour recevoir des offres ont besoin de commentaires envoyés en tant qu’événement d’expérience. Autrement dit, si l’offre nécessite des instructions pour effectuer le rendu, vous pouvez en déduire que vous devez envoyer les commentaires sous la forme d’événements d’expérience.

### Événements personnalisés

Vous pouvez envoyer les commentaires sur les événements personnalisés associés à une offre à Adobe Experience Platform en fonction de vos préférences. Par exemple, si une offre comporte plusieurs boutons, comme *Intéressé(e)*, *Pas intéressé(e)*, etc., vous pouvez envoyer ces événements séparément, mais ils peuvent également être envoyés en tant qu’événements d’expérience.

## Envoyer des données de commentaires

Pour envoyer des données de commentaires, vous devez créer un jeu de données pour collecter les événements et, pour chaque type d’événement, définir un événement d’expérience qui sera envoyé à Adobe Experience Platform.

* Découvrez comment créer un jeu de données où les événements d’expérience seront collectés dans [cette section](create-dataset.md).

* Découvrez comment définir des événements d’expérience afin d’envoyer des données de commentaires dans [cette section](schema-requirement.md).
