---
solution: Journey Optimizer
product: journey optimizer
title: Intégration avec d'autres solutions
description: Découvrez comment intégrer Journey Optimizer à d’autres solutions
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 90d7d4d39fe04198707be3d5b24888cfe5bed308
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 19%

---

# Intégration avec d&#39;autres solutions {#integration}

Avec Adobe Journey Optimizer, vous pouvez facilement gérer, conserver et exporter ces données vers des plateformes ou des systèmes qui font partie de votre pile technologique. Ces intégrations vous aident à résoudre vos cas d’utilisation spécifiques et à étendre la portée fonctionnelle de Adobe Journey Optimizer.

>[!NOTE]
>
> Basé sur Adobe Experience Platform, Adobe Journey Optimizer est nativement connecté à [Profil client en temps réel Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target=&quot;_blank&quot;}. Cette source de données intégrée est préconfigurée et est conçue pour récupérer et utiliser les données de Real-time Customer Profile (par exemple, vérifier si la personne qui a entré un parcours est un client ou non). Elle vous permet d&#39;utiliser les données de profil et les données des événements d&#39;expérience. [En savoir plus](../datasource/adobe-experience-platform-data-source.md).

## Adobe Customer Journey Analytics{#integration-cja}

Vous pouvez utiliser Customer Journey Analytics pour effectuer une analyse avancée sur les données générées par Journey Optimizer.

Journey Optimizer stocke les données dans Adobe Experience Platform. Avec Customer Journey Analytics, vous pouvez obtenir une vue d’ensemble de tous vos parcours, campagnes et offres, avec une distribution de rapports automatisée et des visualisations personnalisées des données.

Après avoir créé votre parcours dans Journey Optimizer, Customer Journey Analytics peut ingérer des données à partir de la plateforme pour commencer des rapports et comprendre l’impact de chaque interaction d’un client avec vos parcours.

En savoir plus sur [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

Vous pouvez exploiter toutes les données d’événement comportemental Adobe Analytics que vous capturez déjà et diffusez en continu dans Adobe Experience Platform pour déclencher des parcours en temps réel et automatiser les expériences de vos clients. Ces données peuvent également être utilisées pour créer des segments pouvant être engagés à l’aide de Journey Optimizer.

En savoir plus sur [Journey Optimizer + Analytics](../event/about-analytics.md).

## Adobe Intelligent Services{#integration-intelligent-service}

Les services intelligents Adobe, qui sont natifs de la plateforme de données clients en temps réel, vous permettent d’exploiter la puissance de l’intelligence artificielle et de l’apprentissage automatique dans les cas d’utilisation de l’expérience client. Les analystes marketing peuvent obtenir des prédictions spécifiques aux besoins d’une entreprise en utilisant des configurations au niveau de l’entreprise sans avoir besoin d’expertise en sciences des données.

Customer AI permet aux marques de créer des scores basés sur l’apprentissage automatique d’attrition ou de conversion qui seront disponibles en tant qu’attributs de profil dans Adobe Experience Platform et qui pourront être utilisés pour personnaliser un parcours.

[En savoir plus](../building-journeys/ai-services-overview.md).


## Adobe Campaign{#integration-ac}

Une intégration est disponible si vous disposez d&#39;Adobe Campaign v7 ou v8. Utilisez cette intégration pour envoyer des emails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle Adobe Campaign.

En savoir plus sur [Journey Optimizer + Campagne](../building-journeys/ajo-ac.md).

Vous pouvez également configurer une intégration avec Adobe Campaign Standard pour envoyer des messages dans vos parcours.

En savoir plus sur [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

## Canaux personnalisés{#integration-custom}

Si vous utilisez un système tiers pour envoyer des messages ou si vous souhaitez que parcours envoie des appels d’API à un système tiers, utilisez des actions personnalisées pour vous connecter à votre parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase, etc.

Les actions personnalisées sont des actions supplémentaires définies par les utilisateurs techniques et mises à la disposition des professionnels du marketing. Une fois configurés, ils s’affichent dans la palette gauche de votre parcours dans le **[!UICONTROL Action]** catégorie. En savoir plus sur [cette page](../building-journeys/about-journey-activities.md#action-activities).

En savoir plus sur [actions personnalisées](../action/about-custom-action-configuration.md).

## Sources de données externes{#integration-external-systems}

Journey Optimizer vous permet de configurer des connexions à des systèmes externes par le biais de sources de données et d&#39;actions personnalisées. Cela vous permet, par exemple, d’enrichir vos parcours de données provenant d’un système de réservation externe.

Découvrez comment utiliser des sources de données externes pour définir une connexion à un système tiers dans [cette section](../datasource/external-data-sources.md).
