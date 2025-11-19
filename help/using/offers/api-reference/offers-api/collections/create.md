---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Création d'une collection
description: Les collections sont des sous-ensembles d'offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l'offre.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 683f8b86-8545-46d0-a4a8-25c5b3c7b9c3
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: ht
source-wordcount: '128'
ht-degree: 100%

---

# Création d&#39;une collection {#create-collection}

Les collections sont des sous-ensembles d&#39;offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l&#39;offre.

Vous pouvez créer une collection en adressant une requête POST à l’API [!DNL Offer Library].

## En-têtes Accept et Content-Type {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent le champ *Type de contenu* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/offer-collections
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}'
```

**Réponse**

Une réponse réussie renvoie des informations sur la collection nouvellement créée, y compris son `id`. Vous pouvez utiliser l’`id` lors d’étapes ultérieures pour mettre à jour ou supprimer votre collection ou pour créer une décision dans un tutoriel ultérieur.

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
