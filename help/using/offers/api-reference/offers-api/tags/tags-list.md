---
title: Répertorier les qualificateurs de collection
description: Les qualificateurs de collection vous permettent de mieux organiser et trier vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 56%

---

# Répertorier les qualificateurs de collection {#list-tags}

Les qualificateurs de collection (précédemment appelés « balises ») vous permettent de mieux organiser et trier vos offres. Par exemple, vous pouvez libeller vos offres Black Friday à l’aide du qualificateur de collection « Black Friday ». Vous pouvez ensuite utiliser la fonctionnalité de recherche de la bibliothèque des offres pour localiser facilement toutes les offres associées à ce qualificateur de collection.

Les qualificateurs de collection peuvent également être utilisées pour regrouper les offres sous forme de collections. Pour plus d’informations, consultez le tutoriel sur la [création de collections](../../../offer-library/creating-collections.md).

Vous pouvez afficher une liste de tous les qualificateurs de collection en adressant une seule requête de GET au [!DNL Offer Library] API.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Paramètres de requête facultatifs en fonction desquels filtrer les résultats. | `limit=2` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Utilisation des paramètres de requête {#using-query-parameters}

Vous pouvez utiliser des paramètres de requête pour paginer et filtrer les résultats lors de l&#39;organisation en liste des ressources.

### Pagination {#paging}

Les paramètres de requête les plus courants pour la pagination sont les suivants :

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `property` | Un filtre de propriété facultatif : <br> <ul> - Les propriétés sont regroupées par opération ET. <br><br> - Les paramètres peuvent être répétés comme suit : property=<property-expr>[&amp;property=<property-expr2>..] ou property=<property-expr1>[,<property-expr2>..] <br><br> - Les expressions de propriété sont au format [!]field[op]value, avec op in [== !=,&lt;=,>=,&lt;,>~], prise en charge des expressions régulières | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Triez les résultats en fonction d&#39;une propriété spécifique. L’ajout d’un - avant le nom (orderby=-name) triera les éléments par nom dans l’ordre décroissant (Z-A). Les expressions de chemin se présentent sous la forme de chemins séparés par des points. Ce paramètre peut être répété comme suit : `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitez le nombre d’entités renvoyées. | `limit=5` |

**Réponse**

Une réponse réussie renvoie une liste des qualificateurs de collection présents.

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
