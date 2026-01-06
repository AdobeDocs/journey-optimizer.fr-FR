---
solution: Journey Optimizer
product: Journey Optimizer
title: Tester, valider et approuver
description: Découvrez toutes les fonctionnalités de test et d’approbation dans Journey Optimizer. Prévisualisez le contenu, simulez des parcours, validez les e-mails, exécutez des expériences, détectez les conflits et configurez des workflows d’approbation avant le lancement.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: test, validation, approbation, assurance qualité, assurance qualité, aq, profils de test, personnalisation, rendu, contrôle de spam, test de contenu, test a/b, détection de conflit, liste de contrôle, bat, données d’exemple, workflow d’approbation, test d’e-mail, validation de workflow
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: tm+mt
source-wordcount: '2328'
ht-degree: 6%

---

# Tester, valider et approuver{#section-overview}

Cette section couvre toutes les fonctionnalités de test et d’approbation de Journey Optimizer. Vous y trouverez des outils pour prévisualiser le contenu avec des profils de test, valider la logique de parcours, vérifier le rendu des e-mails et les scores de spam, exécuter des expériences A/B, détecter des conflits et configurer des workflows d’approbation.

Cette page de destination vous aide à choisir la bonne approche de test en fonction de ce que vous créez (campagnes ou parcours), vous guide tout au long des workflows de test recommandés et fournit un accès rapide à toutes les ressources de test et d’approbation. Commencez par [Choisir votre approche de test](#choose-your-testing-approach) ci-dessous pour identifier les outils qui s’appliquent à votre cas d’utilisation. Pour connaître la définition des termes de test clés, voir [Terminologie clé](#key-terminology).

## Tester et approuver du contenu

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Prévisualiser, tester et valider le contenu

Découvrez comment prévisualiser, tester et valider du contenu personnalisé à l’aide des profils de test, des tests de rendu des e-mails, des évaluations du score de spam, etc.

[Explorer la section Prévisualiser et tester le contenu](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Workflows d’approbation des parcours et des campagnes

Découvrez comment configurer, gérer et exécuter des processus d’approbation pour assurer le contrôle qualité des parcours et des campagnes.

[Découvrir les workflows d’approbation](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Tester votre parcours

Validez votre parcours avant de le publier en le testant avec des profils spécifiques pour vous assurer que les événements, conditions et actions fonctionnent comme prévu. Disponible pour les brouillons de parcours qui utilisent un espace de noms.

[Tester votre parcours](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Test à blanc du parcours

Effectuez un test à blanc pour simuler et valider le chemin d’exécution de votre parcours, ce qui permet d’identifier les problèmes potentiels avant l’activation.

[En savoir plus sur le test à blanc des parcours](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Surveillance et dépannage

Accédez à un ensemble complet de ressources de dépannage, d’alertes système et de codes d’erreur pour résoudre les problèmes d’exécution et de performances des parcours.

[Afficher la surveillance et le dépannage](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization Playground

Testez les expressions de personnalisation dans un environnement sûr. Testez le code avec des exemples de données et prévisualisez les résultats avant de l’appliquer à vos campagnes et parcours.

[En savoir plus sur le laboratoire Personalization](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Expériences de contenu et tests A/B

Optimisez vos campagnes en testant plusieurs variations de contenu et en mesurant les performances pour identifier les traitements les plus performants. Disponible pour les campagnes uniquement (prend en charge les expériences A/B et le bandit manchot).

[En savoir plus sur les expériences de contenu](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Listes de contrôle pour la surveillance des parties prenantes

Incluez automatiquement les adresses des parties prenantes internes dans les diffusions pour surveiller les messages réels envoyés aux clients pour l’assurance qualité et la conformité. Disponible uniquement pour le canal e-mail.

[Configurer les listes de contrôle](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

Détection des conflits

Identifiez les chevauchements potentiels entre les campagnes et les parcours afin d’éviter la surcharge de clients avec trop de communications simultanées. Disponible pour les parcours de campagnes et unitaires, de qualification d’audience et de lecture d’audience.

[Détecter les conflits](../using/conflict-prioritization/conflicts.md)
:::

::::

## Importance des tests et de l’approbation

Les processus de test et d’approbation constituent des points de contrôle qualité essentiels pour protéger la réputation de votre marque et assurer le succès de la campagne. Voici pourquoi ils sont importants :

* **Capturer les erreurs avant qu’elles n’atteignent les clients** - Identifiez les liens rompus, une personnalisation incorrecte, les problèmes de rendu et les défauts logiques dans un environnement contrôlé où les correctifs sont rapides et sans risque.

* **Améliorer la délivrabilité** - Testez les scores de spam, validez l’authentification des e-mails et vérifiez le rendu sur les clients de messagerie pour optimiser l’emplacement des boîtes de réception et les taux d’engagement.

* **Garantir la cohérence de la marque** - Prévisualisez le contenu avec différents profils de test pour vérifier que la personnalisation s’affiche correctement pour divers segments de clientèle et respecte les normes de la marque.

* **Validation de parcours complexes** - Simulez des flux de parcours à plusieurs étapes pour vérifier que les déclencheurs se déclenchent correctement, que les conditions s’évaluent correctement et que les clients reçoivent les messages appropriés au bon moment.

* **Établissement de la responsabilité** - Implémentez des workflows d’approbation officiels qui nécessitent l’approbation des parties prenantes, créant une propriété claire et réduisant les lancements de campagnes non autorisés ou prématurés.

* **Gagnez du temps et économisez des ressources** - Détectez les problèmes dès le début du cycle de développement lorsque les correctifs sont moins coûteux et plus rapides, afin d’éviter des corrections post-lancement coûteuses ou des remontées d’informations du service client.

<!--## Testing capabilities overview

**Testing types available:**

* Content testing: Preview and validate message content before sending → [Choose your testing approach](#choose-your-testing-approach)
* Journey logic testing: Simulate customer progression through journey paths → [Choose your testing approach](#choose-your-testing-approach)
* Technical testing: Validate rendering, deliverability, and authentication → [Technical validation](#2-technical-validation)
* Performance testing: Compare content variations using A/B experiments → [Content Experiments & A/B Testing](#test--approve-content)
* Conflict testing: Detect campaign and journey overlaps → [Conflict Detection](#test--approve-content)
* Approval testing: Structured review workflows before activation → [Approval Workflows](#test--approve-content)

**Key capabilities by context:**

| Capability | Applies to | Channel restrictions | Prerequisites | Primary purpose |
|------------|-----------|---------------------|--------------|-----------------|
| [Test profiles](../using/content-management/test-profiles.md) | Campaigns, Journeys | All channels | Test profiles created | Preview personalized content |
| [Sample input data](../using/test-approve/simulate-sample-input.md) | Campaigns, Journeys | Email, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON file | Test multiple personalization variants |
| [Test mode](../using/building-journeys/testing-the-journey.md) | Journeys only | N/A | Draft journey, namespace configured | Simulate profile progression |
| [Dry run](../using/building-journeys/journey-dry-run.md) | Journeys only | N/A | Journey created | Analyze execution paths |
| [Email rendering](../using/content-management/rendering.md) | Campaigns, Journeys | Email only | Litmus integration | Verify display across clients |
| [Spam score](../using/content-management/spam-report.md) | Campaigns, Journeys | Email only | None | Deliverability validation |
| [Seed lists](../using/configuration/seed-lists.md) | Campaigns, Journeys | Email only | Seed list configured | Stakeholder monitoring |
| [Content experiments](../using/content-management/get-started-experiment.md) | Campaigns only | All channels | None | A/B and multi-armed bandit testing |
| [Conflict detection](../using/conflict-prioritization/conflicts.md) | Campaigns, Journeys (limited) | All channels | None | Prevent customer over-messaging |
| [Approval workflows](../using/test-approve/gs-approval.md) | Campaigns, Journeys | All channels | Approval policy created | Structured review process |
| [Personalization playground](../using/personalization/personalize.md#playground) | All | All channels | None | Learn and test personalization syntax |

**Common testing workflows:**

1. Pre-development: Use [personalization playground](#test--approve-content) to learn syntax
2. During development: Preview with [test profiles](#choose-your-testing-approach), validate with [sample input data](#choose-your-testing-approach)
3. Pre-launch: Run [technical tests](#2-technical-validation) (rendering, spam), check [conflicts](#test--approve-content), submit for [approval](#test--approve-content)
4. Post-launch: Monitor with live reports (see [Monitoring & Troubleshooting](#test--approve-content)), iterate based on results

-->

<!--
## Decision tree for testing method selection

Use this decision tree to quickly identify the right testing tools for your specific scenario. Answer each question based on your context (what you're building, what you need to validate, and which channel you're using) to navigate directly to the relevant capabilities and documentation.

+++ **Question 1: What are you testing?**

* Campaign → [Choose your testing approach](#choose-your-testing-approach)
* Journey → [Choose your testing approach](#choose-your-testing-approach)
* Personalization expressions → [Personalization playground](#test--approve-content)
+++

+++**Question 2: What aspect needs validation?**

* Content and personalization → [Test profiles](#choose-your-testing-approach) or [sample input data](#choose-your-testing-approach)
* Email display → [Email rendering tests](#2-technical-validation)
* Deliverability → [Spam score checks](#2-technical-validation)
* Journey logic and flow → [Test mode](#choose-your-testing-approach) or [dry run](#test--approve-content)
* Performance comparison → [Content experiment](#test--approve-content) (campaigns only)
* Timing conflicts → [Conflict detection](#test--approve-content)
* Stakeholder review → [Approval workflow](#test--approve-content)
+++

+++**Question 3: What channel?**

* Email → All testing methods available (see [Choose your testing approach](#choose-your-testing-approach))
* SMS, Push → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Web, In-app, Code-based → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Multiple channels → Test each channel separately
+++

+++**Question 4: When in the workflow?**

* Before building → [Personalization playground](#test--approve-content) for learning
* During building → [Test profiles](#choose-your-testing-approach) and [sample input data](#choose-your-testing-approach) for validation
* Before launch → [Rendering tests](#2-technical-validation), [spam checks](#2-technical-validation), [conflict detection](#test--approve-content), [approvals](#test--approve-content)
* After launch → [Live reports](../using/building-journeys/report-journey.md) and [monitoring](#test--approve-content)
+++

-->

## Choisir votre approche de test

La bonne approche de test dépend de ce que vous créez et de ce que vous devez valider. Utilisez ce guide pour identifier les outils de test les plus pertinents pour votre scénario.

>[!BEGINTABS]

>[!TAB Test des campagnes]

**Pour toutes les campagnes :**

* Prévisualiser et tester le contenu à l’aide de [profils de test](../using/content-management/test-profiles.md) ou [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md)
* Vérifier le [rendu des e-mails](../using/content-management/rendering.md) sur les appareils et les clients (canal e-mail uniquement)
* Exécuter [contrôles du score de spam](../using/content-management/spam-report.md) (canal e-mail uniquement)
* Vérification [conflits](../using/conflict-prioritization/conflicts.md) avec d’autres campagnes et parcours
* Configurer des [listes de contrôle](../using/configuration/seed-lists.md) pour la surveillance des parties prenantes (canal e-mail uniquement)
* Envoyer pour [approbation](../using/test-approve/gs-approval.md) avant l’activation

**Pour les tests A/B et l’optimisation :**

* Créez des [expériences de contenu](../using/content-management/get-started-experiment.md) pour tester plusieurs traitements et mesurer les performances

**Pour les campagnes déclenchées par API :**

* Utilisez l’[API de simulation Campaign](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-« _blank »} pour déclencher des tâches de BAT par programmation

>[!TAB Test des parcours ]

**Pour tous les parcours :**

* Utilisez [mode test](../using/building-journeys/testing-the-journey.md) pour simuler la progression du profil (les brouillons de parcours uniquement, nécessitent un espace de noms) ou [exécution d’essai](../using/building-journeys/journey-dry-run.md) pour analyser les chemins d’exécution sans envoyer de messages
* Tester des messages individuels à l’aide de [prévisualisation et BAT](../using/content-management/preview-test.md)
* Cochez la case [conflits](../using/conflict-prioritization/conflicts.md) avec d’autres parcours et campagnes.
* Envoyer pour [approbation](../using/test-approve/gs-approval.md) avant publication

**Pour les parcours complexes :**

* Utilisez le mode test et l’exécution d’essai ensemble pour valider minutieusement la logique de branchement et les chemins d’exécution
* Testez systématiquement différentes conditions d’entrée et attributs de profil

**Remarque :** la détection des conflits et la limitation des parcours sont disponibles pour les parcours unitaires, de qualification d’audience et de lecture d’audience uniquement.

>[!TAB Test de la personnalisation]

**Avant de créer du contenu :**

* Testez le [terrain de jeu de la personnalisation](../using/personalization/personalize.md#playground) pour apprendre la syntaxe et tester des expressions avec des exemples de données

**Lors de la création du contenu :**

* Aperçu avec des [profils de test](../using/content-management/test-profiles.md) pour valider correctement les rendus de personnalisation
* Tester plusieurs scénarios à l’aide de [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) provenant de fichiers CSV/JSON (prend en charge jusqu’à 30 variantes)

>[!ENDTABS]

## Bonnes pratiques de test

Pour optimiser l’efficacité de vos efforts de test, suivez ces pratiques recommandées :

1. **Testez tôt et souvent** - N’attendez pas qu’une campagne soit entièrement créée. Testez le contenu, la personnalisation et la logique de manière progressive au fur et à mesure que vous développez.

1. **Utiliser des profils de test réalistes** - [Créez des profils de test](../using/audience/creating-test-profiles.md) qui représentent précisément vos segments d’audience cible, y compris les cas Edge et les différents scénarios de personnalisation.

1. **Test sur les appareils et les clients** - Vérifiez [le rendu des e-mails](../using/content-management/rendering.md) sur les clients de messagerie les plus courants (Gmail, Outlook, Apple Mail) et les appareils (bureau, mobile, tablette) pour garantir un affichage cohérent (canal e-mail uniquement).

1. **Valider entièrement la personnalisation** - Effectuez des tests avec plusieurs [profils de test](../using/content-management/test-profiles.md) dont les valeurs d’attribut sont différentes pour confirmer que les jetons de personnalisation s’affichent correctement et que les valeurs de secours fonctionnent. Utilisez le [terrain de jeu de la personnalisation](../using/personalization/personalize.md#playground) pour tester les expressions de personnalisation et le code avec des exemples de données avant de les appliquer à vos campagnes.

1. **Tester les variations de contenu avec des exemples de données** - Utilisez [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) à partir de fichiers CSV ou JSON pour tester jusqu’à 30 scénarios de personnalisation sans créer de nombreux profils de test, ce qui vous permet de gagner du temps tout en assurant une couverture complète. Prend en charge les canaux e-mail, SMS, notification push, web, expérience basée sur le code, in-app et cartes de contenu.

1. **Utiliser des listes de contrôle pour la surveillance des parties prenantes** - Configurez les [listes de contrôle](../using/configuration/seed-lists.md) pour inclure automatiquement les parties prenantes internes qui recevront des copies de toutes les diffusions au moment de l’exécution pour la surveillance de la qualité et la vérification de la conformité (canal e-mail uniquement).

1. **Simuler des chemins de parcours** - Pour les parcours complexes comportant plusieurs branches, utilisez [mode test](../using/building-journeys/testing-the-journey.md) pour tester différentes conditions d’entrée et attributs de profil afin de valider tous les chemins possibles. Disponible pour les brouillons de parcours qui utilisent un espace de noms.

1. **Vérifier les indicateurs de délivrabilité** - Examinez [les scores de spam](../using/content-management/spam-report.md), le statut d’authentification et les mesures d’intégrité des e-mails avant les envois volumineux (canal e-mail uniquement).

1. **Documenter les résultats des tests** - Conservez des enregistrements des résultats des tests, des problèmes détectés et des résolutions pour améliorer les futurs processus de test et partagez les enseignements avec votre équipe.

1. **Impliquez rapidement les parties prenantes** - Partagez les aperçus et les résultats des tests avec les parties prenantes avant l’[approbation formelle](../using/test-approve/gs-approval.md) afin de recueillir les commentaires et d’aligner les attentes.

## Workflow de test recommandé

Suivez cette approche en 4 phases pour valider vos campagnes et parcours avant le lancement :

| Phase | Éléments à tester | Actions clés |
|-------|-------------|-------------|
| **1. Validation du contenu** | Personalization, conception, rendu | [Aperçu avec profils de test](../using/content-management/preview-test.md), test [plusieurs variations](../using/test-approve/simulate-sample-input.md) avec CSV/JSON, vérification [rendu](../using/content-management/rendering.md) sur tous les appareils |
| **2. Contrôles techniques** | Délivrabilité, liens, conflits | Exécutez [contrôles de score de spam](../using/content-management/spam-report.md), validez les liens, recherchez [conflits](../using/conflict-prioritization/conflicts.md) avec d’autres campagnes. |
| **3. Logique de parcours** (parcours uniquement) | Conditions d’entrée, flux, embranchement | Utilisez [mode test](../using/building-journeys/testing-the-journey.md) pour simuler la progression, exécutez [essai](../using/building-journeys/journey-dry-run.md) pour les chemins complexes |
| **4. Pré-lancement** | Paramètres, validations, surveillance | Envoyer pour [approbation](../using/test-approve/gs-approval.md), vérifier les plannings et les audiences, activer [alertes](../using/reports/alerts.md) |

**Conseil pro :** commencez par le [terrain de jeu de la personnalisation](../using/personalization/personalize.md#playground) pour tester les expressions avant de créer du contenu et vérifiez toujours [détection de conflit](../using/conflict-prioritization/conflicts.md) avant le lancement pour éviter la surmessagerie.

## Tests en action : cas d’utilisation

Découvrez comment les concepts de test s’appliquent aux scénarios réels :

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="Envoi de messages multi-canal" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>Envoyer des messages multicanaux</strong></a>
</div>
<p>
Testez un parcours qui combine la lecture d’audience, les événements de réaction et les e-mails/messages push. Validez l’ensemble du flux, du ciblage des audiences à la diffusion des messages. Concentrez-vous sur la coordination multicanal, les événements de réaction, la validation du flux de bout en bout et les étapes de test/publication.
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="Envoyer un message aux abonnés" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>Envoyer un message aux abonnés</strong></a>
</div>
<p>
Testez des parcours qui ciblent les listes d’abonnements avec une adresse e-mail dynamique. Validez les expressions de personnalisation pour un ciblage correct des abonnés. Concentrez-vous sur les expressions de personnalisation, l’adressage dynamique et le ciblage des listes d’abonnements.
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="Envoyer des messages limités dans le temps" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>Envoyer des messages limités dans le temps</strong></a>
</div>
<p>
Testez des parcours avec des conditions temporelles pour vous assurer que les messages sont envoyés à des jours spécifiques. Validez les activités d’attente et la logique de planification. Concentrez-vous sur les conditions temporelles, les activités d’attente et la validation de la planification.
</p>
</td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/jo-use-cases.md">
<img alt="Explorer d’autres cas d’utilisation de parcours" src="../using/assets/do-not-localize/icon-quick-start.svg">
</a>
<div>
<a href="../using/building-journeys/jo-use-cases.md"><strong>Explorer d’autres cas d’utilisation de parcours </strong></a>
</div>
<p>
Accédez à une collection complète d’exemples pratiques couvrant les événements d’expérience, la messagerie multicanal et les intégrations système externes. Explorez divers scénarios, modèles avancés et approches de test d’intégration.
</p>
</td>
</tr></table>

## Terminologie clé

Familiarisez-vous avec ces concepts de test essentiels pour mieux comprendre les fonctionnalités de test et d’approbation de Journey Optimizer. Chaque terme renvoie à une documentation détaillée.

**[Profils de test](../using/content-management/test-profiles.md)** - Profils client synthétiques (et non clients réels) utilisés pour prévisualiser du contenu personnalisé. Signalé dans le service de profil client en temps réel. Obligatoire pour le mode test et la prévisualisation du contenu. [Découvrez comment créer des profils de test.](../using/audience/creating-test-profiles.md)

**[Mode test](../using/building-journeys/testing-the-journey.md)** - Fonction de simulation de Parcours qui envoie des profils de test par le biais de chemins de parcours. Limites : parcours de brouillon uniquement, espace de noms requis, profils de test uniquement. [Voir la documentation sur le mode test](../using/building-journeys/testing-the-journey.md)

**[Exécution d’essai](../using/building-journeys/journey-dry-run.md)** outil d’analyse d’exécution de Parcours qui effectue le suivi des chemins sans envoyer de messages ni effectuer d’appels API. Cas d’utilisation : validation de la logique sans consommer de ressources. [En savoir plus sur l’essai](../using/building-journeys/journey-dry-run.md)

**[Exemples de données d’entrée](../using/test-approve/simulate-sample-input.md)** - Fichiers CSV ou JSON contenant des valeurs d’attribut de profil pour tester la personnalisation. Prend en charge jusqu’à 30 variantes. Alternative à la création de profils de test. [Comment simuler des variations de contenu ](../using/test-approve/simulate-sample-input.md)

**[Listes de contrôle](../using/configuration/seed-lists.md)** - Adresses e-mail des parties prenantes internes automatiquement incluses dans les diffusions réelles (et non les envois de test). Canal e-mail uniquement. Cas pratique : surveillance de la qualité et conformité. [Configuration des listes de contrôle](../using/configuration/seed-lists.md)

**[Expériences de contenu](../using/content-management/get-started-experiment.md)** - Tests A/B ou expériences de bandit manchot comparant des variations de contenu. Campagnes uniquement, non disponible dans les parcours. [Prise en main des expériences](../using/content-management/get-started-experiment.md) | [Création d’expériences](../using/content-management/content-experiment.md)

**[BAT](../using/content-management/proofs.md)** - Testez les diffusions e-mail envoyées à des adresses e-mail spécifiques à l’aide des données de profil de test. Différent des listes de contrôle (les BAT sont des envois de test manuels, les listes de contrôle sont des copies automatiques des parties prenantes). [Envoi de BAT](../using/content-management/proofs.md)

**[Détection des conflits](../using/conflict-prioritization/conflicts.md)** - Outil qui identifie les campagnes et les parcours qui se chevauchent et ciblent les mêmes audiences. Prise en charge limitée des parcours : unitaire, qualification d’audience et lecture d’audience uniquement. [En savoir plus sur la gestion des conflits](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Workflows d’approbation](../using/test-approve/gs-approval.md)** - Processus de révision en plusieurs étapes nécessitant l’approbation des parties prenantes avant activation. Nécessite la configuration d’une politique d’approbation. [Configurer les validations](../using/test-approve/gs-approval.md) | [Créer des politiques](../using/test-approve/approval-policies.md)

**[Tests de rendu](../using/content-management/rendering.md)** - Validation de l’affichage des e-mails sur les clients de messagerie (Gmail, Outlook, Apple Mail) et les appareils. Nécessite l’intégration de Litmus. [Tester le rendu des e-mails](../using/content-management/rendering.md)

**[Terrain de jeu Personalization](../using/personalization/personalize.md#playground)** - Environnement d’apprentissage interactif pour tester la syntaxe de personnalisation et des expressions de test avec des exemples de données. Aucun jeu de données actif n’est requis. [Accédez au terrain de jeu](../using/personalization/personalize.md#playground)

## Ressources supplémentaires

>[!BEGINTABS]

>[!TAB Guides essentiels ]

* [ Simuler des variations de contenu ](../using/test-approve/simulate-sample-input.md) - Testez jusqu’à 30 scénarios de personnalisation à l’aide de fichiers CSV ou JSON. Idéal pour les tests de contenu multilingue sans créer plusieurs profils de test. Prend en charge les e-mails, SMS, notifications push, web, basées sur le code, in-app et cartes de contenu.

* [Création de profils de test](../using/audience/creating-test-profiles.md) - Créez et gérez des profils de test pour simuler des scénarios client. Découvrez comment marquer les profils pour les tests, définir des attributs et organiser les segments de test.

* [Rapport sur les courriers indésirables](../using/content-management/spam-report.md) - Vérifiez les scores de spam avant l&#39;envoi pour améliorer la délivrabilité et le positionnement dans la boîte de réception. Obtenez des recommandations exploitables pour l’optimisation du contenu.

* [FAQ sur les Parcours ](../using/building-journeys/journey-faq.md) - Référence rapide pour les questions courantes sur les tests de parcours, l’exécution et le dépannage.

>[!TAB Dépendances et relations]

Découvrez comment les fonctionnalités de test sont connectées les unes aux autres et à vos workflows Journey Optimizer au sens large. Cette section mappe les conditions préalables, les dépendances en amont/en aval et les combinaisons de fonctionnalités courantes.

+++**Conditions préalables (requises avant le test)**

* Les profils de test doivent être créés avant d’utiliser le mode test ou l’aperçu de contenu
* Les politiques d’approbation doivent être configurées avant l’envoi pour approbation
* Les listes de contrôle doivent être créées avant d’être ajoutées aux campagnes/parcours
* Intégration de Litmus requise pour les tests de rendu des e-mails
* Le parcours doit être à l’état de brouillon pour utiliser le mode test
* L’espace de noms du parcours doit être configuré pour utiliser le mode test

+++

+++**De quoi dépend le test (en amont)**

* Création de contenu : campagnes ou parcours à tester nécessaires
* Profils de test : requis pour le mode test et la prévisualisation du contenu
* Politiques d’approbation : obligatoire pour les workflows d’approbation
* Configuration : configurations de canal, authentification par e-mail, paramètres de domaine.

+++

+++**Ce qui dépend des tests (en aval)**

* Activation de la campagne/du parcours : impossible d’activer sans résoudre les erreurs
* Publication : une approbation peut être requise avant la publication.
* Surveillance en direct : surveillance et reporting après le lancement
* Optimisation : utilisez les résultats de test pour affiner les campagnes futures.

+++

+++**Fonctionnalités associées**

* Workflows de test et d&#39;approbation - Processus d&#39;assurance qualité
* Tests + détection des conflits - Prévention de la messagerie excessive des clients
* Tests + Expériences de contenu - Optimisation des performances
* Tests + reporting - Cycle d’amélioration continue
* Profils de test + Personalization - Validation du contenu
* Exécution d’essai + mode Test - Validation complète du parcours

+++

+++**Combinaisons de fonctionnalités courantes**

* Tests de contenu : profils de test + exemples de données d’entrée + terrain de jeu Personalization
* Validation des e-mails : rendu des tests + scores de spam + profils de test + BAT
* Validation du parcours : Mode test + Exécution d’essai + Profils de test
* Liste de contrôle de prélancement : tous les tests techniques + détection des conflits + workflows d’approbation

+++

>[!TAB Questions courantes]

+++**Q : Quels sont les tests requis avant de lancer une campagne ?**

**Minimum :** aperçu du contenu avec profils de test + vérification du score de spam (email)
**Recommandé :** + Rendu des e-mails + Détection des conflits + Workflow d’approbation
**Bonne pratique :** + Test d’exemples de données d’entrée + Listes de contrôle + Expérience A/B (si optimisation)

+++

+++**Q : Comment tester la personnalisation sans créer de nombreux profils de test ?**

**Solution de Principal :** utilisez [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) avec des fichiers CSV/JSON (prend en charge jusqu’à 30 variantes)
**Alternative :** créez 3 à 5 profils de test représentatifs [profils de test](../using/audience/creating-test-profiles.md) couvrant les segments clés
**Outil d’apprentissage :** Expérimentez d’abord dans [terrain de jeu de personnalisation](../using/personalization/personalize.md#playground)

+++

+++**Q : Quelle est la différence entre le mode test et le mode essai pour les parcours ?**

**Mode test :** envoie des profils de test par le biais du parcours, déclenche des actions réelles et génère des messages de test. Nécessite un brouillon de parcours + espace de noms.
**Exécution d’essai :** effectue le suivi des chemins d’exécution sans rien envoyer. Fonctionne avec n’importe quel statut de parcours. Aucun message envoyé, aucune action exécutée.
**Utiliser ensemble :** Mode test pour le test des messages + Exécution d’essai pour la validation de la logique - couverture complète.

+++

+++**Q : Puis-je tester les parcours au statut production/actif ?**

**Mode Test :** Non - parcours de brouillon uniquement
**Exécution d’essai :** Oui - fonctionne quel que soit le statut du parcours
**Aperçu du contenu :** Oui - prévisualisez des messages individuels à tout moment
**Solution :** dupliquer le parcours dynamique en mode brouillon pour la validation du mode test complet.

+++

+++**Q : Quelles fonctionnalités de test nécessitent des intégrations externes ?**

**Rendu des e-mails :** nécessite l’intégration de Litmus (licence distincte)
**Tous les autres :** intégré à Journey Optimizer, aucune intégration supplémentaire requise
**Remarque :** les profils de test nécessitent le service de profil client en temps réel (inclus)

+++

+++**Q : Comment tester les campagnes déclenchées par l’API ?**

**Option 1 :** utiliser l’[API de simulation de campagne](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-« _blank »} pour les tests programmatiques
**Option 2 : prévisualisation** contenu avec profils de test dans l’interface utilisateur
**Option 3 :** envoyer des BAT aux adresses e-mail de test
**Bonne pratique :** combinez les trois pour une validation complète

+++

>[!ENDTABS]
