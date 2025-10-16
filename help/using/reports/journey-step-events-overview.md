---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation d’événements d’étape de parcours
description: Découvrez comment utiliser les événements d’étape de parcours dans Adobe Journey Optimizer - comprenez ce qu’ils sont, pourquoi ils sont importants et comment les utiliser à des fins d’analyse et d’optimisation
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin, User
level: Intermediate, Experienced
keywords: parcours, événements d’étape, analyse, création de rapports, surveillance, XDM
hide: true
hidefromtoc: true
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 1%

---

# Utilisation d’événements d’étape de parcours {#work-with-journey-step-events}

Les événements d’étape de parcours sont des événements générés automatiquement qui capturent des informations détaillées sur chaque étape qu’un [profil](../audience/get-started-profiles.md) suit pendant leur progression dans un [parcours &#x200B;](../building-journeys/journey.md) dans Adobe Journey Optimizer. Ces événements offrent une visibilité complète sur les performances du parcours [&#128279;](../building-journeys/report-journey.md) et activent de puissantes fonctionnalités d’analyse.

## Que sont les événements d’étape de parcours ? {#what-are-step-events}

Les événements d’étape de parcours sont des événements [XDM (modèle de données d’expérience)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"} générés par le système et automatiquement créés et envoyés par Adobe Journey Optimizer à [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=fr){target="_blank"} chaque fois qu’un profil passe d’un nœud à un autre dans un parcours. Chaque événement correspond à une activité de parcours [spécifique](../building-journeys/about-journey-activities.md) ou à une transition dans l’expérience de parcours du client.

Il existe deux types principaux d’événements d’étape de parcours :

- **journeyStepEvent** : événements liés à la progression d’un profil individuel via des étapes de parcours
- **journeyStepProfileEvent** : événements qui incluent des informations contextuelles de profil supplémentaires

### Qu’est-ce qui déclenche les événements d’étape de parcours ? {#event-triggers}

Les événements d’étape de parcours sont générés automatiquement pour diverses activités de parcours :

- **Événements d’entrée** : lorsqu’un profil [entre dans un parcours &#x200B;](../building-journeys/entry-management.md)
- **Exécution d’action** : lorsque [&#x200B; messages sont envoyés](../building-journeys/journeys-message.md) ou [actions personnalisées](../building-journeys/using-custom-actions.md) sont effectuées
- **Évaluation des conditions** : lorsque les profils passent par des [conditions](../building-journeys/condition-activity.md) et des points de décision
- **Activités d’attente** : lorsque les profils entrent et sortent [nœuds d’attente](../building-journeys/wait-activity.md)
- **Événements de sortie** : lorsque les profils terminent ou [quittent un parcours &#x200B;](../building-journeys/end-journey.md)
- **Gestion des erreurs** : quand des erreurs se produisent lors de l’exécution du parcours

>[!NOTE]
>
>Les événements d’étape de parcours sont activés par défaut sur toutes les instances. Vous ne pouvez pas modifier ni mettre à jour les [schémas et jeux de données](sharing-overview.md) créés lors de l’approvisionnement des événements d’étape. Ces schémas et jeux de données sont en mode lecture seule.

En savoir plus sur les [schémas d’événement d’étape de parcours &#x200B;](sharing-field-list.md).

## Importance des événements d’étape de parcours {#why-step-events-matter}

Les événements d’étape de parcours fournissent une valeur essentielle aux organisations qui utilisent Adobe Journey Optimizer :

### Analyse et surveillance en temps réel {#real-time-analytics}

- **Suivi des performances des Parcours** : surveillez le flux des profils dans vos parcours en temps réel à l’aide de [rapports dynamiques](live-report.md)
- **Analyse des conversions** : comprendre les points de chute et les chemins de conversion réussis avec [l’analyse des parcours &#x200B;](journey-global-report-cja.md)
- **Détection des erreurs** : identifiez et résolvez les problèmes qui se produisent par le biais de [surveillance et alertes](alerts.md)

### Intégration des données et informations {#data-integration}

- **Analyse multi-plateformes** : combiner des données de parcours avec d’autres [sources de données Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
- **Vue Client 360** : créez des [profils client](../audience/get-started-profiles.md) complets qui incluent les interactions de parcours
- **Modélisation d’attribution** : connecter des points de contact de parcours aux résultats commerciaux en aval à l’aide de [Customer Journey Analytics](cja-ajo.md)

### Opportunités d’optimisation {#optimization}

- **Informations sur les tests A/B** : analysez les performances des différents chemins de parcours à l’aide de l’[expérimentation](campaign-global-report-cja-experimentation.md)
- **Amélioration de Personalization** : utilisez les données de comportement du parcours pour améliorer les expériences futures avec le [contenu dynamique](../personalization/dynamic-content.md)
- **Efficacité opérationnelle** : identifier les goulets d’étranglement et optimiser la conception des parcours [&#128279;](../building-journeys/using-the-journey-designer.md)

## Utilisation des événements d’étape de parcours {#how-to-use-step-events}

### Accès aux données d’événement d’étape de parcours {#accessing-data}

Les données d’événement d’étape de parcours sont automatiquement stockées dans Adobe Experience Platform et sont accessibles via :

1. **Requêtes du lac de données** : utilisez SQL pour interroger le jeu de données `journey_step_events` avec [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=fr){target="_blank"}
2. **Customer Journey Analytics** : analyse des données de parcours au moyen d’[&#x200B; outils d’analyse avancés](cja-ajo.md)
3. **Rapports en temps réel** : accédez aux données par le biais de Journey Optimizer [fonctionnalités de rapports intégrées](gs-reports.md)
4. **API** : accès par programmation aux données d’événement pour les applications personnalisées

En savoir plus sur l’[accès aux jeux de données](../data/datasets-query-examples.md).

### Points de données clés disponibles {#key-data-points}

Les événements d’étape parcours capturent des informations complètes, notamment :

- **identification du Parcours** : [ID du Parcours, version et nom](sharing-journey-fields.md)
- **Informations de profil** : [Identifiant du profil et identités associées](sharing-identity-fields.md)
- **Détails de l’étape** : [nom du nœud, type d’étape et statut d’exécution](sharing-common-fields.md)
- **Horodatages** : durée précise de chaque étape de parcours.
- **Résultats de l’action** : [statut de succès/échec et détails d’exécution](sharing-execution-fields.md)
- **Informations sur les erreurs** : détails [codes d’erreur et descriptions](sharing-field-list.md#discarded-events) lorsque des problèmes se produisent

Explorez toutes les [définitions de champ disponibles](sharing-field-list.md).

### Cas d&#39;utilisation courants {#common-use-cases}

**Suivi des performances**

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

**Analyse Parcours funnel**

- Suivre les taux de conversion à chaque étape du parcours
- Identifier où les profils quittent le plus souvent le parcours
- Mesurer le temps passé dans différentes phases du parcours

En savoir plus [techniques de requête pour l’analyse funnel](query-examples.md#common-queries).

## Exemples et ressources {#samples-resources}

### Exemples et modèles de requête {#query-examples}

Explorez des exemples de requête complets pour l’analyse d’événement d’étape de parcours courante :

- **[Exemples de requête d’événement d’étape de Parcours](query-examples.md)** : requêtes SQL prêtes à l’emploi pour les scénarios d’analyse courants
- **[Exemples de requête de jeu de données](../data/datasets-query-examples.md#journey-step-event)** : exemples de jeux de données d’événements d’étapes de parcours d’interrogation
- **[Requêtes basées sur des profils](query-examples.md#profile-based-queries)** : suivez les parcours et interactions de profils individuels

### Documentation du champ {#field-documentation}

Comprenez la structure de données complète des événements d’étape de parcours :

- **[Liste des champs d’événement d’étape de Parcours](sharing-field-list.md)** : référence complète de tous les champs disponibles
- **[Champs communs](sharing-common-fields.md)** : champs partagés sur journeyStepEvent et journeyStepProfileEvent
- **[Champs d’exécution d’action](sharing-execution-fields.md)** : champs spécifiques au tracking de l’exécution de l’action
- **[champs de Parcours](sharing-journey-fields.md)** : métadonnées et identifiants spécifiques au Parcours

### Bonnes pratiques et résolution des problèmes {#best-practices}

**Optimisation des performances**

- Utilisez `journeyVersionID` au lieu de `journeyVersionName` pour de meilleures performances des requêtes ([en savoir plus sur les propriétés de parcours &#x200B;](../building-journeys/expression/journey-properties.md)).
- Filtrer par périodes pour améliorer la vitesse de requête sur les jeux de données volumineux
- Tirez parti des identités de profil qui correspondent à la configuration de votre espace de noms de parcours [&#128279;](../building-journeys/entry-management.md)

**Qualité des données**

- Surveillez régulièrement les [&#x200B; événements ignorés &#x200B;](sharing-field-list.md#discarded-events) pour identifier les problèmes de données
- Vérifiez que les schémas d’événement correspondent aux exigences de votre analyse.
- Implémenter une gestion appropriée des erreurs dans les requêtes personnalisées

**Stratégies Analytics**

- Combinez des événements d’étape de parcours avec des [données de commentaires de message](../data/datasets-query-examples.md#message-feedback-event-dataset) pour une attribution complète
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

- **[Présentation du partage des étapes de Parcours](sharing-overview.md)** : comprendre le flux des données de parcours vers Adobe Experience Platform
- **[Dictionnaire des schémas natifs](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr){target="_blank"}** : référence complète des schémas XDM
- **[Création de rapports Journey Optimizer](report-gs-cja.md)** : présentation des fonctionnalités de création de rapports dans Journey Optimizer

### Guides d’intégration {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)** : analyse des données Journey Optimizer dans CJA
- **[Gestion des données](../data/export-datasets.md)** : exporter et gérer des données de parcours
- **[Confidentialité et gouvernance](../privacy/audit-logs.md)** : considérations relatives à la gouvernance des données pour les événements de parcours


**Étapes suivantes :**

- Commencez par [créer vos premiers rapports de parcours &#x200B;](sharing-overview.md)
- Explorez les [exemples de requête](query-examples.md) pour des cas d’utilisation spécifiques
- Découvrez les [bonnes pratiques de gestion des parcours &#x200B;](../building-journeys/journey.md)
