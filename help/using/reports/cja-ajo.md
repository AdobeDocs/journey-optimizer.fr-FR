---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser Customer Journey Analytics
description: Prendre en main Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 928ad6822efbe95c0ddf5456531d92be8b4bed75
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 95%

---

# Utiliser [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer]
L’intégration de  à [!DNL Customer Journey Analytics] offre une vue d’ensemble de tous vos parcours avec une distribution de rapports automatisée et des visualisations personnalisées des données.

![](assets/cja.png)

Une fois que vous avez créé votre parcours dans [!DNL Journey Optimizer], vous pouvez commencer à importer vos données clients dans [!DNL Customer Journey Analytics] afin de lancer des rapports et de comprendre l’impact de chaque interaction d’un client avec vos parcours.

➡️ [Découvrir Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=fr){target=&quot;_blank&quot;}

Avant d’utiliser [!DNL Customer Journey Analytics] pour vos parcours, vous devez d’abord configurer cette intégration :

1. [Création d’une connexion](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=fr) in [!DNL Customer Journey Analytics] avec le **[!UICONTROL Jeu de données]** vous souhaitez envoyer à Adobe Experience Platform.

   [!DNL Journey Optimizer] peuvent être configurés :
   * [Événement d’étape de parcours](../data/datasets-query-examples.md#journey-step-event) : permet d’afficher qui entre dans vos parcours et jusqu’où ils vont.
   * [Jeux de données de retour/tracking de message](../data/datasets-query-examples.md#message-feedback-event-dataset) : permet d’afficher les informations de diffusion sur vos messages envoyés par le biais de [!DNL Journey Optimizer].
   * [Jeux de données d’entité et de parcours](../data/datasets-query-examples.md#entity-dataset) : permet de rechercher des noms conviviaux et de les utiliser dans vos rapports.

1. [Créez une vue de données](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=fr) pour configurer les dimensions et mesures à utiliser dans votre rapport.

   Vous pouvez créer des mesures spécifiques dans Journey Optimizer pour mieux refléter les données de vos parcours. [En savoir plus](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html?lang=fr#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


L’utilisation de [!DNL Journey Optimizer] avec [!DNL Customer Journey Analytics] peut entraîner des incohérences dans les données de rapport, qui sont dues aux problèmes suivants :

* **[!DNL Journey Optimizer] et [!DNL Customer Journey Analytics] synchronisent les données à partir du connecteur Azure Data Lake Storage (ADLS) pour la création de rapports.**

   Le temps de traitement des données entrantes peut différer légèrement d’un produit à l’autre. En conséquence, les données peuvent ne pas correspondre lors de l’affichage des rapports allant d’une date donnée jusqu’à la date actuelle. Pour réduire les incohérences, utilisez des périodes qui excluent le jour en cours.

* **Dans les rapports [!DNL Journey Optimizer], la mesure Envoyé comprend également la mesure Reprise.**

   **[!UICONTROL Les Reprises]** ne seront pas incluses dans la mesure **[!UICONTROL Envoyé]** dans [!DNL Customer Journey Analytics]. Par conséquent, les mesures **[!UICONTROL Envoyé]** de [!DNL Customer Journey Analytics] afficheront des valeurs inférieures à [!DNL Journey Optimizer]. Toutefois, les données de reprise convergent vers la mesure **[!UICONTROL Messages envoyés avec succès]** ou **[!UICONTROL Rebonds.]**
Pour réduire les incohérences, utilisez des périodes qui datent d’une semaine ou même d’avant.

* **Les rapports sont alimentés à partir d’une autre source de données.**

   Cela peut entraîner de incohérences de 1 à 2 % des données entre les produits. 
