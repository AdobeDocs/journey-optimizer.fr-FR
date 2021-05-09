---
title: Champs d'exécution d'action de événements de parcoursStep
description: Champs d'exécution d'action de événements de parcoursStep
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Champs d&#39;exécution d&#39;action de événements d&#39;étape de parcours {#sharing-execution-fields}

![](../assets/do-not-localize/badge.png)

Ce mixin sera partagé par les variables voyageStepEvent et voyageStepProfileEvent.

Si l’étape comporte une action à traiter, ces champs sont ajoutés à la charge utile du événement.

## actionID

ID de l’action en cours d’exécution.

Type : string

## actionName

Nom de l’action. Si aucun nom n&#39;a été défini, stepName est exécuté.

Type : string

## actionType

Type de l&#39;action.

Type : string

## actionParamétré

Indique si l’action est paramétrée ou non.

Type : booléen

## actionExecutionTime

Durée (en millisecondes) d’exécution d’une action en cours.

Type : long

## actionExecutionError

Type d’erreur survenant lors de l’appel de l’action.

Type : string

Valeurs :
* http
* recouvrement
* timeout
* erreur

## actionExecutionErrorCode

Code d&#39;erreur d&#39;exécution d&#39;action. Présente si l’erreur comporte un code, par exemple HTTP.

Type : string

## actionExecutionOriginError

Un dépassement de délai peut se produire dans deux cas :

* lors de la première tentative, une action est exécutée. Dans ce cas, l’exécution n’est pas terminée, il n’y a donc pas d’erreur sous-jacente.
* sur une nouvelle tentative : dans ce cas, actionExecOrigError/actionExecOrigErrorCode décrit l&#39;erreur rencontrée lors de la tentative avant la nouvelle tentative.

Par exemple, un courrier électronique est envoyé et une erreur HTTP 500 est renvoyée lors de la première tentative. La récupération est refaite, mais la durée des deux tentatives dépasse le délai d&#39;attente. Ensuite, l’exécution de l’action est balisée en tant que délai d’expiration. La partie action se présente comme suit :

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

## actionExecutionOriginCode

Code d&#39;erreur de l&#39;actionExecOrigError.

Type : string

## actionBusinessType

Indique le type d’action.

Valeurs :

* construction
* Courriel ACS
* SMS ACS
* Push ACS
* client
* Epsilon
* ...

Type : string

## deliveryJobID

Cette section décrit l’ID de tâche de diffusion pour le Parcours par lot.

Type : string

## batchDeliveryID

Cette section décrit l&#39;ID de diffusion du Parcours de commandes.

Type : string

## fromSegmentTrigger

Cette section décrit si le Parcours de lot est déclenché à partir du segment d’Audience.

Type : booléen

## actionSchedulerCount

Nombre de demandes de notification de Planificateur envoyées au service de Planificateur pendant le traitement de l’étape.

Type : long
