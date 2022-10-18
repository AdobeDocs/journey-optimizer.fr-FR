---
title: Exemples de requêtes de jeux de données
description: Exemples de requêtes de jeux de données
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: 15dc5e2854358f7f200a54a3f06fa6e98f146efe
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 82%

---

# Cas d’utilisation des jeux de données {#tracking-datasets}

Dans cette page, vous trouverez la liste des jeux de données Adobe Journey Optimizer et des cas d’utilisation associés :

[Jeu de données d’événement d’expérience de tracking e-mail](../start/datasets-query-examples.md#email-tracking-experience-event-dataset)
[Jeu de données d’événement de retour de message](../start/datasets-query-examples.md#message-feedback-event-dataset)
[Jeu de données d’événement d’expérience de tracking de notifications Push](../start/datasets-query-examples.md#push-tracking-experience-event-dataset)
[Événement d’étape de parcours](../start/datasets-query-examples.md#journey-step-event)
[Jeu de données d’événement Decisioning](../start/datasets-query-examples.md#ode-decisionevents)
[Jeu de données du service de consentement](../start/datasets-query-examples.md#consent-service-dataset)
[Jeu de données d’événement de retour en Cci](../start/datasets-query-examples.md#bcc-feedback-event-dataset)
[Jeu de données d’entité](../start/datasets-query-examples.md#entity-dataset)

## Jeu de données d’événement d’expérience de tracking e-mail{#email-tracking-experience-event-dataset}

_Nom dans l’interface : Jeu de données d’événement d’expérience de tracking e-mail sur CJM_

Jeu de données système pour l’ingestion d’événements d’expérience de tracking e-mail à partir de Journey Optimizer.

Le schéma associé est celui d’événements d’expérience de tracking e-mail sur CJM.

Cette requête affiche le nombre de différentes interactions d’e-mail (ouvertures, clics) pour un message donné :

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
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
from cjm_email_tracking_experience_event_dataset
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

_Nom dans l’interface : Jeu de données d’événement de retour de message CJM_

Jeu de données pour l’ingestion d’événements de retour d’application push et d’e-mail à partir de Journey Optimizer.

Le schéma associé est celui d’événements de retour de message CJM.

Cette requête affiche le nombre de différents statuts de retour par e-mail (envoyés, rebonds, etc.) pour un message donné :

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
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
from cjm_message_feedback_event_dataset
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
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

Envois quotidiens d’e-mails :

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Recherchez si un ID d’e-mail particulier a reçu un e-mail ou non et, dans le cas contraire, quelle était l’erreur, la catégorie de rebond, le code :

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Recherchez la liste de tous les ID d’e-mails individuels qui ont eu une erreur particulière, une catégorie de rebond ou un code dans les x dernières heures/jours ou qui ont été associés à une diffusion de message spécifique :

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Taux de hard bounce au niveau agrégé :

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Erreurs permanentes regroupées par code de rebond :

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

## Jeu de données d’événement d’expérience de tracking de notifications Push {#push-tracking-experience-event-dataset}

_Nom dans l’interface : Jeu de données d’événement d’expérience de tracking de notifications Push sur CJM_

Jeu de données pour l’ingestion d’événements d’expérience de suivi de mobile pour les notifications push à partir de Journey Optimizer.

Le schéma associé est celui d’événements d’expérience de tracking de notifications Push sur CJM.

Exemple de requête :

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
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

## Jeu de données d’événement Decisioning{#ode-decisionevents}

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
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## Jeu de données du service de consentement{#consent-service-dataset}

_Nom dans l’interface : Jeu de données du service de consentement CJM (jeu de données système)_

Jeu de données pour le service de consentement Journey Optimizer.

Le schéma associé est celui du service de consentement CJM.

Requête pour répertorier les ID d’e-mail ayant consenti à recevoir un e-mail :

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Requête pour renvoyer la valeur de consentement pour un ID d&#39;e-mail où l’ID d&#39;e-mail serait l’entrée :

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## Jeu de données d’événement de retour en Cci{#bcc-feedback-event-dataset}

_Nom dans l’interface : Jeu de données d’événement de retour en Cci AJO (jeu de données système)_

Jeu de données pour stocker des informations pour les messages en Cci.

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
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Jeu de données d’entité{#entity-dataset}

_Nom dans l’interface : ajo_entity_dataset (jeu de données système)_

Jeu de données permettant de stocker les métadonnées des entités pour les messages envoyés à l’utilisateur final.

Le schéma associé est le schéma d’entité AJO.

Ce jeu de données vous donne accès aux métadonnées définies par le marketeur, ce qui vous permet d’obtenir de meilleures informations sur les rapports lorsque des jeux de données Journey Optimizer sont exportés pour la visualisation de rapports dans des outils externes. Pour ce faire, utilisez l’attribut messageID qui permet de regrouper divers jeux de données tels que le jeu de données de retour des messages et les jeux de données de suivi des événements d’expérience afin d’obtenir les détails d’une diffusion de message d’envoi au suivi au niveau du profil.

**Remarques importantes**

* Une entrée pour un message n’est créée qu’après la publication d’un parcours ou d’une campagne.

* L&#39;entrée peut s&#39;afficher 30 minutes après la publication de l&#39;opération/du parcours.

>[!NOTE]
>
>Pour l’instant, il y a deux entrées pour chaque publication de messages dans le jeu de données d’entité pour des raisons de compatibilité futures. Cela n’a aucune incidence sur votre capacité à utiliser des requêtes de jointure selon les besoins dans les jeux de données pour récupérer les informations souhaitées.

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
  INNER JOIN cjm_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
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
  INNER JOIN cjm_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
