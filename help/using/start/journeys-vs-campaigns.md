---
solution: Journey Optimizer
product: journey optimizer
title: 'Parcours ou campagnes : choisir la bonne approche'
description: Comparez les Parcours, les campagnes d’action et les campagnes déclenchées par API pour choisir l’approche appropriée à vos besoins marketing dans Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: parcours, campagne, comparaison, choisir, décision, workflow, temps réel, lot, orchestration, à plusieurs étapes, planifié, déclenché par API, piloté par événement
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
TQID: https://experienceleague.adobe.com/RWLVSULVO0idnCs5OVQR1yVvNv1G0JwP3y-3sNXQg50
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: addf009e-030a-4310-8534-776a3e62ed48
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: d4be496be65eef2c9cab727804f762350957223a
workflow-type: tm+mt
source-wordcount: 2483
ht-degree: 29%

---

# Parcours ou campagnes : choisissez la bonne approche {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Sur cette page :** Comparer des parcours avec des campagnes déclenchées par action et API afin de choisir l’approche appropriée pour chaque cas d’utilisation marketing dans Adobe Journey Optimizer. Pour les campagnes orchestrées, voir [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre deux méthodes principales pour atteindre et impliquer vos clients : **Parcours** et **Campagnes**. Les parcours sont conçus pour une orchestration en temps réel et à plusieurs étapes pilotée par le comportement du client. Les campagnes sont mieux adaptées aux diffusions ponctuelles ou planifiées vers une audience définie, ou aux activations de canaux entrants vers Edge pour une personnalisation à faible latence. Une fois que vous avez choisi une campagne, vous pouvez choisir le type de campagne qui correspond le mieux à votre cas d’utilisation.

Ce guide vous aide à choisir entre les Parcours, les campagnes d’action et les campagnes déclenchées par l’API en fonction du style d’exécution, des besoins en données et du cas d’utilisation, avec une comparaison rapide, une arborescence de décision et des exemples concrets.

>[!NOTE]
>
>Les **campagnes orchestrées** présentent des caractéristiques architecturales distinctes (exécution par lots côté hub, données relationnelles à entités multiples) qui nécessitent des conseils dédiés. Ils ne sont pas inclus dans les tableaux de comparaison ci-dessous afin d’éviter une simplification excessive. [En savoir plus sur les campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

## Comparaison rapide {#quick-overview}

| Approche | Idéal pour | Style d’exécution |
|----------|----------|-----------------|
| **Parcours** | Expériences clients en temps réel et à plusieurs étapes avec logique conditionnelle | Orchestration 1:1 : chaque profil à son propre rythme |
| **Campagnes d’action** | Activations planifiées ou récurrentes vers des audiences | Exécution par lots : audience traitée ensemble au moment de l’envoi |
| **Campagnes déclenchées par API** | Messages déclenchés par un événement ou transactionnels provenant de systèmes externes | Exécution à la demande : déclenchée par un appel API avec payload |

>[!TIP]
>
>**Règle empirique rapide :** avez-vous besoin que chaque client évolue à son propre rythme avec la logique en temps réel ? Utilisez **&#x200B;**. Envoyer un seul message à une audience selon un planning ? Utilisez **Campagnes d’action**. Déclencher un seul message depuis un système externe via l&#39;API ? Utilisez des **campagnes déclenchées par API** — ou un **parcours d’événement unitaire** si vous avez besoin d’une orchestration à plusieurs étapes après l’événement envoyé par l’API. Besoin d’une personnalisation entrante basée sur Edge ? Utilisez **Campagnes d’action**.

## Comparaison détaillée {#detailed-comparison}

Utilisez ce tableau complet pour comprendre les principales différences :

| Fonctionnalité | Parcours | Campagnes d’action | Campagnes déclenchées par API |
|---------|----------|------------------|------------------------|
| **Objectif principal** | Orchestration 1:1 en plusieurs étapes avec contexte client en temps réel | Diffusion de messages ponctuels ou récurrents aux audiences | Messages transactionnels ou pilotés par un événement déclenchés par des systèmes externes |
| **Type de zone de travail** | Zone de travail 1:1 : chaque profil évolue à son propre rythme. | Aucune zone de travail : exécution d’action unique | Aucune zone de travail : exécution d’action unique |
| **Flux d’exécution** | Actions séquentielles, le profil conserve son état tout au long du parcours. | Exécution simultanée pour l’audience entière | Exécution immédiate par appel API |
| **Mécanisme d’entrée** | Événements, audiences, qualifications, événements métier | Activation et planification manuelles | Appel API depuis un système externe |
| **Modèle de données** | Profil en temps réel + données d’événement | Données de profil des audiences Experience Platform | Données de payload de l’API avec recherche de profil facultative |
| **Segmentation** | Audiences préconfigurées + conditions en temps réel | Audiences préconfigurées à partir d’Experience Platform | Ciblage piloté par la payload (aucune audience planifiée) |
| **Traitement du profil** | Individuel, en temps réel (au fur et à mesure des événements) | Par lots, tous en même temps | Par appel API, piloté par la payload |
| **Personnalisation** | Données contextuelles en temps réel + attributs de profil | Attributs de profil | Données de payload + attributs de profil facultatifs |
| **Complexité** | Plusieurs étapes avec embranchement, temps d’attente, conditions | Action unique ou workflow simple | Action unique avec mappage de la payload |
| **Idéal pour** | Parcours du cycle de vie client, intégration, abandon de panier | Campagnes promotionnelles, newsletters, annonces | Confirmations de commande, alertes d’expédition, réinitialisations de mot de passe |
| **Timing** | Continu, toujours actif une fois publié | Dates de début/fin planifiées | À la demande, piloté par les événements via l’API |
| **Gestion des états** | Maintient l’état de la clientèle pour les actions en temps réel. | Exécution sans état | Exécution sans état par appel |
| **À utiliser quand** | Plusieurs points de contact sont nécessaires avec la logique de décision en temps réel. | Message simple à une audience à une heure spécifique | Le système externe doit déclencher un message immédiatement |
| **Fonctionnalités uniques** | Réactions en temps réel, activités d’attente, fréquence basée sur les profils | Planification, ciblage d&#39;audience, contrôle des taux | Mappage de la payload de l’API, déclenchement système à système |

## Guide de décision {#decision-guide}

Suivez cet arbre de décision pour choisir la bonne approche. De nombreuses marques utilisent plusieurs types ; choisissez le meilleur ajustement pour chaque cas d’utilisation.

### Étape 1 : quelle est votre exigence d’exécution ?

**Réponses individuelles en temps réel au comportement des clients ?**
→ **Utiliser des Parcours**
* Les profils doivent progresser à leur propre rythme.
* Logique conditionnelle basée sur le comportement
* Le contexte en temps réel est essentiel.

**Diffusion simple d’un message à une audience à une heure planifiée ?**
→ **Utiliser des campagnes d’action**
* Tous les profils reçoivent le message simultanément.
* Envois planifiés ou récurrents
* Aucune logique complexe à plusieurs étapes n’est nécessaire.

**Message immédiat déclenché par un système externe ?**
→ **utiliser des campagnes déclenchées par API** (message unique) **ou un parcours d’événement unitaire** (orchestration à plusieurs étapes)
* Déclenché à la demande via un appel API : les campagnes diffusent un message ; les parcours unitaires ingèrent l&#39;événement via l&#39;ingestion [Experience Platform](../event/additional-steps-to-send-events-to-journey.md) et exécutent un flux de parcours complet
* Personnalisation basée sur la payload
* Choisissez des campagnes lorsqu’aucune logique à plusieurs étapes n’est nécessaire

**Workflow par lots complexe avec segmentation avancée, données multi-entités ou nombre exact de pré-envois ?**
→ **Utiliser des campagnes orchestrées** — Consultez [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) pour obtenir des conseils détaillés.

>[!NOTE]
>
>* **Composition d’audience ad hoc** — Les campagnes orchestrées vous permettent de définir votre audience cible directement dans la zone de travail de la campagne à l’aide du créateur de règles intégré, sans avoir à précréer et à évaluer d’abord une audience Adobe Experience Platform. [Découvrez comment créer votre première règle](../orchestrated/build-query.md)
>* **Données fédérées** — Utilisez la composition d’audiences fédérées pour interroger votre entrepôt de données d’entreprise et créer ou enrichir des audiences sans importer de données sensibles dans Adobe Experience Platform. [En savoir plus sur la composition d’audiences fédérées](../audience/federated-audience-composition.md)

### Étape 2 : valider votre choix

| Vos besoins | Approche recommandée | Pourquoi |
|-----------|---------------------|-----|
| Accueillir une nouvelle clientèle avec l’intégration en plusieurs étapes | Parcours | Entrée en temps réel, plusieurs points de contact, chemins conditionnels |
| Envoyer une newsletter mensuelle aux personnes abonnées | Campagnes d’action | Message planifié simple à l’audience |
| Abandon de panier avec séquence de rappel | Parcours | Déclencheur en temps réel, temps d’attente, suivi conditionnel |
| Annonce promotionnelle à l’ensemble de la clientèle | Campagnes d’action | Message ponctuel, diffusion immédiate |
| Réengager les personnes inactives en fonction de leur comportement | Parcours | Déclenché par la qualification d’audience, chemin personnalisé |
| Vente flash déclenchée par un événement métier | Parcours (événement métier) | Déclencheur en temps réel affectant plusieurs membres de la clientèle |
| Message transactionnel déclenché par API (envoi unique) | Campagnes déclenchées par API | Déclencheur de système externe, diffusion immédiate en une seule fois |
| Flux à plusieurs étapes déclenché par API | Parcours (Événement unitaire) | Le système externe envoie un événement unitaire via l’API ; le parcours orchestre les étapes de suivi. |
| Workflow par lots complexe avec des données multi-entités | Campagnes orchestrées | Voir [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) |

## Principales distinctions expliquées {#key-distinctions}

### Parcours : orchestration en temps réel 1:1

**Qu’est-ce qui rend cela unique ?**
* Chaque profil conserve un état et un contexte individuels.
* Les profils rejoignent le parcours et progressent à leur propre rythme.
* Prise de décision en temps réel basée sur le comportement et les événements
* Les activités d’attente créent un timing personnalisé.
* L’embranchement conditionnel crée des chemins uniques par profil.
* Écoute active intégrée : l’inaction pendant une période définie peut également déclencher l’étape suivante, et pas seulement des événements explicites. [En savoir plus sur les activités d’attente](../building-journeys/wait-activity.md)
* Limitation de la fréquence : contrôlez la fréquence à laquelle un client peut saisir ou recevoir des messages d&#39;un parcours. [En savoir plus sur la limitation du parcours &#x200B;](../conflict-prioritization/journey-capping.md)
* Fractionnement de l’audience par pourcentage : divisez les profils en groupes aléatoires basés sur un pourcentage pour exécuter des expériences A/B sur plusieurs chemins de parcours. [En savoir plus sur le partage en pourcentage](../building-journeys/condition-activity.md)
* Mode test : validation de la logique de parcours et de la diffusion des messages avec des profils de test avant publication en direct. [En savoir plus sur le mode test](../building-journeys/testing-the-journey.md)

**Exemple de flux :**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Chaque personne voit sa propre chronologie de parcours en fonction de ses actions.

[En savoir plus sur les parcours](../building-journeys/journey.md)

### Campagnes : diffusion simple par lots ou déclenchée

**Qu’est-ce qui rend cela unique ?**
* Tous les profils sont traités de manière identique et simultanée.
* Exécution sans état : aucun contexte conservé
* Planification simple ou déclenchement par API
* Idéal pour les communications de diffusion
* Diffusion entrante multi-surface : ajoutez jusqu’à 10 actions de canal entrant (expérience basée sur le code, in-app, carte de contenu, web) dans une seule campagne, à l’aide des règles de ciblage pour créer des variantes de message en fonction de l’appartenance à l’audience ou des attributs de profil. [En savoir plus](../campaigns/campaign-action.md#multi-action)

**Exemple de flux :**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Tout le monde reçoit le même message en même temps.

**Types :**
* **Campagnes d’action** : diffusion planifiée vers les audiences (ponctuelle ou récurrente)
* **Campagnes déclenchées par API** : diffusion à la demande déclenchée par un appel API avec des données de payload

[En savoir plus sur les campagnes](../campaigns/get-started-with-campaigns.md)

## Exemples de cas d’utilisation {#use-cases}

### Cas d’utilisation de parcours

* **Récupération après abandon de panier** : déclenché par l’événement d’ajout au panier, attente d’un passage en caisse, envoi de rappels en cas d’absence d’achat
* **Intégration de la clientèle** : série de bienvenue à plusieurs étapes avec du contenu personnalisé basé sur les données de profil
* **Mise à niveau du niveau de fidélité** : déclenché lorsque le client ou la cliente atteint un nouveau niveau, en vue d’envoyer des félicitations et des avantages.
* **Campagnes d’anniversaire** : entrée basée sur la date de naissance, offres personnalisées
* **Réengagement** : déclenché par la qualification de l’audience (inactivité), la diffusion progressive

### Cas d’utilisation de Campaign (déclenchés par une action et une API)

**Campagnes d’action :**
* **Newsletters mensuelles** : diffusion par lots planifiée vers le segment des personnes abonnées
* **Annonces promotionnelles** : offres sensibles au facteur temps destinées aux audiences cibles
* **Lancements de produits** : annonce coordonnée à l’intention de l’ensemble de la clientèle
* **Vœux saisonniers** : messages de vœux à des dates spécifiques

**Campagnes déclenchées par l’API :**
* **Confirmations de commande** : déclenchées par le système e-commerce après l’achat
* **Notifications d’expédition** : déclenchées par le système logistique
* **Alertes de comptes** : déclenchées par le système de détection des fraudes
* **Réinitialisations du mot de passe** : déclenchées par une action de la personne dans l’application

## Disponibilité des fonctionnalités {#feature-availability}

### Canaux

| Canal | Parcours | Campagnes d’action | Campagnes déclenchées par API |
|---------|:--------:|:----------------:|:-----------------------:|
| E-mail | ✅ | ✅ | ✅ |
| Notification push | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ |
| In-app | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Basé sur le code | ✅ | ✅ | ❌ |
| Cartes de contenu | ✅ | ✅ | ❌ |
| Courrier | ✅ | ✅ | ❌ |
| LINE | ✅ | ✅ | ✅ |
| WhatsApp | ✅ | ✅ | ✅ |

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
| Déclenchement de l’API | ✅ (événement unitaire uniquement — événement envoyé via l’API) | ❌ | ✅ |
| Données multi-entités | ❌ | ❌ | ❌ |
| Nombres exacts de messages de pré-envoi | ❌ | ❌ | ❌ |
| Segmentation à la demande | ❌ | ❌ | ❌ |
| Optimisation de l’heure d’envoi | ✅ | ❌ | ❌ |
| Tests A/B | ✅ | ✅ | ❌ |
| Workflows d’approbation | ✅ | ✅ | ✅ |

>[!NOTE]
>
>Pour plus d’informations sur les fonctionnalités des campagnes orchestrées, notamment les expériences de contenu, le déclenchement d’API par lots et la segmentation d’entités multiples, consultez la section [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

## Questions courantes {#common-questions}

+++ Puis-je combiner des parcours et des campagnes dans ma stratégie marketing ?

Oui. De nombreuses organisations utilisent toutes les approches pour différents scénarios :

* **&#x200B;**&#x200B;pour l’engagement comportemental en temps réel
* **Campagnes d’action** pour les communications planifiées ou les activations entrantes
* **Campagnes déclenchées par API** pour les messages transactionnels
* **Campagnes orchestrées** pour les campagnes par lots complexes et gourmandes en données, consultez la section [Prise en main des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

Utilisez l’outil approprié pour chaque cas d’utilisation plutôt que de forcer une approche pour tout.

+++

+++ Puis-je convertir une campagne en parcours ou inversement ?

Non, vous devez recréer l’expérience au format approprié. Cependant, vous pouvez réutiliser du contenu, des audiences et des concepts logiques.

+++

+++ Quelle approche est la plus facile à élaborer ?

Les campagnes d’action sont généralement les plus simples (point de contact unique ou engagement diffusé à une audience), suivies de campagnes déclenchées par l’API, puis de Parcours (plus complexes avec une logique à plusieurs étapes).

+++

+++ Quelle est l’approche la plus adaptée aux audiences de grande taille ?

Tous les trois peuvent être adaptés à l’échelle ; le bon choix dépend de votre modèle :

* Les campagnes **Lecture d’audience** et **Action** sont optimisées pour les audiences par lots volumineuses (un message ou flux vers plusieurs profils à la fois).
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
>* [comparaison des types de Parcours &#x200B;](../building-journeys/journey.md#journey-types-comparison)
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
