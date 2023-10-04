---
title: Rechercher un qualificateur de collection
description: Les qualificateurs de collection vous permettent de mieux organiser et trier vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 38%

---


# Rechercher un qualificateur de collection {#look-up-tag}

Vous pouvez rechercher des qualificateurs de collection spécifiques (précédemment appelés &quot;balises&quot;) en adressant une demande de GET à la fonction [!DNL Offer Library] API incluant le qualificateur de collection `id` dans le chemin d’accès de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | L’identifiant de l’entité que vous souhaitez rechercher. | `tag1234` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie les détails du qualificateur de collection, y compris les informations sur votre qualificateur de collection unique. `id`.

```json
{
       "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
