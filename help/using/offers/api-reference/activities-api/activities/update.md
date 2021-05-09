---
title: Mettre à jour les décisions
description: Une décision contient la logique qui sous-tend la sélection d’une offre.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# Mettre à jour une décision

Vous pouvez modifier ou mettre à jour une décision dans votre conteneur en adressant une demande PATCH à l&#39;API [!DNL Offer Library].

Pour plus d’informations sur le correctif JSON, y compris les opérations disponibles, consultez la [documentation officielle sur le correctif JSON](http://jsonpatch.com/).

## En-têtes Accepter et Type de contenu

Le tableau suivant présente les valeurs valides qui comprennent les champs *Content-Type* et *Accepter* dans l’en-tête de la requête :

| Nom de l’en-tête | Valeur |
| ----------- | ----- |
| Accepter | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**Format d’API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la décision. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Demande**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Example Activity Name"
        }
    ]'
```

| Paramètre | Description |
| --------- | ----------- |
| `op` | Appel d&#39;opération utilisé pour définir l&#39;action nécessaire pour mettre à jour la connexion. Les opérations comprennent : `add`, `replace` et `remove`. |
| `path` | Chemin d’accès du paramètre à mettre à jour. |
| `value` | Nouvelle valeur avec laquelle vous souhaitez mettre à jour votre paramètre. |

**Réponse**

Une réponse positive renvoie les détails mis à jour de la décision, y compris son identifiant d&#39;instance unique et sa décision `@id`.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T21:28:24.284719Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
