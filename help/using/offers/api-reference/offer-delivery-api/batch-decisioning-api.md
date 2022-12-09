---
title: API Batch Decisioning
description: Découvrez comment utiliser l’API Batch Decisioning pour sélectionner les meilleures offres pour les profils segmentés dans une portée de décision prédéfinie.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 34ab78408981d2b53736b31c94412da06cb860c4
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---


# Diffusez des offres à l’aide de la fonction [!DNL Batch Decisioning] API {#deliver-offers-batch}

Le [!DNL Batch Decisioning] L’API permet aux entreprises d’utiliser la fonctionnalité de prise de décision pour tous les profils d’un segment donné dans un appel unique. Le contenu de l’offre pour chaque profil du segment est placé dans un jeu de données Adobe Experience Platform où il est disponible pour les workflows par lots personnalisés.

Avec le [!DNL Batch Decisioning] API, vous pouvez renseigner un jeu de données avec les meilleures offres pour tous les profils d’un segment Adobe Experience Platform pour les portées de décision. Par exemple, une organisation peut vouloir exécuter [!DNL Batch Decisioning] afin qu’ils puissent envoyer des offres à un fournisseur de diffusion de messages. Ces offres sont ensuite utilisées comme contenu envoyé pour la diffusion de messages par lots à un même segment d’utilisateurs.

Pour ce faire, l’organisation :

* Exécutez la variable [!DNL Batch Decisioning] API, qui contient deux requêtes :

   1. A **Requête POST par lots** pour démarrer une charge de travail afin de traiter par lots les sélections d’offres.

   2. A **Requête GET de lot** pour obtenir l’état de la charge de travail par lots.

* Exportez le jeu de données vers l’API du fournisseur de diffusion de messages.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

>[!NOTE]
>
>La prise de décision par lots peut également être effectuée à l’aide de l’interface de Journey Optimizer. Pour plus d’informations, reportez-vous à la section [cette section](../../batch-delivery.md), qui fournit des informations sur les conditions préalables et les limites globales à prendre en compte lors de l’utilisation de la prise de décision par lots.

* **Nombre de tâches par lot en cours d’exécution par jeu de données**: Jusqu’à cinq tâches par lot peuvent être exécutées à la fois, par jeu de données. Toutes les autres requêtes par lots avec le même jeu de données de sortie sont ajoutées à la file d’attente. Une tâche en file d’attente est sélectionnée pour traitement une fois la tâche précédente en cours d’exécution.
* **Limitation de la fréquence**: Un lot s’exécute hors de l’instantané de profil qui se produit une fois par jour. Le [!DNL Batch Decisioning] L’API limite la fréquence et charge toujours les profils à partir de l’instantané le plus récent.

## Prise en main {#getting-started}

Avant d’utiliser cette API, veillez à suivre les étapes préalables suivantes.

### Préparer la décision {#prepare-decision}

Pour préparer une ou plusieurs décisions, veillez à créer un jeu de données, un segment et une décision. Ces prérequis sont présentés dans la section [cette section](../../batch-delivery.md).

### Exigences d’API {#api-requirements}

Tous [!DNL Batch Decisioning] Les demandes nécessitent les en-têtes suivants en plus de ceux qui sont référencés dans la variable [Guide de développement de l’API Decision Management](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: Chaîne unique qui identifie la requête.
* `x-sandbox-name`: Nom de l’environnement de test.
* `x-sandbox-id`: ID de l’environnement de test.

## Démarrage d’un traitement par lot {#start-a-batch-process}

Pour démarrer une charge de travail afin de prendre des décisions de traitement par lots, envoyez une requête POST à la fonction `/workloads/decisions` point de terminaison .

>[!NOTE]
>
>Vous trouverez des informations détaillées sur le temps de traitement des tâches par lots dans la section [cette section](../../batch-delivery.md).

**Format d’API**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `xdm:segmentIds` | La valeur est un tableau qui contient l’identifiant unique du segment. Elle ne peut contenir qu’une seule valeur. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | Le jeu de données de sortie dans lequel les événements de décision peuvent être écrits. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Un wrapper qui contient la variable `placementId` et `activityId` |  |
| `xdm:activityId` | Identifiant unique de la décision. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Identifiant d’emplacement unique. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Il s’agit d’un champ facultatif indiquant le nombre d’éléments, tels que les options demandées pour la portée de la décision. Par défaut, l’API renvoie une option par portée, mais vous pouvez demander explicitement plus d’options en spécifiant ce champ. Au moins 1 et 30 options peuvent être demandées par portée. | `1` |
| `xdm:includeContent` | Il s’agit d’un champ facultatif qui est `false` par défaut. If `true`, le contenu de l’offre est inclus dans les événements de décision du jeu de données. | `false` |

Reportez-vous à la section [Documentation de la gestion des décisions](../../get-started/starting-offer-decisioning.md) pour un aperçu des concepts et propriétés principaux.

**Réponse**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `@id` | UUID généré par la gestion des décisions qui identifie une seule charge de travail. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID d’organisation. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | ID de conteneur. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Heure à laquelle la demande de charge de travail de décision a été créée. | `1648078924834` |
| `ode:status` | État de la charge de travail. | `ode:status: "QUEUED"` |

## Récupération des informations sur une décision de lot {#retrieve-information-on-a-batch-decision}

Pour récupérer des informations sur une décision spécifique, envoyez une requête GET à la variable `/workloads/decisions` point de terminaison tout en fournissant la valeur d’ID de charge de travail correspondante pour votre décision.

**Format d’API**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | UUID généré par la gestion des décisions qui identifie une seule charge de travail. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Réponse**

```json
{
    "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `@id` | UUID généré par la gestion des décisions qui identifie une seule charge de travail. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID d’organisation | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | ID de conteneur | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Heure à laquelle la demande de charge de travail de décision a été créée. | `1648076994405` |
| `ode:status` | L’état de la charge de travail commence par &quot;QUEUED&quot; et passe à &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; ou &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Cela affiche plus de détails, tels que sparkJobId et batchID si l’état est &quot;PROCESSING&quot; ou &quot;INGESTING&quot;. Il affiche les détails de l’erreur si l’état est &quot;ERROR&quot;. |  |

## Étapes suivantes {#next-steps}

En suivant ce guide de l’API, vous avez vérifié l’état de la charge de travail et envoyé des offres à l’aide de [!DNL] [!DNL Batch Decisioning]] API. Pour plus d’informations, voir [Présentation de la gestion des décisions](../../get-started/starting-offer-decisioning.md).
