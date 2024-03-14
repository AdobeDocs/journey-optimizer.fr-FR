---
title: Prise en main des API de diffusion d’offres
description: Découvrez les API disponibles pour diffuser des offres personnalisées.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 100%

---

# Prise en main des API de diffusion d’offres {#about-decisioning-apis}

Vous pouvez diffuser des offres à l’aide de l’une des API suivantes : API **Decisioning** ou **Edge Decisioning.** En outre, l’API **Batch Decisioning** vous permet de diffuser des offres à tous les profils d’une audience donnée en un seul appel. Le contenu de l’offre pour chaque profil de l’audience est placé dans un jeu de données Adobe Experience Platform où il est disponible pour les workflows par lots personnalisés.

Cette page contient des informations sur les fonctionnalités spécifiques disponibles avec les API **Decisioning** et **Edge Decisioning**. Même si toutes deux vous permettent de diffuser des offres à vos clients, il est recommandé d’utiliser l’API **Edge Decisioning** chaque fois que possible pour les cas d’utilisation entrants. Cette dernière assure une latence plus faible et un débit plus élevé sur votre plateforme.

Pour plus d’informations sur l’utilisation des API, reportez-vous aux sections suivantes :
* [API Decisioning](decisioning-api.md)
* [API Edge Decisioning](edge-decisioning-api.md)
* [API Batch Decisioning](batch-decisioning-api.md)

## Gérer l&#39;accès à un conteneur {#manage-access-to-container}

Un conteneur est un mécanisme d&#39;isolement qui permet de séparer différentes préoccupations. L&#39;ID de conteneur est le premier élément de chemin d&#39;accès pour toutes les API du référentiel. Tous les objets de prise de décision résident dans un conteneur.

Un administrateur peut regrouper des entités principales, des ressources et des autorisations d&#39;accès similaires dans des profils. La charge de gestion est ainsi réduite et est assurée par l&#39;[Adobe Admin Console](https://adminconsole.adobe.com/). Pour créer des profils et leur affecter des utilisateurs, vous devez être un administrateur de produit pour Adobe Experience Platform. Il suffit de créer des profils de produit qui correspondent à certaines autorisations en une seule étape, puis d&#39;ajouter des utilisateurs à ces profils. Les profils agissent comme des groupes ayant reçu des autorisations, et chaque utilisateur réel ou technique de ce groupe hérite de ces autorisations.

Avec les privilèges d&#39;administrateur, vous pouvez accorder ou retirer des autorisations aux utilisateurs et utilisatrices via [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=fr){target="_blank"}.

### Liste des conteneurs accessibles aux utilisateurs et aux intégrations {#list-containers-accessible-to-users-and-integrations}

**Format d&#39;API**

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

Une réponse positive renvoie des informations concernant les conteneurs de gestion de décision. Cela inclut un attribut `instanceId` dont la valeur est votre identifiant de conteneur.

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
                "repo:createdDate": "2023-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2023-09-16T07:54:32.098139Z",
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

## Fonctionnalités de l’API Edge Decisioning {#edge}

**Demande unique pour les événements d’expérience et les demandes de prise de décision**

Grâce à l’API Edge Decisioning, vous pouvez envoyer l’événement d’expérience lui-même ainsi que la demande de prise de décision, et ce en une seule demande au lieu de deux.

Par exemple, si un client visite votre site web, la demande comprendra l’événement d’expérience (la visite du client sur la page) et elle recevra une offre en retour pour remplir la page visitée.

**Stockage des données contextuelles dans Adobe Experience Platform**

Les données contextuelles font référence aux données dont vous ne prenez connaissance qu’au moment où vous voulez récupérer une offre. Par exemple, la couleur de l’article acheté, la météo au moment de l’achat, etc.

Lors de la transmission de données contextuelles avec une demande de l’API Edge Decisioning, les données sont stockées dans le profil Adobe Experience Platform, pour une réutilisation ultérieure.

>[!NOTE]
>
>Pour que les données contextuelles soient stockées, vous devez avoir configuré un schéma XDM dédié.

**Mise à jour du compteur de limitation de la fréquence**

Si la limitation de la fréquence a été activée pour certaines de vos offres afin de définir la fréquence à laquelle leur nombre de limitation est réinitialisé, le compteur est mis à jour et disponible dans une décision de l’API Edge Decisioning en moins de 3 secondes. [Découvrir comment ajouter des contraintes à une offre](../../offer-library/add-constraints.md)

## Fonctionnalités de l’API Decisioning {#decisioning}

Les fonctionnalités répertoriées ci-dessous ne sont disponibles qu’avec l’API Decisioning. Si vous avez besoin de l’une d’entre elles pour répondre à vos besoins, utilisez l’API Decisioning. Dans le cas contraire, il est recommandé d’utiliser les API Edge Decisioning.

* **Contenu et caractéristiques de l’offre** : vous pouvez choisir de ne pas renvoyer le contenu et les caractéristiques d’une offre à l’aide d’une option dédiée.
* **Métadonnées de l’offre** : permet d’activer une option pour renvoyer les métadonnées d’une offre.
* **Politique de fusion** : permet d’utiliser dans votre demande une politique de fusion différente de celle associée à votre sandbox.
* **Événements de prise de décision et capping de la fréquence** : permet de bloquer les événements de prise de décision pour qu’ils ne soient pas comptabilisés par toute limitation de fréquence qui se produit.
* **Propositions en double** : permet d’activer une option pour ne pas dédupliquer les propositions.
