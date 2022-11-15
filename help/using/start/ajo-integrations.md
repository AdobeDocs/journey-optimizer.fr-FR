---
solution: Journey Optimizer
product: journey optimizer
title: Intégration avec d'autres solutions
description: Découvrez comment intégrer Journey Optimizer à d’autres solutions
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 34d768502bfb2ce792beae8b1257fdddefc55ed7
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 37%

---

# Intégration avec d&#39;autres solutions {#integration}

Avec Adobe Journey Optimizer, vous pouvez facilement gérer, conserver et exporter ces données vers des plateformes ou des systèmes qui font partie de votre pile technologique. Ces intégrations vous aident à résoudre vos cas d’utilisation spécifiques et à étendre la portée fonctionnelle de Adobe Journey Optimizer.

>[!NOTE]
>
> Basé sur Adobe Experience Platform, Adobe Journey Optimizer est nativement connecté à [Profil client en temps réel Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target=&quot;_blank&quot;}. Cette source de données intégrée est préconfigurée et est conçue pour récupérer et utiliser les données de Real-time Customer Profile (par exemple, vérifier si la personne qui a entré un parcours est un client ou non). Elle vous permet d&#39;utiliser les données de profil et les données des événements d&#39;expérience.


## Création de rapports{#integration-reporting}

### Adobe Customer Journey Analytics{#integration-cja}

Vous pouvez exporter les données générées par Journey Optimizer afin d’effectuer une analyse avancée dans Customer Journey Analytics.

L’intégration de Journey Optimizer avec Customer Journey Analytics offre une vue d’ensemble de tous vos parcours avec la distribution de rapports automatisée et des visualisations personnalisées des données.

Après avoir créé votre parcours dans Journey Optimizer, vous pouvez importer vos données client dans Customer Journey Analytics afin de lancer des rapports et de comprendre l’impact de chaque interaction d’un client avec vos parcours.

En savoir plus sur [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

### Adobe Analytics{#integration-aa}

Vous pouvez exploiter toutes les données d’événement comportemental Adobe Analytics que vous capturez déjà et diffusez en continu dans Adobe Experience Platform afin de déclencher des parcours et d’automatiser les expériences de vos clients.

En savoir plus sur [Journey Optimizer + Analytics](../event/about-analytics.md).

## Apprentissage automatique{#integration-intelligent-service}

L’intégration à Adobe Intelligent Services vous permet d’exploiter la puissance de l’intelligence artificielle et de l’apprentissage automatique dans les cas d’utilisation de l’expérience client. Les analystes marketing peuvent obtenir des prédictions spécifiques aux besoins d’une entreprise en utilisant des configurations au niveau de l’entreprise sans avoir besoin d’expertise en sciences des données.

## Envoi des messages {#integration-messages}

Vous pouvez utiliser un système tiers pour envoyer des messages.

### Adobe Campaign{#integration-ac}

Une intégration est disponible si vous disposez d&#39;Adobe Campaign v7 ou v8. Utilisez cette intégration pour envoyer des emails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle Adobe Campaign.

En savoir plus sur [Journey Optimizer + Campagne](../building-journeys/ajo-ac.md).

Vous pouvez également configurer une intégration avec Adobe Campaign Standard pour envoyer des messages dans vos parcours.

En savoir plus sur [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

### Canaux personnalisés{#integration-custom}

Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, c’est à cet emplacement que vous configurez la connexion de ce système aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase, etc.

Les actions personnalisées sont des actions supplémentaires définies par les utilisateurs techniques et mises à la disposition des professionnels du marketing. Une fois configurés, elles apparaissent dans la palette gauche de votre parcours, dans la catégorie **[!UICONTROL Action]**. En savoir plus sur [cette page](../building-journeys/about-journey-activities.md#action-activities).

En savoir plus sur [actions personnalisées](../action/about-custom-action-configuration.md).

## Systèmes externes{#integration-external-systems}

Journey Optimizer vous permet de configurer des connexions à des systèmes externes par le biais de sources de données et d&#39;actions personnalisées. Vous pouvez ainsi, par exemple, enrichir vos parcours de données provenant d&#39;un système de réservation externe ou envoyer des messages à l&#39;aide d&#39;un système tiers tel qu&#39;Epsilon ou Facebook.

Découvrez comment utiliser des sources de données externes pour définir une connexion à un système tiers dans [cette section](../datasource/external-data-sources.md).
