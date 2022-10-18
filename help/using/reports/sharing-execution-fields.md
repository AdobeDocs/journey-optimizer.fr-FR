---
solution: Journey Optimizer
product: journey optimizer
title: Champs d'exécution d'action des événements journeyStep
description: Champs d'exécution d'action des événements journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 100%

---

# Champs d&#39;exécution d&#39;action des événements journeyStep {#sharing-execution-fields}

Ce groupe de champs sera partagé par les variables journeyStepEvent et journeyStepProfileEvent.

Si l’étape comporte une action à traiter, ces champs sont ajoutés à la payload de l’événement.

## actionID {#actionid-field}

ID de l’action en cours d’exécution.

Type : chaîne

## actionName {#actionname-field}

Nom de l’action Si aucun nom n’a été défini, stepName est exécuté.

Type : chaîne

## actionType {#actionType-field}

Type de l’action.

Type : chaîne

## actionParameterized {#actionparameterized-field}

Indique si l’action est paramétrée ou non.

Type : booléen

## actionExecutionTime {#actionexecutiontime-field}

Durée (en millisecondes) d’exécution d’une action en cours.

Type : long

## actionExecutionError {#actionexecutionerror-field}

Type d’erreur se produisant lors de l’appel de l’action.

Type : chaîne

Valeurs :
* http
* capping
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Code d’erreur d’exécution d’action. Présent si l’erreur comporte un code, par exemple HTTP.

Type : chaîne

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Une temporisation peut se produire dans deux cas :

* Lors de la première tentative d’exécution d’une action. Dans ce cas, l’exécution n’est pas terminée, il n’y a donc pas d’erreur associée.
* Lors d’une nouvelle tentative : dans ce cas, le code actionExecOrigError/actionExecOrigErrorCode décrit l’erreur rencontrée lors de la tentative, et avant la nouvelle tentative.

Par exemple, un e-mail est envoyé et une erreur HTTP 500 est renvoyée lors de la première tentative. La récupération est de nouveau tentée, mais la durée des deux tentatives excède la temporisation. L’exécution de l’action est ensuite balisée pour indiquer un dépassement de délai. La partie action se présente comme suit :

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

Type : chaîne

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Code d’erreur d’actionExecOrigError.

Type : chaîne

## actionBusinessType {#actionbusinesstype-field}

Indique le type d’action.

Valeurs :

* builtin
* ACS E-mail
* ACS SMS
* ACS Push
* customer
* Epsilon
* ...

Type : chaîne

## deliveryJobID {#deliveryjobid-field}

Cette section décrit l’ID de traitement de diffusion pour le parcours par lot.

Type : chaîne

## batchDeliveryID {#batchdeliveryid-field}

Cette section décrit l’ID de diffusion pour le parcours par lot.

Type : chaîne

## fromSegmentTrigger {#fromsegmenttrigger-field}

Cette section décrit si le parcours par lot est déclenché à partir du segment d’audience.

Type : booléen

## actionSchedulerCount {#actionschedulercount-field}

Nombre de demandes de notification de Planificateur envoyées au service Planificateur au cours du traitement de l’étape.

Type : long
