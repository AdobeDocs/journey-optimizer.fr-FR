---
solution: Journey Optimizer
product: journey optimizer
title: Liste des champs d’événement d’étape
description: Liste des champs d’événement d’étape
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '320'
ht-degree: 100%

---

# Liste des champs d’événement d’étape {#sharing-field-list}

Les champs d’événement d’étape sont organisés par catégorie.

* Champs d’informations de débogage
* Champs du parcours
* Champs de profil
* Champs d’événement de service

Pour l’attribut identityMap, l’identité principale est définie par défaut sous la forme « primary = true ».

## debugInfo {#debuginfo-field}

| Nom du champ | Type | Description |
|---|---|------------|
| requestId | Chaîne | ID de requête utilisé par Journey Optimizer pour suivre le flux d’une requête. |

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
| Identifiant | Chaîne | Identifiant du traitement d’export d’audiences déclenchée |
| statut | Chaîne | Statut du traitement d’export d’audiences : en file d’attente, commencé, terminé |
| exportCountTotal | Nombre entier | Valeur maximale possible du traitement d’export d’audiences |
| exportCountRealized | Nombre entier | Nombre réel d’audiences exportées par le traitement |
| exportCountFailed | Nombre entier | Nombre d’audiences ayant échoué lors de l’export par le traitement |
| exportSegmentID | Chaîne | Identifiant de l’audience à exporter |
| eventType | Chaîne | Type d’événement indiquant s’il s’agit d’un événement d’erreur ou d’un événement d’information : Info, Erreur |
| eventCode | Chaîne | Le code d’erreur indiquant la raison eventType correspondant |

## stepEvents {#stepevents-field}

Cette catégorie contient les champs d’événement d’étape d’origine. Reportez-vous à cette [section](../reports/sharing-legacy-fields.md).
