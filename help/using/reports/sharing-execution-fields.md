---
solution: Journey Optimizer
product: journey optimizer
title: Champs d’exécution d’action des événements journeyStep
description: Champs d’exécution d’action des événements journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Champs d’exécution d’action des événements journeyStep {#sharing-execution-fields}

Ce groupe de champs sera partagé par les variables journeyStepEvent et journeyStepProfileEvent.

Si l’étape comporte une action à traiter, ces champs seront ajoutés à la payload de l’événement.

## actionID {#actionid-field}

Identifiant de l’action en cours d’exécution.

Type : string

## actionName {#actionname-field}

Nom de l’action. Si aucun nom n’a été défini, stepName est exécuté.

Type : string

## actionType {#actionType-field}

Type de l’action.

Type : string

## actionParameterized {#actionparameterized-field}

Indique si l’action est paramétrée ou non.

Type : boolean

## actionExecutionTime {#actionexecutiontime-field}

Durée (en millisecondes) d’exécution d’une action en cours.

Type : long

## actionExecutionError {#actionexecutionerror-field}

Type d’erreur qui se produit lorsque l’action est appelée.

Type : string

Valeurs :
* http
* capping
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Code de l’erreur d’exécution d’action. Présent si l’erreur comporte un code, par exemple HTTP.

Type : string

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Un délai d’expiration peut se produire dans deux cas :

* lors de la première tentative d’exécution d’une action. Dans ce cas, l’exécution n’est pas terminée, il n’y a donc pas d’erreur sous-jacente
* lors d’une nouvelle tentative : dans ce cas, actionExecOrigError/actionExecOrigErrorCode décrit l’erreur rencontrée lors de la tentative avant la nouvelle tentative.

Par exemple, un email est envoyé et une erreur HTTP 500 est renvoyée lors de la première tentative. La récupération est reprise, mais la durée des deux tentatives dépasse le délai d’attente. Ensuite, l’exécution de l’action est balisée comme délai d’expiration. La partie action se présente comme suit :

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

Type : string

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Code d’erreur de actionExecOrigError.

Type : string

## actionBusinessType {#actionbusinesstype-field}

Indique le type d’action.

Valeurs :

* builtin
* ACS Email
* SMS ACS
* ACS Push
* client
* Epsilon
* ...

Type : string

## deliveryJobID {#deliveryjobid-field}

Cette section décrit l’identifiant de tâche de diffusion pour le parcours par lots.

Type : string

## batchDeliveryID {#batchdeliveryid-field}

Cette section décrit l’identifiant de diffusion pour le parcours par lots.

Type : string

## fromSegmentTrigger {#fromsegmenttrigger-field}

Cette section décrit si le parcours par lots est déclenché à partir du segment d’audience.

Type : boolean

## actionSchedulerCount {#actionschedulercount-field}

Nombre de demandes de notification du planificateur envoyées au service du planificateur pendant le traitement de l’étape.

Type : long
