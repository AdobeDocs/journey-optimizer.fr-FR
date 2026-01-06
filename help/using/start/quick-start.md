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
source-git-commit: d3765f66beff13aaf77cd585c5da5f93c44fa1df
workflow-type: ht
source-wordcount: '1724'
ht-degree: 100%

---


# Rôles et responsabilités

Adobe Journey Optimizer (AJO) permet aux marques de proposer des expériences connectées, contextualisées et personnalisées tout au long du parcours client. Conçu dans une optique d’évolutivité, de vitesse et de flexibilité de bout en bout, Journey Optimizer combine trois principaux facteurs de valeur dans une application unifiée :

* **Informations sur les clientes et les clients et engagement en temps réel** basés sur le profil client en temps réel d’Adobe
* **Orchestration omnicanal moderne** par le biais de zones de travail unifiées pour les parcours en temps réel et les campagnes par lots, ainsi qu’un concepteur de messages moderne
* **Prise de décision et personnalisation intelligentes** grâce à la gestion des décisions et aux fonctionnalités d’IA/de ML

Journey Optimizer propose deux approches d’orchestration qui répondent à des besoins marketing différents :

* **Parcours** : idéal pour l’engagement individuel et en temps réel, où chaque client ou cliente évolue à son propre rythme, en fonction de son comportement ou d’événements.
* **Campagnes orchestrées** : idéal pour les campagnes par lots, de type « un à plusieurs », où les audiences progressent ensemble par le biais de workflows à plusieurs étapes selon un planning ; idéal pour les promotions saisonnières, les lancements de produits et les communications basées sur les comptes.

Cette expérience unifiée vous permet d’implémenter des cas d’utilisation complets en un seul endroit, de la définition d’audiences et de la conception de parcours à la création de contenu personnalisé et à l’analyse de résultats. Cette documentation explique les rôles clés impliqués dans l’utilisation efficace de Journey Optimizer, leurs responsabilités et la manière de commencer.

**Remarque importante :** Adobe Journey Optimizer définit des rôles distincts avec des responsabilités spécifiques. Selon la structure de votre entreprise, une seule personne peut assumer plusieurs rôles ou tous les rôles.

## Guides de démarrage rapide basés sur les rôles

Pour simplifier l’implémentation, Adobe Journey Optimizer organise les tâches en rôles spécifiques, en fonction de l’expertise. Chaque rôle se concentre sur les tâches essentielles requises pour offrir une expérience client transparente.

| Rôle | Responsabilités principales | Compétences principales | Tâches standard |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrateur ou administratrice** | Configuration de l’environnement et gestion des accès | Configuration du système, gestion des utilisateurs et utilisatrices, sécurité | Configurer des sandbox, gérer les autorisations des utilisateurs et des utilisatrices, configurer des canaux et les préréglages de messages |
| **Ingénieur ou ingénieure de données** | Données de profils clients et sources de données | Modélisation des données, schémas XDM, connecteurs source | Modélisez les données de profils et les données métier dans des schémas, configurez les connecteurs source et surveillez l’ingestion des données |
| **Développeur ou développeuse** | Implémentation technique et intégrations | SDK mobile/web, API, architecture basée sur des événements | Intégrer des SDK, implémenter des événements et créer des points d’entrée d’actions personnalisées |
| **Responsable marketing** | Conception de parcours et expériences personnalisées | Orchestration de parcours, création de contenu, ciblage d’audiences | Concevoir des parcours clients, créer et personnaliser des messages, gérer des offres et des composants de décision, définir des audiences |

Chaque rôle aborde une phase spécifique de l’implémentation d’Adobe Journey Optimizer et assure un processus de déploiement structuré et efficace.

## Ordre d’implémentation et dépendances des rôles

Une implémentation réussie de Journey Optimizer suit généralement cette séquence, qui reflète les dépendances entre les rôles :

1. **Administrateur ou administratrice** : configure l’environnement.\
   L’administrateur ou l’administratrice pose les bases en configurant les sandbox et les contrôles d’accès et en préparant les configurations des canaux. Ces tâches doivent être effectuées en premier pour permettre aux autres équipes de travailler.
   * Configurer des sandbox de développement, d’évaluation et de production
   * Configurer les rôles, les autorisations et le contrôle d’accès au niveau de l’objet (OLAC)
   * Configurer les configurations de canal (e-mail, SMS, notification push, in-app, web, cartes de contenu)
   * Déléguer des sous-domaines et configurer des groupes d’adresses IP
   * Configurer des listes de suppression et des politiques de consentement

2. **Ingénieur ou ingénieure de données** : crée la base des données.\
   Les ingénieurs et ingénieures de données créent l’infrastructure de données qui sert de base à la personnalisation et définissent la manière dont les données client circulent dans le système.
   * Créer des espaces de noms d’identités pour l’identification des clientes et des clients
   * Concevoir des schémas XDM (profils, événements d’expérience, relationnels)
   * Configurer des jeux de données et les activer pour une utilisation avec le profil client en temps réel
   * Configurer l’ingestion des données (par lots et en streaming)
   * Créer des attributs calculés pour les calculs complexes
   * Configurer des événements et des sources de données pour les parcours

3. **Développeur ou développeuse** : implémente les intégrations techniques.\
   Les développeurs et les développeuses connectent les applications à Journey Optimizer en intégrant des SDK, en envoyant des événements et en créant des points d’entrée d’API. Ces implémentations permettent aux parcours de se déclencher et de s’exécuter.
   * Intégrer le SDK mobile (iOS/Android) à la configuration des notifications push
   * Implémenter le SDK Web pour les expériences web
   * Envoyer des événements à partir d’applications pour déclencher des parcours
   * Créer des points d’entrée d’actions personnalisées pour les intégrations à des systèmes externes
   * Tester les implémentations à l’aide d’Adobe Experience Platform Assurance

4. **Responsable marketing** : conçoit et exécute les expériences client\
   Les responsables marketing tirent parti de tout le travail fondamental réalisé pour créer des parcours et du contenu et optimiser les expériences client sur tous les canaux.
   * Créer des audiences à l’aide de la segmentation, du chargement d’un fichier CSV ou de la composition d’audiences
   * Concevoir du contenu personnalisé avec l’assistant IA et des modèles
   * Créer des parcours multicanaux avec des déclencheurs d’événement et d’audience
   * Tester avec des workflows d’approbation avant le lancement
   * Surveiller les performances et les optimiser en fonction des informations de rapports

**Remarque :** bien que cette séquence soit standard, certaines activités peuvent se produire en parallèle. Par exemple, les développeurs et développeuses peuvent travailler sur les intégrations d’applications pendant que les ingénieurs et ingénieures de données configurent les schémas.

## Prise en main par rôle

Chaque rôle commence par des tâches spécifiques adaptées à son objectif. L’accomplissement de ces étapes initiales garantit une intégration et une harmonisation plus fluides avec le processus de mise en œuvre global :

### Pour les responsables marketing {#for-marketers}

En tant que responsable marketing ou qu’utilisateur ou utilisatrice professionnel, vous concevez des parcours client pour offrir des expériences personnelles et contextuelles à tous les points de contact. Vous travaillez dans une interface unifiée pour implémenter des cas d’utilisation complets du début à la fin.

**Les fonctionnalités clés que vous allez utiliser :**

* **Journey Orchestration** : créez un engagement client individuel et en temps réel où chaque personne évolue à son propre rythme, déclenché par un comportement ou des événements sur plusieurs canaux.
* **Orchestration de campagne** : concevez et automatisez des campagnes par lots complexes et à plusieurs étapes à grande échelle à l’aide d’une zone de travail visuelle. Parfait pour les campagnes lancées par une marque, comme des promotions saisonnières, des lancements de produits et des communications basées sur les comptes. Exploitez la segmentation d’entités multiples pour créer des audiences précises en connectant les données client à des entités associées (par exemple, comptes, achats, réservations).
* **Concepteur de messages moderne** : concevez et personnalisez des e-mails et des messages mobiles à l’aide d’une interface de type glisser-déposer. Modifier les modèles prêts à l’emploi pour accélérer le délai de mise sur le marché
* **Gestion des décisions** : créez et gérez des offres, des règles d’éligibilité et d’autres composants dans une bibliothèque centralisée qui peuvent être incorporés dans des e-mails et des points de contact avec la clientèle
* **Gestion des ressources** : accédez à Adobe Experience Manager Assets Essentials, entièrement intégré à Journey Optimizer pour un accès aux ressources et une diffusion des ressources rationalisés.
* **Définition d’audience** : créez des audiences à la demande avec un ajustement instantané à l’aide de requêtes relationnelles, avec de la visibilité avant envoi pour une évaluation précise de la taille des audiences.
* **Services d’IA/de ML** : utilisez l’optimisation de l’heure d’envoi et les scores d’engagement prédictifs pour cibler les clientes et les clients à forte valeur ajoutée et pour réduire le risque d’attrition.

**Commencez par :** utiliser des modèles de cas d’utilisation et des assistants pour créer et déployer facilement de nouveaux parcours client.

[Commencer en tant que responsable marketing →](path/marketer.md)

### Pour les ingénieurs et ingénieures de données {#for-data-engineers}

En tant qu’architecte ou ingénieur ou ingénieure de données, vous configurez et gérez les données de profil client et d’autres sources de données utilisées dans les expériences orchestrées par Journey Optimizer.

**Principales responsabilités :**

* **Données de profil client** : modélisez les données de profil client et les données commerciales dans des schémas pour créer une vue unifiée à 360 degrés du client ou de la cliente.
* **Modélisation des données relationnelles** : pour les campagnes orchestrées, concevez des schémas relationnels afin de permettre la segmentation d’entités multiples, en connectant les données client à des entités associées, telles que des comptes, des achats, des abonnements et des réservations, pour une création d’audience flexible.
* **Connecteurs source** : configurez les connecteurs source pour ingérer des données provenant du Web ou d’un CRM, des données hors ligne, ou d’autres sources dans Adobe Experience Platform.
* **Résolution d’identités** : configurez des espaces de noms d’identités pour mettre à jour en continu les profils et déplacer les clientes et les clients dans et hors des segments et des parcours en temps réel.
* **Sources de données** : configurez les sources de données pour écouter en temps réel les signaux externes sur le parcours client.
* **Gestion des profils** : activez les jeux de données pour une utilisation avec le profil client en temps réel afin d’offrir des expériences personnalisées.
* **Qualité des données** : surveillez l’ingestion des données pour vous assurer que tout se déroule correctement dans Journey Optimizer.

**Commencez par :** modéliser votre premier schéma de profil client et configurer un connecteur source pour commencer à ingérer des données.

[Commencer en tant qu’ingénieur ou ingénieure de données →](path/data-engineer.md)

### Pour les administrateurs et administratrices {#for-administrators}

En tant qu’administrateur ou administratrice, vous configurez l’environnement Journey Optimizer pour permettre à vos équipes de travailler efficacement et en toute sécurité.

**Principales responsabilités :**

* **Sandbox** : créez et gérez des sandbox pour partitionner les données et les parcours pour différents groupes d’utilisateurs et d’utilisatrices (développement, test, production).
* **Gestion des utilisateurs et des utilisatrices** : configurez des groupes d’utilisateurs et d’utilisatrices et des autorisations pour contrôler l’accès aux différentes fonctionnalités.
* **Configuration des canaux** : configurez les canaux de diffusion et les préréglages de messages pour garantir la cohérence de l’identité de marque dans les messages et les ressources diffusés via Journey Optimizer.
* **Sécurité et gouvernance** : appliquez le contrôle d’accès au niveau de l’objet (OLAC), configurez des politiques de consentement et implémentez des politiques de gouvernance des données.
* **Délivrabilité** : déléguez des sous-domaines, créez des groupes d’adresses IP et gérez les listes de suppression et les listes autorisées.
* **Configuration de parcours** : mettez en place des éléments et des configurations de parcours pour vos équipes.

**Commencez par :** configurer des sandbox et des autorisations utilisateur, puis définissez vos premières configurations de canal et vos premiers préréglages de messages.

[Commencer en tant qu’administrateur ou administratrice →](path/administrator.md)

### Pour les développeurs et développeuses {#for-developers}

Implémentez des intégrations techniques qui connectent Journey Optimizer à vos applications.

**Principales responsabilités :**

* Intégrer le SDK mobile Adobe Experience Platform (iOS/Android)
* Implémenter le SDK Web pour les expériences web et les notifications push web
* Configurer les informations d’identification et les certificats des notifications push
* Envoyer des événements à partir d’applications pour déclencher des parcours
* Créer des points d’entrée d’API que Journey Optimizer peut appeler via des actions personnalisées
* Implémenter des expériences basées sur du code pour les surfaces web, mobiles, ou autres
* Tester et déboguer des implémentations avec Adobe Experience Platform Assurance
* Utiliser les API Journey Optimizer pour un accès par programmation

**Commencez par** : intégrer le SDK mobile ou Web, puis implémenter votre premier événement pour déclencher un parcours.

[Commencer en tant que développeur ou développeuse →](path/developer.md)

## Collaboration entre les différents rôles

La réussite des implémentations de Journey Optimizer nécessite une collaboration entre tous les rôles. Chaque rôle fonctionne avec les autres pour offrir des expériences client fluides :

>[!BEGINTABS]

>[!TAB Administrateurs et administratrices]

**Les administrateurs et administratrices** autorisent toutes les équipes à travailler en gérant les accès et les configurations. Ils peuvent collaborer avec :

* **Ingénieurs et ingénieures de données** : octroient des autorisations pour la gestion des données, approuvent l’accès aux sandbox, coordonne les politiques de gouvernance.
* **Développeurs et développeuses** : fournissent des informations d’identification d’API, configurent des environnements de test et approuvent les configurations de canaux.
* **Responsables marketing** : attribuent des autorisations pour les parcours/campagnes, configurent des canaux et assistent les environnements de test.

>[!TAB Ingénieurs et ingénieures de données]

**Les ingénieurs et ingénieures de données** fournissent la base des données à tout le monde. Ils peuvent collaborer avec :

* **Administrateurs et administratrices** : demandent des autorisations pour la gestion des données, coordonnent les politiques de gouvernance et de conservation des données.
* **Développeurs et développeuses** : fournissent des schémas XDM et des structures d’événement, définissent des formats de payload d’événement, testent l’ingestion des données.
* **Responsables marketing** : créent des attributs calculés pour la personnalisation, créent des audiences et configurent des schémas relationnels

>[!TAB Développeurs et développeuses]

**Les développeurs et développeuses** implémentent des intégrations techniques sur lesquelles se basent les parcours. Ils peuvent collaborer avec :

* **Ingénieurs et ingénieures de données** : obtiennent des schémas XDM et des structures d’événement, s’alignent sur les exigences en matière de collecte de données, testent la diffusion des événements.
* **Administrateurs et administratrices** : indiquent les spécifications des API, demandent les autorisations et les informations d’identification, coordonnent la stratégie de test.
* **Responsables marketing** : identifient les déclencheurs d’événements, implémentent le suivi, assurent les tests de parcours et résolvent les problèmes.

>[!TAB Responsables marketing]

**Les responsables marketing** conçoivent des expériences client et envoient des commentaires. Ils peuvent collaborer avec :

* **Ingénieurs et ingénieures de données** : demandent des attributs calculés, coordonnent les exigences en matière d’audience, fournissent des retours sur la qualité des données.
* **Développeurs et développeuses** : s’alignent sur les déclencheurs d’événements, testent les implémentations, valident le suivi.
* **Administrateurs et administratrices** : demandent des configurations de canal, confirment l’accès aux fonctionnalités, coordonnent les habilitations.

>[!ENDTABS]

**Bonne pratique :** organisez régulièrement des réunions transverses pour harmoniser les priorités, partager vos progrès et résoudre les problèmes rencontrés par les différentes équipes.

## Vidéo pratique {#video}

Pour en savoir plus sur les principales fonctionnalités et les personas les plus importants de Journey Optimizer, regardez la vidéo de présentation. La vidéo présente l’interface d’utilisation et met en évidence les fonctionnalités clés en fonction des workflows spécifiques aux rôles.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Ressources supplémentaires

Pour des mises à jour et des formations plus approfondies, consultez les ressources suivantes :

>[!BEGINTABS]

>[!TAB Formation et documentation]

* [Tutoriels vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr){target="_blank"} - Tutoriels vidéo détaillés pour tous les rôles
* [Bibliothèque de cas d’utilisation de parcours](../building-journeys/jo-use-cases.md) - Exemples pratiques et modèles d’implémentation
* [Fonctionnalités intelligentes et fonctionnalités d’IA](ai-features.md) - Découvrez l’assistant IA, l’optimisation de l’heure d’envoi et la génération de contenu.
* [Guide de l’interface d’utilisation](user-interface.md) - Naviguez efficacement dans Journey Optimizer.

>[!TAB Restez à jour]

* [Notes de mise à jour](../rn/release-notes.md) - Dernières fonctionnalités, améliorations et correctifs
* [Mises à jour de la documentation](../rn/documentation-updates.md) - Suivez les modifications récentes de la documentation.
* [Notifications de produit](../rn/releases.md#staying-informed) - Découvrez comment vous abonner aux e-mails et aux alertes dans le produit pour les mises à jour de Journey Optimizer.

>[!TAB Communauté et assistance]

* [Communauté Experience League ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Communiquez avec d’autres utilisateurs, utilisatrices, experts et expertes.
* [Forum de produits](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Posez des questions et partagez vos connaissances.

>[!ENDTABS]
