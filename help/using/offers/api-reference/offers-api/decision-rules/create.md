---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Création d’une règle de décision
description: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.
feature: Decision Management, API
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/wpVQ64pwXQz9So3T8MLgooq3gmwEBC28lEq3UllDDL8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 100%

---

# Création d’une règle de décision {#create-decision-rule}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../../../experience-decisioning/gs-experience-decisioning.md)


Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.

## En-têtes Accept et Content-Type {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent le champ *Type de contenu* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |

**Format d’API**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |

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

Une réponse réussie renvoie des informations sur l’`id` de règle de décision nouvellement créé. Vous pouvez utiliser l’`id` lors d’étapes ultérieures pour mettre à jour ou supprimer votre règle de décision ou l’utiliser dans un tutoriel ultérieur pour créer des décisions, des règles de décision et des offres de secours.

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
