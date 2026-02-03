---
solution: Journey Optimizer
product: journey optimizer
title: Exemples de requêtes
description: Exemples de requêtes
feature: Reporting, Journeys
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 26ad12c3-0a2b-4f47-8f04-d25a6f037350
source-git-commit: 4a15ee3ac4805880ce80f788e4619b501afb3d8b
workflow-type: tm+mt
source-wordcount: '3337'
ht-degree: 77%

---

# Exemples de requêtes{#query-examples}

Cette section fournit des exemples couramment utilisés pour interroger les événements d’étape du parcours dans le lac de données. Avant de s’intéresser à des cas d’utilisation spécifiques, il est important de comprendre les identifiants clés utilisés dans les données d’événement de parcours.

Assurez-vous que les champs utilisés dans vos requêtes ont des valeurs associées dans le schéma correspondant.

## Compréhension des identifiants clés {#key-identifiers}

+++Quelle est la différence entre ID, instanceID et profileID ?

* ID : unique pour toutes les entrées d’événement d’étape. Deux événements d’étape différents ne peuvent pas avoir le même identifiant.
* instanceID : l’instanceID est le même pour tous les événements d’étape associés à un profil lors de l’exécution d’un parcours. Si un profil rejoint à nouveau le parcours, un instanceID différent est utilisé. Ce nouvel instanceID sera le même pour tous les événements d’étape de cette nouvelle instance (du début à la fin).
* profileID : identité du profil correspondant à l’espace de noms du parcours.

>[!NOTE]
>
>À des fins de dépannage, nous vous recommandons d’utiliser journeyVersionID au lieu de journeyVersionName lors de l’interrogation de parcours. Pour plus d’informations sur les attributs des propriétés de parcours, consultez [cette section](../building-journeys/expression/journey-properties.md#journey-properties-fields).

+++

## Cas d’utilisation de base/requêtes courantes {#common-queries}

+++Nombre de profils ayant rejoint un parcours au cours d’une période donnée

Cette requête donne le nombre de profils distincts étant entrés dans le parcours donné dans la période donnée.

_Requête du lac de données_

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND _experience.journeyOrchestration.stepEvents.instanceType = 'unitary'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).

+++

+++Règle ayant empêché un profil de rejoindre un parcours donné

Cette requête renvoie les informations sur l’ensemble de règles et les règles rejetées lorsqu’un profil ne peut pas rejoindre un parcours en raison des règles de limitation ou d’éligibilité.

_Exemple_

```sql
SELECT 
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.ID AS RULESET_ID,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.name AS RULESET_NAME,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.rejectedRules.ID AS RULE_ID,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.rejectedRules.name AS RULE_NAME
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard'
AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID='3855072d-79c3-438a-a5c3-c77fd6843812'
AND
    timestamp >= to_date('2025-05-16')
```

+++

+++Quelle règle a empêché un profil de recevoir une action de parcours ?

Cette requête renvoie les détails de l’événement d’étape pour les profils qui ont été ignorés lors d’un parcours et qui n’ont pas reçu d’action de parcours. Elle permet d’identifier pourquoi les profils ont été ignorés en raison de règles métier telles que les contraintes liées aux heures creuses.

_Requête du lac de données_

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.profileID,
    _experience.journeyOrchestration.stepEvents.instanceID,
    _experience.journeyOrchestration.stepEvents.journeyID,
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.actionExecutionError,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    DATE(timestamp),
    timestamp
FROM journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = '<eventType>' AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>' AND
    _experience.journeyOrchestration.stepEvents.instanceID = '<instanceID>';
```

_Exemple_

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.profileID,
    _experience.journeyOrchestration.stepEvents.instanceID,
    _experience.journeyOrchestration.stepEvents.journeyID,
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.actionExecutionError,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    DATE(timestamp),
    timestamp
FROM journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'quietHours' AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID = '6f21a072-6235-4c39-9f6a-9d9f3f3b2c3a' AND
    _experience.journeyOrchestration.stepEvents.instanceID = 'unitary_089dc93a-1970-4875-9660-22433b18e500';
```


Les résultats de la requête affichent les champs qui permettent de savoir pourquoi les profils ont été ignorés :

* **actionExecutionError** : lorsque la valeur est définie sur `businessRuleProfileDiscarded`, cela indique que le profil a été ignoré en raison d’une règle métier. Le champ `eventType` fournit des détails supplémentaires sur la règle métier qui a provoqué l’exclusion.

* **eventType** : indique le type de la règle métier à l’origine de l’exclusion :
   * `quietHours` : le profil a été ignoré en raison de la configuration des heures creuses.
   * `forcedDiscardDueToQuietHours` : le profil a été ignoré de force, car la limite du mécanisme de sécurisation pour les profils en heures creuses a été atteinte.

+++

+++Nombre d’erreurs qui se sont produites sur chaque nœud d’un parcours spécifique pendant une certaine période

Cette requête comptabilise les profils distincts qui ont rencontré des erreurs à chaque nœud d’un parcours, regroupés par nom de nœud. Elle inclut tous les types d’erreurs d’exécution d’action et de récupération.

_Requête du lac de données_

```sql
SELECT
_experience.journeyOrchestration.stepEvents.nodeName,
count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (_experience.journeyOrchestration.stepEvents.actionExecutionError is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginCode is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginError is not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchError is not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchErrorCode is not NULL
  )
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

+++

+++Nombre d’événements rejetés d’un parcours spécifique pendant une certaine période

Cette requête compte le nombre total d’événements qui ont été supprimés d’un parcours. Elle filtre divers codes d’événement de rejet, y compris les erreurs de traitement d’export de segments, les rejets du Dispatcher et les rejets de machine d’état.

_Requête du lac de données_

```sql
SELECT
count(_id) AS NUMBER_OF_EVENTS_DISCARDED
FROM journey_step_events
WHERE (
   _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'error'
   OR _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard'
   OR _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode = 'discard'
   OR _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode is not null
)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

+++

+++Qu’advient-il d’un profil spécifique dans un parcours spécifique pendant une période spécifique ?

Cette requête renvoie tous les événements d’étape et de service pour le profil et le parcours donnés pour la période spécifiée dans l’ordre chronologique.

_Requête du lac de données_

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

+++

+++Durée écoulée entre deux nœuds 

Ces requêtes peuvent être utilisées notamment pour estimer le temps passé dans une activité d’attente. Vous pouvez ainsi vous assurer que l’activité d’attente est correctement configurée.

_Requête du lac de données_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    T1.INSTANCE_ID AS INSTANCE_ID,
    T1.NODE_NAME AS START_NODE_NAME,
    T2.NODE_NAME AS END_NODE_NAME,
    DATEDIFF(millisecond,T1.TS_START,T2.TS_END) AS ELAPSED_TIME_MS
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

_Requête du lac de données_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    AVG(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS AVERAGE_ELAPSED_TIME,
    MIN(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MIN_ELAPSED_TIME,
    MAX(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MAX_ELAPSED_TIME
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

+++

+++Vérification des détails d’un événement serviceEvent 

Le jeu de données Événements de l’étape du parcours contient tous les événements stepEvents et serviceEvents. Les événements stepEvents sont utilisés dans les rapports, dans la mesure où ils se rapportent aux activités (événement, actions, etc.) des profils d’un parcours. Les événements serviceEvents sont stockés dans le même jeu de données et indiquent des informations supplémentaires à des fins de débogage, comme la raison du rejet d’un événement d’expérience.

Voici un exemple de requête permettant de vérifier le détail d’un événement serviceEvent :

_Requête du lac de données_

```sql
SELECT

     _experience.journeyOrchestration.profile.ID, 
     _experience.journeyOrchestration.journey.versionID, 
     to_json(_experience.journeyOrchestration.serviceEvents) 

FROM journey_step_event 

WHERE _experience.journeyOrchestration.serviceType is not null;
```

## Erreurs de message/d’action {#message-action-errors}

+++Liste de chaque erreur rencontrée dans les parcours

Cette requête permet de répertorier chaque erreur rencontrée dans les parcours lors de l’exécution d’un message/d’une action.

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) AS ERROR_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName = '<message-name>'
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
ORDER BY ERROR_COUNT DESC;
```

_Exemple de sortie_

| actionExecutionError | ERROR_COUNT |
|---|---|
| TimedOut | 145 |
| ErrorConnecting | 87 |
| InvalidResponse | 23 |

Cette requête renvoie toutes les erreurs différentes qui se sont produites lors de l’exécution d’une action dans un parcours, ainsi que le nombre de fois où chaque erreur s’est produite, classées par fréquence.

+++

## Requêtes basées sur un profil {#profile-based-queries}

+++Rechercher si un profil a rejoint un parcours spécifique

Cette requête vérifie si un profil spécifique a rejoint un parcours en comptant les événements associés à cette combinaison de profil et de parcours.

```sql
SELECT count(distinct _id) AS EVENT_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_Exemple de sortie_

| EVENT_COUNT |
|---|
| 3 |

Cette requête renvoie le nombre exact de fois où un profil est entré dans un parcours. Un résultat supérieur à 0 confirme que le profil est entré dans le parcours.

+++

+++Rechercher si un message spécifique a été envoyé à un profil

Méthode 1 : si le nom de votre message n’est pas unique dans le parcours (il est utilisé à plusieurs endroits).

```sql
SELECT count(distinct _id) AS MESSAGE_SENT_COUNT 
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.nodeID = '<NodeId in the UI corresponding to the message>' 
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_Exemple de sortie_

| MESSAGE_SENT_COUNT |
|---|
| 1 |

Un résultat supérieur à 0 confirme l’exécution réussie de l’action de message. Cette requête ne nous indique que si l’action du message a bien été exécutée côté parcours.

Méthode 2 : si le nom de votre message est unique dans le parcours.

```sql
SELECT count(distinct _id) AS MESSAGE_SENT_COUNT 
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.nodeName = '<NodeName in the UI corresponding to the message>' 
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_Exemple de sortie_

| MESSAGE_SENT_COUNT |
|---|
| 1 |

La requête renvoie le nombre de fois où le message a été appelé avec succès pour le profil sélectionné.

+++

+++Rechercher tous les messages reçus par un profil au cours des 30 derniers jours

Cette requête récupère toutes les actions de message exécutées avec succès pour un profil spécifique au cours des 30 derniers jours, regroupées par nom de message.

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName AS MESSAGE_NAME, 
       count(distinct _id) AS MESSAGE_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.nodeType = 'action' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' 
AND timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
ORDER BY MESSAGE_COUNT DESC;
```

_Exemple de sortie_

| MESSAGE_NAME | MESSAGE_COUNT |
|---|---|
| Welcome Email | 1 |
| Recommandation de produit | 3 |
| Rappel d’abandon de panier | 2 |
| Newsletter Hebdomadaire | 4 |

La requête renvoie la liste de tous les messages ainsi que leur nombre appelés pour le profil sélectionné.

+++

+++Rechercher tous les parcours qu’un profil a rejoint au cours des 30 derniers jours

Cette requête renvoie tous les parcours rejoints par un profil spécifique au cours des 30 derniers jours, ainsi que le nombre d’entrées pour chaque parcours.

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME, 
       count(distinct _id) AS ENTRY_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeType = 'start' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' 
AND timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
ORDER BY ENTRY_COUNT DESC;
```

_Exemple de sortie_

| NOM_parcours | ENTRY_COUNT |
|---|---|
| Parcours de bienvenue v2 | 1 |
| Recommandations de produit | 5 |
| Campagne de réengagement | 2 |

La requête renvoie la liste de tous les noms de parcours ainsi que le nombre de fois où le profil interrogé a rejoint chaque parcours.

+++

+++Nombre de profils qualifiés pour un parcours par jour

Cette requête fournit une répartition quotidienne du nombre de profils distincts ayant rejoint un parcours dans une période spécifiée.

```sql
SELECT DATE(timestamp) AS ENTRY_DATE, 
       count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS PROFILES_COUNT 
FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) DESC;
```

_Exemple de sortie_

| ENTRY_DATE | PROFILES_COUNT |
|---|---|
| 25/11/2024 | 1 245 |
| 24/11/2024 | 1 189 |
| 23/11/2024 | 15 340 |
| 22/11/2024 | 1 205 |
| 21/11/2024 | 1 167 |

La requête renvoie, pour la période définie, le nombre de profils ayant rejoint le parcours chaque jour. Si un profil a rejoint le parcours via plusieurs identités, il sera comptabilisé deux fois. Si la reprise est activée, le nombre de profils peut être dupliqué sur différents jours s’il est entré à nouveau dans le parcours un autre jour.

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).


+++

## Requêtes relatives à la lecture d’audience {#read-segment-queries}

+++Temps nécessaire pour terminer un traitement d’export d’audiences

Cette requête calcule la durée d’un traitement d’export d’audience en recherchant la différence de temps entre le moment où le traitement a été mis en file d’attente et celui où il s’est terminé.

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

La requête renvoie la différence de temps, en minutes, entre le moment où le traitement d’export d’audiences a été mis en file d’attente et celui où il s’est terminé.

+++

+++Nombre de profils qui ont été ignorés par le parcours, car il s’agissait de doublons.

Cette requête comptabilise le nombre de profils distincts qui ont été ignorés en raison d’erreurs de duplication des instances lors de l’activité Lecture d’audience.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours, car il s&#39;agissait de doublons.

+++

+++Nombre de profils qui ont été ignorés par le parcours en raison d&#39;un espace de noms non valide

Cette requête renvoie le nombre de profils qui ont été ignorés, car ils contenaient un espace de noms non valide ou une identité manquante pour l’espace de noms requis.

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours, car ils contenaient un espace de noms non valide ou aucune identité pour cet espace de noms.

+++

+++Nombre de profils qui ont été ignorés par le parcours en raison de l&#39;absence de carte d&#39;identité

Cette requête comptabilise les profils qui ont été ignorés, car il leur manquait un mappage d’identité requis pour l’exécution du parcours.

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours, car la carte d&#39;identité était manquante.

+++

+++Nombre de profils qui ont été ignorés par le parcours, car celui-ci se trouvait dans le nœud de test et que le profil n&#39;était pas un profil de test

Cette requête identifie les profils qui ont été ignorés lorsque le parcours était en cours d’exécution en mode test, mais dont l’attribut testProfile n’était pas défini sur vrai.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours, car le traitement d’export a été exécuté en mode test, mais l’attribut testProfile des profils n’était pas défini sur vrai.

+++

+++Nombre de profils qui ont été ignorés par le parcours en raison d’une erreur interne

Cette requête renvoie le nombre de profils qui ont été ignorés en raison d’erreurs système internes lors de l’exécution du parcours.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

La requête renvoie tous les identifiants de profil qui ont été ignorés par le parcours en raison d&#39;une erreur interne.

+++

+++Vue d’ensemble de la lecture d’audience pour une version de parcours donnée

Cette requête fournit une vue d’ensemble complète de l’activité Lecture d’audience, y compris les détails du traitement d’export de segments, les codes d’événement, les statuts et le nombre de profils pour toutes les étapes du processus d’export d’audience.

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

Elle renvoie tous les événements de service liés à la version de parcours donnée. Nous pouvons suivre la chaîne des opérations :

* création de rubrique
* création de tâche d’export
* arrêt de tâche d’export (avec des mesures sur les profils exportés)
* arrêt de traitement secondaire

Nous pouvons également détecter des problèmes tels que :

* erreurs lors de la création d’un traitement d’export ou de rubrique (y compris les temporisations sur les appels API d’export d’audience)
* tâches d’export pouvant être bloquées (dans le cas d’une version de parcours donnée où aucun événement n’est associé à la fin de la tâche d’export)
* problèmes secondaires, si nous avons reçu un événement de fin de tâche d&#39;exportation, mais pas de fin de traitement secondaire

IMPORTANT : si aucun événement n&#39;est renvoyé par cette requête, cela peut être dû à l&#39;une des raisons suivantes :

* la version du parcours n&#39;a pas atteint le planning
* si la version de parcours est censée avoir déclenché le traitement d’export en appelant l’orchestrateur, un problème s’est produit dans le flux en amont : problème lors du déploiement de parcours, événement métier ou problème lié au planificateur.

+++


+++Obtention des erreurs de lecture d’audience pour une version de parcours donnée

Cette requête filtre les codes d’événement d’erreur spécifiques liés aux échecs de lecture d’audience, tels que les erreurs de création de rubrique, les erreurs d’appel API, les temporisations et les traitements d’export ayant échoué.

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

+++

+++Obtention de l&#39;état du traitement des tâches d&#39;exportation

Cette requête récupère le statut des traitements d’export d’audience, indiquant s’ils ont réussi ou échoué avec les mesures d’export de profils.

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

Si aucun enregistrement n&#39;est renvoyé, cela signifie que :

* une erreur s’est produite lors de la création d’un traitement d’export ou rubrique
* la tâche d’export est toujours en cours d’exécution

+++

+++Obtention de mesures sur les profils exportés, y compris les abandons et les mesures de tâches d’export pour chaque tâche d’export

Cette requête combine le nombre de profils ignorés avec les mesures de traitement d’export afin de fournir une vue complète des performances d’export d’audience pour chaque traitement d’export.

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

+++

+++Obtention de mesures agrégées (traitements d’export d’audiences et abandons) sur tous les traitements d’export

Cette requête agrège les mesures globales de tous les traitements d’export pour une version de parcours donnée. Cette requête est utile pour les parcours récurrents ou les parcours déclenchés par un événement métier avec réutilisation de rubrique.

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

Elle renvoie les mesures globales d&#39;une version de parcours donnée, quelles que soient les tâches qui ont pu être exécutées pour celle-ci (dans le cas de parcours récurrents, les événements métier ont déclenché les tâches exploitant la réutilisation de rubrique).

+++

## Requêtes relatives à la qualification de l’audience {#segment-qualification-queries}

+++Profil rejeté en raison d’une réalisation d’audience différente de celle configurée

Cette requête identifie les profils qui ont été ignorés, car leur statut de réalisation de l’audience ne correspondait pas à la configuration de la qualification d’audience du parcours (par exemple, configuré pour « rejoint », mais profil « sorti »).

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

Cette requête renvoie tous les identifiants de profil qui ont été ignorés par la version de parcours en raison d’une réalisation d’audience incorrecte.

+++

+++Événements de qualification d’audience rejetés pour toute autre raison pour un profil spécifique

Cette requête récupère toutes les qualifications d’audience ou tous les événements externes qui ont été ignorés pour un profil spécifique en raison d’erreurs de service internes.

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

Cette requête renvoie tous les événements (événements externes/événements de qualification d’audience) qui ont été ignorés pour une autre raison pour un profil.

+++

## Requêtes basées sur un événement {#event-based-queries}

+++Vérifier si un événement métier a été reçu pour un parcours

Cette requête comptabilise le nombre de fois qu’un événement métier a été reçu par un parcours, regroupé par date, au cours d’une période spécifiée.

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.nodeName = '<node-name-corresponding-to-business-event>' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '<last x hours>' hour)
```

+++

+++Vérifier si l’événement externe d’un profil a été rejeté, car aucun parcours associé n’a été trouvé

Cette requête identifie le moment où un événement externe pour un profil spécifique a été ignoré, car aucun parcours actif ou correspondant n’était configuré pour recevoir cet événement.

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '<eventId>' AND
_experience.journeyOrchestration.profile.ID = '<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).

+++

+++Vérifier si un événement externe d’un profil a été rejeté pour toute autre raison

Cette requête récupère les événements externes qui ont été ignorés pour un profil spécifique en raison d’erreurs de service internes, ainsi que l’identifiant d’événement et le code d’erreur.

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='<eventID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).

+++

+++Vérifier le nombre de tous les événements rejetés par stateMachine par errorCode

Cette requête agrège tous les événements ignorés par la machine d’état de parcours, regroupés par code d’erreur afin d’identifier les raisons les plus courantes des abandons.

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).

+++

+++Vérifier tous les événements rejetés, car une nouvelle entrée n’était pas autorisée

Cette requête identifie tous les événements qui ont été ignorés, car un profil a tenté de rejoindre à nouveau un parcours alors qu’une nouvelle entrée n’était pas autorisée dans la configuration du parcours.

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).

+++

## Requêtes pour les profils engageables {#engageable-profiles-queries}

Ces requêtes vous aident à surveiller et à analyser votre nombre de profils engageables. Un profil engageable est un profil unique qui a été engagé par le biais de parcours ou de campagnes au cours des 12 derniers mois. En savoir plus sur [Profils engageables et utilisation de la licence](../audience/license-usage.md#what-is-engageable-profile).

>[!IMPORTANT]
>
>**Bonnes pratiques pour interroger des profils pouvant être engagés :**
>* Assurez-vous que chaque champ non agrégé est inclus dans la clause `GROUP BY`
>* Évitez de référencer des jeux de données qui n’existent pas dans votre sandbox : confirmez les noms des jeux de données dans l’interface utilisateur de Platform
>* Utilisez des `distinct` lors du comptage des profils uniques pour éviter les doublons dans les espaces de noms d’identité
>* Lors de l’utilisation de `LIMIT`, placez-le à la fin de la requête après `ORDER BY` clauses .

+++Comptage des profils uniques engagés par un parcours spécifique

Cette requête renvoie le nombre de profils distincts qui ont été engagés par un parcours spécifique, ce qui contribue au nombre de profils engageables.

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND timestamp > (now() - interval '12' month);
```

Cette requête vous aide à comprendre le nombre de profils uniques qu’un parcours spécifique a contribué au nombre de vos [profils engageables](../audience/license-usage.md) au cours des 12 derniers mois.

+++

+++Compter les profils engagés par parcours au cours des 12 derniers mois

Cette requête affiche le nombre de profils uniques engagés par chaque parcours dans votre organisation au cours des 12 derniers mois, ce qui vous aide à identifier les parcours qui contribuent le plus au nombre de vos [profils engageables](../audience/license-usage.md).

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.journeyVersionID AS JOURNEY_VERSION_ID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '12' month)
GROUP BY 
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName
ORDER BY ENGAGED_PROFILES DESC;
```

_Exemple de sortie_

| PARCOURS_VERSION_ID | NOM_parcours | ENGAGED_PROFILES |
|---|---|---|
| 67b14482-143e-4f83-9cf5-cfec0fca3d26 | Bienvenue dans Campaign v2 | 125 450 |
| a3c21b89-456d-4e21-b8f3-9a8e7c6d5432 | Parcours de lancement du produit | 98 230 |
| f9e8d7c6-b5a4-3210-9876-543210fedcba | Flux de réengagement | 45 670 |

Cette sortie vous permet d’identifier les parcours qui impliquent le plus de profils et qui contribuent le plus significativement au nombre de profils engageables.

>[!NOTE]
>
>Cette requête regroupe à la fois les `journeyVersionID` et les `journeyVersionName`. Les deux champs doivent être inclus dans la clause `GROUP BY`, car ils sont sélectionnés dans la requête. L’omission de champs de la clause `GROUP BY` entraîne l’échec de la requête.

+++

+++Compter les profils engagés par les parcours quotidiennement au cours des 30 derniers jours

Cette requête fournit une répartition quotidienne des nouveaux profils engagés, ce qui vous aide à identifier les pics de nombre [Profils engageables](../audience/license-usage.md).

```sql
SELECT 
    DATE(timestamp) AS ENGAGEMENT_DATE,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '30' day)
GROUP BY DATE(timestamp)
ORDER BY ENGAGEMENT_DATE DESC;
```

_Exemple de sortie_

| ENGAGEMENT_DATE | ENGAGED_PROFILES |
|---|---|
| 25/11/2024 | 8 450 |
| 24/11/2024 | 7 820 |
| 23/11/2024 | 125 340 |
| 22/11/2024 | 9 230 |
| 21/11/2024 | 8 670 |

Cette sortie vous permet de surveiller les tendances quotidiennes et d’identifier lorsqu’un grand nombre de profils sont engagés. Dans cet exemple, le 23 novembre montre un pic significatif (125 340 profils) par rapport à l’engagement quotidien type (environ 8 000 profils), ce qui justifierait une enquête pour déterminer quel parcours ou quelle campagne a provoqué l’augmentation de votre nombre de [profils engageables](../audience/license-usage.md).

+++

+++Identifier les parcours qui ont récemment impliqué de grandes audiences

Cette requête permet d’identifier les parcours qui ont engagé un grand nombre de nouveaux profils au cours des dernières périodes, ce qui peut expliquer des augmentations soudaines du nombre [de profils engageables](../audience/license-usage.md).

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.journeyVersionID AS JOURNEY_VERSION_ID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME,
    DATE(timestamp) AS ENGAGEMENT_DATE,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '7' day)
AND _experience.journeyOrchestration.stepEvents.nodeType = 'start'
GROUP BY 
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName,
    DATE(timestamp)
HAVING count(distinct _experience.journeyOrchestration.stepEvents.profileID) > 1000
ORDER BY ENGAGEMENT_DATE DESC, ENGAGED_PROFILES DESC;
```

_Exemple de sortie_

| PARCOURS_VERSION_ID | NOM_parcours | ENGAGEMENT_DATE | ENGAGED_PROFILES |
|---|---|---|---|
| 67b14482-143e-4f83-9cf5-cfec0fca3d26 | Campagne du Vendredi noir | 23/11/2024 | 125 340 |
| a3c21b89-456d-4e21-b8f3-9a8e7c6d5432 | Parcours de lancement du produit | 22/11/2024 | 45 230 |
| f9e8d7c6-b5a4-3210-9876-543210fedcba | Newsletter des fêtes | 21/11/2024 | 32 150 |

Cette requête filtre les parcours qui ont impliqué plus de 1 000 profils par jour au cours des 7 derniers jours. La sortie indique quels parcours et dates spécifiques sont responsables des engagements de profil volumineux. Ajustez le seuil de la clause de `HAVING` en fonction de vos besoins (par exemple, remplacez `> 1000` par `> 10000` pour des seuils plus élevés).

+++

+++Nombre total de profils uniques engagés sur tous les parcours au cours des 12 derniers mois

Cette requête fournit un nombre de profils uniques engagés dans tous les parcours au cours des 12 derniers mois, ce qui vous donne un aperçu de votre engagement basé sur les parcours.

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS TOTAL_ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '12' month);
```

_Exemple de sortie_

| TOTAL_ENGAGED_PROFILES |
|---|
| 2 547 890 |

Ce nombre unique représente le nombre total de profils uniques qui ont été engagés par au moins un parcours au cours des 12 derniers mois.

>[!NOTE]
>
>Cette requête comptabilise des identifiants de profil distincts dans le jeu de données d’événements d’étape de parcours. Le nombre réel de profils engageables affiché dans le [Tableau de bord d’utilisation de la licence](../audience/license-usage.md) peut différer légèrement, car il inclut également les profils engagés dans des campagnes et d’autres fonctionnalités de Journey Optimizer autres que parcours.

+++

## Requêtes courantes basées sur des parcours {#journey-based-queries}

+++Nombre de parcours actifs quotidiens

Cette requête renvoie un nombre quotidien de versions de parcours uniques qui avaient une activité, ce qui vous permet de comprendre les modèles d’exécution de parcours au fil du temps.

```sql
SELECT DATE(timestamp) AS ACTIVITY_DATE, 
       count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) AS ACTIVE_JOURNEYS
FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) DESC;
```

_Exemple de sortie_

| ACTIVITY_DATE | PARCOURS_ACTIFS |
|---|---|
| 25/11/2024 | 12 |
| 24/11/2024 | 15 |
| 23/11/2024 | 14 |
| 22/11/2024 | 11 |
| 21/11/2024 | 13 |

La requête renvoie, pour la période définie, le nombre de parcours uniques qui se déclenchent chaque jour. Un seul parcours qui se déclenche plusieurs jours sera comptabilisé une fois par jour.


+++

## Requêtes sur les instances du parcours {#journey-instances-queries}

+++Nombre de profils dans un état spécifique à une heure spécifique

Cette requête utilise des expressions de table communes (CTE) pour identifier les profils qui attendent actuellement à un nœud spécifique dans un parcours en recherchant les profils qui sont passés par le nœud mais qui ne sont pas encore passés aux nœuds suivants.

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

+++

+++Nombre de profils qui ont quitté le parcours au cours de la période spécifique

Cette requête comptabilise les instances de parcours qui se sont fermées au cours d’une période spécifiée, y compris les sorties dues à des achèvements, des erreurs, des temporisations ou des erreurs de limitation.

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

+++

+++Nombre de profils ayant quitté le parcours pendant la période spécifique avec le nœud/l&#39;état

Cette requête fournit une répartition détaillée des sorties de parcours, indiquant le nom du nœud et le statut de sortie pour chaque instance de sortie afin d’identifier où et pourquoi les profils ont quitté le parcours.

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

+++

## Requêtes liées aux mesures de performances des actions personnalisées {#query-custom-action}

+++ Nombre total d’appels réussis, d’erreurs et de requêtes pour chaque seconde de chaque point d’entrée sur une période spécifique

Cette requête fournit des mesures de performances pour les actions HTTP personnalisées, notamment le nombre total d’appels, les appels réussis, le nombre d’erreurs par type (4xx, 5xx, temporisations, limitations) et le débit en requêtes par seconde pour chaque point d’entrée.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (<actionExecutionOriginStartTime filter> OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND <timestamp filter>))
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND timestamp > (now() - interval '1' day)))
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++ Série temporelle d’appels réussis, d’erreurs et de débits pour chaque point d’entrée sur une période spécifique

Cette requête fournit les mêmes mesures de performances que la requête précédente, mais organisées sous la forme d’une série temporelle, montrant comment les performances des points d’entrée varient au fil du temps avec une granularité minute par minute.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(COALESCE(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, timestamp), 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (<actionExecutionOriginStartTime filter> OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND
           <timestamp filter>))
GROUP BY 
    ENDPOINT, SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(COALESCE(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, timestamp), 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND
           timestamp > (now() - interval '1' day)))
GROUP BY 
    ENDPOINT, SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++Latence de réponse de chaque point d’entrée aux 50e, 95e, 99e et 99,9e percentiles sur une période spécifique

Cette requête calcule les centiles du temps de réponse pour les points d’entrée d’action personnalisés, ce qui vous permet de comprendre la distribution de la latence et d’identifier les valeurs aberrantes de performance à différents seuils de centile.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS SUCCESSFUL_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS SUCCESSFUL_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++Série temporelle de percentiles de latence de réponse pour chaque point d’entrée sur une période spécifique

Cette requête fournit des centiles de latence organisés sous la forme d’une série temporelle, ce qui vous permet de suivre l’évolution des temps de réponse des points d’entrée au fil du temps à différents niveaux de centile.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,    
    COUNT(1) AS SUCCESSFUL_CALLS,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,    
    COUNT(1) AS SUCCESSFUL_CALLS,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++ Temps d’attente en file d’attente sur des points d’entrée encombrés aux 50e et 95e percentiles sur une période spécifique

Cette requête analyse les temps d’attente dans la file d’attente pour les points d’entrée limités, en affichant les temps d’attente des 50e et 95e centiles pour vous permettre de comprendre l’impact de la limitation sur vos actions personnalisées.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++ Série temporelle de percentiles de temps d’attente en file d’attente pour chaque point d’entrée encombré

Cette requête fournit des centiles de temps d’attente de file d’attente sous la forme d’une série temporelle, ce qui vous permet de surveiller l’impact de la limitation sur les temps d’attente au fil du temps pour chaque point d’entrée.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++ Nombre d’erreurs par type et code pour un point d’entrée spécifique sur une période spécifique

Cette requête fournit une répartition détaillée des erreurs pour un point d’entrée spécifique, regroupées par type d’erreur et code d’erreur, y compris des informations sur les tentatives de reprise.

_Requête du lac de données_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionExecutionError AS ERROR_TYPE,
    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode AS ERROR_CODE,
    COUNT(1) AS CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionOriginError IS NOT NULL THEN 1 END) AS CALLS_WITH_RETRY
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint = '<endpoint URI>' AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL AND
    (<actionExecutionOriginStartTime filter>) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND <timestamp filter>))
GROUP BY 
    ERROR_TYPE, ERROR_CODE
ORDER BY
    ERROR_TYPE, ERROR_CODE;
```

_Exemple_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionExecutionError AS ERROR_TYPE,
    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode AS ERROR_CODE,
    COUNT(1) AS CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionOriginError IS NOT NULL THEN 1 END) AS CALLS_WITH_RETRY
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint = 'https://example.com/my/endpoint' AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND timestamp > (now() - interval '1' day)))
GROUP BY 
    ERROR_TYPE, ERROR_CODE
ORDER BY
    ERROR_TYPE, ERROR_CODE;
```

+++

