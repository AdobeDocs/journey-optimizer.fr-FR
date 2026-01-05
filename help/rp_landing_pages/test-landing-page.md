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
source-git-commit: fb13aee243757de7fe47bdd9d9ebad47069e24ba
workflow-type: tm+mt
source-wordcount: '3103'
ht-degree: 5%

---

# Tester, valider et approuver{#section-overview}

Cette section couvre toutes les fonctionnalités de test et d’approbation de Journey Optimizer. Vous y trouverez des outils pour prévisualiser le contenu avec des profils de test, valider la logique de parcours, vérifier le rendu des e-mails et les scores de spam, exécuter des expériences A/B, détecter des conflits et configurer des workflows d’approbation.

Cette page de destination vous aide à choisir la bonne approche de test en fonction de ce que vous créez (campagnes ou parcours), vous guide tout au long des workflows de test recommandés et fournit un accès rapide à toutes les ressources de test et d’approbation. Commencez par [Choisir votre approche de test](#choose-your-testing-approach) ci-dessous pour identifier les outils qui s’appliquent à votre cas d’utilisation.

## Présentation des fonctionnalités de test

**Types de test disponibles :**

* Tests de contenu : prévisualisez et validez le contenu du message avant l’envoi → [Test des campagnes](#testing-campaigns), [Test de la personnalisation](#testing-personalization)
* Test de la logique de parcours : Simuler la progression du client par le biais de chemins de parcours → [Test des parcours &#x200B;](#testing-journeys)
* Tests techniques : validation du rendu, de la délivrabilité et de l’authentification → [&#x200B; Validation technique](#2-technical-validation)
* Tests de performance : comparaison des variations de contenu à l’aide d’expériences A/B → [expériences de contenu](#content-experiments--ab-testing)
* Test des conflits : détecter les chevauchements de campagnes et de parcours → [détection des conflits](#conflict-detection)
* Tests d’approbation : workflows de révision structurés avant activation → [workflows d’approbation](#approval-workflows-for-journeys-and-campaigns)

**Fonctionnalités clés par contexte :**

| Fonctionnalité | Application | Restrictions de canal | Conditions préalables | objectif du Principal | Documentation |
|------------|-----------|---------------------|--------------|-----------------|---------------|
| [Profils de test](../using/content-management/test-profiles.md) | Campagnes, Parcours | Tous les canaux | Profils de test créés | Prévisualiser du contenu personnalisé | [Guide](#testing-campaigns) |
| [Exemple de données d’entrée](../test-approve/simulate-sample-input.md) | Campagnes, Parcours | E-mail, SMS, notification push, web, basé sur le code, in-app, cartes de contenu | Fichier CSV/JSON | Test de plusieurs variantes de personnalisation | [Guide](#simulate-content-variations) |
| [Mode Test](../using/building-journeys/testing-the-journey.md) | Parcours uniquement | S/O | Brouillon de parcours, espace de noms configuré | Simuler la progression d’un profil | [Carte](#test-your-journey) |
| [&#x200B; Exécution d’essai &#x200B;](../using/building-journeys/journey-dry-run.md) | Parcours uniquement | S/O | Parcours créé | Analyse des chemins d’exécution | [Carte](#journey-dry-run) |
| [Rendu des e-mails](../using/content-management/rendering.md) | Campagnes, Parcours | E-mail uniquement | Intégration de Litmus | Vérification de l’affichage sur plusieurs clients | [Workflow](#2-technical-validation) |
| [Score de spam](../using/content-management/spam-report.md) | Campagnes, Parcours | E-mail uniquement | Aucune | Validation de la diffusion | [Workflow](#2-technical-validation) |
| [Listes de contrôle](../using/configuration/seed-lists.md) | Campagnes, Parcours | E-mail uniquement | Liste de contrôle configurée | Surveillance des parties prenantes | [Carte](#seed-lists-for-stakeholder-monitoring) |
| [&#x200B; Expériences de contenu &#x200B;](../using/content-management/get-started-experiment.md) | Campagnes uniquement | Tous les canaux | Aucune | Test A/B et bandit manchot | [Carte](#content-experiments--ab-testing) |
| [Détection des conflits](../using/conflict-prioritization/conflicts.md) | Campagnes, Parcours (limité) | Tous les canaux | Aucune | Empêcher les messages excessifs des clients | [Carte](#conflict-detection) |
| [Workflows d’approbation](../using/test-approve/gs-approval.md) | Campagnes, Parcours | Tous les canaux | Politique de validation créée | Processus d’examen structuré | [Carte](#approval-workflows-for-journeys-and-campaigns) |
| [Terrain de jeu Personalization](../using/personalization/personalize.md#playground) | Toutes | Tous les canaux | Aucune | Découvrir et tester la syntaxe de personnalisation | [Carte](#personalization-playground) |

**Workflows de test courants :**

1. Développement préalable : utilisez [terrain de jeu de personnalisation](#testing-personalization) pour apprendre la syntaxe
2. Pendant le développement : aperçu avec des [profils de test](#testing-campaigns), validation avec des [exemples de données d’entrée](#simulate-content-variations)
3. Prélancement : exécution [tests techniques](#2-technical-validation) (rendu, spam), vérification [conflits](#conflict-detection), envoi pour [approbation](#approval-workflows-for-journeys-and-campaigns).
4. Après le lancement : effectuez une surveillance à l’aide de rapports dynamiques (voir [Surveillance et dépannage](#monitoring--troubleshooting)), puis effectuez une itération en fonction des résultats


## Importance des tests et de l’approbation

Les processus de test et d’approbation constituent des points de contrôle qualité essentiels pour protéger la réputation de votre marque et assurer le succès de la campagne. Voici pourquoi ils sont importants :

* **Capturer les erreurs avant qu’elles n’atteignent les clients** - Identifiez les liens rompus, une personnalisation incorrecte, les problèmes de rendu et les défauts logiques dans un environnement contrôlé où les correctifs sont rapides et sans risque.

* **Améliorer la délivrabilité** - Testez les scores de spam, validez l’authentification des e-mails et vérifiez le rendu sur les clients de messagerie pour optimiser l’emplacement des boîtes de réception et les taux d’engagement.

* **Garantir la cohérence de la marque** - Prévisualisez le contenu avec différents profils de test pour vérifier que la personnalisation s’affiche correctement pour divers segments de clientèle et respecte les normes de la marque.

* **Validation de parcours complexes** - Simulez des flux de parcours à plusieurs étapes pour vérifier que les déclencheurs se déclenchent correctement, que les conditions s’évaluent correctement et que les clients reçoivent les messages appropriés au bon moment.

* **Établissement de la responsabilité** - Implémentez des workflows d’approbation officiels qui nécessitent l’approbation des parties prenantes, créant une propriété claire et réduisant les lancements de campagnes non autorisés ou prématurés.

* **Gagnez du temps et économisez des ressources** - Détectez les problèmes dès le début du cycle de développement lorsque les correctifs sont moins coûteux et plus rapides, afin d’éviter des corrections post-lancement coûteuses ou des remontées d’informations du service client.

## Terminologie clé

**[Profils de test](../using/content-management/test-profiles.md)** = profils clients synthétiques (et non réels) utilisés pour prévisualiser le contenu personnalisé. Signalé dans le service de profil client en temps réel. Obligatoire pour le mode test et la prévisualisation du contenu. [Découvrez comment créer des profils de test.](../using/audience/creating-test-profiles.md)

**[Mode test](../using/building-journeys/testing-the-journey.md)** = fonction de simulation de Parcours qui envoie des profils de test par le biais de chemins de parcours. Limites : parcours de brouillon uniquement, espace de noms requis, profils de test uniquement. [Voir la documentation sur le mode test](../using/building-journeys/testing-the-journey.md)

**[Exécution d’essai](../using/building-journeys/journey-dry-run.md)** = outil d’analyse d’exécution de Parcours qui effectue le suivi des chemins sans envoyer de messages ni effectuer d’appels API. Cas d’utilisation : validation de la logique sans consommer de ressources. [En savoir plus sur l’essai](../using/building-journeys/journey-dry-run.md)

**[Exemples de données d’entrée](../test-approve/simulate-sample-input.md)** = fichiers CSV ou JSON contenant des valeurs d’attribut de profil pour tester la personnalisation. Prend en charge jusqu’à 30 variantes. Alternative à la création de profils de test. [Comment simuler des variations de contenu &#x200B;](../test-approve/simulate-sample-input.md)

**[Listes de contrôle](../using/configuration/seed-lists.md)** = adresses e-mail des parties prenantes internes automatiquement incluses dans les diffusions réelles (et non les envois de test). Canal e-mail uniquement. Cas pratique : surveillance de la qualité et conformité. [Configuration des listes de contrôle](../using/configuration/seed-lists.md)

**[Expériences de contenu](../using/content-management/get-started-experiment.md)** = tests A/B ou expériences de bandit à plusieurs bras comparant les variations de contenu. Campagnes uniquement, non disponible dans les parcours. [Prise en main des expériences](../using/content-management/get-started-experiment.md) | [Création d’expériences](../using/content-management/content-experiment.md)

**[BAT](../using/content-management/proofs.md)** = Tester les diffusions par e-mail envoyées à des adresses e-mail spécifiques à l’aide des données de profil de test. Différent des listes de contrôle (les BAT sont des envois de test manuels, les listes de contrôle sont des copies automatiques des parties prenantes). [Envoi de BAT](../using/content-management/proofs.md)

**[Détection des conflits](../using/conflict-prioritization/conflicts.md)** = Outil qui identifie les campagnes et les parcours qui se chevauchent et ciblent les mêmes audiences. Prise en charge limitée des parcours : unitaire, qualification d’audience et lecture d’audience uniquement. [En savoir plus sur la gestion des conflits &#x200B;](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Workflows d’approbation](../using/test-approve/gs-approval.md)** = processus de révision en plusieurs étapes nécessitant l’approbation des parties prenantes avant activation. Nécessite la configuration d’une politique d’approbation. [Configurer les validations](../using/test-approve/gs-approval.md) | [Créer des politiques](../using/test-approve/approval-policies.md)

**[Tests de rendu](../using/content-management/rendering.md)** = validation de l’affichage des e-mails sur les clients de messagerie (Gmail, Outlook, Apple Mail) et les appareils. Nécessite l’intégration de Litmus. [Tester le rendu des e-mails](../using/content-management/rendering.md)

**[Terrain de jeu Personalization](../using/personalization/personalize.md#playground)** = environnement d’apprentissage interactif pour tester la syntaxe de personnalisation et des expressions de test avec des exemples de données. Aucun jeu de données actif n’est requis. [Accédez au terrain de jeu](../using/personalization/personalize.md#playground)

## Arborescence de décision pour la sélection de la méthode de test

Utilisez cette arborescence de décision pour identifier rapidement les outils de test appropriés à votre scénario spécifique. Répondez à chaque question en fonction de votre contexte (ce que vous créez, ce que vous devez valider et quel canal vous utilisez) pour accéder directement aux fonctionnalités et à la documentation appropriées.

+++ **Question 1 : Qu’est-ce que vous testez**

* Campagne → [Test des campagnes](#testing-campaigns)
* Parcours → [Test des parcours &#x200B;](#testing-journeys)
* Expressions de Personalization → [terrain de jeu Personalization](#testing-personalization)
+++

+++**Question 2 : Quel aspect doit être validé ?**

* Contenu et personnalisation → [Profils de test](#testing-campaigns) ou [exemples de données d’entrée](#simulate-content-variations)
* Affichage des e-mails → [tests de rendu des e-mails](#2-technical-validation)
* Délivrabilité → [contrôles du score de spam](#2-technical-validation)
* Logique et flux du parcours → [mode Test](#testing-journeys) ou [exécution à sec](#journey-dry-run)
* Comparaison des performances → [Expérience de contenu](#content-experiments--ab-testing) (campagnes uniquement)
* Conflits de minutage → [détection des conflits](#conflict-detection)
* Révision par les parties prenantes → [workflow d’approbation](#approval-workflows-for-journeys-and-campaigns)
+++

+++**Question 3 : Quel canal ?**

* E-mail → toutes les méthodes de test disponibles (voir [Test des campagnes](#testing-campaigns))
* SMS, notification push → [test de contenu](#testing-campaigns), [exemples de données d’entrée](#simulate-content-variations), [workflows d’approbation](#approval-workflows-for-journeys-and-campaigns)
* Web, in-app, basé sur du code → [test de contenu](#testing-campaigns), [exemples de données d’entrée](#simulate-content-variations), [workflows d’approbation](#approval-workflows-for-journeys-and-campaigns)
* Plusieurs canaux → Tester chaque canal séparément
+++

+++**Question 4 : À quel moment dans le workflow ?**

* Avant de créer → [terrain de jeu Personalization](#personalization-playground) pour l&#39;apprentissage
* Lors de la création de → [Profils de test](#testing-campaigns) et [données d’entrée d’exemple](#simulate-content-variations) pour la validation
* Avant le lancement → [Rendu des tests](#2-technical-validation), [vérifications de spam](#email-spam-report), [détection de conflit](#conflict-detection), [approbations](#approval-workflows-for-journeys-and-campaigns)
* Après le lancement → [Rapports dynamiques](../using/building-journeys/report-journey.md) et [surveillance](#monitoring--troubleshooting)
+++


## Choisir votre approche de test

La bonne approche de test dépend de ce que vous créez et de ce que vous devez valider. Utilisez ce guide pour identifier les outils de test les plus pertinents pour votre scénario.

### Tester des campagnes

**Pour toutes les campagnes :**

* Prévisualiser et tester le contenu à l’aide de [profils de test](../using/content-management/test-profiles.md) ou [exemples de données d’entrée](../test-approve/simulate-sample-input.md)
* Vérifier le [rendu des e-mails](../using/content-management/rendering.md) sur les appareils et les clients (canal e-mail uniquement)
* Exécuter [contrôles du score de spam](../using/content-management/spam-report.md) (canal e-mail uniquement)
* Vérification [conflits](../conflict-prioritization/conflicts.md) avec d’autres campagnes et parcours
* Configurer des [listes de contrôle](../configuration/seed-lists.md) pour la surveillance des parties prenantes (canal e-mail uniquement)
* Envoyer pour [approbation](../using/test-approve/gs-approval.md) avant l’activation

**Pour les tests A/B et l’optimisation :**

* Créez des [expériences de contenu](../using/content-management/get-started-experiment.md) pour tester plusieurs traitements et mesurer les performances

**Pour les campagnes déclenchées par API :**

* Utilisez l’[API de simulation Campaign](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} pour déclencher des tâches de BAT par programmation

### Test des parcours

**Pour tous les parcours :**

* Utilisez [mode test](../using/building-journeys/testing-the-journey.md) pour simuler la progression du profil (les brouillons de parcours uniquement, nécessitent un espace de noms) ou [exécution d’essai](../using/building-journeys/journey-dry-run.md) pour analyser les chemins d’exécution sans envoyer de messages
* Tester des messages individuels à l’aide de [prévisualisation et BAT](../using/content-management/preview-test.md)
* Cochez la case [conflits](../conflict-prioritization/conflicts.md) avec d’autres parcours et campagnes.
* Envoyer pour [approbation](../using/test-approve/gs-approval.md) avant publication

**Pour les parcours complexes :**

* Utilisez le mode test et l’exécution d’essai ensemble pour valider minutieusement la logique de branchement et les chemins d’exécution
* Testez systématiquement différentes conditions d’entrée et attributs de profil

**Remarque :** la détection des conflits et la limitation des parcours sont disponibles pour les parcours unitaires, de qualification d’audience et de lecture d’audience uniquement.

### Test de la personnalisation

**Avant de créer du contenu :**

* Testez le [terrain de jeu de la personnalisation](../using/personalization/personalize.md#playground) pour apprendre la syntaxe et tester des expressions avec des exemples de données

**Lors de la création du contenu :**

* Aperçu avec des [profils de test](../using/content-management/test-profiles.md) pour valider correctement les rendus de personnalisation
* Tester plusieurs scénarios à l’aide de [exemples de données d’entrée](../test-approve/simulate-sample-input.md) provenant de fichiers CSV/JSON (prend en charge jusqu’à 30 variantes)

## Bonnes pratiques de test

Pour optimiser l’efficacité de vos efforts de test, suivez ces pratiques recommandées :

1. **Testez tôt et souvent** - N’attendez pas qu’une campagne soit entièrement créée. Testez le contenu, la personnalisation et la logique de manière progressive au fur et à mesure que vous développez.

1. **Utiliser des profils de test réalistes** - [Créez des profils de test](../using/audience/creating-test-profiles.md) qui représentent précisément vos segments d’audience cible, y compris les cas Edge et les différents scénarios de personnalisation.

1. **Test sur les appareils et les clients** - Vérifiez [le rendu des e-mails](../using/content-management/rendering.md) sur les clients de messagerie les plus courants (Gmail, Outlook, Apple Mail) et les appareils (bureau, mobile, tablette) pour garantir un affichage cohérent (canal e-mail uniquement).

1. **Valider entièrement la personnalisation** - Effectuez des tests avec plusieurs [profils de test](../using/content-management/test-profiles.md) dont les valeurs d’attribut sont différentes pour confirmer que les jetons de personnalisation s’affichent correctement et que les valeurs de secours fonctionnent. Utilisez le [terrain de jeu de la personnalisation](../using/personalization/personalize.md#playground) pour tester les expressions de personnalisation et le code avec des exemples de données avant de les appliquer à vos campagnes.

1. **Tester les variations de contenu avec des exemples de données** - Utilisez [exemples de données d’entrée](../test-approve/simulate-sample-input.md) à partir de fichiers CSV ou JSON pour tester jusqu’à 30 scénarios de personnalisation sans créer de nombreux profils de test, ce qui vous permet de gagner du temps tout en assurant une couverture complète. Prend en charge les canaux e-mail, SMS, notification push, web, expérience basée sur le code, in-app et cartes de contenu.

1. **Utiliser des listes de contrôle pour la surveillance des parties prenantes** - Configurez les [listes de contrôle](../configuration/seed-lists.md) pour inclure automatiquement les parties prenantes internes qui recevront des copies de toutes les diffusions au moment de l’exécution pour la surveillance de la qualité et la vérification de la conformité (canal e-mail uniquement).

1. **Simuler des chemins de parcours** - Pour les parcours complexes comportant plusieurs branches, utilisez [mode test](../using/building-journeys/testing-the-journey.md) pour tester différentes conditions d’entrée et attributs de profil afin de valider tous les chemins possibles. Disponible pour les brouillons de parcours qui utilisent un espace de noms.

1. **Vérifier les indicateurs de délivrabilité** - Examinez [les scores de spam](../using/content-management/spam-report.md), le statut d’authentification et les mesures d’intégrité des e-mails avant les envois volumineux (canal e-mail uniquement).

1. **Documenter les résultats des tests** - Conservez des enregistrements des résultats des tests, des problèmes détectés et des résolutions pour améliorer les futurs processus de test et partagez les enseignements avec votre équipe.

1. **Impliquez rapidement les parties prenantes** - Partagez les aperçus et les résultats des tests avec les parties prenantes avant l’[approbation formelle](../using/test-approve/gs-approval.md) afin de recueillir les commentaires et d’aligner les attentes.

## Workflow de test recommandé

Suivez cette approche systématique pour garantir des tests approfondis et des approbations fluides :

### &#x200B;1. Développement et prévisualisation du contenu

Commencez par créer votre contenu et par utiliser les fonctionnalités de prévisualisation pour vérifier la conception et la personnalisation initiales :

* Concevoir le contenu de votre [e-mail](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notification push](../using/push/create-push.md) ou d’un autre canal

* Utilisez la fonction **[Simuler du contenu](../using/content-management/preview-test.md)** pour prévisualiser avec des profils de test

* Cochez [jetons de personnalisation](../using/personalization/personalization-syntax.md), contenu dynamique et valeurs de secours

* Testez les expressions de personnalisation dans le **[terrain de jeu de la personnalisation](../using/personalization/personalize.md#playground)** pour tester et affiner votre code avec des exemples de données avant de l’appliquer au contenu en direct

* Testez plusieurs variations à l’aide de **[exemples de données d’entrée](../test-approve/simulate-sample-input.md)** provenant de fichiers CSV/JSON pour valider la personnalisation dans divers scénarios de profil

* Vérifier le [rendu](../using/content-management/rendering.md) sur différents formats d’écran et clients de messagerie

### &#x200B;2. Validation technique

Validez les aspects techniques ayant un impact sur la délivrabilité et les fonctionnalités :

* Exécutez [&#x200B; contrôles de score de spam &#x200B;](../using/content-management/spam-report.md) pour identifier les problèmes de délivrabilité potentiels

* Tester les liens pour s’assurer qu’ils ne sont pas rompus et effectuer correctement le suivi

* Valider la configuration [authentification par e-mail](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)

* Vérifier le rendu HTML et rechercher les problèmes de compatibilité CSS

* Test [responsive design](../using/email/content-from-scratch.md) sur les appareils mobiles et les ordinateurs de bureau

* Recherchez les [conflits potentiels](../conflict-prioritization/conflicts.md) avec d’autres campagnes et parcours pour éviter la fatigue des messages client et les problèmes de minutage

### &#x200B;3. Essais Parcours (parcours uniquement)

Si vous testez un parcours, validez la logique d’orchestration :

* Activez le **[mode Test](../using/building-journeys/testing-the-journey.md)** pour simuler la progression du profil tout au long du parcours

* Tester différentes [conditions d’entrée](../using/building-journeys/entry-management.md) et qualifications d’audience

* Vérifiez que [les activités d’attente](../using/building-journeys/wait-activity.md), [les conditions](../using/building-journeys/condition-activity.md) et la logique de branchement fonctionnent correctement

* Utilisez **[Exécution d’essai](../using/building-journeys/journey-dry-run.md)** pour les parcours complexes afin d’analyser les chemins d’exécution sans envoyer de messages

* Vérifiez que les [événements](../using/event/about-events.md) se déclenchent correctement et [actions personnalisées](../using/action/about-custom-action-configuration.md) s’exécutent comme prévu

### &#x200B;4. Soumission d’approbation

Une fois le test terminé et les problèmes résolus :

* Soumettez la campagne ou le parcours à validation conformément à la [politique de validation](../using/test-approve/approval-policies.md) de votre organisation

* Incluez les résultats du test et la documentation avec la [demande d’approbation](../using/test-approve/request-approval.md)

* Répondre à tout commentaire ou demande de modification de la part des [approbateurs](../using/test-approve/review-approve-request.md)

* Effectuez les révisions nécessaires et testez-les à nouveau si les modifications sont importantes.

### &#x200B;5. Vérification préalable au lancement

Avant d’activer votre campagne ou votre parcours :

* Effectuez une révision finale de tous les paramètres, audiences et [plannings](../using/building-journeys/journey-properties.md)

* Vérifier que toutes les approbations sont en place et documentées

* Vérifiez que les heures d’envoi et les [fuseaux horaires](../using/building-journeys/timezone-management.md) sont corrects.

* Activez la [&#x200B; surveillance et alertes &#x200B;](../using/reports/alerts.md) pour suivre les performances après le lancement

### &#x200B;6. Surveiller et itérer

Après le lancement, continuez la surveillance pour détecter rapidement tout problème :

* Configurer des [alertes système](../using/reports/alerts.md) pour les erreurs de parcours, les taux de rebond élevés ou un faible engagement

* Examinez les [rapports dynamiques](../using/building-journeys/report-journey.md) pour suivre les performances par rapport aux attentes

* Préparez-vous à [mettre en pause ou modifier](../using/building-journeys/journey-pause.md) les parcours en cas de problèmes critiques

* Documenter les leçons apprises pour améliorer les futurs processus de test

## Tests en action : cas d’utilisation

Découvrez comment les concepts de test s’appliquent aux scénarios réels :

| Exemple d’utilisation | Ce que vous apprendrez | Principales priorités en matière de test |
|----------|-------------------|-------------------|
| **[Envoyer des messages multicanaux](../using/building-journeys/journeys-uc.md)** | Testez un parcours qui combine la lecture d’audience, les événements de réaction et les e-mails/messages push. Validez l’ensemble du flux, du ciblage des audiences à la diffusion des messages. | Coordination multicanal, événements de réaction, validation du flux de bout en bout, étapes de test et de publication |
| **[Envoyer un message aux abonnés](../using/building-journeys/message-to-subscribers-uc.md)** | Testez des parcours qui ciblent les listes d’abonnements avec une adresse e-mail dynamique. Validez les expressions de personnalisation pour un ciblage correct des abonnés. | expressions Personalization, adressage dynamique, ciblage de liste d’abonnements |
| **[Envoyer des messages limités dans le temps](../using/building-journeys/weekday-email-uc.md)** | Testez des parcours avec des conditions temporelles pour vous assurer que les messages sont envoyés à des jours spécifiques. Validez les activités d’attente et la logique de planification. | Conditions temporelles, activités d’attente, validation de la planification |
| **[Explorer d’autres cas d’utilisation de parcours](../using/building-journeys/jo-use-cases.md)** | Accédez à une collection complète d’exemples pratiques couvrant les événements d’expérience, la messagerie multicanal et les intégrations système externes. | Divers scénarios, modèles avancés, tests d’intégration |

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
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Expériences de contenu et tests A/B

Optimisez vos campagnes en testant plusieurs variations de contenu et en mesurant les performances pour identifier les traitements les plus performants. Disponible pour les campagnes uniquement (prend en charge les expériences A/B et le bandit manchot).

[En savoir plus sur les expériences de contenu](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

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

## Ressources supplémentaires

### Guides de test et de validation essentiels

* [&#x200B; Simuler des variations de contenu &#x200B;](../test-approve/simulate-sample-input.md) - Testez jusqu’à 30 scénarios de personnalisation à l’aide de fichiers CSV ou JSON. Idéal pour les tests de contenu multilingue sans créer plusieurs profils de test. Prend en charge les e-mails, SMS, notifications push, web, basées sur le code, in-app et cartes de contenu.

* [Création de profils de test](../using/audience/creating-test-profiles.md) - Créez et gérez des profils de test pour simuler des scénarios client. Découvrez comment marquer les profils pour les tests, définir des attributs et organiser les segments de test.

* [Rapport sur les courriers indésirables](../using/content-management/spam-report.md) - Vérifiez les scores de spam avant l&#39;envoi pour améliorer la délivrabilité et le positionnement dans la boîte de réception. Obtenez des recommandations exploitables pour l’optimisation du contenu.

* [FAQ sur les Parcours &#x200B;](../using/building-journeys/journey-faq.md) - Référence rapide pour les questions courantes sur les tests de parcours, l’exécution et le dépannage.

### Dépendances et relations

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

* Workflows de test et d’approbation = processus d’assurance qualité
* Tests + détection des conflits = Prévention de la messagerie excessive des clients
* Tests + Expériences de contenu = Optimisation des performances
* Tests + reporting = cycle d’amélioration continue
* Profils de test + Personalization = Validation du contenu
* Exécution d’essai + Mode test = Validation complète du parcours

+++

+++**Combinaisons de fonctionnalités courantes**

* Tests de contenu : profils de test + exemples de données d’entrée + terrain de jeu Personalization
* Validation des e-mails : rendu des tests + scores de spam + profils de test + BAT
* Validation du parcours : Mode test + Exécution d’essai + Profils de test
* Liste de contrôle de prélancement : tous les tests techniques + détection des conflits + workflows d’approbation

+++

### Questions courantes

+++**Q : Quels sont les tests requis avant de lancer une campagne ?**

**Minimum :** aperçu du contenu avec profils de test + vérification du score de spam (email)
**Recommandé :** + Rendu des e-mails + Détection des conflits + Workflow d’approbation
**Bonne pratique :** + Test d’exemples de données d’entrée + Listes de contrôle + Expérience A/B (si optimisation)

+++

+++**Q : Comment tester la personnalisation sans créer de nombreux profils de test ?**

**Solution de Principal :** utilisez [exemples de données d’entrée](../test-approve/simulate-sample-input.md) avec des fichiers CSV/JSON (prend en charge jusqu’à 30 variantes)
**Alternative :** créez 3 à 5 profils de test représentatifs [profils de test](../using/audience/creating-test-profiles.md) couvrant les segments clés
**Outil d’apprentissage :** Expérimentez d’abord dans [terrain de jeu de personnalisation](../using/personalization/personalize.md#playground)

+++

+++**Q : Quelle est la différence entre le mode test et le mode essai pour les parcours ?**

**Mode test :** envoie des profils de test par le biais du parcours, déclenche des actions réelles et génère des messages de test. Nécessite un brouillon de parcours + espace de noms.
**Exécution d’essai :** effectue le suivi des chemins d’exécution sans rien envoyer. Fonctionne avec n’importe quel statut de parcours. Aucun message envoyé, aucune action exécutée.
**Utiliser ensemble :** Mode test pour le test des messages + Exécution d’essai pour la validation de la logique = couverture complète.

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

**Option 1 :** utiliser [API de simulation de campagne](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} pour les tests programmatiques
**Option 2 : prévisualisation** contenu avec profils de test dans l’interface utilisateur
**Option 3 :** envoyer des BAT aux adresses e-mail de test
**Bonne pratique :** combinez les trois pour une validation complète

+++


### Rubriques connexes

* [Gestion de contenu](content-management-landing-page.md) - Découvrez comment concevoir, prévisualiser et gérer du contenu à l’aide de modèles, de fragments et du Designer d’e-mail. Bonnes pratiques de création de contenu en Principal pour une valorisation de marque cohérente.

* [Reporting et Analytics](reporting-landing-page.md) - Analysez les performances des campagnes et des parcours à l’aide de rapports, de tableaux de bord et de mesures complets. Prenez des décisions axées sur les données pour optimiser les expériences client.

* [Configuration de Parcours &#x200B;](configure-journeys-landing-page.md) - Configurez les sources de données, les événements et les actions personnalisées pour activer une orchestration de parcours sophistiquée. Configurez les bases techniques de la création de parcours.

* [Gestion de campagne](../using/campaigns/get-started-with-campaigns.md) - Explorez les différents types de campagne et apprenez à créer, planifier et optimiser des campagnes par lots et en temps réel pour un impact maximal.
