---
title: Liste des offres de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: dd95c040-d905-4f5a-8cc5-58e39082e57e
source-git-commit: bee5e067e70e065c9db14448c42224a9ec09c5bf
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 48%

---

# Liste des offres de secours {#list-fallback-offers}

Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.. Les étapes de création d&#39;une offre de secours consistent à créer une ou plusieurs représentations, comme lors de la création d&#39;une offre.

Vous pouvez afficher une liste de toutes les offres de secours en adressant une seule requête de GET au [!DNL Offer Library] API.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=fallback&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=2` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=fallback&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Utilisation des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `property` | Un filtre de propriété facultatif : <ul><li> Les propriétés sont regroupées par opération ET. <br><br> - Les paramètres peuvent être répétés comme suit : property=`<property-expr>`[&amp;property=`<property-expr2>`..] ou property=`<property-expr1>`[&amp;`<property-expr2>`..] <br><br> - Les expressions de propriété sont au format `[!]field[op]` value, avec op in `[==,!=,'<=',>=,<,>,~]`, prise en charge des expressions régulières  </li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitez le nombre d’entités renvoyées. | `limit=5` |

**Réponse**

Une réponse réussie renvoie une liste d’offres de secours auxquelles vous avez accès.

```json
{
      "results": [
        {
            "created": "2023-06-08T14:04:41.011+00:00",
            "modified": "2023-06-08T14:04:41.011+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "fallbackOffer1234",
            "name": "Fallback Offer Web",
            "description": "Fallback Offer Web Description",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement5678",
                    "components": [
                        {
                            "type": "imagelink",
                            "format": "image/png",
                            "deliveryURL": "https://mysite.com"
                        }
                    ]
                }
            ]
        },
        {
            "created": "2022-10-07T11:23:55.885+00:00",
            "modified": "2022-10-07T11:23:55.885+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.7"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "fallbackOffer5678",
            "name": "Fallback Offer email",
            "status": "approved",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/email",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "component-text",
                            "format": "text/template",
                            "content": "Get free shipping!"
                        }
                    ]
                }
            ],
            "labels": [
                "core/C1"
            ]
        }
    ],
    "count": 2,
    "total": 3,
    "_links": {
        "self": {
            "href": "/offers?offer-type=fallback&href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offers?offer-type=fallback&href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
