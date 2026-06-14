---
solution: Journey Optimizer
product: journey optimizer
title: Packages et fonctionnalités Journey Optimizer
description: Découvrez comment Adobe Journey Optimizer est compilé et quelles fonctionnalités sont disponibles en fonction de votre offre de base, des modules complémentaires de canal et des modules complémentaires de fonctionnalités avancées.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: parcours optimizer, package, licence, campagnes, parcours, canaux, prise de décision, sortant, mobile, web, modulaire
hide: true
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 3%

---


# Packages et fonctionnalités Adobe Journey Optimizer {#ajo-packages-v2}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez le fonctionnement du package Adobe Journey Optimizer modulaire sur les offres de base, les modules complémentaires de canal et le module complémentaire Decisioning, afin que vous puissiez choisir la combinaison qui correspond à vos cas d’utilisation d’engagement et à votre budget.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] utilise un modèle d’emballage modulaire. Commencez par l’offre de base qui correspond à votre cas d’utilisation principal, puis ajoutez les canaux et les fonctionnalités avancées dont vous avez besoin.

>[!NOTE]
>
>La disponibilité des packages et des fonctionnalités incluses peut varier en fonction de votre accord, des modules complémentaires sélectionnés et de la disponibilité régionale. Contactez votre représentant Adobe pour obtenir des détails spécifiques à votre organisation.

## Étape 1 — Choisissez votre offre de base {#base-offers}

Trois offres de base sont disponibles. Choisissez celle qui correspond à la manière dont vous interagissez principalement avec les clients.

| Offre de base | Idéal pour | Comportement de base |
|-----------|---------|--------------|
| **Journey Optimizer - Campagnes** | Diffusion par lots planifiée par le marketeur | Orchestration planifiée basée sur les audiences. Workflows de campagne à une ou plusieurs étapes utilisant le magasin de données relationnel. |
| **Journey Optimizer - Parcours** | Engagement client en temps réel | Piloté par les événements, orchestration 1:1. Prend en charge le traitement des parcours par lots et par flux. |
| **Journey Optimizer - Campagnes et Parcours** | Clients ayant besoin des deux | Combine l’orchestration des campagnes basée sur les audiences et l’orchestration des parcours en temps réel. |

### Campagnes vs Parcours - quelle est la différence ? {#campaigns-vs-journeys}

| | Journey Optimizer - Campagnes | JOURNEY OPTIMIZER - PARCOURS | Journey Optimizer - Campagnes et Parcours |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| Orchestration par lots basée sur les audiences | ✓ | Limité aux cas d’utilisation parcours | ✓ |
| Orchestration basée sur les événements en temps réel | — | ✓ | ✓ |
| Messages transactionnels (e-mail, push, SMS) | ✓ | ✓ | ✓ |
| Modules complémentaires de canal disponibles | ✓ | ✓ | ✓ |
| Module complémentaire Prise de décision disponible | ✓ | ✓ | ✓ |

>[!NOTE]
>
>Les droits totaux de volume de données diffèrent : les clients **Campagnes** reçoivent 15 Ko par profil adressable ; **Parcours** et **Campagnes et Parcours** reçoivent 75 Ko par profil adressable.

## Étape 2 — Ajoutez les canaux dont vous avez besoin {#channel-addons}

Les canaux ne sont pas regroupés dans l’offre de base. Sélectionnez le module complémentaire de canal ou l’offre groupée de modules complémentaires qui correspond à votre stratégie d’engagement.

>[!BEGINTABS]

>[!TAB Diffusion sortante]

Touchez des audiences par le biais des canaux de messagerie sortants.

**Inclut :** e-mail, notifications push, courrier

**Cas d’utilisation standard :** e-mails promotionnels, alertes push transactionnelles, campagnes par e-mail physiques.

**Surfaces prises en charge :** boîte de réception, écran de verrouillage de l’appareil mobile/plateau de notification, adresse postale

Inclut les principes de délivrabilité pour la prise en charge du réchauffement des adresses IP sur les nouvelles instances. [En savoir plus sur la délivrabilité ](../reports/deliverability.md)

>[!TAB Mobile]

Impliquez les utilisateurs de l’application avec des expériences mobiles en session et persistantes.

**Inclut :** la messagerie in-app, les notifications push, les cartes de contenu, les canaux basés sur le code pour les surfaces mobiles

**Cas d’utilisation standard :** flux d’intégration, annonces de fonctionnalités, incitations à la fidélité, offres in-app en temps réel

**Surfaces prises en charge :** écrans d’applications mobiles, barre d’état de notification, emplacements de contenu persistants, surfaces d’applications personnalisées via SDK

>[!TAB Web]

Personnalisez des expériences web sans déployer de code.

**Inclut** canal web (éditeur visuel et non visuel), des canaux basés sur du code pour les surfaces web

**Cas d’utilisation standard :** bannières de page d’accueil, personnalisation de page de destination, tests A/B, personnalisation web découplée via l’API

**Surfaces prises en charge :** pages de navigateur, applications monopages (SPA), points d’entrée web découplés

>[!TAB Tous les canaux]

Le module complémentaire **Tous les canaux** offre une diffusion sortante + Mobile + Web dans un seul achat.

Idéal pour les organisations qui ont besoin d’une couverture omnicanal complète sur les surfaces web, des applications mobiles et sortantes.

>[!ENDTABS]

**WhatsApp** est disponible en tant que module complémentaire distinct pour les clients qui doivent envoyer des messages via WhatsApp Business. [Découvrez comment utiliser WhatsApp](../whatsapp/get-started-whatsapp.md)

## Étape 3 — Ajout de fonctionnalités avancées {#advanced-addons}

### Prise de décision {#decisioning-addon}

Le module complémentaire **Decisioning** vous permet de définir, de gérer et de diffuser la meilleure offre, la meilleure action ou la meilleure expérience pour chaque profil en temps réel, sur n’importe quel canal.

**Ce que cela déverrouille :**
- Sélection d&#39;offres en temps réel à l&#39;aide de règles d&#39;éligibilité, d&#39;une logique de classement et de contraintes
- Modèles de classement optimisés par l’IA pour optimiser automatiquement les performances des offres
- Politiques de prise de décision utilisables dans les parcours, les campagnes et les expériences basées sur du code

**Disponible le :** les trois offres de base, sous réserve de votre contrat de licence. [Découvrez comment utiliser la prise de décision](../experience-decisioning/gs-experience-decisioning.md) | [En savoir plus sur les modèles d’IA](../offers/ranking/ai-models.md)

## Comparer en un coup d’œil {#comparison-matrix}

| Fonctionnalité | Journey Optimizer - Campagnes | JOURNEY OPTIMIZER - PARCOURS | Journey Optimizer - Campagnes et Parcours | Module complémentaire obligatoire |
|-----------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|
| Messages transactionnels (e-mail, push, SMS) | ✓ | ✓ | ✓ | — |
| Campagnes par lots | ✓ | — | ✓ | — |
| Campagnes orchestrées _(e-mail, SMS, notification push, publipostage direct uniquement)_ | ✓ | — | ✓ | — |
| Parcours automatisés | — | ✓ | ✓ | — |
| Déclencheurs d’événement en temps réel | — | ✓ | ✓ | — |
| Email | ✓ | ✓ | ✓ | Diffusion sortante |
| Notifications push | ✓ | ✓ | ✓ | Diffusion sortante |
| Canal Courrier | ✓ | ✓ | ✓ | Diffusion sortante |
| SMS/MMS | ✓ | ✓ | ✓ | Diffusion sortante |
| Messagerie in-app | ✓ | ✓ | ✓ | Mobile |
| Cartes de contenu | ✓ | ✓ | ✓ | Mobile |
| Canal web | ✓ | ✓ | ✓ | Web |
| Expériences basées sur du code | ✓ | ✓ | ✓ | Mobile ou Web |
| WhatsApp | ✓ | ✓ | ✓ | WhatsApp |
| Prise de décision | Dépend de la licence | Dépend de la licence | Dépend de la licence | Prise de décision |
| Classement optimisé par l&#39;IA | Dépend de la licence | Dépend de la licence | Dépend de la licence | Prise de décision |

## Questions fréquentes {#faq}

+++**Chaque offre de base inclut-elle chaque canal ?**

Non. [!DNL Adobe Journey Optimizer] utilise un modèle modulaire : l’offre de base détermine votre capacité d’orchestration (campagnes, Parcours ou les deux) et les modules complémentaires de canal déterminent les surfaces de messagerie avec lesquelles vous pouvez interagir. Vous choisissez la combinaison qui correspond à votre cas d’utilisation et à votre budget.

+++

+++**Quelle est la différence entre les campagnes et les Parcours ?**

Les **campagnes** sont basées sur l’audience et planifiées par le spécialiste marketing. Vous définissez une audience, créez un message et planifiez ou déclenchez-le sous la forme d’un envoi par lots. Elles sont particulièrement adaptées aux campagnes promotionnelles, aux newsletters et aux workflows d’audience à plusieurs étapes.

Les **Parcours** sont pilotés par les événements et en temps réel. Ils réagissent au comportement individuel des clients au fur et à mesure et orchestrent des expériences 1:1 entre les points de contact. Elles sont particulièrement adaptées aux flux d’intégration, aux séquences après achat et aux messages déclenchés en temps réel.

**Campagnes et Parcours** vous donne les deux fonctionnalités dans une seule licence.

+++

+++**Quels canaux sont pris en charge dans les campagnes orchestrées ?**

Les campagnes orchestrées (workflows d’audience à plusieurs étapes utilisant la fonctionnalité d’orchestration des campagnes) prennent uniquement en charge les **e-mails, SMS, notifications push et publipostage direct**. Les canaux web, in-app, basés sur du code et de carte de contenu ne sont pas pris en charge dans les workflows de campagne orchestrés.

+++

+++**Decisioning est-il inclus dans chaque configuration ?**

Non. Decisioning est un module complémentaire de fonctionnalité avancé distinct et n&#39;est inclus par défaut dans aucune offre de base. Contactez votre représentant Adobe pour ajouter Decisioning à votre configuration.

+++

+++**J’ai entendu parler de Select, Prime ou Ultimate. S&#39;agit-il toujours du modèle d&#39;emballage actuel?**

[!DNL Adobe Journey Optimizer] est désormais proposé par le biais d’un modèle de package modulaire conçu autour d’offres de base (campagnes, Parcours, campagnes et Parcours) et de modules complémentaires. Si vous êtes déjà client ou cliente utilisant la terminologie Select, Prime ou Ultimate et que vous avez des questions sur vos droits actuels, contactez votre représentant ou représentante Adobe.

+++
