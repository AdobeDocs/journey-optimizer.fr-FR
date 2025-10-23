---
solution: Journey Optimizer
product: journey optimizer
title: API Capping
description: Découvrez comment utiliser l’API Capping
feature: Journeys, API
role: Developer
level: Beginner
keywords: externe, API, optimizer, limitation
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '730'
ht-degree: 100%

---

# Utiliser l’API Capping {#work}

L’API Capping vous permet de créer, configurer et surveiller vos configurations de limitation.

Cette section fournit des informations générales sur l’utilisation de l’API. Consultez la description détaillée de l’API dans la [Documentation des API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

## Description de l’API de limitation et collection Postman {#description}

Le tableau ci-dessous répertorie les commandes disponibles pour l’API de limitation. Des informations détaillées, notamment des exemples de requête, des paramètres et des formats de réponse, sont disponibles dans la [documentation des API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/){target="_blank"}.

| Méthode | Chemin | Description |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Obtention d’une liste des configurations de limitation des points d’entrée |
| [!DNL POST] | /endpointConfigs | Création d’une configuration de limitation des points d’entrée |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Déploiement d’une configuration de limitation des points d’entrée |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Annulation du déploiement d’une configuration de limitation des points d’entrée |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Vérification de la possibilité de déployer ou non une configuration de limitation des points d’entrée |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Mise à jour de la configuration de limitation des points d’entrée |
| [!DNL GET] | /endpointConfigs/`{uid}` | Récupération d’une configuration de limitation des points d’entrée |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Suppression d’une configuration de limitation des points d’entrée |

Lorsqu’une configuration est créée ou mise à jour, une vérification est automatiquement effectuée pour garantir la syntaxe et l’intégrité de la payload.
Si certains problèmes se produisent, l’opération renvoie un avertissement ou des erreurs pour vous aider à corriger la configuration.

En outre, une collection Postman est disponible [ici](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) pour vous aider lors de la configuration de test.

Elle a été créée pour partager la collection de variables Postman générée dans __[Intégrations de la console Adobe I/O](https://console.adobe.io/integrations) > Essayer > Télécharger pour Postman__, qui génère un fichier d’environnement Postman contenant les valeurs d’intégration sélectionnées.

Une fois le téléchargement puis le chargement effectués dans Postman, vous devez ajouter trois variables : `{JO_HOST}`, `{BASE_PATH}` et `{SANDBOX_NAME}`.

* `{JO_HOST}` : URL de passerelle [!DNL Journey Optimizer]
* `{BASE_PATH}` : point d’entrée pour l’API.
* `{SANDBOX_NAME}` : l’en-tête **x-sandbox-name** (par exemple, « prod ») correspondant au nom sandbox dans lequel les opérations d’API auront lieu. Pour plus d’informations, consultez la [Présentation des sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=fr){target="_blank"}.

## Configuration du point d’entrée

Voici la structure de base d’une configuration de point d’entrée :

```json
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>Le paramètre **maxHttpConnections** est facultatif. Il vous permet de limiter le nombre de connexions que Journey Optimizer va ouvrir au système externe.
>
>La valeur maximale pouvant être définie est de 400. Si rien n’est spécifié, le système peut s’ouvrir à plusieurs milliers de connexions en fonction de l’échelle dynamique du système.
>
>Lorsque la configuration de limitation est déployée, si aucune valeur `maxHttpConnections` n’a été fournie, une valeur par défaut `maxHttpConnections = -1` est ajoutée dans la configuration déployée, et Journey Optimizer utilise la valeur système par défaut.

Exemple :

```json
{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>La configuration n’est active qu’après avoir appelé le point d’entrée **deploy**.

## Avertissement et erreurs

Lorsqu’une méthode **canDeploy** est appelée, le processus valide la configuration et renvoie le statut de validation identifié par son identifiant unique, au choix :

```json
"ok" or "error"
```

Les erreurs potentielles sont les suivantes :

* **ERR_ENDPOINTCONFIG_100**: capping config: missing or invalid url
* **ERR_ENDPOINTCONFIG_101**: capping config: malformed url
* **ERR_ENDPOINTCONFIG_102**: capping config: malformed url: wildchar in url not allowed in host:port
* **ERR_ENDPOINTCONFIG_103**: capping config: missing HTTP methods
* **ERR_ENDPOINTCONFIG_104**: capping config: no call rating defined
* **ERR_ENDPOINTCONFIG_107**: capping config: invalid max calls count (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: capping config: invalid max calls count (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: capping config: can&#39;t create endpoint config: invalid payload
* **ERR_ENDPOINTCONFIG_112**: capping config: can&#39;t create endpoint config: expecting a JSON payload
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: invalid service name `<!--<given value>-->`: must be &#39;dataSource&#39; or &#39;action&#39;

L’avertissement potentiel est :

**ERR_ENDPOINTCONFIG_106**: capping config: max HTTP connections not defined: no limitation by default

## Cas d’utilisation

Cette section répertorie les principaux cas d’utilisation de la gestion des configurations de limitation dans [!DNL Journey Optimizer] et les commandes API associées requises pour mettre en œuvre le cas d’utilisation.

Des détails sur chaque commande API sont disponibles dans la [description de l’API et collection Postman](#description).

+++Créer et déployer une configuration de limitation

Appels API à utiliser :

1. **`list`** : récupère les configurations existantes.
1. **`create`** : crée une configuration.
1. **`candeploy`** : vérifie que la configuration peut être déployée.
1. **`deploy`** : déploie la configuration.

+++

+++Mettre à jour et déployer une configuration de limitation (pas encore déployée)

Appels API à utiliser :

1. **`list`** : récupère les configurations existantes.
1. **`get`** : récupère les détails d’une configuration spécifique.
1. **`update`** : modifie la configuration.
1. **`candeploy`** : vérifie l’éligibilité du déploiement.
1. **`deploy`** : déploie la configuration.

+++

+++Annuler le déploiement et supprimer une configuration de limitation déployée

Appels API à utiliser :

1. **`list`** : récupère les configurations existantes.
1. **`undeploy`** : annule le déploiement de la configuration.
1. **`delete`** : supprime la configuration.

+++

+++Supprimer une configuration de limitation déployée en une seule étape

En un seul appel API, vous pouvez annuler le déploiement et supprimer la configuration à l’aide du paramètre `forceDelete`.

Appels API à utiliser :

1. **`list`** : récupère les configurations existantes.
1. **`delete`(avec le paramètre `forceDelete`)** : force la suppression d’une configuration déployée en une seule étape.

+++

+++Mettre à jour une configuration de limitation déployée

>[!NOTE]
>
>Un redéploiement est nécessaire après la mise à jour d’une configuration déployée.

Appels API à utiliser :

1. **`list`** : récupère les configurations existantes.
1. **`get`** : récupère les détails d’une configuration spécifique.
1. **`update`** : modifie la configuration.
1. **`undeploy`** : annule le déploiement de la configuration avant d’appliquer les modifications.
1. **`candeploy`** : vérifie l’éligibilité du déploiement.
1. **`deploy`** : déploie la configuration mise à jour.

+++
