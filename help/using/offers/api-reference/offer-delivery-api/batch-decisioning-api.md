---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: API Batch Decisioning
description: Découvrez comment utiliser l’API Batch Decisioning pour sélectionner les meilleures offres pour les profils d’audiences dans une portée de décision prédéfinie.
badge: label="Hérité" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 100%

---


# Diffuser des offres à l’aide de l’API [!DNL Batch Decisioning] {#deliver-offers-batch}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../../experience-decisioning/gs-experience-decisioning.md)

L’API [!DNL Batch Decisioning] permet aux organisations d’utiliser la fonctionnalité de prise de décision pour tous les profils d’une audience donnée en un seul appel. Le contenu de l’offre pour chaque profil de l’audience est placé dans un jeu de données Adobe Experience Platform où il est disponible pour les workflows par lots personnalisés.

Avec l’API [!DNL Batch Decisioning], vous pouvez renseigner un jeu de données avec les meilleures offres pour tous les profils d’une audience Adobe Experience Platform pour les portées de décision. Par exemple, une organisation peut vouloir exécuter [!DNL Batch Decisioning] afin de pouvoir envoyer des offres à un fournisseur de diffusion de messages. Ces offres sont ensuite utilisées comme contenu envoyé pour la diffusion de messages par lots à une même audience d’utilisateurs et d’utilisatrices.

Pour ce faire, l&#39;organisation :

* Exécute l&#39;API [!DNL Batch Decisioning], qui contient deux requêtes :

   1. Une **Requête POST par lots** pour démarrer une charge de travail afin de traiter par lots les sélections d&#39;offres.

   2. Une **Requête GET par lots** pour obtenir l&#39;état de la charge de travail par lots.

* Exporte le jeu de données vers l&#39;API du fournisseur de diffusion de messages.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=fr) to learn more about exporting audiences.) -->

>[!NOTE]
>
>La diffusion des décisions par lots peut également être effectuée à l’aide de l’interface de Journey Optimizer. Pour plus d’informations, reportez-vous à [cette section](../../batch-delivery.md), qui fournit des informations sur les conditions préalables et les limites globales à prendre en compte lors de l’utilisation de la diffusion des décisions par lots.

* **Nombre de tâches par lot en cours d’exécution par jeu de données** : jusqu’à cinq traitements par lot peuvent être exécutées à la fois, par jeu de données. Toutes les autres requêtes par lots avec le même jeu de données de sortie sont ajoutées à la file d’attente. Une tâche en file d’attente est sélectionnée pour traitement une fois que la tâche précédente a fini son exécution.
* **Capping de la fréquence** : un lot s&#39;exécute hors de l&#39;instantané de profil qui se produit une fois par jour. L&#39;API [!DNL Batch Decisioning] limite la fréquence et charge toujours les profils à partir de l&#39;instantané le plus récent.

## Prise en main {#getting-started}

Avant d&#39;utiliser cette API, veillez à suivre les étapes préalables suivantes.

### Préparer la décision {#prepare-decision}

Pour préparer une ou plusieurs décisions, veillez à créer un jeu de données, une audience et une décision. Ces prérequis sont présentés dans [cette section](../../batch-delivery.md).

### Exigences en termes d&#39;API {#api-requirements}

Toutes les requêtes [!DNL Batch Decisioning] nécessitent les en-têtes suivants en plus de ceux qui sont référencés dans le [Guide du développeur de l&#39;API Decision Management](../getting-started.md) :

* `Content-Type` : `application/json`
* `x-request-id` : Chaîne unique qui identifie la requête.
* `x-sandbox-name` : Nom du sandbox.

## Démarrage d&#39;un traitement par lot {#start-a-batch-process}

Pour démarrer une charge de travail afin de prendre des décisions concernant le traitement par lots, envoyez une requête POST au point d’entrée `/workloads/decisions`.

>[!NOTE]
>
>Vous trouverez des informations détaillées sur le temps de traitement des traitements par lots dans [cette section](../../batch-delivery.md).

**Format d’API**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/dwm` |

**Requête**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
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
| `xdm:activityId` | Identifiant unique de la décision. |  |
| `xdm:dataSetId` | Jeu de données de sortie dans lequel les événements de décision peuvent être écrits. | `6196b4a1a63bd118dafe093c` |
| `xdm:includeContent` | Il s&#39;agit d&#39;un champ facultatif qui est `false` par défaut. Si `true`, le contenu de l&#39;offre est inclus dans les événements de décision du jeu de données. | `false` |
| `xdm:itemCount` | Il s’agit d&#39;un champ facultatif indiquant le nombre d&#39;éléments, tels que les options demandées pour la portée de la décision. Par défaut, l&#39;API renvoie une option par portée, mais vous pouvez demander explicitement plus d&#39;options en spécifiant ce champ. Un minimum de 1 option et un maximum de 30 options peuvent être demandés par portée. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Identifiant d’emplacement unique. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | Wrapper qui contient `placementId` et `activityId`. |  |
| `xdm:segmentIds` | La valeur est un tableau qui contient l’identifiant unique de l’audience. Il ne peut contenir qu’une seule valeur. | `609028e4-e66c-4776-b0d9-c782887e2273` |

Reportez-vous à la section [Documentation de la gestion des décisions](../../get-started/starting-offer-decisioning.md) pour un aperçu des concepts et propriétés principaux.

**Réponse**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `@id` | L’UUID généré par la gestion des décisions qui identifie une seule charge de travail. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | L’ID de l’organisation | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | L&#39;heure à laquelle la requête de charge de travail de la décision a été créée. | `1648078924834` |
| `ode:status` | L&#39;état de la charge de travail. | `ode:status: "QUEUED"` |

## Récupération des informations sur une décision par lot {#retrieve-information-on-a-batch-decision}

Pour récupérer des informations sur une décision spécifique, envoyez une requête GET au point d’entrée `/workloads/decisions` tout en fournissant la valeur d’ID de charge de travail correspondante pour votre décision.

**Format d’API**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | L’UUID généré par la gestion des décisions qui identifie une seule charge de travail. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Requête**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Propriété | Description | Exemple |
| -------- | ----------- | ------- |
| `@id` | L’UUID généré par la gestion des décisions qui identifie une seule charge de travail. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | L’ID de l’organisation | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | L&#39;heure à laquelle la requête de charge de travail de décision a été créée. | `1648076994405` |
| `ode:status` | Le statut de la charge de travail commence par « QUEUED » et passe à « PROCESSING », « INGESTING », « COMPLETED » ou « ERROR ». | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Elle affiche plus de détails, tels que sparkJobId et batchID si l&#39;état est « PROCESSING » ou « INGESTING ». Elle affiche les détails de l’erreur si l&#39;état est « ERROR ». |  |

## Étapes suivantes {#next-steps}

En suivant ce guide de l&#39;API, vous avez vérifié l&#39;état de la charge de travail et envoyé des offres à l&#39;aide de l&#39;API [!DNL [!DNL Batch Decisioning]]. Pour plus d&#39;informations, consultez la [présentation de la gestion des décisions](../../get-started/starting-offer-decisioning.md).
