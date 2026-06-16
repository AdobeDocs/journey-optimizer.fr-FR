---
solution: Journey Optimizer
product: journey optimizer
title: hub d’intégration de Journey Optimizer
description: Un hub d’intégration organisé pour Adobe Journey Optimizer qui rassemble des instructions détaillées, des cas d’utilisation réels et du contenu vidéo afin que les nouveaux utilisateurs puissent se préparer rapidement et offrir leur première expérience client.
feature: Get Started
topic: Content Management
role: User
level: Beginner
hide: true
keywords: parcours optimizer, intégration, hub d’intégration, cas d’utilisation, vidéos, tutoriels, prise en main, préparation, premier parcours
source-git-commit: 7af5076bb9a394110de6400991285ab2be86962d
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 12%

---

# hub d’intégration de Journey Optimizer {#onboarding-hub}


>[!BEGINSHADEBOX]

**Sur cette page :** Accélérez votre navigation sur Adobe Journey Optimizer : regardez une courte orientation, suivez les instructions étape par étape pour livrer votre première expérience, parcourez les cas d’utilisation réels et explorez le contenu vidéo traité.

>[!ENDSHADEBOX]

<!-- 
rebuild
-->

Vous découvrez [!DNL Adobe Journey Optimizer] ? Ce hub rassemble les ressources qui vous aident à passer de zéro à votre première expérience client en direct, avec des instructions étape par étape pour des objectifs communs, des cas d’utilisation réels qui montrent ce qui est possible et du contenu vidéo traité (tutoriels, présentations et pratiques).

>[!TIP]
>
>Vous ne savez pas quelle fonctionnalité correspond à votre objectif ? Commencez par le guide de l’objectif [d’abord trouver la fonctionnalité Journey Optimizer appropriée à votre objectif](ajo-use-case-guide.md) puis revenez ici pour obtenir des instructions détaillées.

## Commencer ici : regarder et apprendre {#start-here}

S&#39;il vous reste dix minutes, commencez par cette vidéo d&#39;orientation. Il décrit l’interface et met en évidence les fonctionnalités clés par rôle.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

Ensuite, développez votre confiance pratique avec ces ressources d’apprentissage :

* [Tutoriels Journey Optimizer &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — Vidéos détaillées et procédures pas à pas pour chaque rôle.
* [Liste de lecture vidéo sélectionnée par des experts](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"} — Ensemble séquentiel de courtes vidéos à regarder dans l’ordre.
* [Sandbox de formation](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} — Un environnement sûr avec des exemples de données à pratiquer.
* [Défis pratiques](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"} — Appliquez ce que vous apprenez avec des exercices guidés.

## Créer votre première expérience {#build-first}

Chacune des étapes ci-dessous est courte et axée sur les résultats : ce que vous allez créer, à qui elle est destinée et comment y parvenir. Sélectionnez l’objectif qui correspond à votre premier projet et suivez les liens vers la documentation détaillée.

### Bienvenue aux nouveaux clients {#build-welcome}

**Vous allez créer :** une série de bienvenue automatisée qui accueille chaque nouvel abonné et encourage les inactifs.
**Idéal pour les spécialistes marketing :** · **Fonctionnalité :** parcours déclenché par un événement

1. Confirmez que vos [profils et audiences unifiés](../audience/get-started-profiles.md) reçoivent l’événement d’inscription.
2. [Créez votre premier parcours &#x200B;](../building-journeys/journey-gs.md) et utilisez l’événement d’inscription comme entrée.
3. Ajoutez un [e-mail](../email/get-started-email.md) de bienvenue, puis une étape d’attente et une [notification push](../push/get-started-push.md) de suivi pour les profils qui n’ont pas encore été engagés.
4. [Personnalisez le contenu](../personalization/personalize.md) avec des attributs de profil tels que le prénom et les centres d’intérêt déclarés.

➡️ [Commencer par les parcours &#x200B;](../building-journeys/journey-gs.md)

### Récupérer les paniers abandonnés {#build-cart}

**Vous allez créer :** un flux de récupération en temps réel qui rappelle aux clients les éléments laissés derrière.
**Idéal pour les spécialistes marketing :** · **Fonctionnalité :** parcours déclenché par un événement

1. Assurez-vous que l’événement d’abandon de panier atteint Journey Optimizer (contactez votre [équipe de données](../data/gs-data.md) si nécessaire).
2. [Création d’un parcours &#x200B;](../building-journeys/journey-gs.md) déclenché par l’événement d’abandon.
3. Envoyez un e-mail de rappel personnalisé ; s’il n’y a pas de clic dans les 24 heures, connectez-vous à un suivi [push](../push/get-started-push.md).
4. [&#x200B; Personnaliser &#x200B;](../personalization/personalize.md) avec les éléments abandonnés et le statut de fidélité.

➡️ [Commencer par les parcours &#x200B;](../building-journeys/journey-gs.md)

### Envoi de messages transactionnels {#build-transactional}

**Vous allez créer :** confirmations de commande à la demande, d’expédition ou de rendez-vous déclenchées par un système externe.
**Idéal pour** spécialistes marketing et développeurs · **Fonctionnalité :** campagne déclenchée par l’API

1. Examinez le fonctionnement des [campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md) et la payload attendue.
2. Concevez le modèle de message et [personnalisez](../personalization/personalize.md)-le avec les détails de la transaction.
3. Demandez au développeur d’appeler le point d’entrée de campagne à partir de votre système de commande ou d’exécution.

➡️ [Utiliser des campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md)

### Lancer une campagne avec des tests A/B {#build-campaign}

**Vous allez créer :** une promotion planifiée qui sélectionne automatiquement le contenu le plus performant.
**Idéal pour les professionnels du marketing** · **Fonctionnalité :** Campagne planifiée + expérimentation de contenu

1. [Commencez avec des campagnes](../campaigns/get-started-with-campaigns.md) et définissez votre audience.
2. Utilisez la [génération de contenu par l’IA](../content-management/gs-generative.md) pour brouiller l’objet et copier les variations.
3. Configurez une [expérience de contenu](../content-management/experiment-accelerator-gs.md) pour tester des variantes sur un échantillon, puis envoyez le gagnant au reste.

➡️ [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)

### Personnaliser les offres par client {#build-offers}

**Vous allez créer :** une décision qui affiche la meilleure offre pour chaque client.
**Idéal pour les professionnels du marketing** · **Fonctionnalité : prise de décision**

1. [Commencez avec Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) et créez vos offres et vos règles d&#39;éligibilité.
2. Ajoutez la décision à un message de parcours ou de campagne [&#128279;](../building-journeys/journey-gs.md).
3. Couche dans [Fonctionnalités d’IA](ai-features.md) pour classer et optimiser automatiquement les offres.

➡️ [Prise en main d’Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Cas d’utilisation par objectif {#use-cases}

Les exemples ci-dessus présentent les points de départ les plus courants, mais Journey Optimizer prend en charge de nombreux autres scénarios, depuis les notifications de panne proactives et le réengagement du client jusqu’à la messagerie en temps réel tenant compte de l’emplacement. Chaque scénario combine une ou plusieurs fonctionnalités qui fonctionnent ensemble.

Pour trouver la fonctionnalité exacte de *votre* objectif, utilisez l’index complet organisé par objectif dans [Trouver la fonctionnalité Journey Optimizer appropriée pour votre objectif](ajo-use-case-guide.md). Pour obtenir des exemples complets et détaillés, consultez la bibliothèque de cas d’utilisation de Parcours [&#128279;](../building-journeys/jo-use-cases.md).

## Bibliothèque vidéo {#videos}

Parcourez le contenu vidéo traité par rubrique. Chaque onglet fournit des liens vers les tutoriels et listes de lecture appropriés sur Experience League.

>[!BEGINTABS]

>[!TAB Prise en main]

* [Présentation de Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — Concepts de base et présentation du produit.
* [Présentation des tutoriels Journey Optimizer &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — Catalogue complet de vidéos guidées.

>[!TAB Parcours et campagnes]

* [Présentation de la création d’un parcours &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — Créez votre premier parcours déclenché par un événement.
* [Créer des parcours avec Journey Agent](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} — Créez des parcours à partir d&#39;une invite en langage naturel.

>[!TAB Personalization et IA]

* [Assistant AI pour la génération de contenu](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} — Générez une copie, des images et des variations.
* [Utiliser la prise de décision pour personnaliser les offres web](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — Adapter les offres par client.

>[!TAB Rapports et optimisation]

* [Surveillez et analysez votre parcours avec des rapports dynamiques](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — Suivez les performances en temps réel.
* [Créer des expériences de contenu pour les campagnes par e-mail](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — Tester et optimiser le contenu.

>[!ENDTABS]

## Liste de contrôle d’intégration par rôle {#checklist}

L’intégration s’étend sur plusieurs rôles. Choisissez votre rôle pour afficher un chemin de départ ciblé :

* **Administrateur** — Configurez des sandbox, des autorisations et des canaux. [Prise en main en tant qu’administrateur](path/administrator.md)
* **Ingénieur de données** — Modélisez des schémas et ingérez des données. [Prise en main en tant qu’ingénieur de données](path/data-engineer.md)
* **Développeur** — Intégrez des SDK et déclenchez des événements. [Prise en main en tant que développeur](path/developer.md)
* **Professionnel du marketing** — Créez des parcours, du contenu et des audiences. [Prise en main en tant que spécialiste marketing](path/marketer.md)

Pour une présentation complète de la façon dont ces rôles fonctionnent ensemble, voir [Rôles et responsabilités](quick-start.md).

## Ressources connexes {#related-resources}

* [Trouvez la fonctionnalité Journey Optimizer adaptée à votre objectif](ajo-use-case-guide.md) — Guide de décision Goal-First pour chaque fonctionnalité.
* [Bibliothèque de cas d’utilisation de Parcours &#x200B;](../building-journeys/jo-use-cases.md) — Exemples pratiques et modèles d’implémentation.
* [Terminologie clé](terminology.md) — Clarifiez les concepts sous-jacents à chaque fonctionnalité.
* [Fonctionnalités intelligentes et d’IA](ai-features.md) — Explorez l’assistant d’IA, l’optimisation de l’heure d’envoi et la génération de contenu.
* [Prise en main de la gestion des données](../data/gs-data.md) — Comment les données sont-elles ingérées, unifiées et activées ?
