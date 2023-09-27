---
title: Création d’une offre de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 31%

---

# Création d’une offre de secours {#create-fallback-offer}

Vous pouvez créer une offre de secours en adressant une requête de POST à la variable [!DNL Offer Library] API.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant affiche les valeurs valides qui comprennent la variable *Content-Type* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID de l’entité que vous souhaitez mettre à jour. | `fallbackOffer1234` |

**Requête**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

**Réponse**

Une réponse réussie renvoie des informations sur l’offre de secours nouvellement créée, y compris son offre de secours unique. `id`. Vous pouvez utiliser la variable `id` lors d’étapes ultérieures pour mettre à jour ou supprimer votre offre de secours ou pour créer une décision dans un tutoriel ultérieur.


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
