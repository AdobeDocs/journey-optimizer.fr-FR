---
title: Création d'une collection
description: Les collections sont des sous-ensembles d'offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l'offre.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 683f8b86-8545-46d0-a4a8-25c5b3c7b9c3
source-git-commit: 5fa3c0c39de43450b199a41c4a4a032674dd4887
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 95%

---

# Création d&#39;une collection {#create-collection}

Les collections sont des sous-ensembles d&#39;offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l&#39;offre.

Vous pouvez créer une collection en adressant une requête POST à l&#39;API [!DNL Offer Library], tout en fournissant votre ID de conteneur.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent les champs *Content-Type* et *Accept* dans l&#39;en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps/` |

**Requête**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**Réponse**

Une réponse réussie renvoie des informations sur la collection nouvellement créée, y compris son identifiant d&#39;instance unique et l&#39;`@id` d&#39;emplacement. Vous pouvez utiliser l&#39;ID d&#39;instance aux étapes suivantes pour mettre à jour ou supprimer votre collection. Vous pouvez utiliser votre `@id` de collection unique dans un tutoriel ultérieur pour créer une décision.

```json
{
    "instanceId": "0bf31c20-13f1-11eb-a752-e58fd7dc4cb3",
    "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
