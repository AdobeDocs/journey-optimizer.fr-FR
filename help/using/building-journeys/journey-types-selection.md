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
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
TQID: https://experienceleague.adobe.com/rEANha6Lppyd5vog-0kZ3aL9VvZHc9kziW-d-jiWqeA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 172377e79df0e214288d5a10e48f449a4009c2fb
workflow-type: tm+mt
source-wordcount: 2053
ht-degree: 26%

---

# Types de parcours et guide de sélection {#journey-types-selection}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment comparer les quatre types de parcours (événement unitaire, lecture d’audience, qualification de l’audience et événement métier) et utiliser le guide de décision et la matrice de compatibilité des fonctionnalités pour choisir le bon type d’événement pour votre cas d’utilisation.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] prend en charge quatre types de parcours, chacun conçu pour différents mécanismes d’entrée et scénarios métier. Ce guide vous aide à comprendre les différences entre les types et à choisir celui qui convient à votre cas d’utilisation.

>[!NOTE]
>
>Vous ne savez pas quel type choisir ? Commencez par les parcours d’événement unitaire **pour les expériences basées sur un événement ou les** parcours de lecture d’audience **pour les campagnes planifiées. Ils couvrent la plupart des cas d’utilisation courants.**

## Vue d’ensemble des types de parcours {#journey-types}

>[!BEGINTABS]

>parcours d’événement unitaires][!TAB 

**Utilisation :** expériences déclenchées par un événement en temps réel

Les parcours d’événement unitaire **sont déclenchés individuellement lorsqu’une action spécifique se produit (achat, connexion à l’application, envoi du formulaire).** Les profils entrent un par un en temps réel, ce qui en fait l’outil idéal pour des réponses immédiates basées sur le comportement.

**Parfait pour :** les confirmations de commande après l’achat, les e-mails de bienvenue lorsque quelqu’un s’abonne, les notifications de réinitialisation de mot de passe et la personnalisation après connexion.

➡️ [En savoir plus sur les événements](../event/about-events.md) | [Cas d’utilisation : message aux personnes abonnées](message-to-subscribers-uc.md)

>[!TAB Parcours de lecture d’audience]

**Utilisation :** campagnes planifiées pour des segments d’audience

**Lire les parcours d’audience** commencez par une audience [!DNL Adobe Experience Platform] et envoyez des messages par lots à tous les profils simultanément. Ce type de parcours est idéal pour les communications planifiées à grande échelle. Utilisez l’option **lecture incrémentielle** sur les parcours récurrents pour traiter uniquement les profils qui ont rejoint l’audience depuis la dernière exécution, plutôt que de retraiter l’audience complète à chaque fois.

**Parfait pour : les newsletters mensuelles** les campagnes promotionnelles pour cibler les segments, les annonces de produits, les séries récurrentes de réengagement et les campagnes marketing saisonnières.

➡️ [En savoir plus sur la lecture d’audience](read-audience.md) | [Commencer avec les audiences](../audience/about-audiences.md)

>[!TAB Parcours de qualification d’audience]

**Utilisation :** réponses en temps réel aux modifications de l’appartenance à l’audience

**Parcours de qualification d’audience** : ils sont déclenchés lorsque les profils se qualifient pour une audience spécifique ou en sortent. Les profils entrent individuellement lorsqu’ils répondent à des critères, ce qui permet un engagement immédiat lorsque le comportement des clients change. Pour le comportement d’entrée en temps réel, l’audience doit être **évaluée en flux continu**; les audiences évaluées par lots déclenchent une entrée uniquement à la fenêtre d’évaluation suivante (jusqu’à 24 heures).

**Parfait pour :** les notifications de mise à niveau de niveau VIP, les messages de célébration du premier achat, les alertes de risque d’attrition et les transitions d’étape du cycle de vie de la fidélité.

➡️ [En savoir plus sur la qualification d’audience](audience-qualification-events.md) | [Création d’audiences](../audience/creating-a-segment-definition.md)

>[!TAB Parcours d’événement métier]

**Utilisation :** conditions métier affectant plusieurs clients et clientes

Les parcours d’événement métier **sont déclenchés par un événement au niveau de l’entreprise (mises à jour d’actions, variations de prix) qui affecte plusieurs profils simultanément.** En interne, le déclencheur d’événement métier est toujours suivi d’une étape Lecture d’audience qui ingère les profils pertinents. De ce fait, l’entrée de profil suit les règles de débit Lecture d’audience, et non le débit d’événement unitaire.

**Parfait pour :** alertes de faible stock aux clients intéressés, annonces de vente flash, notifications de chute de prix et alertes de retour en stock de produits.

➡️ [En savoir plus sur les événements métier](../event/about-creating-business.md) | [Gestion des entrées](entry-management.md)

>[!ENDTABS]

## Guide de décision : choisir votre type de parcours {#decision-guide}

Utilisez le tableau ci-dessous pour faire correspondre votre objectif au type de parcours approprié. Pour la plupart des nouveaux utilisateurs, les parcours **Événement unitaire** ou **Lecture d’audience** couvrent la majorité des cas d’utilisation.

| Votre objectif | Type de parcours recommandé | Pourquoi |
|-----------|--------------------------|-----|
| Envoyer une confirmation de commande après l’achat | Événement unitaire | Réponse immédiate à une action individuelle |
| Envoyer une newsletter mensuelle aux personnes abonnées | Lecture d’audience | Communication par lots planifiée |
| Avertir la clientèle lorsqu’elle atteint le statut VIP | Qualification d’audience | Réponse en temps réel à l’entrée d’audience en flux continu |
| Alerter la clientèle en cas de faible stock des articles suivis | Événement métier | La condition métier affecte plusieurs personnes. |
| Accueillir les nouvelles personnes utilisant l’application | Événement unitaire | Déclenché par l’événement d’inscription |
| Réengager les clients inactifs (récurrent, planifié) | Lecture d’audience | Exécution par lots récurrente pour une audience d’inactivité |
| Promotion saisonnière sur le segment cible | Lecture d’audience | Campagne planifiée vers l’audience |
| Annonce de vente flash | Événement métier | La décision commerciale affecte plusieurs personnes. |
| Réagissez dès qu’un client atteint le niveau de fidélité Gold | Qualification d’audience | Audience de streaming, entrée individuelle en temps réel |

## Comparaison détaillée des types de parcours {#journey-types-comparison}

| Aspect | Parcours d’événements unitaires | Parcours de lecture d’audience | Parcours de qualification d’audience | Parcours d’événement métier |
|--------|------------------------|------------------------|--------------------------------|------------------------|
| **Mécanisme d’entrée** | Déclencheur d’événement individuel | Lot planifié | Modification de l’appartenance à une audience de streaming en temps réel | Événement de niveau professionnel + étape Lecture d’audience |
| **Délai d’entrée** | Temps réel, au fur et à mesure des événements | Planifié (unique ou récurrent) | Temps réel, à mesure que la qualification se produit (audiences en flux continu) ; retardé pour les audiences évaluées par lots | Déclencheur en temps réel ; l’ingestion de profil suit le débit Lecture d’audience |
| **Entrée de profil** | Un à la fois | Tout en une seule fois (par lots) | Un à la fois | Plusieurs profils via l’étape Lecture d’audience interne |
| **Source du déclencheur** | Action de la clientèle (achat, clic, connexion) | Planning basé sur le temps | Entrée ou sortie de l’appartenance à une audience | Condition commerciale (stock, prix) |
| **Idéal pour** | Messages transactionnels, réponses comportementales | Campagnes marketing, newsletters, programmes récurrents | Programmes de fidélité, transitions d’étape du cycle de vie | Alertes de stock, promotions, conditions métier |
| **À utiliser dans les cas suivants** | Réponse immédiate aux actions individuelles nécessaires | Atteindre des segments d’audience volumineux selon le planning | Réponse aux changements de statut du client en temps réel | Les événements métier affectent plusieurs clients simultanément |
| **Exemples** | Confirmation de commande, réinitialisation du mot de passe | Newsletter mensuelle, campagne saisonnière | Mise à niveau de VIP, alerte de risque de résiliation | Alerte de stock faible, vente flash, baisse de prix |
| **Reprise** | Configurable | Une fois par exécution | Configurable par événement de qualification ; un profil déjà dans le parcours ne peut pas entrer à nouveau la même version | Plusieurs profils peuvent être affectés par le même événement. |
| **Débit max** | 5 000 TPS (niveau organisation partagé avec qualification d’audience) | 20 000 TPS par sandbox | 5 000 TPS (niveau d’organisation partagé avec événement unitaire) | Événement métier : 5 000 TPS ; étape Lecture d’audience : 20 000 TPS |
| **Exigences de données** | Schéma d’événement avec données de déclenchement | [!DNL Adobe Experience Platform] une audience | Audience de diffusion en continu (requise pour l’entrée en temps réel) ; audience par lots prise en charge, mais entrée retardée | Schéma d’événement métier |

## Compatibilité des fonctionnalités par type de parcours {#feature-compatibility}

Toutes les fonctionnalités ne sont pas disponibles pour tous les types de parcours. Utilisez cette matrice pour identifier les fonctionnalités qui fonctionnent avec les types de parcours :

| Fonctionnalité | Événement unitaire | Lecture d’audience | Qualification d’audience | Événement métier |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Mécanismes d’entrée** | | | | |
| Entrée déclenchée par un événement | ✅ | ❌ | ❌ | ✅ (l’événement métier déclenche le parcours ; les profils rejoignent le site par le biais d’une étape Lecture d’audience interne) |
| Entrée planifiée | ❌ | ✅ | ❌ | ❌ |
| Entrée basée sur l’audience | ❌ | ✅ (lot) | ✅ (streaming) | ❌ |
| **Fonctionnalités d’orchestration** | | | | |
| Activités d’attente | ✅ | ✅ | ✅ | ✅ |
| Activités de condition | ✅ | ✅ | ✅ | ✅ |
| Actions personnalisées | ✅ | ✅ | ✅ | ✅ |
| Activité Lecture d’audience (dans le parcours) | ✅ | ✅ | ✅ | ✅ |
| Activité Qualification de l’audience (dans le parcours) | ✅ | ✅ | ✅ | ✅ |
| Activité Saut | ✅ | ❌ | ❌ | ✅ |
| **Gestion des profils** | | | | |
| Reprise de profil | ✅ Configurable | ❌ Une fois par exécution | ✅ configurable (le profil déjà dans le parcours ne peut pas entrer à nouveau la même version) | ✅ Par événement |
| Configuration de l’espace de noms | ✅ Requis | ✅ Facultatif | ✅ Requis | ✅ Requis |
| Limite de profils | ✅ | ✅ | ✅ | ✅ |
| **Tests et optimisation** | | | | |
| Mode test | ✅ | ✅ | ✅ | ✅ |
| Test à blanc | ✅ | ✅ | ✅ | ✅ |
| Expériences de chemin (test A/B) | ✅ | ✅ | ✅ | ❌ |
| Optimisation de l’heure d’envoi | ✅ | ✅ | ✅ | ✅ |
| **Canaux** | | | | |
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Notifications push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Messages in-app | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Cartes de contenu | ✅ | ✅ | ✅ | ✅ |
| **Fonctionnalités avancées** | | | | |
| Lecture incrémentielle | ❌ | ✅ | ❌ | ❌ |
| Exporter l’audience | ✅ | ✅ | ✅ | ✅ |
| Gestion des fuseaux horaires | ✅ | ✅ | ✅ | ✅ |
| Événements de réaction | ✅ | ✅ | ✅ | ✅ |
| Sources de données externes | ✅ | ✅ | ✅ | ✅ |
| Plafonnement/limitation | ✅ | ✅ | ✅ | ✅ |

**Légende :** ✅ = pris en charge | ❌ = non pris en charge

>[!NOTE]
>
>Limites des activités de saut : un parcours commençant par une activité Lecture d’audience ou Qualification d’audience ne peut pas contenir d’activité Saut et ne peut pas être la cible d’une activité Saut à partir d’un autre parcours.

## Étapes suivantes {#next-steps}

Maintenant que vous comprenez les types de parcours, vous pouvez effectuer ce qui suit :

* **[Créer votre premier parcours](journey-gs.md)** – Guide détaillé
* **[En savoir plus sur le concepteur de parcours](using-the-journey-designer.md)** – Concevoir la zone de travail de votre parcours
* **[Explorer les fonctionnalités du parcours](journey.md#capabilities)** – Découvrir les fonctionnalités avancées
* **[Voir les questions fréquentes sur les parcours](journey-faq.md)** – Réponses aux questions fréquentes

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page présente une comparaison complète des quatre types de parcours AJO (Événement unitaire, Lecture d’audience, Qualification d’audience et Événement métier), ainsi qu’un guide de décision et une matrice de compatibilité des fonctionnalités pour aider les utilisateurs à choisir le type approprié pour leur cas d’utilisation.

**Intentions:**

* Choisissez le type de parcours approprié pour un cas d’utilisation professionnel donné à l’aide du tableau de décision
* Comparez les types de parcours côte à côte à l’aide de la matrice de compatibilité des fonctionnalités détaillée
* Savoir quand utiliser les parcours Lecture d’audience pour les communications par lots planifiées
* savoir quand utiliser des parcours d’événement unitaires pour les expériences déclenchées par un événement en temps réel ;
* Savoir quand utiliser les parcours de qualification d’audience pour les réponses de changement de statut en temps réel
* Savoir quand utiliser des parcours d’événement métier pour les communications axées sur les conditions commerciales
* comprendre les limites de débit par type de parcours lors de la planification de déploiements à volume élevé ;

**Glossaire:**

* parcours d’événement unitaire **: parcours déclenché par une action individuelle spécifique du client (par exemple, achat, connexion) où les profils en saisissent une à une en temps réel.***(spécifique au produit)*
* parcours Lecture d’audience **: parcours qui commence par une audience Adobe Experience Platform et envoie des messages par lots à tous les profils simultanément selon un planning.***(spécifique au produit)*
* parcours de qualification d’audience **: parcours qui se déclenche lorsque les profils remplissent les critères d’un segment d’audience spécifique ou le quittent.** Nécessite une audience évaluée en flux continu pour le comportement d’entrée en temps réel. *(spécifique au produit)*
* parcours d’événement métier **: parcours déclenché par un événement au niveau de l’entreprise (par exemple, mise à jour des stocks, changement de prix) qui affecte plusieurs profils simultanément ; toujours associé à une étape Lecture d’audience interne pour l’ingestion de profil.***(spécifique au produit)*
* **Lecture incrémentielle** : une fonctionnalité de lecture d’audience qui traite uniquement les profils qui ont rejoint l’audience depuis la dernière exécution, et non l’audience complète à chaque fois. Disponible pour les parcours Lecture d’audience uniquement. *(spécifique au produit)*
* **Audience de diffusion en continu** : audience Adobe Experience Platform évaluée en continu en temps réel, par opposition à une audience par lots évaluée selon un planning (par exemple, quotidiennement). Requis pour que les parcours de qualification d’audience adoptent un comportement d’entrée en temps réel. *(spécifique au produit)*

**Mécanismes de sécurisation :**

* La lecture incrémentielle est disponible uniquement pour les parcours Lecture d’audience, et non pour les parcours Événement unitaire, Qualification d’audience ou Événement métier
* Les expériences de chemin (tests A/B) ne sont pas prises en charge pour les parcours d’événement métier.
* La rentrée du profil dans les parcours Lecture d’audience est limitée à une seule fois par exécution.
* Les parcours Qualification d’audience et Lecture d’audience ne peuvent pas contenir d’activité Saut ni être la cible d’une activité Saut à partir d’un autre parcours
* Les parcours de qualification d’audience nécessitent une audience évaluée par flux pour la saisie en temps réel ; les audiences évaluées par lots entraînent des retards de saisie allant jusqu’à 24 heures
* Les parcours d’événement unitaire et de qualification d’audience partagent une limite de débit de 5 000 TPS au niveau de l’organisation. Les parcours de lecture d’audience prennent en charge jusqu’à 20 000 TPS par sandbox
* Un profil déjà présent dans un parcours ne peut pas entrer à nouveau la même version de ce parcours, quelle que soit la configuration de reprise

**Terminologie:**

* Nom canonique : parcours d’événement unitaire — variantes : parcours déclenché par un événement, parcours unitaire
* Nom canonique : parcours Lecture d’audience - variantes : parcours par lots, parcours de déclenchement de segment, parcours de lecture de segment.
* Nom canonique : parcours de qualification d’audience — variantes : parcours d’événement de qualification d’audience
* Nom canonique : parcours d’événement métier — variantes : parcours déclenché par un événement métier
* Ne les confondez pas : « Lire le parcours d’audience » ≠ « parcours de qualification de l’audience » — Lire l’audience traite tous les membres de l’audience par lots selon le calendrier prévu ; la qualification de l’audience répond aux changements d’appartenance individuels en temps réel (audiences en flux continu uniquement pour une entrée immédiate)
* Ne les confondez pas : « parcours d’événement unitaire » ≠ « parcours d’événement métier » - L’événement unitaire est déclenché par une action du client affectant un profil ; l’événement métier est déclenché par une condition commerciale et ingère plusieurs profils via une étape interne Lecture d’audience .

**FAQ:**

* **Q : Quel type de parcours dois-je utiliser pour une newsletter mensuelle ?** — Utilisez un parcours Lecture d’audience ; il est conçu pour une communication par lots planifiée simultanée à tous les profils d’un segment ciblé.
* **Q : Quel type de parcours gère une confirmation de commande après un achat ?** utilisez un parcours d&#39;événement unitaire qui fournit une réponse immédiate en temps réel à une action individuelle du client.
* **Q : Puis-je exécuter des expériences de chemin A/B dans un parcours d’événement métier ?** — Non ; les expériences de chemin ne sont pas prises en charge pour les parcours d’événement métier.
* **Q : Quelle est la différence entre un parcours d’événement unitaire et un parcours de qualification d’audience ?** — Un parcours d’événement unitaire est déclenché par une action client spécifique (par exemple, un achat) ; un parcours de qualification d’audience se déclenche lorsqu’un profil entre ou sort d’un segment d’audience en fonction de l’évaluation des critères de diffusion en continu.
* **Q : Quels types de parcours prennent en charge la lecture incrémentielle ?** — Seuls les parcours Lecture d’audience prennent en charge la lecture incrémentielle, contrairement aux trois autres types de parcours.
* **Q : Puis-je utiliser une activité Saut dans un parcours Lecture d’audience ?** — Non ; les parcours commençant par une activité Lecture d’audience ou Qualification d’audience ne peuvent pas contenir d’activité Saut et ne peuvent pas être la cible d’un Saut à partir d’un autre parcours.
* **Q : Mon parcours de qualification d’audience ne se déclenche pas en temps réel. Pourquoi ?** — Les parcours de qualification d’audience nécessitent une audience évaluée en flux continu. Si l’audience est évaluée par lots (par exemple, un instantané quotidien), la saisie est retardée jusqu’à la fenêtre d’évaluation suivante, qui peut prendre jusqu’à 24 heures.
* **Q : Quelle est la différence de débit entre les parcours Événement unitaire et Lecture d’audience ?** — Les parcours d’événement unitaire partagent une limite de 5 000 TPS avec les parcours de qualification d’audience au niveau de l’organisation. Lisez Les parcours d’audience prennent en charge jusqu’à 20 000 TPS par sandbox, ce qui les rend mieux adaptés aux campagnes par lots à grande échelle.

+++
