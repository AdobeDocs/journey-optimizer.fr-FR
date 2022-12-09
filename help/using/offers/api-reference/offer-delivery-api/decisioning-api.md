---
title: Diffuser des offres
description: La gestion de la décision est un ensemble de services et d’interfaces utilisateur qui permet aux marketeurs de créer et de proposer des expériences d’offres personnalisées aux utilisateurs finaux par le biais de canaux et d’applications en s’appuyant sur une logique commerciale et des règles de décision.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: d3a22f223353dfa5d43acab400cea3d5c314662f
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Diffuser des offres à l’aide de l’API de prise de décision {#decisioning-api}

Avec la gestion de la décision, vous pouvez créer et diffuser des expériences d’offres personnalisées destinées aux utilisateurs finaux, sur différents canaux et applications à l’aide d’une logique commerciale et de règles de décision. Une offre est un message marketing auquel des règles peuvent être associées et qui spécifie qui est éligible pour voir l’offre.

Vous pouvez créer et diffuser des offres en envoyant une requête POST à la fonction [!DNL Decisioning] API.

Ce tutoriel nécessite une compréhension pratique des API, en particulier en ce qui concerne la gestion des décisions. Pour plus d’informations, voir [Guide de développement de l’API Decision Management](../getting-started.md). Ce tutoriel nécessite également que vous disposiez d’un identifiant d’emplacement et d’une valeur d’identifiant de décision uniques. Si vous n’avez pas acquis ces valeurs, consultez les tutoriels pour [création d’un emplacement](../offers-api/placements/create.md) et [création d’une décision](../activities-api/activities/create.md).

➡️  [Découvrez cette fonctionnalité en vidéo](#video)

## En-têtes Accepter et Type de contenu {#accept-and-content-type-headers}

Le tableau suivant affiche les valeurs valides qui comprennent la variable *Content-Type* et *Accepter* dans l’en-tête de la requête :

| Nom de l’en-tête | Valeur |
| ----------- | ----- |
| Accepter | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**Format d’API**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
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

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Cet objet contient les identifiants d’emplacement et de décision. |
| `xdm:propositionRequests.xdm:placementId` | Identifiant d’emplacement unique. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | Identifiant de décision unique. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | Nombre d’offres à renvoyer. Le nombre maximal est 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Cet objet contient des informations sur le profil pour lequel la décision est requise. Pour une requête API, celle-ci contient un profil. |
| `xdm:profiles.xdm:identityMap` | Cet objet contient un ensemble d’identités de l’utilisateur final basées sur le code d’intégration d’espace de noms de l’identité. La carte des identités peut comporter plusieurs identités de chaque espace de noms. Pour plus d’informations sur les espaces de noms, voir [cette page](../../../segment/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | Identifiant généré par le client qui peut être utilisé pour identifier de manière unique une demande de décision de profil. Cet ID est repris dans la réponse et n’influence pas le résultat de la décision. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Cet objet représente la structure de contrôle des règles de déduplication. Il se compose d’une série d’indicateurs qui indiquent si la même option peut être proposée pour une certaine dimension. Un indicateur défini sur true signifie que les doublons sont autorisés et ne doivent pas être supprimés dans la catégorie indiquée par l’indicateur. Un indicateur défini sur false signifie que le moteur de décision ne doit pas faire la même proposition dans la dimension et choisir plutôt la meilleure option pour l’une des sous-décisions. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Si cette valeur est définie sur true, plusieurs décisions peuvent se voir attribuer la même option. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Si cette valeur est définie sur true, plusieurs emplacements peuvent se voir attribuer la même option. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Identifie la stratégie de fusion par laquelle régir les données renvoyées par le service d’accès aux profils. Si l’un d’eux n’est pas spécifié dans la requête, la gestion de la décision ne transmettra aucun service d’accès aux profils, sinon elle transmettra l’identifiant fourni par l’appelant. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Ensemble d’indicateurs qui formate le contenu de la réponse. |
| `xdm:responseFormat.xdm:includeContent` | Une valeur booléenne qui, si elle est définie sur `true`, inclut le contenu de la réponse. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Objet utilisé pour spécifier les métadonnées supplémentaires renvoyées. Si cette propriété n’est pas incluse, alors `xdm:id` et `repo:etag` sont renvoyés par défaut. | `name` |
| `xdm:responseFormat.xdm:activity` | Cet indicateur identifie les informations de métadonnées spécifiques renvoyées pour `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Cet indicateur identifie les informations de métadonnées spécifiques renvoyées pour `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Cet indicateur identifie les informations de métadonnées spécifiques renvoyées pour `xdm:placement`. | `name`, `channel`, `componentType` |

**Réponse**

Une réponse réussie renvoie des informations sur votre proposition, y compris son unique `xdm:propositionId`.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `xdm:propositionId` | Identifiant unique de l’entité de proposition associée à un événement de décision XDM. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Cet objet contient une seule proposition de décision. Plusieurs options peuvent être renvoyées pour la décision. Si aucune option n’est trouvée, l’offre de secours de la décision est renvoyée. Les propositions de décision uniques incluent toujours : `options` ou une propriété `fallback` . Lorsqu’elle est présente, la variable `options` ne peut pas être vide. |
| `xdm:propositions.xdm:activity` | Cet objet contient l’identifiant unique d’une décision. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Cet objet contient l’identifiant unique d’un emplacement d’offre. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Cet objet contient une seule option, y compris son identifiant unique. S’il est présent, cet objet ne peut pas être vide. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Définit le type du composant. `@type` agit comme contrat de traitement pour le client. Lorsque l’expérience est assemblée, le compositeur recherche le ou les composants ayant un type spécifique. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Format du contenu de la réponse. | Le contenu de la réponse peut être : `text`, `html block`ou `image link` |
| `xdm:score` | Score d’une option calculée à la suite d’une fonction de classement associée à l’option ou à la décision. Ce champ sera renvoyé par l’API si une fonction de classement est impliquée dans la détermination du score d’une offre au cours du classement. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Cet objet contient une seule offre de secours, y compris son identifiant unique. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | Manifestation physique ou numérique de la ressource. En règle générale, le format doit inclure le type de média de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé, par exemple, la liste de [Types de médias Internet](http://www.iana.org/assignments/media-types/) définition des formats de médias informatiques. | `"dc:format": "image/png"` ou `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | URL facultative pour lire la ressource à partir d’un réseau de diffusion de contenu ou d’un point d’entrée de service. Cette URL est utilisée pour accéder publiquement à la ressource à partir d’un agent utilisateur. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Heure à laquelle le message de réponse de décision a été créé. Il s’agit de l’époque. | `"ode:createDate": 1566497582038` |

## Tutoriel vidéo {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de la gestion des décisions.

>[!NOTE]
>
>Cette vidéo s’applique au service d’application Offer Decisioning basé sur Adobe Experience Platform. Il fournit toutefois des conseils génériques pour utiliser Offer dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Étapes suivantes {#next-steps}

En suivant ce guide d’API, vous avez créé et diffusé des offres à l’aide de la variable [!DNL Decisions] API. Pour plus d’informations, voir [Présentation de la gestion des décisions](../../../offers/get-started/starting-offer-decisioning.md).
