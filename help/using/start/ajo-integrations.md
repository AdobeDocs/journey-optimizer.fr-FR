---
solution: Journey Optimizer
product: journey optimizer
title: Intégration à d’autres solutions
description: Découvrez comment intégrer Journey Optimizer à d’autres solutions.
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 90d7d4d39fe04198707be3d5b24888cfe5bed308
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 100%

---

# Intégration à d’autres solutions {#integration}

Adobe Journey Optimizer vous permet de gérer, conserver et exporter en toute facilité ces données vers des plateformes ou systèmes faisant partie de votre pile technologique. Ces intégrations vous aident à résoudre vos cas d’utilisation spécifiques et à accroitre la portée des fonctionnalités d’Adobe Journey Optimizer.

>[!NOTE]
>
> Adobe Journey Optimizer repose sur la technologie d’Adobe Experience Platform et est connecté nativement au [Profil client en temps réel Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target=&quot;_blank&quot;}. Cette source de données intégrée est préconfigurée et conçue pour récupérer et utiliser des données du profil client en temps réel (par exemple, vérifier si la personne qui est entrée dans un parcours est un client ou non). Elle vous permet d’utiliser les données de profil et les données des événements d’expérience. [En savoir plus](../datasource/adobe-experience-platform-data-source.md).

## Adobe Customer Journey Analytics{#integration-cja}

Customer Journey Analytics vous permet d’effectuer une analyse avancée des données générées par Journey Optimizer.

Journey Optimizer stocke les données dans Adobe Experience Platform. Customer Journey Analytics vous offre ensuite un affichage holistique de tous vos parcours, campagnes et offres, avec distribution automatique de rapports et visualisations personnalisées des données.

Une fois votre parcours créé dans Journey Optimizer, Customer Journey Analytics peut ingérer les données de Platform pour lancer des rapports et saisir l’impact de chaque interaction d’un client avec vos parcours.

En savoir plus sur [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

Vous pouvez exploiter toutes les données d’événement comportemental Adobe Analytics que vous capturez déjà et diffusez en continu dans Adobe Experience Platform afin de déclencher en temps réel des parcours et d’automatiser les expériences de vos clients. Ces données peuvent également être utilisées pour créer des segments qui peuvent être engagés à l’aide de Journey Optimizer.

En savoir plus sur [Journey Optimizer + Analytics](../event/about-analytics.md).

## Services intelligents Adobe{#integration-intelligent-service}

Les services intelligents Adobe, intégrés nativement à Real-Time Customer Data Platform, vous permettent de tirer parti de la puissance de l’intelligence artificielle et du machine learning dans les cas d’utilisation de l’expérience client. Les analystes marketing peuvent obtenir des prédictions spécifiques aux besoins d’une entreprise en utilisant des configurations au niveau de l’entreprise sans avoir besoin d’expertise en sciences des données.

L’IA dédiée aux clients permet aux marques de créer des scores d’attrition ou de conversion basés sur le machine learning, qui seront disponibles sous forme d’attributs de profil dans Adobe Experience Platform et prêts à être utilisés pour personnaliser un parcours.

[En savoir plus](../building-journeys/ai-services-overview.md).


## Adobe Campaign{#integration-ac}

Une intégration est disponible si vous disposez d’Adobe Campaign v7 ou v8. Utilisez cette intégration pour envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’Adobe Campaign.

En savoir plus sur [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Vous pouvez également configurer une intégration à Adobe Campaign Standard pour envoyer des messages dans vos parcours.

En savoir plus sur [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

## Canaux personnalisés{#integration-custom}

Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, utilisez les actions personnalisées pour établir la connexion aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;}, Firebase, etc.

Les actions personnalisées sont des actions supplémentaires définies par les utilisateurs techniques et mises à la disposition des professionnels du marketing. Une fois configurées, elles apparaissent dans la palette gauche de votre parcours, dans la catégorie **[!UICONTROL Action]**. En savoir plus sur [cette page](../building-journeys/about-journey-activities.md#action-activities).

En savoir plus sur les [actions personnalisées](../action/about-custom-action-configuration.md).

## Sources de données externes{#integration-external-systems}

Journey Optimizer vous permet de configurer des connexions à des systèmes externes par le biais de sources de données et d’actions personnalisées. Vous pouvez ainsi, par exemple, enrichir vos parcours avec des données provenant d’un système de réservation externe.

Découvrez comment utiliser des sources de données externes pour définir une connexion à un système tiers dans [cette section](../datasource/external-data-sources.md).
