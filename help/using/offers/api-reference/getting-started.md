---
title: Prise en main
description: Découvrez comment commencer à utiliser l’API de la bibliothèque des offres pour effectuer des opérations essentielles à l’aide du moteur de décisions.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 100%

---

# Guide du développeur de l&#39;API de gestion des décisions {#decision-management-api-developer-guide}

Ce guide du développeur décrit les étapes à suivre pour commencer à utiliser l&#39;API [!DNL Offer Library]. Le guide fournit ensuite des exemples d’appels d’API pour effectuer des opérations clés à l’aide du moteur de décisions.

➡️ [En savoir plus sur les composants de la gestion des décisions dans cette vidéo](#video)

## Conditions préalables {#prerequisites}

Ce guide nécessite une compréhension professionnelle des composants suivants d&#39;Adobe Experience Platform :

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;} : cadre normalisé selon lequel [!DNL Experience Platform] organise les données de l’expérience client.
   * [Notions de base sur la composition du schéma](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr){target=&quot;_blank&quot;} : en savoir plus sur les blocs de création de base des schémas XDM.
* [Gestion des décisions](../../../using/offers/get-started/starting-offer-decisioning.md) : explique les concepts et les composants utilisés pour la prise de décision basée sur l’expérience en général et la gestion des décisions en particulier. Illustre les stratégies utilisées pour choisir la meilleure option à présenter lors de l&#39;expérience client.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr){target=&quot;_blank&quot;} : PQL est un langage puissant pour écrire des expressions sur des instances XDM. PQL est utilisé pour définir des règles de décision.

## Lecture d&#39;exemples d&#39;appels API {#reading-sample-api-calls}

Ce guide fournit des exemples d’appels API pour démontrer comment formater vos requêtes. Il s’agit notamment de chemins d’accès, d’en-têtes requis et de payloads de requêtes correctement formatés. L’exemple JSON renvoyé dans les réponses de l’API est également fourni. Pour plus d&#39;informations sur les conventions utilisées dans la documentation pour les exemples d&#39;appels d&#39;API, voir la section concernant la [lecture d&#39;exemples d&#39;appels d&#39;API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=fr#how-do-i-format-an-api-request){target=&quot;_blank&quot;} dans le guide de dépannage [!DNL Experience Platform].

## Collecte des valeurs des en-têtes requis {#gather-values-for-required-headers}

Pour effectuer des appels aux API [!DNL Adobe Experience Platform], vous devez d&#39;abord suivre le [tutoriel d&#39;authentification](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=fr){target=&quot;_blank&quot;} Le tutoriel d&#39;authentification fournit les valeurs de chacun des en-têtes requis dans tous les appels d&#39;API [!DNL Experience Platform], comme indiqué ci-dessous :

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Toutes les requêtes contenant une payload (POST, PUT, PATCH) requièrent un en-tête supplémentaire :

* `Content-Type: application/json`

## Gérer l&#39;accès à un conteneur {#manage-access-to-container}

Un conteneur est un mécanisme d&#39;isolement qui permet de séparer différentes préoccupations. L&#39;ID de conteneur est le premier élément de chemin d&#39;accès pour toutes les API du référentiel. Tous les objets de prise de décision résident dans un conteneur.

Un administrateur peut regrouper des entités principales, des ressources et des autorisations d&#39;accès similaires dans des profils. La charge de gestion est ainsi réduite et est assurée par l&#39;[Adobe Admin Console](https://adminconsole.adobe.com/). Pour créer des profils et leur affecter des utilisateurs, vous devez être un administrateur de produit pour Adobe Experience Platform. Il suffit de créer des profils de produit qui correspondent à certaines autorisations en une seule étape, puis d&#39;ajouter des utilisateurs à ces profils. Les profils agissent comme des groupes ayant reçu des autorisations, et chaque utilisateur réel ou technique de ce groupe hérite de ces autorisations.

Avec les privilèges d&#39;administrateur, vous pouvez accorder ou retirer des autorisations aux utilisateurs via l‘[Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Pour plus d&#39;informations, voir la [présentation du contrôle d&#39;accès](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=fr){target=&quot;_blank&quot;}

### Liste des conteneurs accessibles aux utilisateurs et aux intégrations {#list-containers-accessible-to-users-and-integrations}

**Format d&#39;API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtre la liste des conteneurs par leur association aux contextes de produits. | `acp` |
| `{PROPERTY}` | Filtre le type de conteneur renvoyé. | `_instance.containerType==decisioning` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse positive renvoie des informations concernant les conteneurs de gestion de décision. Elle inclut un attribut `instanceId` dont la valeur est votre identifiant de conteneur.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Étapes suivantes {#next-steps}

Ce document couvrait les connaissances préalables requises pour effectuer des appels à l&#39;API [!DNL Offer Library], y compris l&#39;acquisition de votre ID de conteneur. Vous pouvez désormais procéder aux exemples d&#39;appel fournis dans ce guide de développement et suivre leurs instructions.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Vidéo pratique {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de gestion des décisions.


>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

