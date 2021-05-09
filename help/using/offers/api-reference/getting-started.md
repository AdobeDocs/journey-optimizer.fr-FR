---
title: Prise en main
description: Découvrez comment début à l’aide de l’API de la bibliothèque d’Offres pour effectuer des opérations clés à l’aide du moteur de gestion des décisions.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Guide du développeur de l’API de gestion des décisions

Ce guide du développeur décrit les étapes à suivre pour vous aider à début à l&#39;aide de l&#39;API [!DNL Offer Library]. Le guide fournit ensuite des exemples d’appels d’API pour effectuer des opérations clés à l’aide du moteur de gestion des décisions.

![](../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité dans la vidéo](#video)

## Conditions préalables

Ce guide nécessite une compréhension pratique des composants suivants de Adobe Experience Platform :

* [[!DNL Experience Data Model (XDM) System]](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html): Cadre normalisé selon lequel  [!DNL Experience Platform] organiser les données d’expérience client.
   * [Principes de base de la composition](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) des schémas : Découvrez les éléments de base des schémas XDM.
* [Gestion des](../../../using/offers/get-started/starting-offer-decisioning.md) décisions : Explique les concepts et les composants utilisés pour la prise de décision d’expérience en général et en particulier l’Offer decisioning. Illustre les stratégies utilisées pour choisir la meilleure option à présenter lors de l’expérience d’un client.
* [[!DNL Profile Query Language (PQL)]](https://docs.adobe.com/content/help/en/experience-platform/segmentation/pql/overview.html): PQL est un langage puissant pour écrire des expressions sur des instances XDM. PQL est utilisé pour définir des règles de décision.

## Lecture des exemples d’appels d’API

Ce guide fournit des exemples d’appels d’API pour montrer comment formater vos requêtes. Il s’agit notamment des chemins d’accès, des en-têtes requis et des charges de requête correctement formatées. L’exemple JSON renvoyé dans les réponses de l’API est également fourni. Pour plus d&#39;informations sur les conventions utilisées dans la documentation pour les exemples d&#39;appels d&#39;API, consultez la section [comment lire des exemples d&#39;appels d&#39;API](https://docs.adobe.com/content/help/en/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request) dans le guide de dépannage [!DNL Experience Platform].

## Rassembler les valeurs des en-têtes requis

Pour appeler les API [!DNL Platform], vous devez d&#39;abord suivre le didacticiel d&#39;authentification [](https://docs.adobe.com/content/help/en/experience-platform/tutorials/authentication.html). Le didacticiel d&#39;authentification fournit les valeurs de chacun des en-têtes requis dans tous les appels d&#39;API [!DNL Experience Platform], comme indiqué ci-dessous :

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Toutes les requêtes qui contiennent une charge utile (POST, PUT, PATCH) nécessitent un en-tête supplémentaire :

* `Content-Type: application/json`

## Gérer l’accès à un conteneur

Un conteneur est un mécanisme d&#39;isolation qui permet de séparer les différentes préoccupations. L’ID de conteneur est le premier élément de chemin d’accès pour toutes les API du référentiel. Tous les objets de prise de décision résident dans un conteneur.

Un administrateur peut regrouper des entités principales, des ressources et des autorisations d’accès similaires dans des profils. Cela réduit la charge de gestion et est pris en charge par [Adobe Admin Console](https://adminconsole.adobe.com/). Pour créer des profils et y affecter des utilisateurs, vous devez être un administrateur de produit pour Adobe Experience Platform. Il suffit de créer des profils de produits qui correspondent à certaines autorisations en une seule étape, puis d’ajouter simplement des utilisateurs à ces profils. Les profils agissent comme des groupes auxquels des autorisations ont été accordées et chaque utilisateur réel ou technique de ce groupe hérite de ces autorisations.

Avec les privilèges d’administrateur, vous pouvez accorder ou retirer des autorisations aux utilisateurs par l’intermédiaire du [Adobe Admin Console](https://adminconsole.adobe.com/). Pour plus d&#39;informations, consultez la [présentation du Contrôle d&#39;accès](https://docs.adobe.com/content/help/en/experience-platform/access-control/home.html).

### Conteneurs de liste accessibles aux utilisateurs et aux intégrations

**Format d’API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtres la liste des conteneurs par leur association aux contextes de produits. | `acp` |
| `{PROPERTY}` | Filtres le type de conteneur renvoyé. | `_instance.containerType==decisioning` |

**Demande**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse positive renvoie des informations concernant les conteneurs de gestion des décisions. Ceci inclut un attribut `instanceId` dont la valeur est votre identifiant de conteneur.

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

## Étapes suivantes

Ce document couvrait les connaissances préalables requises pour effectuer des appels à l&#39;API [!DNL Offer Library], y compris l&#39;acquisition de votre ID de conteneur. Vous pouvez maintenant passer aux exemples d’appels fournis dans ce guide du développeur et suivre leurs instructions.

## Vidéo didactique {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de la gestion des décisions.

>[!NOTE]
>
>Cette vidéo s’applique au service d’applications d’Offer decisioning créé sur Adobe Experience Platform. Toutefois, il fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
