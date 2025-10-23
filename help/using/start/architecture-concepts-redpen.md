---
solution: Journey Optimizer
product: journey optimizer
title: Architecture d’AJO
description: Architecture et relation avec AEP
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '463'
ht-degree: 100%

---

# Architecture

## Vue d’ensemble : articulation d’Adobe Journey Optimizer

Adobe Journey Optimizer (AJO) et Adobe Experience Platform (AEP) fonctionnent ensemble pour permettre une personnalisation pilotée par les données à grande échelle. Cet écosystème fonctionne comme un flux continu où les données sont collectées, analysées et appliquées pour créer des parcours client personnalisés.

![](../assets/do-not-localize/get-started-big-picture.png)


### Clé de voûte : Adobe Experience Platform (AEP)

Adobe Experience Platform sert de colonne vertébrale, ce qui permet aux marques de centraliser les données client et de les activer pour offrir des expériences personnalisées.

- **Plateforme de données** : AEP fonctionne comme le hub central pour la collecte, la gestion et la structuration des données client afin d’assurer la cohérence entre les systèmes.
- **Ingestion de données (sources)** : les marques importent des données de divers systèmes, tels que les plateformes CRM, les sites web, les applications mobiles et le stockage dans le cloud, à l’aide de connecteurs préconfigurés. Par exemple, un connecteur Source ingère les données d’achat d’une plateforme d’e-commerce.
- **Profil client en temps réel** : cette fonctionnalité crée des profils unifiés en fusionnant des données provenant de plusieurs sources. Par exemple, un profil peut associer des interactions par e-mail et des achats en magasin afin d’offrir une vue complète du client ou de la cliente.
- **Couche de gouvernance** : cette couche régit l’accès aux données, la conformité en matière de confidentialité et la sécurité. Cela garantit que les marques utilisent en toute sécurité les données client tout en respectant les réglementations.

### Moteur d’orchestration : Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer applique les données et les informations d’AEP pour offrir des expériences client intelligentes et personnalisées sur différents canaux.

- **Compréhension de la clientèle** : les profils client en temps réel permettent la segmentation en audiences pour la messagerie ciblée. Par exemple, une audience comprend des acheteurs et acheteuses fréquents identifiés par l’historique des achats.
- **Contenu et offres** :
   - **Gestion de contenu** : cette fonctionnalité fournit des outils pour créer, gérer et personnaliser du contenu sur plusieurs canaux. Par exemple, vous pouvez créer un fragment de contenu réutilisable pour un en-tête d’e-mail promotionnel.
   - **Gestion des décisions** : ce système utilise la logique en temps réel pour sélectionner la meilleure offre ou le meilleur message pour chaque individu. Par exemple, un client ou une cliente éligible peut recevoir une offre de remise basée sur son historique de navigation.
- **Gestion des parcours et des campagnes** : cette fonctionnalité automatise les séquences d’interactions (Parcours) ou planifie des messages ciblés uniques (Campagnes). Par exemple, un parcours déclenche des e-mails de relance après une consultation de produit.
- **Diffusion (Connexions)** :
   - **Canaux** : cette fonctionnalité diffuse des messages et des offres par le biais de plateformes de communication telles que les e-mails, les SMS, les notifications push et le courrier.
   - **Destinations** : cette fonctionnalité exporte les données de profil et d’audience vers des systèmes externes à des fins d’activation ou d’analyse. Par exemple, les données d’audience sont envoyées à une plateforme de médias sociaux pour le ciblage publicitaire.
- **Mesure et analyse** : cette fonctionnalité effectue le suivi de l’engagement des clientes et clients et des performances des campagnes avec des rapports. Ces informations permettent une amélioration continue.

## Cycle d’optimisation continu

Cet écosystème fonctionne comme un cycle d’optimisation continu. Les données approfondissent la compréhension des clientes et des clients, ce qui guide la personnalisation des contenus et oriente les décisions. Elles sont orchestrées dans des parcours, diffusées sur l’ensemble des canaux, mesurées pour en évaluer l’efficacité et affinées au fil du temps.

![](../assets/do-not-localize/get-started-flow.png)

## Architecture détaillée

![Architecture d’Adobe Journey Optimizer](assets/ajo-architecture.png)


## Confidentialité et sécurité

Les pratiques de confidentialité et de sécurité d’Adobe Experience Cloud s’appliquent à Adobe Journey Optimizer. Ces mesures garantissent la conformité aux réglementations de confidentialité, ce qui permet aux marques de proposer des expériences personnalisées tout en préservant la confiance de leur clientèle.
