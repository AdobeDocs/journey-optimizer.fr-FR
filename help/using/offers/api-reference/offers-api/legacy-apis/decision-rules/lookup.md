---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Recherche d’une règle de décision
description: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.
feature: Decision Management, API
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 3099736d-7109-4c94-aea6-053a9b885278
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 100%

---

# Rechercher une règle de décision {#lookup-decision-rule}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)


Vous pouvez rechercher une règle de décision spécifique en adressant une requête GET à l’API [!DNL Offer Library] qui inclut soit la règle de décision `@id` soit le nom de la règle de décision dans le chemin de la requête.

**Format d’API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les règles de décision. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | Définit le schéma associé aux règles de décision. | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `id` | Chaîne utilisée pour faire correspondre la propriété `@id` des entités. La chaîne correspond exactement. Les paramètres `id` et `name` ne peuvent pas être utilisés ensemble. | `xcore:eligibility-rule:124e0faf5b8ee89b` |
| `name` | Chaîne utilisée pour faire correspondre la propriété xdm:name des entités. La chaîne correspond exactement, avec la capitalisation, mais des caractères génériques peuvent être utilisés. Les paramètres `id` et `name` ne peuvent pas être utilisés ensemble | `Sales rule` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie les détails de la règle de décision spécifique que vous avez recherchée, y compris des informations sur son `id` de règle de décision unique.

```json
  {
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2023-10-21T20:14:08.153670Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-21T20:13:43.048666Z",
                "repo:lastModifiedDate": "2023-10-21T20:13:43.048666Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales rule",
                    "description": "Decisioning rule for sales",
                    "xdm:definedOn": {
                        "profile": {
                            "xdm:schema": {
                                "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                                "version": "1"
                            },
                            "xdm:referencePaths": [
                                "person.name.firstName"
                            ]
                        }
                    },
    "condition": {
                        "format": "pql/text",
        "type": "PQL",
                        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
                    },
                    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
            }
}
```
