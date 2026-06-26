---
solution: Journey Optimizer
product: journey optimizer
title: 'types de parcours : choisissez le bon'
description: Comparez les types de parcours et choisissez celui qui convient à votre cas d’utilisation grâce aux guides de décision et à la matrice de compatibilité des fonctionnalités.
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: types de parcours, unitaire, lecture d’audience, qualification d’audience, événement métier, comparaison, guide de décision, choisir, sélection, temps réel, planifié, par lots, déclenché par un événement
version: Journey Orchestration
source-git-commit: d4ed86ea2833c1753d89186a460ba24ae57773fd
workflow-type: tm+mt
source-wordcount: '2109'
ht-degree: 10%

---


# types de parcours : choisissez le bon {#journey-types-selection}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez les quatre types de parcours AJO (événement unitaire, lecture d’audience, qualification de l’audience et événement métier) et trouvez celui qui correspond à votre cas d’utilisation.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] prend en charge quatre types de parcours, chacun conçu pour un type de déclencheur et un scénario d’entreprise différents. Comprendre la différence vous permet de créer une expérience adaptée dès le départ.

## Les quatre types de parcours {#journey-types}

>[!BEGINTABS]

>parcours d’événement unitaires][!TAB 

**Utilisation :** expériences déclenchées par un événement en temps réel

Les parcours d’événement unitaire **sont déclenchés individuellement lorsqu’une action spécifique se produit (achat, connexion à l’application, envoi du formulaire).** Les profils entrent un par un en temps réel, ce qui en fait l’outil idéal pour des réponses immédiates basées sur le comportement.

**Parfait pour : récupération après abandon de panier** intégration d’un nouveau membre, e-mails de bienvenue lorsque quelqu’un s’abonne et personnalisation après connexion.

➡️ [En savoir plus sur les événements](../event/about-events.md) | [Cas d’utilisation de Message aux abonnés](message-to-subscribers-uc.md) | [Créez votre premier parcours ](journey-gs.md)

>[!TAB Parcours de lecture d’audience]

**Utilisation :** campagnes planifiées pour des segments d’audience

**Lire les parcours d’audience** commencez par une audience [!DNL Adobe Experience Platform] et envoyez des messages par lots à tous les profils simultanément. Ce type de parcours est idéal pour les communications planifiées à grande échelle. Utilisez l’option **lecture incrémentielle** sur les parcours récurrents pour traiter uniquement les profils qui ont rejoint l’audience depuis la dernière exécution, plutôt que de retraiter l’audience complète à chaque fois.

**Parfait pour : les newsletters mensuelles** les campagnes promotionnelles pour cibler les segments, les annonces de produits, les séries récurrentes de réengagement et les campagnes marketing saisonnières.

➡️ [En savoir plus sur la lecture d’audience](read-audience.md) | [Prise en main des audiences](../audience/about-audiences.md) | [Créer votre premier parcours ](journey-gs.md)

>[!TAB Parcours de qualification d’audience]

**Utilisation :** réponses en temps réel aux modifications de l’appartenance à l’audience

**Parcours de qualification d’audience** : ils sont déclenchés lorsque les profils se qualifient pour une audience spécifique ou en sortent. Les profils entrent individuellement lorsqu’ils répondent à des critères, ce qui permet un engagement immédiat lorsque le comportement des clients change. Utilisez des audiences **évaluées par flux** — il s’agit du seul type d’audience pris en charge pour cette activité.

>[!CAUTION]
>
>À compter d’**août 2026**, les parcours utilisant une audience par lots dans un nœud de qualification d’audience ne pourront pas être publiés. [Découvrez comment migrer vos parcours ](aq-batch-audiences-migration.md)

**Parfait pour :** les notifications de mise à niveau de niveau VIP, les messages de célébration du premier achat, les alertes de risque d’attrition et les transitions d’étape du cycle de vie de la fidélité.

➡️ [En savoir plus sur la qualification de l’audience](audience-qualification-events.md) | [Création d’audiences](../audience/creating-a-segment-definition.md) | [Création de votre premier parcours ](journey-gs.md)

>[!TAB Parcours d’événement métier]

**Utilisation :** conditions métier affectant plusieurs clients et clientes

Les parcours d’événement métier **sont déclenchés par un événement au niveau de l’entreprise (mises à jour d’actions, variations de prix) qui affecte plusieurs profils simultanément.** En interne, le déclencheur d’événement métier est toujours suivi d’une étape Lecture d’audience qui ingère les profils pertinents. De ce fait, l’entrée de profil suit les règles de débit Lecture d’audience, et non le débit d’événement unitaire.

**Parfait pour :** alertes de faible stock aux clients intéressés, annonces de vente flash, notifications de chute de prix et alertes de retour en stock de produits.

➡️ [En savoir plus sur les événements métier](../event/about-creating-business.md) | [Gestion d’entrée](entry-management.md) | [Créer votre premier parcours ](journey-gs.md)

>[!ENDTABS]

## Quel type devez-vous utiliser ? {#decision-guide}

La réponse se résume généralement à une seule question : *qu’est-ce qui lance le parcours ?*

Si un **client fait quelque chose de spécifique** (abandonne un panier, s’inscrit, effectue un achat), utilisez un **parcours d’événement unitaire**. Il se déclenche immédiatement lorsque l’action se produit, un profil à la fois.

Si vous souhaitez **atteindre un public selon un calendrier** (newsletter mensuelle, campagne saisonnière, série récurrente de réengagement), utilisez un **parcours Lecture d’audience**. Vous définissez l’audience et le timing ; AJO traite tout le monde en même temps.

Si vous souhaitez répondre **au moment où un client atteint un jalon** (adhésion à un niveau de fidélité, atteinte d’un seuil de risque de résiliation, premier achat terminé), utilisez un **parcours de qualification de l’audience**. Il se déclenche dès que l’appartenance à l’audience de diffusion en continu change, et non selon un planning fixe.

Si quelque chose change **dans votre entreprise** qui affecte plusieurs clients à la fois (un niveau de stock baisse, un prix change, une vente démarre), utilisez un **parcours d&#39;événement métier**.

>[!TIP]
>
>**Vous ne savez pas par où commencer ?** La plupart des équipes commencent par **Événement unitaire** pour les expériences déclenchées par le comportement et **Lecture d’audience** pour les campagnes. Ces deux cas couvrent la majorité des cas d’utilisation.

| Votre objectif | Type de parcours recommandé | Pourquoi |
|-----------|--------------------------|-----|
| Récupérer un panier abandonné | Événement unitaire | Réponse immédiate à un comportement individuel |
| Envoyer une newsletter mensuelle aux personnes abonnées | Lecture d’audience | Communication par lots planifiée |
| Avertir la clientèle lorsqu’elle atteint le statut VIP | Qualification d’audience | Réponse en temps réel à l’entrée d’audience en flux continu |
| Alerter la clientèle en cas de faible stock des articles suivis | Événement métier | La condition métier affecte plusieurs personnes. |
| Accueillir les nouvelles personnes utilisant l’application | Événement unitaire ou qualification d’audience | Événement d’inscription (événement unitaire) ou entrée dans une audience de diffusion en continu pour un nouvel utilisateur (qualification d’audience) |
| Réengager les clients inactifs (récurrent, planifié) | Lecture d’audience | Exécution par lots récurrente pour une audience d’inactivité |
| Promotion saisonnière sur le segment cible | Lecture d’audience | Campagne planifiée vers l’audience |
| Annonce de vente flash | Événement métier | La décision commerciale affecte plusieurs personnes. |
| Réagissez dès qu’un client atteint le niveau de fidélité Gold | Qualification d’audience | Audience de streaming, entrée individuelle en temps réel |

## Référence de disponibilité des fonctionnalités {#feature-compatibility}

Tous les types de parcours prennent en charge l’ensemble des canaux AJO (e-mail, notification push, SMS, in-app, web, cartes de contenu), les activités d’orchestration principales (attente, condition, actions personnalisées), le mode test, l’exécution d’essai et l’optimisation de l’heure d’envoi. Le tableau ci-dessous présente uniquement les fonctionnalités qui diffèrent selon les types.

>[!NOTE]
>
>Limites des activités de saut : un parcours commençant par une activité Lecture d’audience ou Qualification d’audience ne peut pas contenir d’activité Saut et ne peut pas être la cible d’une activité Saut à partir d’un autre parcours.
>
>L’activité Lecture d’audience, car l’entrée de parcours n’est disponible que dans les parcours **Lecture d’audience** et **Événement métier**. Elle ne peut pas être ajoutée aux parcours d’entrée Événement unitaire ou Qualification d’audience.

| Fonctionnalité | Événement unitaire | Lecture d’audience | Qualification d’audience | Événement métier |
|-----------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Entrée** | | | | |
| Entrée déclenchée par un événement | ✅ | ❌ | ❌ | ✅ (l’événement métier déclenche le parcours ; les profils rejoignent le site par le biais d’une étape Lecture d’audience interne) |
| Entrée planifiée | ❌ | ✅ | ❌ | ❌ |
| Entrée basée sur l’audience | ❌ | ✅ (lot) | ✅ (streaming uniquement) | ❌ |
| **Orchestration** | | | | |
| Activité Lecture d’audience (entrée de parcours) | ❌ | ✅ | ❌ | ✅ (étape automatique après événement métier) |
| Activité Saut | ✅ | ❌ | ❌ | ✅ |
| **Gestion des profils** | | | | |
| Reprise de profil | ✅ Configurable | ❌ Une fois par exécution par défaut ([Forcer une reprise sur une périodicité](read-audience.md#schedule) disponible) | ✅ configurable (le profil déjà dans le parcours ne peut pas entrer à nouveau la même version) | ✅ Par événement |
| **Optimisation** : | | | | |
| Expériences de chemin (test A/B) | ✅ | ✅ | ✅ | ❌ |
| **Avancé** | | | | |
| Lecture incrémentielle | ❌ | ✅ | ❌ | ❌ |
| Débit maximal | 5 000 TPS (niveau organisation partagé avec qualification d’audience) | 20 000 TPS par sandbox | 5 000 TPS (niveau d’organisation partagé avec événement unitaire) | Événement métier : 5 000 TPS ; étape Lecture d’audience : 20 000 TPS |

**Légende :** ✅ = pris en charge | ❌ = non pris en charge

## Étapes suivantes {#next-steps}

Maintenant que vous avez choisi un type de parcours :

* **[Créer votre premier parcours](journey-gs.md)** — Guide détaillé de l’entrée à la publication
* **[En savoir plus sur le concepteur de parcours](using-the-journey-designer.md)** — Concevez la zone de travail de votre parcours
* **[Entrée de profil dans parcours](entry-management.md)** — Règles d’entrée, reprise et débit par type
* **[Prise en main de parcours](journey.md)** — Présentation des principes fondamentaux et des fonctionnalités
* **[FAQ Journey Orchestration](journey-faq.md)** — Questions courantes traitées

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
* Par défaut, la rentrée du profil dans les parcours Lecture d’audience est limitée à une seule fois par exécution. Utilisez Forcer une rentrée sur une périodicité lors des exécutions planifiées pour permettre aux profils de rentrer à nouveau lors de la prochaine exécution
* L’activité Lecture d’audience est uniquement disponible en tant qu’entrée de parcours dans les parcours d’événement Lecture d’audience et Entreprise , et non dans les parcours d’entrée Événement unitaire ou Qualification d’audience .
* Les parcours Qualification d’audience et Lecture d’audience ne peuvent pas contenir d’activité Saut ni être la cible d’une activité Saut à partir d’un autre parcours
* Les parcours de qualification d’audience nécessitent une audience évaluée en flux continu. À compter d’août 2026, les audiences évaluées par lots ne pourront plus être utilisées dans un nœud de qualification d’audience. Consultez le [ guide de migration](aq-batch-audiences-migration.md)
* Les parcours d’événement unitaire et de qualification d’audience partagent une limite de débit de 5 000 TPS au niveau de l’organisation. Les parcours de lecture d’audience prennent en charge jusqu’à 20 000 TPS par sandbox
* Un profil déjà présent dans un parcours ne peut pas entrer à nouveau la même version de ce parcours, quelle que soit la configuration de reprise

**Terminologie:**

* Nom canonique : parcours d’événement unitaire — variantes : parcours déclenché par un événement, parcours unitaire
* Nom canonique : Lire le parcours d’audience - variantes : parcours par lots
* Nom canonique : parcours de qualification d’audience — variantes : parcours d’événement de qualification d’audience
* Nom canonique : parcours d’événement métier — variantes : parcours déclenché par un événement métier
* Ne les confondez pas : « Lire le parcours d’audience » ≠ « parcours de qualification de l’audience » — Lire l’audience traite tous les membres de l’audience par lots selon le calendrier prévu ; la qualification de l’audience répond aux changements d’appartenance individuels en temps réel (audiences en flux continu uniquement pour une entrée immédiate)
* Ne les confondez pas : « parcours d’événement unitaire » ≠ « parcours d’événement métier » - L’événement unitaire est déclenché par une action du client affectant un profil ; l’événement métier est déclenché par une condition commerciale et ingère plusieurs profils via une étape interne Lecture d’audience .

**FAQ:**

* **Q : Quel type de parcours dois-je utiliser pour une newsletter mensuelle ?** — Utilisez un parcours Lecture d’audience ; il est conçu pour une communication par lots planifiée simultanée à tous les profils d’un segment ciblé.
* **Q : Quel type de parcours dois-je utiliser pour récupérer un panier abandonné ?** — Utilisez un parcours d&#39;événement unitaire ; il se déclenche immédiatement lorsque l&#39;événement d&#39;abandon se produit et répond au comportement de l&#39;individu en temps réel.
* **Q : Puis-je exécuter des expériences de chemin A/B dans un parcours d’événement métier ?** — Non ; les expériences de chemin ne sont pas prises en charge pour les parcours d’événement métier.
* **Q : Quelle est la différence entre un parcours d’événement unitaire et un parcours de qualification d’audience ?** — Un parcours d’événement unitaire est déclenché par une action client spécifique (par exemple, un achat) ; un parcours de qualification d’audience se déclenche lorsqu’un profil entre ou sort d’un segment d’audience en fonction de l’évaluation des critères de diffusion en continu.
* **Q : Quels types de parcours prennent en charge la lecture incrémentielle ?** — Seuls les parcours Lecture d’audience prennent en charge la lecture incrémentielle, contrairement aux trois autres types de parcours.
* **Q : Puis-je ajouter une activité Lecture d’audience à un parcours d’événement unitaire ?** — Non ; l&#39;activité Lecture d&#39;audience est uniquement disponible en tant qu&#39;entrée de parcours dans les parcours Lecture d&#39;audience et Événement métier.
* **Q : Puis-je utiliser une activité Saut dans un parcours Lecture d’audience ?** — Non ; les parcours commençant par une activité Lecture d’audience ou Qualification d’audience ne peuvent pas contenir d’activité Saut et ne peuvent pas être la cible d’un Saut à partir d’un autre parcours.
* **Q : Puis-je accueillir de nouveaux utilisateurs de l’application avec un parcours de qualification d’audience ?** — Oui, si l’entrée est pilotée par une audience de diffusion en continu (par exemple, lorsqu’un profil rejoint un segment de nouvel utilisateur) ; un parcours d’événement unitaire d’inscription est également un modèle courant.
* **Q : Mon parcours de qualification d’audience ne se déclenche pas en temps réel. Pourquoi ?** — Les parcours de qualification d’audience nécessitent une audience évaluée en flux continu. L’utilisation d’une audience évaluée par lots est obsolète et sera bloquée à partir d’août 2026. [Voir le guide de migration](aq-batch-audiences-migration.md)
* **Q : Quelle est la différence de débit entre les parcours Événement unitaire et Lecture d’audience ?** — Les parcours d’événement unitaire partagent une limite de 5 000 TPS avec les parcours de qualification d’audience au niveau de l’organisation. Lisez Les parcours d’audience prennent en charge jusqu’à 20 000 TPS par sandbox, ce qui les rend mieux adaptés aux campagnes par lots à grande échelle.

+++
