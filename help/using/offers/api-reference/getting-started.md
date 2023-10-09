---
title: Prise en main
description: Découvrez comment commencer à utiliser l’API de la bibliothèque des offres pour effectuer des opérations essentielles à l’aide du moteur de décisions.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 7e9984aee1eba29a2757b025ca0aa1092d95a761
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 93%

---

# Guide du développeur de l&#39;API de gestion des décisions {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Nouvelles API de gestion de décision"
>abstract="De nouvelles API pour la création et la gestion d’objets de gestion de décision sont désormais disponibles. Les api héritées seront prises en charge jusqu’au 03/27/2024."

Ce guide du développeur décrit les étapes à suivre pour commencer à utiliser l&#39;API [!DNL Offer Library]. Le guide fournit ensuite des exemples d’appels d’API pour effectuer des opérations clés à l’aide du moteur de décisions.

➡️ [En savoir plus sur les composants de la gestion des décisions dans cette vidéo](#video)

## Conditions préalables {#prerequisites}

Ce guide nécessite une compréhension professionnelle des composants suivants d&#39;Adobe Experience Platform :

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"} : cadre normalisé selon lequel [!DNL Experience Platform] organise les données de l’expérience client.
   * [Notions de base de la composition du schéma](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr){target="_blank"} : en savoir plus sur les blocs de création de base des schémas XDM.
* [Gestion des décisions](../../../using/offers/get-started/starting-offer-decisioning.md) : explique les concepts et les composants utilisés pour la prise de décision basée sur l’expérience en général et la gestion des décisions en particulier. Illustre les stratégies utilisées pour choisir la meilleure option à présenter lors de l&#39;expérience client.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr){target="_blank"} : PQL est un langage puissant pour écrire des expressions sur des instances XDM. PQL est utilisé pour définir des règles de décision.

## Lecture d&#39;exemples d&#39;appels API {#reading-sample-api-calls}

Ce guide fournit des exemples d’appels API pour démontrer comment formater vos requêtes. Il s’agit notamment de chemins d’accès, d’en-têtes requis et de payloads de requêtes correctement formatés. L’exemple JSON renvoyé dans les réponses de l’API est également fourni. Pour plus d’informations sur les conventions utilisées dans la documentation pour les exemples d’appels d’API, voir la section concernant la [lecture d’exemples d’appels d’API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=fr#how-do-i-format-an-api-request){target="_blank"} dans le guide de dépannage [!DNL Experience Platform].

## Collecter des valeurs pour les en-têtes requis {#gather-values-for-required-headers}

Pour lancer des appels aux API [!DNL Adobe Experience Platform], vous devez d’abord suivre le [tutoriel d’authentification](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=fr){target="_blank"}. Le tutoriel d&#39;authentification fournit les valeurs de chacun des en-têtes requis dans tous les appels d&#39;API [!DNL Experience Platform], comme indiqué ci-dessous :

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Toutes les requêtes contenant une payload (POST, PUT, PATCH) requièrent un en-tête supplémentaire :

* `Content-Type: application/json`

## Étapes suivantes {#next-steps}

Dans ce document, vous avez découvert les connaissances préalables requises pour effectuer des appels vers l’API [!DNL Offer Library]. Vous pouvez désormais procéder aux exemples d&#39;appel fournis dans ce guide de développement et suivre leurs instructions.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Vidéo pratique {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de gestion des décisions.


>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

