---
solution: Journey Optimizer
product: journey optimizer
title: Rôles et responsabilités d’AJO
description: Découvrez les différents rôles impliqués dans Adobe Journey Optimizer et leurs responsabilités
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d2cdafef6f2d69ea85d9d042c859a8b1e7654d7d
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---


# Rôles et responsabilités d’AJO

Adobe Journey Optimizer (AJO) permet aux marques de proposer des parcours clients connectés et contextualisés tout au long du cycle de vie du client. Il permet aux équipes de personnaliser les interactions à grande échelle et d’aligner les attentes des clients sur les objectifs commerciaux. Cette documentation explique les rôles clés d’une utilisation efficace de Journey Optimizer, leurs responsabilités et la manière de commencer.

**Remarque importante :** Adobe Journey Optimizer définit des rôles distincts avec des responsabilités spécifiques. Une seule personne peut assumer plusieurs rôles ou tous les rôles, selon la structure de votre entreprise.

## Guides de démarrage rapide basés sur les rôles

Pour simplifier la mise en œuvre, AJO organise les tâches en rôles spécifiques en fonction de l’expertise. Chaque rôle se concentre sur les tâches essentielles requises pour offrir une expérience client transparente.

| Rôle | Responsabilités en matière de Principal | Compétences clés | Tâches standard |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrateur** | Configuration du système et gestion des autorisations | Configuration du système, gestion des utilisateurs, sécurité | Configuration des sandbox, gestion des utilisateurs, configuration des canaux |
| **Ingénieur de données** | Configurer la structure et les flux de données | Modélisation des données, conception de schémas, intégration d’API | Configurer des schémas, gérer des jeux de données et configurer des sources de données |
| **Développeur** | Intégrations et personnalisations techniques | Développement mobile, implémentation d’API, codage | Intégrer des applications mobiles, implémenter des API, créer des actions personnalisées |
| **Professionnel du marketing** | Conception et exécution de parcours client | Stratégie marketing, création de contenu, conception de parcours | Création de campagnes, conception de parcours et analyse de rapports |

Chaque rôle aborde une phase spécifique de la mise en œuvre d’AJO et assure un processus de déploiement structuré et efficace.

## Ordre d’implémentation et dépendances des rôles

Une implémentation Journey Optimizer réussie suit généralement cette séquence, qui reflète les dépendances entre les rôles :

1. **Administrateur** : configure l’environnement.\
   L’administrateur pose les bases techniques du système et assure un accès et une configuration appropriés à tous les utilisateurs.
   * Configuration des sandbox et des autorisations
   * Configurer l’accès utilisateur
   * Configuration des canaux de messagerie et des paramètres techniques

2. **Ingénieur de données** : crée la base de données\
   Les ingénieurs de données définissent la structure et le flux de données, qui sont essentiels pour les expériences personnalisées.
   * Conception et implémentation de schémas
   * Configurer des espaces de noms d’identité
   * Configurer l’ingestion des données
   * Créer des profils de test

3. **Développeur** : gère les intégrations techniques.\
   Les développeurs permettent à AJO d’interagir avec des applications mobiles, des sites web et des systèmes externes en implémentant des intégrations techniques. Les notifications push, par exemple, reposent sur des configurations dirigées par le développeur.
   * Intégrer des applications mobiles pour les notifications push
   * Implémentation de SDK web
   * Développement d’intégrations personnalisées à l’aide d’API
   * Création d’actions personnalisées pour les systèmes tiers

4. **Professionnel du marketing** : crée et lance des parcours\
   Les professionnels du marketing se servent des bases jetées par d’autres rôles pour concevoir et déployer des expériences client. Ils se concentrent sur la segmentation de l’audience, le contenu personnalisé et l’optimisation du parcours.
   * Concevoir des segments d’audience
   * Création de contenu personnalisé
   * Création et test de parcours
   * Analyse des performances et optimisation

**Remarque :** bien que cette séquence soit typique, certaines activités peuvent se produire en parallèle. Par exemple, les développeurs peuvent travailler sur les intégrations d’applications pendant que les ingénieurs de données configurent les schémas.

## Prise en main par rôle

Chaque rôle commence par des tâches spécifiques adaptées à son objectif. L’accomplissement de ces étapes initiales garantit une intégration et un alignement plus fluides avec le processus de mise en œuvre global :

1. **Pour les spécialistes marketing** : concentrez-vous sur la création de parcours, la conception de messages et l’exécution de campagnes.\
   Exemple : commencez par créer une campagne par e-mail de bienvenue pour les nouveaux clients.

2. **Pour les ingénieurs de données** : établir la base de données, configurer des schémas et intégrer des sources de données.\
   Exemple : configurez un schéma pour effectuer le suivi de l’historique des achats des clients pour les recommandations personnalisées.

3. **Pour les administrateurs** : configurer des environnements, gérer des autorisations et configurer des canaux de messagerie.\
   Exemple : configuration d’environnements sandbox pour tester différentes stratégies de messagerie.

4. **Pour les développeurs** : intégrez des applications mobiles, implémentez des API et créez des intégrations personnalisées.\
   Exemple : utilisez l’API AJO pour déclencher des notifications push en fonction des actions des clients dans votre application mobile.

Cliquez sur votre rôle ci-dessous pour accéder à des conseils spécifiques adaptés à vos responsabilités :

* [Prise en main en tant que marketeur](path/marketer.md)
* [Prise en main en tant qu’ingénieur de données](path/data-engineer.md)
* [Prise en main en tant qu’administrateur](path/administrator.md)

## Vidéo pratique {#video}

Pour en savoir plus sur les principales fonctionnalités et personnalités de Journey Optimizer, regardez la vidéo d’introduction. La vidéo décrit l’interface utilisateur et met en évidence les fonctionnalités clés en fonction des workflows spécifiques aux rôles.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Ressources supplémentaires

Pour des mises à jour et un apprentissage plus approfondis, consultez les ressources suivantes :
* [Notes de mise à jour](https://experienceleague.adobe.com/docs/journey-optimizer/using/rn/release-notes.html)
* [Tutoriels vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr)