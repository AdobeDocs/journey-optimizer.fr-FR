---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les parcours
description: 'Commencer avec les parcours : découvrez les types de parcours, les workflows, les fonctionnalités et les bonnes pratiques pour créer des expériences clients personnalisées dans Adobe Journey Optimizer.'
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: parcours, découverte, commencer, unitaire, lecture d’audience, qualification d’audience, événement métier, temps réel, planifié, lot, déclenché par un événement, workflow, orchestration, personnalisation, multicanal
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: ht
source-wordcount: '1448'
ht-degree: 100%

---


# Commencer avec les parcours{#jo-general-principle}

Adobe Journey Optimizer vous permet de créer des parcours clients personnalisés et à plusieurs étapes qui s’adaptent en temps réel au comportement et aux besoins de votre audience. Grâce à une zone de travail intuitive par glisser-déposer, vous pouvez orchestrer des messages et des actions sur plusieurs canaux, en exploitant les données contextuelles et le ciblage des audiences pour un impact maximal.

Ce guide fournit une feuille de route claire pour vous aider à comprendre les principes de base des parcours, à choisir le type de parcours approprié à votre cas d’utilisation et à concevoir en toute confiance des parcours qui offrent des expériences clients significatives et opportunes.

## Que sont les parcours ?

Les **parcours** sont des expériences clients automatisées à plusieurs étapes qui orchestrent des interactions personnalisées entre les canaux en réponse au comportement client, aux événements métier ou aux campagnes planifiées.

Utilisez [!DNL Journey Optimizer] pour :

* créer des cas d’utilisation d’**orchestration en temps réel** à l’aide de données contextuelles stockées dans des événements ou des sources de données ;
* concevoir des **scénarios avancés à plusieurs étapes** qui répondent dynamiquement au comportement client et aux événements métier ;
* diffuser des **expériences personnalisées 1:1** à grande échelle par e-mail, notification push, SMS, in-app, web, etc.

![Interface du concepteur de parcours avec la palette, la zone de travail et le volet Propriétés](assets/journey38.png)

➡️ **Vous souhaitez commencer à créer ?** [Créez votre premier parcours ](journey-gs.md) en 5 minutes.

### Parcours ou campagnes : quand utiliser l’un ou l’autre {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer propose trois approches pour atteindre les clientes et clients : les **parcours** (orchestration en temps réel 1:1), les **campagnes** (diffusion simple par lots ou déclenchée par API) et les **campagnes orchestrées** (workflows de zone de travail par lots avec des données multi-entités).

**Décision rapide :**

* Utilisez les **parcours** pour des expériences à plusieurs étapes, axées sur le comportement, où chaque cliente ou client progresse à son propre rythme.
* Utilisez des **campagnes d’action/déclenchées par API** pour une diffusion de messages simple, planifiée ou déclenchée auprès de vos audiences.
* Utilisez des **campagnes orchestrées** pour les workflows par lots complexes nécessitant une segmentation multi-entités et un nombre exact de pré-envois.

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Choisissez votre type de parcours. {#journey-types}

Adobe Journey Optimizer prend en charge quatre types de parcours, chacun conçu pour différents mécanismes d’entrée et scénarios métier :

* **Parcours unitaires** : expériences déclenchées par un événement en temps réel (confirmations de commande, e-mails de bienvenue).
* **Parcours de lecture d’audience** : communications par lots planifiées à des segments d’audience (newsletters, campagnes promotionnelles)
* **Parcours de qualification d’audience** : réponses en temps réel aux modifications de l’appartenance à l’audience (mises à niveau de VIP, réengagement)
* **Parcours d’événement métier** : conditions métier affectant plusieurs clientes et clients (alertes de stock, ventes flash).

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Créer avec le concepteur de parcours {#journey-designer}

Le **[concepteur de parcours](using-the-journey-designer.md)** est votre zone de travail visuelle pour créer des expériences clients. Grâce à une interface intuitive par glisser-déposer, vous pouvez orchestrer chaque étape de votre parcours sans avoir à écrire de code.

![Interface du concepteur de parcours avec la palette, la zone de travail et le volet Propriétés](assets/journey38.png)

### Ce que vous pouvez faire dans le concepteur :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Définir des points d’entrée**

Choisissez le mode d’entrée des clientes et clients : par le biais d’un événement, d’un segment d’audience ou d’une qualification d’audience.

[En savoir plus sur la gestion des entrées](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Envoyer des messages**

Utilisez des actions de canal intégrées pour les e-mails, les notifications push, les SMS/MMS, les messages in-app, les messages web, etc., le tout dans Journey Optimizer.

[Envoyer des messages dans les parcours](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Ajouter une logique et des conditions**

Créez des branches pour votre parcours en fonction des attributs de profil, de l’appartenance à l’audience ou des événements en temps réel.

[Utiliser des conditions](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=fr)

**Utiliser des données**

Utilisez des données contextuelles issues d’événements, d’Adobe Experience Platform ou de services d’API tiers.

[Utiliser des sources de données](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Connecter des systèmes externes**

Créez des actions personnalisées pour intégrer des systèmes tiers afin d’envoyer des messages ou de déclencher des workflows.

[Configurer des actions personnalisées](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Ajouter des activités d’orchestration**

Utilisez les temps d’attente, les sauts, les mises à jour de profil et la gestion de l’audience pour créer des flux sophistiqués.

[Explorer toutes les activités](about-journey-activities.md)
:::

::::

➡️ **Formation pratique :** [regardez la vidéo sur le concepteur de parcours](#video) ou [explorez des cas d’utilisation de bout en bout](jo-use-cases.md).

## Workflow de création de votre parcours {#workflow}

La création de parcours optimaux suit un processus clair et reproductible. Voici votre workflow détaillé :

**1. Planifier** → **2. Concevoir** → **3. Tester** → **4. Publier** → **5. Surveiller** → **6. Optimiser**

### &#x200B;1. Planifier votre parcours {#plan}

Avant d’ouvrir le concepteur, clarifiez vos objectifs :

* **Quel est l’objectif ?** (par exemple, intégrer une nouvelle clientèle, réengager des utilisateurs et utilisatrices inactifs)
* **Qui est l’audience ?** (segment spécifique, individus pilotés par un événement)
* **Quel type de parcours convient ?** (voir les [types de parcours ](#journey-types) ci-dessus)
* **Quels canaux allez-vous utiliser ?** (e-mail, notification push, SMS, etc.)

### &#x200B;2. Concevoir dans la zone de travail {#design}

Utilisez le concepteur de parcours pour créer votre flux :

* **Définir des conditions d’entrée** : définissez l’entrée des profils (événement, audience, qualification).
* **Ajouter une logique d’orchestration** : incluez des temps d’attente, des conditions et des points de décision.
* **Configurer les messages** : concevez vos communications ou utilisez des modèles existants.
* **Configurer des actions** : configurez des actions intégrées ou personnalisées à exécuter.
* **Définir les critères de sortie** : spécifiez quand et comment les profils terminent le parcours.

[Découvrir comment utiliser le concepteur de parcours →](using-the-journey-designer.md)

### &#x200B;3. Tester avant la mise en ligne {#test}

Testez toujours votre parcours pour détecter les problèmes avant que les clientes et clients ne les rencontrent :

* Utilisez le **mode test** pour simuler le parcours avec des profils de test.
* Utilisez un **test à blanc** pour prévisualiser l’exécution du parcours sans affecter les données réelles ou envoyer des messages.
* Vérifiez que toutes les conditions, tous les messages et toutes les actions fonctionnent comme prévu.
* Vérifiez les délais, les flux de données et la personnalisation.

[Tester votre parcours →](testing-the-journey.md) | [En savoir plus sur le test à blanc →](journey-dry-run.md)

### &#x200B;4. Publier votre parcours {#publish}

Une fois le test terminé, publiez votre parcours pour l’activer :

* Vérifiez les paramètres et propriétés finaux.
* Publiez le parcours afin de l’activer pour les clientes et clients réels.
* Remarque : les parcours actifs peuvent être arrêtés, mais pas modifiés (vous devez en créer une nouvelle version).

[Publier votre parcours →](publish-journey.md)

### &#x200B;5. Surveiller les performances {#monitor}

Suivez les performances réelles de votre parcours :

* Affichez des rapports et des analyses de parcours.
* Surveillez les taux d’entrée, d’achèvement et d’erreur.
* Configurez des alertes pour les problèmes critiques.

[Surveiller et établir des rapports → ](report-journey.md) | [Configurer les alertes →](../reports/alerts.md)

### &#x200B;6. Optimiser et itérer {#optimize}

Utilisez les informations pour apporter des améliorations :

* Analysez les mesures d’engagement et les taux de conversion.
* Testez l’optimisation de l’heure d’envoi.
* Créez de nouvelles versions de parcours avec des améliorations.
* Utilisez les recommandations optimisées par l’IA.

[Optimiser vos parcours →](optimize.md) | [→ Optimisation de l’heure d’envoi](send-time-optimization.md)

➡️ **Vous voulez démarrer ?** [Créer votre premier parcours maintenant→](journey-gs.md)

## Cas d’utilisation réels {#use-cases}

Découvrez des exemples pratiques qui montrent comment appliquer des concepts de parcours pour résoudre des problèmes marketing courants :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Bienvenue aux nouvelles personnes abonnées**

Lorsqu’un client ou une cliente s’abonne à votre service, déclenchez un parcours de bienvenue qui l’encourage à effectuer les étapes d’intégration.

[Afficher le cas d’utilisation →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Optimisation de l’heure d’envoi**

Utilisez l’IA pour diffuser des e-mails lorsque chaque personne cliente est la plus susceptible d’interagir, en maximisant les taux d’ouverture et de clics.

[Afficher le cas d’utilisation →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Accélérer les diffusions**

Augmentez progressivement le volume des messages pour améliorer votre réputation d’envoi et éviter les problèmes de délivrabilité.

[Afficher le cas d’utilisation →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Ciblage par jour de la semaine**

Envoyez du contenu différent en fonction du jour de la semaine où les clientes et clients rejoignent votre parcours pour une meilleure pertinence.

[Afficher le cas d’utilisation →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Campagnes multicanaux**

Orchestrez des expériences optimales sur les canaux e-mail, push, SMS et web dans un seul parcours.

[Afficher le cas d’utilisation →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Tous les cas d’utilisation**

Explorez la bibliothèque complète des cas d’utilisation de parcours avec des implémentations détaillées.

[Tout parcourir →](jo-use-cases.md) | [Bibliothèque de cas d’utilisation →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explorer les fonctionnalités de parcours {#capabilities}

À mesure que vous vous familiarisez avec la création de parcours, explorez ces puissantes fonctionnalités pour créer des expériences clients sophistiquées :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Expressions avancées**

Créez des conditions dynamiques et une personnalisation à l’aide de l’éditeur d’expression pour la manipulation de données et une logique complexe.

[Découvrir les expressions](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=fr)

**Gestion des fuseaux horaires**

Gérez les audiences globales avec des ajustements de fuseau horaire automatiques et des heures d’envoi optimales.

[Gérer les fuseaux horaires](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Mode test et test à blanc**

Validez les parcours avec des profils de test avant la mise en ligne et prévisualisez l’exécution sans affecter les données réelles.

[Utiliser un test à blanc](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=fr)

**Copier dans le sandbox**

Dupliquez des parcours dans les sandbox pour rationaliser les workflows de test et de déploiement.

[Copier les parcours](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Balises et organisation**

Utilisez des balises pour classer et filtrer les parcours afin d’améliorer la gestion à grande échelle.

[Organiser avec des balises](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Contrôle de débit**

Limitez le débit des messages pour gérer la réputation des envois et éviter de surcharger les systèmes.

[Contrôler le débit](limit-throughput.md)
:::

::::

[Afficher toutes les fonctionnalités du parcours →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Apprendre en regardant {#video}

Obtenez une présentation visuelle des composants de parcours et découvrez les principes de base de la création de parcours dans la zone de travail :

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Vous voulez plus de vidéos ?** [Découvrir les tutoriels vidéo sur les parcours](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Questions courantes {#common-questions}

+++ Quelle est la différence entre un parcours et une campagne ?

Adobe Journey Optimizer propose trois approches :

* **Parcours** : orchestration en temps réel 1:1 où chaque profil parcourt les différentes étapes à son propre rythme. Idéal pour les expériences à plusieurs étapes axées sur le comportement avec une logique conditionnelle (par exemple, intégration, abandon de panier).

* **Campagnes (d’action et déclenchées par API)** : diffusion simple des messages aux audiences, s’exécutant simultanément sur tous les profils selon le planning ou via un déclencheur API. Idéal pour les campagnes promotionnelles, les newsletters et les messages transactionnels.

* **Campagnes orchestrées** : workflows par lots à plusieurs étapes avec segmentation complexe à l’aide de données relationnelles (profils + produits/magasins/réservations). Tous les profils sont traités avec le nombre exact de pré-envois. Idéal pour les promotions saisonnières, les lancements de produits et les campagnes nécessitant des données multi-entités.

**Différence clé** : les parcours conservent l’état individuel du client ou de la cliente pour les actions en temps réel. Les campagnes d’action/API diffusent des messages simples par lots. Les campagnes orchestrées fournissent des zones de travail de workflows par lots avec des fonctionnalités de segmentation multi-entités.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Découvrir les campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Puis-je modifier un parcours actif ?

Vous pouvez modifier des éléments limités (nom, contenu du message), mais les modifications structurelles nécessitent la création d’une nouvelle version. [Découvrir les versions de parcours](publish-journey.md#journey-versions)

+++

➡️ **Vous avez d’autres questions ?** [Consulter l’intégralité des question fréquentes sur les parcours](journey-faq.md) avec plus de 40 réponses détaillées

## Besoin d’aide ? {#help}

### Liens rapides pour les tâches courantes

* **[Créer votre premier parcours](journey-gs.md)** – Guide détaillé pour les personnes qui débutent
* **[Questions fréquentes sur les  parcours](journey-faq.md)** – Réponses aux questions courantes
* **[Dépannage](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** – Diagnostiquer et résoudre les problèmes
* **[Référence des codes d’erreur](error-codes-reference.md)** – Comprendre les messages d’erreur
* **[Mécanismes de sécurisation et limitations](../start/guardrails.md)** – Limites techniques et bonnes pratiques

### Recevoir des notifications sur les problèmes

Configurez des **[alertes de parcours](../reports/alerts.md)** pour recevoir des notifications en temps réel en cas d’erreurs ou d’anomalies dans les parcours.

### Ressources supplémentaires

* **[Hub de gestion des parcours](/help/rp_landing_pages/manage-journey-landing-page.md)** – Outils de filtrage, d’optimisation et de gestion des profils
* **[Référence des activités de parcours](/help/rp_landing_pages/about-journey-building-landing-page.md)** – Guide complet de tous les types d’activités
* **[Résolution des problèmes d’exécution](troubleshooting-execution.md)** – Déboguer les problèmes d’exécution de parcours
* **[Résolution des problèmes d’activités entrantes](troubleshooting-inbound.md)** – Corriger les problèmes d’entrée et de qualification

**Vous voulez créer votre premier parcours ?** [ Cʼest parti ! →](journey-gs.md)
