---
title: Collecte de données
description: En savoir plus sur la collecte de données de retour de la gestion de la décision
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: c9e970bc231fc3d19f0243b71256ea0f5a981af7
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# Collecte de données de gestion des décisions {#data-collection}

## Présentation de la collecte de données

Vous pouvez collecter les commentaires des offers decisionings dans Adobe Experience Platform, notamment les offres qui s’affichent et la manière dont les utilisateurs interagissent avec eux. Ces données peuvent être utilisées pour :
* Composante [Rapports de gestion des décisions](../reports/get-started-events.md);
* Utilisation [capping de la fréquence](../offer-library/add-constraints.md#capping) les règles;
* Création [Modèles AI](../ranking/create-ranking-strategies.md) qui peut être utilisé comme méthode de classement.

## Types d’événements

La manière dont les données sont collectées varie en fonction du type d’événement que vous souhaitez capturer.

### Événements de décision

Chaque fois que la gestion des décisions prend une décision, les informations relatives à cet événement de décision sont **automatiquement** envoyé à Adobe Experience Platform pour tous les canaux. [En savoir plus](../reports/get-started-events.md).

### Impression et clic sur les événements

Les impressions et les clics de la gestion des décisions sont définis comme suit :

* Un **impression** est lorsqu’une offre est affichée pour un utilisateur.

* A **click** est lorsqu’un utilisateur clique ou interagit avec une offre.

Les commentaires sur les impressions et les clics sont capturés en fonction de la variable [!DNL Journey Optimizer] canal utilisé.

**Emails** créé par [!DNL Journey Optimizer] **automatiquement** effectuer le suivi des impressions et des clics ;

Cependant, **la plupart des canaux** nécessite l’envoi des données d’impression et de clics dans Adobe Experience Platform en tant que **événement d’expérience**. Cela inclut :

* Pages Web utilisant la variable [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr){target="_blank"} pour effectuer le rendu des offres

* Applications mobiles utilisant la variable [SDK Adobe Experience Platform Mobile](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Kiosques
* Messages envoyés par le biais d’applications tierces
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Les canaux qui utilisent une requête d’API de prise de décision pour recevoir des offres ont besoin de commentaires envoyés en tant qu’événement d’expérience. En d’autres termes, si l’offre a besoin d’instructions sur le rendu, vous pouvez supposer que vous devez envoyer des commentaires en tant qu’événements d’expérience.

### Événements personnalisés

Vous pouvez envoyer des commentaires sur les événements personnalisés liés à une offre dans Adobe Experience Platform en fonction de vos préférences. Par exemple, si une offre comporte plusieurs boutons, tels que *Intéressé*, *Pas intéressé*, etc., vous pouvez envoyer ces événements séparément, mais ils peuvent également être envoyés en tant qu’événements d’expérience. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Envoi de données de retour

Pour envoyer des données de retour, vous devez créer un jeu de données pour collecter les événements et, pour chaque type d’événement, définir un événement d’expérience qui sera envoyé à Adobe Experience Platform.

* Découvrez comment créer un jeu de données où les événements d’expérience seront collectés dans [cette section](create-dataset.md).

* Découvrez comment définir des événements d’expérience pour envoyer des données de retour dans [cette section](schema-requirement.md).

