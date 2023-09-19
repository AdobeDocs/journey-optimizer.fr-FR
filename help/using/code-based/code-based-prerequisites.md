---
title: Conditions préalables requises pour une expérience basée sur le code
description: Pour pouvoir modifier des applications et des pages web à l’aide de la fonction basée sur le code Journey Optimizer, suivez les conditions préalables sur cette page.
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 43%

---

# Conditions préalables et mécanismes de sécurisation {#web-prerequisites}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main du canal basé sur le code](get-started-code-based.md)
* **[Conditions préalables basées sur le code](code-based-prerequisites.md)**
* [Exemples de mise en oeuvre basés sur le code](code-based-implementation-samples.md)
* [Création d’expériences basées sur du code](create-code-based.md)

>[!ENDSHADEBOX]

Pour pouvoir utiliser des actions d’expérience basées sur le code dans [!DNL Journey Optimizer] et diffusez la payload du contenu de code qui peut être utilisée par vos applications, procédez comme suit :

* Pour ajouter des modifications à vos applications, vous devez disposer d’une mise en oeuvre spécifique. [En savoir plus](#implementation-prerequisites)

* Pour que les expériences basées sur le code soient correctement diffusées, veillez à définir les paramètres Adobe Experience Platform détaillés. [here](#delivery-prerequisites).

## Notes de mise en garde {#caution-notes-web}

* Le canal d’expérience basé sur le code est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

* Actuellement dans [!DNL Journey Optimizer] vous pouvez uniquement créer des expériences basées sur du code dans **campagnes**. [En savoir plus](../campaigns/create-campaign.md#configure)

## Conditions préalables à l’implémentation {#implementation-prerequisites}

L’expérience basée sur le code prend en charge n’importe quel type d’implémentation client, comme illustré dans les options ci-dessous. Vous pouvez utiliser une méthode de mise en oeuvre côté client, côté serveur ou hybride pour vos propriétés :

* Côté client uniquement : pour ajouter des modifications à vos pages web ou applications mobiles, vous devez mettre en oeuvre l’une des fonctionnalités suivantes : [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} sur vos applications mobiles.

* Mode hybride : vous pouvez utiliser l’[API de serveur du réseau Edge d’AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=fr){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Côté serveur : vous pouvez utiliser la variable [API du serveur réseau AEP Edge](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur. Votre équipe de développement doit gérer la réponse et effectuer le rendu des modifications côté client dans l’implémentation de votre application.

Vous trouverez des exemples pour chaque méthode de mise en oeuvre ci-dessus dans la section [cette section](code-based-implementation-samples.md).

## Conditions préalables à la diffusion {#delivery-prerequisites}

Pour que les expériences basées sur le code soient correctement diffusées, les paramètres suivants doivent être définis :

* Dans la [Collecte de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}, assurez-vous qu’un train de données est défini, de telle sorte que sous le service **[!UICONTROL Adobe Experience Platform]**, l’option **[!UICONTROL Adobe Journey Optimizer]** soit activée.

  Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target="_blank"}.

  ![](../web/assets/web-aep-datastream-ajo.png)

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  Cette politique de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}.

  ![](../web/assets/web-aep-merge-policy.png)

## Conditions préalables à l’expérience de contenu {#experiment-prerequisites}

Pour activer des expériences de contenu pour le canal basé sur le code, vous devez vous assurer que la variable [dataset](../data/get-started-datasets.md) utilisé dans l’implémentation de votre application [datastream](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=fr){target="_blank"} est également inclus dans votre configuration de création de rapports.

En d’autres termes, lors de la configuration des rapports d’expérience, si vous ajoutez un jeu de données qui n’est pas présent dans votre flux de données d’application, les données d’application ne s’afficheront pas dans les rapports d’expérience de contenu.

Découvrez comment ajouter des jeux de données pour les rapports d’expérience de contenu dans [cette section](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Le jeu de données est utilisé en lecture seule par le système de création de rapports de [!DNL Journey Optimizer] et n’affecte pas la collecte ni l’ingestion de données.


