---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Liste des collections
description: Les collections sont des sous-ensembles d’offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l’offre.
feature: Decision Management, API, Collections
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: ce39d77d-6d81-48d7-9e73-e1d537874018
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%

---

# Liste des collections {#list-collections}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)


Les collections sont des sous-ensembles d’offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l’offre.

Vous pouvez afficher une liste de toutes les collections au sein d’un conteneur en adressant une seule requête GET à l’API [!DNL Offer Library].

**Format d’API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=2` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les collections. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | Définit le schéma associé aux collections. <https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1> |  |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=1` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Utiliser des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `q` | Chaîne de requête facultative à rechercher dans les champs sélectionnés. La chaîne de requête doit être en minuscules et peut être entourée de guillemets doubles pour l&#39;empêcher d&#39;être divisée en symboles et pour échapper les caractères spéciaux. Les caractères `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` ont une signification spéciale et doivent être précédés d&#39;une barre oblique inverse lorsqu&#39;ils apparaissent dans la chaîne de requête. | `demo collection` |
| `qop` | Applique l&#39;opérateur ET ou OU aux valeurs du paramètre de chaîne de requête q. | `AND` / `OR` |
| `field` | Liste facultative des champs à laquelle limiter la recherche. Ce paramètre peut être répété comme suit : field=field1[,field=field2,...] et (les expressions du chemin se présentent sous la forme de chemins séparés par des points, tels que _instance.xdm::name). | `_instance.xdm:name` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un `-` devant le titre (`orderby=-title`) trie les éléments par titre dans l’ordre décroissant (Z-A). | `-repo:createdDate` |
| `limit` | Limitez le nombre de collections renvoyées. | `limit=5` |

**Réponse**

Une réponse positive renvoie une liste de collections présentes dans le conteneur auquel vous avez accès.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2023-10-21T21:14:19.282175Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2023-10-20T02:37:11.263718Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:tag:124bd3de7f598dd8"
                    ],
                    "xdm:name": "Mobile Demo",
                    "xdm:filterType": "anyTags",
                    "@id": "xcore:offer-filter:124bd44648f17ec1"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-09-17T14:36:29.272451Z",
                "repo:lastModifiedDate": "2023-09-17T14:36:29.272451Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:personalized-offer:1221fbedfa4d98b0"
                    ],
                    "xdm:name": "demo collection",
                    "xdm:filterType": "offers",
                    "@id": "xcore:offer-filter:1221fc71c74d98b4"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 8,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
