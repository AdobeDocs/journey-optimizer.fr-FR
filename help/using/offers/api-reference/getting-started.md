---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Prise en main
description: Découvrez comment commencer à utiliser l’API de la bibliothèque des offres pour effectuer des opérations essentielles à l’aide du moteur de décisions.
badge: label="Hérité" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: ht
source-wordcount: '400'
ht-degree: 100%

---

# Guide de développement de l’API de gestion des décisions {#decision-management-api-developer-guide}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Nouvelles API de gestion des décisions"
>abstract="De nouvelles API pour la création et la gestion d’objets de gestion de décision sont désormais disponibles. Les API héritées seront prises en charge jusqu’au 27/03/2024."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="Nouvelles API de gestion des décisions"
>abstract="De nouvelles API pour la création et la gestion d’objets de gestion de décision sont désormais disponibles. Les API héritées seront prises en charge jusqu’au 27/03/2024."

Ce guide de développement décrit les étapes à suivre pour commencer à utiliser l’API [!DNL Offer Library]. Le guide fournit ensuite des exemples d’appels d’API pour effectuer des opérations clés à l’aide du moteur de décisions.

➡️ [Découvrir les composants de la gestion des décisions dans cette vidéo](#video)

## Conditions préalables {#prerequisites}

Ce guide nécessite une compréhension professionnelle des composants suivants d&#39;Adobe Experience Platform :

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"} : Cadre normalisé selon lequel [!DNL Experience Platform] organise les données de l&#39;expérience client.
   * [Notions de base de la composition du schéma](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr){target="_blank"} : en savoir plus sur les blocs de création de base des schémas XDM.
* [Gestion des décisions](../../../using/offers/get-started/starting-offer-decisioning.md) : explique les concepts et les composants utilisés pour la prise de décision en général et la gestion des décisions en particulier. Illustre les stratégies utilisées pour choisir la meilleure option à présenter lors de l’expérience du client ou de la cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr){target="_blank"} : PQL est un langage puissant pour écrire des expressions sur des instances XDM. PQL est utilisé pour définir des règles de décision.

## Lecture d&#39;exemples d&#39;appels API {#reading-sample-api-calls}

Ce guide fournit des exemples d’appels API pour démontrer comment formater vos requêtes. Il s’agit notamment de chemins d’accès, d’en-têtes requis et de payloads de requêtes correctement formatés. L’exemple JSON renvoyé dans les réponses de l’API est également fourni. Pour plus d’informations sur les conventions utilisées dans la documentation pour les exemples d’appels d’API, voir la section concernant la [lecture d’exemples d’appels d’API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=fr#how-do-i-format-an-api-request){target="_blank"} dans le guide de dépannage [!DNL Experience Platform].

## Collecte des valeurs des en-têtes requis {#gather-values-for-required-headers}

Pour lancer des appels aux API [!DNL Adobe Experience Platform], vous devez d’abord suivre le [tutoriel d’authentification](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=fr){target="_blank"}. Le tutoriel d&#39;authentification fournit les valeurs de chacun des en-têtes requis dans tous les appels d&#39;API [!DNL Experience Platform], comme indiqué ci-dessous :

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Toutes les requêtes contenant une payload (POST, PUT, PATCH) requièrent un en-tête supplémentaire :

* `Content-Type: application/json`

>[!NOTE]
>
>Les vérifications d’autorisations sont appliquées en fonction des profils de produit attribués. Seules les autorisations accordées dans le profil de produit associé déterminent quelles ressources peuvent être accessibles ou gérées via l’API.

## Étapes suivantes {#next-steps}

Dans ce document, vous avez découvert les connaissances préalables requises pour effectuer des appels vers l’API [!DNL Offer Library]. Vous pouvez désormais procéder aux exemples d&#39;appel fournis dans ce guide de développement et suivre leurs instructions.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!-- ## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/342829?captions=fre_fr&quality=12) -->

