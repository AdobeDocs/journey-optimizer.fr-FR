---
title: Rechercher une règle d’éligibilité
description: Les règles d’éligibilité permettent de définir les candidats éligibles en fonction de ce que vous souhaitez cibler, comme les attributs de profil et les audiences.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: a74f4c87-0b89-4583-97f5-df8e2a30a19b
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 100%

---

# Rechercher une règle d’éligibilité {#list-eligibility-rule}

Vous pouvez rechercher une règle d’éligibilité spécifique en effectuant une requête GET sur l’API Bibliothèque des offres qui inclut l’ID dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez rechercher. | `rule1234` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse renvoie les détails de la règle d’éligibilité.

```json
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
    "exdRule": false,
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
}
```
