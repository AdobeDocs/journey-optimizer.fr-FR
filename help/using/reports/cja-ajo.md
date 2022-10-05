---
title: Utilisation de Customer Journey Analytics
description: Prise en main du Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: ce0906afb8561c586cb080c4a49c58fb5bfac6a9
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 7%

---

# Utilisation d’[!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)
[!DNL Journey Optimizer] intégration avec [!DNL Customer Journey Analytics] offre une vue d’ensemble de tous vos parcours avec une distribution de rapports automatisée et des visualisations personnalisées des données.

Après avoir créé votre parcours dans [!DNL Journey Optimizer], vous pouvez importer vos données client dans [!DNL Customer Journey Analytics] pour lancer des rapports et comprendre l’impact de chaque interaction d’un client avec vos parcours.

➡️ [Discover Customer Journey Analytics](https://docs.adobe.com/content/help/fr-FR/experience-cloud/user-guides/home.translate.html){target=&quot;_blank&quot;}

Avant d’utiliser [!DNL Customer Journey Analytics] pour vos parcours, vous devez d’abord configurer cette intégration :

1. [Création d’une connexion](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=fr) in [!DNL Customer Journey Analytics] avec le **[!UICONTROL Jeu de données]** vous souhaitez envoyer à Platform.

   Les éléments suivants [!DNL Journey Optimizer] peut être configuré :
   * [Événement d’étape de parcours](../start/datasets-query-examples.md#journey-step-event): vous permet de voir qui entre dans vos parcours et jusqu’où ils arrivent.
   * [Message Feedback/Tracking des jeux de données](../start/datasets-query-examples.md#message-feedback-event-dataset): vous permet d’afficher les informations de diffusion sur vos messages envoyés par le biais de [!DNL Journey Optimizer].
   * [Jeux de données d’entité et de Parcours](../start/datasets-query-examples.md#entity-dataset): vous permet de rechercher des noms conviviaux et de les utiliser dans vos rapports.

1. [Création d’une vue de données](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=fr) pour configurer les dimensions et mesures à utiliser pour votre rapport.

   Vous pouvez créer des mesures spécifiques à Journey Optimizer pour mieux refléter les données de vos parcours. [En savoir plus](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Utilisation [!DNL Journey Optimizer] avec [!DNL Customer Journey Analytics] peut entraîner des incohérences dans les données des rapports dues à :

* **Les [!DNL Journey Optimizer] et [!DNL Customer Journey Analytics] synchroniser les données à partir d’Azure Data Lake Storage (ADLS) pour la création de rapports ;**

   Le temps de traitement des données entrantes peut différer légèrement d’un produit à l’autre. En conséquence, les données peuvent ne pas correspondre lors de l’affichage des rapports d’une date donnée à la date actuelle. Pour réduire les incohérences, utilisez des périodes à l’exception du jour en cours.

* **Dans [!DNL Journey Optimizer] la mesure Envoyés comprend également la mesure Reprise .**

   **[!UICONTROL Reprises]** ne sera pas inclus dans **[!UICONTROL Envoyé]** dans [!DNL Customer Journey Analytics]. Cela entraînera [!DNL Customer Journey Analytics] **[!UICONTROL Envoyé]** pour afficher les valeurs inférieures à [!DNL Journey Optimizer]. Toutefois, les données de reprise sont converties dans la variable **[!UICONTROL Messages envoyés avec succès]** ou **[!UICONTROL Rebonds]** mesure.
Pour réduire les incohérences, utilisez des périodes d’une semaine ou même plus tard.

* **Les rapports sont diffusés à partir d’une autre source de données.**

   Cela peut entraîner des incohérences de données entre 1 et 2 % entre les produits.
