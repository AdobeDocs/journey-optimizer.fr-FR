---
title: Conditions préalables requises pour les canaux web
description: Pour créer et accéder à des pages web dans l’interface utilisateur de Journey Optimizer, remplissez les conditions préalables répertoriées sur cette page.
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: 65a33d6836c43564ef7c93660a8076677ea5cba8
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 99%

---

# Conditions préalables et barrières de sécurité {#web-prerequisites}

Pour créer et accéder à des pages web dans l’interface utilisateur de [!DNL Journey Optimizer], remplissez les conditions préalables suivantes :

* Pour ajouter des modifications à votre site web, vous devez disposer d’une implémentation spécifique. [En savoir plus](#implementation-prerequisites).

* Pour accéder au concepteur web de [!DNL Journey Optimizer], une extension de navigateur Google Chrome spécifique doit être installée. [En savoir plus](#visual-authoring-prerequesites).

* Pour que l’expérience web soit correctement diffusée, veillez à définir les paramètres d’Adobe Experience Platform détaillés [ici](#delivery-prerequisites).

## Attention

Dans [!DNL Journey Optimizer], vous ne pouvez actuellement créer des expériences web qu’en utilisant des **campagnes**. [En savoir plus](../campaigns/create-campaign.md#configure).


Les campagnes web de [!DNL Journey Optimizer] ciblent les nouveaux profils qui n’ont jamais été engagés sur d’autres canaux. Cela augmente le nombre total de profils engageables, ce qui peut avoir des implications de coût si le nombre contractuel de profils engageables que vous avez achetés est dépassé. Les mesures de licence de chaque package sont répertoriées à la page [Description du produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html).

## Conditions préalables à l’implémentation {#implementation-prerequisites}

Actuellement, deux types d’implémentation sont pris en charge pour permettre la création et la diffusion de campagnes de canal web sur vos propriétés web :

* Côté client uniquement : pour ajouter des modifications à votre site web, vous devez implémenter le [SDK web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} sur votre site web.

* Mode hybride : vous pouvez utiliser l’[API de serveur du réseau Edge d’AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=fr){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>L’implémentation côté serveur uniquement n’est actuellement pas prise en charge.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Conditions préalables à la création visuelle {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Pour pouvoir ouvrir, créer et prévisualiser vos pages web de manière fiable dans le concepteur web de [!DNL Journey Optimizer], vous devez disposer de l’extension de navigateur [Visual Editing Helper d’Adobe Experience Cloud ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} installée sur votre navigateur web.

>[!CAUTION]
>
>Google Chrome et Microsoft Edge sont actuellement les seuls navigateurs qui prennent en charge la création de pages web dans [!DNL Journey Optimizer].

### Installer l’extension Visual Editing Helper {#install-visual-editing-helper}

Pour télécharger et installer l’extension de navigateur Visual Editing Helper, suivez les étapes ci-dessous :

1. Ouvrez un nouvel onglet dans votre navigateur (Google Chrome ou Microsoft Edge).

1. Accédez au [Chrome Web Store de Google](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Si vous utilisez Microsoft Edge, sélectionnez **[!UICONTROL Autorisation les extensions d’autres magasins]** sur la bannière supérieure. Vous pourrez ainsi ajouter des extensions du Chrome Web Store à Microsoft Edge.

1. Recherchez l’extension de navigateur [Visual Editing Helper d’Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} et accédez-y.

1. Cliquez sur **[!UICONTROL Ajouter à Chrome]** > **[!UICONTROL Ajouter l’extension]**.

   >[!NOTE]
   >
   >Si vous utilisez Microsoft Edge, l’extension sera ajoutée à Edge même si le bouton indique **[!UICONTROL Ajouter à Chrome]**.

1. Assurez-vous que l’extension de navigateur Visual Editing Helper est correctement activée dans la barre d’outils de votre navigateur.

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

L’extension Visual Editing Helper d’Adobe Experience Cloud est désormais automatiquement activée lorsqu’un site web est ouvert dans le concepteur web [!DNL Journey Optimizer] pour optimiser la création.

L’extension ne dispose d’aucun paramètre conditionnel et gère automatiquement tous les paramètres, y compris les paramètres des cookies SameSite.

>[!NOTE]
>
>Certains sites web peuvent ne pas s’ouvrir de manière fiable dans le concepteur web [!DNL Journey Optimizer], et ce, pour l’une des raisons suivantes :
>
> * Le site Web possède des politiques strictes en matière de sécurité.
> * Le site Web se trouve dans un iframe.
> * Le site d’assurance qualité et/ou d’étape du client n’est pas disponible pour le grand public (site interne).


### Résoudre les problèmes de chargement du site web {#troubleshooting}

Lors de l’utilisation du concepteur web d’Adobe [!DNL Journey Optimizer], si vous tentez de charger un site web et que ce chargement échoue, un message s’affiche vous suggérant d’installer l’[extension de navigateur Visual Editing Helper](#install-visual-editing-helper).

Si l’extension de navigateur Visual Editing Helper est correctement installée, mais que le site web ne parvient toujours pas à se charger ou se comporte de manière inattendue, un correctif potentiel consiste à ouvrir votre site web dans le navigateur et à accepter les cookies avant de tenter de le charger dans le concepteur web de [!DNL Journey Optimizer].

Pour les pages sous authentification, si le chargement de la page de connexion échoue ou si vous ne parvenez pas à vous connecter :

* Essayez d’abord de vous connecter dans un nouvel onglet du navigateur et accédez à la page souhaitée, puis copiez l’URL et essayez de l’ouvrir dans le concepteur web de [!DNL Journey Optimizer].

* Si vous ne parvenez toujours pas à charger votre site web dans le concepteur web de [!DNL Journey Optimizer], contactez l’assistance clientèle d’Adobe pour signaler le problème, en veillant à spécifier l’URL défaillante.

## Conditions préalables à la diffusion {#delivery-prerequisites}

Pour que l’expérience web soit correctement diffusée, les paramètres suivants doivent être définis :

* Dans la [Collecte de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}, assurez-vous qu’un flux de données est défini, de telle sorte que sous le service **[!UICONTROL Adobe Experience Platform]**, les deux options suivantes soient activées : **[!UICONTROL Segmentation Edge]** et **[!UICONTROL Adobe Journey Optimizer]**.

   Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target="_blank"}.

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >L’option **[!UICONTROL Adobe Journey Optimizer]** ne peut être activée que lorsque l’option **[!UICONTROL Segmentation Edge]** est déjà activée.

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

   Cette politique de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}.

   ![](assets/web-aep-merge-policy.png)

## Domaines de marque pour les ressources {#branded-domains-for-assets}

Lors de la création d’expériences web, si vous ajoutez du contenu provenant de la bibliothèque d’[Adobe Experience Manager Assets Essentials](../email/assets-essentials.md), vous devez configurer le sous-domaine qui sera utilisé pour publier ce contenu. [En savoir plus](web-delegated-subdomains.md).
