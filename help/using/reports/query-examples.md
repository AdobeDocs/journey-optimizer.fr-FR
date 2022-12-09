---
solution: Journey Optimizer
product: journey optimizer
title: Exemples de requêtes
description: Exemples de requêtes
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 26ad12c3-0a2b-4f47-8f04-d25a6f037350
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 0%

---

# Exemples de requêtes{#query-examples}

Cette section répertorie plusieurs exemples couramment utilisés pour interroger les événements d’étape du parcours dans le lac de données.

Assurez-vous que les champs utilisés dans vos requêtes ont des valeurs associées dans le schéma correspondant.

**Quelle est la différence entre id, instanceid et profileid ?**

* id: unique pour toutes les entrées d’événement d’étape. Deux événements d’étape différents ne peuvent pas avoir le même identifiant.
* instanceId : instanceID est le même pour tous les événements d’étape associés à un profil au sein d’une exécution de parcours. Si un profil entre de nouveau dans le parcours, un instanceId différent est utilisé. Ce nouvel instanceId sera le même pour tous les événements d’étape de l’instance réentrée (du début à la fin).
* profileID : l’identité du profil correspondant à l’espace de noms du parcours.

## Cas d’utilisation de base/requêtes courantes {#common-queries}

**Nombre de profils entrés dans un parcours au cours d’une certaine période**

Cette requête indique le nombre de profils distincts ayant rejoint le parcours donné au cours de la période donnée.

_Requête du lac de données_

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND _experience.journeyOrchestration.stepEvents.instanceType = 'unitary'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

**Le nombre d’erreurs qui se sont produites sur chaque noeud d’un parcours spécifique pendant une certaine durée**

_Requête du lac de données_

```sql
SELECT
_experience.journeyOrchestration.stepEvents.nodeName,
count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersiionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (_experience.journeyOrchestration.stepEvents.actionExecutionError not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginCode not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginError not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchError not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchErrorCode  not NULL
  )
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**Nombre d’événements ignorés d’un parcours spécifique au cours d’une certaine période**

_Requête du lac de données_

```sql
SELECT
count(_id) AS NUMBER_OF_EVENTS_DISCARDED
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersiionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

**Qu’advient-il d’un profil spécifique dans un parcours spécifique pendant une période spécifique ?**

_Requête du lac de données_

Cette requête renvoie, dans l’ordre chronologique, tous les événements d’étape et de service du profil et du parcours donnés pour la période spécifiée.

```sql
SELECT
timestamp,
_experience.journeyOrchestration.stepEvents.journeyVersionID,
_experience.journeyOrchestration.stepEvents.profileID,
_experience.journeyOrchestration.stepEvents.nodeName,
_experience.journeyOrchestration.stepEvents.journeyNodeProcessed,
_experience.journeyOrchestration.serviceType,
to_json(_experience.journeyOrchestration.profile),
to_json(_experience.journeyOrchestration.serviceEvents)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (
    _experience.journeyOrchestration.stepEvents.profileID='<profileID>'
    OR _experience.journeyOrchestration.profile.ID='<profileID>'
  );
ORDER BY timestamp;
```


## Erreurs de message/d’action {#message-action-errors}

**Liste de chaque erreur rencontrée dans les parcours**

Cette requête permet de répertorier chaque erreur rencontrée dans les parcours lors de l’exécution d’un message/d’une action.

_Requête du lac de données_

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName=<'message-name'>
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
```

_Exemple_

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName='Message - 100KB Email with Gateway and Kafkav2'
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
```

Cette requête renvoie toutes les erreurs différentes qui se sont produites lors de l’exécution d’une action dans un parcours, ainsi que le nombre de fois où elle s’est produite.

## Requêtes basées sur un profil {#profile-based-queries}

**Déterminer si un profil a participé à un parcours spécifique**

_Requête du lac de données_

```sql
SELECT count(distinct _id) FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_Exemple_

```sql
SELECT count(distinct _id) FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = 'ec9efdd0-8a7c-4d7a-a765-b2cad659fa4e' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

Le résultat doit être supérieur à 0. Cette requête renvoie le nombre exact d’entrées d’un profil dans un parcours.

**Recherche si un profil a été envoyé à un message spécifique**

Méthode 1 : si le nom de votre message n’est pas unique dans le parcours (il est utilisé à plusieurs endroits).

_Requête du lac de données_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='<NodeId in the UI corresponding to the message>' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_Exemple_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='17ae65a1-02dd-439d-b54e-b56a78520eba' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

Le résultat doit être supérieur à 0. Cette requête ne nous indique que si l’action du message a bien été exécutée côté parcours.

Méthode 2 : si le nom de votre message est unique dans le parcours.

_Requête du lac de données_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeName='<NodeName in the UI corresponding to the message>' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_Exemple_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='Message- 100KB Email' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

La requête renvoie la liste de tous les messages ainsi que leur nombre appelé pour le profil sélectionné.

**Recherche de tous les messages reçus par un profil au cours des 30 derniers jours**

_Requête du lac de données_

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.nodeType = 'action' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
```

_Exemple_

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.nodeType = 'action' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
```

La requête renvoie la liste de tous les messages ainsi que leur nombre appelé pour le profil sélectionné.

**Rechercher tous les parcours entrés par un profil au cours des 30 derniers jours**

_Requête du lac de données_

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
```

_Exemple_

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
```

La requête renvoie la liste de tous les noms de parcours, ainsi que le nombre de fois où le profil interrogé est entré dans le parcours.

**Nombre de profils qualifiés pour un parcours quotidien**

_Requête du lac de données_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.profileID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

_Exemple_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.profileID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '100' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

La requête renvoie, pour la période définie, le nombre de profils entrés chaque jour dans le parcours. Si un profil saisi via plusieurs identités, il sera comptabilisé deux fois. Si la rentrée est activée, le nombre de profils peut être dupliqué sur plusieurs jours s’il est rentré dans le parcours un autre jour.

## Requêtes relatives au segment de lecture {#read-segment-queries}

**Temps nécessaire pour terminer une tâche d’exportation de segments**

_Requête du lac de données_

```sql
select DATEDIFF (minute,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'queued') ,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'finished')) AS export_job_runtime;
```

_Exemple_

```sql
select DATEDIFF (minute,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'queued') ,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'finished')) AS export_job_runtime;
```

La requête renvoie la différence de temps, en minutes, entre le moment où la tâche d’exportation de segments a été mise en file d’attente et celui où elle s’est terminée.

**Nombre de profils qui ont été ignorés par le parcours car il s’agissait de doublons**

_Requête du lac de données_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

_Exemple_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours car il s’agissait de doublons.

**Nombre de profils ignorés par le parcours en raison d’un espace de noms non valide**

_Requête du lac de données_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

_Exemple_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours car ils contenaient un espace de noms non valide ou aucune identité pour cet espace de noms.

**Nombre de profils ignorés par le parcours en raison de l’absence de carte d’identité**

_Requête du lac de données_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

_Exemple_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours car la carte d’identité était manquante.

**Nombre de profils qui ont été ignorés par le parcours, car celui-ci se trouvait dans le noeud test et que le profil n’était pas un profil de test**

_Requête du lac de données_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

_Exemple_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours, car la tâche d’exportation a été exécutée en mode test, mais que l’attribut testProfile n’était pas défini sur true.

**Nombre de profils qui ont été ignorés par le parcours en raison d’une erreur interne**

_Requête du lac de données_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

_Exemple_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours en raison d’une erreur interne.

**Présentation du segment de lecture pour une version de parcours donnée**

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator'
```

Elle renvoie tous les événements de service liés à la version de parcours donnée. Nous pouvons suivre la chaîne des opérations :

* création de rubrique
* création de tâche d’exportation
* terminer la tâche d’exportation (avec des mesures sur les profils exportés)
* arrêt du traitement des workflows

Nous pouvons également détecter des problèmes tels que :

* erreurs lors de la création d’une tâche d’exportation ou de rubrique (y compris les dépassements de délai sur les appels d’API d’exportation de segments)
* tâches d’exportation pouvant être bloquées (dans le cas d’une version de parcours donnée, aucun événement n’est associé à la fin de la tâche d’exportation)
* problèmes de traitement, si nous avons reçu un événement de fin de tâche d’exportation, mais qu’aucun événement de fin de traitement de traitement de traitement de traitement n’a été envoyé

IMPORTANT : si aucun événement n’est renvoyé par cette requête, cela peut être dû à l’une des raisons suivantes :

* la version du parcours n’a pas atteint la planification
* si la version du parcours est censée déclencher la tâche d’exportation en appelant l’orchestrateur, un problème s’est produit sur le flux upstram : Problème sur le déploiement du parcours, l’événement commercial ou le problème avec le planificateur.

**Obtenir les erreurs de lecture de segment pour une version de parcours donnée**

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'ERROR_TOPIC_CREATION',
        'ERROR_EXPORTJOB_APICALL',
        'ERROR_EXPORTJOB_APICALL_TIMEOUT',
        'ERROR_EXPORTJOB_FAILED'
    )
```

**Obtention de l’état du traitement des tâches d’exportation**

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT 
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'INFO_EXPORTJOB_SUCCEEDED',
        'ERROR_EXPORTJOB_FAILED'
    )
```

Si aucun enregistrement n’est renvoyé, cela signifie que :

* une erreur s’est produite lors de la création d’une tâche de rubrique ou d’exportation
* la tâche d’exportation est toujours en cours d’exécution

**Obtention de mesures sur les profils exportés, y compris les enregistrements et les mesures de tâches d’exportation pour chaque tâche d’exportation**

_Requête du lac de données_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
 
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
  
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.EXPORTJOB_ID = T2.EXPORTJOB_ID
```

**Obtention de mesures agrégées (tâches d’exportation de segments et abandons) sur toutes les tâches d’exportation**

_Requête du lac de données_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.journey.versionID
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
          _experience.journeyOrchestration.journey.versionID
 
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.JOURNEYVERSION_ID = T2.JOURNEYVERSION_ID
```

Cette requête est différente de la précédente.

Elle renvoie les mesures globales d’une version de parcours donnée, quelles que soient les tâches pouvant avoir été exécutées pour celle-ci (dans le cas de parcours récurrents, les événements d’entreprise ont déclenché ceux qui utilisent la réutilisation des rubriques).

## Requêtes relatives à la qualification du segment {#segment-qualification-queries}

**Profil ignoré en raison d’une réalisation de segment différente de celle configurée**

_Requête du lac de données_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

_Exemple_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = 'a868f3c9-4888-46ac-a274-94cdf1c4159d' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

Cette requête renvoie tous les identifiants de profil qui ont été ignorés par la version du parcours en raison d’une mauvaise réalisation du segment.

**Événements de qualification de segment ignorés par toute autre raison pour un profil spécifique**

_Requête du lac de données_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = '<profile-id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

_Exemple_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = 'mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

Cette requête renvoie tous les événements (événements externes/événements de qualification de segment) qui ont été ignorés pour une autre raison d’un profil.

## Requêtes basées sur un événement {#event-based-queries}

**Vérification de la réception d’un événement commercial pour un parcours**

_Requête du lac de données_

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.nodeName = '<node-name-corresponding-to-business-event>' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '<last x hours>' hour)
```

_Exemple_

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = 'b1093bd4-11f3-44cc-961e-33925cc58e18' AND
_experience.journeyOrchestration.stepEvents.nodeName = 'TEST_MLTrainingSession' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '6' hour)
```

**Vérifier si un événement externe d’un profil a été ignoré car aucun parcours associé n’a été trouvé**

_Requête du lac de données_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '<eventId>' AND
_experience.journeyOrchestration.profile.ID = '<profileId>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

_Exemple_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '515bff852185e434ca5c83bcfc4f24626b1545ca615659fc4cfff91626ce61a6' AND
_experience.journeyOrchestration.profile.ID = 'mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

**Vérifier si un événement externe d’un profil a été ignoré pour une autre raison**

_Requête du lac de données_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='<eventID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

_Exemple_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='81c51be978d8bdf9ef497076b3e12b14533615522ecea9f5080a81c736491656' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

**Vérifier le nombre de tous les événements ignorés par stateMachine par errorCode**

_Requête du lac de données_

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

_Exemple_

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

**Vérifier tous les événements ignorés car la rentrée n’était pas autorisée**

_Requête du lac de données_

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

_Exemple_

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

## Requêtes courantes basées sur un parcours {#journey-based-queries}

**Nombre de parcours actifs par jour**

_Requête du lac de données_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

_Exemple_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '100' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

La requête renvoie, pour la période définie, le nombre de parcours uniques qui se sont déclenchés chaque jour. Un seul parcours déclenchant plusieurs jours sera comptabilisé une fois par jour.

## Requêtes sur les instances de parcours {#journey-instances-queries}

**Nombre de profils dans un état spécifique à une heure spécifique**

_Requête du lac de données_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = '<specific node name>' AND
        <filter on time for profile in specific node>
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in (<list of next node names from the specific node>)
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'<date pattern>') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_Exemple_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = 'slack_bso_tests - test1' AND
        T1.TS > (now() - interval '18 hour')
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in ('slack_bso_tests - test2')
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

**Nombre de profils qui ont quitté le parcours au cours de la période spécifique**

_Requête du lac de données_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_Exemple_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

**Nombre de profils ayant quitté le parcours au cours de la période spécifique avec le noeud/le statut**

_Requête du lac de données_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

_Exemple_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

