---
title: Répertorier les décisions
description: Une décision contient la logique sous-tendant la sélection d’une offre.
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: ht
source-wordcount: '155'
ht-degree: 100%

---

# Rechercher une décision

Vous pouvez rechercher des décisions (auparavant « activités d’offre ») spécifiques en exécutant une requête GET sur l’API [!DNL Offer Library] qui inclut les décisions `@id` ou le nom de l’activité dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | Définit le schéma associé aux décisions. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `id` | Chaîne utilisée pour faire correspondre la propriété `@id` des entités. La chaîne correspond exactement. Les paramètres `id` et `name` ne peuvent pas être utilisés ensemble. | `xcore:offer-activity:124527ab00b2ebbc` |
| `name` | Chaîne utilisée pour correspondre à la propriété xdm:name des entités. La chaîne correspond exactement, avec la capitalisation, mais des caractères génériques peuvent être utilisés. Les paramètres « id » et « name » ne peuvent pas être utilisés ensemble. | `LBAR` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie les détails de l’emplacement, y compris les informations sur votre ID de conteneur, l’ID d’instance et l’`@id` de décision unique.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2020-10-19T19:50:08.047489Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-14T22:12:10.300775Z",
                "repo:lastModifiedDate": "2020-10-14T22:12:10.300775Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "LBAR",
                    "xdm:endDate": "2021-02-28T08:00:00.000Z",
                    "xdm:startDate": "2020-10-14T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:124527ab00b2ebbc"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
