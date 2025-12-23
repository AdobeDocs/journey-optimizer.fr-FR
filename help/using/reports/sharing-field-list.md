---
solution: Journey Optimizer
product: journey optimizer
title: Liste des champs d’événement d’étape
description: Liste des champs d’événement d’étape
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 4f13f863a5e08cc0e92c26d782d888f0d6d2fea4
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 98%

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

Ce mixin contient tous les champs correspondant à un traitement d’export de profil. Ces événements sont générés par activité **Lecture d&#39;audience** pour effectuer le suivi du cycle de vie des opérations d’export d’audience (en file d’attente, démarrées, terminées, erreurs). Contrairement aux événements d’étape standard, les serviceEvents ne sont pas liés à des profils individuels, mais au nœud Lecture d’audience lui-même, ce qui signifie qu’ils peuvent ne pas être associés à un identifiant de profil.

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

En savoir plus sur les types d’événements dans [cette section](#discarded-events).

## stepEvents {#stepevents-field}

Cette catégorie contient les champs d’événement d’étape d’origine. Reportez-vous à cette [section](../reports/sharing-legacy-fields.md).


## Résolution des problèmes liés aux types d’événements rejetés dans les événements d’étape de Parcours  {#discarded-events}

Lors de l’interrogation d’événements d’étape de parcours pour des enregistrements avec `eventCode = 'discard'`, vous pouvez rencontrer plusieurs types d’événements.

Vous trouverez ci-dessous des définitions, des causes courantes et des étapes de dépannage pour les `eventTypes` de rejet les plus fréquents :

* **EXTERNAL_KEY_COMPUTATION_ERROR** : le système n’a pas pu calculer un identifiant unique (clé externe) pour le client ou la cliente à partir des données d’événement.

  **Causes courantes** : identifiants clients manquants ou incorrects (par exemple, e-mail, ID client) dans la payload d’événement.

  **Dépannage** : vérifiez la configuration de l’événement pour les identifiants requis et assurez-vous que les données d’événement sont complètes et au bon format.

* **NO_INTERESTED_JOURNEYS_FOR_SEGMENTMEMBERSHIP_EVENT** : un événement de qualification de segment a été reçu, mais aucun parcours n’est configuré pour répondre à ce segment.

  **Causes courantes** : aucun parcours n’utilise le segment comme déclencheur, les parcours sont à l’état de brouillon/arrêté ou les identifiants de segment ne correspondent pas.

  **Dépannage** : assurez-vous qu’au moins un parcours est actif et configuré pour le segment, puis vérifiez les identifiants de segment.

* **PARCOURS_INSTANCE_ID_NOT_CREATED** : le système n&#39;a pas réussi à créer d&#39;instance de parcours pour le client.

  **Causes courantes** : événements en double, volume d’événements élevé, contraintes de ressources système.

  **Dépannage** : implémentez la déduplication, évitez les pics de trafic, optimisez la conception du parcours et contactez l’assistance en cas de persistance.

* **EVENT_WITH_NO_JOURNEY** : un événement a été reçu, mais aucun parcours actif n’est configuré pour y répondre.

  **Causes courantes** : incohérence entre le nom et l’ID de l’événement, parcours non publié, sandbox/organisation incorrects, incompatibilité entre le profil et le mode de test.

  **Dépannage** : vérifiez la configuration de l’événement et du parcours, vérifiez le statut du parcours et utilisez des outils de débogage.

* Pour les rejets se produisant dans des parcours en pause :

   * **PAUSED_JOURNEY_VERSION** : rejets survenus au point d’entrée du parcours.
   * **JOURNEY_IN_PAUSED_STATE** : rejets survenus lorsque les profils se trouvent dans un parcours.

  Pour en savoir plus sur ces événements et sur la manière de les résoudre, consultez la section [Mettre en pause un parcours](../building-journeys/journey-pause.md#discards-troubleshoot).

## Ressources supplémentaires

* [Exemples de requête de jeu de données - Événement d’étape de parcours](../data/datasets-query-examples.md#journey-step-event).
* [Exemples de requêtes - Requêtes basées sur un événement](query-examples.md#event-based-queries).
* [Dictionnaire de schémas intégré](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr)

