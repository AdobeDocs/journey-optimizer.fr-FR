---
title: Création d’une offre de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 100%

---

# Création d&#39;une offre de secours

Vous pouvez créer une offre de secours en adressant une requête POST à l&#39;API [!DNL Offer Library], tout en fournissant votre identifiant de conteneur.

## En-têtes Accepter et Type de contenu

Le tableau suivant montre les valeurs valides qui comprennent les champs *Content-Type* et *Accept* dans l&#39;en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les offres de secours. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:status": "approved",
        "xdm:name": "Fallback for sales",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ]
}'
```

**Réponse**

Une réponse réussie renvoie des informations sur l&#39;offre de secours nouvellement créée, y compris son identifiant d&#39;instance unique et l&#39;`@id` d&#39;emplacement. Vous pouvez utiliser l&#39;ID d&#39;instance lors d&#39;étapes ultérieures pour mettre à jour ou supprimer votre offre de secours. Vous pouvez utiliser votre offre de secours unique `@id` dans un tutoriel ultérieur pour créer une décision.


```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2020-10-21T22:28:11.111732Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
