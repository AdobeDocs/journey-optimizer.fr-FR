---
title: Configuration des cartes de contenu
description: Conditions préalables du canal des cartes de contenu
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 73%

---

# Conditions préalables des cartes de contenu {#content-card-configuration-prereq}

Pour qu’Adobe Journey Optimizer affiche correctement les cartes de contenu, vous devez configurer les paramètres Adobe Experience Platform suivants :

* **Collecte de données dʼAdobe Experience Platform**

  [Créez un train de données](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/configure){target="_blank"} et [ajoutez le service Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/configure#aep){target="_blank"}. Activez les options **[!UICONTROL Segmentation Edge]** et **[!UICONTROL Adobe Journey Optimizer]**. Cela permet de s’assurer que les événements entrants Journey Optimizer sont gérés par Adobe Experience Platform Edge Network.
Ajoutez le groupe de champs **Événement d’expérience - Interaction de proposition** à votre jeu de données pour inclure ces données dans vos rapports. [En savoir plus sur les trains de données](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Assurez-vous d’avoir une politique de fusion par défaut avec l’option **Politique de fusion Active-On-Edge** activée dans le menu Experience Platform **[!UICONTROL Client ou cliente]** > **[!UICONTROL Profils]** > **[!UICONTROL Politiques de fusion]**. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  >[!NOTE]
  >
  >Lors de l’utilisation d’une politique de fusion personnalisée **[!UICONTROL Préférence de jeu de données]**, veillez à ajouter le jeu de données **[!UICONTROL Parcours entrant]** dans la politique de fusion spécifiée.

* **SDK web ou mobile Adobe Experience Platform**

  Concernant les applications web et mobiles, pour ajouter des modifications à vos pages web ou à vos applications mobiles, vous devez mettre en œuvre le [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/platform-learn/implement-web-sdk/overview){target="_blank"} sur votre site web ou le [SDK mobile Adobe Experience Platform](https://developer.adobe.com/client-sdks/home/){target="_blank"} sur vos applications mobiles.

* **Journey Optimizer**

  Créez une [configuration de carte de contenu](#content-card-configuration).

* **Dépannage**

  Utilisez la vue **Edge Delivery** dans **Adobe Experience Platform Assurance** pour résoudre les problèmes liés aux expériences mobiles. Les requêtes et les données de profil peuvent être examinées, tout comme les appels Edge. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **Expériences de contenu**

  Assurez-vous que le jeu de données utilisé dans le [train de données](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/overview#_blank){target="_blank"} de votre application est également inclus dans votre configuration des rapports d’expérience de contenu. Les données de l’application ne s’afficheront pas dans les rapports si les jeux de données ne correspondent pas.

  Découvrez comment ajouter des jeux de données pour les rapports d’expérience de contenu dans [cette section](../reports/reporting-configuration.md).

## Mécanisme de sécurisation de la gestion des profils {#profile-management-guardrail}

Les cartes de contenu [!DNL Journey Optimizer] peuvent cibler des profils pseudonymes, c’est-à-dire des profils qui ne sont pas authentifiés ou qui ne sont pas encore connus, car ils n’ont encore jamais été engagés sur d’autres canaux. C’est le cas, par exemple, lors du ciblage de tous les visiteurs ou audiences en fonction d’identifiants temporaires tels qu’ECID.

Cela augmente le nombre total de profils engageables, ce qui peut avoir des implications de coût si le nombre contractuel de profils engageables que vous avez achetés est dépassé. Les mesures de licence de chaque package sont répertoriées dans la page [Description de produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Vous pouvez vérifier le nombre de profils engageables dans le [tableau de bord de l’utilisation des licences](../audience/license-usage.md).

Pour que vos profils engageables restent dans des limites raisonnables, Adobe recommande de définir une durée de vie (TTL) pour supprimer automatiquement les profils pseudonymes du profil client en temps réel s’ils n’ont pas été vus ou engagés dans une fenêtre temporelle spécifique.

>[!NOTE]
>
>Découvrez comment configurer l’expiration des données pour les profils pseudonymes dans la documentation d’[Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

Adobe recommande de définir la valeur de durée de vie sur 14 jours pour correspondre à la durée de vie actuelle du profil Edge.