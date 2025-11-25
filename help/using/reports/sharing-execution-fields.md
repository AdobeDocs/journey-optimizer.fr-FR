---
solution: Journey Optimizer
product: journey optimizer
title: Champs d'exécution d'action des événements journeyStep
description: Champs d'exécution d'action des événements journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: ht
source-wordcount: '663'
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

Le champ `actionExecutionTime` représente le temps total (en millisecondes) nécessaire à l’exécution de l’action, y compris le temps d’attente de la requête dans la file d’attente (si la limitation est configurée et la limite de débit est atteinte) et le temps d’exécution réel (y compris la latence du réseau vers le point d’entrée externe).

Le champ `Timestamp` indique l’heure de fin de l’exécution de l’action. L’heure d’entrée du profil dans le nœud d’action personnalisée s’obtient en soustrayant `actionExecutionTime` de `Timestamp`.

Par exemple, si `Timestamp` est « 2025-02-04 09:39:03 UTC » et `actionExecutionTime` est de 1 813 227 ms (~31 minutes), le profil est entré dans le nœud à environ « 2025-02-04 09:08:32 UTC ».


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

Un dépassement de délai peut se produire dans deux cas :

* Lors de la première tentative d’exécution d’une action. Dans ce cas, l’exécution n’est pas terminée, il n’y a donc pas d’erreur associée.
* Lors d’une nouvelle tentative : dans ce cas, le code actionExecOrigError/actionExecOrigErrorCode décrit l’erreur rencontrée lors de la tentative, et avant la nouvelle tentative.

Par exemple, un e-mail est envoyé et une erreur HTTP 500 est renvoyée lors de la première tentative. La récupération est de nouveau tentée, mais la durée des deux tentatives excède le délai d’attente. L’exécution de l’action est ensuite balisée pour indiquer un dépassement de délai. La partie action se présente comme suit :

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

## actionOriginEndpoint {#actionoriginendpoint}

URI du point d’entrée d’action personnalisée utilisé dans l’action.

Type : chaîne

## actionOriginMethod {#actionoriginmethod}

Indique la méthode utilisée dans la requête HTTP (GET ou POST).

Type : chaîne

## actionOriginIsMTLS {#actionoriginismtls}

Indique si le protocole MTLS est activé ou non pour le point d’entrée.

Type : booléen

## actionIsProxy {#actionisproxy}

Indique si un proxy HTTP avec une plage d’adresses IP définie est utilisé pour l’appel.

Type : booléen

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

Indique la date et l’heure auxquelles la requête HTTP est envoyée. En cas de nouvelles tentatives, il s’agit de la date et de l’heure auxquelles la dernière tentative est effectuée. La date et l’heure utilisent le format ISO 8601 avec le fuseau horaire UTC.

Notez que la date et l’heure seront généralement légèrement postérieures à l’entrée du profil dans le nœud d’action personnalisée, ou significativement postérieures à son entrée dans le nœud en cas de limitation.

Type : date et heure

## actionExecutionOriginTime {#actionexecutionorigintime}

Indique le temps de réponse de l’appel HTTP. En cas de nouvelles tentatives, il s’agit de la durée de la dernière tentative effectuée. Cette fonction mesure le temps entre le moment où la requête HTTP est envoyée et le moment où la réponse complète est renvoyée à partir du serveur. Attention, cela exclut le temps passé dans la file d’attente en cas de limitation.

Type : long

## actionIsThrottled {#actionisthrottled}

Indique si la limitation est activée pour le point d’entrée.

Type : booléen

## actionWaitTime {#actionwaittime}

Indique lorsque la limite de débit configurée est atteinte pour un point d’entrée limité. Les appels sont placés en file d’attente et traités à la fréquence configurée. Ce champ indique le temps que l’appel a passé en file d’attente avant d’être exécuté. Spécifié uniquement si actionIsThrottled == true.

Type : long

## actionBusinessType {#actionbusinesstype-field}

Indique le type d’action.

Valeurs :

* builtin
   * ACS E-mail
   * ACS SMS
   * ACS Push
* client ou cliente
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
