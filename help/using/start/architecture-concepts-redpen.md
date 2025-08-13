---
solution: Journey Optimizer
product: journey optimizer
title: Architecture d’AJO
description: Architecture et relation avec AEP
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: f94067ffb421bfd095ed3fcb3001af0e5dc44ab3
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Architecture

## Vue d’ensemble : comment Adobe Journey Optimizer s’intègre

Adobe Journey Optimizer (AJO) et Adobe Experience Platform (AEP) fonctionnent ensemble pour permettre une personnalisation pilotée par les données à grande échelle. Cet écosystème fonctionne comme un flux continu où les données sont collectées, analysées et appliquées pour créer des parcours clients personnalisés.

![](../assets/do-not-localize/get-started-big-picture.png)


### Concepts de base : Adobe Experience Platform (AEP)

Adobe Experience Platform sert de colonne vertébrale, ce qui permet aux marques de centraliser les données client et de les activer pour offrir des expériences personnalisées.

- **Data Platform** : AEP fonctionne comme le hub central pour la collecte, la gestion et la structuration des données client afin d’assurer la cohérence entre les systèmes.
- **Ingestion de données (sources)** : les marques importent des données de divers systèmes, tels que les plateformes CRM, les sites web, les applications mobiles et le stockage dans le cloud, à l’aide de connecteurs préconfigurés. Par exemple, un connecteur Source ingère les données d’achat d’une plateforme d’e-commerce.
- **Real-time Customer Profile** : cette fonctionnalité crée des profils unifiés en fusionnant des données provenant de plusieurs sources. Par exemple, un profil combine des interactions avec les e-mails et des achats en magasin pour fournir une vue complète d’un client.
- **Couche de gouvernance** : cette couche régit l’accès aux données, la conformité en matière de confidentialité et la sécurité. Cela garantit que les marques utilisent en toute sécurité les données client tout en respectant les réglementations.

### Moteur d’orchestration : Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer applique les données et les informations d’AEP pour offrir des expériences client intelligentes et personnalisées sur différents canaux.

- **Compréhension du client** : les profils client en temps réel permettent la segmentation en audiences pour la messagerie ciblée. Par exemple, une audience comprend des acheteurs fréquents identifiés par l’historique des achats.
- **Contenu et offres** :
   - **Gestion de contenu** : cette fonctionnalité fournit des outils pour créer, gérer et personnaliser du contenu sur plusieurs canaux. Par exemple, vous pouvez créer un fragment de contenu réutilisable pour un en-tête d’e-mail promotionnel.
   - **Gestion des décisions** : ce système utilise la logique en temps réel pour sélectionner la meilleure offre ou le meilleur message pour chaque individu. Par exemple, un client éligible peut recevoir une offre de remise basée sur son historique de navigation.
- **Gestion des Parcours et des campagnes** : cette fonctionnalité automatise les séquences d’interactions (Parcours) ou planifie des messages ciblés uniques (campagnes). Par exemple, un Parcours déclenche des e-mails de relance après une consultation de produit.
- **Diffusion (Connexions)**:
   - **Canaux** : cette fonctionnalité diffuse des messages et des offres par le biais de plateformes de communication telles que les e-mails, les SMS, les notifications push et le courrier.
   - **Destinations** : cette fonctionnalité exporte les données de profil et d’audience vers des systèmes externes à des fins d’activation ou d’analyse. Par exemple, les données d’audience sont envoyées à une plateforme de médias sociaux pour le ciblage publicitaire.
- **Mesure et analyse** : cette fonctionnalité effectue le suivi de l’engagement des clients et des performances des campagnes avec des rapports. Ces informations permettent une amélioration continue.

## Cycle d’optimisation continue

Cet écosystème fonctionne comme un cycle d’optimisation continu. Les données favorisent la compréhension des clients, ce qui éclaire le contenu personnalisé et les décisions. Elles sont orchestrées dans des parcours, diffusées sur l’ensemble des canaux, mesurées pour en évaluer l’efficacité et affinées au fil du temps.

![](../assets/do-not-localize/get-started-flow.png)

## Architecture détaillée

![Architecture Adobe Journey Optimizer](assets/ajo-architecture.png)


## Confidentialité et sécurité

Les pratiques de confidentialité et de sécurité de Adobe Experience Cloud s’appliquent à Adobe Journey Optimizer. Ces mesures garantissent la conformité aux réglementations de confidentialité, ce qui permet aux marques de proposer des expériences personnalisées tout en préservant la confiance des clients.
