---
solution: Journey Optimizer
product: Journey Optimizer
title: Tester et approuver
description: Tester et approuver
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# Tester et approuver{#section-overview}

L’assurance qualité est essentielle pour offrir des expériences client exceptionnelles. Adobe Journey Optimizer fournit des fonctionnalités complètes de test et d’approbation pour vous aider à valider le contenu, vérifier la logique de parcours et vous assurer que les campagnes répondent à des normes de qualité avant d’atteindre votre audience. De la prévisualisation de messages personnalisés avec des profils de test à la simulation de flux de parcours complexes, ces outils vous permettent d&#39;identifier et de résoudre les problèmes dès le début, de réduire les risques et de préserver l&#39;intégrité de la marque. Que vous testiez le rendu des e-mails sur plusieurs appareils, validiez des parcours à plusieurs étapes ou établissiez des workflows d’approbation officiels, cette section vous guide à travers les bonnes pratiques et les processus détaillés pour renforcer la confiance dans vos campagnes et parcours. En mettant en œuvre des tests approfondis et des approbations structurées, vous minimiserez les erreurs, améliorerez la délivrabilité et créerez des expériences transparentes qui résonnent avec vos clients.

## Importance des tests et de l’approbation

Les processus de test et d’approbation constituent des points de contrôle qualité essentiels pour protéger la réputation de votre marque et assurer le succès de la campagne. Voici pourquoi ils sont importants :

* **Capturer les erreurs avant qu’elles n’atteignent les clients** - Identifiez les liens rompus, une personnalisation incorrecte, les problèmes de rendu et les défauts logiques dans un environnement contrôlé où les correctifs sont rapides et sans risque.

* **Améliorer la délivrabilité** - Testez les scores de spam, validez l’authentification des e-mails et vérifiez le rendu sur les clients de messagerie pour optimiser l’emplacement des boîtes de réception et les taux d’engagement.

* **Garantir la cohérence de la marque** - Prévisualisez le contenu avec différents profils de test pour vérifier que la personnalisation s’affiche correctement pour divers segments de clientèle et respecte les normes de la marque.

* **Validation de parcours complexes** - Simulez des flux de parcours à plusieurs étapes pour vérifier que les déclencheurs se déclenchent correctement, que les conditions s’évaluent correctement et que les clients reçoivent les messages appropriés au bon moment.

* **Établissement de la responsabilité** - Implémentez des workflows d’approbation officiels qui nécessitent l’approbation des parties prenantes, créant une propriété claire et réduisant les lancements de campagnes non autorisés ou prématurés.

* **Gagnez du temps et économisez des ressources** - Détectez les problèmes dès le début du cycle de développement lorsque les correctifs sont moins coûteux et plus rapides, afin d’éviter des corrections post-lancement coûteuses ou des remontées d’informations du service client.

## Bonnes pratiques de test

Pour optimiser l’efficacité de vos efforts de test, suivez ces pratiques recommandées :

1. **Testez tôt et souvent** - N’attendez pas qu’une campagne soit entièrement créée. Testez le contenu, la personnalisation et la logique de manière progressive au fur et à mesure que vous développez.

1. **Utiliser des profils de test réalistes** - [Créez des profils de test](../using/audience/creating-test-profiles.md) qui représentent précisément vos segments d’audience cible, y compris les cas Edge et les différents scénarios de personnalisation.

1. **Test sur les appareils et les clients** - Vérifiez [le rendu des e-mails](../using/content-management/rendering.md) sur les clients de messagerie les plus courants (Gmail, Outlook, Apple Mail) et les appareils (bureau, mobile, tablette) pour garantir un affichage cohérent.

1. **Valider entièrement la personnalisation** - Effectuez des tests avec plusieurs [profils de test](../using/content-management/test-profiles.md) dont les valeurs d’attribut sont différentes pour confirmer que les jetons de personnalisation s’affichent correctement et que les valeurs de secours fonctionnent.

1. **Simuler des chemins de parcours** - Pour les parcours complexes comportant plusieurs branches, utilisez [mode test](../using/building-journeys/testing-the-journey.md) pour tester différentes conditions d’entrée et attributs de profil afin de valider tous les chemins possibles.

1. **Vérifier les indicateurs de délivrabilité** - Vérifier [scores de spam](../using/content-management/spam-report.md), le statut d’authentification et les mesures d’intégrité des e-mails avant les envois volumineux.

1. **Documenter les résultats des tests** - Conservez des enregistrements des résultats des tests, des problèmes détectés et des résolutions pour améliorer les futurs processus de test et partagez les enseignements avec votre équipe.

1. **Impliquez rapidement les parties prenantes** - Partagez les aperçus et les résultats des tests avec les parties prenantes avant l’[approbation formelle](../using/test-approve/gs-approval.md) afin de recueillir les commentaires et d’aligner les attentes.

## Workflow de test recommandé

Suivez cette approche systématique pour garantir des tests approfondis et des approbations fluides :

### &#x200B;1. Développement et prévisualisation du contenu

Commencez par créer votre contenu et par utiliser les fonctionnalités de prévisualisation pour vérifier la conception et la personnalisation initiales :

* Concevoir le contenu de votre [e-mail](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notification push](../using/push/create-push.md) ou d’un autre canal
* Utilisez la fonction **[Simuler du contenu](../using/content-management/preview-test.md)** pour prévisualiser avec des profils de test
* Cochez [jetons de personnalisation](../using/personalization/personalization-syntax.md), contenu dynamique et valeurs de secours
* Vérifier le [rendu](../using/content-management/rendering.md) sur différents formats d’écran et clients de messagerie

### &#x200B;2. Validation technique

Validez les aspects techniques ayant un impact sur la délivrabilité et les fonctionnalités :

* Exécutez [ contrôles de score de spam ](../using/content-management/spam-report.md) pour identifier les problèmes de délivrabilité potentiels
* Tester les liens pour s’assurer qu’ils ne sont pas rompus et effectuer correctement le suivi
* Valider la configuration [authentification par e-mail](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)
* Vérifier le rendu HTML et rechercher les problèmes de compatibilité CSS
* Test [responsive design](../using/email/content-from-scratch.md) sur les appareils mobiles et les ordinateurs de bureau

### &#x200B;3. Essais Parcours

Pour les parcours, validez la logique d’orchestration :

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
* Activez la [ surveillance et alertes ](../using/reports/alerts.md) pour suivre les performances après le lancement

### &#x200B;6. Surveiller et itérer

Après le lancement, continuez la surveillance pour détecter rapidement tout problème :

* Configurer des [alertes système](../using/reports/alerts.md) pour les erreurs de parcours, les taux de rebond élevés ou un faible engagement
* Examinez les [rapports dynamiques](../using/building-journeys/report-journey.md) pour suivre les performances par rapport aux attentes
* Préparez-vous à [mettre en pause ou modifier](../using/building-journeys/journey-pause.md) les parcours en cas de problèmes critiques
* Documenter les leçons apprises pour améliorer les futurs processus de test

## Tests en action : cas d’utilisation

Découvrez comment les concepts de test s’appliquent aux scénarios réels :

* **[Envoyer des messages multicanaux](../using/building-journeys/journeys-uc.md)** - Ce cas d’utilisation montre comment tester un parcours qui combine la lecture d’audience, les événements de réaction et les e-mails/messages push. Découvrez comment valider l’ensemble du flux du ciblage d’audience à la diffusion de messages, et consultez les étapes de test et de publication en action.

* **[Envoyer un message aux abonnés](../using/building-journeys/message-to-subscribers-uc.md)** - Découvrez comment tester les parcours qui ciblent les listes d’abonnements avec une adresse e-mail dynamique. Cet exemple montre comment valider les expressions de personnalisation et s’assurer que les messages atteignent les abonnés appropriés.

* **[Envoyer des messages limités dans le temps](../using/building-journeys/weekday-email-uc.md)** - Découvrez comment tester les parcours avec des conditions temporelles pour vous assurer que les messages sont envoyés à des jours spécifiques. Découvrez comment valider les activités d’attente et la logique de planification.

* **[Explorez d’autres cas d’utilisation de parcours](../using/building-journeys/jo-use-cases.md)** - Accédez à une collection complète d’exemples pratiques couvrant les événements d’expérience, la messagerie multicanal et les intégrations système externes.

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

Validez votre parcours avant de le publier en le testant avec des profils spécifiques pour vous assurer que les événements, conditions et actions fonctionnent comme prévu.

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

::::

## Ressources supplémentaires

### Guides de test et de validation essentiels

* [Rapport dynamique dans votre Parcours ](../using/building-journeys/report-journey.md) - Surveillez les mesures de parcours en temps réel pour suivre les performances et identifier les problèmes lors de l’exécution. Accédez aux répartitions détaillées de la progression du profil, des déclencheurs d’événement et des taux d’achèvement de l’action.

* [Création de profils de test](../using/audience/creating-test-profiles.md) - Créez et gérez des profils de test pour simuler des scénarios client réels et valider la personnalisation. Découvrez comment marquer les profils pour les tests, définir des valeurs d’attribut et organiser les segments de profil de test.

* [Rapport sur les spams par e-mail](../using/content-management/spam-report.md) - Vérifiez le score de spam de vos e-mails avant envoi pour améliorer la délivrabilité et le placement des boîtes de réception. Découvrez comment les filtres anti-spam évaluent votre contenu et obtenez des recommandations d’amélioration.

* [FAQ sur les Parcours ](../using/building-journeys/journey-faq.md) - Trouvez des réponses aux questions courantes sur la création, le test, l&#39;exécution et le dépannage de parcours. Référence rapide pour résoudre des problèmes fréquents et comprendre le comportement du parcours.

### Rubriques connexes

* [Gestion de contenu](content-management-landing-page.md) - Découvrez comment concevoir, prévisualiser et gérer du contenu à l’aide de modèles, de fragments et du Designer d’e-mail. Bonnes pratiques de création de contenu en Principal pour une valorisation de marque cohérente.

* [Reporting et Analytics](reporting-landing-page.md) - Analysez les performances des campagnes et des parcours à l’aide de rapports, de tableaux de bord et de mesures complets. Prenez des décisions axées sur les données pour optimiser les expériences client.

* [Configuration de Parcours ](configure-journeys-landing-page.md) - Configurez les sources de données, les événements et les actions personnalisées pour activer une orchestration de parcours sophistiquée. Configurez les bases techniques de la création de parcours.

* [Gestion de campagne](../using/campaigns/get-started-with-campaigns.md) - Explorez les différents types de campagne et apprenez à créer, planifier et optimiser des campagnes par lots et en temps réel pour un impact maximal.
