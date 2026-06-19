---
solution: Journey Optimizer
product: journey optimizer
title: Guide de projet d’intégration | Adobe Journey Optimizer
description: Planifiez et gérez un projet d’intégration Adobe Journey Optimizer pour les rôles d’administrateur, de données, de développeur et de marketeur.
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: parcours optimizer, intégration, projet d’intégration, déploiement, plan d’implémentation, administrateur, csm, partenaire d’implémentation, liste de contrôle échelonnée
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# Guide de projet d’intégration {#onboarding-hub}

>[!BEGINSHADEBOX]

**Sur cette page :** planifiez et coordonnez un déploiement Adobe Journey Optimizer complet avec une liste de contrôle échelonnée qui couvre les rôles d’administrateur, d’ingénieur de données, de développeur et de marketeur.

>[!ENDSHADEBOX]

Cette page est destinée aux **administrateurs système et partenaires d’implémentation** pour la coordination d’un déploiement Journey Optimizer complet. Il fournit une liste de contrôle échelonnée couvrant tous les rôles, avec des liens vers des guides détaillés spécifiques aux rôles.

>[!NOTE]
>
>Si vous êtes une personne qui débute avec un rôle spécifique, accédez à [Prise en main de Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) à la place.

## Phase 1 — Configuration de l’environnement (administrateur) {#phase-1}

Effectuez d’abord ces tâches fondamentales afin que les autres rôles puissent commencer leur travail :

* [ ] Configurer des sandbox (développement, évaluation, production)
* [ ] Configurer les rôles utilisateur et les autorisations dans Adobe Admin Console
* [ ] Configurer des profils de produit et un contrôle d’accès au niveau de l’objet
* [ ] Déléguer des sous-domaines et configurer des groupes d’adresses IP
* [ ] Configurer des configurations de canal (e-mail, SMS, notification push, web, in-app, courrier)
* [ ] Configurer des listes de suppression et des politiques de consentement

➡️ Voir tous les détails : [Prise en main pour les administrateurs](path/administrator.md)

## Phase 2 — Base de données (ingénieur de données) {#phase-2}

Créez la couche de données qui alimente les profils, les audiences et les déclencheurs de parcours :

* [ ] Définir des espaces de noms d’identité
* [ ] Créer des schémas XDM (profil, événements d’expérience, relationnel)
* [ ] Configurer et activer des jeux de données pour le profil client en temps réel
* [ ] Configurer l’ingestion des données (par lots et par flux)
* [ ] Créer des attributs calculés
* [ ] Configurer des événements de parcours et des sources de données

➡️ Voir tous les détails : [Prise en main pour les ingénieurs de données](path/data-engineer.md)

## Phase 3 — Intégrations techniques (développeur) {#phase-3}

Connectez vos applications afin que les parcours puissent s’exécuter sur des données en temps réel :

* [ ] Intégrer Mobile SDK (iOS/Android) avec la configuration push
* [ ] Implémenter Web SDK pour les expériences web et les notifications push web
* [ ] Implémenter l’envoi d’événements à partir d’applications
* [ ] Créer des points d’entrée d’action personnalisés pour les intégrations système externes
* [ ] la validation à l’aide d’Adobe Experience Platform Assurance

➡️ Voir tous les détails : [Prise en main pour les développeurs](path/developer.md)

## Phase 4 — Premières expériences (spécialiste marketing) {#phase-4}

Jetez les bases en lançant vos premiers parcours et campagnes :

* [ ] Créer la première audience (définition de segment ou chargement CSV)
* [ ] Créer un parcours de test avec une action d’e-mail
* [ ] Configurer des modèles et des fragments de contenu
* [ ] Publier et surveiller une campagne
* [ ] Vérifier les rapports dynamiques

➡️ Voir tous les détails : [Prise en main pour les professionnels du marketing](path/marketer.md)

## Liste de contrôle d’intégration (imprimable) {#checklist}

| Phase | Propriétaire | Statut |
|-------|-------|--------|
| Configuration de l’environnement | Administrateur | |
| Base des données | Ingénieur de données | |
| Intégrations techniques | Développeur | |
| Premières expériences | Spécialiste marketing | |

## Ressources connexes {#related-resources}

* [Rôles et responsabilités](quick-start.md) — Comment les quatre rôles fonctionnent ensemble et l’ordre de mise en œuvre recommandé.
* [Tutoriels Journey Optimizer &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — Vidéos détaillées et procédures pas à pas pour chaque rôle.
* [Prise en main de la gestion des données](../data/gs-data.md) — Comment les données sont-elles ingérées, unifiées et activées ?
