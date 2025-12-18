---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: mise à jour d’un emplacement
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Decision Management, API
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 100%

---

# Mettre à jour un emplacement {#update-placement}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)


Vous pouvez modifier ou mettre à jour un emplacement en adressant une requête PATCH à l’API [!DNL Offer Library].

Pour plus d&#39;informations sur JSON Patch, notamment les opérations disponibles, consultez la [documentation JSON Patch](https://jsonpatch.com/) officielle.

## En-têtes Accept et Content-Type {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent le champ *Type de contenu* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |

**Format d&#39;API**

```http
PATCH /{ENDPOINT_PATH}/placements/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID de l’entité que vous souhaitez mettre à jour. | `offerPlacement1234` |

**Requête**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated placement"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated placement description"
    }
]'
```

| Paramètre | Description |
| --------- | ----------- |
| `op` | Appel d’opération utilisé pour définir l’action nécessaire pour mettre à jour la connexion. Les opérations comprennent : `add`, `replace`, `remove`, `copy` et `test`. |
| `path` | Chemin d’accès du paramètre à mettre à jour. |
| `value` | Nouvelle valeur avec laquelle vous souhaitez mettre à jour votre paramètre. |

**Réponse**

Une réponse réussie renvoie les détails mis à jour de l’emplacement, y compris son `id` d’emplacement unique.

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
