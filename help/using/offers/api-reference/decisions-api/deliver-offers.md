---
title: Diffusion d’offres
description: La gestion des décisions est un ensemble de services et de programmes d’interface utilisateur qui permet aux spécialistes du marketing de créer et de diffuser des expériences d’offre personnalisées pour les utilisateurs finaux sur plusieurs canaux et applications à l’aide d’une logique métier et de règles de décision.
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 69%

---

# Diffuser des offres à l’aide de l’API Decisions

Avec la gestion des décisions, vous pouvez créer et diffuser des expériences d’offre personnalisées par l’utilisateur final, entre canaux et applications, en utilisant la logique métier et les règles de décision. Une offre est un message marketing auquel des règles peuvent être associées et qui spécifie qui est éligible pour voir l’offre.

Vous pouvez créer et diffuser des offres en effectuant une requête POST à l’API [!DNL Decisions].

Ce didacticiel nécessite une bonne compréhension des API, en particulier en ce qui concerne la gestion des décisions. Pour plus d&#39;informations, consultez le [Guide du développeur de l&#39;API de gestion des décisions](../getting-started.md). Ce didacticiel nécessite également que vous disposiez d’un ID de placement et d’une valeur d’ID de décision uniques. Si vous n’avez pas acquis ces valeurs, consultez les didacticiels pour [créer un emplacement](../offers-api/placements/create.md) et [créer une décision](../activities-api/activities/create.md).

![](../../../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité en vidéo](#video)

## En-têtes Accepter et Type de contenu

Le tableau suivant montre les valeurs valides qui comprennent les champs *Type de contenu* et *Accepter* dans l’en-tête de la requête :

| Nom de l’en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**Format d’API**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/ode/` |
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
| `xdm:propositionRequests` | Cet objet contient les identifiants de placement et de décision. |
| `xdm:propositionRequests.xdm:placementId` | Identifiant d’emplacement unique. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | Identificateur de décision unique. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | Nombre d’offres à renvoyer. Le nombre maximal est 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Cet objet contient des informations sur le profil pour lequel la décision est demandée. Pour une requête d’API, il contient un profil. |
| `xdm:profiles.xdm:identityMap` | Cet objet contient un ensemble d’identités d’utilisateur final basées sur le code d’intégration d’espace de noms de l’identité. Le mappage d’identité peut comporter plusieurs identités de chaque espace de noms. Pour plus d’informations sur les espaces de noms, voir la [présentation de l’espace de noms d’identité](https://docs.adobe.com/content/help/fr-FR/experience-platform/identity/namespaces.html). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | Identifiant généré par le client pouvant être utilisé pour identifier de manière unique une demande de décision de profil. Cette identifiant est repris dans la réponse et n’influence pas le résultat de la décision. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Cet objet représente la structure de contrôle des règles de déduplication. Il s’agit d’une série d’indicateurs qui définissent si la même option peut être proposée dans une certaine dimension. Un indicateur défini sur true signifie que les duplicatas sont autorisés et ne doivent pas être supprimés pour la catégorie indiquée par l’indicateur. Un indicateur défini sur false signifie que le moteur de décision ne doit pas faire la même proposition pour la dimension et doit plutôt choisir la meilleure option suivante pour l’une des sous-décisions. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Si elle est définie sur true, plusieurs décisions peuvent se voir attribuer la même option. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Si la valeur est définie sur true, plusieurs emplacements peuvent se voir attribuer la même option. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Identifie la stratégie de fusion selon laquelle gérer les données renvoyées par le service d’accès aux profils. Si l’un d’eux n’est pas spécifié dans la demande, Decision Management ne transmettra aucun service d’accès au profil, sinon il transmettra l’identifiant fourni par l’appelant. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Ensemble d’indicateurs qui formate le contenu de la réponse. |
| `xdm:responseFormat.xdm:includeContent` | Valeur booléenne qui, si elle est définie sur `true`, inclut le contenu de la réponse. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Objet utilisé pour spécifier les métadonnées supplémentaires renvoyées. Si cette propriété n’est pas incluse, `xdm:id` et `repo:etag` sont renvoyés par défaut. | `name` |
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
| `xdm:propositionId` | Identifiant unique de l’entité de proposition associée à un événement XDM DecisionEvent. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Cet objet contient une seule proposition de décision. Plusieurs options peuvent être renvoyées pour la décision. Si aucune option n&#39;est trouvée, l&#39;offre de secours de la décision est renvoyée. Les propositions de décision uniques comprennent toujours une propriété `options` ou une propriété `fallback`. Lorsqu’elle est présente, la propriété `options` ne peut pas être vide. |
| `xdm:propositions.xdm:activity` | Cet objet contient l&#39;identifiant unique d&#39;une décision. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Cet objet contient l’identifiant unique d’un emplacement d’offre. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Cet objet contient une seule option, y compris son identifiant unique. En cas de présence, cet objet ne peut pas être vide. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Définit le type du composant. `@type` agit en tant que contrat de traitement pour le client. Une fois l’expérience assemblée, le compositeur recherche le ou les composants ayant un type spécifique. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Format du contenu de la réponse. | Le contenu de la réponse peut être : `text`, `html block` ou `image link` |
| `xdm:score` | Score d’une option calculée à la suite d’une fonction de classement associée à l’option ou à la décision. Ce champ est renvoyé par l’API si une fonction de classement est impliquée dans la détermination du score d’une offre au cours du classement. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Cet objet contient une seule offre de secours, y compris son identifiant unique. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | Manifestation physique ou numérique de la ressource. En règle générale, le format doit inclure le type de média de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé, par exemple, la liste des [types de médias Internet](http://www.iana.org/assignments/media-types/) définissant les formats de médias informatiques. | `"dc:format": "image/png"` ou `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | URL facultative permettant de lire le fichier à partir d’un réseau de diffusion de contenu ou d’un point d’entrée de service. Cette URL permet d’accéder publiquement à la ressource à partir d’un agent utilisateur. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Heure à laquelle le message de réponse à la décision a été créé. Il s’agit de l’époque. | `"ode:createDate": 1566497582038` |

## Tutoriel vidéo {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de la gestion des décisions.

>[!NOTE]
>
>Cette vidéo s’applique au service d’applications d’Offer decisioning créé sur Adobe Experience Platform. Toutefois, il fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Étapes suivantes

En suivant ce guide d’API, vous avez créé et diffusé des offres à l’aide de l’API [!DNL Decisions]. Pour plus d&#39;informations, consultez l&#39;[aperçu de la gestion des décisions](../../../offers/get-started/starting-offer-decisioning.md).
