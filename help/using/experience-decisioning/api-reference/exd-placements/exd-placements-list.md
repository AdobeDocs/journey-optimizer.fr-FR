---
title: Liste des emplacements d’extension
description: Les emplacements d’extension se composent de collections associées à des contraintes et à des méthodes de classement pour déterminer les offres.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 100%

---

# Liste des emplacements d’extension {#list-exd-placements}

Vous pouvez afficher une liste de tous les emplacements d’extension en effectuant une seule requête GET sur l’API Bibliothèque des offres.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/exd-placements?{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |

## Utiliser des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources. Vous pouvez filtrer par statut, canal et channelConfiguration.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `property` | Un filtre de propriété facultatif : <ul><li>Les propriétés sont regroupées par opération AND.</li><li>Les paramètres peuvent être répétés comme suit : property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] ou property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Les expressions de propriété sont au format `[!]field[op]value`, avec `op` dans `[==,!=,<=,>=,<,>,~]`, prenant en charge les expressions régulières.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitez le nombre d’entitées renvoyées. | `limit=5` |

**Requête**

```shell
curl --location --request GET 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{"query":"","variables":{}}'
```

**Réponse**

Une réponse renvoie une liste des emplacements d’extension auxquelles vous avez accès.

```json
{
    "results": [
        {
            "created": "2024-11-14T23:30:29.820Z",
            "modified": "2024-11-14T23:30:29.820Z",
            "etag": 1,
            "schemas": [
                "exd-placement"
            ],
            "createdBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "lastModifiedBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "id": "dps:exd-placement:19c61da45ed96159",
            "name": "testing-alfa",
            "description": "atest",
            "tags": [
                "35801d6b-6371-449d-9083-d895fc120569"
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "channelConfiguration": "fb8e9621-a5e8-485f-9f3f-d040c601ebc4",
            "status": "active"
        },
        {
            "created": "2024-10-22T00:18:17.997Z",
            "modified": "2024-10-22T05:04:15.315Z",
            "etag": 2,
            "schemas": [
                ""
            ],
            "createdBy": "71486D7B5F4011980A494030@AdobeID",
            "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
            "id": "dps::19a7426d533db126",
            "name": "Test Exd Placement capacitor",
            "description": "Wooden system",
            "status": "archived"
        }
    ],
    "count": 2,
    "total": 2,
    "_links": {
        "self": {
            "href": "/exd-placements?orderby=-modified&limit=50",
            "type": "application/json"
        }
    }
}
```
