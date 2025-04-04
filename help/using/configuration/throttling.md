---
solution: Journey Optimizer
product: journey optimizer
title: API de limitation
description: Découvrez comment utiliser l’API de limitation.
feature: Journeys, API
role: User
level: Beginner
keywords: externe, API, optimizer, plafonnement
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: ecb479f0875cfe1865a60667da6e2f84fad5044a
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 69%

---

# Utiliser l’API de limitation

L’API de limitation vous permet de créer, de configurer et de surveiller vos configurations de limitation, afin de limiter le nombre d’événements envoyés par seconde.

Cette section fournit des informations générales sur l’utilisation de l’API. Consultez la description détaillée de l’API dans la [Documentation des API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

>[!IMPORTANT]
>
>Actuellement, une seule configuration est autorisée par organisation. La configuration doit être définie dans la sandbox de production (indiquée par x-sandbox-name dans les en-têtes).
>
>La configuration s’applique au niveau de l’organisation.
>
>Lorsque la limite définie dans l’API est atteinte, les événements suivants sont mis en file d’attente pendant 6 heures au maximum. Cette valeur ne peut pas être modifiée.

## Description de l’API de limitation et collection Postman {#description}

Le tableau ci-dessous répertorie les commandes disponibles pour l’API de limitation. Des informations détaillées, notamment des exemples de requête, des paramètres et des formats de réponse, sont disponibles dans la documentation des API Adobe Journey Optimizer [](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Méthode | Chemin | Description |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | Obtention d’une liste des configurations de limitation |
| [!DNL POST] | /throttlingConfigs | Création d’une configuration de limitation |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | Déploiement d’une configuration de limitation |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | Annulation du déploiement d’une configuration de limitation |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | Vérification de la possibilité de déployer une configuration de limitation ou non |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | Mise à jour d’une configuration de limitation |
| [!DNL GET] | /throttlingConfigs/`{uid}` | Récupération d’une configuration de limitation |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | Suppression d’une configuration de limitation |

En outre, une collection Postman est disponible [ici](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json) pour vous aider dans votre configuration de test.

Cette collection a été configurée pour partager la collection de variables Postman générée via __[Intégrations de la console Adobe I/O](https://console.adobe.io/integrations) > Essayer > Télécharger pour Postman__, qui génère un fichier d’environnement Postman avec les valeurs d’intégration sélectionnées.

Une fois le téléchargement puis le chargement effectués dans Postman, vous devez ajouter trois variables : `{JO_HOST}`, `{BASE_PATH}` et `{SANDBOX_NAME}`.
* `{JO_HOST}` : URL de passerelle [!DNL Journey Optimizer].
* `{BASE_PATH}` : point d’entrée pour l’API.
* `{SANDBOX_NAME}` : l’en-tête **x-sandbox-name** (par exemple, « prod ») correspondant au nom sandbox dans lequel les opérations d’API auront lieu. Pour plus d’informations, consultez la [Présentation des sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=fr).

## Configuration de limitation{#configuration}

Vous trouverez ci-dessous la structure d’une configuration de limitation. Les attributs **name** et **description** sont facultatifs.

```
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

Exemple :

```
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

## Erreurs

Lors de la création ou de la mise à jour d’une configuration, le processus valide la configuration donnée et renvoie le statut de validation identifié par son ID unique :

```
"ok" or "error"
```

>[!IMPORTANT]
>
>Les attributs **maxThroughput**, **urlPattern** et **methods** sont obligatoires.
>
>La valeur de **maxThroughput** doit être comprise entre 200 et 5 000.

Lors de la création, de la suppression ou du déploiement d’une configuration de limitation, les erreurs suivantes peuvent se produire :

* **ERR_THROTTLING_CONFIG_100** - Configuration de limitation : `<mandatory attribute>` est obligatoire.
* **ERR_THROTTLING_CONFIG_101** - Configuration de limitation : maxThroughput est obligatoire et doit être supérieur ou égal à 200 et inférieur ou égal à 5 000.
* **ERR_THROTTLING_CONFIG_104** - Configuration de limitation : modèle d’URL incorrect
* **ERR_THROTTLING_CONFIG_105** - Configuration de limitation : la partie hôte du modèle d’URL contient des caractères génériques non autorisés.
* **ERR_THROTTLING_CONFIG_106** - Configuration de limitation : payload non valide
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456** - « Impossible de supprimer une configuration de limitation déployée. Annulez le déploiement avant de la supprimer. »
* **THROTTLING_CONFIG_DELETE_ERROR : 1457** - « Impossible de supprimer la configuration de limitation en raison d’une erreur inattendue. »
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458** - « Impossible de déployer la configuration de limitation en raison d’une erreur inattendue. »
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459** - « Impossible d’annuler le déploiement de la configuration de limitation en raison d’une erreur inattendue. »
* **THROTTLING_CONFIG_GET_ERROR: 1460** - « Impossible d’obtenir la configuration de limitation en raison d’une erreur inattendue. »
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461** - « Impossible de mettre à jour la configuration de limitation : la version d’exécution n’est pas active. »
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462** - « Impossible de mettre à jour la configuration de limitation en raison d’une erreur inattendue. »
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463** - « Opération non autorisée sur la configuration de limitation : il ne s’agit pas d’une sandbox de production. »
* **THROTTLING_CONFIG_CREATE_ERROR: 1464** - « Impossible de créer la configuration de limitation en raison d’une erreur inattendue. »
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465** - « Impossible de créer la configuration de limitation : une seule configuration est autorisée par organisation. »
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466** - « Impossible de déployer la configuration de limitation : elle est déjà déployée. »
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467** - « Configuration de limitation introuvable. »
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468** - « Impossible d’annuler le déploiement de la configuration de limitation : elle n’a pas encore été déployée. »

**Exemples d’erreurs**

Lors de la création d’une configuration sur une sandbox hors production :

```
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

Au cas où la sandbox donnée n’existe pas :

```
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

Lors de la création d’une autre configuration :

```
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## Cycle de vie de la configuration au niveau de l’exécution {#config}

Lorsque le déploiement d’une configuration est annulé, celle-ci est marquée comme inactive au niveau de l’exécution et le traitement des événements en attente se poursuit pendant 24 heures. Elle est ensuite supprimée du service d’exécution.

Une fois la configuration non déployée, il est possible de la mettre à jour et de la redéployer. Vous créerez alors une nouvelle configuration d’exécution, qui sera prise en compte dans l’exécution des actions à venir.

Lors de la mise à jour d’une configuration déjà déployée, les nouvelles valeurs sont prises en compte immédiatement. Les ressources système sous-jacentes sont automatiquement adaptées. Cette opération est optimale par rapport à l’annulation du déploiement, puis au redéploiement de la configuration.

## Exemples de réponses {#responses}

**Création - POST**

```
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**Mise à jour - PUT**

```
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**Lecture (après mise à jour) - GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**Lecture (après déploiement) - GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## Cas d’utilisation {#uc}

Cette section répertorie les cas d’utilisation clés pour la gestion des configurations de limitation dans [!DNL Journey Optimizer] et les commandes d’API associées requises pour mettre en œuvre le cas d’utilisation.

Des détails sur chaque commande d’API sont disponibles dans la [description de l’API et collection Postman](#description).

+++Création et déploiement d’une nouvelle configuration de limitation

Appels d’API à utiliser :

1. **`list`** - Récupère les configurations existantes.
1. **`create`** - Crée une configuration.
1. **`candeploy`** - Vérifie si la configuration peut être déployée.
1. **`deploy`** - Déploie la configuration.

+++

+++Mise à jour et déploiement d’une configuration de limitation (pas encore déployée)

Appels d’API à utiliser :

1. **`list`** - Récupère les configurations existantes.
1. **`get`** - Récupère les détails d’une configuration spécifique.
1. **`update`** - Modifie la configuration.
1. **`candeploy`** - Vérifie l’éligibilité du déploiement.
1. **`deploy`** - Déploie la configuration.

+++

+++Annuler le déploiement et supprimer une configuration de limitation déployée

Appels d’API à utiliser :

1. **`list`** - Récupère les configurations existantes.
1. **`undeploy`** - Annule le déploiement de la configuration.
1. **`delete`** - Supprime la configuration.

+++

+++Supprimer une configuration de limitation déployée

En un seul appel API, vous pouvez annuler le déploiement et supprimer la configuration à l’aide du paramètre `forceDelete` .

Appels d’API à utiliser :

1. **`list`** - Récupère les configurations existantes.
1. **`delete`(avec `forceDelete` paramètre)** Force la suppression d’une configuration déployée en une seule étape.

+++

+++Mettre à jour une configuration de limitation déjà déployée

>[!NOTE]
>
>Il n’est pas nécessaire d’annuler le déploiement de la configuration avant la mise à jour.

Appels d’API à utiliser :

1. **`list`** - Récupère les configurations existantes.
1. **`get`** - Récupère les détails d’une configuration spécifique.
1. **`update`** - Modifie la configuration.

+++
