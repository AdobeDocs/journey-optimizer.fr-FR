---
solution: Journey Optimizer
product: journey optimizer
title: Champs communs des événements journeysteps
description: Champs communs des événements journeysteps
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
TQID: https://experienceleague.adobe.com/MWcV6FkgtiFJd9Y7q8CvTXQsL68cD5JcvqjmoEyiYhI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 659
ht-degree: 96%

---

# Champs communs des événements journeysteps {#sharing-common-fields}

>[!BEGINSHADEBOX]

**Sur cette page :** référencez les champs d’événement d’étape de parcours communs que Journey Optimizer envoie à Adobe Experience Platform pour chaque étape traitée dans un parcours.

>[!ENDSHADEBOX]

Ce groupe de champs sera partagé par les événements suivants : **journeyStepEvent** et **journeyStepProfileEvent**.

Il s’agit des champs XDM communs que [!DNL Journey Optimizer] envoie à Adobe Experience Platform. Des champs communs seront envoyés pour chaque étape traitée dans un parcours. Des champs plus spécifiques sont utilisés pour les actions et enrichissements personnalisés.

Certains de ces champs ne sont disponibles que dans des modèles de traitement spécifiques (exécution d’action, récupération de données, etc.) afin de limiter la taille des événements.


>[!NOTE]
>
>Pour plus d’informations sur les attributs des propriétés de parcours, consultez [cette section](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## entrance {#entrance-field}

Indique si l’utilisateur est entré dans le parcours. S’il n’est pas présent, nous supposons que la valeur est false.

Type : booléen

Valeurs : Vrai/Faux

## rentrée {#reentrance-field}

Indique si l’utilisateur est entré de nouveau dans le parcours avec la même instance. S’il n’est pas présent, nous supposons que la valeur est false.

Type : booléen

Valeurs : Vrai/Faux

## instanceEnded {#instance-ended-field}

Indique si l’instance s’est terminée (avec succès ou non).

Type : booléen

## eventID {#eventid-field}

ID de l’événement traité, pour le traitement de l’étape. Si l’événement est externe, la valeur est son eventId. Si l’événement est interne, la valeur est l’eventId interne (tel que scheduledNotificationReceived, executedAction, etc.).

Type : chaîne

## nodeID {#nodeid-field}

ID de nœud client (à partir de la zone de travail).

Type : chaîne

## stepID {#stepdid-field}

Identifiant unique de l’étape en cours de traitement.

Type : chaîne

## stepName {#stepname-field}

Nom de l’étape en cours de traitement.

Type : chaîne

## stepType {#steptype-field}

Type de l’étape.

Type : chaîne

Valeurs possibles :

* Condition
* Action
* Planificateur
* Retardateur

## stepStatus {#stepstatus-field}

Statut de l’étape, représentant l’état de l’étape, une fois son traitement terminé (et l’événement de l’étape déclenché).

Type : chaîne

Le statut peut être :

* terminée : l’étape n’a aucune transition et son traitement s’est terminé avec succès.
* erreur : le traitement de l’étape a généré une erreur.
* transitions : l’étape attend qu’un événement effectue une transition vers une autre étape.
* limitée : l’étape a échoué avec une erreur de limitation survenue pendant une action ou un enrichissement.
* temporisation : l’étape a échoué avec une erreur de temporisation survenue pendant une action ou un enrichissement.
* instanceTimedout : l’étape a arrêté son traitement, car l’instance a atteint son délai d’expiration.

## journeyID {#journeyid-field}

ID du parcours.

Type : chaîne

## journeyVersionID {#journeyversionid-field}

Identifiant de la version du parcours. Cet identifiant représente la référence d’identité du parcours, dans le cas du journeyStepEvent.

Type : chaîne

>[!NOTE]
>
>À des fins de dépannage, nous vous recommandons d’utiliser journeyVersionID au lieu de journeyVersionName lors de l’interrogation de parcours.

## journeyVersionName {#journeyversionname-field}

Nom de la version du parcours.

Type : chaîne

>[!NOTE]
>
>À des fins de dépannage, nous vous recommandons d’utiliser journeyVersionID au lieu de journeyVersionName lors de l’interrogation de parcours.

## journeyVersion {#journeyversion-field}

Nom de la version du parcours.

Type : chaîne

## instanceID {#instanceid-field}

ID interne de l’instance de parcours.

Type : chaîne

## externalKey {#externalkey-field}

Clé externe extraite de l’événement pour le traiter.

Type : chaîne

## parentStepID {#parenstepid-field}

ID d’étape du parent de l’étape en cours de traitement dans l’instance.

Type : chaîne

## parentStepName {#parentstepname-field}

Nom de l’étape du parent de l’étape en cours.

Type : chaîne

## parentTransitionID {#parenttransitionid-field}

Identifiant de la transition qui a conduit l’instance à l’étape de traitement.

Type : chaîne

## parentTransitionName {#parenttransitionname-field}

Nom de la transition qui a conduit l’instance à l’étape de traitement.

Type : chaîne

## inTest {#intest-field}

Indique si ce parcours est en mode test ou non.

Type : booléen

## processingTime {#processingtime-field}

Durée totale, en millisecondes, entre l’entrée de l’étape d’instance et la fin du traitement.

Type : long

## instanceType {#instancetype-field}

Indique le type d’instance, s’il s’agit d’un lot ou d’une unité.

Type : chaîne

Valeurs : batch/unitary

## recurrenceIndex {#recurrenceindex-field}

Indice de la récurrence si le parcours est « batch » et récurrent (pour la première exécution, recurrenceIndex = 1).

Type : long

## isBatchToUnitary {#isbatchtounitary-field}

Indique si cette instance unitaire a été déclenchée à partir d’une instance de lot.

Type : booléen

## batchExternalKey {#batchexternalkey-field}

Clé externe pour un événement batch.

Type : chaîne

## batchInstanceID {#batchinstanceid-field}

Il s’agit de l’ID d’instance de lot.

Type : chaîne

## batchUnitaryBranchID {#batchunitarybranchid-field}

si l’instance a été déclenchée à partir d’une instance de lot, ID de branche unitaire.

Type : chaîne

## exitCriteriaID

Identifiant du exitCriteria

Type : chaîne

## exitCriteriaName

Nom du exitCriteria

Type : chaîne