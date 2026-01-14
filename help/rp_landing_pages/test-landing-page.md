---
solution: Journey Optimizer
product: Journey Optimizer
title: Tester, valider et approuver
description: Découvrez toutes les fonctionnalités de test et d’approbation dans Journey Optimizer. Prévisualisez le contenu, simulez des parcours, validez des e-mails, exécutez des expériences, détectez les conflits et configurez des workflows d’approbation avant le lancement.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: tester, valider, approuver, approbation, assurance qualité, aq, profils de test, personnalisation, rendu, contrôle de spam, expérience de contenu, test a/b, détection de conflit, liste de contrôle, bat, données d’exemple, workflow d’approbation, test d’e-mail, workflow de validation
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---

# Tester, valider et approuver{#section-overview}

Cette section couvre toutes les fonctionnalités de test et d’approbation de Journey Optimizer. Vous y trouverez des outils pour prévisualiser le contenu avec des profils de test, valider la logique de parcours, vérifier le rendu des e-mails et les scores de spam, exécuter des expériences A/B, détecter des conflits et configurer des workflows d’approbation.

Cette page de destination vous permet de choisir la bonne approche de test en fonction de ce que vous créez (campagnes ou parcours), vous guide tout au long des workflows de test recommandés et fournit un accès rapide à toutes les ressources de test et d’approbation. Commencez par [Choisir votre approche de test](#choose-your-testing-approach) ci-dessous pour identifier les outils qui s’appliquent à votre cas d’utilisation. Pour connaître la définition des termes de test clés, voir [Terminologie clé](#key-terminology).

## Tester et approuver du contenu

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=fr)

Prévisualiser, tester et valider le contenu

Découvrez comment prévisualiser, tester et valider du contenu personnalisé à l’aide des profils de test, des tests de rendu des e-mails, des évaluations du score de spam, etc.

[Explorer la section Prévisualiser et tester le contenu](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=fr)

Workflows d’approbation des parcours et des campagnes

Découvrez comment configurer, gérer et exécuter des processus d’approbation pour assurer le contrôle qualité des parcours et des campagnes.

[Découvrir les workflows d’approbation](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=fr)

Tester votre parcours

Validez votre parcours avant de le publier en le testant avec des profils spécifiques pour vous assurer que les événements, conditions et actions fonctionnent comme prévu. Disponible pour les brouillons de parcours qui utilisent un espace de noms.

[Tester votre parcours](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=fr)

Test à blanc du parcours

Effectuez un test à blanc pour simuler et valider le chemin d’exécution de votre parcours, ce qui permet d’identifier les problèmes potentiels avant l’activation.

[En savoir plus sur le test à blanc des parcours](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

Surveillance et dépannage

Accédez à un ensemble complet de ressources de dépannage, d’alertes système et de codes d’erreur pour résoudre les problèmes d’exécution et de performances des parcours.

[Afficher la surveillance et le dépannage](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg?lang=fr)

Terrain de jeu de personnalisation

Testez les expressions de personnalisation dans un environnement sécurisé. Testez le code avec des données d’exemple et prévisualisez les résultats avant de l’appliquer à vos campagnes et parcours.

[En savoir plus sur le terrain de jeu de personnalisation](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

Expériences de contenu et tests A/B

Optimisez vos campagnes en testant plusieurs variations de contenu et en mesurant les performances pour identifier les traitements les plus performants. Disponible pour les campagnes uniquement (expériences A/B et de bandit manchot prises en charge).

[En savoir plus sur les expériences de contenu](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

Listes de contrôle pour la surveillance des parties prenantes

Incluez automatiquement les adresses des parties prenantes internes dans les diffusions pour surveiller les messages réels envoyés aux clientes et clients pour l’assurance qualité et la conformité. Disponible uniquement pour le canal E-mail.

[Configurer les listes de contrôle](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=fr)

Détection des conflits

Identifiez les chevauchements potentiels entre les campagnes et les parcours afin d’éviter de submerger les clientes et clients avec trop de communications simultanées. Disponible pour les campagnes et les parcours unitaires, de qualification d’audience et de lecture d’audience.

[Détecter les conflits](../using/conflict-prioritization/conflicts.md)
:::

::::

## Importance des tests et de l’approbation

Les processus de test et d’approbation constituent des points de contrôle qualité essentiels pour protéger la réputation de votre marque et assurer le succès de la campagne. Voici pourquoi ils sont importants :

* **Détecter les erreurs avant qu’elles n’atteignent les clientes et clients** : identifiez les liens rompus, une personnalisation incorrecte, les problèmes de rendu et les erreurs de logique dans un environnement contrôlé où les correctifs sont rapides et sans risque.

* **Améliorer la délivrabilité** : testez les scores de spam, validez l’authentification des e-mails et vérifiez le rendu sur les clients de messagerie pour optimiser le placement dans les boîtes de réception et les taux d’engagement.

* **Garantir la cohérence de la marque** : prévisualisez le contenu avec différents profils de test pour vérifier que la personnalisation s’affiche correctement pour divers segments de clientèle et respecte les normes de la marque.

* **Valider les parcours complexes** : simulez des flux de parcours à plusieurs étapes pour vérifier que les déclencheurs fonctionnent correctement, que les conditions sont évaluées correctement et que les clientes et clients reçoivent les messages appropriés au bon moment.

* **Établir la responsabilité** : implémentez des workflows d’approbation officiels qui nécessitent l’approbation des parties prenantes, créant une responsabilité claire et réduisant les lancements de campagnes non autorisés ou prématurés.

* **Économiser du temps et des ressources** : détectez les problèmes dès le début du cycle de développement lorsque les correctifs sont moins coûteux et plus rapides, afin d’éviter des corrections post-lancement coûteuses ou des remontées d’informations du service clientèle.

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

**Pour toutes les campagnes :**

* Prévisualiser et tester le contenu à l’aide de [profils de test](../using/content-management/test-profiles.md) ou d’[exemples de données d’entrée](../using/test-approve/simulate-sample-input.md)
* Vérifier le [rendu des e-mails](../using/content-management/rendering.md) sur les appareils et les clients (canal E-mail uniquement)
* Exécuter des [contrôles du score de spam](../using/content-management/spam-report.md) (canal E-mail uniquement)
* Rechercher des [conflits](../using/conflict-prioritization/conflicts.md) avec d’autres campagnes et parcours
* Configurer des [listes de contrôle](../using/configuration/seed-lists.md) pour la surveillance des parties prenantes (canal E-mail uniquement)
* Envoyer pour [approbation](../using/test-approve/gs-approval.md) avant l’activation

**Pour les tests A/B et l’optimisation :**

* Créer des [expériences de contenu](../using/content-management/get-started-experiment.md) pour tester plusieurs traitements et mesurer les performances

**Pour les campagnes déclenchées par API :**

* Utiliser l’[API Campaign Simulation](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} pour déclencher des traitements de BAT par programme

>[!TAB Test de parcours]

**Pour tous les parcours :**

* Utiliser le [mode test](../using/building-journeys/testing-the-journey.md) pour simuler la progression du profil (brouillons de parcours uniquement, espace de noms requis) ou un [test à blanc](../using/building-journeys/journey-dry-run.md) pour analyser les chemins d’exécution sans envoyer de messages
* Tester des messages individuels à l’aide de la [prévisualisation et de BAT](../using/content-management/preview-test.md)
* Rechercher des [conflits](../using/conflict-prioritization/conflicts.md) avec d’autres parcours et campagnes
* Envoyer pour [approbation](../using/test-approve/gs-approval.md) avant publication

**Pour les parcours complexes :**

* Utiliser le mode test et le test à blanc ensemble pour valider de manière approfondie la logique de branchement et les chemins d’exécution
* Tester systématiquement différentes conditions d’entrée et attributs de profil

**Remarque :** la détection des conflits et la limitation des parcours sont disponibles uniquement pour les parcours unitaires, de qualification d’audience et de lecture d’audience.

>[!TAB Test de la personnalisation]

**Avant de créer du contenu :**

* Tester le [terrain de jeu de personnalisation](../using/personalization/personalize.md#playground) pour apprendre la syntaxe et tester des expressions avec des données d’exemple

**Lors de la création du contenu :**

* Prévisualiser avec des [profils de test](../using/content-management/test-profiles.md) pour valider correctement les rendus de personnalisation
* Tester plusieurs scénarios à l’aide d’[exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) provenant de fichiers CSV/JSON (30 variantes prises en charge)

>[!ENDTABS]

## Bonnes pratiques en matière de test

Pour maximiser l’efficacité de vos efforts de test, suivez ces pratiques recommandées :

1. **Tester tôt et souvent** : n’attendez pas qu’une campagne soit entièrement créée. Testez le contenu, la personnalisation et la logique de manière progressive au fur et à mesure que vous développez.

1. **Utiliser des profils de test réalistes** : [créez des profils de test](../using/audience/creating-test-profiles.md) qui représentent précisément vos segments d’audience cible, y compris les cas Edge et les différents scénarios de personnalisation.

1. **Tester sur les appareils et les clients** : vérifiez le [rendu des e-mails](../using/content-management/rendering.md) sur les clients de messagerie les plus courants (Gmail, Outlook, Apple Mail) et les appareils (ordinateur, téléphone mobile, tablette) pour garantir un affichage cohérent (canal E-mail uniquement).

1. **Valider minutieusement la personnalisation** : effectuez des tests avec plusieurs [profils de test](../using/content-management/test-profiles.md) dont les valeurs d’attribut sont différentes pour confirmer le bon rendu des jetons de personnalisation et le fonctionnement des valeurs de secours. Utilisez le [terrain de jeu de personnalisation](../using/personalization/personalize.md#playground) pour tester les expressions de personnalisation et le code avec des données d’exemple avant de les appliquer à vos campagnes.

1. **Tester les variations de contenu avec des données d’exemple** : utilisez des [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) à partir de fichiers CSV ou JSON pour tester jusqu’à 30 scénarios de personnalisation sans créer de nombreux profils de test, ce qui vous permet de gagner du temps tout en assurant une couverture complète. Prend en charge les canaux E-mail, SMS, Notification push, Web, Expérience basée sur du code, In-app et Cartes de contenu.

1. **Utiliser des listes de contrôle pour la surveillance des parties prenantes** : configurez des [listes de contrôle](../using/configuration/seed-lists.md) pour inclure automatiquement les parties prenantes internes qui recevront des copies de toutes les diffusions au moment de l’exécution à des fins de surveillance de la qualité et de vérification de la conformité (canal E-mail uniquement).

1. **Simuler des chemins de parcours** : pour les parcours complexes comportant plusieurs branches, utilisez le [mode test](../using/building-journeys/testing-the-journey.md) pour tester différentes conditions d’entrée et attributs de profil afin de valider tous les chemins possibles. Disponible pour les brouillons de parcours qui utilisent un espace de noms.

1. **Vérifier les indicateurs de délivrabilité** : examinez les [scores de spam](../using/content-management/spam-report.md), le statut d’authentification et les mesures d’intégrité des e-mails avant les envois volumineux (canal E-mail uniquement).

1. **Documenter les résultats des tests** : conservez les enregistrements des résultats des tests, des problèmes détectés et des résolutions pour améliorer les futurs processus de test et partagez les enseignements avec votre équipe.

1. **Impliquer rapidement les parties prenantes** : partagez les aperçus et les résultats des tests avec les parties prenantes avant l’[approbation formelle](../using/test-approve/gs-approval.md) afin de recueillir les commentaires et d’harmoniser les attentes.

## Workflow de test recommandé

Suivez cette approche en 4 phases pour valider vos campagnes et parcours avant le lancement :

| Phase | Éléments à tester | Actions clés |
|-------|-------------|-------------|
| **1. Validation du contenu** | Personnalisation, conception, rendu | [Prévisualiser avec des profils de test](../using/content-management/preview-test.md), tester [plusieurs variations](../using/test-approve/simulate-sample-input.md) avec CSV/JSON, vérifier le [rendu](../using/content-management/rendering.md) sur différents appareils |
| **2. Contrôles techniques** | Délivrabilité, liens, conflits | Exécuter les [contrôles de score de spam](../using/content-management/spam-report.md), valider les liens, rechercher des [conflits](../using/conflict-prioritization/conflicts.md) avec d’autres campagnes |
| **3. Logique de parcours** (parcours uniquement) | Conditions d’entrée, flux, embranchement | Utiliser le [mode test](../using/building-journeys/testing-the-journey.md) pour simuler la progression, exécuter un [test à blanc](../using/building-journeys/journey-dry-run.md) pour les chemins complexes |
| **4. Pré-lancement** | Paramètres, approbations, surveillance | Envoyer pour [approbation](../using/test-approve/gs-approval.md), vérifier les plannings et les audiences, activer les [alertes](../using/reports/alerts.md) |

**Conseil professionnel :** commencez par le [terrain de jeu de personnalisation](../using/personalization/personalize.md#playground) pour tester les expressions avant de créer du contenu et vérifiez toujours la [détection de conflits](../using/conflict-prioritization/conflicts.md) avant le lancement pour éviter une sur-sollicitation.

## Tests en action : cas d’utilisation

Découvrez comment les concepts de test s’appliquent aux scénarios réels :

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="Envoyer des messages multicanaux" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>Envoyer des messages multicanaux</strong></a>
</div>
<p>
Testez un parcours qui combine la lecture d’audience, les événements de réaction et les e-mails/messages push. Validez l’ensemble du flux, depuis le ciblage de l’audience jusqu’à la diffusion des messages. Concentrez-vous sur la coordination multicanal, les événements de réaction, la validation du flux de bout en bout et les étapes de test/publication.
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="Envoyer un message aux personnes abonnées" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>Envoyer un message aux personnes abonnées</strong></a>
</div>
<p>
Testez des parcours qui ciblent les listes d’abonnements avec un adressage dynamique des e-mails. Validez les expressions de personnalisation pour un ciblage correct des personnes abonnées. Concentrez-vous sur les expressions de personnalisation, l’adressage dynamique et le ciblage des listes d’abonnements.
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="Envoyer des messages selon des conditions temporelles" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>Envoyer des messages selon des conditions temporelles</strong></a>
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
<a href="../using/building-journeys/jo-use-cases.md"><strong>Explorer d’autres cas d’utilisation de parcours</strong></a>
</div>
<p>
Accédez à un ensemble complet d’exemples pratiques couvrant les événements d’expérience, les messages multicanaux et les intégrations systèmes externes. Explorez divers scénarios, modèles avancés et approches de test d’intégration.
</p>
</td>
</tr></table>

## Terminologie clé

Familiarisez-vous avec ces concepts de test essentiels pour mieux comprendre les fonctionnalités de test et d’approbation de Journey Optimizer. Chaque terme renvoie à une documentation détaillée.

**[Profils de test](../using/content-management/test-profiles.md)** : profils de clientes et clients synthétiques (et non clientes et clients réels) utilisés pour prévisualiser du contenu personnalisé. Signalé dans le service de profil client en temps réel. Obligatoire pour le mode test et la prévisualisation du contenu. [En savoir plus sur la création de profils de test](../using/audience/creating-test-profiles.md)

**[Mode test](../using/building-journeys/testing-the-journey.md)** : fonctionnalité de simulation de parcours qui envoie des profils de test par le biais de chemins de parcours. Limites : brouillons de parcours uniquement, espace de noms requis, profils de test uniquement. [Voir la documentation sur le mode test](../using/building-journeys/testing-the-journey.md)

**[Test à blanc](../using/building-journeys/journey-dry-run.md)** : outil d’analyse d’exécution de parcours qui effectue le suivi des chemins sans envoyer de messages ni effectuer d’appels API. Cas d’utilisation : valider la logique sans consommer de ressources. [En savoir plus sur le test à blanc](../using/building-journeys/journey-dry-run.md)

**[Exemples de données d’entrée](../using/test-approve/simulate-sample-input.md)** : fichiers CSV ou JSON contenant des valeurs d’attribut de profil pour tester la personnalisation. Prend en charge jusqu’à 30 variantes. Alternative à la création de profils de test. [Simuler des variations de contenu](../using/test-approve/simulate-sample-input.md)

**[Listes de contrôle](../using/configuration/seed-lists.md)** : adresses e-mail des parties prenantes internes automatiquement incluses dans les diffusions réelles (et non les envois de test). Canal E-mail uniquement. Cas d’utilisation : surveillance de la qualité et conformité. [Configurer des listes de contrôle](../using/configuration/seed-lists.md)

**[Expériences de contenu](../using/content-management/get-started-experiment.md)** : tests A/B ou expériences de bandit manchot comparant des variations de contenu. Campagnes uniquement, non disponible dans les parcours. [Commencer avec les expériences](../using/content-management/get-started-experiment.md) | [Créer des expériences](../using/content-management/content-experiment.md)

**[BAT](../using/content-management/proofs.md)** : testez les diffusions par e-mail envoyées à des adresses e-mail spécifiques à l’aide des données de profil de test. Différent des listes de contrôle (les BAT sont des envois de test manuels, les listes de contrôle sont des copies automatiques des parties prenantes). [Envoyer des BAT](../using/content-management/proofs.md)

**[Détection de conflits](../using/conflict-prioritization/conflicts.md)** : outil qui identifie les campagnes et les parcours qui se chevauchent et ciblent les mêmes audiences. Prise en charge limitée des parcours : types unitaires, de qualification d’audience et de lecture d’audience uniquement. [En savoir plus sur la gestion des conflits](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Workflows d’approbation](../using/test-approve/gs-approval.md)** : processus de révision en plusieurs étapes nécessitant l’approbation des parties prenantes avant activation. Nécessite la configuration de politiques d’approbation. [Configurer les approbations](../using/test-approve/gs-approval.md) | [Créer des politiques](../using/test-approve/approval-policies.md)

**[Tests de rendu](../using/content-management/rendering.md)** : validation de l’affichage des e-mails sur les clients de messagerie (Gmail, Outlook, Apple Mail) et les appareils. Nécessite l’intégration de Litmus. [Tester le rendu des e-mails](../using/content-management/rendering.md)

**[Terrain de jeu de personnalisation](../using/personalization/personalize.md#playground)** : environnement d’apprentissage interactif pour tester la syntaxe de personnalisation et des expressions de test avec des données d’exemple. Aucun jeu de données actif n’est requis. [Accéder au terrain de jeu](../using/personalization/personalize.md#playground)

## Ressources supplémentaires

>[!BEGINTABS]

>[!TAB Guides essentiels]

* [Simuler des variations de contenu](../using/test-approve/simulate-sample-input.md) : testez jusqu’à 30 scénarios de personnalisation à l’aide de fichiers CSV ou JSON. Idéal pour les tests de contenu multilingue sans créer plusieurs profils de test. Prend en charge les expériences d’e-mails, de SMS, de notifications push, web, basées sur du code, in-app et de cartes de contenu.

* [Créer des profils de test](../using/audience/creating-test-profiles.md) : créez et gérez des profils de test pour simuler des scénarios clients. Découvrez comment marquer les profils pour les tests, définir des attributs et organiser les segments de test.

* [Rapport sur les spams](../using/content-management/spam-report.md) : vérifiez le score de spam avant l’envoi pour améliorer la délivrabilité et le placement dans les boîtes de réception. Obtenez des recommandations exploitables pour l’optimisation du contenu.

* [Questions fréquentes sur les parcours](../using/building-journeys/journey-faq.md) : référence rapide pour les questions fréquentes sur le test, l’exécution et le dépannage de parcours.

>[!TAB Dépendances et relations]

Découvrez comment les fonctionnalités de test sont reliées entre elles et à vos workflows Journey Optimizer. Cette section mappe les conditions préalables, les dépendances en amont/en aval et les combinaisons de fonctionnalités courantes.

+++**Conditions préalables (requises avant le test)**

* Les profils de test doivent être créés avant d’utiliser le mode test ou l’aperçu de contenu.
* Les politiques d’approbation doivent être configurées avant l’envoi pour approbation.
* Les listes de contrôle doivent être créées avant d’être ajoutées aux campagnes/parcours.
* L’intégration de Litmus est requise pour les tests de rendu des e-mails.
* Le parcours doit être à l’état de brouillon pour utiliser le mode test.
* L’espace de noms du parcours doit être configuré pour utiliser le mode test.

+++

+++**Éléments dont dépendent les tests (en amont)**

* Création de contenu : campagnes ou parcours à tester nécessaires
* Profils de test : requis pour le mode test et l’aperçu du contenu
* Politiques d’approbation : obligatoires pour les workflows d’approbation
* Configuration : configurations de canal, authentification des e-mails, paramètres de domaine.

+++

+++**Éléments dont dépendent les tests (en aval)**

* Activation de la campagne ou du parcours : activation impossible sans résoudre les erreurs
* Publication : une approbation peut être requise avant la publication.
* Surveillance en direct : surveillance et reporting après le lancement
* Optimisation : utilisez les résultats des tests pour affiner les campagnes futures.

+++

+++**Fonctionnalités associées**

* Workflows de test et d’approbation : processus d’assurance qualité
* Tests et détection des conflits : prévention de la sursollicitation des clientes et clients
* Tests et expériences de contenu : optimisation des performances
* Tests et reporting : cycle d’amélioration continue
* Profils de test et personnalisation : validation du contenu
* Test à blanc et mode test : validation complète du parcours

+++

+++**Combinaisons de fonctionnalités courantes**

* Tests de contenu : profils de test + exemples de données d’entrée + terrain de jeu de personnalisation
* Validation des e-mails : tests du rendu + scores de spam + profils de test + BAT
* Validation des parcours : mode test + test à blanc + profils de test
* Liste de contrôle avant lancement : tous les tests techniques + détection des conflits + workflows d’approbation

+++

>[!TAB Questions courantes]

+++**Q : quels sont les tests requis avant de lancer une campagne ?**

**Minimum :** aperçu du contenu avec profils de test + vérification du score de spam (e-mail)
**Recommandation :** + rendu des e-mails + détection des conflits + workflow d’approbation
**Bonne pratique :** + test d’exemples de données d’entrée + listes de contrôle + expérience A/B (si optimisation)

+++

+++**Q : comment tester la personnalisation sans créer de nombreux profils de test ?**

**Solution principale :** utilisez des [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) avec des fichiers CSV/JSON (30 variantes prises en charge).
**Alternative :** créez 3 à 5 [profils de test](../using/audience/creating-test-profiles.md) représentatifs couvrant les segments clés.
**Outil d’apprentissage :** expérimentez d’abord dans le [terrain de jeu de personnalisation](../using/personalization/personalize.md#playground).

+++

+++**Q : Quelle est la différence entre le mode test et le test à blanc pour les parcours ?**

**Mode test :** envoie des profils de test par le biais du parcours, déclenche des actions réelles et génère des messages de test. Nécessite un brouillon de parcours + un espace de noms.
**Test à blanc :** effectue le suivi des chemins d’exécution sans rien envoyer. Fonctionne avec n’importe quel statut de parcours. Aucun message envoyé, aucune action exécutée.
**À utiliser ensemble :** mode test pour le test des messages + test à blanc pour la validation de la logique : couverture complète.

+++

+++**Q : puis-je tester les parcours en production/actifs ?**

**Mode test :** non, uniquement les brouillons de parcours.
**Test à blanc :** oui, fonctionne quel que soit le statut du parcours.
**Aperçu du contenu :** oui, prévisualisez des messages individuels à tout moment.
**Solution :** dupliquez le parcours actif en mode brouillon pour la validation du mode test complet.

+++

+++**Q : quelles fonctionnalités de test nécessitent des intégrations externes ?**

**Rendu des e-mails :** nécessite l’intégration de Litmus (licence distincte).
**Toutes les autres :** intégrées à Journey Optimizer, aucune intégration supplémentaire requise
**Remarque :** les profils de test nécessitent le service de profil client en temps réel (inclus).

+++

+++**Q : comment tester les campagnes déclenchées par API ?**

**Option 1 :** utilisez l’[API Campaign Simulation](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} pour les tests programmatiques.
**Option 2 :** prévisualisez le contenu avec des profils de test dans l’interface d’utilisation.
**Option 3 :** envoyez des BAT pour tester les adresses e-mail.
**Bonne pratique :** combinez les trois pour une validation complète.

+++

>[!ENDTABS]
