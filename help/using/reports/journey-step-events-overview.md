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
exl-id: 9f8e7d6c-5b4a-3928-1756-849302a11c2b
source-git-commit: df3abb7da17eb21e5e4120b55bdeb61fec3e202d
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 3%

---

# Utilisation d’événements d’étape de parcours {#work-with-journey-step-events}

Les événements d’étape de parcours sont des événements générés automatiquement qui capturent des informations détaillées sur chaque étape d’un profil au fur et à mesure de leur progression dans un parcours Adobe Journey Optimizer. Ces événements offrent une visibilité complète sur les performances du parcours et activent de puissantes fonctionnalités d’analyse.

## Que sont les événements d’étape de parcours ? {#what-are-step-events}

Les événements d’étape de parcours sont des événements XDM (modèle de données d’expérience) générés par le système que Adobe Journey Optimizer crée et envoie automatiquement à Adobe Experience Platform chaque fois qu’un profil passe d’un nœud à un autre dans un parcours. Chaque événement correspond à une action ou à une transition spécifique dans l’expérience de parcours du client ou de la cliente.

Il existe deux types principaux d’événements d’étape de parcours :

- **journeyStepEvent** : événements liés à la progression d’un profil individuel via des étapes de parcours
- **journeyStepProfileEvent** : événements qui incluent des informations contextuelles de profil supplémentaires

### Qu’est-ce qui déclenche les événements d’étape de parcours ? {#event-triggers}

Les événements d’étape de parcours sont générés automatiquement pour diverses activités de parcours :

- **Événements d’entrée** : lorsqu’un profil entre dans un parcours
- **Exécution d’action** : lorsque des messages sont envoyés ou que des actions personnalisées sont effectuées
- **Évaluation de condition** : lorsque les profils passent par des points de décision
- **Activités d’attente** : lorsque des profils entrent dans des nœuds d’attente et en sortent
- **Événements de sortie** : lorsque les profils terminent ou quittent un parcours
- **Gestion des erreurs** : quand des erreurs se produisent lors de l’exécution du parcours

>[!NOTE]
>
>Les événements d’étape de parcours sont activés par défaut sur toutes les instances. Vous ne pouvez pas modifier ni mettre à jour les schémas et les jeux de données créés lors de l’approvisionnement des événements d’étape. Ces schémas et jeux de données sont en mode lecture seule.

## Importance des événements d’étape de parcours {#why-step-events-matter}

Les événements d’étape de parcours fournissent une valeur essentielle aux organisations qui utilisent Adobe Journey Optimizer :

### Analyse et surveillance en temps réel {#real-time-analytics}

- **Suivi des performances des Parcours** : surveillez le flux des profils dans vos parcours en temps réel
- **Analyse des conversions** : comprendre les points de chute et les chemins de conversion réussis
- **Détection des erreurs** : identifier et résoudre les problèmes au fur et à mesure qu’ils se produisent

### Intégration des données et informations {#data-integration}

- **Analyse multi-plateformes** : combiner des données de parcours avec d’autres sources de données Adobe Experience Platform
- **Vue Client 360** : créez des profils client complets qui incluent des interactions de parcours
- **Modélisation d’attribution** : connecter les points de contact du parcours aux résultats commerciaux en aval

### Opportunités d’optimisation {#optimization}

- **Informations sur les tests A/B** : analysez les performances des différents chemins de parcours
- **Amélioration de Personalization** : utilisez les données de comportement du parcours pour améliorer les expériences futures
- **Efficacité opérationnelle** : identifier les goulets d&#39;étranglement et optimiser la conception des parcours

## Utilisation des événements d’étape de parcours {#how-to-use-step-events}

### Accès aux données d’événement d’étape de parcours {#accessing-data}

Les données d’événement d’étape de parcours sont automatiquement stockées dans Adobe Experience Platform et sont accessibles via :

1. **Requêtes du lac de données** : utilisez SQL pour interroger le jeu de données `journey_step_events`
2. **Customer Journey Analytics** : analyse des données de parcours à l’aide d’outils d’analyse avancés
3. **Création de rapports en temps réel** : accès aux données par le biais des fonctionnalités de création de rapports intégrées de Journey Optimizer
4. **API** : accès par programmation aux données d’événement pour les applications personnalisées

### Points de données clés disponibles {#key-data-points}

Les événements d’étape parcours capturent des informations complètes, notamment :

- **identification du Parcours** : ID de Parcours, version et nom
- **Informations de profil** : identifiant du profil et identités associées
- **Détails de l’étape** : nom du nœud, type d’étape et statut d’exécution
- **Horodatages** : durée précise de chaque étape de parcours.
- **Résultats de l’action** : statut de succès/échec et détails d’exécution
- **Informations sur les erreurs** : codes d’erreur détaillés et descriptions lorsque des problèmes se produisent

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

- Utilisez `journeyVersionID` au lieu de `journeyVersionName` pour de meilleures performances des requêtes.
- Filtrer par périodes pour améliorer la vitesse de requête sur les jeux de données volumineux
- Utiliser les identités de profil correspondant à la configuration de votre espace de noms de parcours

**Qualité des données**

- Surveillez régulièrement les [ événements ignorés ](sharing-field-list.md#discarded-events) pour identifier les problèmes de données
- Vérifiez que les schémas d’événement correspondent aux exigences de votre analyse.
- Implémenter une gestion appropriée des erreurs dans les requêtes personnalisées

**Stratégies Analytics**

- Combiner des événements d’étape de parcours avec des données de commentaires de message pour une attribution complète
- Utilisez l’analyse temporelle pour comprendre la vitesse du parcours et les goulots d’étranglement.
- Création d’analyses de cohortes pour comparer différentes variations de parcours

### Fonctionnalités d’analyse avancées {#advanced-analytics}

Intégration de **Customer Journey Analytics**
Les événements d’étape de parcours peuvent être analysés à l’aide de Customer Journey Analytics pour :

- Modélisation d’attribution avancée
- Visualisation de parcours cross-canal
- Analyse prédictive des résultats du parcours

**Prise de décision en temps réel**
Utilisez des modèles d’événement d’étape de parcours pour :

- Déclencher la personnalisation en temps réel
- Implémenter l’optimisation dynamique des parcours
- Activer les recommandations contextuelles sur la prochaine meilleure action

## Ressources supplémentaires {#additional-resources}

### Liens vers la documentation {#documentation-links}

- **[Présentation du partage des étapes de Parcours](sharing-overview.md)** : comprendre le flux des données de parcours vers Adobe Experience Platform
- **[Dictionnaire des schémas natifs](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr)** : référence complète des schémas XDM
- **[Création de rapports Journey Optimizer](report-gs-cja.md)** : présentation des fonctionnalités de création de rapports dans Journey Optimizer

### Guides d’intégration {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)** : analyse des données Journey Optimizer dans CJA
- **[Gestion des données](../data/export-datasets.md)** : exporter et gérer des données de parcours
- **[Confidentialité et gouvernance](../privacy/audit-logs.md)** : considérations relatives à la gouvernance des données pour les événements de parcours

Les événements d’étape de parcours constituent la base des analyses de parcours avancées dans Adobe Journey Optimizer. En comprenant et en exploitant efficacement ces événements, vous pouvez obtenir des informations détaillées sur le comportement des clients, optimiser les performances du parcours et offrir à vos clients et à vos clientes des expériences plus personnalisées.
