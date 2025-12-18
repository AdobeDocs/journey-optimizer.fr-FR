---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Requêtes de données contextuelles et de décision
description: Découvrez comment transmettre des données contextuelles dans les requêtes de décision.
badge: label="Hérité" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Requêtes de données contextuelles et de décision {#context-data-decisioning}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)

Cette section vous guide tout au long de la transmission des données contextuelles dans les requêtes de décision et de leur utilisation dans les règles d&#39;éligibilité.

>[!BEGINSHADEBOX]

Pour aller plus loin, vous pouvez également utiliser le contexte dans des **formules de classement** pour améliorer vos offres. Des exemples détaillés de formules de classement utilisant des données contextuelles sont disponibles dans [cette section](../offers/ranking/create-ranking-formulas.md#context-data).

>[!ENDSHADEBOX]

## Transmettre des données contextuelles dans les requêtes de décision

Les données contextuelles dans les requêtes de décision sont définies à l’aide de la clé suivante : `xdm:ContextData`.

Les attributs de données contextuelles ne sont pas pilotés par le schéma XDM. Vous pouvez transmettre n’importe quelle donnée contextuelle dans JSON dans le cadre de la payload de requête de décision.

Voici un exemple de requête de décision comportant des données contextuelles (voir `xdm:ContextData`) :

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## Utiliser des données contextuelles dans les règles d’éligibilité

Voici des exemples illustrant comment utiliser les données contextuelles transmises dans les requêtes de décision dans les règles d’éligibilité.

* Éligible si les fonctionnalités de données contextuelles contiennent une valeur particulière :

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* Éligible si le canal est non vide et égal à mobile :

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
