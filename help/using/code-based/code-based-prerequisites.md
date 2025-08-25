---
title: Conditions préalables à une expérience basée sur du code
description: Pour pouvoir modifier des applications et des pages web à l’aide de la fonctionnalité basée sur le code Journey Optimizer, respectez les conditions préalables présentées dans cette page.
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 70%

---

# Conditions préalables à une expérience basée sur du code {#code-based-prerequisites}

Pour pouvoir utiliser des actions d’expérience basée sur le code dans [!DNL Journey Optimizer] et diffuser la payload du contenu du code qui peut être utilisée par vos applications, procédez comme suit :

* Pour ajouter des modifications à vos applications, vous devez disposer d’une mise en œuvre spécifique. [En savoir plus](#implementation-prerequisites)

* Pour que les expériences basées sur le code soient correctement diffusées, veillez à définir les paramètres d’Experience Platform présentés [ici](#delivery-prerequisites).

* Pour que les données s’affichent dans vos rapports d’expérience basée sur du code, assurez-vous de respecter ces [conditions préalables à la création de rapports](#reporting-prerequisites).

* Lors de la création d’une [configuration de canal d’expérience basée sur du code](code-based-configuration.md), assurez-vous de saisir une chaîne/un chemin ou un URI de surface correspondant à l’élément déclaré dans votre propre implémentation. Cela garantit que le contenu est diffusé à l’emplacement souhaité dans l’application ou la page spécifiée. Sinon, les modifications ne sont pas diffusées. [En savoir plus](code-based-surface.md)

## Conditions préalables à l’implémentation {#implementation-prerequisites}

L’expérience basée sur le code prend en charge n’importe quel type d’implémentation du client ou de la cliente, comme illustré dans les options ci-dessous. Vous pouvez utiliser une méthode d’implémentation côté client, côté serveur ou hybride pour vos propriétés :

* Côté client uniquement : pour ajouter des modifications à vos pages web ou à vos applications mobiles, vous devez implémenter le [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} sur votre site web ou le [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} sur vos applications mobiles.

* Mode hybride : vous pouvez utiliser l’API du serveur AEP Edge Network [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur. La réponse est fournie à la SDK web Adobe Experience Platform pour effectuer le rendu des modifications côté client. Pour en savoir plus, consultez la documentation de l’API du serveur Adobe Experience Platform [Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=fr){target="_blank"}. Pour en savoir plus sur le mode hybride, consultez quelques exemples d’implémentation dans [cet article de blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Côté serveur : vous pouvez utiliser l’API du serveur AEP Edge Network [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur. Votre équipe de développement doit gérer la réponse et effectuer le rendu des modifications côté client dans la mise en œuvre de votre application.

Vous trouverez des exemples de chaque méthode d’implémentation ci-dessus dans [cette section](code-based-implementation-samples.md).

## Conditions préalables à la diffusion {#delivery-prerequisites}

Pour que les expériences basées sur le code soient correctement diffusées, les paramètres suivants doivent être définis :

* Dans la [Collecte de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}, assurez-vous qu’un train de données est défini, de telle sorte que sous le service **[!UICONTROL Adobe Experience Platform]** l’option **[!UICONTROL Adobe Journey Optimizer]** soit activée.

  Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}, assurez-vous d’avoir une politique de fusion avec l’option **[!UICONTROL Politique de fusion Active-On-Edge]** activée. Pour ce faire, sélectionnez une politique sous le menu Experience Platform **[!UICONTROL Client ou cliente]** > **[!UICONTROL Profils]** > **[!UICONTROL Politiques de fusion]**. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  Cette politique de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Pour résoudre les problèmes liés à la diffusion d’expériences web Journey Optimizer, vous pouvez utiliser la vue **Edge Delivery** dans **Adobe Experience Platform Assurance**. Ce plug-in vous permet de regarder en détail les appels de requête, de vérifier si les appels Edge attendus se produisent comme prévu et d’examiner les données de profil, notamment les mappages d’identités, les appartenances à des segments et les paramètres de consentement. En outre, vous pouvez consulter les activités pour lesquelles la requête a rempli les critères et identifier celles pour lesquelles elle ne l’a pas fait.

  L’utilisation du plug-in **Edge Delivery** vous aide à obtenir les informations nécessaires pour comprendre vos implémentations entrantes et résoudre leurs problèmes efficacement.

  [En savoir plus sur la vue Edge Delivery](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery)

## Conditions préalables des rapports {#reporting-prerequisites}

Pour activer la création de rapports pour le canal basé sur le code, vous devez vous assurer que le [jeu de données](../data/get-started-datasets.md) utilisé dans votre implémentation d’application [flux de données](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=fr){target="_blank"} est également inclus dans votre configuration de création de rapports.

En d’autres termes, lors de la configuration des rapports, si vous ajoutez un jeu de données qui n’est pas présent dans le train de données de votre application, les données de l’application ne s’afficheront pas dans vos rapports.

Découvrez comment ajouter des jeux de données pour les rapports dans [cette section](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Le jeu de données est utilisé en lecture seule par le système de création de rapports de [!DNL Journey Optimizer] et n’a aucune incidence sur la collecte ou l’ingestion de données.
