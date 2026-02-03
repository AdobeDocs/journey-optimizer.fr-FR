---
title: Prérequis pour le canal web
description: Pour créer et accéder à des pages web dans l’interface utilisateur de Journey Optimizer, remplissez les conditions préalables répertoriées sur cette page.
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 22e1f08f434a3ceb4be6c539d4007178062cba9e
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 97%

---

# Conditions préalables et mécanismes de sécurisation {#web-prerequisites}

Pour créer et accéder à des pages web dans l’interface utilisateur de [!DNL Journey Optimizer], remplissez les conditions préalables suivantes :

* Pour ajouter des modifications à votre site web, vous devez disposer d’une implémentation spécifique. [En savoir plus](#implementation-prerequisites)

* Pour accéder au concepteur web de [!DNL Journey Optimizer], une extension de navigateur Google Chrome spécifique doit être installée. [En savoir plus](#visual-authoring-prerequisites)

* Pour que l’expérience web soit correctement diffusée, veillez à définir les paramètres d’Adobe Experience Platform détaillés [ici](#delivery-prerequisites).

* Pour activer les rapports pour le canal web, vous devez vous assurer que le jeu de données utilisé dans le train de données de votre implémentation web est également inclus dans la configuration des rapports. [En savoir plus](#experiment-prerequisites)

>[!IMPORTANT]
>
>* Les campagnes web de [!DNL Journey Optimizer] ciblent les nouveaux profils qui n’ont jamais été engagés sur d’autres canaux. Cela augmente le nombre total de [profils engageables](../audience/license-usage.md), ce qui peut avoir des implications de coût si le nombre contractuel de profils engageables que vous avez achetés est dépassé. Les mesures de licence de chaque package sont répertoriées dans la page [Description de produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Vous pouvez vérifier le nombre de profils engageables dans le [tableau de bord d’utilisation des licences](../audience/license-usage.md).
>
>* Lors du ciblage de profils pseudonymes (personnes non authentifiés) avec vos pages web, pensez à définir une durée de vie (TTL) pour la suppression automatique des profils afin de maîtriser le nombre de profils engageables et les coûts associés. [En savoir plus](../start/guardrails.md#profile-management-inbound)

## Conditions préalables à l’implémentation {#implementation-prerequisites}

Deux types d’implémentation sont pris en charge pour permettre la création et la diffusion de campagnes de canal web sur vos propriétés web :

* Côté client uniquement : pour ajouter des modifications à votre site web, vous devez implémenter le [SDK web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} sur votre site web.

  >[!NOTE]
  >
  >Assurez-vous que la version de votre [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/release-notes){target="_blank"} est 2.16 ou supérieure.

* Mode hybride : vous pouvez utiliser l’[API du serveur Edge Network AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur ; la réponse est transmise au SDK Web Adobe Experience Platform afin d’appliquer les modifications côté client. Pour plus d’informations, consultez la [documentation de l’API du serveur Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=fr){target="_blank"} Adobe Experience Platform. Vous pouvez en savoir plus sur le mode hybride et consulter quelques exemples de mise en œuvre dans cet [article de blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>L’implémentation côté serveur uniquement n’est actuellement pas prise en charge avec le canal web. Si vous disposez d’une implémentation côté serveur uniquement pour vos pages web, vous pouvez utiliser le [canal d’expérience basée sur du code](../code-based/get-started-code-based.md) à la place.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Conditions préalables à la création visuelle {#visual-authoring-prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_web_browser_extension"
>title="Créer une règle de correspondance de pages"
>abstract="Pour accéder au concepteur web de [!DNL Journey Optimizer], vous devez installer une extension de navigateur spécifique : Visual Editing Helper d’Adobe Experience Cloud, disponible uniquement sur Google Chrome ou Microsoft Edge."

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Pour pouvoir ouvrir, créer et prévisualiser vos pages web de manière fiable dans le concepteur web de [!DNL Journey Optimizer], vous devez avoir installé l’extension de navigateur [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} sur votre navigateur.

>[!CAUTION]
>
>Google Chrome et Microsoft Edge sont actuellement les seuls navigateurs qui prennent en charge la création de pages web dans [!DNL Journey Optimizer].

### Installer l’extension Visual Editing Helper {#install-visual-editing-helper}

Pour télécharger et installer l’extension de navigateur Visual Editing Helper, suivez les étapes ci-dessous :

1. Ouvrez un nouvel onglet dans votre navigateur (Google Chrome ou Microsoft Edge).

1. Accédez au [Chrome Web Store de Google](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Si vous utilisez Microsoft Edge, sélectionnez **[!UICONTROL Autorisation les extensions d’autres magasins]** sur la bannière supérieure. Vous pourrez ainsi ajouter des extensions du Chrome Web Store à Microsoft Edge.

1. Recherchez et accédez à l’extension de navigateur [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}.

1. Cliquez sur **[!UICONTROL Ajouter à Chrome]** > **[!UICONTROL Ajouter l’extension]**.

   >[!NOTE]
   >
   >Si vous utilisez Microsoft Edge, l’extension sera ajoutée à Edge même si le bouton indique **[!UICONTROL Ajouter à Chrome]**.

1. Assurez-vous que l’extension de navigateur Visual Editing Helper est correctement activée dans la barre d’outils de votre navigateur.

   ![](assets/web-visual-editing-extension-edge.png)

L’extension Visual Editing Helper d’Adobe Experience Cloud est désormais automatiquement activée lorsqu’un site web est ouvert dans le [concepteur web](web-visual-editor.md) [!DNL Journey Optimizer] pour optimiser la création.

L’extension ne dispose d’aucun paramètre conditionnel et gère automatiquement tous les paramètres, y compris les paramètres des cookies SameSite.

>[!NOTE]
>
>Certains sites web peuvent ne pas s’ouvrir de manière fiable dans le concepteur web [!DNL Journey Optimizer], et ce, pour l’une des raisons suivantes :
>
> * Le site web a des politiques de sécurité strictes.
> * Le site web est dans un iframe.
> * Le site d’assurance qualité ou d’évaluation du client ou de la cliente n’est pas disponible pour le monde extérieur (le site est interne).

### Résoudre les problèmes de chargement du site web {#troubleshooting}

Lors de l’utilisation du concepteur web d’Adobe [!DNL Journey Optimizer], si vous tentez de charger un site web et que ce chargement échoue, un message s’affiche vous suggérant d’installer l’[extension de navigateur Visual Editing Helper](#install-visual-editing-helper).

1. Assurez-vous que l’extension de navigateur Visual Editing Helper est correctement installée.

1. Si le site web se comporte toujours de manière inattendue, assurez-vous que les cookies tiers sont autorisés dans votre navigateur. Sinon, la page web ne peut pas être chargée dans le concepteur web [!DNL Journey Optimizer].

Pour les pages sous authentification, si le chargement de la page de connexion échoue ou si vous ne parvenez pas à vous connecter :

1. Essayez d’abord de vous connecter dans un nouvel onglet du navigateur et accédez à la page souhaitée, puis copiez l’URL et essayez de l’ouvrir dans le concepteur web de [!DNL Journey Optimizer].

2. Si vous ne parvenez toujours pas à charger votre site web dans le concepteur web de [!DNL Journey Optimizer], contactez l’assistance clientèle d’Adobe pour signaler le problème, en veillant à spécifier l’URL défaillante.

## Conditions préalables à la diffusion {#delivery-prerequisites}

Pour que l’expérience web soit correctement diffusée, les paramètres suivants doivent être définis :

* Dans la [collecte de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}, assurez-vous qu’un train de données est défini et que, dans le service **[!UICONTROL Adobe Experience Platform]**, l’option **[!UICONTROL Adobe Journey Optimizer]** est activée.

  Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}, assurez-vous d’avoir une politique de fusion avec l’option **[!UICONTROL Politique de fusion Active-On-Edge]** activée. Pour ce faire, sélectionnez une politique dans le menu Experience Platform **[!UICONTROL Client ou cliente]** > **[!UICONTROL Profils]** > **[!UICONTROL Politiques de fusion]**. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  Cette politique de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Pour résoudre les problèmes liés à la diffusion d’expériences web Journey Optimizer, vous pouvez utiliser la vue **Edge Delivery** dans **Adobe Experience Platform Assurance**. Ce plug-in vous permet de regarder en détail les appels de requête, de vérifier si les appels Edge attendus se produisent comme prévu et d’examiner les données de profil, notamment les mappages d’identités, les appartenances à des segments et les paramètres de consentement. En outre, vous pouvez consulter les activités pour lesquelles la requête a rempli les critères et identifier celles pour lesquelles elle ne l’a pas fait.

  L’utilisation du plug-in **Edge Delivery** vous aide à obtenir les informations nécessaires pour comprendre vos implémentations entrantes et résoudre leurs problèmes efficacement.

  [En savoir plus sur la vue Edge Delivery](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery)

## Conditions préalables aux rapports {#experiment-prerequisites}

Pour activer les rapports pour le canal web, vous devez vous assurer que le [jeu de données](../data/get-started-datasets.md) utilisé dans le [train de données](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=fr){target="_blank"} de votre implémentation web est également inclus dans la configuration des rapports.

En d’autres termes, lors de la configuration des rapports, si vous ajoutez un jeu de données qui n’est pas présent dans votre train de données web, les données web ne s’afficheront pas dans vos rapports.

Découvrez comment ajouter des jeux de données pour les rapports dans [cette section](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Le jeu de données est utilisé en lecture seule par le système de création de rapports de [!DNL Journey Optimizer] et n’a aucune incidence sur la collecte ou l’ingestion de données.

Si vous **n’utilisez pas** les [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=fr#field-group){target="_blank"} prédéfinis suivants pour le schéma de votre jeu de données : `AEP Web SDK ExperienceEvent` et `Consumer Experience Event` (tels que définis sur [cette page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html?lang=fr#add-field-groups){target="_blank"}), assurez-vous d’ajouter les groupes de champs suivants : `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` et `Web Details`. Ceux-ci sont nécessaires pour la création de rapports [!DNL Journey Optimizer], car ils effectuent le suivi des campagnes et des parcours auxquels chaque profil participe.

[En savoir plus sur la configuration des rapports](../reports/reporting-configuration.md)

>[!NOTE]
>
>L’ajout de ces groupes de champs n’a aucune incidence sur la collecte de données standard. Seules les pages où une campagne ou un parcours est en cours d’exécution sont concernées. Les autres éléments de suivi restent inchangés.

## Domaines de marque pour les ressources {#branded-domains-for-assets}

Lors de la création d’expériences web, si vous ajoutez du contenu provenant de la bibliothèque [Adobe Experience Manager Assets](../integrations/assets.md), vous devez configurer le sous-domaine qui sera utilisé pour publier ce contenu. [En savoir plus](web-delegated-subdomains.md)
