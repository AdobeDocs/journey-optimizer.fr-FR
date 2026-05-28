---
title: Mettre à jour une collection d’éléments
description: Les collections sont des sous-ensembles d’offres basés sur des conditions prédéfinies établies par des responsables marketing, telles que la catégorie de l’offre.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: a2b7779d-8c2e-4ff9-8cc3-90846f100c98
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qYudO0NFgw9zjq843wK8zVMwr-nk29HPdXAHLBUc7qg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# Mettre à jour une collection d’éléments {#update-item-collection}

Vous pouvez modifier ou mettre à jour une collection d’éléments en adressant une requête PATCH à l’API Bibliothèque des offres.

Pour plus d’informations sur JSON Patch, notamment les opérations disponibles, consultez la [documentation JSON Patch](https://jsonpatch.com/) officielle.

**Format d’API**

```http
PATCH /{ENDPOINT_PATH}/item-collections/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez mettre à jour. | `itemCollections1234` |

**Requête**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated item collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated item collection description"
    }
]'
```

| Paramètre | Description |
| --------- | ----------- |
| `value` | Nouvelle valeur avec laquelle vous souhaitez mettre à jour votre paramètre. |
| `path` | Chemin d’accès du paramètre à mettre à jour. |
| `op` | Appel d’opération utilisé pour définir l’action nécessaire pour mettre à jour la connexion. Les opérations comprennent : `add`, `replace`, `remove`, `copy` et `test`. |

**Réponse**

Une réponse réussie renvoie les détails mis à jour de la collection d’éléments, y compris son `id`.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
