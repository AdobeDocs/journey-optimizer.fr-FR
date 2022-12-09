---
solution: Journey Optimizer
product: journey optimizer
title: Champs de récupération des données des événements journeyStep
description: Champs de récupération des données des événements journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Champs de récupération des données des événements journeyStep {#sharing-fetch-fields}

Ce groupe de champs sera partagé par les variables journeyStepEvent et journeyStepProfileEvent.

Lors du traitement d’une étape, il est possible de récupérer N données sur les groupes de champs.

## fetchTotalTime {#fetchtotaltime-field}

Durée totale de la récupération des données en millisecondes pendant le traitement de l’étape.

Type : long

## fetchTypeInError {#fetchtypeinerror-field}

Définit si la récupération en erreur se trouve sur Adobe Experience Platform ou sur une source de données personnalisée.

Type : string

Valeurs :
* aep
* custom

## fetchError {#fetcherror-field}

Type d’erreur qui se produit lors du traitement de la récupération des données.

Type : string

Valeurs :
* http
* capping
* timedout
* error

## fetchErrorCode {#fetcherrorcode-field}

Code de l’erreur de récupération. Présent si l’erreur comporte un code, par exemple HTTP. Par exemple, si actionExecError est http, le code 404 représente l’erreur HTTP 404.

Type : string

## fetchOriginError {#fetchoriginerror-field}

Un délai d’expiration peut se produire dans deux cas :

* lors de la première tentative d’exécution de l’action. Dans ce cas, l’exécution n’est pas terminée, il n’y a donc pas d’erreur sous-jacente
* lors d’une nouvelle tentative : dans ce cas, actionExecOrigError/actionExecOrigErrorCode décrit l’erreur rencontrée lors de la tentative avant la nouvelle tentative.

Par exemple, les données sont extraites du service de profil unifié et une erreur HTTP 500 est renvoyée lors de la première tentative. La récupération est reprise, mais la durée des deux tentatives dépasse le délai d’attente. Ensuite, l’exécution de l’action est balisée comme délai d’expiration. La partie action se présente comme suit :

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Type : string

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

Code d’erreur fourni par le système [!DNL Journey Optimizer] est interrogé. Par exemple, il peut s’agir d’un 404, d’un 500, etc.

Type : string

## fetchCount {#fetchcount-field}

Nombre de récupérations de données, quel que soit le type de source.

Type : long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Durée totale (en millisecondes) nécessaire à la récupération des données d’Adobe Experience Platform. Remarque : ce délai est calculé à partir du moment où le moteur envoie l’événement d’enrichissement au service d’enrichissement et reçoit la réponse.

Type : long

## fetchPlatformCount {#fetchplatformcount-field}

Nombre de récupérations de données dans Adobe Experience Platform.

Type : long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Laps de temps consacré à la récupération des données personnalisées en millisecondes. Remarque : ce temps est calculé à partir du moment où le moteur envoie l’événement d’enrichissement au service d’enrichissement et reçoit la réponse

Type : long

## fetchCustomCount {#fetchcustomcount-field}

Nombre de récupérations de données personnalisées sur des systèmes externes.

Type : long
