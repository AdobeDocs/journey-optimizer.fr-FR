---
solution: Journey Optimizer
product: journey optimizer
title: Parcours et campagnes - Choisir la bonne approche
description: Comparez les parcours, les campagnes et les campagnes orchestrées afin de choisir l’approche appropriée à vos besoins marketing dans Adobe Journey Optimizer
feature: Journeys, Campaigns, Get Started, Overview
role: User
level: Beginner
keywords: parcours, campagne, orchestré, comparaison, choisir, décision, workflow, temps réel, lot, orchestration, à plusieurs étapes, planifié, déclenché par API, piloté par événement
hide: true
hidefromtoc: true
source-git-commit: c1efa56fc3f3c93bdc4b9c7a9f4e81b58cbcff72
workflow-type: tm+mt
source-wordcount: '1453'
ht-degree: 4%

---


# Parcours et campagnes : choisissez la bonne approche {#journeys-vs-campaigns}

Adobe Journey Optimizer propose trois approches puissantes pour atteindre et impliquer vos clients. Il est essentiel de comprendre quand utiliser chacun d’eux pour créer des expériences marketing efficaces.

Ce guide vous aide à choisir entre **Parcours**, **Campagnes d’action**, **Campagnes déclenchées par l’API** et **Campagnes orchestrées** en fonction de vos besoins marketing spécifiques.

## Aperçu de la comparaison rapide {#quick-overview}

| Approche | Idéal pour | Style d&#39;exécution |
|----------|----------|-----------------|
| **Parcours** | Expériences client en temps réel et à plusieurs étapes avec logique conditionnelle | 1:1 orchestration : chaque profil à son propre rythme |
| **Campagnes d’action** | Diffusions planifiées ou récurrentes vers les audiences | Exécution par lots : audience traitée ensemble au moment de l’envoi |
| **Campagnes déclenchées par API** | Messages déclenchés par un événement ou transactionnels provenant de systèmes externes | Exécution à la demande : déclenchée par un appel API avec payload |
| **Campagnes orchestrées** | Workflows par lots complexes avec segmentation d’entités multiples | Zone de travail par lots : tous les profils sont traités ensemble |

## Comparaison détaillée {#detailed-comparison}

Utilisez ce tableau complet pour comprendre les principales différences :

| Fonctionnalité | Parcours | Campagnes d’action | Campagnes déclenchées par API | Campagnes orchestrées |
|---------|----------|------------------|------------------------|----------------------|
| **Objectif de Principal** | Orchestration en plusieurs étapes 1:1 avec contexte client en temps réel | Diffusion de messages ponctuelle ou récurrente aux audiences | Messages transactionnels ou pilotés par un événement déclenchés par des systèmes externes | Campagnes par lots à plusieurs étapes avec des workflows de segmentation complexes |
| **Type de zone de travail** | 1:1 toile - chaque profil voyage à son propre rythme | Aucune zone de travail - exécution d’action unique | Aucune zone de travail - exécution d’action unique | Zone de travail par lots : tous les profils sont traités ensemble |
| **Flux d’exécution** | Actions séquentielles, le profil conserve l’état tout au long du parcours | Exécution simultanée pour l’audience entière | Exécution immédiate par appel API | Workflow par lots à plusieurs étapes avec activités et transitions |
| **Mécanisme d’entrée** | Événements, audiences, qualifications, événements métier | Activation et planification manuelles | Appel API depuis un système externe | Exécution planifiée du workflow par lots |
| **Modèle de données** | Profil en temps réel + données d’événement | Données de profil des audiences Experience Platform | Données de payload de l’API avec recherche de profil facultative | Données relationnelles multi-entités (profils, produits, boutiques, réservations) |
| **Segmentation** | Audiences préconfigurées + conditions en temps réel | Audiences préconfigurées à partir d’Experience Platform | Ciblage piloté par la payload (aucune audience planifiée) | Audiences à la demande créées dans la zone de travail avec un nombre exact |
| **Traitement des profils** | Individuel, en temps réel (au fur et à mesure des événements) | Lot, tous en même temps | Par appel API, piloté par la payload | Lot, le tout avec prise en charge multi-entités |
| **Personnalisation** | Données contextuelles en temps réel + attributs de profil | Attributs de profil | Données de payload + attributs de profil facultatifs | Données à entités multiples pour le ciblage de précision |
| **Complexité** | Plusieurs étapes avec embranchement, temps d’attente, conditions | Action unique ou workflow simple | Action unique avec mappage de la payload | Workflows par lots à plusieurs étapes avec segmentation, enrichissement et divisions |
| **Idéal pour** | Parcours du cycle de vie du client, intégration, abandon de panier | Campagnes promotionnelles, newsletters, annonces | Confirmations de commande, alertes d’expédition, réinitialisations de mot de passe | Campagnes saisonnières complexes, promotions à plusieurs étapes, lancements de produits |
| **Planning** | Continu, toujours actif une fois publié | Dates de début/fin planifiées | À la demande, piloté par les événements via l’API | Exécution par lots selon le calendrier |
| **Gestion des états** | Maintient l’état du client pour les actions en temps réel | Exécution sans état | Exécution sans état par appel | Traitement par lots avec tables de travail |
| **Utiliser quand** | Plusieurs points de contact nécessaires avec la logique de décision en temps réel | Message simple à une audience à une heure spécifique | Le système externe doit déclencher un message immédiatement | Nécessite une segmentation complexe, des données multi-entités ou des nombres exacts de pré-envois |
| **Fonctionnalités uniques** | Réactions en temps réel, activités d’attente, fréquence basée sur les profils | Planification, ciblage d&#39;audience, contrôle des taux | Mappage de la payload de l’API, déclenchement système à système | Jeux de données relationnels, segmentation d’entités multiples, nombres exacts, envoi à plusieurs niveaux |

## Guide de décision {#decision-guide}

Suivez cet arbre de décision pour choisir la bonne approche :

### Étape 1 : Quelle est votre exigence d’exécution ?

**Réactions individuelles en temps réel au comportement des clients ?**
→ **Utiliser des Parcours**
* Les profils doivent avancer à leur propre rythme
* Logique conditionnelle basée sur le comportement
* Le contexte en temps réel est essentiel.

**Diffusion simple d’un message à une audience à une heure planifiée ?**
→ **Utiliser des campagnes d’action**
* Tous les profils reçoivent le message simultanément
* Envois planifiés ou récurrents
* Aucune logique complexe à plusieurs étapes n’est nécessaire

**Message immédiat déclenché par un système externe ?**
→ **utiliser des campagnes déclenchées par API**
* Déclenché à la demande via un appel API
* Personnalisation basée sur la payload
* Aucune logique complexe à plusieurs étapes n’est nécessaire

**Workflow par lots complexe avec segmentation avancée ?**
→ **Utiliser des campagnes orchestrées**
* Données multi-entités nécessaires (produits, magasins, réservations)
* Exiger des nombres exacts de pré-envois
* Traitement par lots en plusieurs étapes avec fractionnement et enrichissement

### Étape 2 : valider votre choix

| Vos besoins | Approche recommandée | Pourquoi |
|-----------|---------------------|-----|
| Accueillir de nouveaux clients avec l’intégration en plusieurs étapes | Parcours | Entrée en temps réel, plusieurs points de contact, chemins conditionnels |
| Envoyer une newsletter mensuelle aux abonnés | Campagne d’action | Message planifié simple à l’audience |
| Abandon de panier avec séquence de rappel | Parcours | Déclencheur en temps réel, temps d&#39;attente, suivi conditionnel |
| Annonce promotionnelle à tous les clients | Campagne d’action | Message ponctuel, diffusion immédiate |
| Réengager les utilisateurs inactifs en fonction de leur comportement | Parcours | Déclenché par la qualification d’audience et le chemin personnalisé |
| Vente Flash déclenchée par un événement métier | Parcours (Événement métier) | Déclencheur en temps réel affectant plusieurs clients |
| Promotion saisonnière avec intégration du catalogue de produits | Campagne orchestrée | Données multi-entités, segmentation complexe, décomptes exacts |
| Message transactionnel déclenché par API | Campagne déclenchée par l’API | Déclencheur de système externe, diffusion immédiate |
| Envoi à plusieurs niveaux par réservation | Campagne orchestrée | Relations à entités multiples, un message par réservation |

## Principales distinctions expliquées {#key-distinctions}

### Parcours : 1:1 orchestration en temps réel

**Qu’est-ce qui le rend unique**
* Chaque profil conserve un état et un contexte individuels
* Les profils entrent et progressent à leur propre rythme
* Prise de décision en temps réel basée sur le comportement et les événements
* Les activités d’attente créent une durée personnalisée
* L’embranchement conditionnel crée des chemins uniques par profil

**Exemple de flux :**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Chaque client voit sa propre chronologie de parcours en fonction de ses actions.

[En savoir plus sur Parcours](../building-journeys/journey.md)

### Campagnes : diffusion simple par lots ou déclenchée

**Qu’est-ce qui le rend unique**
* Tous les profils sont traités de manière identique et simultanée
* Exécution sans état - aucun contexte conservé
* Planification simple ou déclenchement de l’API
* Idéal pour les communications de diffusion

**Exemple de flux :**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Tout le monde reçoit le même message en même temps.

**Types:**
* **Campagnes d’action** : diffusion planifiée vers les audiences (ponctuelle ou récurrente)
* **Campagnes déclenchées par API** : diffusion à la demande déclenchée par un appel API avec des données de payload

[En savoir plus sur les campagnes](../campaigns/get-started-with-campaigns.md)

### Campagnes orchestrées : workflows de zone de travail par lots

**Qu’est-ce qui le rend unique**
* Canevas par lots avec activités et transitions (similaire à la canevas par parcours, mais orienté lot)
* Prise en charge des données relationnelles à entités multiples (profils + produits + boutiques + réservations)
* Création d’audiences à la demande dans la zone de travail
* Nombre exact avant envoi (visibilité avant envoi)
* Envoi à plusieurs niveaux (un message par entité, par exemple, par réservation)
* Tous les profils traités ensemble par lots

**Exemple de flux :**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Associe la complexité du workflow à l’exécution de campagnes par lots.

[En savoir plus sur les campagnes orchestrées .](../orchestrated/gs-orchestrated-campaigns.md)

## Exemples de cas d’utilisation {#use-cases}

### Cas d’utilisation de parcours

* **Récupération après abandon de panier** : déclenché par l’événement d’ajout au panier, attente d’un passage en caisse, envoi de rappels en cas d’absence d’achat
* **Intégration des clients** : série de bienvenue à plusieurs étapes avec du contenu personnalisé basé sur les données de profil
* **Mise à niveau du niveau de fidélité** : déclenché lorsque le client atteint un nouveau niveau, envoyez des félicitations et des avantages
* **Campagnes d’anniversaire** : saisie basée sur la date de naissance, offres personnalisées
* **Réengagement** : déclenché par la qualification de l’audience (inactivité), la diffusion progressive

### Cas d’utilisation de Campaign (déclenchés par action et API)

**Campagnes d’action :**
* **Newsletters mensuelles** : diffusion par lots planifiée vers le segment des abonnés
* **Annonces promotionnelles** : offres sensibles au facteur temps destinées aux audiences cibles
* **Lancements de produits** : annonce coordonnée à l’intention de tous les clients
* **Salutations saisonnières** : messages de vacances à des dates spécifiques

**Campagnes déclenchées par l’API :**
* **Confirmations de commande** : Déclenché par le système e-commerce après l’achat
* **Notifications d’expédition** : déclenchées par le système logistique
* **Alertes de comptes** : Déclenché par le système de détection des fraudes
* **Réinitialisations du mot de passe** : déclenchées par une action de l’utilisateur dans l’application

### Cas d&#39;utilisation de Campaign orchestré

* **Promotion saisonnière avec intégration de catalogues** : interroger le catalogue de produits, identifier les clients éligibles, segmenter par préférences, envoyer des recommandations de produits personnalisées
* **Campagnes spécifiques au magasin** : ciblez les clients situés à proximité d’emplacements de magasin spécifiques avec des données d’inventaire de magasin.
* **Communications multi-réservation** : Envoyez un message par réservation (réservations d&#39;hôtel, réservations de vols)
* **Orchestration de segments complexes** : créez des audiences étape par étape avec un enrichissement à partir de plusieurs sources de données
* **Validation de la pré-envoi** : obtenez le nombre exact de destinataires avant de lancer des campagnes majeures

## Disponibilité des fonctionnalités {#feature-availability}

### Canaux

| Canal | Parcours | Campagnes d’action | Campagnes déclenchées par API | Campagnes orchestrées |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Notification push | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ |
| In-app | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Basé sur le code | ✅ | ✅ | ❌ | ❌ |
| Cartes de contenu | ✅ | ✅ | ❌ | ❌ |
| Courrier | ✅ | ✅ | ❌ | ❌ |

### Fonctionnalités avancées

| Fonctionnalité | Parcours | Campagnes d’action | Campagnes déclenchées par API | Campagnes orchestrées |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Workflows à plusieurs étapes | ✅ | ❌ | ❌ | ✅ |
| Déclencheurs en temps réel | ✅ | ❌ | ✅ | ❌ |
| Activités d’attente | ✅ | ❌ | ❌ | ✅ |
| Branchement conditionnel | ✅ | ❌ | ❌ | ✅ |
| Exécution planifiée | ✅ | ✅ | ✅ | ✅ |
| Déclenchement de l’API | ❌ | ❌ | ✅ | ❌ |
| Données multi-entités | ❌ | ❌ | ❌ | ✅ |
| Nombre exact de messages de pré-envoi | ❌ | ❌ | ❌ | ✅ |
| Segmentation à la demande | ❌ | ❌ | ❌ | ✅ |
| Optimisation de l’heure d’envoi | ✅ | ✅ | ✅ | ✅ |
| A/B testing | ✅ | ✅ | ❌ | ❌ |
| Workflows d’approbation | ✅ | ✅ | ✅ | ❌ |

## Questions courantes {#common-questions}

+++ Puis-je combiner des parcours et des campagnes dans ma stratégie marketing ?

Absolument ! La plupart des entreprises utilisent les trois approches pour différents scénarios :

* Parcours d’engagement comportemental en temps réel
* Action Campagnes pour les communications de diffusion planifiées
* Campagnes déclenchées par API pour les messages transactionnels
* Campagnes orchestrées pour des campagnes par lots complexes utilisant de nombreuses données

+++

+++ Puis-je convertir une campagne en parcours ou vice versa ?

Non, vous devez recréer l’expérience au format approprié. Cependant, vous pouvez réutiliser du contenu, des audiences et des concepts logiques.

+++

+++ Quelle approche est la plus facile à élaborer ?

Les campagnes d’action sont généralement les plus simples (message unique à l’audience), suivies des campagnes déclenchées par l’API, des Parcours (plus complexes avec une logique à plusieurs étapes) et des campagnes orchestrées (les plus complexes en raison des fonctionnalités de workflow de zone de travail et d’entités multiples).

+++

+++ Quelle est la plus adaptée aux audiences de grande taille ?

Tous trois peuvent être adaptés à l’échelle, mais :

* parcours Les campagnes **Lecture d’audience** et **Action** sont optimisées pour les audiences par lots volumineuses
* **Campagnes orchestrées** excellez dans la segmentation complexe avec des jeux de données volumineux
* **Parcours unitaires** traitez les profils individuellement, de sorte que l’échelle dépend du volume d’événements

+++

+++ Puis-je utiliser la même audience pour tous les parcours et campagnes ?

Oui, les audiences créées dans Adobe Experience Platform peuvent être utilisées selon les trois approches.

+++

## Étapes suivantes {#next-steps}

Vous souhaitez commencer à créer ? Consultez la documentation détaillée relative à l’approche choisie :

* **[Prise en main des Parcours](../building-journeys/journey.md)** - En savoir plus sur les types de parcours, le concepteur et les workflows
* **[Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)** - Explorer les campagnes déclenchées par une action et une API
* **[Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)** - Découverte des workflows de zone de travail par lots

**Besoin d’aide pour prendre une décision ?**
* [Comparaison des types de parcours](../building-journeys/journey.md#journey-types-comparison)
* [Comparaison des types de campagne](../campaigns/get-started-with-campaigns.md#campaign-types)
* [FAQ sur Parcours](../building-journeys/journey-faq.md)
* [FAQ sur les campagnes orchestrées](../orchestrated/orchestrated-campaigns-faq.md)

