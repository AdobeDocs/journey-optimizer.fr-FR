---
title: Lister des stratégies de sélection
description: Les stratégies de sélection se composent de collections associées à des contraintes et à des méthodes de classement pour déterminer les offres.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: be0f683d-1d39-47f6-b565-1cc7ee06ee71
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/u90FzwxAaE8VS3wt0ArcZq0ibha1-1Rn0btxbRfniyA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 100%

---

# Lister des stratégies de sélection {#list-selection-strategies}

Une stratégie de sélection est constituée d’une collection associée à une contrainte d’éligibilité et d’une méthode de classement permettant de déterminer les offres à afficher lorsqu’elles sont sélectionnées dans une [politique de décision](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision).

Vous pouvez afficher une liste de toutes les stratégies de sélection en adressant une seule requête GET à l’API Bibliothèque des offres.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/selection-strategies?{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=2` |

## Utiliser des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `property` | Un filtre de propriété facultatif : <ul><li>Les propriétés sont regroupées par opération AND.</li><li>Les paramètres peuvent être répétés comme suit : property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] ou property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Les expressions de propriété sont au format `[!]field[op]value`, avec `op` dans `[==,!=,<=,>=,<,>,~]`, prenant en charge les expressions régulières.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitez le nombre d’entitées renvoyées. | `limit=5` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie une liste de stratégies de sélection auxquelles vous avez accès.

```json
{
    "results": [
        {
            "created": "2024-02-08T03:01:50.924Z",
            "modified": "2024-02-16T23:03:03.019Z",
            "etag": 4,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "selectionStrategy1234",
            "name": "Selection Strategy One",
            "description": "Selection Strategy",
            "rank": {
                "priority": 1,
                "order": {
                    "orderEvaluationType": "static"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "eligibilityRule",
                "eligibilityRule": "offerRule1234"
            },
            "optionSelection": {
                "filter": "itemCollection1234",
            }
        },
        {
            "created": "2024-01-11T11:12:06.775Z",
            "modified": "2024-01-15T14:36:02.994Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "selectionStrategy5678",
            "name": "Selection Strategy Two",
            "rank": {
                "priority": 1,
                "order": {
                    "orderEvaluationType": "scoringFunction",
                    "function": "rankingFormula5678"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            "optionSelection": {
                "filter": "itemCollection5678"
            }
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/selection-strategies?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/selection-strategies?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
