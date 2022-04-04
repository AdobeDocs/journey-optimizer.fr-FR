---
title: API Batch Decisioning
description: Découvrez comment utiliser l’API Batch Decisioning pour sélectionner les meilleures offres pour les profils segmentés dans une portée de décision prédéfinie.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 3c40f3b6f76272db32b929a886a0cd63f797a842
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 8%

---


# Diffusez des offres à l’aide de la fonction [!DNL Batch Decisioning] API {#deliver-offers-batch}

Le [!DNL Batch Decisioning] L’API permet aux entreprises d’utiliser la fonctionnalité d’offer decisioning pour tous les profils d’un segment donné dans un appel unique. Le contenu de l’offre pour chaque profil du segment est placé dans un jeu de données Adobe Experience Platform où il est disponible pour les workflows par lots personnalisés.

Avec le [!DNL Batch Decisioning] API, vous pouvez renseigner un jeu de données avec les meilleures offres pour tous les profils d’un segment Adobe Experience Platform pour les portées de décision. Par exemple, une organisation peut vouloir exécuter [!DNL Batch Decisioning] afin qu’ils puissent envoyer des offres à un fournisseur de diffusion de messages. Ces offres sont ensuite utilisées comme contenu envoyé pour la diffusion de messages par lots à un même segment d’utilisateurs.

Pour ce faire, l’organisation :

* Exécutez la variable [!DNL Batch Decisioning] API, qui contient deux requêtes :

   1. A **Requête de POST par lots** pour démarrer une charge de travail afin de traiter par lots les sélections d’offres.

   2. A **GET par lots** pour obtenir l’état de la charge de travail par lots.

* Exportez le jeu de données vers l’API du fournisseur de diffusion de messages.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## Prise en main {#getting-started}

Avant d’utiliser cette API, veillez à suivre les étapes préalables suivantes.

### Préparer la décision {#prepare-decision}

Suivez les étapes ci-dessous pour préparer une ou plusieurs décisions :

* Pour exporter le résultat de la décision, créez un jeu de données à l’aide du schéma &quot;ODE DecisionEvents&quot;.

* Créez un segment Platform qui doit être évalué puis mis à jour. Reportez-vous à la section [documentation sur la segmentation](http://www.adobe.com/go/segmentation-overview-en) pour en savoir plus sur la mise à jour de l’évaluation de l’appartenance à un segment.

* Créez une décision (dont la portée de décision est composée d’un ID de décision et d’un ID de référencement) dans Adobe Journey Optimizer. Reportez-vous à la section [section sur la définition des portées de décision](../../offer-activities/create-offer-activities.md) du guide sur la création de décisions pour en savoir plus.

### Exigences d’API {#api-requirements}

Tous [!DNL Batch Decisioning] Les demandes nécessitent les en-têtes suivants en plus de ceux qui sont référencés dans la variable [Guide de développement de l’API Decision Management](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: Chaîne unique qui identifie la requête.
* `x-sandbox-name`: Nom de l’environnement de test.
* `x-sandbox-id`: ID de l’environnement de test.

## Démarrage d’un traitement par lot {#start-a-batch-process}

Pour démarrer une charge de travail afin de prendre des décisions concernant le traitement par lots, envoyez une demande de POST à la fonction `/workloads/decisions` point de terminaison .

**Format d’API**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/ode` |
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
| `xdm:placementId` | Identifiant d&#39;emplacement unique. | `xcore:offer-placement:1410c4117306488a` |
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
| `@id` | UUID généré par l’Offer decisioning qui identifie une seule charge de travail. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | L’identifiant de votre organisation IMS. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Votre ID de conteneur. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Heure à laquelle la demande de charge de travail de décision a été créée. | `1648078924834` |
| `ode:status` | État de la charge de travail. | `ode:status: "QUEUED"` |

## Récupération des informations sur une décision de lot {#retrieve-information-on-a-batch-decision}

Pour récupérer des informations sur une décision spécifique, envoyez une demande de GET à la fonction `/workloads/decisions` point de terminaison tout en fournissant la valeur d’ID de charge de travail correspondante pour votre décision.

**Format d’API**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | UUID généré par l’Offer decisioning qui identifie une seule charge de travail. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

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
| `@id` | UUID généré par l’Offer decisioning qui identifie une seule charge de travail. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Identifiant de l’organisation IMS | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | ID de conteneur | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Heure à laquelle la demande de charge de travail de décision a été créée. | `1648076994405` |
| `ode:status` | L’état de la charge de travail commence par &quot;QUEUED&quot; et passe à &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; ou &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Cela affiche plus de détails, tels que sparkJobId et batchID si l’état est &quot;PROCESSING&quot; ou &quot;INGESTING&quot;. Il affiche les détails de l’erreur si l’état est &quot;ERROR&quot;. |  |

## Niveaux de service {#service-levels}

L’heure de bout en bout de chaque décision de lot correspond à la durée entre le moment où la charge de travail est créée et le moment où le résultat de la décision est disponible dans le jeu de données de sortie. La taille du segment dans le payload de la requête du POST est le facteur principal qui affecte le temps de décision du lot de bout en bout.  Vous trouverez ci-dessous quelques observations relatives à différentes tailles de segment :

| Taille du segment | Temps de traitement de bout en bout |
|--------------|----------------------------|
| 10 000 profils ou moins | 6 minutes |
| 1 million de profils ou moins | 10 minutes |
| 15 millions de profils ou moins | 75 minutes |

## Limites {#limitations}

Lors de l’utilisation de la variable [!DNL Batch Decisioning] Pour l’API, gardez à l’esprit les restrictions suivantes :

* **Traitement par lot unique par jeu de données**: Actuellement, une seule tâche par lot peut être exécutée par jeu de données à la fois. Toutes les autres requêtes avec le même jeu de données de sortie répondraient avec HTTP 429 (Too many requests) avant la fin de la requête précédente.
* **Limitation de la fréquence**: Un lot s’exécute hors de l’instantané de profil qui se produit une fois par jour. Le [!DNL Batch Decisioning] L’API limite la fréquence et charge toujours les profils à partir de l’instantané le plus récent.

## Étapes suivantes {#next-steps}

En suivant ce guide de l’API, vous avez vérifié l’état de la charge de travail et envoyé des offres à l’aide de [!DNL] [!DNL Batch Decisioning]] API. Pour plus d&#39;informations, consultez la [présentation de la gestion des décisions](../../get-started/starting-offer-decisioning.md).

