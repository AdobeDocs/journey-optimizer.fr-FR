---
title: Créer une offre personnalisée
description: Une offre personnalisée est un message marketing personnalisable basé sur des règles d’éligibilité et des contraintes.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Créer une offre personnalisée {#create-personalized-offer}

Une offre personnalisée est un message marketing personnalisable basé sur des règles d’éligibilité et des contraintes.

Vous pouvez créer une offre personnalisée en adressant une requête POST à la variable [!DNL Offer Library] API, lors de la saisie de votre ID de conteneur.

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant affiche les valeurs valides qui comprennent la variable *Content-Type* et *Accepter* dans l’en-tête de la requête :

| Nom de l’en-tête | Valeur |
| ----------- | ----- |
| Accepter | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Format d’API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
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
            "xdm:startDate": "2020-10-01T16:00:00Z",
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

Une réponse réussie renvoie des informations sur l’offre personnalisée nouvellement créée, y compris son identifiant d’instance unique et l’emplacement. `@id`. Vous pouvez utiliser l’ID d’instance aux étapes suivantes pour mettre à jour ou supprimer votre offre personnalisée.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2020-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Limites {#limitations}

Les représentations des offres et certaines contraintes d’offre ne sont actuellement pas prises en charge avec le mobile. [!DNL Experience Edge] workflows, par exemple `Capping`. Le `Capping` valeur de champ indique le nombre de fois où une offre peut être présentée à tous les utilisateurs. Pour plus d’informations, voir [Documentation sur les règles d’éligibilité et les contraintes d’offre](../../../offer-library/creating-personalized-offers.md).