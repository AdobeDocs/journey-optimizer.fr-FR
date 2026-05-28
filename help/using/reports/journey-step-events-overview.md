---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des événements d’étape de parcours
description: 'Découvrez comment utiliser les événements d’étape de parcours dans Adobe Journey Optimizer : comprenez ce qu’ils sont, pourquoi ils sont importants et comment les utiliser à des fins d’analyse et d’optimisation.'
feature: Journeys, Reporting
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: parcours, événements d’étape, analyse, rapports, surveillance, XDM
exl-id: 2e7c5ea5-d8c5-416d-ab88-d2bc02043558
TQID: https://experienceleague.adobe.com/PSXSN-31GNlM0zBKcCvdKPciHt5zhQPPCffFrUoIxUs
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
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 937
ht-degree: 98%

---

# Utiliser des événements d’étape de parcours {#work-with-journey-step-events}

Les événements d’étape de parcours sont des événements générés automatiquement qui capturent des informations détaillées sur chaque étape qu’un [profil](../audience/get-started-profiles.md) suit au fur et à mesure de sa progression dans un [parcours](../building-journeys/journey.md) dans Adobe Journey Optimizer. Ces événements offrent une visibilité complète sur les [performances du parcours](../building-journeys/report-journey.md) et permettent de puissantes fonctionnalités d’analyse.

## Présentation des événements d’étape de parcours {#what-are-step-events}

Les événements d’étape de parcours sont des événements [XDM (modèle de données d’expérience)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"} générés par le système et automatiquement créés et envoyés par Adobe Journey Optimizer à [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=fr){target="_blank"} chaque fois qu’un profil passe d’un nœud à un autre dans un parcours. Chaque événement correspond à une [activité de parcours](../building-journeys/about-journey-activities.md) spécifique ou à une transition dans l’expérience de parcours du client ou de la cliente.

Il existe deux principaux types d’événements d’étape de parcours :

- **journeyStepEvent** : événements liés à la progression d’un profil individuel via les étapes d’un parcours.
- **journeyStepProfileEvent** : événements qui incluent des informations contextuelles de profil supplémentaires.

### Qu’est-ce qui déclenche les événements d’étape de parcours ? {#event-triggers}

Les événements d’étape de parcours sont générés automatiquement pour diverses activités de parcours :

- **Événements d’entrée** : lorsqu’un profil [rejoint un parcours](../building-journeys/entry-management.md).
- **Exécution d’action** : lorsque des [messages sont envoyés](../building-journeys/journey-action.md) ou que des [actions personnalisées](../building-journeys/using-custom-actions.md) sont effectuées.
- **Évaluation des conditions** : lorsque les profils passent par des [conditions](../building-journeys/conditions.md) et des points de décision.
- **Activités d’attente** : lorsque les profils rejoignent et quittent des [nœuds d’attente](../building-journeys/wait-activity.md).
- **Événements de sortie** : lorsque les profils terminent ou [quittent un parcours &#x200B;](../building-journeys/end-journey.md)
- **Gestion des erreurs** : lorsque des erreurs se produisent lors de l’exécution d’un parcours.

>[!NOTE]
>
>Les événements d’étape de parcours sont activés par défaut sur toutes les instances. Vous ne pouvez pas modifier ni mettre à jour les [schémas et les jeux de données](sharing-overview.md) créés lors de l’approvisionnement des événements d’étape. Ces schémas et jeux de données sont en lecture seule.

En savoir plus sur les [schémas d’événement d’étape de parcours](sharing-field-list.md).

## Importance des événements d’étape de parcours {#why-step-events-matter}

Les événements d’étape de parcours fournissent une valeur essentielle aux organisations qui utilisent Adobe Journey Optimizer :

### Analyse et surveillance en temps réel {#real-time-analytics}

- **Suivi des performances des parcours** : surveillez le flux des profils dans vos parcours en temps réel à l’aide de [rapports dynamiques](live-report.md).
- **Analyse des conversions** : comprenez les points d’abandon et les chemins de conversion réussis avec l’[analyse des parcours](journey-global-report-cja.md).
- **Détection des erreurs** : identifiez et résolvez les problèmes qui se produisent par le biais de [la surveillance et d’alertes](alerts.md)

### Intégration des données et data insights {#data-integration}

- **Analyse sur plusieurs plateformes** : combinez des données de parcours avec d’autres [sources de données Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md).
- **Vue à 360 des clientes et clients** : créez des [profils clients](../audience/get-started-profiles.md) complets qui incluent les interactions de parcours.
- **Modélisation d’attribution** : connectez des points de contact de parcours aux résultats commerciaux en aval à l’aide de [Customer Journey Analytics](cja-ajo.md).

### Opportunités d’optimisation {#optimization}

- **Informations des tests A/B** : analysez les performances des différents chemins de parcours à l’aide de l’[expérimentation](campaign-global-report-cja-experimentation.md).
- **Amélioration de la personnalisation** : utilisez les données de comportement du parcours pour améliorer les expériences futures avec le [contenu dynamique](../personalization/dynamic-content.md).
- **Efficacité opérationnelle** : identifiez les goulots d’étranglement et optimisez la [conception des parcours](../building-journeys/using-the-journey-designer.md).

## Utilisation des événements d’étape de parcours {#how-to-use-step-events}

### Accès aux données d’événement d’étape de parcours {#accessing-data}

Les données d’événement d’étape de parcours sont automatiquement stockées dans Adobe Experience Platform. Voici comment y accéder :

1. **Requêtes du lac de données** : utilisez SQL pour interroger le jeu de données `journey_step_events` avec le [service de requête](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=fr){target="_blank"}.
2. **Customer Journey Analytics** : analysez des données de parcours au moyen d’[outils d’analyse avancés](cja-ajo.md).
3. **Reporting en temps réel** : accédez aux données par le biais des [fonctionnalités de reporting intégrées](gs-reports.md) de Journey Optimizer.
4. **API** : accédez par programme aux données d’événement pour les applications personnalisées.

En savoir plus sur l’[accès aux jeux de données](../data/datasets-query-examples.md).

### Points de données clés disponibles {#key-data-points}

Les événements d’étape de parcours capturent des informations complètes, notamment :

- **Identification du parcours** : [ID du parcours, version et nom](sharing-journey-fields.md).
- **Informations sur le profil** : [ID du profil et identités associées](sharing-identity-fields.md).
- **Détails de l’étape** : [nom du nœud, type d’étape et statut d’exécution](sharing-common-fields.md).
- **Horodatages** : durée précise de chaque étape de parcours.
- **Résultats de l’action** : [statut de réussite/d’échec et détails de l’exécution](sharing-execution-fields.md).
- **Informations sur les erreurs** : [codes d’erreur détaillés et leur description](sharing-field-list.md#discarded-events) lorsque des problèmes se produisent.

Explorez toutes les [définitions de champ disponibles](sharing-field-list.md).

### Cas d’utilisation courants {#common-use-cases}

**Surveillance des performances**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**Analyse des erreurs**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**Analyse de l’entonnoir du parcours**

- Suivre les taux de conversion à chaque étape du parcours
- Identifier à quel moment les profils quittent le plus souvent le parcours
- Mesurer le temps passé dans les différentes phases du parcours

Découvrez d’autres [techniques de requête pour l’analyse d’entonnoir](query-examples.md#common-queries).

## Exemples et ressources {#samples-resources}

### Exemples et modèles de requête {#query-examples}

Explorez des exemples de requête complets pour l’analyse d’événements d’étapes de parcours le plus courants :

- **[Exemples de requête d’événement d’étape de parcours](query-examples.md)** : requêtes SQL prêtes à l’emploi pour les scénarios d’analyse les plus courants.
- **[Exemples de requête de jeu de données](../data/datasets-query-examples.md#journey-step-event)** : exemples de requêtes sur les jeux de données d’événement d’étape de parcours.
- **[Requêtes basées sur des profils](query-examples.md#profile-based-queries)** : suivez les parcours et interactions de profils spécifiques.

### Documentation des champs {#field-documentation}

Examinez la structure de données complète des événements d’étape de parcours :

- **[Liste des champs d’événement d’étape de parcours](sharing-field-list.md)** : référence complète de tous les champs disponibles.
- **[Champs communs](sharing-common-fields.md)** : champs partagés sur journeyStepEvent et journeyStepProfileEvent.
- **[Champs d’exécution d’action](sharing-execution-fields.md)** : champs spécifiques au suivi de l’exécution de l’action.
- **[Champs du parcours](sharing-journey-fields.md)** : métadonnées et identifiants spécifiques au parcours.

### Bonnes pratiques et résolution des problèmes {#best-practices}

**Optimisation des performances**

- Utilisez `journeyVersionID` au lieu de `journeyVersionName` pour améliorer les performances des requêtes ([en savoir plus sur les propriétés de parcours](../building-journeys/expression/journey-properties.md)).
- Filtrez par périodes pour améliorer la vitesse des requêtes sur des jeux de données volumineux.
- Tirez parti des identités de profil qui correspondent à la [configuration de l’espace de noms de votre parcours](../building-journeys/entry-management.md).

**Qualité des données**

- Surveillez régulièrement les [événements ignorés](sharing-field-list.md#discarded-events) pour identifier les problèmes de données.
- Vérifiez que les schémas d’événement correspondent aux exigences de votre analyse.
- Implémentez une gestion appropriée des erreurs dans les requêtes personnalisées.

**Stratégies d’analyse**

- Combinez des événements d’étape de parcours avec des [données de retour de message](../data/datasets-query-examples.md#message-feedback-event-dataset) pour une attribution complète.
- Utilisez l’analyse temporelle pour comprendre la vitesse du parcours et les goulots d’étranglement.

### Fonctionnalités d’analyse avancées {#advanced-analytics}

Intégration de **Customer Journey Analytics**
Les événements d’étape de parcours peuvent être analysés à l’aide de [Customer Journey Analytics](cja-ajo.md) pour :

- Modélisation d’attribution avancée
- Visualisation de parcours cross-canal
- Analyse prédictive des résultats du parcours

Découvrez comment [configurer Customer Journey Analytics](report-gs-cja.md) pour les données Journey Optimizer.

## Ressources supplémentaires {#additional-resources}

### Liens vers la documentation {#documentation-links}

- **[Présentation du partage des étapes de parcours](sharing-overview.md)** : comprendre le flux des données de parcours vers Adobe Experience Platform.
- **[Dictionnaire des schémas natifs](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr){target="_blank"}** : référence complète des schémas XDM.
- **[Création de rapports Journey Optimizer](report-gs-cja.md)** : présentation des fonctionnalités de création de rapports dans Journey Optimizer.

### Guides d’intégration {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)** : analyse des données Journey Optimizer dans CJA.
- **[Gestion des données](../data/export-datasets.md)** : exporter et gérer des données de parcours.
- **[Confidentialité et gouvernance](../privacy/audit-logs.md)** : considérations relatives à la gouvernance des données pour les événements de parcours.


**Étapes suivantes :**

- Commencez par [créer vos premiers rapports de parcours](sharing-overview.md).
- Explorez les [exemples de requête](query-examples.md) pour des cas d’utilisation spécifiques.
- En savoir plus sur [les bonnes pratiques relatives à la gestion des parcours](../building-journeys/journey.md).
