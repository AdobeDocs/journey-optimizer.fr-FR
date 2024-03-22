---
title: Barrières de sécurité et conditions préalables de l’expérience basées sur le code
description: Pour pouvoir modifier des applications et des pages web à l’aide de la fonctionnalité basée sur le code Journey Optimizer, respectez les conditions préalables présentées dans cette page.
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: d2ac4dfe40559f01db59e314e8838f51b39a8659
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 87%

---

# Barrières de sécurité et conditions préalables {#web-prerequisites}

Pour pouvoir utiliser des actions d’expérience basée sur le code dans [!DNL Journey Optimizer] et diffuser la payload du contenu du code qui peut être utilisée par vos applications, procédez comme suit :

* Pour ajouter des modifications à vos applications, vous devez disposer d’une mise en oeuvre spécifique. [En savoir plus](#implementation-prerequisites)

* Pour que les expériences basées sur le code soient correctement diffusées, veillez à définir les paramètres d’Experience Platform présentés [ici](#delivery-prerequisites).

>[!CAUTION]
>
>* Le canal d’expérience basé sur le code n’est pas disponible pour les organisations qui ont acheté l’Adobe. **Bouclier sanitaire** et **Protection de la vie privée et protection** offres complémentaires.
>
>* Vous pouvez uniquement créer des expériences basées sur du code dans **campagnes**. [En savoir plus](../campaigns/create-campaign.md#configure


## Conditions préalables à l’implémentation {#implementation-prerequisites}

L’expérience basée sur le code prend en charge n’importe quel type d’implémentation du client ou de la cliente, comme illustré dans les options ci-dessous. Vous pouvez utiliser une méthode d’implémentation côté client, côté serveur ou hybride pour vos propriétés :

* Côté client uniquement : pour ajouter des modifications à vos pages web ou applications mobiles, vous devez mettre en œuvre le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} sur vos applications mobiles.

* Mode hybride : vous pouvez utiliser l’[API EP Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=fr){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Côté serveur : vous pouvez utiliser l’[API AEP Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur. Votre équipe de développement doit gérer la réponse et effectuer le rendu des modifications côté client dans la mise en œuvre de votre application.

Vous trouverez des exemples de chaque méthode d’implémentation ci-dessus dans [cette section](code-based-implementation-samples.md).

## Conditions préalables à la diffusion {#delivery-prerequisites}

Pour que les expériences basées sur le code soient correctement diffusées, les paramètres suivants doivent être définis :

* Dans la [Collecte de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}, assurez-vous qu’un train de données est défini, de telle sorte que sous le service **[!UICONTROL Adobe Experience Platform]**, l’option **[!UICONTROL Adobe Journey Optimizer]** soit activée.

  Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target="_blank"}.

  ![](../web/assets/web-aep-datastream-ajo.png)

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  Cette politique de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}.

  ![](../web/assets/web-aep-merge-policy.png)

## Conditions préalables à l’expérience de contenu {#experiment-prerequisites}

Pour activer les expériences de contenu pour le canal basé sur le code, vous devez vous assurer que le [jeu de données](../data/get-started-datasets.md) utilisé dans le [train de données](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=fr){target="_blank"} de votre implémentation web est également inclus dans la configuration des rapports.

En d’autres termes, lors de la configuration des rapports d’expérience, si vous ajoutez un jeu de données qui n’est pas présent dans le train de données de votre application, les données de l’application ne s’afficheront pas dans les rapports d’expérience de contenu.

Découvrez comment ajouter des jeux de données pour les rapports d’expérience de contenu dans [cette section](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Le jeu de données est utilisé en lecture seule par le système de création de rapports de [!DNL Journey Optimizer] et n’affecte pas la collecte ni l’ingestion de données.
