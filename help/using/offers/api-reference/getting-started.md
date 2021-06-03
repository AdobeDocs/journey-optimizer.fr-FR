---
title: Prise en main
description: Découvrez comment commencer à utiliser l’API de la bibliothèque des offres pour effectuer des opérations essentielles à l’aide du moteur de gestion de décision.
source-git-commit: 741fe2b614e3ded57c4a7ecd9b7333bdd99ab359
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 96%

---

# Guide du développeur de l’API de gestion de décision

Ce guide du développeur décrit les étapes à suivre pour vous aider à démarrer l’API [!DNL Offer Library]. Le guide fournit ensuite des exemples d’appels API pour effectuer des opérations clés à l’aide du moteur de gestion de déciion.

![](../../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité en vidéo](#video)

## Conditions préalables

Ce guide nécessite une compréhension professionnelle des composants suivants d’Adobe Experience Platform :

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr) : Cadre normalisé selon lequel [!DNL Experience Platform] organise les données de l’expérience client.
   * [Notions de base de la composition du schéma](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html) : en savoir plus sur les blocs de création de base des schémas XDM.
* [Gestion de décision](../../../using/offers/get-started/starting-offer-decisioning.md) : explique les concepts et les composants utilisés pour la prise de décision basée sur l’expérience en général et pour la prise de décision relative aux offres en particulier. Illustre les stratégies utilisées pour choisir la meilleure option à présenter lors de l’expérience client.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr) : PQL est un langage puissant pour écrire des expressions sur des instances XDM. PQL est utilisé pour définir des règles de décision.

## Lecture d’exemples d’appels API

Ce guide fournit des exemples d’appels API pour démontrer comment formater vos requêtes. Il s’agit notamment de chemins d’accès, d’en-têtes requis et de payloads de requêtes correctement formatés. L’exemple JSON renvoyé dans les réponses de l’API est également fourni. Pour plus d’informations sur les conventions utilisées dans la documentation pour les exemples d’appels d’API, voir la section concernant la [lecture d’exemples d’appels d’API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request) dans le guide de dépannage[!DNL Experience Platform].

## Collecte des valeurs des en-têtes requis

Pour lancer des appels aux API [!DNL Platform], vous devez d’abord suivre le [tutoriel d’authentification](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html). Le tutoriel d’authentification fournit les valeurs de chacun des en-têtes requis dans tous les appels d’API [!DNL Experience Platform], comme indiqué ci-dessous :

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Toutes les requêtes contenant une payload (POST, PUT, PATCH) requièrent un en-tête supplémentaire :

* `Content-Type: application/json`

## Gérer l’accès à un conteneur

Un conteneur est un mécanisme d’isolement qui permet de séparer différentes préoccupations. L’ID de conteneur est le premier élément de chemin d’accès pour toutes les API du référentiel. Tous les objets de prise de décision résident dans un conteneur.

Un administrateur peut regrouper des entités principales, des ressources et des autorisations d’accès similaires dans des profils. La charge de gestion est ainsi réduite et est assurée par l’[Adobe Admin Console](https://adminconsole.adobe.com/). Pour créer des profils et leur affecter des utilisateurs, vous devez être un administrateur de produit pour Adobe Experience Platform. Il suffit de créer des profils de produit qui correspondent à certaines autorisations en une seule étape, puis d’ajouter des utilisateurs à ces profils. Les profils agissent comme des groupes ayant reçu des autorisations, et chaque utilisateur réel ou technique de ce groupe hérite de ces autorisations.

Avec les privilèges d’administrateur, vous pouvez accorder ou retirer des autorisations aux utilisateurs via l‘[Adobe Admin Console](https://adminconsole.adobe.com/). Pour plus d’informations, voir la [présentation du contrôle d’accès](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

### Liste des conteneurs accessibles aux utilisateurs et aux intégrations

**Format d’API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtre la liste des conteneurs par leur association aux contextes de produits. | `acp` |
| `{PROPERTY}` | Filtre le type de conteneur renvoyé. | `_instance.containerType==decisioning` |

**Requête**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse positive renvoie des informations concernant les conteneurs de gestion de décision. Elle inclut un attribut `instanceId` dont la valeur est votre identifiant de conteneur.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Étapes suivantes

Ce document couvrait les connaissances préalables requises pour effectuer des appels à l’API [!DNL Offer Library], y compris l’acquisition de votre ID de conteneur. Vous pouvez désormais procéder aux exemples d’appel fournis dans ce guide de développement et suivre leurs instructions.

## Tutoriel vidéo {#video}

La vidéo suivante est destinée à vous aider à comprendre les composants de gestion de décision.

>[!NOTE]
>
>Cette vidéo s’applique au service applicatif d’Offer Decisioning créé sur Adobe Experience Platform. Toutefois, elle fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
