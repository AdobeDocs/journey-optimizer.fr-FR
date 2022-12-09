---
title: Prise en main
description: Découvrez comment commencer à utiliser l’API de la bibliothèque des offres pour effectuer des opérations clés à l’aide du moteur de prise de décision.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Guide de développement de l’API Decision Management {#decision-management-api-developer-guide}

Ce guide de développement décrit les étapes à suivre pour vous aider à commencer à utiliser le [!DNL Offer Library] API. Le guide fournit ensuite des exemples d’appels API pour effectuer des opérations clés à l’aide du moteur de prise de décision.

➡️ [En savoir plus sur les composants de la gestion de la décision dans cette vidéo](#video)

## Conditions préalables {#prerequisites}

Ce guide nécessite une compréhension pratique des composants suivants d’Adobe Experience Platform :

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;} : Le cadre normalisé selon lequel [!DNL Experience Platform] organise les données d’expérience client.
   * [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html){target=&quot;_blank&quot;} : Découvrez les blocs de création de base des schémas XDM.
* [Gestion des décisions](../../../using/offers/get-started/starting-offer-decisioning.md): Explique les concepts et les composants utilisés pour la prise de décision basée sur l’expérience en général et la gestion de la décision en particulier. Illustre les stratégies utilisées pour choisir la meilleure option à présenter lors de l’expérience d’un client.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;} : PQL est un langage puissant pour écrire des expressions sur des instances XDM. PQL est utilisé pour définir des règles de décision.

## Lecture d’exemples d’appels API {#reading-sample-api-calls}

Ce guide fournit des exemples d’appels API pour démontrer comment formater vos requêtes. Il s’agit notamment des chemins d’accès, des en-têtes requis et des payloads de requête correctement formatés. L’exemple JSON renvoyé dans les réponses de l’API est également fourni. Pour plus d’informations sur les conventions utilisées dans la documentation pour les exemples d’appels API, consultez la section sur [lecture d’exemples d’appels API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;} dans la variable [!DNL Experience Platform] guide de dépannage.

## Collecte de valeurs pour les en-têtes requis {#gather-values-for-required-headers}

Pour lancer des appels à [!DNL Adobe Experience Platform] API, vous devez d’abord renseigner la variable [tutoriel sur l’authentification](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}. Le tutoriel sur l’authentification indique les valeurs de chacun des en-têtes requis dans tous les [!DNL Experience Platform] Appels API, comme illustré ci-dessous :

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Toutes les requêtes contenant un payload (POST, PUT, PATCH) nécessitent un en-tête supplémentaire :

* `Content-Type: application/json`

## Gérer l’accès à un conteneur {#manage-access-to-container}

Un conteneur est un mécanisme d’isolation qui permet de séparer différentes préoccupations. L’ID de conteneur est le premier élément de chemin d’accès pour toutes les API de référentiel. Tous les objets de prise de décision résident dans un conteneur.

Un administrateur peut regrouper des entités de sécurité, des ressources et des autorisations d’accès similaires dans des profils. Cela réduit la charge de gestion et est pris en charge par [Adobe Admin Console](https://adminconsole.adobe.com/). Pour créer des profils et leur affecter des utilisateurs, vous devez être un administrateur de produit pour Adobe Experience Platform dans votre entreprise. Il suffit de créer des profils de produit qui correspondent à certaines autorisations en une seule étape, puis d’ajouter simplement des utilisateurs à ces profils. Les profils agissent comme des groupes auxquels des autorisations ont été accordées et chaque utilisateur réel ou technique de ce groupe hérite de ces autorisations.

Avec les privilèges d’administrateur, vous pouvez accorder ou retirer des autorisations aux utilisateurs via le [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Pour plus d’informations, voir [Présentation du contrôle d’accès](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html){target=&quot;_blank&quot;}.

### Conteneurs de liste accessibles aux utilisateurs et aux intégrations {#list-containers-accessible-to-users-and-integrations}

**Format d’API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtre la liste des conteneurs en fonction de leur association aux contextes de produit. | `acp` |
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

Une réponse réussie renvoie des informations concernant les conteneurs de gestion de décision. Cela inclut une `instanceId` , dont la valeur est votre ID de conteneur.

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

Ce document couvrait les connaissances préalables requises pour effectuer des appels à la fonction [!DNL Offer Library] API, notamment l’acquisition de votre ID de conteneur. Vous pouvez maintenant passer aux exemples d’appels fournis dans ce guide de développement et suivre leurs instructions.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Vidéo pratique {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de la gestion des décisions.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

