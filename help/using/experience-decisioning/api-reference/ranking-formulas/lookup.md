---
title: Rechercher une formule de classement
description: Les formules de classement permettent de définir les fonctions de notation utilisées pour classer les éléments.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f048b2d1-d26b-4987-8acb-3558df506ec2
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
workflow-type: ht
source-wordcount: '80'
ht-degree: 100%

---

# Rechercher  {#list-ranking-formula}

Vous pouvez rechercher une formule de classement spécifique en effectuant une requête GET sur l’API Bibliothèque des offres qui inclut l’ID dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez rechercher. | `rankingFormula1234` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse renvoie les détails de la formule de classement.

```json
{
    "created": "2024-08-08T23:45:15.380Z",
    "modified": "2024-10-22T18:15:05.909Z",
    "etag": 36,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/ranking-function"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:ranking-function:1947f5372cc4ed74",
    "name": "[Do not delete] - Cypress e2e - edit",
    "description": "some description",
    "returnType": {
        "type": "INTEGER"
    },
    "exdFunction": true,
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "42 = 11"
    }
}
```
