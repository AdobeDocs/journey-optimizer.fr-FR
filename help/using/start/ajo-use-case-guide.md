---
solution: Journey Optimizer
product: journey optimizer
title: Choisir la bonne fonctionnalité pour votre objectif | Adobe Journey Optimizer
description: Découvrez les principaux cas d’utilisation pour lesquels Adobe Journey Optimizer est conçu, avec des conseils sur les fonctionnalités d’AJO les mieux adaptées à chaque scénario.
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: parcours optimizer, cas d’utilisation, guide de décision, quelle fonctionnalité, commencer, objectifs pour les professionnels de la santé, tutoriels
source-git-commit: b20d08d5547e8f08bd92a8f1463d11e823f51fcf
workflow-type: tm+mt
source-wordcount: '3147'
ht-degree: 31%

---

# Choisir la bonne fonctionnalité pour votre objectif {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**Sur cette page :** commencez par ce que vous souhaitez accomplir, puis passez à la fonctionnalité Adobe Journey Optimizer qui la résout, sans avoir besoin de connaître au préalable le nom de la fonctionnalité.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre de nombreuses fonctionnalités, et la bonne dépend de ce que vous essayez d’accomplir. Ce guide est organisé autour des objectifs commerciaux plutôt que des fonctionnalités du produit : recherchez l’objectif qui correspond à vos besoins, puis suivez le lien pour commencer à utiliser la fonctionnalité recommandée.

Utilisez cette page comme un routeur rapide — scannez pour votre objectif et sautez directement à la bonne fonctionnalité. Si vous débutez, commencez par [Prise en main de Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) pour trouver le point d’entrée approprié pour votre rôle.

>[!NOTE]
>
>Pour obtenir des exemples d’implémentation détaillés, consultez la bibliothèque de cas d’utilisation de Parcours [&#128279;](../building-journeys/jo-use-cases.md).

Lorsqu’un tutoriel de bout en bout n’est pas disponible pour un scénario spécifique, le lien vous mène au meilleur point de départ actuel pour apprendre la fonctionnalité et commencer.

L’IA est intégrée à la plupart de ces fonctionnalités. Recherchez la balise **(AI)** dans les tableaux ci-dessous. L’[assistant d’IA](ai-features.md#ai-assistant) conversationnel peut également répondre à tout moment aux questions sur les produits et obtenir des informations opérationnelles de surface sur vos parcours. Pour l’ensemble complet des fonctionnalités intelligentes, voir [Fonctionnalités intelligentes et IA](ai-features.md).

>[!TIP]
>
>Vous découvrez Journey Optimizer ? Commencez par [Prise en main de Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) pour choisir le bon chemin pour votre rôle, puis lisez [Qu’est-ce que Journey Optimizer](get-started.md) pour l’essentiel. Pour vous familiariser avec les activités pratiques, parcourez les tutoriels [&#128279;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} suivez une liste de lecture vidéo [sélectionnée par des experts](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"} et exercez-vous dans un [sandbox de formation](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} ou avec les [&#x200B; défis pratiques](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}.

## Configuration de Journey Optimizer pour votre équipe {#setup-admin}

Pour les administrateurs et les utilisateurs techniques qui doivent configurer l’environnement avant de créer des parcours ou des campagnes.

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Configurer des canaux e-mail, SMS ou push avant l’envoi | Configuration des canaux | [Prise en main de la configuration des canaux](../configuration/get-started-configuration.md) |
| Préchauffer une nouvelle adresse IP pour l’envoi d’e-mails | Plan de préchauffage des adresses IP | [Prise en main du préchauffage d’adresses IP](../configuration/ip-warmup-gs.md) |
| Configurer les rôles, les autorisations et le contrôle d’accès | Contrôle d’accès | [Prise en main du contrôle d’accès](../administration/permissions-overview.md) |
| Travail dans plusieurs environnements ou régions | Sandbox | [Utiliser des sandbox](../administration/sandboxes.md) |

## Impliquez les clients au fur et à mesure des événements {#engage-real-time}

Pour les scénarios où vous réagissez à une action ou à un événement client au fur et à mesure qu’il se produit.

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Accueillir automatiquement un nouveau client ou abonné | Parcours déclenché par un événement | [Prise en main des parcours &#x200B;](../building-journeys/journey-gs.md) · [Introduction à la création d’un parcours &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |

>[!BEGINSHADEBOX]

**Avant de créer :** assurez-vous que (1) un événement d’entrée de parcours [&#128279;](../event/about-events.md) est configuré pour capturer le déclencheur d’inscription, (2) qu’une [surface de canal e-mail ou push](../configuration/channel-surfaces.md) est configurée pour votre sandbox et (3) qu’au moins un [profil de test](../audience/creating-test-profiles.md) est disponible pour valider le parcours avant la publication.

>[!ENDSHADEBOX]

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Récupérer un panier abandonné ou une session de navigation | Parcours déclenché par un événement | [Prise en main de parcours](../building-journeys/journey-gs.md) · [Tutoriel sur la navigation abandonnée](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |

>[!BEGINSHADEBOX]

**Avant de créer :** vous avez besoin (1) d’un [événement comportemental](../event/about-events.md) qui capture l’action de panier ou de navigation à partir de votre SDK web ou mobile, (2) d’une stratégie [activité d’attente](../building-journeys/wait-activity.md) décidée (généralement 1 à 4 heures avant le premier coup de pouce) et (3) d’une surface de canal prête pour le message de relance. Remarque : le parcours doit inclure une condition pour quitter les profils qui ont effectué l’achat avant la fin de la période d’attente.

>[!ENDSHADEBOX]

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Déclencher un parcours à partir de l’envoi d’un formulaire de site web | Parcours déclenché par un événement | [Prise en main de parcours](../building-journeys/journey-gs.md) · [Tutoriel](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| Réagir au comportement in-app (ouverture de l’application, affichage de l’écran) | Parcours + in-app | [Prise en main d’In-app](../in-app/get-started-in-app.md) |
| Envoyer des confirmations de commande, d’expédition ou de rendez-vous | Campagne déclenchée par l’API | [Utiliser des campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md) |
| Réengager les clients inactifs ou obsolètes | Parcours + audiences | [Prise en main des profils et des audiences](../audience/get-started-profiles.md) · [Création d’audiences à l’aide du créateur de règles](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |

>[!BEGINSHADEBOX]

**Avant de créer :** vous avez besoin (1) d’une [audience définie dans Adobe Experience Platform](../audience/about-audiences.md) qui identifie les profils inactifs (par exemple, aucun achat ou connexion dans les 60 jours), (2) d’une décision sur le canal de réengagement (e-mail, notification push ou SMS) et (3) d’une règle de suppression ou d’une [limitation de fréquence](../conflict-prioritization/channel-capping.md) pour éviter de contacter les profils ayant reçu récemment un message. Utilisez une entrée de parcours **Lecture d’audience**, et non un événement, pour ce scénario.

>[!ENDSHADEBOX]

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Tester un parcours avec des données réelles avant de l’activer | essai parcours | [Testez votre parcours avec un essai](../building-journeys/journey-dry-run.md) |
| Mettre en pause un parcours dynamique pour apporter des modifications sans arrêter les profils en cours | Parcours de la pause et de la reprise | [Mettre en pause et reprendre un parcours &#x200B;](../building-journeys/journey-pause.md) |
| Créer ou optimiser un parcours à partir d’une invite en langage naturel | Journey Agent **(AI)** | [Agents d’IA](ai-features.md#ai-agents) · Tutoriel Journey Agent [&#128279;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## Atteindre les audiences à grande échelle {#reach-at-scale}

Pour une diffusion de type « un à plusieurs » planifiée vers une audience définie.

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Envoi d’une newsletter ou d’une promotion à un segment | Campagne planifiée | [Commencer à utiliser les campagnes](../campaigns/get-started-with-campaigns.md) |

>[!BEGINSHADEBOX]

**Avant de créer :** vous avez besoin (1) d’un [segment d’audience publié](../audience/about-audiences.md) dans Adobe Experience Platform, (2) d’une [surface de canal e-mail](../configuration/channel-surfaces.md) avec un domaine d’envoi vérifié et (3) de tout [fragment de contenu ou modèle](../content-management/fragments.md) vous prévoyez de réutiliser des modèles déjà publiés. Les campagnes planifiées sont le bon choix ici (et non les parcours), s’il s’agit d’un envoi unique ou récurrent sans logique de branchement.

>[!ENDSHADEBOX]

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Lancer un produit avec un test A/B | Expérimentation de contenu **(AI)** | [Prise en main de l’expérimentation de contenu](../content-management/experiment-accelerator-gs.md) · [Création d’expériences de contenu pour les campagnes par e-mail](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| Informer les clients d’une panne ou d’une mise à jour du service | Campagne planifiée + audiences | [À propos des audiences](../audience/about-audiences.md) |
| Concevoir une campagne à plusieurs étapes avec une logique d’embranchement | Campagnes orchestrées | [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) |
| Cibler uniquement les profils qui ont changé depuis ma dernière exécution de campagne | Campagnes orchestrées — requête incrémentale | [Création de requêtes dans des campagnes orchestrées](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| Vérifier le nombre de profils qui correspondent à mon audience avant le lancement | Prévisualisation de l’audience | [À propos des audiences](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| Coordonner la messagerie sur de nombreux canaux à grande échelle | Orchestration | [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) · [Évolution de l’orchestration à l’engagement omnicanal](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| Envoyer chaque message au meilleur moment pour chaque client | **d’optimisation de l’heure d’envoi (AI)** | [Optimisation de l’heure d’envoi](../building-journeys/send-time-optimization.md) |

## Personnaliser ce que chaque client voit {#personalize}

Pour adapter les offres et le contenu à chaque individu.

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Afficher la meilleure offre pour chaque client | Prise de décision | [Prise en main d’Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) · [Tutoriel sur les offres web](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |

>[!BEGINSHADEBOX]

**Avant la génération :** decisioning nécessite une séquence de configuration spécifique. Vous avez besoin (1) [d’éléments de décision (offres) créés](../experience-decisioning/items.md) avec des règles d’éligibilité et des attributs, (2) d’une [stratégie de sélection](../experience-decisioning/selection-strategies.md) ou formule de classement configurée, et (3) d’une [politique de décision](../experience-decisioning/create-decision.md) associée à la surface où les offres apparaîtront. L’omission de cette séquence est la raison la plus courante pour laquelle les premières configurations de prise de décision ne parviennent pas à renvoyer de résultats.

>[!ENDSHADEBOX]

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Classer les offres à l&#39;aide d&#39;une formule (code postal, revenu, météo) | Decisioning — formule de classement | [Formules de classement](../experience-decisioning/ranking/ranking-formulas.md) · [Tutoriel sur les formules de classement](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} · [Tutoriel sur les données météorologiques](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| Utilisation de données de produit externes ou de gestion de la relation client pour personnaliser les offres | Prise de décision - Recherche de jeu de données AEP | [Utiliser la recherche de jeu de données dans la prise de décision](../experience-decisioning/context-data.md) |
| Adapter le contenu du message aux données de profil | Personnalisation | [Personnaliser votre contenu](../personalization/personalize.md) |
| Générer des variantes de copie, d’image et de message | Génération de contenu par l’IA **(AI)** | [Génération de contenu AI](../content-management/gs-generative.md) · [Tutoriel](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| Conversion d’une image de conception en modèle d’e-mail modifiable | Convertisseur d’image en HTML **(AI)** | [Convertir une image en modèle d’e-mail](../content-management/image-to-html.md) |
| Classement et personnalisation automatiques des offres | Modèles de classement AI **(AI)** | [Modèles d’IA pour la prise de décision](../experience-decisioning/ranking/ai-models.md) |
| Diffuser du contenu contextuel toujours actif (pas de campagne) | Cartes de contenu | [Prise en main des cartes de contenu](../content-card/get-started-content-card.md) · [Création de cartes de contenu](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| Diffuser du contenu personnalisé via l’API vers une application ou une surface | Expérience basée sur du code | [Commencer avec une expérience basée sur du code](../code-based/get-started-code-based.md) |
| Contrôler les parties d’un modèle d’e-mail que mon équipe peut modifier | Verrouillage de contenu | [Verrouiller le contenu dans des modèles d’e-mail](../content-management/content-locking.md) |

## Coordonner et régir la diffusion {#coordinate-govern}

Pour contrôler comment, quand et à quelle fréquence les clients sont contactés sur plusieurs canaux.

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Prévenir la fatigue des messages sur plusieurs canaux | Capping de la fréquence | [Définir le capping de la fréquence par canal](../conflict-prioritization/channel-capping.md) |
| Résoudre les messages en conflit ou en concurrence | Hiérarchisation des conflits | [Identifier les conflits potentiels](../conflict-prioritization/conflicts.md) · [Tutoriel](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| Choix du parcours prioritaire | Arbitrage des parcours | [Utilisation de formules pour classer les parcours &#x200B;](../conflict-prioritization/journey-ranking-formulas.md) |
| Respecter les heures calmes et le consentement | Heures calmes / Confidentialité | [Définir des heures calmes](../conflict-prioritization/quiet-hours.md) |
| Application des politiques de consentement et des libellés d’utilisation des données sur tous les canaux | Consentement et gouvernance des données | [Prise en main de la confidentialité](../privacy/get-started-privacy.md) |
| Recevez une alerte lorsqu’un parcours présente des taux d’erreur ou de rejet élevés | Alertes de parcours | [Configurer des alertes de parcours &#x200B;](../reports/alerts.md) |

## Choisir un canal de diffusion {#choose-channel}

| Je souhaite envoyer... | Canal | Commencer ici |
| --- | --- | --- |
| Newsletters, promotions ou messages transactionnels par e-mail | Email | [Prise en main des e-mails](../email/get-started-email.md) |
| Notifications push mobiles (iOS et Android) | Notification push | [Prise en main des notifications push](../push/get-started-push.md) |
| SMS, MMS ou SMS | SMS/MMS/RCS | [Prise en main des SMS/MMS/RCS](../mobile/get-started-mobile.md) · [Mobile Learning Hub](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| Messages WhatsApp via l’API Meta Cloud | WhatsApp | [Commencer avec WhatsApp](../whatsapp/get-started-whatsapp.md) |
| Superpositions et bannières dans le navigateur ou dans l’application | In-app | [Prise en main d’In-app](../in-app/get-started-in-app.md) |
| Contenu de page web personnalisé | Web | [Prise en main du canal web](../web/get-started-web.md) |
| Toute surface via l’API (kiosque, appareil connecté, application découplée) | Expérience basée sur du code | [Commencer avec une expérience basée sur du code](../code-based/get-started-code-based.md) |
| Éléments de courrier physiques déclenchés à partir d’un parcours | Canal Courrier | [Prise en main du courrier](../direct-mail/get-started-direct-mail.md) |

## Mesurer et optimiser {#measure-optimize}

Pour le suivi des performances, le diagnostic des problèmes et l’amélioration des résultats au fil du temps.

| Je veux... | Fonctionnalité recommandée | Commencer ici |
| --- | --- | --- |
| Voir Mesures de performances pour un parcours ou une campagne dynamique | Rapports dynamiques | [Rapports dynamiques](../reports/live-report.md) · [Surveillez et analysez votre parcours à l’aide de rapports dynamiques](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| Rapport sur les performances complètes de la campagne ou du parcours une fois qu’elle est terminée. | Rapports globaux | [Commencer la création de rapports](../reports/gs-reports.md) |
| Analysez une expérience et obtenez des recommandations pour l’étape suivante | Experimentation Agent **(AI)** | [&#128279;](ai-features.md#experimentation-agent) · [Tutoriel](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| Surveiller l’intégrité et la latence des actions personnalisées dans mes parcours | Surveillance des actions personnalisées | [Utiliser des actions personnalisées](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| Recevez une alerte lorsque les taux d’erreurs de parcours ou de rejet dépassent les seuils. | Alertes de parcours | [Configurer des alertes de parcours &#x200B;](../reports/alerts.md) |

## Flux de démarrage {#starter-flows}

Chaque flux de démarrage ci-dessous est un ensemble court d’étapes axées sur les résultats : ce que vous allez créer, à qui il est destiné et comment y parvenir. Sélectionnez l’objectif qui correspond à votre premier projet et suivez les liens vers la documentation détaillée.

### Bienvenue aux nouveaux clients {#flow-welcome}

**Vous allez créer :** une série de bienvenue automatisée qui accueille chaque nouvel abonné et encourage les inactifs.
**Idéal pour les spécialistes marketing :** · **Fonctionnalité :** parcours déclenché par un événement

1. Confirmez que vos [profils et audiences unifiés](../audience/get-started-profiles.md) reçoivent l’événement d’inscription.
1. [Créez votre premier parcours &#x200B;](../building-journeys/journey-gs.md) et utilisez l’événement d’inscription comme entrée.
1. Ajoutez un [e-mail](../email/get-started-email.md) de bienvenue, puis une étape d’attente et une [notification push](../push/get-started-push.md) de suivi pour les profils qui n’ont pas encore été engagés.
1. [Personnalisez le contenu](../personalization/personalize.md) avec des attributs de profil tels que le prénom et les centres d’intérêt déclarés.

➡️ [Commencer par les parcours &#x200B;](../building-journeys/journey-gs.md)

### Récupérer les paniers abandonnés {#flow-cart}

**Vous allez créer :** un flux de récupération automatisé qui rappelle aux clients les éléments laissés derrière.
**Idéal pour les spécialistes marketing :** · **Fonctionnalité :** parcours déclenché par un événement

1. Assurez-vous que l’événement d’abandon de panier atteint Journey Optimizer (contactez votre [équipe de données](../data/gs-data.md) si nécessaire).
1. [Création d’un parcours &#x200B;](../building-journeys/journey-gs.md) déclenché par l’événement d’abandon.
1. Envoyez un e-mail de rappel personnalisé ; s’il n’y a pas de clic dans les 24 heures, connectez-vous à un suivi [push](../push/get-started-push.md).
1. [&#x200B; Personnaliser &#x200B;](../personalization/personalize.md) avec les éléments abandonnés et le statut de fidélité.

➡️ [Commencer par les parcours &#x200B;](../building-journeys/journey-gs.md)

### Envoi de messages transactionnels {#flow-transactional}

**Vous allez créer :** confirmations de commande à la demande, d’expédition ou de rendez-vous déclenchées par un système externe.
**Idéal pour** spécialistes marketing et développeurs · **Fonctionnalité :** Campagne déclenchée par un système externe

1. Examinez le fonctionnement des campagnes [déclenchées par un système externe](../campaigns/api-triggered-campaigns.md) et la payload attendue.
1. Concevez le modèle de message et [personnalisez](../personalization/personalize.md)-le avec les détails de la transaction.
1. Demandez au développeur d’appeler le point d’entrée de campagne à partir de votre système de commande ou d’exécution.

➡️ [utiliser des campagnes déclenchées par un système externe](../campaigns/api-triggered-campaigns.md)

### Lancer une campagne avec des tests de contenu {#flow-campaign}

**Vous allez créer :** une promotion planifiée qui sélectionne automatiquement le contenu le plus performant.
**Idéal pour les professionnels du marketing** · **Fonctionnalité :** Campagne planifiée + expérimentation de contenu

1. [Commencez avec des campagnes](../campaigns/get-started-with-campaigns.md) et définissez votre audience.
1. Utilisez [génération de contenu](../content-management/gs-generative.md) pour brouiller l’objet et copier les variations.
1. Configurez une [expérience de contenu](../content-management/experiment-accelerator-gs.md) pour tester des variantes sur un échantillon, puis envoyez le gagnant au reste.

➡️ [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)

### Personnaliser les offres par client {#flow-offers}

**Vous allez créer :** une décision qui affiche la meilleure offre pour chaque client.
**Idéal pour les professionnels du marketing** · **Fonctionnalité : prise de décision**

1. [Commencez avec Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) et créez vos offres et vos règles d&#39;éligibilité.
1. Ajoutez la décision à un message de parcours ou de campagne [&#128279;](../building-journeys/journey-gs.md).
1. Ajoutez des [fonctionnalités intelligentes](ai-features.md) pour classer et optimiser automatiquement les offres.

➡️ [Prise en main d’Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Exemples de scénarios {#example-scenarios}

Ces exemples illustrent comment les fonctionnalités de Journey Optimizer se combinent selon les différents rôles, secteurs et canaux.

### Récupération après livraison retardée {#scenario-delayed-shipment}

**Rôle :** spécialiste marketing | **Fonctionnalité principale :** [profil unifié + exclusion d’audience](../audience/get-started-profiles.md)

Supposons qu’une boutique de vêtements envoie généralement des enquêtes après achat à tous les clients et clientes qui ont acheté des produits au cours des 7 derniers jours. En raison des intempéries, quelques envois ont été retardés. En identifiant les clientes et clients qui n’ont pas reçu leurs achats, la boutique de vêtements peut les exclure de l’envoi de l’enquête de satisfaction client programmée et envoyer à la place un e-mail personnalisé s’excusant du retard et proposant un code de remise avec des recommandations de produits basées sur leurs achats précédents.

[Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)

### Engagement en magasin en temps réel {#scenario-instore}

**Rôle :** spécialiste marketing | **Fonctionnalité principale :** [déclenchement du géorepérage + notification push](../push/get-started-push.md)

Le même retailer peut interagir avec un client fidèle qui se rend sur le parking du magasin en lui envoyant une notification push à propos d&#39;un pull à nouveau en stock à la taille du client.

[Prise en main des notifications push](../push/get-started-push.md)

### Récupération après abandon de panier {#scenario-cart}

**Rôle :** spécialiste marketing | **Fonctionnalité principale :** [parcours à plusieurs étapes déclenché par un événement](../building-journeys/journey-gs.md)

Lorsqu’un client ajoute des articles à un panier en ligne, mais quitte le panier sans effectuer l’achat, Journey Optimizer détecte l’événement et lance automatiquement un parcours de récupération. La personne reçoit un e-mail personnalisé lui rappelant les articles abandonnés. Si elle ne clique pas dans les 24 heures, une notification push de suivi est envoyée, personnalisée en fonction de son historique de navigation et de son statut de fidélité.

[Créer votre premier parcours](../building-journeys/journey-gs.md)

### Série de bienvenue pour le service de streaming {#scenario-welcome}

**Rôle :** responsable marketing | **Fonctionnalité principale :** [parcours de bienvenue déclenché par un événement](../building-journeys/journey-gs.md)

Lorsqu’une personne s’abonne à un service de streaming, Journey Optimizer détecte l’événement d’inscription et lance immédiatement un parcours de bienvenue en plusieurs étapes. La personne reçoit un e-mail de bienvenue l’encourageant à ouvrir l’application pour la première fois. Si aucune activité de connexion n’est détectée dans les 48 heures, une notification push de suivi est envoyée avec des recommandations de contenu personnalisées basées sur ses intérêts indiqués lors de l’inscription, transformant ainsi une personne abonnée passive en utilisateur ou utilisatrice actif et engagé dès le premier jour.

[Créer votre premier parcours](../building-journeys/journey-gs.md)

### Rappel de la réservation avec itinéraire {#scenario-reservation}

**Rôle :** responsable marketing | **Fonctionnalité principale :** [messages concernant la date et le lieu](../campaigns/get-started-with-campaigns.md)

Une marque d’hôtellerie-restauration envoie à chaque personne un rappel une heure avant sa réservation. La notification inclut le nom du client ou de la cliente, l’heure de la réservation et les indications géographiques du lieu, générés automatiquement à partir du profil client et des données de réservation, sans intervention manuelle de l’équipe marketing.

[Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)

### Notification proactive de panne de service {#scenario-outage}

**Rôle :** opérations | **Fonctionnalité principale :** [sélection automatisée d’audiences à grande échelle](../audience/about-audiences.md)

En cas d’interruption de service, Journey Optimizer identifie automatiquement les personnes concernées en fonction des données de leur compte et des comportements d’utilisation. Ces personnes reçoivent une notification proactive reconnaissant le problème et décrivant les étapes suivantes pour transformer une expérience potentiellement négative en un moment de transparence et de confiance, à grande échelle.

[Créer votre premier parcours](../building-journeys/journey-gs.md)

### Campagne promotionnelle intelligente {#scenario-ai-campaign}

**Rôle :** spécialiste marketing | **Fonctionnalité principale :** [Génération de contenu + expérimentation](ai-features.md)

Une marque de vente au détail planifiant le lancement d’un produit utilise l’assistant IA de Journey Optimizer pour générer plusieurs variations d’objet et de corps de message en quelques minutes, en s’appuyant sur un prompt en langage naturel et sur les directives de marque chargées. L’expérimentation de contenu intégrée identifie automatiquement la variante la plus performante parmi un échantillon d’audience initial. Le message gagnant est ensuite déployé auprès des destinataires restants, ce qui optimise l’engagement sans effort supplémentaire de rédaction.

[Explorer les fonctionnalités intelligentes](ai-features.md) | [En savoir plus sur l’expérimentation de contenu](../content-management/experiment-accelerator-gs.md)

### Alertes de maintenance via l’application mobile {#scenario-maintenance}

**Rôle :** opérations | **Fonctionnalité principale :** [orchestration de parcours non marketing](../building-journeys/journey-gs.md)

Les personnes autres que les responsables marketing comme les équipes opérationnelles et le service clientèle peuvent utiliser [!DNL Adobe Journey Optimizer] pour gérer les notifications opérationnelles ou surveiller les processus d’intégration. Par exemple, un parc d’attraction où les visiteurs et visiteuses téléchargent une application mobile dans le cadre de leur expérience : le personnel de maintenance peut utiliser Journey Optimizer pour informer les visiteurs et visiteuses du parc des attractions actuellement fermées en raison de travaux de maintenance.

[Créer votre premier parcours](../building-journeys/journey-gs.md)

## Bibliothèque vidéo {#videos}

Parcourez le contenu vidéo traité par rubrique. Chaque onglet fournit des liens vers les tutoriels et listes de lecture appropriés sur Experience League.

>[!BEGINTABS]

>[!TAB Prise en main]

* [Présentation de Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — Concepts de base et présentation du produit.
* [Présentation des tutoriels Journey Optimizer &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — Catalogue complet de vidéos guidées.

>[!TAB Parcours et campagnes]

* [Présentation de la création d’un parcours &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — Créez votre premier parcours déclenché par un événement.
* [Créer des parcours avec Journey Agent](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} — Créez des parcours à partir d&#39;une invite en langage naturel.

>[!TAB Personalization et intelligence]

* [Assistant AI pour la génération de contenu](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} — Générez une copie, des images et des variations.
* [Utiliser la prise de décision pour personnaliser les offres web](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — Adapter les offres par client.

>[!TAB Rapports et optimisation]

* [Surveillez et analysez votre parcours à l’aide de rapports dynamiques](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — Suivez les performances au fur et à mesure de l’exécution des parcours.
* [Créer des expériences de contenu pour les campagnes par e-mail](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — Tester et optimiser le contenu.

>[!ENDTABS]

## Choix entre des parcours, des campagnes et des campagnes orchestrées {#choosing}

| Scénario | Utilisation |
|----------|-----|
| Basé sur le comportement, à plusieurs étapes, chaque client évolue à son propre rythme | Parcours |
| Message simple planifié ou déclenché par API à une audience | Campaign |
| Workflow par lots complexe avec segmentation d’entités multiples | Campagne orchestrée |

## Vous n&#39;êtes pas sûr ? {#not-sure}

Si votre objectif correspond à un terme que vous ne connaissez pas ou si vous ne savez pas quelle fonctionnalité pointe le tableau, commencez par consulter la page de terminologie clé [&#128279;](terminology.md) afin de clarifier les concepts sous-jacents à chaque fonctionnalité.

Vous pouvez également gagner en confiance grâce aux exercices de bout en bout dans les tutoriels [&#128279;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
