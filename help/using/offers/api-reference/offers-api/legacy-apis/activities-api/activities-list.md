---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Création de listes de décisions
description: Une décision contient la logique qui sous-tend la sélection d’une offre.
feature: Decision Management, API
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: e9bd7602-8945-4768-8a56-dc13ade32a0b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-QsG7rzICxULvvVarkve6ZfwjxJP6fpdocdnmlEynso
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 100%

---

# Création de listes de décisions {#list-decisions}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../../../../experience-decisioning/gs-experience-decisioning.md)


Une décision contient la logique qui sous-tend la sélection d’une offre.

Vous pouvez afficher une liste de toutes les décisions au sein d&#39;un conteneur en exécutant une seule requête GET sur l&#39;API [!DNL Offer Library].

**Format d’API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | Définit le schéma associé aux décisions. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=2` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `q` | Chaîne de requête facultative à rechercher dans les champs sélectionnés. La chaîne de requête doit être en minuscules et peut être entourée de guillemets doubles pour l&#39;empêcher d&#39;être divisée en symboles et pour échapper les caractères spéciaux. Les caractères `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` ont une signification spéciale et doivent être précédés d&#39;une barre oblique inverse lorsqu&#39;ils apparaissent dans la chaîne de requête. | `default` |
| `qop` | Applique l&#39;opérateur ET ou OU aux valeurs du paramètre de chaîne de requête q. | `AND` / `OR` |
| `field` | Liste facultative des champs à laquelle limiter la recherche. Ce paramètre peut être répété comme suit : field=field1[,field=field2,...] et (les expressions du chemin se présentent sous la forme de chemins séparés par des points, tels que _instance.xdm::name). | `_instance.xdm:name` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un `-` devant le titre (`orderby=-title`) trie les éléments par titre dans l’ordre décroissant (Z-A). | `-repo:createdDate` |
| `limit` | Limite le nombre de décisions renvoyées. | `limit=5` |

**Réponse**

Une réponse positive renvoie une liste des décisions présentes dans le conteneur auquel vous avez accès.

```json
{
    "results": [
        {
            "created": "2022-07-05T09:02:02.835+00:00",
            "modified": "2022-08-16T21:40:58.573+00:00",
            "etag": 12,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision1234",
            "name": "Test Decision One",
            "status": "live",
            "startDate": "2022-05-18T00:09:57.706+00:00",
            "endDate": "2032-08-13T21:40:58.235+00:00",
            "fallback": "fallbackOffer1234",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234",
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 0,
                        "order": {
                            "orderEvaluationType": "ranking-strategy",
                            "rankingStrategy": "123456789123"
                        }
                    },
                    "profileConstraint": {
                        "profileConstraintType": "none"
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }
            ]
        },
        {
            "created": "2022-09-05T14:12:13.773+00:00",
            "modified": "2022-09-05T14:12:13.773+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision5678",
            "name": "Test Decision Two",
            "status": "live",
            "startDate": "2022-08-31T21:00:00.000+00:00",
            "endDate": "2023-02-03T22:00:00.000+00:00",
            "fallback": "fallbackOffer5678",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234"
                    ],
                    "rank": {
                        "priority": 2
                    },
                    "optionSelection": {
                        "filter": "offerCollection5678"
                    }
                },
                {
                    "placements": [
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 1
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }          
            ]
        }
    ],
    "count": 2,
    "total": 21,
    "_links": {
        "self": {
            "href": "/offer-decisions?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-decisions?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
