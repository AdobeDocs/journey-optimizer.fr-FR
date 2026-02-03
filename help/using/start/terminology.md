---
solution: Journey Optimizer
product: journey optimizer
title: Terminologie clé
description: Termes et concepts essentiels dans Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: ht
source-wordcount: '751'
ht-degree: 100%

---

# Terminologie clé {#key-terminology}

Ce guide de référence définit les termes essentiels que vous rencontrerez lorsque vous utiliserez Adobe Journey Optimizer. La compréhension de ces concepts vous permet de naviguer sur la plateforme en toute confiance et de collaborer efficacement avec votre équipe.

>[!TIP]
>
>Pour des explications détaillées des fonctionnalités et des workflows, reportez-vous aux sections de documentation spécifiques référencées tout au long de ce guide.

## Termes relatifs à la plateforme principale {#core-terms}

| Terme | Définition |
|------|------------|
| **Adobe Journey Optimizer** | Application permettant de créer et de diffuser des messages personnalisés aux clientes et clients sur plusieurs canaux (e-mail, SMS, notifications push, web). Elle vous permet de créer des parcours clients qui répondent aux actions des clientes et des clients en temps réel. |
| **Adobe Experience Platform** | Base d’Adobe Journey Optimizer qui collecte et organise toutes les données client en un seul endroit. Elle crée des profils clients unifiés que Journey Optimizer utilise pour la personnalisation. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=fr){target="_blank"} |
| **Profil client en temps réel** | Vue unifiée en temps réel de chaque cliente et client qui combine des données issues de plusieurs canaux, notamment des données en ligne, hors ligne, CRM et tierces. Chaque profil est mis à jour de manière dynamique à mesure que les clientes et clients interagissent avec votre marque. [En savoir plus](../audience/get-started-profiles.md) |
| **Sandbox** | Espace de travail distinct pour tester et expérimenter sans affecter les communications actuellement diffusées à la clientèle. Adobe Journey Optimizer fournit plusieurs sandbox pour les environnements de développement, de test et de production. [En savoir plus](../administration/sandboxes.md) |

## Termes relatifs aux parcours et aux campagnes {#journey-campaign-terms}

| Terme | Définition |
|------|------------|
| **Parcours** | Série d’étapes reliées entre elles qui guident les clientes et les clients à travers des expériences liées à votre marque au fil du temps. Chaque étape se produit en fonction des actions des clientes et clients ou des déclencheurs temporels, ce qui permet des interactions séquentielles et personnalisées. [En savoir plus](../building-journeys/journey.md) |
| **Campagne** | Communication unique ou ensemble de communications envoyés à une audience spécifique. Contrairement aux parcours qui se déploient au fur et à mesure, les campagnes diffusent les messages selon un planning ou un déclencheur, soit immédiatement, soit à un moment planifié. [En savoir plus](../campaigns/get-started-with-campaigns.md) |
| **Événement** | Action ou occurrence qui déclenchent ou font avancer un parcours. Les événements peuvent être des actions des clientes et clients (achat, abandon de panier) ou des événements système (date/heure, modification des données). [En savoir plus](../event/about-events.md) |
| **Canal** | Méthode utilisée pour communiquer avec les clientes et clients : e-mail, SMS, notifications push, messages in-app, web ou courrier. Chaque canal nécessite une configuration spécifique. [En savoir plus](../configuration/get-started-configuration.md) |

## Termes relatifs à la clientèle et à l’audience {#customer-audience-terms}

| Terme | Définition |
|------|------------|
| **Audience** | Groupe de clientes et clients qui partagent des caractéristiques ou des comportements communs, tels que « clientes et clients ayant effectué un achat au cours des 30 derniers jours » ou « membres du programme de fidélité ». Les audiences sont utilisées pour cibler des segments clients spécifiques. [En savoir plus](../audience/about-audiences.md) |
| **Qualification d’audience** | Processus qui se produit lorsqu’un client ou une cliente rejoint ou quitte une audience. Journey Optimizer peut déclencher des actions lorsqu’une personne rejoint ou quitte une audience, assurant ainsi des communications opportunes et pertinentes. [En savoir plus](../building-journeys/audience-qualification-events.md) |
| **Audience engageable** | Nombre de profils clients que vous pouvez contacter activement via Adobe Journey Optimizer en fonction de votre contrat de licence. Cela fait généralement référence aux profils engagés au cours des 12 derniers mois. |
| **Profil de test** | Profils fictifs utilisés pour tester et prévisualiser des messages avant de les envoyer à des clientes et clients réels. Les profils de test permettent de vérifier la personnalisation, le contenu et la logique du parcours. [En savoir plus](../audience/creating-test-profiles.md) |

## Termes relatifs au contenu et à la personnalisation {#content-terms}

| Terme | Définition |
|------|------------|
| **Personnalisation** | Processus de personnalisation du contenu en fonction des clientes et clients individuels à l’aide de leurs données de profil, de leurs préférences et de leurs comportements. Par exemple, l’insertion du nom d’un client ou d’une cliente, ou l’affichage de recommandations de produits en fonction de l’historique de navigation. [En savoir plus](../personalization/personalize.md) |
| **Modèle de contenu** | Conception de message réutilisable pouvant être utilisée dans plusieurs campagnes et parcours pour maintenir la cohérence de la marque et accélérer la création de contenu. [En savoir plus](../content-management/content-templates.md) |
| **Fragment** | Bloc de contenu réutilisable (par exemple, en-tête, pied de page ou bannière promotionnelle) pouvant être utilisé sur plusieurs messages pour garantir la cohérence et permettre des mises à jour centralisées. [En savoir plus](../content-management/fragments.md) |
| **Page de destination** | Page web autonome sur laquelle les clients et clients peuvent s’inscrire ou se désinscrire des communications, s’abonner à des services ou fournir des informations au moyen de formulaires en ligne. [En savoir plus](../landing-pages/get-started-lp.md) |

## Termes relatifs aux offres et aux décisions {#decision-terms}

| Terme | Définition |
|------|------------|
| **Gestion des décisions** | Fonctionnalité qui sélectionne automatiquement le meilleur contenu ou la meilleure offre pour chaque client ou cliente en fonction des données de profil en temps réel, du contexte et des règles métier. [En savoir plus](../offers/get-started/starting-offer-decisioning.md) |
| **Offre** | Message marketing, remise ou promotion pouvant être présentés aux clientes et clients. Les offres incluent des règles d’éligibilité qui déterminent les clientes et clients qui peuvent les recevoir. [En savoir plus](../offers/offer-library/creating-personalized-offers.md) |
| **Politique de décision** | Ensemble de règles et de stratégies qui déterminent l’offre à présenter à quelle personne et à quel moment, en fonction de contraintes telles que les règles d’éligibilité, de priorité et de limitation. [En savoir plus](../experience-decisioning/create-decision.md) |

## Termes relatifs aux données et à la configuration {#data-config-terms}

| Terme | Définition |
|------|------------|
| **Schéma** | Structure qui définit l’organisation des données dans Adobe Experience Platform, notamment les noms de champ, les types de données et les relations. Les schémas garantissent la cohérence des données entre les systèmes. [En savoir plus](../data/get-started-schemas.md) |
| **Jeu de données** | Collection de données (généralement un tableau) qui suit un schéma spécifique. Les jeux de données stockent les données client, les événements d’interaction et d’autres informations utilisées pour la personnalisation. [En savoir plus](../data/get-started-datasets.md) |

>[!NOTE]
>
>Pour obtenir un glossaire complet des termes d’Adobe Experience Platform, reportez-vous au glossaire [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=fr){target="_blank"}.

## Rubriques connexes {#related-topics}

* [Comprendre le fonctionnement de Journey Optimizer](understanding-ajo.md)
* [Commencer avec l’interface utilisateur](user-interface.md)
* [Choisir votre rôle et votre parcours de formation](quick-start.md)

