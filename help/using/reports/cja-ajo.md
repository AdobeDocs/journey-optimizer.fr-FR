---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de Customer Journey Analytics
description: Prise en main de Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 928ad6822efbe95c0ddf5456531d92be8b4bed75
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Utilisation de [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] intégration avec [!DNL Customer Journey Analytics] offre une vue d’ensemble de tous vos parcours avec une distribution de rapports automatisée et des visualisations personnalisées des données.

![](assets/cja.png)

Après avoir créé votre parcours dans [!DNL Journey Optimizer], vous pouvez importer vos données client dans [!DNL Customer Journey Analytics] pour créer des rapports et comprendre l’impact de chaque interaction d’un client avec vos parcours.

➡️ [Découvrez Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

Avant d’utiliser [!DNL Customer Journey Analytics] pour vos parcours, vous devez d’abord configurer cette intégration :

1. [Création d’une connexion](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] avec le **[!UICONTROL Dataset]** vous souhaitez envoyer à Adobe Experience Platform.

   Les éléments suivants [!DNL Journey Optimizer] peut être configuré :
   * [Événement d’étape du parcours](../data/datasets-query-examples.md#journey-step-event): vous permet de voir qui entre dans vos parcours et jusqu’où ils arrivent.
   * [Message Feedback/Tracking des jeux de données](../data/datasets-query-examples.md#message-feedback-event-dataset): vous permet d’afficher les informations de diffusion sur vos messages envoyés par le biais de [!DNL Journey Optimizer].
   * [Jeux de données d’entité et de parcours](../data/datasets-query-examples.md#entity-dataset): vous permet de rechercher des noms conviviaux et de les utiliser dans vos rapports.

1. [Création d’une vue de données](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) pour configurer les dimensions et mesures à utiliser pour votre rapport.

   Vous pouvez créer des mesures spécifiques à Journey Optimizer pour mieux refléter les données de vos parcours. [En savoir plus](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Utilisation [!DNL Journey Optimizer] avec [!DNL Customer Journey Analytics] peut entraîner des incohérences dans les données des rapports dues à :

* **Les [!DNL Journey Optimizer] et [!DNL Customer Journey Analytics] synchroniser les données à partir d’Azure Data Lake Storage (ADLS) pour la création de rapports ;**

   Le temps de traitement des données entrantes peut différer légèrement d’un produit à l’autre. En conséquence, les données peuvent ne pas correspondre lors de l’affichage des rapports d’une date donnée à la date actuelle. Pour réduire les incohérences, utilisez des périodes à l’exception du jour en cours.

* **Dans [!DNL Journey Optimizer] la mesure Envoyés comprend également la mesure Reprise .**

   **[!UICONTROL Retries]** ne sera pas inclus dans **[!UICONTROL Sent]** dans [!DNL Customer Journey Analytics]. Cela entraînera [!DNL Customer Journey Analytics] **[!UICONTROL Sent]** pour afficher les valeurs inférieures à [!DNL Journey Optimizer]. Toutefois, les données de reprise sont converties dans la variable **[!UICONTROL Messages successfully sent]** ou **[!UICONTROL Bounces]** mesure.
Pour réduire les incohérences, utilisez des périodes d’une semaine ou même plus tard.

* **Les rapports sont diffusés à partir d’une autre source de données.**

   Cela peut entraîner des incohérences de données entre 1 et 2 % entre les produits.
