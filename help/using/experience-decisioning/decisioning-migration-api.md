---
title: API de migration Decisioning
description: Découvrez comment utiliser l’API du service de migration Decisioning pour migrer des objets de gestion des décisions entre des sandbox avec une résolution de dépendance automatisée et une prise en charge de restauration.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 9ac3eaba0b4c6536c1c447df825eb5f5c0afc900
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 5%

---


# API de migration Decisioning {#decisioning-migration-api}

L’API Decisioning Migration Service vous permet de migrer des objets Decision Management d’un sandbox à un autre. Le processus de migration s’exécute sous la forme de workflows asynchrones qui incluent l’analyse des dépendances, l’exécution et des fonctionnalités de restauration facultatives.

Cette API vous permet de transférer facilement votre contenu de prise de décision entre les environnements (par exemple, du développement à l’évaluation ou de l’évaluation à la production) tout en préservant l’intégrité et les relations des données.

Pour en savoir plus sur les avantages et les fonctionnalités de Decisioning par rapport à la gestion des décisions, voir [Avantages de la migration vers Decisioning](migrate-to-decisioning.md).

## Fonctionnalités {#capabilities}

L’API du service de migration Decisioning offre les fonctionnalités suivantes :

* **Analyse des dépendances** - Identifiez toutes les dépendances requises entre les sandbox source et cible, y compris les exigences en matière d’attributs, de segments et de jeux de données.
* **Portée de migration flexible** - Exécutez les migrations au niveau de la sandbox, de l’offre ou de la décision en fonction de vos besoins.
* **Prise en charge de la restauration** - Rétablissez une migration terminée si des problèmes sont détectés lors de la validation.

## Conditions préalables {#prerequisites}

### Autorisations nécessaires {#permissions}

Pour utiliser l’API de migration, vous avez besoin des autorisations appropriées dans les sandbox source et cible :

**Sandbox Source** - Accès en lecture aux objets de gestion des décisions

**Sandbox cible** - Création et modification de l’accès aux objets Decisioning

Les autorisations standard incluent :

* Gestion/affichage de la prise de décision
* Gérer/Afficher Les Décisions
* Gestion des offres
* Gestion des stratégies de classement
* Gestion des campagnes (si vous migrez des artefacts liés aux campagnes)
* Gestion/affichage des flux de données (si vous créez un flux de données)
* Gestion/Affichage Des Schémas

>[!NOTE]
>
>Découvrez comment attribuer des autorisations Decisioning dans [cette section](gs-experience-decisioning.md#steps). Pour obtenir la liste complète des autorisations, reportez-vous à la page [Autorisations intégrées](../administration/ootb-permissions.md#ootb-permissions).

### Préparation de votre sandbox cible {#target-sandbox-preparation}

Avant d’exécuter une migration, vérifiez que votre sandbox cible est correctement configuré :

* **Attributs** - Vérifiez que les attributs de profil et les attributs de contexte requis existent dans le sandbox cible ou préparez des mappages pour ces derniers.
* **Segments** - Assurez-vous que les segments requis existent dans le sandbox cible ou prévoyez de les mapper à l’aide de l’espace de noms et de l’identifiant.
* **Jeu de données** - Identifiez un nom de jeu de données à utiliser pour la migration (`dependency.datasetName`).
* **Flux de données** - Décidez si la migration doit créer un flux de données (`createDataStream`).

Pour plus d’informations sur la gestion des sandbox, voir [&#x200B; Utilisation et affectation de sandbox](../administration/sandboxes.md).

## Bases d’API {#api-basics}

### URL de base {#base-urls}

Utilisez les URL de base suivantes en fonction de votre environnement :

* **Production** : `https://platform.adobe.io`
* **Évaluation** : `https://platform-stage.adobe.io`

### Authentification {#authentication}

Toutes les requêtes API nécessitent les en-têtes suivants :

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

Pour obtenir des instructions détaillées sur la configuration de l’authentification, consultez le guide d’authentification de [Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

### Modèle de workflow {#workflow-model}

Chaque appel API crée ou récupère une ressource de workflow. Les workflows sont des opérations asynchrones qui effectuent le suivi de la progression et des résultats des tâches de migration.

Un workflow possède les propriétés suivantes :

* `id` - Identifiant unique du workflow (UUID)
* `status` - Statut actuel du workflow : `New`, `Running`, `Completed`, `Failed` ou `Cancelled`
* `result` - Sortie du workflow une fois terminée (inclut les résultats et les avertissements de la migration)
* `errors` - Détails d’erreur structurés en cas d’échec
* `_etag` - Identifiant de version utilisé pour les opérations de suppression (utilisateurs du service uniquement)
* `_links.self` - URL du workflow pour la récupération du statut

## Workflow de migration {#migration-workflow}

Le processus de migration se compose de deux étapes principales : l&#39;analyse des dépendances et l&#39;exécution de la migration. Pour garantir une migration réussie, procédez comme suit.

### Étape 1 : analyser les dépendances {#analyze-dependencies}

Avant la migration, utilisez le workflow de dépendance pour identifier ce qui doit être mappé de la gestion des décisions à la prise de décision dans votre sandbox cible. Cette analyse vous aide à comprendre les relations entre les objets et à préparer les mappages nécessaires.

#### Création d’un workflow de dépendance {#create-dependency-workflow}

Utilisez l’appel API suivant pour créer un workflow d’analyse des dépendances.

**Format d’API**

```http
POST /migration/service/dependency
```

**Dépendance au niveau du sandbox (recommandée en premier)**

Commencez par une analyse au niveau du sandbox pour obtenir une vue complète de toutes les dépendances :

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Dépendance de niveau offre**

Pour analyser les dépendances uniquement pour des offres spécifiques, définissez `requestLevel: "offer"` et fournissez un tableau `offersList` avec les identifiants des offres à analyser.

**Dépendance de niveau décision**

Pour analyser les dépendances uniquement pour des décisions spécifiques, définissez `requestLevel: "decision"` et fournissez un tableau `decisionsList` avec les ID de décision à analyser.

#### Vérification du statut du workflow de dépendance {#poll-dependency-status}

Interrogez le workflow de dépendance pour vérifier la fin de l’analyse.

**Format d’API**

```http
GET /migration/service/dependency/{id}
```

**Requête**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

Lorsque le champ de `status` affiche `Completed`, l’analyse des dépendances est prête. Utilisez la sortie du workflow pour créer vos mappages de dépendance de migration :

* **profileAttributeDependency** - Mappe les attributs de profil source aux attributs de profil cible
* **contextAttributeDependency** - Mappe les attributs de contexte source aux attributs de contexte cible.
* **segmentsDependency** - Mappe les clés de segment source aux identifiants de segment cible (`{segmentNamespace, segmentId}`).
* **datasetName** - Spécifie le nom du jeu de données cible pour la migration

### Étape 2 : exécuter la migration {#execute-migration}

Une fois que vous avez analysé les dépendances et préparé vos mappages, vous pouvez exécuter la migration.

#### Création d’un workflow de migration {#create-migration-workflow}

Utilisez les mappages de dépendance de l’étape 1 pour configurer et exécuter votre migration.

**Format d’API**

```http
POST /migration/service/migrations
```

**Migration au niveau des sandbox**

Pour migrer tous les objets de prise de décision d’un sandbox à un autre :

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**Migration au niveau des offres**

Pour migrer des offres spécifiques uniquement, utilisez `requestLevel: "offer"` et ajoutez un tableau `offersList` :

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migration au niveau de la décision**

Pour migrer des décisions spécifiques uniquement, utilisez `requestLevel: "decision"` et ajoutez un tableau `decisionsList` :

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Surveillance du statut de migration {#poll-migration-status}

Interrogez le workflow de migration pour suivre sa progression.

**Format d’API**

```http
GET /migration/service/migrations/{id}
```

**Requête**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

**Résultats de la migration**

Lorsque le champ `status` affiche `Completed`, la migration a réussi. Le `result` de workflow comprend les éléments suivants :
* Mappages des objets migrés
* Tous les avertissements rencontrés lors de la migration

Lorsque le champ `status` s’affiche, `Failed` le tableau de `errors[]` et `result.error` champ pour en savoir plus sur le problème.

## Validation de la migration {#validate-migration}

Une fois la migration terminée, vérifiez que tous les objets ont été migrés correctement.

### Liste de contrôle de validation {#validation-checklist}

1. **Segments** - Vérifiez que tous les segments référencés se résolvent correctement dans le sandbox cible en fonction de vos mappages.
2. **Attributs** - Vérifiez que tous les attributs de profil et les attributs de contexte existent dans le sandbox cible et sont correctement mappés.
3. **Objets de prise de décision** - Consultez les objets migrés dans l’interface utilisateur de Journey Optimizer :
   * Offres (éléments de décision)
   * Règles d’éligibilité
   * Formules de classement
   * Stratégies de sélection
   * Politiques de décision
4. **Test du flux de données** - Si un flux de données a été créé, testez la diffusion d’exécution à l’aide de l’API Edge Interact.

### Exemple {#test-runtime-delivery}

Si votre migration a créé un flux de données, vous pouvez tester la diffusion de l’offre à l’aide de l’exemple suivant :

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Restaurer une migration {#rollback}

Si vous rencontrez des problèmes lors de la validation, vous pouvez annuler une migration terminée afin de restaurer le sandbox cible à son état précédent.

### Création d’un workflow de restauration {#create-rollback-workflow}

Lancez une restauration en créant un workflow de restauration qui fait référence à la migration que vous souhaitez annuler.

**Format d’API**

```http
POST /migration/service/rollbacks/{migrationWorkflowId}
```

Remplacez `{migrationWorkflowId}` par l’identifiant du workflow de migration que vous souhaitez restaurer.

**Requête**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### Surveillance du statut de restauration {#poll-rollback-status}

Recherchez le workflow de restauration pour suivre sa progression.

**Format d’API**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**Requête**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

## Gestion des workflows simultanés {#handle-concurrency}

L’API de migration permet à un seul workflow de s’exécuter à la fois par organisation. Si vous tentez de créer un workflow alors qu’un autre est en cours, vous recevrez une réponse d’erreur **409 Conflit** (« Un workflow est déjà en cours... »).

Dans ce cas, attendez que le workflow en cours soit terminé ou récupérez l’ID du workflow et interrogez son statut. Une fois le workflow en cours terminé, vous pouvez en créer un nouveau.

## Référence de mapping d’entités {#entity-mapping}

Lors de la migration de la gestion des décisions vers la prise de décision, les entités sont mappées comme suit :

| Gestion des décisions | Prise de décision |
|-------------------|-------------|
| Offre | Élément de décision |
| Collection d’offres | Collection d&#39;éléments |
| Règle d’éligibilité | Règle d’éligibilité |
| Formule de classement | Formule de classement |
| Décision | Stratégie de sélection + politique de décision |
| Campagne | *de Campaign (contenu de base uniquement)* |
| Emplacement | Configuration Surface + Canal |
| Balise | Balise unifiée |

## Nettoyage du workflow {#cleanup}

Les ressources de workflow ne peuvent être supprimées que par les utilisateurs et utilisatrices du service. Les opérations de suppression nécessitent un en-tête `If-Match` avec la valeur de `_etag` du workflow.

**Opérations de suppression disponibles :**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>La suppression de workflow n’est disponible que pour les comptes de service disposant des autorisations appropriées. Si vous devez supprimer une ressource de workflow, contactez votre administrateur ou administratrice système.

## Rubriques connexes {#related-topics}

* [Migration de la gestion des décisions vers la prise de décision](migrate-to-decisioning.md) - Découvrez les avantages et les fonctionnalités de la migration vers la prise de décision
* [Commencer avec la prise de décisions](gs-experience-decisioning.md)
* [Mécanismes de sécurisation et limitations des décisions](decisioning-guardrails.md)
* [Commencer à utiliser les API Decisioning](api-reference/getting-started.md)
