---
title: Créer des décisions
description: Une décision contient la logique sous-tendant la sélection d’une offre.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 553501b0-30a9-4795-9a9d-f42df5f4f2ea
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: ht
source-wordcount: '114'
ht-degree: 100%

---

# Créer une décision {#create-decision}

Vous pouvez créer une décision en adressant une requête POST à l’API [!DNL Offer Library], tout en fournissant votre ID de conteneur.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent les champs *Content-Type* et *Accept* dans l&#39;en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
      "_instance": {
          "xdm:name": "Test API",
          "xdm:startDate": "2022-01-20T16:00:00Z",
          "xdm:endDate": "2022-01-27T16:00:00Z",
          "xdm:status": "live",
          "xdm:criteria": [
              {
                  "xdm:placements": [
                      "xcore:offer-placement:1457f9322f005194"
                  ],
                  "xdm:optionSelection": {
                      "xdm:filter": "xcore:offer-filter:1457f93227d0b6f0"
                  }
              }
          ],
          "xdm:fallback": "xcore:fallback-offer:13c259399d8bf013"
      },
      "_links": {}
  }'
```

**Réponse**

Une réponse réussie renvoie des informations sur la décision nouvellement créée, y compris son identifiant d’instance unique et l’`@id` d’emplacement. Vous pouvez utiliser l’ID d’instance aux étapes suivantes pour mettre à jour ou supprimer votre décision.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
