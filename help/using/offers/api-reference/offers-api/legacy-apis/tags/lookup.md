---
title: Rechercher un qualificateur de collection
description: Les qualificateurs de collection vous permettent de mieux organiser et trier vos offres.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 100%

---

# Rechercher un qualificateur de collection {#look-up-tag}

Vous pouvez rechercher des qualificateurs de collection spécifiques (auparavant appelés « balises ») en exécutant une requête GET sur l’API [!DNL Offer Library] qui inclut l’`id` de qualificateur de collection dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez rechercher. | `tag1234` |

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

Une réponse réussie renvoie les détails du qualificateur de collection, y compris les informations sur l’`id` de votre qualificateur de collection unique.

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
