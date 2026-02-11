---
solution: Journey Optimizer
product: journey optimizer
title: 'Parcours ou campagnes : choisir la bonne approche'
description: Comparez les parcours, les campagnes et les campagnes orchestrées afin de choisir l’approche appropriée à vos besoins marketing dans Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
role: User
level: Beginner
keywords: parcours, campagne, orchestré, comparaison, choisir, décision, workflow, temps réel, lot, orchestration, à plusieurs étapes, planifié, déclenché par API, piloté par événement
hide: true
hidefromtoc: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
source-git-commit: 6a32a60f153ff4880ce974e77bc11eed1e20a7c7
workflow-type: tm+mt
source-wordcount: '1453'
ht-degree: 85%

---

# Parcours ou campagnes : choisir la bonne approche {#journeys-vs-campaigns}

Adobe Journey Optimizer propose trois approches puissantes pour atteindre et engager votre clientèle. Il est essentiel de comprendre quand utiliser chacune d’elles pour créer des expériences marketing efficaces.

Ce guide vous aide à choisir entre **Parcours**, **Campagnes d’action**, **Campagnes déclenchées par l’API** et **Campagnes orchestrées** en fonction de vos besoins marketing spécifiques.

## Comparaison rapide {#quick-overview}

| Approche | Idéal pour | Style d’exécution |
|----------|----------|-----------------|
| **Parcours** | Expériences clients en temps réel et à plusieurs étapes avec logique conditionnelle | Orchestration 1:1 : chaque profil à son propre rythme |
| **Campagnes d’action** | Diffusions planifiées ou récurrentes vers les audiences | Exécution par lots : audience traitée ensemble au moment de l’envoi |
| **Campagnes déclenchées par API** | Messages déclenchés par un événement ou transactionnels provenant de systèmes externes | Exécution à la demande : déclenchée par un appel API avec payload |
| **Campagnes orchestrées** | Workflows par lots complexes avec segmentation d’entités multiples | Zone de travail par lots : tous les profils sont traités ensemble. |

## Comparaison détaillée {#detailed-comparison}

Utilisez ce tableau complet pour comprendre les principales différences :

| Fonctionnalité | Parcours | Campagnes d’action | Campagnes déclenchées par API | Campagnes orchestrées |
|---------|----------|------------------|------------------------|----------------------|
| **Objectif principal** | Orchestration 1:1 en plusieurs étapes avec contexte client en temps réel | Diffusion de messages ponctuels ou récurrents aux audiences | Messages transactionnels ou pilotés par un événement déclenchés par des systèmes externes | Campagnes par lots en plusieurs étapes avec des workflows de segmentation complexes |
| **Type de zone de travail** | Zone de travail 1:1 : chaque profil évolue à son propre rythme. | Aucune zone de travail : exécution d’action unique | Aucune zone de travail : exécution d’action unique | Zone de travail par lots : tous les profils sont traités ensemble. |
| **Flux d’exécution** | Actions séquentielles, le profil conserve son état tout au long du parcours. | Exécution simultanée pour l’audience entière | Exécution immédiate par appel API | Workflow par lots en plusieurs étapes avec activités et transitions |
| **Mécanisme d’entrée** | Événements, audiences, qualifications, événements métier | Activation et planification manuelles | Appel API depuis un système externe | Exécution planifiée du workflow par lots |
| **Modèle de données** | Profil en temps réel + données d’événement | Données de profil des audiences Experience Platform | Données de payload de l’API avec recherche de profil facultative | Données relationnelles multi-entités (profils, produits, boutiques, réservations) |
| **Segmentation** | Audiences préconfigurées + conditions en temps réel | Audiences préconfigurées à partir d’Experience Platform | Ciblage piloté par la payload (aucune audience planifiée) | Audiences à la demande créées dans la zone de travail avec des nombres exacts |
| **Traitement du profil** | Individuel, en temps réel (au fur et à mesure des événements) | Par lots, tous en même temps | Par appel API, piloté par la payload | Par lots, le tout avec prise en charge multi-entités |
| **Personnalisation** | Données contextuelles en temps réel + attributs de profil | Attributs de profil | Données de payload + attributs de profil facultatifs | Données multi-entités pour un ciblage précis |
| **Complexité** | Plusieurs étapes avec embranchement, temps d’attente, conditions | Action unique ou workflow simple | Action unique avec mappage de la payload | Workflows par lots en plusieurs étapes avec segmentation, enrichissement et partages |
| **Idéal pour** | Parcours du cycle de vie client, intégration, abandon de panier | Campagnes promotionnelles, newsletters, annonces | Confirmations de commande, alertes d’expédition, réinitialisations de mot de passe | Campagnes saisonnières complexes, promotions en plusieurs étapes, lancements de produits |
| **Timing** | Continu, toujours actif une fois publié | Dates de début/fin planifiées | À la demande, piloté par les événements via l’API | Exécution par lots selon le planning |
| **Gestion des états** | Maintient l’état de la clientèle pour les actions en temps réel. | Exécution sans état | Exécution sans état par appel | Traitement par lots avec tables de travail |
| **À utiliser quand** | Plusieurs points de contact sont nécessaires avec la logique de décision en temps réel. | Message simple à une audience à une heure spécifique | Le système externe doit déclencher un message immédiatement | Nécessite une segmentation complexe, des données multi-entités ou des nombres exacts de pré-envois. |
| **Fonctionnalités uniques** | Réactions en temps réel, activités d’attente, fréquence basée sur les profils | Planification, ciblage d&#39;audience, contrôle des taux | Mappage de la payload de l’API, déclenchement système à système | Jeux de données relationnels, segmentation multi-entités, nombres exacts, envoi à plusieurs niveaux |

## Guide de décision {#decision-guide}

Suivez cet arbre de décision pour choisir la bonne approche :

### Étape 1 : quelle est votre exigence d’exécution ?

**Réactions individuelles en temps réel au comportement de la clientèle ?**
→ **Utiliser des parcours**
* Les profils doivent progresser à leur propre rythme.
* Logique conditionnelle basée sur le comportement
* Le contexte en temps réel est essentiel.

**Diffusion simple d’un message à une audience à une heure planifiée ?**
→ **Utiliser des campagnes d’action**
* Tous les profils reçoivent le message simultanément.
* Envois planifiés ou récurrents
* Aucune logique complexe à plusieurs étapes n’est nécessaire.

**Message immédiat déclenché par un système externe ?**
→ **utiliser des campagnes déclenchées par API**
* Déclenché à la demande via un appel API
* Personnalisation basée sur la payload
* Aucune logique complexe à plusieurs étapes n’est nécessaire.

**Workflow par lots complexe avec segmentation avancée ?**
→ **Utiliser des campagnes orchestrées**
* Données multi-entités nécessaires (produits, magasins, réservations)
* Exiger des nombres exacts de pré-envois
* Traitement par lots en plusieurs étapes avec partages et enrichissement

### Étape 2 : valider votre choix

| Vos besoins | Approche recommandée | Pourquoi |
|-----------|---------------------|-----|
| Accueillir une nouvelle clientèle avec l’intégration en plusieurs étapes | Parcours | Entrée en temps réel, plusieurs points de contact, chemins conditionnels |
| Envoyer une newsletter mensuelle aux personnes abonnées | Campagne d’action | Message planifié simple à l’audience |
| Abandon de panier avec séquence de rappel | Parcours | Déclencheur en temps réel, temps d’attente, suivi conditionnel |
| Annonce promotionnelle à l’ensemble de la clientèle | Campagne d’action | Message ponctuel, diffusion immédiate |
| Réengager les personnes inactives en fonction de leur comportement | Parcours | Déclenché par la qualification d’audience, chemin personnalisé |
| Vente flash déclenchée par un événement métier | Parcours (événement métier) | Déclencheur en temps réel affectant plusieurs membres de la clientèle |
| Promotion saisonnière avec intégration du catalogue de produits | Campagne orchestrée | Données multi-entités, segmentation complexe, nombres exacts |
| Message transactionnel déclenché par API | Campagne déclenchée par API | Déclencheur de système externe, diffusion immédiate |
| Envoi à plusieurs niveaux par réservation | Campagne orchestrée | Relations multi-entités, un message par réservation |

## Principales distinctions expliquées {#key-distinctions}

### Parcours : orchestration en temps réel 1:1

**Qu’est-ce qui rend cela unique ?**
* Chaque profil conserve un état et un contexte individuels.
* Les profils rejoignent le parcours et progressent à leur propre rythme.
* Prise de décision en temps réel basée sur le comportement et les événements
* Les activités d’attente créent un timing personnalisé.
* L’embranchement conditionnel crée des chemins uniques par profil.

**Exemple de flux :**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Chaque personne voit sa propre chronologie de parcours en fonction de ses actions.

[En savoir plus sur les parcours](../building-journeys/journey.md)

### Campagnes : diffusion simple par lots ou déclenchée

**Qu’est-ce qui rend cela unique ?**
* Tous les profils sont traités de manière identique et simultanée.
* Exécution sans état : aucun contexte conservé
* Planification simple ou déclenchement par API
* Idéal pour les communications de diffusion

**Exemple de flux :**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Tout le monde reçoit le même message en même temps.

**Types :**
* **Campagnes d’action** : diffusion planifiée vers les audiences (ponctuelle ou récurrente)
* **Campagnes déclenchées par API** : diffusion à la demande déclenchée par un appel API avec des données de payload

[En savoir plus sur les campagnes](../campaigns/get-started-with-campaigns.md)

### Campagnes orchestrées : workflows de zone de travail par lots

**Qu’est-ce qui rend cela unique ?**
* Zone de travail par lots avec activités et transitions (similaire à la zone de travail de parcours, mais orientée lots)
* Prise en charge des données relationnelles multi-entités (profils + produits + magasins + réservations)
* Création d’audiences à la demande dans la zone de travail
* Nombres exacts avant envoi (visibilité avant envoi)
* Envoi à plusieurs niveaux (un message par entité, par exemple, par réservation)
* Tous les profils sont traités ensemble par lots.

**Exemple de flux :**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Associe la complexité du workflow à l’exécution de campagnes par lots.

[En savoir plus sur les campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

## Exemples de cas d’utilisation {#use-cases}

### Cas d’utilisation de parcours

* **Récupération après abandon de panier** : déclenché par l’événement d’ajout au panier, attente d’un passage en caisse, envoi de rappels en cas d’absence d’achat
* **Intégration de la clientèle** : série de bienvenue à plusieurs étapes avec du contenu personnalisé basé sur les données de profil
* **Mise à niveau du niveau de fidélité** : déclenché lorsque le client ou la cliente atteint un nouveau niveau, en vue d’envoyer des félicitations et des avantages.
* **Campagnes d’anniversaire** : entrée basée sur la date de naissance, offres personnalisées
* **Réengagement** : déclenché par la qualification de l’audience (inactivité), la diffusion progressive

### Cas d’utilisation des campagnes (action et déclenchées par API)

**Campagnes d’action :**
* **Newsletters mensuelles** : diffusion par lots planifiée vers le segment des personnes abonnées
* **Annonces promotionnelles** : offres sensibles au facteur temps destinées aux audiences cibles
* **Lancements de produits** : annonce coordonnée à l’intention de l’ensemble de la clientèle
* **Vœux saisonniers** : messages de vœux à des dates spécifiques

**Campagnes déclenchées par API :**
* **Confirmations de commande** : déclenchées par le système e-commerce après l’achat
* **Notifications d’expédition** : déclenchées par le système logistique
* **Alertes de comptes** : déclenchées par le système de détection des fraudes
* **Réinitialisations du mot de passe** : déclenchées par une action de la personne dans l’application

### Cas d’utilisation des campagnes orchestrées

* **Promotion saisonnière avec intégration de catalogues** : interrogez le catalogue de produits, identifiez la clientèle éligible, segmentez par préférences, envoyez des recommandations de produits personnalisées.
* **Campagnes spécifiques au magasin** : ciblez la clientèle située à proximité d’emplacements de magasin spécifiques avec des données d’inventaire de magasin.
* **Communications multi-réservations** : envoyez un message par réservation (réservations d’hôtel, réservations de vols).
* **Orchestration de segments complexes** : créez des audiences étape par étape avec un enrichissement à partir de plusieurs sources de données.
* **Validation de pré-envoi** : obtenez les nombres exacts de destinataires avant de lancer des campagnes majeures.

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
| Courrier | ✅ | ✅ | ❌ | ✅ |

### Fonctionnalités avancées

| Fonctionnalité | Parcours | Campagnes d’action | Campagnes déclenchées par API | Campagnes orchestrées |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Workflows en plusieurs étapes | ✅ | ❌ | ❌ | ✅ |
| Déclencheurs en temps réel | ✅ | ❌ | ✅ | ❌ |
| Activités d’attente | ✅ | ❌ | ❌ | ✅ |
| Branchement conditionnel | ✅ | ❌ | ❌ | ✅ |
| Exécution planifiée | ✅ | ✅ | ✅ | ✅ |
| Déclenchement de l’API | ❌ | ❌ | ✅ | ❌ |
| Données multi-entités | ❌ | ❌ | ❌ | ✅ |
| Nombres exacts de messages de pré-envoi | ❌ | ❌ | ❌ | ✅ |
| Segmentation à la demande | ❌ | ❌ | ❌ | ✅ |
| Optimisation de l’heure d’envoi | ✅ | ✅ | ✅ | ✅ |
| Tests A/B | ✅ | ✅ | ❌ | ❌ |
| Workflows d’approbation | ✅ | ✅ | ✅ | ❌ |

## Questions courantes {#common-questions}

+++ Puis-je combiner des parcours et des campagnes dans ma stratégie marketing ?

Absolument ! La plupart des entreprises utilisent les trois approches pour différents scénarios :

* Parcours d’engagement comportemental en temps réel
* Campagnes d’action pour les communications de diffusion planifiées
* Campagnes déclenchées par API pour les messages transactionnels
* Campagnes orchestrées pour des campagnes par lots complexes utilisant de nombreuses données

+++

+++ Puis-je convertir une campagne en parcours ou inversement ?

Non, vous devez recréer l’expérience au format approprié. Cependant, vous pouvez réutiliser du contenu, des audiences et des concepts logiques.

+++

+++ Quelle approche est la plus facile à élaborer ?

Les campagnes d’action sont généralement les plus simples (message unique à l’audience), suivies des campagnes déclenchées par API, des parcours (plus complexes avec une logique à plusieurs étapes) et des campagnes orchestrées (les plus complexes en raison des fonctionnalités de workflow de zone de travail et multi-entités).

+++

+++ Quelle est l’approche la plus adaptée aux audiences de grande taille ?

Les trois peuvent être adaptées à l’échelle, mais :

* Les **parcours de lecture d’audience** et les **campagnes d’action** sont optimisés pour les audiences par lots de grande taille.
* Les **campagnes orchestrées** excellent dans la segmentation complexe avec des jeux de données volumineux.
* Les **parcours unitaires** traitent les profils individuellement, de sorte que l’échelle dépend du volume d’événements.

+++

+++ Puis-je utiliser la même audience pour l’ensemble des parcours et campagnes ?

Oui, les audiences créées dans Adobe Experience Platform peuvent être utilisées selon les trois approches.

+++

## Étapes suivantes {#next-steps}

Vous souhaitez commencer à créer ? Consultez la documentation détaillée relative à l’approche choisie :

* **[Commencer avec les parcours](../building-journeys/journey.md)** : découvrez les types de parcours, le concepteur et les workflows.
* **[Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)** : explorez les campagnes d’action et déclenchées par API.
* **[Commencer avec les campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)** : découvrez les workflows de zone de travail par lots.

**Besoin d’aide pour prendre une décision ?**
* [Comparaison des types de parcours](../building-journeys/journey.md#journey-types-comparison)
* [Comparaison des types de campagne](../campaigns/get-started-with-campaigns.md#campaign-types)
* [Questions fréquentes sur les parcours](../building-journeys/journey-faq.md)
* [Questions fréquentes sur les campagnes orchestrées](../orchestrated/orchestrated-campaigns-faq.md)
