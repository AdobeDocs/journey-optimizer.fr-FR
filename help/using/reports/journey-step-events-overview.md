---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des événements d’étape de parcours
description: 'Découvrez comment utiliser les événements d’étape de parcours dans Adobe Journey Optimizer : comprenez ce qu’ils sont, pourquoi ils sont importants et comment les utiliser à des fins d’analyse et d’optimisation.'
feature: Journeys, Reporting
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: parcours, événements d’étape, analyse, rapports, surveillance, XDM
source-git-commit: 17e0528849f2bd4d3cbf279c34c98a8359cad797
workflow-type: ht
source-wordcount: '898'
ht-degree: 100%

---

# Utiliser des événements d’étape de parcours {#work-with-journey-step-events}

Les événements d’étape de parcours sont des événements générés automatiquement qui capturent des informations détaillées sur chaque étape qu’un [profil](../audience/get-started-profiles.md) suit au fur et à mesure de sa progression dans un [parcours](../building-journeys/journey.md) dans Adobe Journey Optimizer. Ces événements offrent une visibilité complète sur les [performances du parcours](../building-journeys/report-journey.md) et permettent de puissantes fonctionnalités d’analyse.

## Présentation des événements d’étape de parcours {#what-are-step-events}

Les événements d’étape de parcours sont des événements [XDM (modèle de données d’expérience)](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/home){target="_blank"} générés par le système et automatiquement créés et envoyés par Adobe Journey Optimizer à [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=fr){target="_blank"} chaque fois qu’un profil passe d’un nœud à un autre dans un parcours. Chaque événement correspond à une [activité de parcours](../building-journeys/about-journey-activities.md) spécifique ou à une transition dans l’expérience de parcours du client ou de la cliente.

Il existe deux principaux types d’événements d’étape de parcours :

- **journeyStepEvent** : événements liés à la progression d’un profil individuel via les étapes d’un parcours.
- **journeyStepProfileEvent** : événements qui incluent des informations contextuelles de profil supplémentaires.

### Qu’est-ce qui déclenche les événements d’étape de parcours ? {#event-triggers}

Les événements d’étape de parcours sont générés automatiquement pour diverses activités de parcours :

- **Événements d’entrée** : lorsqu’un profil [rejoint un parcours](../building-journeys/entry-management.md).
- **Exécution d’action** : lorsque des [messages sont envoyés](../building-journeys/journeys-message.md) ou que des [actions personnalisées](../building-journeys/using-custom-actions.md) sont effectuées.
- **Évaluation des conditions** : lorsque les profils passent par des [conditions](../building-journeys/condition-activity.md) et des points de décision.
- **Activités d’attente** : lorsque les profils rejoignent et quittent des [nœuds d’attente](../building-journeys/wait-activity.md).
- **Événements de sortie** : lorsque les profils terminent ou [quittent un parcours ](../building-journeys/end-journey.md)
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

1. **Requêtes du lac de données** : utilisez SQL pour interroger le jeu de données `journey_step_events` avec [Query Service](https://experienceleague.adobe.com/fr/docs/experience-platform/query/home){target="_blank"}.
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

**Intégration de Customer Journey Analytics**
Vous pouvez analyser les événements d’étape de parcours à l’aide de [Customer Journey Analytics](cja-ajo.md) à des fins de :

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
