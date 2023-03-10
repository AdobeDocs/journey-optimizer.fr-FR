---
title: Collecte de données
description: En savoir plus sur la collecte de données de retour de la gestion de la décision
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 6%

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

1. D’une part, certains canaux **automatiquement** effectuer le suivi des impressions et des clics ; En voici la liste :

   * Emails créés par [!DNL Journey Optimizer]
   * Notifications push mobiles créées par [!DNL Journey Optimizer]
   * Applications mobiles utilisant la variable [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=fr#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou SDK Mobile<!--TBC--> pour effectuer le rendu des offres <!--need more info + link-->

   >[!NOTE]
   >
   >Si Adobe effectue le rendu visuel de l’offre à l’utilisateur final sur le canal, vous pouvez supposer que l’Adobe enverra automatiquement les commentaires.

1. D’un autre côté, certains canaux nécessitent que les données d’impression et de clics soient envoyées dans Adobe Experience Platform en tant que **événement d’expérience**.

   Sauf les applications mobiles qui utilisent le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=fr#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou SDK Mobile<!--TBC-->, tous les canaux qui utilisent une requête d’API de prise de décision pour recevoir des offres ont besoin de commentaires envoyés en tant qu’événement d’expérience. Cela inclut :

   * Pages web
   * Kiosques
   * Messages envoyés par le biais d’applications tierces

   >[!NOTE]
   >
   >Si l’offre a besoin d’instructions sur le rendu, vous pouvez supposer que vous devez envoyer des commentaires en tant qu’événements d’expérience.

### Événements personnalisés

Vous pouvez envoyer des commentaires sur les événements personnalisés liés à une offre dans Adobe Experience Platform en fonction de vos préférences. Par exemple, si une offre comporte plusieurs boutons, tels que *Intéressé*, *Pas intéressé*, etc., vous pouvez envoyer ces événements séparément, mais ils peuvent également être envoyés en tant qu’événements d’expérience. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Envoi de données de retour

Pour envoyer des données de retour, vous devez créer un jeu de données pour collecter les événements et, pour chaque type d’événement, définir un événement d’expérience qui sera envoyé à Adobe Experience Platform.

* Découvrez comment créer un jeu de données où les événements d’expérience seront collectés dans [cette section](create-dataset.md).

* Découvrez comment définir des événements d’expérience pour envoyer des données de retour dans [cette section](schema-requirement.md).

