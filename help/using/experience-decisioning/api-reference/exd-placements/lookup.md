---
title: Rechercher un emplacement d’extension
description: Les emplacements d’extension se composent de collections associées à des contraintes et à des méthodes de classement pour déterminer les offres.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: cc8ae245-a96a-401e-9157-e7d4b8982081
TQID: https://experienceleague.adobe.com/0vmTC00aXOb5CDyz77rupZZSnywE1n7eOx6czrtJZIU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 100%

---

# Rechercher un emplacement d’extension {#list-exd-placement}

Vous pouvez rechercher un emplacement d’extension spécifique en effectuant une requête GET sur l’API Bibliothèque des offres qui inclut l’ID dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez rechercher. | `placement1234` |

**Requête**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19c5fa7448c6fcab' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Réponse**

Une réponse renvoie les détails de l’emplacement d’extension.

```json
{
    "created": "2024-11-14T20:56:45.540Z",
    "modified": "2024-11-14T20:56:45.540Z",
    "etag": 1,
    "schemas": [
        "exd-placement"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:exd-placement:19c5fa7448c6fcab",
    "name": "Test Exd Placement1 Car",
    "description": "brand panel",
    "tags": [
        "3d75b849-b344-402b-9d9e-5d750bd46884"
    ],
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "channelConfiguration": "530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
    "status": "active"
}            
```
