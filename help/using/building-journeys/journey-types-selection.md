---
solution: Journey Optimizer
product: journey optimizer
title: Types de parcours et guide de sélection
description: Comparez les types de parcours et choisissez celui qui convient à votre cas d’utilisation avec les guides de décision et la matrice de compatibilité des fonctionnalités.
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: types de parcours, unitaire, lecture d’audience, qualification d’audience, événement métier, comparaison, guide de décision, choisir, sélection, temps réel, planifié, par lots, déclenché par événement
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: f749eae4e0a826428880e913219cf6f5a135b17c
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 4%

---


# Types de parcours et guide de sélection {#journey-types-selection}

Adobe Journey Optimizer prend en charge quatre types de parcours, chacun conçu pour différents mécanismes d’entrée et scénarios métier. Ce guide vous aide à comprendre les différences et à choisir le type approprié à votre cas d’utilisation.

## Types de parcours - Aperçu {#journey-types}

>[!BEGINTABS]

>[!TAB parcours unitaires ]

**Quand utiliser :** expériences déclenchées par un événement en temps réel

Les **parcours unitaires** sont déclenchés individuellement lorsqu’une action spécifique se produit (achat, connexion à l’application, envoi du formulaire). Les profils entrent un par un en temps réel, ce qui en fait l’outil idéal pour des réponses immédiates basées sur le comportement.

**Parfait pour :** les confirmations de commande après l’achat, les e-mails de bienvenue lorsque quelqu’un s’abonne, l’abandon de panier déclenché par la navigation et les notifications de réinitialisation de mot de passe.

➡️ [En savoir plus sur les événements](../event/about-events.md) | [Cas pratique Message aux abonnés](message-to-subscribers-uc.md)

>[!TAB Lire les parcours d’audience]

**Utilisation :** Campagnes planifiées aux segments d’audience

**Lisez parcours d’audience** commencez par une audience Adobe Experience Platform et envoyez des messages par lots à tous les profils simultanément. Ce type de parcours est idéal pour les communications planifiées à grande échelle.

**Parfait pour : les newsletters mensuelles** les campagnes promotionnelles pour cibler les segments, les annonces de produits et les campagnes marketing saisonnières.

➡️ [En savoir plus sur la lecture d’audience](read-audience.md) | [Prise en main des audiences](../audience/about-audiences.md)

>[!TAB parcours de qualification d’audience]

**Utilisation :** réponses en temps réel aux modifications de l’appartenance à l’audience

**parcours de qualification d’audience** se déclenchent lorsque les profils sont qualifiés pour une audience spécifique (ou en sortent). Les profils entrent individuellement lorsqu’ils répondent à des critères en temps réel, ce qui permet un engagement immédiat lorsque le comportement des clients change.

**Parfait pour :** les notifications de mise à niveau de niveau VIP, le réengagement lorsque les clients deviennent inactifs, les messages de célébration du premier achat et le ciblage géographique lorsque les clients se déplacent.

➡️ [En savoir plus sur la qualification de l’audience](audience-qualification-events.md) | [Création d’audiences](../audience/creating-a-segment-definition.md)

>[!TAB parcours d’événement métier]

**Utilisation :** conditions commerciales affectant plusieurs clients et clientes

Les **parcours d’événement métier** sont déclenchés par des événements au niveau de l’entreprise (mises à jour de stocks, alertes météorologiques, changements de prix) qui affectent plusieurs profils simultanément. Ils répondent à des conditions commerciales plus larges plutôt qu&#39;à des actions individuelles.

**Parfait pour :** les alertes de faible stock destinées aux clients intéressés, les annonces de vente flash, les promotions basées sur la météo, les notifications de chute de prix et les alertes de retour en stock de produits.

➡️ [En savoir plus sur les événements métier](../event/about-creating-business.md) | [Gestion des entrées](entry-management.md)

>[!ENDTABS]

## Guide de décision : choix de votre type de parcours {#decision-guide}

Suivez cette arborescence de décision pour sélectionner le type de parcours approprié à votre cas d’utilisation :

### Étape 1 : qu’est-ce qui déclenche le parcours ?

* **Le client effectue une action spécifique** (achat, clic, connexion) → Passer à l’étape 2
* **Heure/planning** (envoi à une heure spécifique ou récurrent) → **Utiliser le parcours Lecture d’audience**
* **Modifications du statut du client** (joint/quitte un segment) → Accéder à l’étape 3
* **Condition commerciale** (niveau de stock, variation de prix, météo) → **Utiliser le parcours d’événement métier**

### Étape 2 : Déclencheurs d’action client individuels

* **Une réponse immédiate et en temps réel est-elle nécessaire ?**
   * Oui → **Utiliser le parcours unitaire**
   * Ne pas → le parcours Lecture d’audience avec exécution planifiée

### Étape 3 : modifications du statut du client

* **Besoin de répondre lorsque des clients rejoignent OU quittent un segment ?**
   * Oui → **utiliser le parcours de qualification d’audience**
   * Non, uniquement lors de la saisie → Considérer le parcours unitaire avec l’événement ou Lecture d’audience avec le filtre d’audience

### Sélection rapide par cas d’utilisation

| Votre objectif | Type de parcours recommandé | Pourquoi |
|-----------|------------------------|-----|
| Envoyer une confirmation de commande après l&#39;achat | Unitaire | Réponse immédiate à une action individuelle |
| Envoyer une newsletter mensuelle aux abonnés | Lecture d’audience | Communication par lots planifiée |
| Avertir les clients lorsqu’ils atteignent le statut VIP | Qualification de l’audience | Réponse en temps réel au changement de statut |
| Alerter les clients sur le faible stock d’éléments en cours de contrôle | Événement métier | La conjoncture affecte plusieurs clients |
| Bienvenue dans la nouvelle application. | Unitaire | Déclenché par l’événement d’inscription |
| Réengager les clients inactifs | Qualification de l’audience | Répond à l’entrée de segment inactif |
| Promotion saisonnière sur le segment cible | Lecture d’audience | Campagne planifiée vers l’audience |
| Annonce de vente flash | Événement métier | La décision commerciale affecte plusieurs clients |

>[!NOTE]
>
>Vous ne savez pas quel type choisir ? Commencez par les **parcours unitaires** pour les expériences basées sur un événement ou les **parcours de lecture d’audience** pour les campagnes planifiées. Ils couvrent la plupart des cas d’utilisation courants.

## comparaison détaillée des types de parcours {#journey-types-comparison}

Utilisez ce tableau pour comparer rapidement les types de parcours et choisir celui qui convient à votre cas d’utilisation :

| Aspect | Parcours unitaires | Lecture des parcours d’audience | Parcours de qualification d’audience | Parcours d’événement métier |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Mécanisme d’entrée** | Déclencheur d’événement individuel | Lot planifié | Modification de l’appartenance à une audience en temps réel | Événement au niveau de l’entreprise |
| **Délai d’entrée** | Temps réel, au fur et à mesure des événements | Planifié (unique ou récurrent) | Temps réel, à mesure que la qualification est effectuée | En temps réel, lorsque l’événement métier se déclenche |
| **Entrée de profil** | Un à la fois | Tout en une seule fois (par lots) | Un à la fois | Plusieurs profils simultanément |
| **Source du déclencheur** | Action du client (achat, clic, connexion) | Planning basé sur l&#39;heure | Appartenance à une audience (entrée/sortie) | État des affaires (stock, météo, prix) |
| **Idéal pour** | Messages transactionnels, réponses comportementales | Campagnes marketing, newsletters | Programmes de fidélité, étapes du cycle de vie | Alertes d&#39;inventaire, promotions, conditions commerciales |
| **Utiliser quand** | Réponse immédiate aux actions individuelles nécessaires | Atteindre des segments d’audience volumineux selon le calendrier | Réponse aux modifications du statut du client | Les événements métier affectent plusieurs clients |
| **Exemples** | Confirmation de commande, réinitialisation du mot de passe | Newsletter mensuelle, campagne saisonnière | Mise à niveau de VIP, alerte d’inactivité | Alerte de stock faible, vente flash, baisse de prix |
| **Rentrée** | Configurable (autoriser plusieurs entrées par profil) | Chaque profil entre une fois par exécution | Paramétrable par événement de qualification | Plusieurs profils peuvent être affectés par le même événement |
| **Exigences en matière de données** | Schéma des événements avec données de déclenchement | Audience Adobe Experience Platform | Audience par lots ou en flux continu | Schéma des événements métier |

## Compatibilité des fonctionnalités par type de parcours {#feature-compatibility}

Toutes les fonctionnalités ne sont pas disponibles pour tous les types de parcours. Utilisez cette matrice pour identifier les fonctionnalités qui fonctionnent avec les types de parcours :

| Fonctionnalité | Unitaire | Lecture d’audience | Qualification de l’audience | Événement métier |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Mécanismes d’entrée** |
| Entrée déclenchée par événement | ✅ | ❌ | ❌ | ✅ |
| Entrée planifiée | ❌ | ✅ | ❌ | ❌ |
| Entrée basée sur l’audience | ❌ | ✅ | ✅ | ❌ |
| **Fonctionnalités d’orchestration** |
| Activités d’attente | ✅ | ✅ | ✅ | ✅ |
| Activités de condition | ✅ | ✅ | ✅ | ✅ |
| Actions personnalisées | ✅ | ✅ | ✅ | ✅ |
| Activité Lecture d’audience (dans le parcours) | ✅ | ✅ | ✅ | ✅ |
| Activité Qualification de l’audience | ✅ | ✅ | ✅ | ✅ |
| Activité Saut | ✅ | ✅ | ✅ | ✅ |
| **Gestion des profils** |
| Reprise du profil | ✅ configurable | ❌ une fois par exécution | ✅ configurable | ✅ par événement |
| Configuration de l’espace de noms | ✅ obligatoire | ✅ Facultatif | ✅ obligatoire | ✅ obligatoire |
| Limite de profils | ✅ | ✅ | ✅ | ✅ |
| **Tests et optimisation** |
| Mode Test | ✅ | ✅ | ✅ | ✅ |
| Exécution d’essai | ✅ | ✅ | ✅ | ✅ |
| Expériences de chemin (test A/B) | ✅ | ✅ | ✅ | ❌ |
| Optimisation de l’heure d’envoi | ✅ | ✅ | ✅ | ✅ |
| **Canaux** |
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Notifications push | ✅ | ✅ | ✅ | ✅ |
| SMS / MMS | ✅ | ✅ | ✅ | ✅ |
| Messages in-app | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Cartes de contenu | ✅ | ✅ | ✅ | ✅ |
| **Fonctionnalités avancées** |
| Lecture incrémentielle | ❌ | ✅ | ❌ | ❌ |
| Exporter l’audience | ✅ | ✅ | ✅ | ✅ |
| Gestion des fuseaux horaires | ✅ | ✅ | ✅ | ✅ |
| Événements de réaction | ✅ | ✅ | ✅ | ✅ |
| Sources de données externes | ✅ | ✅ | ✅ | ✅ |
| Limitation/Limitation | ✅ | ✅ | ✅ | ✅ |

**Légende :** ✅ = Pris en charge | ❌ = non pris en charge

## Étapes suivantes {#next-steps}

Maintenant que vous comprenez les types de parcours, vous êtes prêt à :

* **[Création de votre premier parcours](journey-gs.md)** - Guide détaillé
* **[En savoir plus sur le concepteur de parcours](using-the-journey-designer.md)** - Concevoir la zone de travail de votre parcours
* **[Explorer les fonctionnalités du parcours](journey.md#capabilities)** - Découvrir les fonctionnalités avancées
* **[Voir la FAQ sur le parcours](journey-faq.md)** - Réponses aux questions courantes

**Besoin de comparer avec des campagnes ?**

* [Guide de comparaison des Parcours et des campagnes](../start/journeys-vs-campaigns.md) - Choisissez entre les parcours, les campagnes Action/API et les campagnes orchestrées

