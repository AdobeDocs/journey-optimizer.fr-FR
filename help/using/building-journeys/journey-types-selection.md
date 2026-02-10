---
solution: Journey Optimizer
product: journey optimizer
title: Types de parcours et guide de sélection
description: Comparez les types de parcours et choisissez celui qui convient à votre cas d’utilisation grâce aux guides de décision et à la matrice de compatibilité des fonctionnalités.
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: types de parcours, unitaire, lecture d’audience, qualification d’audience, événement métier, comparaison, guide de décision, choisir, sélection, temps réel, planifié, par lots, déclenché par un événement
version: Journey Orchestration
hide: true
hidefromtoc: true
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 96%

---

# Types de parcours et guide de sélection {#journey-types-selection}

[!DNL Adobe Journey Optimizer] prend en charge quatre types de parcours, chacun conçu pour différents mécanismes d’entrée et scénarios métier. Ce guide vous aide à comprendre les différences entre les types et à choisir celui qui convient à votre cas d’utilisation.

## Vue d’ensemble des types de parcours {#journey-types}

>[!BEGINTABS]

>[!TAB Parcours unitaires]

**Utilisation :** expériences déclenchées par un événement en temps réel

Les **parcours unitaires** sont déclenchés individuellement lorsqu’une action spécifique se produit (achat, connexion à l’application, envoi de formulaire). Les profils rejognent le parcours un par un en temps réel, ce qui en fait l’outil idéal pour des réponses immédiates basées sur le comportement.

**Parfaits pour :** les confirmations de commande après l’achat, les e-mails de bienvenue lorsque quelqu’un s’abonne, l’abandon de panier déclenché par la navigation et les notifications de réinitialisation de mot de passe.

➡️ [En savoir plus sur les événements](../event/about-events.md) | [Cas d’utilisation : message aux personnes abonnées](message-to-subscribers-uc.md)

>[!TAB Parcours de lecture d’audience]

**Utilisation :** campagnes planifiées pour des segments d’audience

**Lire les parcours d’audience** commencez par une audience [!DNL Adobe Experience Platform] et envoyez des messages par lots à tous les profils simultanément. Ce type de parcours est idéal pour les communications planifiées à grande échelle.

**Parfaits pour :** les newsletters mensuelles, les campagnes promotionnelles pour cibler des segments, les annonces de produits et les campagnes marketing saisonnières.

➡️ [En savoir plus sur la lecture d’audience](read-audience.md) | [Commencer avec les audiences](../audience/about-audiences.md)

>[!TAB Parcours de qualification d’audience]

**Utilisation :** réponses en temps réel aux modifications de l’appartenance à l’audience

**Parcours de qualification d’audience** : ils sont déclenchés lorsque les profils se qualifient pour une audience spécifique ou en sortent. Les profils rejoignent individuellement le parcours lorsqu’ils répondent à des critères en temps réel, ce qui permet un engagement immédiat lorsque le comportement client change.

**Parfaits pour :** les notifications de mise à niveau de niveau VIP, le réengagement lorsque la clientèle devient inactive, les messages de félicitations pour le premier achat et le ciblage géographique lorsque la clientèle se déplace.

➡️ [En savoir plus sur la qualification d’audience](audience-qualification-events.md) | [Création d’audiences](../audience/creating-a-segment-definition.md)

>[!TAB Parcours d’événement métier]

**Utilisation :** conditions métier affectant plusieurs clients et clientes

**Parcours d’événement métier** : ils sont déclenchés par des événements au niveau de l’entreprise (mises à jour des stocks, alertes météorologiques, changements de prix) qui affectent plusieurs profils simultanément. Ils répondent à des conditions métier générales plutôt qu’à des actions individuelles.

**Parfaits pour :** les alertes de faible stock destinées aux clients et clientes intéressés, les annonces de vente flash, les promotions basées sur la météo, les notifications de baisse de prix et les alertes de retour en stock de produits.

➡️ [En savoir plus sur les événements métier](../event/about-creating-business.md) | [Gestion des entrées](entry-management.md)

>[!ENDTABS]

## Guide de décision : choix de votre type de parcours {#decision-guide}

Utilisez cet arbre de décision pour sélectionner le type de parcours qui convient à votre cas d’utilisation :

### Étape 1 : qu’est-ce qui déclenche le parcours ?

* **Le client effectue une action particulière** (achat, clic, connexion) → Passer à l’étape 2
* **Heure/planning** (envoi à une heure spécifique ou récurrent) → **Utiliser un parcours de lecture d’audience**
* **Modifications du statut du client ou de la cliente** (rejoint/quitte un segment) → Passer à l’étape 3
* **Condition métier** (niveau de stock, changement de prix, météo) → **Utiliser un parcours d’événement métier**

### Étape 2 : déclencheurs d’action client individuels

* **Une réponse immédiate et en temps réel est-elle nécessaire ?**
   * Oui → **Utiliser un parcours unitaire**
   * Non → Envisager le parcours de lecture d’audience avec exécution planifiée

### Étape 3 : modifications du statut du client ou de la cliente

* **Est-il nécessaire de répondre lorsque des clients et clientes rejoignent OU quittent un segment ?**
   * Oui → **Utiliser un parcours de qualification d’audience**
   * Non, uniquement lorsqu’ils le rejoignent → Envisager un parcours unitaire avec un événement ou un parcours de lecture d’audience avec un filtre d’audience

### Sélection rapide par cas d’utilisation

| Votre objectif | Type de parcours recommandé | Pourquoi |
|-----------|------------------------|-----|
| Envoyer une confirmation de commande après l’achat | Unitaire | Réponse immédiate à une action individuelle |
| Envoyer une newsletter mensuelle aux personnes abonnées | Lecture d’audience | Communication par lots planifiée |
| Avertir la clientèle lorsqu’elle atteint le statut VIP | Qualification d’audience | Réponse en temps réel au changement de statut |
| Alerter la clientèle en cas de faible stock des articles suivis | Événement métier | La condition métier affecte plusieurs personnes. |
| Accueillir les nouvelles personnes utilisant l’application | Unitaire | Déclenché par l’événement d’inscription |
| Réengager les personnes inactives | Qualification d’audience | Répond à l’entrée de segment d’inactivité |
| Promotion saisonnière sur le segment cible | Lecture d’audience | Campagne planifiée vers l’audience |
| Annonce de vente flash | Événement métier | La décision commerciale affecte plusieurs personnes. |

>[!NOTE]
>
>Vous ne savez pas quel type choisir ? Commencez par les **parcours unitaires** pour les expériences basées sur un événement ou les **parcours de lecture d’audience** pour les campagnes planifiées. Ils couvrent la plupart des cas d’utilisation courants.

## Comparaison détaillée des types de parcours {#journey-types-comparison}

Utilisez ce tableau pour comparer rapidement les types de parcours et choisir celui qui convient à votre cas d’utilisation :

| Aspect | Parcours unitaires | Parcours de lecture d’audience | Parcours de qualification d’audience | Parcours d’événement métier |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Mécanisme d’entrée** | Déclencheur d’événement individuel | Lot planifié | Modification de l’appartenance à une audience en temps réel | Événement au niveau de l’entreprise |
| **Délai d’entrée** | Temps réel, au fur et à mesure des événements | Planifié (unique ou récurrent) | Temps réel, au fur et à mesure de la qualification | En temps réel, lorsque l’événement métier se déclenche. |
| **Entrée de profil** | Un à la fois | Tout en une seule fois (par lots) | Un à la fois | Plusieurs profils simultanément |
| **Source du déclencheur** | Action de la clientèle (achat, clic, connexion) | Planning basé sur le temps | Appartenance à une audience (entrée/sortie) | Condition métier (stock, météo, prix) |
| **Idéal pour** | Messages transactionnels, réponses comportementales | Campagnes marketing, newsletters | Programmes de fidélité, étapes du cycle de vie | Alertes de stock, promotions, conditions métier |
| **À utiliser dans les cas suivants** | Réponse immédiate aux actions individuelles nécessaires | Atteindre des segments d’audience volumineux selon le planning | Réponse aux modifications du statut des clientes et clients | Événements métier affectant plusieurs clientes et clients |
| **Exemples** | Confirmation de commande, réinitialisation du mot de passe | Newsletter mensuelle, campagne saisonnière | Mise à niveau de VIP, alerte d’inactivité | Alerte de stock faible, vente flash, baisse de prix |
| **Reprise** | Configurable (autoriser plusieurs entrées par profil) | Chaque profil entre une fois par exécution. | Configurable par événement de qualification | Plusieurs profils peuvent être affectés par le même événement. |
| **Exigences de données** | Schéma d’événement avec données de déclenchement | [!DNL Adobe Experience Platform] une audience | Audience par lots ou en streaming | Schéma d’événement métier |

## Compatibilité des fonctionnalités par type de parcours {#feature-compatibility}

Toutes les fonctionnalités ne sont pas disponibles pour tous les types de parcours. Utilisez cette matrice pour identifier les fonctionnalités qui fonctionnent avec les types de parcours :

| Fonctionnalité | Unitaire | Lecture d’audience | Qualification d’audience | Événement métier |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Mécanismes d’entrée** |
| Entrée déclenchée par un événement | ✅ | ❌ | ❌ | ✅ |
| Entrée planifiée | ❌ | ✅ | ❌ | ❌ |
| Entrée basée sur l’audience | ❌ | ✅ | ✅ | ❌ |
| **Fonctionnalités d’orchestration** |
| Activités d’attente | ✅ | ✅ | ✅ | ✅ |
| Activités de condition | ✅ | ✅ | ✅ | ✅ |
| Actions personnalisées | ✅ | ✅ | ✅ | ✅ |
| Activité Lecture d’audience (dans le parcours) | ✅ | ✅ | ✅ | ✅ |
| Activité Qualification d’audience | ✅ | ✅ | ✅ | ✅ |
| Activité Saut | ✅ | ✅ | ✅ | ✅ |
| **Gestion des profils** |
| Reprise de profil | ✅ Configurable | ❌ Une fois par exécution | ✅ Configurable | ✅ Par événement |
| Configuration de l’espace de noms | ✅ Requis | ✅ Facultatif | ✅ Requis | ✅ Requis |
| Limite de profils | ✅ | ✅ | ✅ | ✅ |
| **Tests et optimisation** |
| Mode test | ✅ | ✅ | ✅ | ✅ |
| Test à blanc | ✅ | ✅ | ✅ | ✅ |
| Expériences de chemin (test A/B) | ✅ | ✅ | ✅ | ❌ |
| Optimisation de l’heure d’envoi | ✅ | ✅ | ✅ | ✅ |
| **Canaux** |
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Notifications push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Messages in-app | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Cartes de contenu | ✅ | ✅ | ✅ | ✅ |
| **Fonctionnalités avancées** |
| Lecture incrémentielle | ❌ | ✅ | ❌ | ❌ |
| Exporter l’audience | ✅ | ✅ | ✅ | ✅ |
| Gestion des fuseaux horaires | ✅ | ✅ | ✅ | ✅ |
| Événements de réaction | ✅ | ✅ | ✅ | ✅ |
| Sources de données externes | ✅ | ✅ | ✅ | ✅ |
| Plafonnement/limitation | ✅ | ✅ | ✅ | ✅ |

**Légende :** ✅ = pris en charge | ❌ = non pris en charge

## Étapes suivantes {#next-steps}

Maintenant que vous comprenez les types de parcours, vous pouvez effectuer ce qui suit :

* **[Créer votre premier parcours](journey-gs.md)** – Guide détaillé
* **[En savoir plus sur le concepteur de parcours](using-the-journey-designer.md)** – Concevoir la zone de travail de votre parcours
* **[Explorer les fonctionnalités du parcours](journey.md#capabilities)** – Découvrir les fonctionnalités avancées
* **[Voir les questions fréquentes sur les parcours](journey-faq.md)** – Réponses aux questions fréquentes

**Besoin de comparer avec des campagnes ?**

* [Guide de comparaison entre les parcours et les campagnes](../start/journeys-vs-campaigns.md) – Choisir entre les parcours, les campagnes d’action/API et les campagnes orchestrées
