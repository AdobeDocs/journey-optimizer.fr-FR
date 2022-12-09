---
solution: Journey Optimizer
product: journey optimizer
title: Champs communs des événements journeysteps
description: Champs communs des événements journeysteps
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Champs communs des événements journeysteps {#sharing-common-fields}

Ce groupe de champs sera partagé par les variables journeyStepEvent et journeyStepProfileEvent.

Il s’agit des champs XDM communs qui [!DNL Journey Optimizer] envoie vers Adobe Experience Platform. Des champs communs seront envoyés pour chaque étape traitée dans un parcours. Des champs plus spécifiques sont utilisés pour les actions et enrichissements personnalisés.

Certains de ces champs ne sont disponibles que dans des modèles de traitement spécifiques (exécution d’action, récupération de données, etc.) afin de limiter la taille des événements.

## entrée {#entrance-field}

Indique si l’utilisateur est entré dans le parcours. Si elle n’est pas présente, nous supposons que la valeur est false.

Type : boolean

Valeurs : true/false

## reentry {#reentrance-field}

Indique si l’utilisateur est rentré dans le parcours avec la même instance. Si elle n’est pas présente, nous supposons que la valeur est false.

Type : boolean

Valeurs : true/false

## instanceEnded {#instance-ended-field}

Indique si l’instance s’est terminée (avec succès ou non).

Type : boolean

## eventID {#eventid-field}

Identifiant d’événement dans le traitement, pour le traitement de l’étape. Si l’événement est externe, la valeur est son eventId. Si l’événement est interne, la valeur est l’eventId interne (tel que scheduledNotificationReceived, executeAction, etc.).

Type : string

## nodeID {#nodeid-field}

ID de noeud client (à partir de la zone de travail).

Type : string

## stepID {#stepdid-field}

Identifiant unique de l’étape en cours de traitement.

Type : string

## stepName {#stepname-field}

Nom de l’étape en cours de traitement.

Type : string

## stepType {#steptype-field}

Type de l’étape.

Type : string

Valeurs possibles :

* Condition
* Action
* Planificateur
* Minuteur

## stepStatus {#stepstatus-field}

État de l’étape, représentant l’état de l’étape, une fois son traitement terminé (et l’événement d’étape déclenché).

Type : string

L’état peut être :

* Terminé : l’étape n’a aucune transition et son traitement s’est terminé avec succès.
* error: le traitement de l’étape a généré une erreur.
* transitions : l’étape attend qu’un événement effectue une transition vers une autre étape.
* limitée : l’étape a échoué en cas d’erreur de limitation survenue lors d’une action ou d’un enrichissement.
* timedout : l’étape a échoué en cas d’erreur de délai d’expiration, survenue lors d’une action ou d’un enrichissement.
* instanceTimedout : l’étape a arrêté son traitement, car l’instance a atteint son délai d’expiration.

## journeyID {#journeyid-field}

Identifiant du parcours.

Type : string

## journeyVersionID {#journeyversionid-field}

ID de la version du parcours. Cet identifiant représente la référence d’identité du parcours, dans le cas de journeyStepEvent.

Type : string

## journeyVersionName {#journeyversionname-field}

Nom de la version du parcours.

Type : string

## journeyVersion {#journeyversion-field}

Version du parcours.

Type : string

## instanceID {#instanceid-field}

Identifiant interne de l’instance de parcours.

Type : string

## externalKey {#externalkey-field}

Clé externe extraite de l’événement pour le traiter.

Type : string

## parentStepID {#parenstepid-field}

Identifiant de l’étape du parent de l’étape en cours de traitement dans l’instance.

Type : string

## parentStepName {#parentstepname-field}

Nom de l’étape du parent de l’étape en cours.

Type : string

## parentTransitionID {#parenttransitionid-field}

Identifiant de la transition qui a conduit l&#39;instance à l&#39;étape de traitement.

Type : string

## parentTransitionName {#parenttransitionname-field}

Nom de la transition qui a conduit l&#39;instance à l&#39;étape de traitement.

Type : string

## inTest {#intest-field}

Indique si ce parcours est en mode test ou non.

Type : boolean

## processingTime {#processingtime-field}

Durée totale, en millisecondes, entre l’entrée de l’étape de l’instance et la fin du traitement.

Type : long

## instanceType {#instancetype-field}

Indique le type d’instance, s’il s’agit d’un lot ou d’une unité.

Type : string

Valeurs : batch/unitaire

## recurrenceIndex {#recurrenceindex-field}

Index de la périodicité si le parcours est batch et récurrent (la première exécution a recurrenceIndex = 1).

Type : long

## isBatchToUnitary {#isbatchtounitary-field}

Indique si cette instance unitaire a été déclenchée à partir d’une instance de lot.

Type : boolean

## batchExternalKey {#batchexternalkey-field}

Clé externe pour l’événement batch.

Type : string

## batchInstanceID {#batchinstanceid-field}

il s’agit de l’identifiant de l’instance de lot.

Type : string

## batchUnitaryBranchID {#batchunitarybranchid-field}

si l’instance a été déclenchée à partir d’une instance de lot, identifiant de branche unitaire.

Type : string
