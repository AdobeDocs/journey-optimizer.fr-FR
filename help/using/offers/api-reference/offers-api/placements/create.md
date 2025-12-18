---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Création d’un emplacement
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Decision Management, API
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 7b735873-86f5-466f-b079-5e84d9f03a08
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 100%

---

# Créer un emplacement {#create-placement}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)


Vous pouvez créer un emplacement en adressant une requête POST à l’API [!DNL Offer Library].

## En-têtes Accept et Content-Type {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent le champ *Type de contenu* dans l’en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Content-Type | `application/json` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/placements
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/placements' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "New placement",
    "description": "Placement description",
    "componentType": "html",
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "itemCount": 1,
    "allowDuplicatePlacements": false,
    "returnContent": true,
    "returnMetaData": {
        "decisionName": false,
        "offerName": false,
        "offerAttributes": false,
        "offerPriority": false,
        "placementName": false,
        "channelType": false,
        "contentType": false
    }
}'
```

**Réponse**

Une réponse réussie renvoie les détails de l’emplacement nouvellement créé et son `id`. Vous pouvez l’utiliser aux étapes suivantes pour mettre à jour ou supprimer votre emplacement. Vous pouvez utiliser l’`id` d’emplacement unique dans des tutoriels ultérieurs pour créer des décisions, des règles de décision et des offres de secours.

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
