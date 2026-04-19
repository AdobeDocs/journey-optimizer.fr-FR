---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer
description: Découvrez les fonctionnalités clés et les cas pratiques d’Adobe Journey Optimizer
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: parcours optimizer, en quoi consiste ajo, adobe parcours optimizer, prise en main, omnicanal, personnalisation, parcours client
exl-id: 956178c0-9985-4ff8-a29e-17dd367ce4d4
source-git-commit: 8d7d97857eb65359bee6165d43427e92a2ce4fc5
workflow-type: tm+mt
source-wordcount: '1467'
ht-degree: 23%

---

# Prise en main de Journey Optimizer {#cjm-gs}

Cette page présente Adobe Journey Optimizer : son fonctionnement, ses utilisateurs, ses principales fonctionnalités et sa compatibilité avec l’architecture de Adobe Experience Platform. Il s’agit du point de départ recommandé pour les nouveaux utilisateurs.

## Qu’est-ce que [!DNL Adobe Journey Optimizer] ?{#about-cjm}

[!DNL Adobe Journey Optimizer] est une application d’entreprise permettant de créer et de diffuser des expériences client connectées, contextuelles et personnalisées sur l’ensemble des canaux et des points de contact. Il est créé de manière native sur [!DNL Adobe Experience Platform] et utilise un profil client en temps réel unifié, un framework ouvert API-First, une fonction Offer Decisioning centralisée et des fonctionnalités d&#39;IA/ML. Journey Optimizer permet aux marques d’orchestrer à la fois des campagnes marketing planifiées et des communications déclenchées par un événement en temps réel, à partir d’une seule application et à grande échelle. Le résultat est des expériences de marque significatives qui augmentent la fidélité du client et la valeur à vie.

Ce guide s’applique aux professionnels du marketing, aux équipes opérationnelles et aux administrateurs qui découvrent Journey Optimizer.

➡️ [Découvrir Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction.html?lang=fr){target="_blank"} (vidéo)


<!--
 Use [!DNL Adobe Journey Optimizer] to build multi-step customer journeys that initiate a sequence of interactions, offers, and messages across channels in real time. This approach ensures customers are engaged at the optimal moments based on their actions and relevant business signals. Learn how to build journeys in [this section](../building-journeys/journey-gs.md).

You can also create audience-based campaigns to send messages.
-->


## Cas d’utilisation {#use-cases}

Ces exemples illustrent la façon dont les fonctionnalités de Journey Optimizer fonctionnent ensemble dans différents rôles, secteurs et canaux.

| Cas d’utilisation | Rôle | Fonctionnalité principale |
|----------|------|----------------|
| Récupération d&#39;expédition retardée | Spécialiste marketing | [Profil unifié + exclusion d’audience](../audience/get-started-profiles.md) |
| Engagement en magasin en temps réel | Spécialiste marketing | [Déclenchement de limite géographique + notification push](../push/get-started-push.md) |
| Récupération après abandon de panier | Spécialiste marketing | parcours à plusieurs étapes déclenché par un événement[](../building-journeys/journey-gs.md) |
| Série de bienvenue sur le service de streaming | Spécialiste marketing | parcours de bienvenue déclenché par un événement[](../building-journeys/journey-gs.md) |
| Rappel de la réservation avec les directions | Spécialiste marketing | [Diffusion planifiée + tenant compte de l’emplacement](../campaigns/get-started-with-campaigns.md) |
| Notification proactive de panne de service | Opérations | [Sélection automatisée à grande échelle](../audience/about-audiences.md) |
| Campagne promotionnelle optimisée par l’IA | Spécialiste marketing | [Génération de contenu + expérimentation par l’IA](ai-features.md) |
| Alertes de maintenance via l’application mobile | Opérations | [Orchestration non marketing](../building-journeys/journey-gs.md) |

+++**Récupération différée des expéditions (spécialiste marketing)**

Une boutique de vêtements envoie généralement des enquêtes après achat à tous les clients qui ont acheté des produits la semaine dernière. En raison des intempéries, quelques envois ont été retardés. En identifiant les clientes et clients qui n’ont pas reçu leurs achats, la boutique de vêtements peut les exclure de l’envoi de l’enquête de satisfaction client programmée et envoyer à la place un e-mail personnalisé s’excusant du retard et proposant un code de remise avec des recommandations de produits basées sur leurs achats précédents.

[Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)

+++

+++**Engagement en magasin en temps réel (marketeur)**

Le même retailer peut interagir avec un client fidèle qui se rend sur le parking du magasin en temps réel en lui envoyant une notification push à propos d&#39;un pull à nouveau en stock à la taille du client.

[Commencer avec les notifications push](../push/get-started-push.md)

+++

+++**Récupération après abandon de panier (marketeur)**

Lorsqu’un client ajoute des articles à un panier en ligne, mais quitte le panier sans effectuer l’achat, Journey Optimizer détecte l’événement en temps réel et lance automatiquement un parcours de récupération. Le client reçoit un e-mail personnalisé lui rappelant les articles laissés. S’ils ne cliquent pas dans les 24 heures, une notification push de suivi est envoyée, personnalisée en fonction de leur historique de navigation et de leur statut de fidélité.

[Création de votre premier parcours](../building-journeys/journey-gs.md)

+++

+++**Série de bienvenue sur le service de streaming (marketeur)**

Lorsqu’un client s’abonne à un service de streaming, Journey Optimizer détecte l’événement d’inscription et lance immédiatement un parcours de bienvenue en plusieurs étapes. Le client reçoit un e-mail de bienvenue l’encourageant à ouvrir l’application pour la première fois. Si aucune activité de connexion n’est détectée dans les 48 heures, une notification push de suivi est envoyée avec des recommandations de contenu personnalisées basées sur leurs intérêts déclarés lors de l’inscription, transformant ainsi un abonné passif en un utilisateur actif et engagé dès le premier jour.

[Création de votre premier parcours](../building-journeys/journey-gs.md)

+++

+++**Rappel de la réservation avec les indications (Spécialiste marketing)**

Une marque d&#39;hôtellerie envoie à chaque client un rappel opportun une heure avant sa réservation. La notification inclut le nom du client, l’heure de la réservation et les indications géographiques du lieu de la visite, automatiquement rassemblés à partir du profil client et des données de réservation, sans intervention manuelle de l’équipe marketing.

[Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)

+++

+++**Notification proactive d’interruption de service (équipe d’exploitation)**

En cas d’interruption de service, Journey Optimizer identifie automatiquement les clients concernés en fonction des données de leur compte et des schémas d’utilisation. Ces clients reçoivent une notification proactive reconnaissant le problème et décrivant les étapes suivantes pour transformer une expérience potentiellement négative en un moment de transparence et de confiance, fourni à grande échelle.

[Création de votre premier parcours](../building-journeys/journey-gs.md)

+++

+++**Campagne promotionnelle optimisée par l’IA (marketeur)**

Une marque de vente au détail planifiant le lancement d’un produit utilise l’assistant d’IA de Journey Optimizer pour générer plusieurs variations d’objet et de corps en quelques minutes, en s’appuyant sur une invite en langage naturel et sur les directives de marque téléchargées. L’expérimentation de contenu intégrée identifie automatiquement la variante la plus performante parmi un échantillon d’audience initial. Le message gagnant est ensuite déployé auprès des destinataires restants, ce qui optimise l’engagement sans effort supplémentaire de création de copies.

[Explorer l’IA et les fonctionnalités intelligentes](ai-features.md) | [En savoir plus sur l’expérimentation de contenu](../content-management/experiment-accelerator-gs.md)

+++

+++**Alertes de maintenance via l’application mobile (équipe d’exploitation)**

Les personnes autres que les marketeurs comme les équipes opérationnelles et le service clientèle peuvent utiliser [!DNL Adobe Journey Optimizer] pour gérer les notifications opérationnelles ou surveiller les processus d’intégration. Par exemple, un parc d’attraction où les visiteurs téléchargent une application mobile dans le cadre de leur expérience : le personnel de maintenance peut utiliser Journey Optimizer pour informer les visiteurs du parc des itinéraires actuellement fermés en raison de travaux de maintenance.

[Création de votre premier parcours](../building-journeys/journey-gs.md)

+++

## Fonctionnalités principales {#key-capabilities}

[!DNL Adobe Journey Optimizer] est une application agile et évolutive permettant de créer et de diffuser des expériences clients personnalisées, connectées et opportunes
sur une application, un appareil ou un canal.

![Diagramme présentant trois domaines de fonctionnalités principaux de Journey Optimizer : informations sur le client et engagement en temps réel, orchestration et exécution omnicanal moderne et prise de décision et Personalization intelligentes, le tout reposant sur Adobe Experience Platform.](assets/ajo-capabilities.png)

Les fonctionnalités principales sont les suivantes :

### Informations sur le client et engagement en temps réel

Un profil intégré fusionne les données actives de toutes les sources entre les points de contact des clients, y compris les données comportementales, transactionnelles, financières et opérationnelles afin d’optimiser les expériences personnelles et contextuelles des clients à leur époque. [Découvrez les profils et les audiences](../audience/get-started-profiles.md)

### Exécution et orchestration omnicanal modernes

Zone de travail unique sur laquelle harmoniser et optimiser le parcours client pour 1:1 l’engagement client et la sensibilisation marketing, afin d’aider les marques à proposer une plus grande valeur ajoutée tout au long du cycle de vie du client. Les parcours client conçus dans [!DNL Adobe Journey Optimizer] peuvent être dynamiques et basés sur des événements afin d&#39;aider les marques à réagir aux signaux en temps réel et à associer ces interactions à des campagnes planifiées afin de pouvoir prendre les bonnes décisions concernant les communications à envoyer à un client, le moment et les canaux. Les outils de création de contenu intégrés, notamment le concepteur visuel de type glisser-déposer, les modèles réutilisables, les fragments de contenu et un éditeur de personnalisation, permettent aux équipes de créer, de personnaliser et de gérer des messages pour chaque canal directement au sein du même workflow. [Créer votre premier parcours ](../building-journeys/journey-gs.md) | [Concevoir votre contenu](../../rp_landing_pages/content-management-landing-page.md)

### Prise de décision et Personalization intelligentes

Les marques peuvent appliquer une prise de décision centralisée et intégrer l’intelligence artificielle et le machine learning pour configurer des informations prédictives tout au long de l’expérience client, ce qui facilite l’automatisation des décisions et l’optimisation de l’expérience à grande échelle. Decisioning alimente les offres centralisées sur tous les canaux à l’échelle via [!DNL Adobe Journey Optimizer]. [Explorer Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) | [Découvrir les fonctionnalités d’IA](ai-features.md)


## Disponibilité et licences {#availability}

Cette documentation couvre la version actuelle de Journey Optimizer et s’applique aux utilisateurs B2C et B2B edition, sauf indication contraire. Les composants et fonctionnalités disponibles dans votre environnement dépendent de vos [autorisations](../administration/permissions.md) et de votre [package de licences](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Pour toute question, contactez votre responsable du succès client Adobe ou votre représentant ou représentante Adobe.

Les lignes directrices et procédures générales d&#39;Adobe Experience Cloud sur la protection des données personnelles s&#39;appliquent à [!DNL Journey Optimizer]. [En savoir plus sur la confidentialité d&#39;Adobe Experience Cloud](https://www.adobe.com/fr/privacy/experience-cloud.html){target="_blank"}.


## Architecture {#architecture}

Découvrez l’architecture de base d’[!DNL Adobe Journey Optimizer], les points d’intégration et la relation entre [!DNL Journey Optimizer] et [!DNL Experience Platform], dans le diagramme ci-dessous.

Adobe Experience Platform est une base de données puissante, flexible, ouverte et centralisée qui collecte, normalise, régit, applique les informations d’IA et unifie les données afin d’offrir des expériences client numériques réfléchies et pertinentes.

![Diagramme présentant Adobe Experience Platform comme couche de données de base, avec quatre applications créées en mode natif sur la couche : Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics et Adobe Mix Modeler. Les services partagés tels que le profil client en temps réel, la gouvernance des données et la résolution d’identité sous-tendent les quatre applications ](assets/ajo-aep-architecture-diagram.png){width="70%" zoomable="yes"}.

Quatre applications sont prise en charge en mode natif sur Experience Platform : Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics et Adobe Mix Modeler.

Les fonctionnalités et services principaux de Journey Optimizer fonctionnent à partir des composants fondamentaux d’Adobe Experience Platform, qui inclut le profil client en temps réel. Bien que Journey Optimizer fonctionne de manière transparente et soit interopérable avec Real-Time CDP et Customer Journey Analytics, il peut également fonctionner indépendamment en tant qu’application autonome.

![Diagramme présentant l’architecture interne de Journey Optimizer et ses points d’intégration aux services Adobe Experience Platform, notamment l’ingestion de données, le profil client en temps réel, le moteur de prise de décision et la diffusion de canal sortant par e-mail, notification push, SMS et web.](assets/ajo-architecture-diagram.png){width="70%" zoomable="yes"}


### Plans directeur d’Adobe Journey Optimizer

Les plans directeurs d’expérience digitale fournissent des diagrammes d’architecture du système et des flux de données pour permettre de mieux comprendre la façon dont Adobe Experience Platform et les applications sont intégrées et mises en œuvre. Les plans directeurs fournissent une représentation visuelle des flux de contenu et de données entre les systèmes et les composants, de la séquence des opérations et des dépendances afin de contribuer à la conception et à l’architecture des cas d’utilisation d’Adobe Experience Platform et des applications.

Voir [Plans directeurs d’Adobe Journey Optimizer](https://experienceleague.adobe.com/fr/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.


>[!MORELIKETHIS]
>
>* [Étapes clés pour commencer](quick-start.md) — Guides de démarrage rapide basés sur les rôles pour les administrateurs, les spécialistes du marketing et les ingénieurs de données.
>* [Prise en main de la gestion des données](../data/gs-data.md) — Découvrez comment les données sont ingérées, unifiées et activées dans Journey Optimizer.
>* [Concevoir des parcours et envoyer des messages](../building-journeys/journey-gs.md) — Créez votre premier parcours client et configurez les actions de canal.
>* [Rapports dynamiques](../reports/live-report.md) — Surveillez les performances des campagnes et des parcours en temps réel.
>* [Présentation du tutoriel Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — Présentation vidéo guidée des concepts de base de Journey Optimizer.
>* [Présentation de la sécurité de Journey Optimizer ](https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf) (PDF) : architecture de sécurité, protection des données et détails de conformité.
>* [Description du produit Journey Optimizer ](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} — Décomposition des termes officiels de la licence et des fonctionnalités d&#39;édition.
