---
solution: Journey Optimizer
product: journey optimizer
title: Rôles et responsabilités
description: Découvrez les différents rôles dans Adobe Journey Optimizer et leurs responsabilités.
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 14%

---


# Rôles et responsabilités

Adobe Journey Optimizer permet aux marques de proposer des expériences connectées, contextuelles et personnalisées dans l’ensemble du parcours client. Conçu dans une optique complète d’évolutivité, de vitesse et de flexibilité, Journey Optimizer associe trois principaux facteurs de valeur dans une application unifiée :

* **Informations sur le client en temps réel et engagement** optimisé par le profil client en temps réel d’Adobe
* **Orchestration omnicanal moderne** par le biais de canevas unifiés pour les parcours en temps réel et les campagnes par lots, ainsi qu’un concepteur de messages moderne
* **Prise de décision et personnalisation intelligentes** grâce à la gestion des décisions et aux fonctionnalités d’IA/ML

Journey Optimizer propose deux approches d’orchestration qui répondent à des besoins marketing différents :

* **Parcours** : idéal pour un engagement individuel en temps réel, où chaque client évolue à son propre rythme, en fonction du comportement ou des événements
* **Campagnes orchestrées** : idéal pour les campagnes par lots, de type « un à plusieurs », où les audiences progressent ensemble par le biais de workflows à plusieurs étapes selon un planning, idéal pour les promotions saisonnières, les lancements de produits et les communications basées sur les comptes

Cette expérience unifiée vous permet de mettre en œuvre des cas d’utilisation complets en un seul endroit, de la définition d’audiences et de la conception de parcours à la création de contenu personnalisé et à l’analyse des résultats. Cette documentation explique les rôles clés impliqués dans l’utilisation efficace de Journey Optimizer, leurs responsabilités et la manière de commencer.

**Remarque importante :** Adobe Journey Optimizer définit des rôles distincts avec des responsabilités spécifiques. Selon la structure de votre entreprise, une seule personne peut assumer plusieurs rôles ou tous les rôles.

## Guides de démarrage rapide basés sur les rôles

Pour simplifier la mise en œuvre, Adobe Journey Optimizer organise les tâches en rôles spécifiques en fonction de l’expertise. Chaque rôle se concentre sur les tâches essentielles requises pour offrir une expérience client transparente.

| Rôle | Responsabilités principales | Compétences principales | Tâches standard |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrateur ou administratrice** | Configuration de l’environnement et gestion des accès | Configuration du système, gestion des utilisateurs et utilisatrices, sécurité | Configurer des sandbox, gérer les autorisations utilisateur, configurer des canaux et des préréglages de message |
| **Ingénieur ou ingénieure de données** | Données de profil client et sources de données | Modélisation des données, schémas XDM, connecteurs source | Modélisez les données de profil et métier dans des schémas, configurez les connecteurs source et surveillez l’ingestion des données |
| **Développeur ou développeuse** | Implémentation technique et intégrations | SDK mobile/web, API, architecture orientée événement | Intégrer des SDK, implémenter des événements et créer des points d’entrée d’action personnalisés |
| **Spécialiste marketing** | Conception de parcours et expériences personnalisées | orchestration des parcours, création de contenu, ciblage des audiences | Concevoir des parcours clients, créer et personnaliser des messages, gérer des offres et des composants de décision, définir des audiences |

Chaque rôle aborde une phase spécifique de la mise en œuvre de Adobe Journey Optimizer et assure un processus de déploiement structuré et efficace.

## Ordre d’implémentation et dépendances des rôles

Une implémentation réussie de Journey Optimizer suit généralement cette séquence, qui reflète les dépendances entre les rôles :

1. **Administrateur ou administratrice** : configure l’environnement.\
   L’administrateur ou l’administratrice pose les bases en configurant les sandbox, en configurant les contrôles d’accès et en préparant les configurations de canal. Cela doit d’abord se produire pour permettre à d’autres équipes de travailler.
   * Configuration des sandbox de développement, d’évaluation et de production
   * Configurez les rôles, les autorisations et le contrôle d’accès au niveau de l’objet (OLAC)
   * Configurer des configurations de canal (e-mail, SMS, notification push, in-app, web, cartes de contenu)
   * Délégation de sous-domaines et configuration de pools d&#39;adresses IP
   * Configuration des listes de suppression et des politiques de consentement

2. **Ingénieur ou ingénieure de données** : crée la base des données.\
   Les ingénieurs de données créent l’infrastructure de données qui alimente la personnalisation, définissant la manière dont les données client circulent dans et à travers le système.
   * Créer des espaces de noms d’identité pour l’identification du client
   * Conception de schémas XDM (profil, événements d’expérience, relationnel)
   * Configurer des jeux de données et les activer pour le profil client en temps réel
   * Configuration de l&#39;ingestion des données (par lots et en flux continu)
   * Création d’attributs calculés pour des calculs complexes
   * Configuration d’événements et de sources de données pour parcours

3. **Développeur** : met en œuvre des intégrations techniques.\
   Les développeurs connectent les applications à Journey Optimizer en intégrant des SDK, en envoyant des événements et en créant des points d’entrée d’API. Ces implémentations permettent aux parcours de se déclencher et de s’exécuter.
   * Intégrer Mobile SDK (iOS/Android) à la configuration des notifications push
   * Implémentation de Web SDK pour les expériences web
   * Envoi d’événements depuis des applications pour déclencher des parcours
   * Créer des points d’entrée d’action personnalisés pour les intégrations système externes
   * Tester les implémentations à l’aide d’Adobe Experience Platform Assurance

4. **Professionnel du marketing** : conçoit et exécute les expériences client\
   Les marketeurs tirent parti de tout le travail fondamental pour créer des parcours, créer du contenu et optimiser les expériences client sur tous les canaux.
   * Créer des audiences à l’aide de la segmentation, du chargement CSV ou de la composition des audiences
   * Concevoir du contenu personnalisé avec l’assistant d’IA et des modèles
   * Création de parcours multicanaux avec des déclencheurs d’événement et d’audience
   * Tester avec les workflows d’approbation avant le lancement
   * Surveiller les performances et les optimiser en fonction des informations de rapports

**Remarque :** bien que cette séquence soit standard, certaines activités peuvent se produire en parallèle. Par exemple, les développeurs et développeuses peuvent travailler sur les intégrations d’applications pendant que les ingénieurs et ingénieures de données configurent les schémas.

## Prise en main par rôle

Chaque rôle commence par des tâches spécifiques adaptées à son objectif. L’accomplissement de ces étapes initiales garantit une intégration et une harmonisation plus fluides avec le processus de mise en œuvre global :

### Pour les professionnels du marketing {#for-marketers}

En tant que professionnel du marketing ou praticien/praticienne professionnel, vous concevez des parcours client pour offrir des expériences personnelles et contextuelles à tous les points de contact. Vous travaillerez dans une interface unifiée pour implémenter des cas d’utilisation complets du début à la fin.

**Fonctionnalités clés que vous utiliserez :**

* **Journey Orchestration** : créez un engagement client individuel en temps réel où chaque personne évolue à son propre rythme, déclenché par un comportement ou des événements sur plusieurs canaux
* **Orchestration des campagnes** : concevez et automatisez des campagnes par lots complexes et à plusieurs étapes à grande échelle à l’aide d’une zone de travail visuelle. Parfait pour les campagnes lancées par la marque comme les promotions saisonnières, les lancements de produits et les communications basées sur un compte. Utilisez la segmentation d’entités multiples pour créer des audiences précises en connectant les données client aux entités associées (comptes, achats, réservations).
* **Modern Message Designer** : concevez et personnalisez des e-mails et des messages mobiles à l’aide d’une interface glisser-déposer. Modifier les modèles prêts à l’emploi pour accélérer le délai de mise sur le marché
* **Gestion des décisions** : créez et gérez des offres, des règles d’éligibilité et d’autres composants dans une bibliothèque centralisée qui peut être incorporée dans les e-mails et les points de contact des clients
* **Gestion des ressources** : accédez à Adobe Experience Manager Assets Essentials entièrement intégré à Journey Optimizer pour une diffusion et un accès aux ressources rationalisés
* **Définition d’audience** : créez des audiences à la demande avec un affinement instantané à l’aide de requêtes relationnelles, avec une visibilité de pré-envoi pour un décompte d’audience précis
* **Services AI/ML** : utilisez l’optimisation de l’heure d’envoi et les scores d’engagement prédictifs pour cibler les clients à forte valeur ajoutée et réduire le risque d’attrition

**Commencez par :** utilisez des modèles de cas d’utilisation et des assistants pour créer et déployer facilement de nouveaux parcours client.

[Prise en main en tant qu’→ marketing](path/marketer.md)

### Pour les ingénieurs de données {#for-data-engineers}

En tant qu’architecte ou ingénieur de données, vous configurez et gérez les données de profil client et d’autres sources de données qui alimentent les expériences orchestrées par Journey Optimizer.

**Principales responsabilités :**

* **Données du profil client** : modélisez les données du profil client et les données commerciales dans des schémas pour créer une vue unifiée à 360 degrés du client
* **Modélisation des données relationnelles** : pour les campagnes orchestrées, concevez des schémas relationnels afin de permettre la segmentation d’entités multiples, en connectant les données client à des entités associées telles que des comptes, des achats, des abonnements et des réservations, pour une création d’audience flexible
* **Connecteurs Source** : configurez les connecteurs source pour ingérer les données provenant du Web, du CRM, des données hors ligne et d’autres sources dans Adobe Experience Platform
* **Résolution d’identités** : configurez des espaces de noms d’identité pour mettre à jour en continu les profils et déplacer les clients dans et hors des segments et des parcours en temps réel
* **Sources de données** : configurez les sources de données pour écouter en temps réel les signaux externes sur le parcours client
* **Gestion des profils** : activez des jeux de données pour le profil client en temps réel afin d’offrir des expériences personnalisées
* **Qualité des données** : surveillez l’ingestion des données pour vous assurer que tout se déroule correctement dans Journey Optimizer

**Commencer par :** modélisez votre premier schéma de profil client et configurez un connecteur source pour commencer à ingérer des données.

[Prise en main en tant qu’ingénieur de données →](path/data-engineer.md)

### Pour les administrateurs {#for-administrators}

En tant qu’administrateur ou administratrice, vous configurez l’environnement Journey Optimizer pour permettre à vos équipes de travailler efficacement et en toute sécurité.

**Principales responsabilités :**

* **Sandbox** : créez et gérez des sandbox pour partitionner les données et les parcours pour différents groupes d’utilisateurs (développement, test, production)
* **User Management** : configurez des groupes d’utilisateurs et des autorisations pour contrôler l’accès à différentes fonctionnalités
* **Configuration du canal** : configurez les canaux de diffusion et les préréglages de message pour garantir la cohérence de l’identité graphique des messages et des ressources diffusés via Journey Optimizer
* **Sécurité et gouvernance** : appliquez le contrôle d’accès au niveau de l’objet (OLAC), configurez des politiques de consentement et implémentez des politiques de gouvernance des données
* **Délivrabilité** : déléguez des sous-domaines, créez des groupes d’adresses IP et gérez les listes et listes autorisées de suppression
* **Configuration de Parcours** : définissez des éléments et des configurations de parcours pour vos équipes

**Commencez par :** Configurer des sandbox et des autorisations utilisateur, puis configurer vos premières configurations de canal et vos premiers préréglages de message.

[Prise en main en tant qu’administrateur →](path/administrator.md)

### Pour les développeurs {#for-developers}

Implémentez des intégrations techniques qui connectent Journey Optimizer à vos applications.

**Principales responsabilités :**

* Intégrer Adobe Experience Platform Mobile SDK (iOS/Android)
* Mise en œuvre de Web SDK pour les expériences web et les notifications push web
* Configuration des informations d’identification et des certificats des notifications push
* Envoi d’événements depuis des applications pour déclencher des parcours
* Créer des points d’entrée d’API que Journey Optimizer appelle via des actions personnalisées
* Implémentez des expériences basées sur du code pour les surfaces web, mobiles et autres
* Tester et déboguer des implémentations avec Adobe Experience Platform Assurance
* Utiliser les API Journey Optimizer pour l’accès programmatique

**Commencez par :** intégrez le Mobile ou le Web SDK, puis implémentez votre premier événement pour déclencher un parcours.

[Prise en main en tant que développeur →](path/developer.md)

## Cross-Role Collaboration

La réussite des implémentations de Journey Optimizer nécessite une collaboration entre tous les rôles :

* **Administrateurs** activez d’autres rôles en configurant des sandbox, des autorisations et des canaux.
* **Les ingénieurs de données** fournissent la base de données sur laquelle les développeurs et les spécialistes du marketing s’appuient.
* **Développeurs** implémentez les intégrations techniques que les marketeurs utilisent pour déclencher les parcours
* **Les spécialistes marketing** font part de leurs commentaires à toutes les équipes sur la qualité des données, les demandes de fonctionnalités et l’expérience utilisateur

**Bonne pratique :** organisez régulièrement des réunions transverses pour vous aligner sur les priorités, partager les progrès et résoudre les problèmes rencontrés par les différentes équipes.

## Vidéo pratique {#video}

Pour en savoir plus sur les principales fonctionnalités et les personas les plus importants de Journey Optimizer, regardez la vidéo de présentation. La vidéo présente l’interface d’utilisation et met en évidence les fonctionnalités clés en fonction des workflows spécifiques aux rôles.

>[!VIDEO](https://video.tv.adobe.com/v/3430314?captions=fre_fr&quality=12)

## Ressources supplémentaires

Pour des mises à jour et des formations plus approfondies, consultez les ressources suivantes :

**Formation et documentation :**

* [Tutoriels vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr){target="_blank"} - Tutoriels vidéo détaillés pour tous les rôles
* [Bibliothèque de cas d’utilisation de Parcours &#x200B;](../building-journeys/jo-use-cases.md) - Exemples pratiques et modèles d’implémentation
* [Fonctionnalités intelligentes et d’IA](ai-features.md) - Découvrez l’assistant d’IA, l’optimisation de l’heure d’envoi et la génération de contenu
* [&#x200B; Guide de l’interface utilisateur &#x200B;](user-interface.md) - Naviguez efficacement dans Journey Optimizer

**Restez à jour :**

* [&#x200B; Notes de mise à jour &#x200B;](../rn/release-notes.md) - Dernières fonctionnalités, améliorations et correctifs
* [Mises à jour de la documentation](../rn/documentation-updates.md) - Suivez les modifications récentes de la documentation
* [Notifications de produit](../rn/releases.md#staying-informed) - Découvrez comment vous abonner aux e-mails et aux alertes sur le produit pour les mises à jour de Journey Optimizer

**Communauté et assistance :**

* [Communauté Experience League &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"} - Connectez-vous à d’autres utilisateurs et experts
* [Forum produit](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"} - Posez des questions et partagez vos connaissances
