---
solution: Journey Optimizer
product: journey optimizer
title: Exemples de requêtes de jeux de données
description: Exemples de requêtes de jeux de données
feature: Journeys, Reporting, Use Cases, Datasets, Data Management
topic: Content Management
role: Developer, Admin
level: Experienced
keywords: jeu de données, optimizer, cas d’utilisation
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
TQID: https://experienceleague.adobe.com/bbZLNKJ3wg--z3PcVQ4tTvMtuyR7LMsh7qJjrlZ6L7Y
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 5f839a4ab1e599764c9b797e4a9a42850808e3e3
workflow-type: tm+mt
source-wordcount: 1118
ht-degree: 91%

---

# Exemples de requêtes {#query-examples}

Dans cette page, vous trouverez la liste des jeux de données Adobe Journey Optimizer et des cas d’utilisation associés :

* [Jeu de données d’événement d’expérience de tracking e-mail](#email-tracking-experience-event-dataset)
* [Jeu de données d’événement de retour de message](#message-feedback-event-dataset)
* [Jeu de données d’événement d’expérience de tracking de notifications push](#push-tracking-experience-event-dataset)
* [Événement d’étape de parcours](#journey-step-event)
* [Jeu de données d’événement Decisioning](#ode-decisionevents)
* [Jeu de données d’événement de retour de destinataire Secondaire (Cci)](#bcc-feedback-event-dataset)
* [Jeu de données d’entité](#entity-dataset)

Pour consulter la liste complète des champs et attributs de chaque schéma, consultez le [dictionnaire de schémas de Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr){target="_blank"}.

Consultez également plusieurs [exemples couramment utilisés pour interroger des événements d’étape de parcours](../reports/query-examples.md).


## Jeu de données d’événement d’expérience de tracking e-mail{#email-tracking-experience-event-dataset}

_Nom dans l’interface : Jeu de données d’événement d’expérience de tracking e-mail sur AJO_

Jeu de données système pour l’ingestion d’événements d’expérience de tracking e-mail à partir de Journey Optimizer.

Le schéma associé est celui d’événements d’expérience de tracking e-mail sur AJO.

Cette requête affiche le nombre de différentes interactions d’e-mail (ouvertures, clics) pour un message donné :

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from ajo_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Cette requête affiche la répartition du nombre d’interactions d’e-mail (ouvertures, clics) par message pour un parcours donné :

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from ajo_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## Jeu de données d’événement de retour de message{#message-feedback-event-dataset}

_Nom dans l’interface : Jeu de données d’événement de retour de message AJO_

Jeu de données pour l’ingestion d’événements de retour d’application push et d’e-mail à partir de Journey Optimizer.

Le schéma associé est celui d’événement de retour de message AJO.

>[!NOTE]
>
>Ce jeu de données utilise l’ingestion par lots. Attendez-vous à une latence des données allant jusqu’à 2 heures lors de l’interrogation de ce jeu de données ou de son utilisation à des fins de création de rapports.

Cette requête affiche le nombre de différents statuts de retour par e-mail (envoyés, rebonds, etc.) pour un message donné :

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from ajo_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Cette requête affiche la répartition du nombre de différents statuts de retours par e-mail (envoyés, rebonds, etc.) par message pour un parcours donné :

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from ajo_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

Au niveau agrégé, rapport au niveau des domaines (trié par domaines principaux) : Nom de domaine, Message envoyé, Rebonds

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

Envois quotidiens d’e-mails :

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Recherchez si un ID d’e-mail particulier a reçu un e-mail ou non et, dans le cas contraire, quelle était l’erreur, la catégorie de rebond, le code :

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Recherchez la liste de tous les ID d’e-mails individuels qui ont eu une erreur particulière, une catégorie de rebond ou un code dans les x dernières heures/jours ou qui ont été associés à une diffusion de message spécifique :

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Taux de rebond définitif au niveau agrégé :

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Erreurs permanentes regroupées par code de rebond :

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

>[!NOTE]
>
>Dans certains parcours, les `messageID` peuvent ne pas être uniques pour chaque diffusion individuelle. Si un parcours envoie à nouveau la même action au même profil, le même `messageID` peut être réutilisé. Par conséquent, pour suivre ou attribuer avec précision des événements au niveau de l’envoi individuel, combinez les champs `journeyVersionID`, `journeyActionID` et `batchInstanceID` (pour les parcours par lots) ou `identityMap` pour plus de précision.


### Identifier les adresses en quarantaine après une panne du FAI{#isp-outage-query}

En cas de panne du fournisseur d’accès à Internet (FAI), vous devez identifier les adresses e-mail qui ont été considérées incorrectement comme des rebonds (mises en quarantaine) pour des domaines spécifiques et pendant une période donnée. Pour obtenir ces adresses, utilisez la requête suivante :

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM ajo_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

dans laquelle le format des dates est le suivant : `YYYY-MM-DD HH:MM:SS`.

Une fois identifiées, supprimez ces adresses de la liste de suppression de Journey Optimizer. [En savoir plus](../configuration/manage-suppression-list.md#remove-from-suppression-list).

>[!NOTE]
>
>Lors du référencement de l’identityMap dans le jeu de données d’événement de retour de message, notez qu’il reflète uniquement l’identité utilisée au moment de l’exécution. Pour les notifications push, un événement « envoyé » ne s’appuierait que sur l’ECID lié au jeton push utilisé pour envoyer cette notification, tandis qu’un événement d’« exclusion » pourrait s’appuyer sur une identité personnalisée. Par exemple, si un profil a été exclu car aucun jeton push n’a été trouvé, l’identité utilisée au niveau de la campagne d’action ou du parcours sera sélectionnée pour enregistrer cet événement. Si vous avez besoin d’espaces de noms supplémentaires (par exemple, d’identifiants personnalisés), joignez ces enregistrements de retour à un jeu de données lié au profil (par exemple, profile_snapshot) pour récupérer la liste complète des identités.




## Jeu de données d’événement d’expérience de suivi des notifications push {#push-tracking-experience-event-dataset}

_Nom dans l’interface : Jeu de données d’événement d’expérience de tracking de notifications push sur AJO_

Jeu de données pour l’ingestion d’événements d’expérience de tracking mobile pour les notifications push à partir de Journey Optimizer.

Le schéma associé est celui d’événement d’expérience de tracking de notifications push sur AJO.

Exemple de requête :

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from ajo_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from ajo_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## Événement d’étape de parcours{#journey-step-event}

_Nom interne : Événements d’étape de parcours (jeu de données système)_

Jeu de données pour l’ingestion d’événements d’étape dans le parcours.

Le schéma associé est celui d’événements d’étapes de parcours pour Journey Orchestration.

Cette requête affiche la répartition des succès d’action par libellé d’action pour un parcours donné :

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

Cette requête affiche la répartition des nombres d’étapes renseignés par nodeId et nodeLabel pour un parcours donné. nodeId est inclus ici car nodeLabel peut être le même pour différents nœuds de parcours.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```




Cette requête récupère les nœuds (par nodeID et nodeName) du parcours qui sont associés à la diffusion d’un message à un profil, à l’aide de son identifiant de profil et du jeu de données Événement de retour de message :

```sql
select
    _experience.journeyorchestration.stepevents.nodeID, JSE._experience.journeyorchestration.stepevents.nodeName
from journey_step_events JSE
where 
    _experience.journeyOrchestration.stepEvents.actionID 
    in

    (
    select
        _experience.customerJourneyManagement.messageExecution.journeyActionID
    from  ajo_message_feedback_event_dataset
    where 
        _experience.customerJourneyManagement.messageProfile.messageProfileID = '<PROFILE ID>'
    group by
        _experience.customerJourneyManagement.messageExecution.journeyActionID
    )

group by
    _experience.journeyorchestration.stepevents.nodeID, JSE._experience.journeyorchestration.stepevents.nodeName  
```


Consultez également plusieurs [exemples couramment utilisés pour interroger des événements d’étape de parcours](../reports/query-examples.md).

Découvrez comment [dépanner les types d’événements rejetés dans journey_step_events](../reports/sharing-field-list.md#discarded-events).

## Jeu de données d’événement de prise de décision{#ode-decisionevents}

_Nom dans l’interface : ODE DecisionEvents (jeu de données système)_

Jeu de données pour ingérer des propositions d’offre aux utilisateurs.

Le schéma associé est ODE DecisionEvents.

Cette requête affiche toutes les offres renvoyées le jour précédent :

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

Cette requête indique le nombre de fois où des offres ont été proposées au cours des 30 derniers jours d’une activité/décision particulière et sa priorité d’offre associée.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20230925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

<!--
## Consent service dataset{#consent-service-dataset}

_Name in the interface: CJM Consent Service Dataset (system dataset)_

Dataset for Journey Optimizer Consent service.

The related schema is CJM Consent Service Schema.

Query to list email IDs that have consented to receive email:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query to return consent value for an email ID where email ID would be the input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```
-->

## Jeu de données d’événement de retour de destinataire Secondaire (Cci){#bcc-feedback-event-dataset}

_Nom dans l’interface : Jeu de données d’événement de retour du destinataire Secondaire AJO (jeu de données système). Dans Query Service, le tableau du jeu de données peut toujours être nommé `ajo_bcc_feedback_event_dataset`._

Jeu de données pour les messages e-mail Cci (destinataire secondaire) lorsque l’archivage en Cci est activé.

Requête pour tous les messages en Cci dans les 2 jours (pour une campagne donnée) :

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Requête avec jeu de données de retour pour afficher les utilisateurs qui n’ont pas reçu (tous les rebonds et suppressions) et qui ont une entrée Cci pour un message donné :

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM ajo_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM ajo_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Jeu de données d’entité{#entity-dataset}

_Nom dans l’interface : ajo_ entity_dataset (jeu de données système)_

Jeu de données permettant de stocker les métadonnées des entités pour les messages envoyés à l’utilisateur final.

Le schéma associé est le schéma d’entité AJO.

Ce jeu de données vous donne accès aux métadonnées définies par le spécialiste du marketing, ce qui vous permet d’obtenir de meilleures informations sur les rapports lorsque des jeux de données Journey Optimizer sont exportés pour la visualisation de rapports dans des outils externes. L’attribut messageID permet de regrouper divers jeux de données, tels que les jeux de données de commentaires sur les messages et les jeux de données de suivi des événements d’expérience, pour obtenir des détails sur la diffusion d’un message, de l’envoi au suivi, au niveau d’un profil.

**Remarques importantes**

* Une entrée pour un message n’est créée qu’après la publication d’un parcours ou d’une campagne.

* L&#39;entrée s’affichera 30 minutes après la publication de la campagne ou du parcours.

>[!NOTE]
>
>Pour l’instant, il y a deux entrées pour chaque publication de message dans le jeu de données d’entités pour des raisons de compatibilité future. Cela n’a aucune incidence sur votre capacité à utiliser des requêtes de jointure selon les besoins dans les jeux de données pour récupérer les informations souhaitées.

Si vous souhaitez trier, dans vos rapports, les e-mails envoyés par un parcours spécifique en fonction de l’action qui les a envoyés, vous pouvez joindre le jeu de données Commentaires de message au jeu de données Entité. Les champs à utiliser sont les suivants : `_experience.decisioning.propositions.scopeDetails.correlationID` et `_id field in entity dataset`.

La requête suivante permet d’obtenir le modèle de message associé à une campagne donnée :

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

La requête suivante permet d’obtenir les détails du Parcours et l’objet de l’e-mail associés à tous les événements de commentaires :

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN ajo_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

Vous pouvez assembler des événements d’étape de parcours, des retours de message et des jeux de données de suivi pour obtenir les statistiques sur un profil particulier :

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN ajo_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
