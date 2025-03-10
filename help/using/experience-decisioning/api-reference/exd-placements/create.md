---
title: Création d’un emplacement d’ajout
description: Les stratégies d’extension se composent de collections associées à des contraintes et à des méthodes de classement permettant de déterminer les offres.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 15%

---

# Création d’un emplacement d’ajout {#create-exd-placement}

Vous pouvez créer un emplacement supplémentaire en effectuant une requête POST à l&#39;API de la bibliothèque des offres.

**En-têtes Accept et Content-Type**

Le tableau suivant montre les valeurs valides qui comprennent les champs Type de contenu dans l’en-tête de la requête :

| Paramètre | Description |
| --------- | ----------- |
| Content-Type | `application/json` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/exd-placements
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |

**Requête**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{
  "name": "Test Exd Placement1 Pants",
  "channel": "https://ns.adobe.com/xdm/channel-types/email",
  "tags":["3d75b849-b344-402b-9d9e-5d750bd46884"],
  "channelConfiguration":"530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
  "description": "compressing alarm",
  "status":"active"
}'
```

**Réponse**

Une réponse réussie renvoie les détails de l’emplacement d’extension nouvellement créé, y compris l’identifiant. Vous pouvez utiliser l’identifiant aux étapes suivantes pour mettre à jour ou supprimer votre emplacement ajouté.

```json
{
    "id": "dps:exd-placement:19cb038eca47bead",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "etag": 2,
    "createdDate": "2024-11-18T18:48:56.298Z",
    "lastModifiedDate": "2024-11-18T18:57:27.457Z",
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedByClientId": "CJMTestClientACP"
}
```
