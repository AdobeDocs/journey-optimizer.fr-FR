---
title: Création d'une formule de classement
description: Les formules de classement vous permettent de définir les fonctions de notation utilisées pour classer les éléments.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 23%

---

# Création d&#39;une formule de classement {#create-ranking-formula}

Vous pouvez créer une formule de classement en effectuant une requête POST à l&#39;API de la bibliothèque des offres.

**En-têtes Accept et Content-Type**

Le tableau suivant montre les valeurs valides qui comprennent les champs Type de contenu dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| --------- | ----------- | 
| Content-Type | application/json |

**Format d’API**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

**Réponse**

Une réponse réussie renvoie les détails de la formule de classement nouvellement créée, y compris la `id`. Vous pouvez utiliser le `id` aux étapes suivantes pour mettre à jour ou supprimer votre formule de classement.

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
