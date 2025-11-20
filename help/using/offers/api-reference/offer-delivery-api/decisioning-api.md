---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Diffusion d'offres
description: 'La gestion des décisions est un ensemble de services et d''interfaces utilisateur qui permet aux spécialistes marketing de créer et de proposer des expériences d''offres personnalisées aux utilisateurs finaux par le biais de canaux et d''applications en s''appuyant sur une logique métier et des règles de décision. '
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: ht
source-wordcount: '1051'
ht-degree: 100%

---

# Diffuser des offres à l’aide de l’API Decisioning {#decisioning-api}

Avec la gestion des décisions, vous pouvez créer et proposer des expériences d&#39;offre personnalisées aux utilisateurs finaux par le biais de canaux et des applications en s&#39;appuyant sur une logique métier et des règles de décision.
Une offre est un message marketing auquel des règles peuvent être associées et qui spécifie qui est éligible pour voir l&#39;offre.

Vous pouvez créer et diffuser des offres en effectuant une requête POST à l&#39;API [!DNL Decisioning].

Ce tutoriel nécessite une bonne compréhension des API, tout particulièrement en ce qui concerne la gestion des décisions.
Pour plus d&#39;informations, consultez le [Guide de l&#39;API de gestion des décisions destiné aux développeurs](../getting-started.md).
Ce tutoriel nécessite aussi que vous disposiez d&#39;un identifiant d&#39;emplacement et d&#39;un identifiant de décision uniques. Si vous ne disposez pas de ces valeurs, consultez les tutoriels sur la [création d&#39;un emplacement](../offers-api/placements/create.md) et la [création d&#39;une décision](../activities-api/activities/create.md).

## En-têtes requis {#required-headers}

Le tableau suivant montre les valeurs valides qui comprennent les champs *Content-Type* et *Accept* dans l&#39;en-tête de la requête :

| Nom de l&#39;en-tête | Valeur |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Autorisation | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* Toutes les requêtes contenant une payload (POST, PUT, PATCH) nécessitent l’en-tête de type de contenu.


>[!NOTE]
>
>La vérification des autorisations n’est pas appliquée pour les sandbox individuels. Tant que l’entité appelante présente un jeton valide, l’API de diffusion est autorisée.

## Requête API {#request}

### Format d’API

```https
POST /{ENDPOINT_PATH}/decisions
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/ods` |

### Requête

```shell
curl -X POST 'https://platform.adobe.io/data/core/ods/decisions' \
-H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
-H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}....' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'x-request-id: e9ac8d7e-3e77-4b38-8726-555ef1737b32-example' \
-d '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:15ded04b1786ea27",
            "xdm:placementId": "dps:offer-placement:15d9bc01d35e1238"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "example@adobe.com",
                        "primary": true
                    }
                ]
            }
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

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Cet objet contient les identifiants d&#39;emplacement et de décision. |  |
| `xdm:propositionRequests.xdm:placementId` | Identifiant d&#39;emplacement unique. | `"xdm:placementId": "dps:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | Identifiant de décision unique. | `"xdm:activityId": "dps:offer-activity:ffed0123"` |
| `xdm:itemCount` | Nombre d&#39;offres à renvoyer. Le nombre maximal est 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Cet objet contient des informations sur le profil pour lequel la décision est demandée. Pour une requête d&#39;API, il contient un profil. |  |
| `xdm:profiles.xdm:identityMap` | Cet objet contient un ensemble d&#39;identités d&#39;utilisateur final basées sur le code d&#39;intégration d&#39;espace de noms de l&#39;identité. Le mappage d&#39;identité peut comporter plusieurs identités de chaque espace de noms. Pour plus d’informations sur les espaces de noms, consultez [cette page](../../../audience/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | Identifiant généré par le client pouvant être utilisé pour identifier de manière unique une demande de décision de profil. Cette identifiant est repris dans la réponse et n&#39;influence pas le résultat de la décision. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | Cet objet représente la structure de contrôle des règles de déduplication. Il s&#39;agit d&#39;une série d&#39;indicateurs qui définissent si la même option peut être proposée dans une certaine dimension. Un indicateur défini sur true signifie que les duplicatas sont autorisés et ne doivent pas être supprimés pour la catégorie indiquée par l&#39;indicateur. Un indicateur défini sur false signifie que le moteur de décision ne doit pas faire la même proposition pour la dimension et doit plutôt choisir la meilleure option suivante pour l&#39;une des sous-décisions. |  |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Si la valeur est définie sur true, plusieurs décisions peuvent se voir attribuer la même option. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Si la valeur est définie sur true, plusieurs emplacements peuvent se voir attribuer la même option. | `"xdm:acrossPlacements": true` |
| `xdm:enrichedAudience` | Ajoutez ce paramètre et définissez-le sur « true » si vous ciblez une audience au format CSV. | `"xdm:enrichedAudience": true` |
| `xdm:mergePolicy.xdm:id` | Identifie la politique de fusion selon laquelle gérer les données renvoyées par le service d’accès aux profils. S’i aucune n’est spécifiée dans la requête, la gestion des décisions ne transmet aucun service d’accès au profil. Dans le cas contraire, il transmet l’identifiant fourni par la personne appelante. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Ensemble d&#39;indicateurs qui formate le contenu de la réponse. |  |
| `xdm:responseFormat.xdm:includeContent` | Valeur booléenne qui, si elle est définie sur `true`, inclut le contenu de la réponse. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Objet utilisé pour spécifier les métadonnées supplémentaires renvoyées. Si cette propriété n&#39;est pas incluse, `xdm:id` et `repo:etag` sont renvoyés par défaut. | `name` |
| `xdm:responseFormat.xdm:activity` | Cet indicateur identifie les informations de métadonnées spécifiques renvoyées pour `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Cet indicateur identifie les informations de métadonnées spécifiques renvoyées pour `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Cet indicateur identifie les informations de métadonnées spécifiques renvoyées pour `xdm:placement`. | `name`, `channel`, `componentType` |

### Réponse

Une réponse réussie renvoie des informations sur votre proposition, y compris son unique `xdm:propositionId`.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "dps:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "dps:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "dps:fallback:ccc0222",
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
| `xdm:propositionId` | Identifiant unique de l&#39;entité de proposition associée à un événement XDM DecisionEvent. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Cet objet contient une proposition de décision unique. Plusieurs options peuvent être renvoyées pour la décision. Si aucune option n&#39;est trouvée, l&#39;offre de secours de la décision est renvoyée. Les propositions de décision uniques comprennent toujours une propriété `options` ou `fallback`. Lorsqu&#39;elle est présente, la propriété `options` ne peut pas être vide. |  |
| `xdm:propositions.xdm:activity` | Cet objet contient l&#39;identifiant unique d&#39;une décision. | `"xdm:id": "dps:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Cet objet contient l&#39;identifiant unique d&#39;un emplacement d&#39;offre. | `"xdm:id": "dps:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Cet objet contient une seule option, y compris son identifiant unique. En cas de présence, cet objet ne peut pas être vide. | `xdm:id": "dps:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Définit le type du composant. `@type` agit en tant que contrat de traitement pour le client. Une fois l&#39;expérience assemblée, le compositeur recherche le ou les composants ayant un type spécifique. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Format du contenu de la réponse. | Le contenu de la réponse peut être : `text`, `html block` ou `image link` |
| `xdm:score` | Score d&#39;une option calculée à la suite d&#39;une fonction de classement associée à l&#39;option ou à la décision. Ce champ est renvoyé par l&#39;API si une fonction de classement est impliquée dans la détermination du score d&#39;une offre au cours du classement. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Cet objet contient une seule offre de secours, y compris son identifiant unique. | `"xdm:id": "dps:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | Manifestation physique ou numérique de la ressource. En règle générale, le format doit inclure le type de média de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé, par exemple, la liste des [types de médias Internet](https://www.iana.org/assignments/media-types/) définissant les formats de médias informatiques. | `"dc:format": "image/png"` ou `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | URL facultative permettant de lire le fichier à partir d’un réseau de diffusion de contenu ou d’un point d’entrée de service. Cette URL permet d&#39;accéder publiquement à la ressource à partir d&#39;un agent utilisateur. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Heure à laquelle le message de réponse à la décision a été créé. Il s&#39;agit de l&#39;époque. | `"ode:createDate": 1566497582038` |

**Codes de réponse**

Le tableau ci-dessous répertorie tous les codes qui peuvent être renvoyés dans la réponse :

| Code | Description |
|  ---  |  ---  |
| 200 | Réussite. Une décision a été prise pour des activités données. |
| 400 | Paramètre de requête non valide. La requête ne peut pas être comprise par le serveur en raison d’une syntaxe incorrecte. |
| 403 | Accès interdit, autorisations insuffisantes. |
| 422 | Entité impossible à traiter. La syntaxe de la requête est correcte mais elle ne peut pas être traitée en raison d’erreurs sémantiques. |
| 429 | Trop de requêtes. L’utilisateur ou l‘utilisatrice a envoyé trop de demandes au cours d’une période donnée. |
| 500 | Erreur interne du serveur. Le serveur a rencontré une condition inattendue qui l’a empêché de satisfaire la requête. |
| 503 | Service indisponible en raison d’une surcharge du serveur. Le serveur ne peut actuellement pas traiter la demande en raison d’une surcharge temporaire. |

<!-- ## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/342829/?captions=fre_fr&quality=12) -->

## Étapes suivantes {#next-steps}

En suivant ce guide d&#39;API, vous avez créé et diffusé des offres à l&#39;aide de l&#39;API [!DNL Decisions]. Pour plus d&#39;informations, consultez la [présentation de la gestion des décisions](../../../offers/get-started/starting-offer-decisioning.md).

