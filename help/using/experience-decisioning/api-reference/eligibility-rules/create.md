---
title: Créer une règle d’éligibilité
description: Les règles d’éligibilité permettent de définir les candidats éligibles en fonction de ce que vous souhaitez cibler, comme les attributs de profil et les audiences.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 39c6e82e-c1b1-4dda-a941-3db6324cef37
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 100%

---

# Créer une règle d’éligibilité {#create-eligibility-rule}

Vous pouvez créer une règle d’éligibilité en effectuant une requête POST sur l’API Bibliothèque des offres.

**Format d’API**

```http
POST /{ENDPOINT_PATH}/eligibility-rules 
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '
{
    "name": "test dule",
    "description": "xxxxxx",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "inSegment(\"849807b6-0a76-4895-96d9-89996477f23b\") and billingAddress.city.equals(\"san jose\", false)"
    }
}'
```

**Réponse**

Une réponse renvoie les détails de la nouvelle règle d’éligibilité, y compris son ID. Vous pouvez utiliser l’ID aux étapes suivantes pour mettre à jour ou supprimer votre règle d’éligibilité.

```json
{
    "etag": 1,
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
