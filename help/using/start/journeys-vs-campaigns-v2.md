---
solution: Journey Optimizer
product: journey optimizer
title: 'Parcours ou campagnes : choisir la bonne approche'
description: Comparez les Parcours, les campagnes d’action et les campagnes déclenchées par API pour choisir l’approche appropriée à vos besoins marketing dans Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
hide: true
keywords: parcours, campagne, comparaison, choisir, décision, workflow, temps réel, lot, orchestration, à plusieurs étapes, planifié, déclenché par API, piloté par événement
source-git-commit: ab31811861ccaab22fc787ce3c687204637fbd46
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 12%

---


# Parcours ou campagnes : choisissez la bonne approche {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Sur cette page :** Comparer des parcours avec des campagnes déclenchées par action et API afin de choisir l’approche appropriée pour chaque cas d’utilisation marketing dans Adobe Journey Optimizer. Pour les campagnes orchestrées, voir [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre deux méthodes principales pour atteindre et impliquer vos clients : **Parcours** et **Campagnes**. Les parcours sont conçus pour une orchestration en temps réel et à plusieurs étapes pilotée par le comportement du client. Les campagnes sont mieux adaptées aux diffusions ponctuelles ou planifiées vers une audience définie, ou aux activations de canaux entrants vers Edge pour une personnalisation à faible latence.

>[!NOTE]
>
>Les **campagnes orchestrées** présentent des caractéristiques architecturales distinctes (exécution par lots côté hub, données relationnelles à entités multiples) qui nécessitent des conseils dédiés. Ils ne sont pas inclus dans la comparaison ci-dessous afin d’éviter une simplification excessive. [En savoir plus sur les campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

## Quelle approche devriez-vous utiliser ? {#decision-guide}

La réponse se résume généralement à une seule question : *que doit-il se passer et pour qui ?*

Si vous avez besoin que **chaque client avance à son propre rythme** — recevoir des messages en fonction de ce qu&#39;il fait, attendre, puis réagir à sa prochaine action — utilisez un **Parcours**. Les parcours effectuent le suivi de l’emplacement de chaque profil et de ce qu’ils ont fait, ce qui les rend idéaux pour des expériences à plusieurs étapes telles que des séquences d’intégration, des flux d’abandon de panier ou des programmes de fidélité.

Si vous souhaitez **envoyer un message à un groupe de personnes selon un calendrier** une newsletter, une annonce de produit ou une promotion saisonnière, utilisez une campagne **Action**. Chaque personne de l’audience reçoit le message en même temps, sans avoir besoin de la logique par profil. Les campagnes d’action prennent également en charge les activations de canal entrant (in-app, web, cartes de contenu, basées sur du code) pour une personnalisation Edge à faible latence.

Si un système **externe doit déclencher un message immédiatement** (une confirmation de commande de votre plateforme d’e-commerce, une alerte d’expédition de votre système logistique, une réinitialisation de mot de passe de votre application), utilisez une campagne **déclenchée par l’API** pour un seul message à la demande ou un **parcours d’événement unitaire** si ce déclencheur doit déclencher un flux à plusieurs étapes.

Si vous avez besoin d’un **workflow par lots complexe avec segmentation avancée, données multi-entités ou nombres exacts de pré-envois**, consultez la section [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

>[!TIP]
>
>**Vous ne savez pas par où commencer ?** La plupart des équipes utilisent des Parcours pour les expériences comportementales et orientées événement, ainsi que des campagnes d’action pour les communications planifiées. Ces deux cas couvrent la majorité des cas d’utilisation.

## Comparaison {#quick-overview}

| Approche | Idéal pour | Style d’exécution |
|----------|----------|-----------------|
| **Parcours** | Expériences clients en temps réel et à plusieurs étapes avec logique conditionnelle | 1:1 orchestration : chaque profil à son propre rythme |
| **Campagnes d’action** | Activations planifiées ou récurrentes vers des audiences | Exécution par lots : audience traitée ensemble au moment de l’envoi |
| **Campagnes déclenchées par API** | Messages déclenchés par un événement ou transactionnels provenant de systèmes externes | Exécution à la demande : déclenchée par un appel API avec payload |

## Fonctionnement de chaque approche {#key-distinctions}

### Parcours : 1:1 orchestration en temps réel

Un Parcours est une zone de travail dans laquelle chaque profil parcourt son propre chemin à son propre rythme. AJO effectue le suivi de la situation de chaque personne dans le flux et réagit en temps réel à son comportement, qu’il s’agisse d’une action, d’une période d’inactivité ou d’un changement de profil.

Les fonctionnalités clés incluent les activités d’attente qui créent un timing personnalisé entre les étapes, l’embranchement conditionnel qui achemine les profils vers différents chemins, le capping de la fréquence pour contrôler la fréquence à laquelle un client reçoit des messages et le mode test pour valider la logique avant la mise en ligne. Les parcours peuvent également fractionner les profils en groupes en fonction du pourcentage pour les expériences A/B sur plusieurs chemins d’accès.

Un parcours d’abandon de panier illustre clairement la différence :

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Chaque client voit une chronologie différente en fonction de ce qu’il fait réellement. [En savoir plus sur Parcours](../building-journeys/journey.md)

### Campagnes : diffusion par lots ou déclenchée

Une campagne exécute une seule action, soit sur toutes les personnes d’une audience à la fois, soit sur demande lorsqu’elle est appelée par un système externe. Il n’existe aucune zone de travail et aucun état par profil : tous les profils sont traités de manière identique.

**Campagnes d’action** diffusez à une audience planifiée (unique ou récurrente) et prenez également en charge la diffusion entrante multi-surface (jusqu’à 10 actions de canal entrant par campagne, avec des règles de ciblage pour créer des variantes de message en fonction de l’appartenance à l’audience ou des attributs de profil).

Les **campagnes déclenchées par API** se déclenchent immédiatement lorsqu’un système externe appelle l’API. La personnalisation des messages est pilotée par les données de payload envoyées dans cet appel.

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

[En savoir plus sur les campagnes](../campaigns/get-started-with-campaigns.md)

## Exemples de cas d’utilisation {#use-cases}

| Cas d’utilisation | Approche recommandée | Pourquoi |
|----------|---------------------|-----|
| Accueillir une nouvelle clientèle avec l’intégration en plusieurs étapes | Parcours | Entrée en temps réel, plusieurs points de contact, chemins conditionnels |
| Abandon de panier avec séquence de rappel | Parcours | Déclencheur en temps réel, temps d’attente, suivi conditionnel |
| Réengager les personnes inactives en fonction de leur comportement | Parcours | Déclenché par la qualification d’audience, chemin personnalisé |
| Vente Flash déclenchée par un événement métier | Parcours (événement métier) | Déclencheur en temps réel affectant plusieurs membres de la clientèle |
| Newsletter mensuelle aux abonnés | Campagnes d’action | Message planifié à l’audience |
| Annonce promotionnelle à l’ensemble de la clientèle | Campagnes d’action | Message ponctuel, diffusion immédiate |
| Confirmation de commande ou alerte d’expédition | Campagnes déclenchées par API | Déclencheur de système externe, diffusion immédiate en une seule fois |
| Flux à plusieurs étapes déclenché par API | Parcours (Événement unitaire) | Le système externe envoie l’événement via l’API ; le parcours orchestre les étapes de suivi. |
| Workflow par lots complexe avec des données multi-entités | Campagnes orchestrées | Voir [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) |

## Disponibilité des fonctionnalités {#feature-availability}

### Canaux

Les trois approches prennent en charge l’ensemble complet des canaux sortants d’AJO : e-mail, notification push, SMS, LINE et WhatsApp. Le tableau ci-dessous présente les différences entre les canaux entrants et les canaux numériques.

| Canal | Parcours | Campagnes d’action | Campagnes déclenchées par API |
|---------|:--------:|:----------------:|:-----------------------:|
| In-app | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Basé sur le code | ✅ | ✅ | ❌ |
| Cartes de contenu | ✅ | ✅ | ❌ |
| Courrier | ✅ | ✅ | ❌ |

>[!NOTE]
>
>Pour connaître la disponibilité du canal des campagnes orchestrées, voir [Canaux dans les parcours et les campagnes](../channels/gs-channels.md#channels).

### Fonctionnalités avancées

| Fonctionnalité | Parcours | Campagnes d’action | Campagnes déclenchées par API |
|-----------|:--------:|:----------------:|:-----------------------:|
| Workflows en plusieurs étapes | ✅ | ❌ | ❌ |
| Déclencheurs en temps réel | ✅ | ❌ | ✅ |
| Activités d’attente | ✅ | ❌ | ❌ |
| Branchement conditionnel | ✅ | ❌ | ❌ |
| Exécution planifiée | ✅ | ✅ | ✅ |
| Déclenchement de l’API | ✅ (événement unitaire uniquement) | ❌ | ✅ |
| Optimisation de l’heure d’envoi | ✅ | ❌ | ❌ |
| Tests A/B | ✅ | ✅ | ❌ |
| Workflows d’approbation | ✅ | ✅ | ✅ |
| Données multi-entités | ❌ | ❌ | ❌ |
| Nombres exacts de messages de pré-envoi | ❌ | ❌ | ❌ |

>[!NOTE]
>
>Pour plus d’informations sur les fonctionnalités des campagnes orchestrées, notamment les expériences de contenu, le déclenchement d’API par lots et la segmentation d’entités multiples, consultez la section [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

## Questions courantes {#common-questions}

+++ Puis-je combiner des parcours et des campagnes dans ma stratégie marketing ?

Oui. De nombreuses organisations utilisent toutes les approches pour différents scénarios :

* **** pour l’engagement comportemental en temps réel
* **Campagnes d’action** pour les communications planifiées ou les activations entrantes
* **Campagnes déclenchées par API** pour les messages transactionnels
* **Campagnes orchestrées** pour les campagnes par lots complexes et gourmandes en données, consultez la section [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

Utilisez l’outil approprié pour chaque cas d’utilisation plutôt que de forcer une approche pour tout.

+++

+++ Puis-je convertir une campagne en parcours ou inversement ?

Non, vous devez recréer l’expérience au format approprié. Cependant, vous pouvez réutiliser du contenu, des audiences et des concepts logiques.

+++

+++ Quelle approche est la plus facile à élaborer ?

Les campagnes d’action sont généralement les plus simples (un seul point de contact diffusé à une audience), suivies de campagnes déclenchées par l’API, puis de Parcours, qui nécessitent davantage de travail de conception en raison de la logique à plusieurs étapes.

+++

+++ Quelle est l’approche la plus adaptée aux audiences de grande taille ?

Tous les trois peuvent être adaptés à l’échelle ; le bon choix dépend de votre modèle :

* Les campagnes **Lecture d’audience** et **Action** sont optimisées pour les audiences par lots volumineuses.
* **Les Parcours unitaires (basés sur un événement) traitent les profils individuellement au fur et à mesure des événements. De ce fait, l’échelle dépend du volume et du débit des événements.**

Pour la segmentation complexe avec des jeux de données volumineux et des données d’entités multiples, consultez [Campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ Puis-je utiliser la même audience pour l’ensemble des parcours et campagnes ?

Oui. Les audiences créées dans [!DNL Adobe Experience Platform] peuvent être utilisées dans des Parcours, des campagnes d’action et des campagnes orchestrées. Les campagnes déclenchées par API sont pilotées par la payload et n’utilisent pas les audiences préconfigurées de la même manière.

+++

## Étapes suivantes {#next-steps}

Vous souhaitez commencer à créer ? Consultez la documentation détaillée relative à l’approche choisie :

* **[Prise en main des Parcours](../building-journeys/journey.md)** - types de Parcours, concepteur et workflow
* **[Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)** - Campagnes déclenchées par une action et une API
* **[Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)** - Workflows de zone de travail par lots avec des données multi-entités (conseils distincts)

>[!MORELIKETHIS]
>
>* [comparaison des types de Parcours ](../building-journeys/journey.md#journey-types-comparison)
>* [Comparaison des types de campagne](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [FAQ sur les parcours](../building-journeys/journey-faq.md)
>* [FAQ sur les campagnes orchestrées](../orchestrated/orchestrated-campaigns-faq.md)

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Choisissez entre les Parcours, les campagnes d’action et les campagnes déclenchées par l’API selon que vous avez besoin d’une orchestration 1:1 en temps réel, d’une diffusion par lots planifiée ou entrante ou d’une exécution déclenchée par l’API à la demande.

**Intentions:**
* Comprendre les principales différences entre les Parcours, les campagnes d’action et les campagnes déclenchées par API
* Sélectionner l’approche appropriée pour un cas d’utilisation marketing donné à l’aide du guide de décision et des tableaux de comparaison
* Comprendre à quel moment les campagnes Action prennent en charge les activations de canal entrant par rapport aux diffusions sortantes
* Savoir quand passer aux campagnes orchestrées (composition ad hoc, données fédérées, entités multiples)
* Combinaison efficace de plusieurs approches dans une stratégie marketing

**Glossaire:**
* **Parcours** : flux d’orchestration en temps réel à plusieurs étapes où chaque profil progresse à son propre rythme en fonction du comportement et des événements. *(spécifique au produit)*
* **Campagne d’action** : campagne proposant des activations planifiées ou récurrentes aux audiences, c’est-à-dire des activations de canaux sortants ou entrants jusqu’à la périphérie pour une personnalisation à faible latence. *(spécifique au produit)*
* **Campagne déclenchée par une API** : campagne lancée par un système externe via un appel API, fournissant un message à la demande unique avec une personnalisation pilotée par la payload. *(spécifique au produit)*
* **Campagne orchestrée** : campagne par lots côté hub prenant en charge les données relationnelles à entités multiples, la composition des audiences ad hoc et les sources de données fédérées ; non couvertes par les tableaux de comparaison de cette page. *(spécifique au produit)*
* parcours d’événement unitaire **: parcours déclenché par une seule action de profil en temps réel ; à utiliser lorsque l’orchestration à plusieurs étapes est nécessaire après un événement envoyé par l’API.***(spécifique au produit)*
* **Activation du canal entrant** : diffusion d’expériences personnalisées en périphérie (expérience basée sur le code, in-app, carte de contenu, web) pour un rendu à faible latence, pris en charge dans les campagnes d’action. *(spécifique au produit)*

**Mécanismes de sécurisation :**
* Jusqu’à 10 actions de canal entrant par campagne d’action (limite stricte) - s’applique aux canaux entrants uniquement : expérience basée sur le code, in-app, carte de contenu, web
* Les campagnes orchestrées sont exclues des tableaux de comparaison de cette page afin d’éviter une simplification excessive. Consultez la documentation sur les campagnes orchestrées dédiées pour obtenir des détails architecturaux

**Terminologie:**
* Nom canonique : Campagnes d’action — variantes : « campagnes planifiées », « campagnes de diffusion »
* Nom canonique : campagnes déclenchées par API — variantes : « campagnes transactionnelles », « campagnes pilotées par l’événement »
* Ne les confondez pas : « Campagnes d’action » (diffusion planifiée/entrante aux audiences) ≠ « Campagnes déclenchées par l’API » (à la demande, pilotées par la payload, aucune audience préconfigurée) ≠ « Campagnes orchestrées » (lot côté hub avec données relationnelles)
* Ne les confondez pas : « parcours d’événement unitaire » (déclenché par l’action en temps réel d’un profil) ≠ « parcours d’événement métier » (déclenché par un événement hors profil affectant plusieurs personnes via une étape Lecture d’audience interne)
* Synonymes : « activation du canal entrant » = « action du canal entrant » (utilisé de manière interchangeable sur cette page pour les expériences diffusées sur Edge dans les campagnes d’action)

**FAQ:**
* **Q : Quand dois-je utiliser un Parcours au lieu d’une campagne d’action ?** utilisez des Parcours lorsque les clients doivent avancer à leur propre rythme avec une logique conditionnelle en temps réel sur plusieurs points de contact. Utilisez des campagnes d’action pour une diffusion planifiée ou entrante vers une audience prédéfinie.
* **Q : Les campagnes d’action peuvent-elles être diffusées sur les canaux entrants ?** — Oui. Les campagnes d’action prennent en charge l’activation du canal entrant (expérience basée sur le code, in-app, carte de contenu, web) jusqu’à la périphérie pour une personnalisation à faible latence, avec jusqu’à 10 actions entrantes par campagne et des règles de ciblage pour les variantes de message.
* **Q : Qu’est-ce qui distingue les campagnes orchestrées des campagnes d’action ?** : les campagnes orchestrées exécutent l’exécution par lots côté Hub avec des données relationnelles multi-entités, des nombres exacts de pré-envois, une composition d’audiences ad hoc et la prise en charge des données fédérées. Les campagnes d’action sont des diffusions sans état à exécution unique à des audiences Experience Platform.
* **Q : Quand dois-je utiliser une campagne déclenchée par l’API plutôt qu’un parcours d’événement unitaire ?** — Utilisez une campagne déclenchée par API lorsqu&#39;un système externe doit déclencher immédiatement un seul message avec des données de payload ; utilisez un parcours d&#39;événement unitaire lorsque l&#39;orchestration à plusieurs étapes est nécessaire après l&#39;événement envoyé par l&#39;API.
* **Q : Puis-je combiner des Parcours et des campagnes dans la même stratégie marketing ?** — Oui. Utilisez des Parcours pour l’engagement comportemental en temps réel, des campagnes d’action pour des diffusions planifiées ou des activations entrantes, des campagnes déclenchées par API pour les messages transactionnels et des campagnes orchestrées pour les workflows par lots complexes.

+++
<!-- ai-accordion-version: 1 | source-hash: 873097f5 -->
