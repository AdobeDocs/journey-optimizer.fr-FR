---
title: Créer une offre personnalisée
description: Une offre personnalisée est un message marketing personnalisable basé sur des règles et des contraintes d’éligibilité.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 60%

---

# Créer une offre personnalisée {#create-personalized-offer}

Une offre personnalisée est un message marketing personnalisable basé sur des règles et des contraintes d’éligibilité.

Vous pouvez créer une offre personnalisée en adressant une requête de POST au [!DNL Offer Library] API.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant affiche les valeurs valides qui comprennent la variable *Content-Type* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps/` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test personalized offer with frequency constraint",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "html",
                    "format": "text/html",
                    "language": [
                        "en-us"
                    ],
                    "content": "Hello You qualify for our Discount of 60%"
                }
            ]
        }
    ],
    "selectionConstraint": {
        "startDate": "2022-07-27T05:00:00.000+00:00",
        "endDate": "2023-07-29T05:00:00.000+00:00",
        "profileConstraintType": "none"
    },
    "rank": {
        "priority": 0
    },
    "cappingConstraint": {},
    "frequencyCappingConstraints": [
        {
            "enabled": false,
            "limit": 1,
            "startDate": "2023-05-15T14:25:49.622+00:00",
            "endDate": "2023-05-25T14:25:49.622+00:00",
            "scope": "global",
            "entity": "offer",
            "repeat": {
                "enabled": false,
                "unit": "month",
                "unitCount": 1
            }
        }
    ]
}'
```

**Réponse**

Une réponse réussie renvoie les détails de la nouvelle offre personnalisée, y compris l’identifiant. Vous pouvez utiliser la variable `id` lors des étapes suivantes pour mettre à jour ou supprimer votre offre personnalisée.

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

## Limites {#limitations}

Certaines contraintes et représentations d’offre ne sont actuellement pas prises en charge avec les workflows [!DNL Experience Edge] mobiles, par exemple `Capping`. La valeur du champ `Capping` indique le nombre de fois où une offre peut être présentée à tous les utilisateurs. Pour plus d’informations, voir [Documentation sur les règles d’éligibilité et les contraintes d’offres](../../../offer-library/creating-personalized-offers.md).