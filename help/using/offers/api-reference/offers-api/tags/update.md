---
title: Mettre à jour les balises
description: Les balises vous permettent de mieux organiser et trier vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 918927e1-ad7a-4937-b652-2a0932e9efa1
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Mettre à jour une balise {#update-tag}

Vous pouvez modifier ou mettre à jour une balise dans votre conteneur en adressant une requête PATCH à la fonction [!DNL Offer Library] API.

Pour plus d’informations sur le correctif JSON, y compris les opérations disponibles, voir [Documentation du correctif JSON](http://jsonpatch.com/).

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant affiche les valeurs valides qui comprennent la variable *Content-Type* et *Accepter* dans l’en-tête de la requête :

| Nom de l’en-tête | Valeur |
| ----------- | ----- |
| Accepter | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**Format d’API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les balises. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la balise que vous souhaitez mettre à jour. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Requête**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
          "op": "replace",
          "path": "/_instance/xdm:name",
          "value": "Sales and promotions for the holidays"
        }
    ]'
```

| Paramètre | Description |
| --------- | ----------- |
| `op` | Appel d’opération utilisé pour définir l’action nécessaire pour mettre à jour la connexion. Les opérations incluent : `add`, `replace`, et `remove`. |
| `path` | Chemin d’accès du paramètre à mettre à jour. |
| `value` | Nouvelle valeur avec laquelle vous souhaitez mettre à jour votre paramètre. |

**Réponse**

Une réponse réussie renvoie les détails mis à jour de la balise, y compris son identifiant d’instance unique et la balise. `@id`.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:36:31.782607Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
