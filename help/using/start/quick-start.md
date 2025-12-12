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
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# Rôles et responsabilités

Adobe Journey Optimizer permet aux marques de proposer des parcours clients connectés et contextualisés tout au long du cycle de vie du client. Il permet aux équipes de personnaliser les interactions à grande échelle et d’aligner les attentes des clientes et clients sur les objectifs de l’entreprise. Cette documentation explique les rôles clés impliqués dans l’utilisation efficace de Journey Optimizer, leurs responsabilités et la manière de commencer.

**Remarque importante :** Adobe Journey Optimizer définit des rôles distincts avec des responsabilités spécifiques. Selon la structure de votre entreprise, une seule personne peut assumer plusieurs rôles ou tous les rôles.

## Guides de démarrage rapide basés sur les rôles

Pour simplifier la mise en œuvre, Adobe Journey Optimizer organise les tâches en rôles spécifiques en fonction de l’expertise. Chaque rôle se concentre sur les tâches essentielles requises pour offrir une expérience client transparente.

| Rôle | Responsabilités principales | Compétences principales | Tâches standard |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrateur ou administratrice** | Configuration de l’environnement et gestion des accès | Configuration du système, gestion des utilisateurs et utilisatrices, sécurité | Configuration des sandbox, gestion des autorisations et configuration des configurations de canal |
| **Ingénieur ou ingénieure de données** | Base et architecture des données | Modélisation des données, schémas XDM, qualité des données | Créer des schémas et des jeux de données, configurer l’ingestion des données, gérer le cycle de vie des données |
| **Développeur ou développeuse** | Implémentation technique et intégrations | SDK mobile/web, API, architecture orientée événement | Intégrer des SDK, implémenter des événements et créer des points d’entrée d’action personnalisés |
| **Spécialiste marketing** | Conception et exécution de l’expérience client | conception de parcours, création de contenu, analyse de données | Création de parcours, création de contenu personnalisé et optimisation des campagnes |

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

Concentrez-vous sur la création d’expériences client personnalisées sur tous les canaux.

**Fonctionnalités clés que vous utiliserez :**

* Créez des audiences et des segments à l’aide de plusieurs méthodes (définitions de segment, chargement CSV, composition de l’audience)
* Concevoir du contenu avec l’assistant AI pour la génération de texte et d’images
* Créer des parcours client multicanaux à l’aide du concepteur glisser-déposer
* Tirez parti de l’optimisation de l’heure d’envoi et de la gestion des conflits pour optimiser l’engagement
* Test du contenu et utilisation des workflows de validation avant publication
* Surveiller les performances à l’aide de tableaux de bord de rapports intégrés

**Commencez par :** créer un parcours de bienvenue simple ou une campagne de récupération de panier abandonné à l’aide de modèles préconfigurés.

[Prise en main en tant qu’→ marketing](path/marketer.md)

### Pour les ingénieurs de données {#for-data-engineers}

Établissez la base de données qui alimente les expériences personnalisées.

**Principales responsabilités :**

* Création d’espaces de noms d’identité et configuration de la résolution d’identité
* Concevoir des schémas XDM pour les données de profil et d’événement (standard et relationnelles)
* Configurer des jeux de données et les activer pour le profil client en temps réel
* Configuration des connecteurs source pour l’ingestion de données par lots et par flux
* Créer des attributs calculés pour simplifier la segmentation
* Configurer des événements et des sources de données pour l’exécution du parcours
* Gérer la qualité, la gouvernance et le cycle de vie des données

**Commencer par :** configurer des espaces de noms d’identité et créer votre premier schéma de profil avec les groupes de champs obligatoires.

[Prise en main en tant qu’ingénieur de données →](path/data-engineer.md)

### Pour les administrateurs {#for-administrators}

Configurez et gérez l’environnement Journey Optimizer pour votre organisation.

**Principales responsabilités :**

* Créer et gérer des sandbox pour le développement, les tests et la production
* Configuration des rôles et des autorisations à l’aide de rôles prêts à l’emploi ou personnalisés
* Application du contrôle d’accès au niveau de l’objet (OLAC) pour sécuriser les ressources
* Configurez les configurations de canal pour les e-mails, SMS, notifications push, in-app, web et cartes de contenu
* Déléguer des sous-domaines et créer des groupes d’adresses IP pour la délivrabilité des e-mails
* Gestion des listes de suppression et des listes autorisées
* Configurer les politiques de consentement et la gouvernance des données (avec Healthcare/Privacy Shield)

**Commencez par :** configurer des sandbox, configurer des rôles et des autorisations de base, puis travailler avec votre équipe sur les configurations de canal.

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

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

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
* **Notifications de produit** - Activez les alertes dans votre profil [Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} pour recevoir des notifications sur les nouvelles versions, les fenêtres de maintenance et les annonces importantes. Cliquez sur l’icône de votre profil > Préférences > Notifications à configurer.

**Communauté et assistance :**

* [Communauté Experience League &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Connectez-vous à d’autres utilisateurs et experts
* [Forum produit](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Posez des questions et partagez vos connaissances
