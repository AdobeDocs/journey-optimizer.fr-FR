---
title: Liste des offres personnalisées
description: Une offre personnalisée est un message marketing personnalisable basé sur des règles et des contraintes d’éligibilité.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 45d51918-1106-4b6b-b383-8ab4d9a4f7af
source-git-commit: b3fed5a48480647010f59fa471c505b4031b8701
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 72%

---


# Liste des offres personnalisées {#list-personalized-offers}

Une offre personnalisée est un message marketing personnalisable basé sur des règles et des contraintes d’éligibilité.

Vous pouvez afficher une liste de toutes les offres personnalisées en adressant une seule requête GET à l’API [!DNL Offer Library].

**Format d’API**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=personalized&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=2` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized&limit=2' \
-H 'Accept: *,application/json' \
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
| `property` | Un filtre de propriété facultatif : <ul><li>Les propriétés sont regroupées par opération AND.</li><li>Les paramètres peuvent être répétés comme suit : property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] ou property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...].</li><li>Les expressions de propriété sont au format `[!]field[op]value`, avec `op` dans `[==,!=,<=,>=,<,>,~]`, prenant en charge les expressions régulières.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitez le nombre d’emplacements renvoyés. | `limit=5` |

**Réponse**

Une réponse réussie renvoie une liste d’offres personnalisées présentes aux côtés de celles auxquelles vous avez accès.

```json
{
    "results": [
        {
            "created": "2023-05-15T14:35:16.781+00:00",
            "modified": "2023-05-15T14:38:26.691+00:00",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "personalizedOffer1234",
            "name": "Test personalized offer with frequency constraint",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "html",
                            "format": "text/html",
                            "language": [
                                "en-us"
                            ],
                            "content": "Hello You qualify for our Discount of 60%"
                        }
                    ]
                }
            ],
            "selectionConstraint": {
                "startDate": "2022-07-27T05:00:00.000+00:00",
                "endDate": "2023-07-29T05:00:00.000+00:00",
                "profileConstraintType": "none"
            },
            "rank": {
                "priority": 0
            },
            "cappingConstraint": {},
            "frequencyCappingConstraints": [
                {
                    "enabled": false,
                    "limit": 1,
                    "startDate": "2023-05-15T14:25:49.622+00:00",
                    "endDate": "2023-05-25T14:25:49.622+00:00",
                    "scope": "global",
                    "entity": "offer",
                    "repeat": {
                        "enabled": false,
                        "unit": "month",
                        "unitCount": 1
                    }
                }
            ]
        }
    ],
    "count": 1,
    "total": 1,
    "_links": {
        "self": {
            "href": "/offers?offer-type=personalized&href={SELF_HREF}",
            "type": "application/json"
        }
    }
}
```

Effectuez la pagination si plusieurs offres personnalisées sont manquantes dans la réponse.

**Réponse**

```json
{
    "results": [...],
    "count": 2,
    "total": 43,
    "_links": {
        "self": {
        "href": "/offers?orderby=-modified&limit=2&offer-type=PERSONALIZED",
        "type": "application/json"
        },
        "next": {
        "href": "/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED",
        "type": "application/json"
        }
    }
    }
```

| Mesure | Description |
|---------|-------------|
| `total` | Nombre d’offres personnalisées. |
| `count` | Nombre d’offres renvoyées dans cette réponse. |

Récupérez le point d’entrée d’`_links.next.href` tels que `/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED` et ajoutez-le à l’API.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED
```

```json
{
    "results": [...],
    "count": 2,
    "total": 43,
    "_links": {
        "self": {...},
        "next": {
        "href": "/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED",
        "type": "application/json"
        }
    }
}
```

De même, si vous n’êtes pas sur la première page et que vous devez récupérer la page précédente des offres personnalisées, utilisez la valeur `href` de `_links.prev`. Envoyez une requête à l’URL pour récupérer le jeu de résultats précédent, comme illustré dans l’exemple ci-dessous.

**Réponse**

```json
{
    "results": [...],
    "count": 2,
    "total": 43,
    "_links": {
        "self": {...},
        "next": {...},
        "prev": {
        "href": "/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED",
        "type": "application/json"
        }
    }
}
```
