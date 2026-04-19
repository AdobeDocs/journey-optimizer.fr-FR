---
solution: Journey Optimizer
product: journey optimizer
title: Présentation de Journey Optimizer
description: Découvrez comment Adobe Journey Optimizer fonctionne avec Adobe Experience Platform pour offrir des expériences clients personnalisées.
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: parcours optimizer, fonctionnement, architecture, experience platform, domaines fonctionnels
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
source-git-commit: 8d7d97857eb65359bee6165d43427e92a2ce4fc5
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 74%

---

# Présentation de Journey Optimizer {#understanding-ajo}

Cette page explique comment Adobe Experience Platform et Journey Optimizer fonctionnent ensemble, en couvrant le cycle continu données-expérience, les domaines fonctionnels clés, les détails de l’architecture et les points d’intégration.

Adobe Journey Optimizer et Adobe Experience Platform fonctionnent ensemble pour permettre une personnalisation pilotée par les données à grande échelle. Cette page explique le fonctionnement de ces systèmes et la manière dont leurs domaines fonctionnels clés se combinent pour offrir des expériences clients exceptionnelles. [En savoir plus sur les fonctionnalités clés](get-started.md) | [Explorer la terminologie clé](terminology.md)

## Fonctionnement de Journey Optimizer {#how-it-works}

En l’absence d’une base de données unifiée, les marques sont contraintes de s’appuyer sur plusieurs outils spécifiques aux canaux, ce qui rend difficile le maintien d’une vue cohérente de chaque client ou cliente ou l’action sur son comportement en temps réel. Journey Optimizer résout ce problème en s’appuyant sur Adobe Experience Platform pour connecter les données client, la création de contenu et l’orchestration des parcours dans un système unique et continu. Il en résulte des expériences de marque significatives qui favorisent la fidélité du client et la valeur tout au long de la vie.

Adobe Journey Optimizer fonctionne comme un flux continu où les données sont collectées, analysées et appliquées pour créer des parcours clients personnalisés.

![Diagramme présentant Adobe Experience Platform comme couche de données fondamentale, avec Journey Optimizer reposant sur Real-Time CDP, Customer Journey Analytics et Adobe Mix Modeler, qui partagent tous des services principaux tels que le profil client en temps réel, la gouvernance des données et la résolution d’identité.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform : les bases {#aep-foundation}

Adobe Experience Platform sert de colonne vertébrale, ce qui permet aux marques de centraliser les données client et de les activer pour offrir des expériences personnalisées.

* **Plateforme de données** : hub central pour la collecte, la gestion et la structuration des données client afin d’assurer la cohérence entre les systèmes. [En savoir plus sur les schémas et les jeux de données](../data/get-started-schemas.md)
* **Ingestion de données (sources)** : importe des données de plateformes CRM, de sites web, d’applications mobiles et d’espace de stockage dans le cloud, à l’aide de connecteurs préconfigurés. [Explorer les sources de données](get-started-sources.md)
* **Profil client en temps réel** : crée des profils unifiés en fusionnant des données issues de plusieurs sources (interactions par e-mail, achats en magasin, comportement web). [Découvrir les profils](../audience/get-started-profiles.md)
* **Couche de gouvernance** : régit l’accès aux données, la conformité en matière de confidentialité et la sécurité tout en respectant les réglementations. [Consulter la documentation sur la confidentialité](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer : moteur d’orchestration {#ajo-orchestration}

Adobe Journey Optimizer applique les données et les informations d’Adobe Experience Platform pour offrir des expériences clients intelligentes et personnalisées :

* **Compréhension de la clientèle** : les profils clients en temps réel permettent la segmentation en audiences pour la messagerie ciblée. [Créer des audiences](../audience/about-audiences.md)
* **Contenu et offres** - Un concepteur visuel intégré, des modèles réutilisables et une bibliothèque de ressources centralisée permettent aux équipes de créer et de personnaliser des messages pour n’importe quel canal, sans quitter la plateforme. La personnalisation dynamique adapte le contenu en fonction des attributs, du comportement et du contexte du client. La logique de prise de décision en temps réel sélectionne ensuite la meilleure offre pour chaque individu. [Conception de contenu](../../rp_landing_pages/content-management-landing-page.md) | [Gestion des ressources](../integrations/assets.md) | [Gestion des offres](../offers/get-started/starting-offer-decisioning.md)
* **Gestion des parcours et des campagnes** : automatise les séquences d’interactions (parcours) ou planifie des messages ciblés uniques (campagnes). [Créer des parcours ](../building-journeys/journey-gs.md) | [Créer des campagnes](../campaigns/get-started-with-campaigns.md)
* **Diffusion (connexions)** : diffuse les messages par le biais de canaux (e-mail, SMS, notifications push et courrier) ; exporte les données vers des systèmes externes. [Configurer des canaux](../configuration/get-started-configuration.md)
* **Mesures et analyses** : effectue le suivi de l’engagement de la clientèle et des performances des campagnes avec des rapports pour une amélioration continue. [Afficher les rapports](../reports/campaign-global-report-cja.md)

### Le cycle d’optimisation continue {#optimization-cycle}

Cet écosystème fonctionne comme un cycle d’optimisation continu. Les données approfondissent la compréhension des clientes et des clients, ce qui guide la personnalisation des contenus et oriente les décisions. Elles sont orchestrées dans des parcours, diffusées sur l’ensemble des canaux, mesurées pour en évaluer l’efficacité et affinées au fil du temps.

![Diagramme illustrant le cycle d’optimisation continue dans Journey Optimizer : l’ingestion de données alimente les profils clients, qui éclairent les décisions de contenu et d’offre, sont orchestrées dans des parcours, diffusées sur plusieurs canaux, mesurées en termes de performances et affinées au fil du temps.](../assets/do-not-localize/get-started-flow.png)

## Principaux domaines fonctionnels {#functional-areas}

Journey Optimizer comprend plusieurs zones fonctionnelles clés qui opèrent de manière parfaitement intégrée :

| Zone fonctionnelle | Rôle | Activités clés |
|-----------------|---------|----------------|
| **Gestion des données** | Organiser les données client | Définir des schémas, créer des jeux de données, importer des données de divers systèmes. [En savoir plus](../data/get-started-schemas.md) |
| **Gestion de la clientèle** | Comprendre qui est la clientèle | Créer des profils unifiés, résoudre des identités et créer des audiences. [En savoir plus](../audience/get-started-profiles.md) |
| **Gestion de contenu** | Créer des messages personnalisés | Concevoir des e-mails, gérer des ressources, créer des modèles et des fragments, personnaliser le contenu. [En savoir plus](../../rp_landing_pages/content-management-landing-page.md) |
| **Gestion des décisions** | Sélectionner l’offre la plus adaptée en temps réel | Gérer la bibliothèque des offres, définir des règles, appliquer des contraintes, établir une logique de classement. [En savoir plus](../offers/get-started/starting-offer-decisioning.md) |
| **Gestion des parcours** | Concevoir des expériences clients automatisées | Créer des parcours avec le concepteur visuel, définir des déclencheurs, ajouter des conditions et des étapes d’attente. [En savoir plus](../building-journeys/journey-gs.md) |
| **Connexions** | Connecter les sources de données et les canaux | Configurer les connecteurs sources, configurer les canaux, se connecter aux plateformes externes. [En savoir plus](../configuration/get-started-configuration.md) |
| **Administration et confidentialité** | Contrôler la configuration et la conformité | Gérer les utilisateurs et les utilisatrices, configurer les sandbox, configurer les canaux, gérer les demandes d’accès à des informations personnelles. [En savoir plus](../administration/permissions.md) |

### Comment ces domaines fonctionnent ensemble {#working-together}

Ces domaines fonctionnels fonctionnent selon un cycle continu :

1. **Ingestion de données** : les données sont acheminées vers Adobe Experience Platform et sont structurées par la gestion des données.
2. **Compréhension de la clientèle** : les profils clients en temps réel unifient les données ; la gestion de la clientèle crée des audiences.
3. **Stratégie de contenu et d’offre** : la gestion de contenu crée des messages ; la gestion des décisions définit la logique d’offre.
4. **Orchestration** : la gestion des parcours mappe les interactions sur l’ensemble des canaux, en s’appuyant sur les données clients, le contenu et les décisions.
5. **Diffusion** : les connexions facilitent la diffusion des messages via les canaux ou le partage de données avec des systèmes externes.
6. **Mesure** : les données de performance fournissent des informations qui permettent d’affiner les audiences, le contenu, les décisions et les parcours.
7. **Gouvernance** : les contrôles d’administration et de confidentialité garantissent la conformité à tous les niveaux.

## Détails de l’architecture {#architecture-details}

Pour les équipes techniques, voici le diagramme d’architecture détaillé montrant comment Journey Optimizer s’intègre à Adobe Experience Platform. [Parcourez l’interface](user-interface.md) pour voir comment fonctionnent ces composants dans la pratique.

![Architecture d’Adobe Journey Optimizer](assets/ajo-architecture.png)

Quatre applications sont nativement intégrées à Experience Platform : Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics et Adobe Mix Modeler. Journey Optimizer fonctionne de manière transparente avec ces applications, mais peut également être utilisé de manière indépendante. Pour plus d’informations sur la mise en œuvre, voir [Mécanismes de sécurisation et limitations](guardrails.md).

### Points d’intégration {#integration-points}

Journey Optimizer s’intègre à Adobe Experience Platform à plusieurs niveaux :

* **Couche de données** : elle partage le même profil client en temps réel, le même graphique d’identité et les mêmes jeux de données.
* **Couche de service** : elle utilise les services de gouvernance, de confidentialité et de requête d’Adobe Experience Platform.
* **Couche d’application** : elle permet l’orchestration de parcours, la gestion des décisions et la gestion de contenu en s’appuyant sur Adobe Experience Platform.

En savoir plus sur les [plans directeurs Adobe Journey Optimizer](https://experienceleague.adobe.com/fr/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Confidentialité et sécurité {#privacy-security}

Les pratiques de confidentialité et de sécurité d’Adobe Experience Cloud s’appliquent à Adobe Journey Optimizer. Ces mesures garantissent la conformité aux réglementations en matière de confidentialité (comme le RGPD), ce qui permet de proposer des expériences personnalisées tout en préservant la confiance de la clientèle. [En savoir plus sur la confidentialité dans Journey Optimizer](../privacy/get-started-privacy.md)
