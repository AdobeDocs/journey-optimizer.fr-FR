---
title: Mettre à jour des règles d’éligibilité
description: Les règles d’éligibilité permettent de définir les candidats éligibles en fonction de ce que vous souhaitez cibler, comme les attributs de profil et les audiences.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8d82b4db-2ba8-4692-a63e-9cb3c6c434c3
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 100%

---

# Mettre à jour une règle d’éligibilité {#update-eligibility-rule}

Vous pouvez modifier ou mettre à jour une règle en effectuant une requête PUT sur l’API Bibliothèque des offres.

Pour plus d’informations sur JSON PUT, notamment sur les opérations disponibles, consultez la [documentation JSON PUT](https://jsonpatch.com/) officielle.

**En-têtes Accept et Content-Type**

Le tableau suivant montre les valeurs valides qui comprennent les champs Content-Type dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| --------- | ----------- | 
| Content-Type | `application/json` |

**Format d&#39;API**

```http
PUT /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez mettre à jour. | `rule1234` |

**Requête**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Offer Rule DPS",
    "description": "Offer Rule description",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
    },
    "definedOn": {
        "": {
            "schema": {
                "altId": "_xdm.context.profile",
                "version": "1"
            },
            "referencePaths": [
                "homeAddress.stateProvince"
            ]
        },
        "xEvent": {
            "schema": {
                "altId": "_xdm.context.experienceevent",
                "version": "1"
            },
            "referencePaths": [
                "eventType",
                "commerce.order.priceTotal",
                "commerce.order.currencyCode"
            ]
        }
    }
}'
```

| Paramètre | Description |
| --------- | ----------- |
| `value` | Nouvelle valeur avec laquelle vous souhaitez mettre à jour votre paramètre. |
| `path` | Chemin d’accès du paramètre à mettre à jour. |
| `op` | Appel d’opération utilisé pour définir l’action nécessaire pour mettre à jour la connexion. Les opérations comprennent : `add`, `replace`, `remove`, `copy` et `test`. |

**Réponse**

Une réponse renvoie les détails mis à jour de la règle d’éligibilité, y compris son ID.

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
