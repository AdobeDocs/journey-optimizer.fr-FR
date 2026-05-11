---
solution: Journey Optimizer
product: journey optimizer
title: Schéma d’export des messages AJO
description: En savoir plus sur les champs disponibles dans le jeu de données d’exportation de messages AJO
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportation, messages, jeu de données, schéma, e-mails, SMS
source-git-commit: 9c3baf2558f81eb105c5bfbd98be6ede4ba49c65
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 38%

---

# Schéma d’export des messages AJO {#ajo-message-export-schema}

Lorsque l’option **Exportation de messages** est activée sur une configuration de canal E-mail ou SMS, le contenu du message envoyé est écrit dans le **Jeu de données d’exportation de messages AJO** dans [!DNL Adobe Experience Platform].

Cette section répertorie les champs disponibles dans le jeu de données exporté.

## Champs du jeu de données

+++ _experience

**Champ :** `_experience`\
**Type :** objet

+++

+++ _experience > customerJourneyManagement

**Champ :** `customerJourneyManagement`\
**Type :** objet

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**Champ :** `messageDeliveryMetadata`\
**Type :** objet

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**Champ :** `emailMetadata`\
**Type :** objet

* destinataire

  **Champ :** `recipient`\
  **Type :** objet

   * cci

     **Champ :** `bcc`\
     **Type:** tableau de chaînes

   * cc

     **Champ :** `cc`\
     **Type:** tableau de chaînes

   * E-mail

     **Champ :** `email`\
     **Type :** chaîne

   * nom

     **Champ :** `name`\
     **Type :** chaîne

* expéditeur

  **Champ :** `sender`\
  **Type :** objet

   * E-mail

     **Champ :** `email`\
     **Type :** chaîne

   * errorEmail

     **Champ :** `errorEmail`\
     **Type :** chaîne

   * nom

     **Champ :** `name`\
     **Type :** chaîne

   * responseToEmail

     **Champ :** `replyToEmail`\
     **Type :** chaîne

   * responseToName

     **Champ :** `replyToName`\
     **Type :** chaîne

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**Champ :** `smsMetadata`\
**Type :** objet

* destinataire

  **Champ :** `recipient`\
  **Type :** objet

   * nombre

     **Champ :** `number`\
     **Type :** chaîne

* expéditeur

  **Champ :** `sender`\
  **Type :** objet

   * nombres

     **Champ :** `numbers`\
     **Type:** tableau de chaînes

+++

+++ _experience > customerJourneyManagement > messageExecution

**Champ :** `messageExecution`\
**Type :** objet

* audience

  **Champ :** `audience`\
  **Type :** objet

   * identifiant

     **Champ :** `id`\
     **Type :** chaîne

   * type

     **Champ :** `type`\
     **Type :** chaîne

* fragmentPublicationIDs

  **Champ :** `fragmentPublicationIDs`\
  **Type:** tableau de chaînes

* métadonnées

  **Champ :** `metadata`\
  **Type:** map

   * [Mapper la clé]

     **Type :** chaîne

* parentSourceMeta

  **Champ :** `parentSourceMeta`\
  **Type :** objet

   * sourceActionID

     **Champ :** `sourceActionID`\
     **Type :** chaîne

   * sourceID

     **Champ :** `sourceID`\
     **Type :** chaîne

   * sourceType

     **Champ :** `sourceType`\
     **Type :** chaîne

   * sourceVersionID

     **Champ :** `sourceVersionID`\
     **Type :** chaîne

* batchInstanceID

  **Champ :** `batchInstanceID`\
  **Type :** chaîne

* campaignActionID

  **Champ :** `campaignActionID`\
  **Type :** chaîne

* campaignID

  **Champ :** `campaignID`\
  **Type :** chaîne

* campaignVersionID

  **Champ :** `campaignVersionID`\
  **Type :** chaîne

* journeyActionID

  **Champ :** `journeyActionID`\
  **Type :** chaîne

* journeyVersionID

  **Champ :** `journeyVersionID`\
  **Type :** chaîne

* journeyVersionInstanceID

  **Champ :** `journeyVersionInstanceID`\
  **Type :** chaîne

* journeyVersionNodeID

  **Champ :** `journeyVersionNodeID`\
  **Type :** chaîne

* messageExecutionID

  **Champ :** `messageExecutionID`\
  **Type :** chaîne

* messageID

  **Champ :** `messageID`\
  **Type :** chaîne

* messagePublicationID

  **Champ :** `messagePublicationID`\
  **Type :** chaîne

* messageType

  **Champ :** `messageType`\
  **Type :** chaîne

* waveID

  **Champ :** `waveID`\
  **Type :** chaîne

+++

+++ _experience > customerJourneyManagement > messageProfile

**Champ :** `messageProfile`\
**Type :** objet

* channel

  **Champ :** `channel`\
  **Type :** objet

   * contentTypes

     **Champ :** `contentTypes`\
     **Type:** tableau de chaînes

   * locationTypes

     **Champ :** `locationTypes`\
     **Type:** tableau de chaînes

   * metricTypes

     **Champ :** `metricTypes`\
     **Type:** tableau de chaînes

   * _id

     **Champ :** `_id`\
     **Type :** chaîne

   * _type

     **Champ :** `_type`\
     **Type :** chaîne

   * mediaAction

     **Champ :** `mediaAction`\
     **Type :** chaîne

   * mediaType

     **Champ :** `mediaType`\
     **Type :** chaîne

   * mode

     **Champ :** `mode`\
     **Type :** chaîne

   * referenceSource

     **Champ :** `referringSource`\
     **Type :** chaîne

   * typeAtSource

     **Champ :** `typeAtSource`\
     **Type :** chaîne

* isSendTimeOptimized

  **Champ :** `isSendTimeOptimized`\
  **Type:** booléen

* isTestExecution

  **Champ :** `isTestExecution`\
  **Type:** booléen

* messageProfileID

  **Champ :** `messageProfileID`\
  **Type :** chaîne

* messageProfileTrackingID

  **Champ :** `messageProfileTrackingID`\
  **Type :** chaîne

* requestID

  **Champ :** `requestID`\
  **Type :** chaîne

* secondaryDimensionID

  **Champ :** `secondaryDimensionID`\
  **Type :** chaîne

* secondaryDimensionName

  **Champ :** `secondaryDimensionName`\
  **Type :** chaîne

* variante

  **Champ :** `variant`\
  **Type :** chaîne

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**Champ :** `messageRenderedContent`\
**Type :** objet

* emailContent

  **Champ :** `emailContent`\
  **Type :** objet

   * html

     **Champ :** `html`\
     **Type :** chaîne

   * sujet

     **Champ :** `subject`\
     **Type :** chaîne

   * texte

     **Champ :** `text`\
     **Type :** chaîne

* smsContent

  **Champ :** `smsContent`\
  **Type :** objet

   * média

     **Champ :** `media`\
     **Type :** chaîne

   * message

     **Champ :** `message`\
     **Type :** chaîne

   * title

     **Champ :** `title`\
     **Type :** chaîne

+++

+++ identityMap

**Champ :** `identityMap`\
**Type:** map

* [Mapper la clé]

  **Type:** tableau d’objets

   * authenticatedState

     **Champ :** `authenticatedState`\
     **Type :** chaîne

   * identifiant

     **Champ :** `id`\
     **Type :** chaîne

   * primaire

     **Champ :** `primary`\
     **Type:** booléen

+++

+++ eventType

**Champ :** `eventType`\
**Type :** chaîne

+++

+++ productBy

**Champ :** `producedBy`\
**Type :** chaîne

+++

+++ date et heure

**Champ :** `timestamp`\
**Type:** dateTime

+++
