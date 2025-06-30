---
title: Collecte de données
description: En savoir plus sur la collecte de données des commentaires sur la gestion des décisions
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: 32e3a5b9-0633-48df-95b5-c03536be23a1
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 86%

---

# Collecte de données sur la gestion des décisions {#data-collection}

## Présentation de la collecte de données

Vous pouvez collecter des commentaires concernant la prise de décisions sur les offres dans Adobe Experience Platform, notamment par rapport aux offres présentées et à la manière dont les utilisateurs et utilisatrices interagissent avec elles. Tirez ensuite parti de ces données dans les scénarios suivants :

* élaborer des [rapports de prise de décision](../cja-reporting.md) ;
* Utilisation des règles [capping](../items.md#capping) ;
* créer des [modèles d’IA](../ranking/ai-models.md) qui peuvent être utilisés comme méthode de classement.

## Types d’événements

Le mode de collecte de données varie en fonction du type d’événement que vous souhaitez capturer.

### Événements de décision

Chaque fois que Decisioning prend une décision, les informations relatives à cet événement de décision sont **automatiquement** envoyées à Adobe Experience Platform. <!--TBC + link-->

### Événements d’impression et de clic

Les impressions et les clics de la gestion des décisions sont définis comme suit :

* un événement d’**impression** se produit lorsqu’une offre est présentée à un utilisateur ou une utilisatrice,

* un événement de **clic** survient lorsqu’un utilisateur ou une utilisatrice clique ou interagit avec une offre.

Le mode de capture des commentaires sur les impressions et les clics dépend du canal [!DNL Journey Optimizer] emprunté.

Les **e-mails** créés par [!DNL Journey Optimizer] effectuent **automatiquement** le suivi des impressions et des clics.

Cependant, pour la **plupart des canaux**, les données relatives aux impressions et aux clics doivent être transmises à Adobe Experience Platform en tant qu’**événement d’expérience**. Cela inclut :

* Pages web utilisant [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr){target="_blank"} pour effectuer le rendu des offres

* Applications mobiles utilisant [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=fr){target="_blank"} pour effectuer le rendu des offres - [En savoir plus](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
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
