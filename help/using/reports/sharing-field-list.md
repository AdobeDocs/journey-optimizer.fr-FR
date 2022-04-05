---
title: Liste des champs d’événement d’étape
description: Liste des champs d’événement d’étape
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: c058c4835c560f12e3d53bfb766324405b12968f
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 95%

---

# Liste des champs d’événement d’étape {#sharing-field-list}

Les champs d’événement d’étape sont organisés par catégorie.

* Champs d’informations de débogage
* Champs du parcours
* Champs de profil
* Champs d’événement de service

## debugInfo {#debuginfo-field}

| Nom du champ | Type | Description |
|---|---|------------|
| requestId | Chaîne | ID de requête utilisé par Journey Optimizer pour suivre le flux d’une requête. |

## parcours {#journey-field}

Ce groupe de champs est utilisé dans le schéma du parcours (en relation avec journeyStepEvent). Il contient les champs suivant :

| Nom du champ | Type | Description |
|---|---|------------|
| Identifiant | Chaîne | Identifiant du parcours donné |
| VersionID | Chaîne | Identifiant de la version du parcours. Cet identifiant représente l’identité d’un parcours. |
| nom | Chaîne | Nom du parcours |
| description | Chaîne | Description du parcours |
| version | Chaîne | Version, représentée sous la forme `major`.`minor` |

## profil {#profile-field}

Ce groupe de champs est spécifique à journeyStepEvent : cet événement est en relation avec le parcours, et ne dispose pas de l&#39;identityMap décrivant l&#39;identité du profil, le cas échéant.

Pour journeyStepEvent, nous devons également ajouter des champs liés à l’identité :

| Nom du champ | Type | Description |
|---|---|------------|
| Identifiant | Chaîne | L’identifiant de profil identifie le profil envoyé/utilisé dans un parcours. Par exemple : foo@adobe.com. |
| espace de noms | Chaîne | Ce champ décrit l’espace de noms référencé par le profil utilisé dans le parcours. Par exemple : E-mail, ECID |

## serviceEvents {#servicevents-field}

Ce mixin contient tous les champs correspondant à une tâche d’exportation de profil.

| Nom du champ | Type | Description |
|---|---|------------|
| Identifiant | Chaîne | L’identifiant de la tâche d’exportation de segments déclenchée. |
| statut | Chaîne | Statut de la tâche d’exportation de segments : en file d’attente, commencé, terminé |
| exportCountTotal | Nombre entier | Valeur maximale possible de la tâche d’exportation de segments |
| exportCountRealized | Nombre entier | Le nombre réel de segments exportés par la tâche. |
| exportCountFailed | Nombre entier | Le nombre de segments ayant échoué lors de l’exportation via la tâche. |
| exportSegmentID | Chaîne | Identifiant du segment à exporter |
| eventType | Chaîne | Type d’événement indiquant s’il s’agit d’un événement d’erreur ou d’un événement d’information : Info, Erreur |
| eventCode | Chaîne | Le code d’erreur indiquant la raison eventType correspondant |

## stepEvents {#stepevents-field}

Cette catégorie contient les champs d’événement d’étape d’origine. Reportez-vous à cette [section](../reports/sharing-legacy-fields.md).
