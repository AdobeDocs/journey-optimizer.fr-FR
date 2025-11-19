---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Créer une offre personnalisée
description: Une offre personnalisée est un message marketing personnalisable basé sur des contraintes et des règles d’éligibilité.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 234bee17-c830-4bc0-b258-182804df4cb3
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: ht
source-wordcount: '180'
ht-degree: 100%

---

# Créer une offre personnalisée {#create-personalized-offer}

Une offre personnalisée est un message marketing personnalisable basé sur des contraintes et des règles d’éligibilité.

Vous pouvez créer une offre personnalisée en adressant une requête POST à l’API [!DNL Offer Library], tout en fournissant votre identifiant de conteneur.

## En-têtes Accept et Content-Type {#accept-and-content-type-headers}

Le tableau suivant montre les valeurs valides qui comprennent les champs *Content-Type* et *Accept* dans l&#39;en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Format d&#39;API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les offres personnalisées. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
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
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
        }
    ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2023-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
    },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
    },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
    ]
}'
```

**Réponse**

Une réponse réussie renvoie des informations sur l’offre personnalisée nouvellement créée, y compris son identifiant d’instance unique et l’`@id` d’emplacement. Vous pouvez utiliser l’ID d’instance aux étapes suivantes pour mettre à jour ou supprimer votre offre personnalisée.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2023-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Limites {#limitations}

Certaines contraintes et représentations d’offre ne sont actuellement pas prises en charge avec les workflows [!DNL Experience Edge] mobiles, par exemple `Capping`. La valeur du champ `Capping` indique le nombre de fois où une offre peut être présentée à tous les utilisateurs. Pour plus d’informations, voir [Documentation sur les règles d’éligibilité et les contraintes d’offres](../../../../offer-library/creating-personalized-offers.md).
