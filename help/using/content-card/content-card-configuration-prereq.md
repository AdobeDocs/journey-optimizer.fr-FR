---
title: Configuration des cartes de contenu
description: Prérequis du canal de cartes de contenu
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: d4dce7b31d898d86c330048e6d0a1587e87a617c
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 18%

---

# Conditions préalables des cartes de contenu {#content-card-configuration-prereq}

Pour que Adobe Journey Optimizer affiche correctement les cartes de contenu, vous devez configurer les paramètres Adobe Experience Platform suivants :

* **Collecte de données Adobe Experience Platform**

  [Créez un flux de données](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) et [ajoutez le service Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep). Activez les options **[!UICONTROL Segmentation Edge]** et **[!UICONTROL Adobe Journey Optimizer]** . Cela permet de s’assurer que les événements Journey Optimizer sont gérés par l’Edge Network Adobe Experience Platform.
Ajoutez le groupe de champs **Experience Event - Proposition Interaction** à votre jeu de données pour inclure ces données dans vos rapports. [En savoir plus sur les jeux de données](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)

* **Adobe Experience Platform**

  Assurez-vous que la stratégie de fusion par défaut **Active-On-Edge Merge Policy** est activée sous le menu Experience Platform **[!UICONTROL Client]** > **[!UICONTROL Profils]** > **[!UICONTROL Stratégies de fusion]**. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  >[!NOTE]
  >
  >Lors de l’utilisation d’une politique de fusion personnalisée **[!UICONTROL Préférence de jeu de données]**, veillez à ajouter le jeu de données **[!UICONTROL Parcours entrant]** dans la politique de fusion spécifiée.

* **SDK Web Adobe Experience Platform Mobile ou Platform**

  Pour les applications mobiles et web, pour ajouter des modifications à vos pages web ou applications mobiles, vous devez mettre en oeuvre le [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/platform-learn/implement-web-sdk/overview) sur votre site web ou le [SDK mobile Adobe Experience Platform](https://developer.adobe.com/client-sdks/home/) sur vos applications mobiles.

* **Journey Optimizer**

  Créez une [configuration de carte de contenu](#content-card-configuration).

* **Dépannage**

  Utilisez la vue **Edge Delivery** dans **Adobe Experience Platform Assurance** pour résoudre les problèmes liés aux expériences mobiles. Il peut examiner les requêtes, vérifier les appels Edge et examiner les données de profil. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery)

* **Expériences de contenu**

  Assurez-vous que le jeu de données utilisé dans la [datastream](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank) de votre application est également inclus dans votre configuration de création de rapports d’expérience de contenu. Les données de l’application ne s’afficheront pas dans les rapports si les jeux de données ne correspondent pas.

  Découvrez comment ajouter des jeux de données pour les rapports d’expérience de contenu dans [cette section](../reports/reporting-configuration.md).
