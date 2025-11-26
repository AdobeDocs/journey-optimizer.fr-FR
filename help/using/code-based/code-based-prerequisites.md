---
title: Conditions préalables à une expérience basée sur du code
description: Pour pouvoir modifier des applications et des pages web à l’aide de la fonctionnalité basée sur le code Journey Optimizer, respectez les conditions préalables présentées dans cette page.
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 83%

---

# Conditions préalables à une expérience basée sur du code {#code-based-prerequisites}

Pour pouvoir utiliser des actions d’expérience basée sur le code dans [!DNL Journey Optimizer] et diffuser la payload du contenu du code qui peut être utilisée par vos applications, procédez comme suit :

* Pour ajouter des modifications à vos applications, vous devez disposer d’une mise en œuvre spécifique. [En savoir plus](#implementation-prerequisites)

* Pour que les expériences basées sur le code soient correctement diffusées, veillez à définir les paramètres d’Experience Platform présentés [ici](#delivery-prerequisites).

* Pour que les données s’affichent dans vos rapports d’expérience basée sur du code, assurez-vous de respecter ces [conditions préalables à la création de rapports](#reporting-prerequisites).

* Lors de la création d’une [configuration de canal d’expérience basée sur du code](code-based-configuration.md), assurez-vous de saisir une chaîne/un chemin ou un URI de surface correspondant à l’élément déclaré dans votre propre implémentation. Cela garantit que le contenu est diffusé à l’emplacement souhaité dans l’application ou la page spécifiée. Sinon, les modifications ne sont pas diffusées. [En savoir plus](code-based-surface.md)

>[!NOTE]
>
>Lorsque vous ciblez des profils pseudonymes (visiteurs non authentifiés) avec vos expériences basées sur du code, pensez à définir une durée de vie (TTL) pour la suppression automatique des profils afin de gérer le nombre de profils engageables et les coûts associés. [En savoir plus](#profile-management-guardrail)

## Conditions préalables à l’implémentation {#implementation-prerequisites}

L’expérience basée sur le code prend en charge n’importe quel type d’implémentation du client ou de la cliente, comme illustré dans les options ci-dessous. Vous pouvez utiliser une méthode d’implémentation côté client, côté serveur ou hybride pour vos propriétés :

* Côté client uniquement : pour ajouter des modifications à vos pages web ou applications mobiles, vous devez implémenter le [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} sur votre site web ou le [SDK mobile Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} sur vos applications mobiles.

* Mode hybride : vous pouvez utiliser l’[API du serveur Edge Network AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur ; la réponse est transmise au SDK Web Adobe Experience Platform afin d’appliquer les modifications côté client. Pour plus d’informations, consultez la [documentation de l’API du serveur Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=fr){target="_blank"} Adobe Experience Platform. Vous pouvez en savoir plus sur le mode hybride et consulter quelques exemples de mise en œuvre dans cet [article de blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Côté serveur : vous pouvez utiliser l’[API AEP Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"} pour demander une personnalisation côté serveur. Votre équipe de développement doit gérer la réponse et effectuer le rendu des modifications côté client dans la mise en œuvre de votre application.

Vous trouverez des exemples de chaque méthode d’implémentation ci-dessus dans [cette section](code-based-implementation-samples.md).

## Conditions préalables à la diffusion {#delivery-prerequisites}

Pour que les expériences basées sur le code soient correctement diffusées, les paramètres suivants doivent être définis :

* Dans la [collecte de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}, assurez-vous qu’un train de données est défini et que, dans le service **[!UICONTROL Adobe Experience Platform]**, l’option **[!UICONTROL Adobe Journey Optimizer]** est activée.

  Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}, assurez-vous d’avoir une politique de fusion avec l’option **[!UICONTROL Politique de fusion Active-On-Edge]** activée. Pour ce faire, sélectionnez une politique dans le menu Experience Platform **[!UICONTROL Client ou cliente]** > **[!UICONTROL Profils]** > **[!UICONTROL Politiques de fusion]**. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target="_blank"}

  Cette politique de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Pour résoudre les problèmes liés à la diffusion d’expériences web Journey Optimizer, vous pouvez utiliser la vue **Edge Delivery** dans **Adobe Experience Platform Assurance**. Ce plug-in vous permet de regarder en détail les appels de requête, de vérifier si les appels Edge attendus se produisent comme prévu et d’examiner les données de profil, notamment les mappages d’identités, les appartenances à des segments et les paramètres de consentement. En outre, vous pouvez consulter les activités pour lesquelles la requête a rempli les critères et identifier celles pour lesquelles elle ne l’a pas fait.

  L’utilisation du plug-in **Edge Delivery** vous aide à obtenir les informations nécessaires pour comprendre vos implémentations entrantes et résoudre leurs problèmes efficacement.

  [En savoir plus sur la vue Edge Delivery](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

## Conditions préalables aux rapports {#reporting-prerequisites}

Pour activer les rapports pour le canal basé sur du code, vous devez vous assurer que le [jeu de données](../data/get-started-datasets.md) utilisé dans le [train de données](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=fr){target="_blank"} de l’implémentation de votre application est également inclus dans votre configuration des rapports.

En d’autres termes, lors de la configuration des rapports, si vous ajoutez un jeu de données qui n’est pas présent dans le train de données de votre application, les données de l’application ne s’afficheront pas dans vos rapports.

Découvrez comment ajouter des jeux de données pour les rapports dans [cette section](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Le jeu de données est utilisé en lecture seule par le système de création de rapports de [!DNL Journey Optimizer] et n’a aucune incidence sur la collecte ou l’ingestion de données.

## Mécanisme de sécurisation de la gestion des profils {#profile-management-guardrail}

Les expériences basées sur du code [!DNL Journey Optimizer] peuvent cibler des profils pseudonymes, c’est-à-dire des profils qui ne sont pas authentifiés ou qui ne sont pas encore connus, car ils n’ont encore jamais été engagés sur d’autres canaux. C’est le cas, par exemple, lors du ciblage de tous les visiteurs ou audiences en fonction d’identifiants temporaires tels qu’ECID.

Cela augmente le nombre total de profils engageables, ce qui peut avoir des implications de coût si le nombre contractuel de profils engageables que vous avez achetés est dépassé. Les mesures de licence de chaque package sont répertoriées dans la page [Description de produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Vous pouvez vérifier le nombre de profils engageables dans le [tableau de bord de l’utilisation des licences](../audience/license-usage.md).

Pour que vos profils engageables restent dans des limites raisonnables, Adobe recommande de définir une durée de vie (TTL) pour supprimer automatiquement les profils pseudonymes du profil client en temps réel s’ils n’ont pas été vus ou engagés dans une fenêtre temporelle spécifique.

>[!NOTE]
>
>Découvrez comment configurer l’expiration des données pour les profils pseudonymes dans la documentation d’[Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

Adobe recommande de définir la valeur de durée de vie sur 14 jours pour correspondre à la durée de vie actuelle du profil Edge.
