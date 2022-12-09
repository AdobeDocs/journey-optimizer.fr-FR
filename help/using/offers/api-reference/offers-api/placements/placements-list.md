---
title: Lister des emplacements
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Lister des emplacements {#list-placements}

Les emplacements sont des conteneurs utilisés pour présenter vos offres. Un emplacement permet de s’assurer que le contenu d’offre approprié s’affiche au bon endroit dans votre message. Lorsque vous ajoutez du contenu à une offre, vous serez invité à sélectionner un emplacement dans lequel ce contenu peut être affiché.

Vous pouvez afficher une liste de tous les emplacements d’un conteneur en adressant une seule requête GET à la variable [!DNL Offer Library] API.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les emplacements. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Définit le schéma associé aux emplacements. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs pour filtrer les résultats. | `limit=2` |

## Utilisation des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour page et filtrer les résultats lors de la mise en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `q` | Chaîne de requête facultative à rechercher dans les champs sélectionnés. La chaîne de requête doit être en minuscules et peut être entourée de guillemets doubles pour l’empêcher d’être segmentée en unités lexicales et pour échapper les caractères spéciaux. Les caractères `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` ont une signification spéciale et doivent être précédés d’une barre oblique inverse lorsqu’ils apparaissent dans la chaîne de requête. | JSON du site Web |
| `qop` | Applique l’opérateur ET ou OU aux valeurs du paramètre de chaîne de requête q. | `AND` / `OR` |
| `field` | Liste facultative des champs à laquelle limiter la recherche. Ce paramètre peut être répété comme suit : field=field1[,champ=champ2,...] et (les expressions de chemin se présentent sous la forme de chemins séparés par des points, tels que _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Triez les résultats selon une propriété spécifique. Ajouter un `-` avant le titre (`orderby=-title`) triera les éléments par titre dans l’ordre décroissant (Z-A). | `-repo:createdDate` |
| `limit` | Limitez le nombre d’emplacements renvoyés. | `limit=5` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie une liste d’emplacements présents dans le conteneur auquel vous avez accès.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2020-10-21T19:48:51.843067Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2020-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            },
            {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2020-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
