---
title: Liste des règles d’éligibilité
description: Les règles d’éligibilité permettent de définir les candidats éligibles en fonction de ce que vous souhaitez cibler, comme les attributs de profil et les audiences.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: c8f88954-a721-4d18-9137-035ee9dc1bcf
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 100%

---

# Liste des règles d’éligibilité {#list-eligibilit-rules}

Une règle d’éligibilité se compose d’une expression de règle PQL qui définit la manière dont elle doit définir l’éligibilité.

Vous pouvez afficher une liste de toutes les règles d’éligibilité en effectuant une seule requête GET sur l’API Bibliothèque des offres.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdRule. | `property=exdRule%3D%3Dtrue` |

## Utiliser des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `property` | Un filtre de propriété facultatif : <ul><li>Les propriétés sont regroupées par opération AND.</li><li>Les paramètres peuvent être répétés comme suit : property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] ou property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Les expressions de propriété sont au format `[!]field[op]value`, avec `op` dans `[==,!=,<=,>=,<,>,~]`, prenant en charge les expressions régulières.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitez le nombre d’entitées renvoyées. | `limit=5` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?property=exdRule%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse renvoie une liste de règles d’éligibilité auxquelles vous avez accès.

```json
{
    "results": [
        {
            "created": "2024-10-28T01:18:08.506Z",
            "modified": "2024-10-28T01:18:08.506Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19af09a9ae45a8d3",
            "name": "dasdsa",
            "description": "",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "dasdsa",
                "namespace": "ups"
            }
        },
        {
            "created": "2024-10-27T04:01:29.343Z",
            "modified": "2024-10-27T04:33:44.781Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19ade575cf95e584",
            "name": "nick test pes",
            "description": "dasdsad",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "dasdsad",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "nick test pes",
                "namespace": "ups",
                "estimates": [
                    {
                        "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                        "addressabilityText": "Of total",
                        "color": "#12805c",
                        "estimateData": {
                            "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                            "estimatedSize": 0,
                            "totalRows": 62088,
                            "percent": 0,
                            "standardError": 0,
                            "confidenceInterval": "95%",
                            "state": "RESULT_READY",
                            "profilesReadSoFar": 62088,
                            "numRowsToRead": 62088
                        },
                        "state": "RESULT_READY"
                    }
                ]
            }
        }
    ],
    "count": 2,
    "total": 229,
    "_links": {
        "self": {
            "href": "/offer-rules?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?orderby=-modified&limit=2&start=2024-10-27T01:24:51.785Z",
            "type": "application/json"
        }
    }
}
```
