---
title: Rechercher une stratégie de sélection
description: Les stratégies de sélection se composent de collections associées à des contraintes et à des méthodes de classement pour déterminer les offres.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: db590963-b45b-4844-ac12-775cc955b03e
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: ht
source-wordcount: '81'
ht-degree: 100%

---

# Rechercher une stratégie de sélection {#list-selection-strategy}

Vous pouvez rechercher une stratégie de sélection spécifique en adressant une requête GET à l’API Bibliothèque des offres qui inclut l’identifiant dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez rechercher. | `selectionStrategy1234` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie les détails de la stratégie de sélection.

```json
{
    "created": "2024-02-08T03:01:50.924Z",
    "modified": "2024-02-16T23:03:03.019Z",
    "etag": 4,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "selectionStrategy1234",
    "name": "Selection Strategy One",
    "description": "Selection Strategy",
    "rank": {
        "priority": 1,
        "order": {
            "orderEvaluationType": "static"
        }
    },
    "profileConstraint": {
        "profileConstraintType": "eligibilityRule",
        "eligibilityRule": "offerRule1234"
    },
    "optionSelection": {
        "filter": "itemCollection1234",
    }
}
```
