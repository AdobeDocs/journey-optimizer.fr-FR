---
title: Mettre à jour des stratégies de sélection
description: Les stratégies de sélection se composent de collections associées à des contraintes et à des méthodes de classement pour déterminer les offres.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 060f8c5f-4750-44dc-83aa-630afbc180eb
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: ht
source-wordcount: '127'
ht-degree: 100%

---

# Mettre à jour une stratégie de sélection {#update-selection-strategy}

Vous pouvez modifier ou mettre à jour une stratégie de sélection en adressant une requête PATCH à l’API Bibliothèque des offres.

Pour plus d’informations sur JSON Patch, notamment les opérations disponibles, consultez la [documentation JSON Patch](https://jsonpatch.com/) officielle.

**Format d’API**

```http
PATCH /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez mettre à jour. | `selectionStrategy1234` |

**Requête**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated selection strategy"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated selection strategy description"
    }
]'
```

| Paramètre | Description |
| --------- | ----------- |
| `value` | Nouvelle valeur avec laquelle vous souhaitez mettre à jour votre paramètre. |
| `path` | Chemin d’accès du paramètre à mettre à jour. |
| `op` | Appel d’opération utilisé pour définir l’action nécessaire pour mettre à jour la connexion. Les opérations comprennent : `add`, `replace`, `remove`, `copy` et `test`. |

**Réponse**

Une réponse réussie renvoie les détails mis à jour de la stratégie de sélection, y compris son identifiant.

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
