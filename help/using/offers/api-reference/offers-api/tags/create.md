---
title: Création de balises
description: Les balises vous permettent de mieux organiser et trier vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 100%

---

# Créer une balise {#create-tag}

Vous pouvez créer une balise en adressant une requête POST à l’API [!DNL Offer Library], tout en fournissant votre ID de conteneur.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent les champs *Content-Type* et *Accept* dans l&#39;en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les balises. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**Réponse**

Une réponse réussie renvoie des informations sur la balise nouvellement créée, y compris son identifiant d’instance unique et l’`@id` d’emplacement. Vous pouvez utiliser l’ID d’instance aux étapes suivantes pour mettre à jour ou supprimer votre balise. Vous pouvez utiliser votre `@id` de balise unique dans des tutoriels ultérieurs pour créer des collections et des offres personnalisées.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
