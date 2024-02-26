---
solution: Journey Optimizer
product: journey optimizer
title: Intégration à d’autres solutions
description: Découvrez comment intégrer Journey Optimizer à d’autres solutions.
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: eef253f35bf93edbe5b64b47754e16e4c590f862
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 92%

---

# Intégration à d’autres solutions {#integration}

Avec Adobe Journey Optimizer, vous pouvez facilement gérer, conserver et exporter vos données vers les autres plateformes ou systèmes que vous utilisez. Ces intégrations vous aident à résoudre vos cas d’utilisation spécifiques et à accroitre la portée des fonctionnalités d’Adobe Journey Optimizer.

>[!NOTE]
>
> Adobe Journey Optimizer repose sur la technologie d’Adobe Experience Platform et est connecté nativement au [Profil client en temps réel Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}. Cette source de données intégrée est préconfigurée et conçue pour récupérer et utiliser des données du profil client en temps réel (par exemple, vérifier si la personne qui est entrée dans un parcours est un client ou non). Elle vous permet d’utiliser les données de profil et les données des événements d’expérience. [En savoir plus](../datasource/adobe-experience-platform-data-source.md).
>

## Adobe Customer Journey Analytics {#integration-cja}

Customer Journey Analytics vous permet d’effectuer une analyse avancée des données générées par Journey Optimizer.

Journey Optimizer stocke les données dans Adobe Experience Platform. Customer Journey Analytics vous offre ensuite un affichage holistique de tous vos parcours, campagnes et offres, avec distribution automatique de rapports et visualisations personnalisées des données.

Une fois votre parcours créé dans Journey Optimizer, Customer Journey Analytics peut ingérer les données de Platform pour lancer des rapports et saisir l’impact de chaque interaction d’un client avec vos parcours.

En savoir plus sur [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics {#integration-aa}

Vous pouvez exploiter toutes les données d’événement comportemental Adobe Analytics que vous capturez déjà et diffusez en continu dans Adobe Experience Platform afin de déclencher en temps réel des parcours et d’automatiser les expériences de vos clients. Vous pouvez également utilisez ces données pour créer des audiences qui peuvent être engagées à l’aide de Journey Optimizer.

En savoir plus sur [Journey Optimizer + Analytics](../event/about-analytics.md).


## Adobe Experience Manager Assets {#integration-assets}

Rassemblez les workflows marketing et créatifs à l’aide de [!DNL Adobe Experience Manager Assets]. Intégrés nativement à [!DNL Adobe Journey Optimizer], accédez à [!DNL Adobe Experience Manager Assets] pour stocker, gérer, découvrir et distribuer des ressources numériques. Ceci fournit un référentiel de ressources unique et centralisé que vous pouvez utiliser pour renseigner vos messages.

[!DNL Adobe Experience Manager Assets] est accessible directement depuis [!DNL Adobe Journey Optimizer] via la section **[!UICONTROL Ressources]** du menu de gauche.

En savoir plus sur [Journey Optimizer + Adobe Experience Manager Assets](../content-management/assets.md).


## Adobe Stock {#integration-stock}

Le plug-in d’intégration d’[!DNL Adobe Stock] et du concepteur d’e-mail [!DNL Adobe Journey Optimizer] fournit aux clients et clientes une façon simple de naviguer, d’acquérir des produits sous licence et d’enregistrer des images en vue de les utiliser dans la création de messages.

Avec [!DNL Adobe Journey Optimizer], vous pouvez charger des images dans vos e-mails directement depuis [!DNL Adobe Stock] et les ajouter à votre dossier **[!UICONTROL Ressources]** à l’aide de l’option **[!UICONTROL Trouver des photos Adobe Stock]**. En outre, l’option **[!UICONTROL Trouver des photos Stock similaires]** vous permet de trouver les images correspondant au contenu, à la couleur et à la composition de la ressource utilisée dans votre diffusion.

En savoir plus sur [Journey Optimizer + Stock](../content-management/stock.md).


## Services intelligents Adobe {#integration-intelligent-service}

Les services intelligents Adobe, intégrés nativement à Real-Time Customer Data Platform, vous permettent de tirer parti de la puissance de l’intelligence artificielle et du machine learning dans les cas d’utilisation de l’expérience client. Les personnes analystes marketing peuvent obtenir des prédictions spécifiques aux besoins d’une entreprise en utilisant des configurations au niveau de l’entreprise sans avoir besoin d’expertise en sciences des données.

L’IA dédiée aux clients permet aux marques de créer des scores d’attrition ou de conversion basés sur le machine learning, qui seront disponibles sous forme d’attributs de profil dans Adobe Experience Platform et prêts à être utilisés pour personnaliser un parcours.

[En savoir plus](../building-journeys/ai-services-overview.md).


## Adobe Campaign {#integration-ac}

Une intégration est disponible si vous disposez d’Adobe Campaign v7 ou v8. Utilisez cette intégration pour envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’Adobe Campaign.

En savoir plus sur [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Vous pouvez également configurer une intégration à Adobe Campaign Standard pour envoyer des messages dans vos parcours.

En savoir plus sur [Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).


## Adobe Workfront {#integration-workfront}

Utilisez les modules Adobe Journey Optimizer dans Adobe Workfront pour créer, lire, mettre à jour ou supprimer des enregistrements, ou effectuez un appel d’API personnalisé vers l’API Adobe Journey Optimizer.

Un aperçu de l’étape clé de cette intégration est disponible. [dans cet article de blog](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/accelerating-go-to-market-how-workfront-workfront-fusion-aep-and/ba-p/653685){target="_blank"}.

En savoir plus sur Journey Optimizer + Adobe Workfront [dans la documentation Adobe Workfront](https://experienceleague.adobe.com/docs/workfront/using/adobe-workfront-fusion/fusion-apps-and-modules/adobe-journey-optimizer-modules.html){target="_blank"}.

## Canaux personnalisés {#integration-custom}

Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, utilisez les actions personnalisées pour établir la connexion aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, etc.

Les actions personnalisées sont des actions supplémentaires définies par les utilisateurs techniques et mises à la disposition des professionnels du marketing. Une fois configurées, elles apparaissent dans la palette gauche de votre parcours, dans la catégorie **[!UICONTROL Action]**. En savoir plus sur [cette page](../building-journeys/about-journey-activities.md#action-activities).

En savoir plus sur les [actions personnalisées](../action/about-custom-action-configuration.md).

## Sources de données externes {#integration-external-systems}

Journey Optimizer vous permet de configurer des connexions à des systèmes externes par le biais de sources de données et d’actions personnalisées. Vous pouvez ainsi, par exemple, enrichir vos parcours avec des données provenant d’un système de réservation externe.

Découvrez comment utiliser des sources de données externes pour définir une connexion à un système tiers dans [cette section](../datasource/external-data-sources.md).
