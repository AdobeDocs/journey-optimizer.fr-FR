---
solution: Journey Optimizer
product: journey optimizer
title: Champs de récupération des données des événements journeyStep
description: Champs de récupération des données des événements journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
TQID: https://experienceleague.adobe.com/obaiLWD6yq0dZ5ZhE69q-iLHzI99ll7XJnMNlOpJp1A
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 377
ht-degree: 100%

---

# Champs de récupération des données des événements journeyStep {#sharing-fetch-fields}

Ce groupe de champs sera partagé par les variables journeyStepEvent et journeyStepProfileEvent.

Lors du traitement d’une étape, il est possible de récupérer un nombre quelconque de données dans les groupes de champs.

## fetchTotalTime {#fetchtotaltime-field}

Laps de temps total, en millisecondes, consacré à la récupération des données lors du traitement d’une étape.

Type : long

## fetchTypeInError {#fetchtypeinerror-field}

Définit si la récupération en erreur se trouve dans Adobe Experience Platform ou dans une source de données personnalisée.

Type : chaîne

Valeurs :

* aep
* custom

## fetchError {#fetcherror-field}

Type d’erreur se produisant lors du traitement de la récupération des données.

Type : chaîne

Valeurs :

* http
* capping
* timedout
* error

## fetchErrorCode {#fetcherrorcode-field}

Code de l’erreur de récupération. Présent si l’erreur comporte un code, par exemple HTTP. Par exemple, si actionExecError contient http, le code 404 représente l’erreur HTTP 404.

Type : chaîne

## fetchOriginError {#fetchoriginerror-field}

Une temporisation peut se produire dans deux cas :

* Lors de la première tentative d’exécution de l’action. Dans ce cas, l’exécution n’est pas terminée, il n’y a donc pas d’erreur associée.
* Lors d’une nouvelle tentative : dans ce cas, le code actionExecOrigError/actionExecOrigErrorCode décrit l’erreur rencontrée lors de la tentative, et avant la nouvelle tentative.

Par exemple, les données sont extraites du service Profil unifié et une erreur HTTP 500 est renvoyée lors de la première tentative. La récupération est de nouveau tentée, mais la durée des deux tentatives excède le délai d’expiration. L’exécution de l’action est ensuite balisée pour indiquer un dépassement de délai. La partie action se présente comme suit :

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Type : chaîne

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

Code d’erreur fourni par le système interrogé par [!DNL Journey Optimizer]. Il peut s’agir par exemple d’un code 404, 500, etc.

Type : chaîne

## fetchCount {#fetchcount-field}

Nombre de récupérations de données, quel que soit le type de source.

Type : long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Laps de temps total en millisecondes consacré à la récupération des données sur Adobe Experience Platform. Remarque : ce laps de temps est calculé à partir du moment où le moteur envoie l’événement d’enrichissement au service d’enrichissement et reçoit la réponse.

Type : long

## fetchPlatformCount {#fetchplatformcount-field}

Nombre de récupérations de données sur Adobe Experience Platform.

Type : long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Laps de temps consacré à la récupération des données personnalisées en millisecondes. Remarque : ce laps de temps est calculé à partir du moment où le moteur envoie l’événement d’enrichissement au service d’enrichissement et reçoit la réponse

Type : long

## fetchCustomCount {#fetchcustomcount-field}

Nombre de récupérations de données personnalisées depuis les systèmes externes.

Type : long
