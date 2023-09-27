---
title: recherche d’offres de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8f1fa116-30d2-4732-8973-bbce0dc66dec
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 32%

---

# Rechercher des offres de secours {#look-up-fallback-offers}

Vous pouvez rechercher des offres de secours spécifiques en adressant une demande de GET à la fonction [!DNL Offer Library] API qui inclut l’identifiant de l’offre de secours dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | L’identifiant de l’entité que vous souhaitez rechercher. | `fallbackOffer1234` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie les détails de l’offre de secours, y compris les informations de votre offre de secours et de l’identifiant unique de l’offre de secours.

```json
{
    "created": "2023-06-08T14:04:41.011+00:00",
    "modified": "2023-06-08T14:04:41.011+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "fallbackOffer1234",
    "name": "Fallback Offer Web",
    "description": "Fallback Offer Web Description",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "imagelink",
                    "format": "image/png",
                    "deliveryURL": "https://mysite.com"
                }
            ]
        }
    ]
}
```
