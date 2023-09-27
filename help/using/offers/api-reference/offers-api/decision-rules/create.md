---
title: Créer une règle de décision
description: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 55%

---

# Créer une règle de décision {#create-decision-rule}

Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant affiche les valeurs valides qui comprennent la variable *Content-Type* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les règles de décision. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Sales rule",
    "description": "Decisioning rule for sales",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "definedOn": {
        "profile": {
            "schema": {
                "ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Réponse**

Une réponse réussie renvoie des informations sur la règle de décision nouvellement créée, y compris l’emplacement. `id`. Vous pouvez utiliser la variable `id` lors d’étapes ultérieures pour mettre à jour ou supprimer votre règle de décision ou l’utiliser dans un tutoriel ultérieur pour créer des décisions, des règles de décision et des offres de secours.

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
