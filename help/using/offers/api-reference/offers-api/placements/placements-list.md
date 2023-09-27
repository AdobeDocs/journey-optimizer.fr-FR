---
title: Liste des emplacements
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 52%

---

# Liste des emplacements {#list-placements}

Les emplacements sont des conteneurs utilisés pour présenter vos offres. Un emplacement permet de s&#39;assurer que le contenu d&#39;offre approprié s&#39;affiche au bon endroit dans votre message. Lorsque vous ajoutez du contenu à une offre, vous êtes invité à sélectionner un emplacement dans lequel ce contenu peut être affiché.

Vous pouvez afficher une liste de tous les emplacements en adressant une seule requête de GET au [!DNL Offer Library] API.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/placements?{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/dps` |

## Utilisation des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `property` | Un filtre de propriété facultatif : <br> <ul> - Les propriétés sont regroupées par opération ET. <br><br> - Les paramètres peuvent être répétés comme suit : property=<property-expr>[&amp;property=<property-expr2>..] ou property=<property-expr1>[,<property-expr2>..] <br><br> - Les expressions de propriété sont au format [!]field[op]value, avec op in [== !=,&lt;=,>=,&lt;,>~], prise en charge des expressions régulières | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie une liste d’emplacements présents et auxquels vous avez accès.

```json
{
    "results": [
        {
            "created": "2023-05-15T11:22:50.031+00:00",
            "modified": "2023-05-15T11:22:50.031+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement5678",
            "name": "Placement one",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "itemCount": 1,
            "allowDuplicatePlacements": false,
            "returnContent": false,
            "returnMetaData": {
                "decisionName": true,
                "offerName": true,
                "offerAttributes": true,
                "offerPriority": true,
                "placementName": true,
                "channelType": true,
                "contentType": true
            }
        },
        {
            "created": "2023-05-19T08:29:15.875+00:00",
            "modified": "2023-05-19T08:29:15.875+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement1234",
            "name": "Placement two",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "itemCount": 1,
            "allowDuplicatePlacements": false,
            "returnContent": false,
            "returnMetaData": {
                "decisionName": true,
                "offerName": true,
                "offerAttributes": true,
                "offerPriority": true,
                "placementName": true,
                "channelType": true,
                "contentType": true
            }
        }
    ],
    "count": 2,
    "total": 4,
    "_links": {
        "self": {
            "href": "/placements?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/placements?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
