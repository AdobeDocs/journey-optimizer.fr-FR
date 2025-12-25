---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des parcours
description: Prise en main des parcours
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: parcours, découverte, commencer
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 35%

---


# Prise en main des parcours{#jo-general-principle}

Dans Adobe Journey Optimizer, les parcours vous permettent de créer des parcours clients personnalisés et à plusieurs étapes qui s’adaptent en temps réel au comportement et aux besoins de votre audience. Grâce à une zone de travail intuitive par glisser-déposer, vous pouvez orchestrer des messages et des actions sur plusieurs canaux, en exploitant les données contextuelles et le ciblage des audiences pour un impact maximal. Que vous exploriez des déclencheurs en temps réel, gériez des propriétés de parcours ou utilisiez des outils avancés tels que des actions et des expressions personnalisées, cette section fournit une feuille de route claire pour vous aider à concevoir et à affiner des parcours qui offrent des expériences client significatives et opportunes.

Utilisez [!DNL Journey Optimizer] pour créer des cas d’utilisation d’orchestration en temps réel à l’aide de données contextuelles stockées dans des événements ou des sources de données. Vous pouvez concevoir des scénarios avancés à plusieurs étapes avec les fonctionnalités suivantes :

* Envoyez des diffusions **unitaires** en temps réel, déclenchées lorsqu’un [événement](general-events.md) est reçu ou **par lots** à l’aide de Adobe Experience Platform [audiences](read-audience.md).

* Tirez parti des **données contextuelles** issues des [événements](../event/about-events.md), des informations de Adobe Experience Platform ou des données provenant de services d’API tiers via des [sources de données](../datasource/about-data-sources.md).

* Utilisez les **[actions intégrées](journeys-message.md)** pour envoyer des messages conçus dans [!DNL Journey Optimizer] ou créez des **[actions personnalisées](using-custom-actions.md)** si vous utilisez un système tiers pour envoyer vos messages.

* Avec le **[concepteur de parcours](using-the-journey-designer.md)**, créez vos cas d&#39;utilisation à plusieurs étapes : en toute facilité, faites glisser et déposez un événement d&#39;entrée ou une activité [lecture d&#39;audience](read-audience.md), ajoutez des [conditions](condition-activity.md) et envoyez des messages personnalisés.

➡️ [Découvrir Journey Optimizer en vidéo](#video)

## Vue d’ensemble des parcours

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Prise en main de la création de Parcours

Cette section contient des conseils détaillés pour la conception, le test, la publication et le suivi des parcours clients afin de créer des campagnes omnicanal personnalisées.

[Créer votre premier parcours](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Journey Orchestration - Guide complet

Documentation complète couvrant tous les aspects de la création, de la gestion et de l’optimisation des parcours dans Adobe Journey Optimizer.

[Explorer le guide complet](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Gestion des Parcours

Gérez efficacement les parcours des clientes et clients à l’aide d’outils de filtrage, de gestion des profils, de fuseaux horaires et de techniques d’optimisation.

[Découvrir la gestion des parcours](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

Activités De parcours

Découvrez comment configurer et utiliser des activités telles que les déclencheurs, les étapes de décision, la gestion de l’audience et les messages personnalisés dans les parcours.

[Explorer les activités](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Création d’expressions

Maîtrisez la création d’expressions pour les workflows dynamiques, la manipulation de données et l’orchestration de parcours avancée à l’aide d’outils et d’une syntaxe puissants.

[Découvrir les expressions](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Cas d’utilisation de parcours

Explorez les mises en œuvre réelles d’Adobe Journey Optimizer, y compris la messagerie multicanale et l’intégration à des systèmes externes.

[Découvrir les cas d’utilisation](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Que pouvez-vous faire avec des parcours ?

À partir du concepteur de parcours, les spécialistes marketing peuvent envoyer des messages 1:1 déclenchés en temps réel via n’importe quel canal lorsqu’un événement se produit. Par exemple, lorsqu’une personne s’abonne à un service, cela peut [déclencher un e-mail de bienvenue](message-to-subscribers-uc.md) l’incitant à se connecter pour la première fois à l’application et à définir ses préférences. Des actions telles que terminer l’achat, ouvrir l’e-mail et se connecter à l’application peuvent être utilisées pour faire progresser les nouveaux clients et les nouvelles clientes dans leur parcours.

## Types de parcours

Adobe Journey Optimizer prend en charge quatre types de parcours, chacun conçu pour différents cas d’utilisation et mécanismes d’entrée. Choisissez le type approprié en fonction de la manière dont vous souhaitez que les profils rejoignent et progressent dans vos expériences client.

>[!BEGINTABS]

>[!TAB parcours unitaires ]

Les **parcours unitaires** sont déclenchés individuellement par un événement lorsqu’une action spécifique se produit, comme un achat, une connexion à l’application ou un envoi de formulaire. Les profils rejoignent le parcours un par un en temps réel à la réception de l’événement, ce qui le rend idéal pour les expériences personnalisées basées sur le comportement.

**Caractéristiques principales :**

* Entrée en temps réel pilotée par les événements
* Traitement des profils individuels
* Parfait pour les messages transactionnels et les réponses immédiates
* Prend en charge les données contextuelles issues de l’événement déclencheur

**Cas d’utilisation :**

* Confirmation de commande après achat
* E-mail de bienvenue lorsqu’un utilisateur s’abonne
* Abandon de panier déclenché par le comportement de navigation
* Notifications de réinitialisation du mot de passe

➡️ [En savoir plus sur la configuration des événements](../event/about-events.md) | [Événements généraux](general-events.md) | [Cas pratique Message aux abonnés](message-to-subscribers-uc.md)

>[!TAB Lire les parcours d’audience]

**Lisez parcours d’audience** commencez avec une audience de Adobe Experience Platform et envoyez des messages par lots à tous les profils de cette audience. Ce type de parcours traite l’ensemble de l’audience en même temps, ce qui le rend idéal pour les campagnes planifiées et les communications récurrentes.

**Caractéristiques principales :**

* Traitement par lots des segments ciblés
* Exécution planifiée ou ponctuelle
* Tous les profils rejoignent simultanément
* Prise en charge des communications à grande échelle

**Cas d’utilisation :**

* Newsletters mensuelles
* Campagnes promotionnelles vers les segments cibles
* Annonces de produits à tous les clients
* Campagnes marketing saisonnières

➡️ [En savoir plus sur l’activité Lecture d’audience](read-audience.md) | [Prise en main des audiences](../audience/about-audiences.md) | [Cas d’utilisation de la messagerie multicanal](journeys-uc.md)

>[!TAB parcours de qualification d’audience]

Les **parcours de qualification d’audience** sont déclenchés lorsque les profils remplissent les critères d’un segment d’audience spécifique (ou le quittent). Les profils rejoignent le parcours individuellement car ils répondent aux critères d’audience en temps réel, ce qui permet un engagement immédiat lorsque le comportement des clients change.

**Caractéristiques principales :**

* Entrée basée sur la qualification en temps réel
* Surveillance continue de l’appartenance à l’audience
* Traitement des profils individuels tels qu’ils sont qualifiés
* Idéal avec les audiences en flux continu

**Cas d’utilisation :**

* Notifications de mise à niveau du niveau VIP
* Réengagement lorsque les clients deviennent inactifs
* Messages de célébration du premier achat
* Ciblage géographique lors du déplacement des clients

➡️ [En savoir plus sur la qualification de l’audience](audience-qualification-events.md) | [Activité de condition](condition-activity.md) | [Création de définitions de segment](../audience/creating-a-segment-definition.md)

>[!TAB parcours d’événement métier]

Les **parcours d’événement métier** sont déclenchés par des événements métier (tels que des mises à jour de stocks, des alertes météorologiques ou des changements de prix) qui affectent plusieurs profils simultanément. Plutôt que de réagir aux actions individuelles des clients, ces parcours réagissent à des conditions commerciales plus larges ou à des facteurs externes.

**Caractéristiques principales :**

* Déclenché par des événements au niveau de l’entreprise, et non par des actions individuelles
* Affecte plusieurs profils à la fois
* Cible une audience spécifique lorsque l’événement se produit.
* Associe une synchronisation pilotée par les événements à un ciblage d’audience

**Cas d’utilisation :**

* Alertes de faible stock aux clients intéressés
* Annonces de vente Flash
* Promotions basées sur la météo
* Notifications de chute de prix
* Alertes de retour de stock de produit

➡️ [En savoir plus sur les événements métier](general-events.md) | [Configurer des événements métier](../event/about-creating-business.md) | [Gestion des entrées](entry-management.md)

>[!ENDTABS]

## Parcours Designer{#journey-designer}

Le [concepteur de parcours ](using-the-journey-designer.md) fournit tout ce dont les marketeurs et les professionnels du parcours ont besoin pour orchestrer des parcours 1:1 à plusieurs étapes sur plusieurs canaux. Vous y trouverez une zone de travail intuitive par glisser-déposer pour orchestrer chaque étape du parcours, définir l’audience cible et inclure les messages, les offres et le contenu sur les canaux que les membres de l’audience cible verront en fonction du comportement, des données contextuelles et des événements métier.

Le concepteur de parcours fournit tout ce dont vous avez besoin pour concevoir des expériences à plusieurs étapes :

* **[Actions de canal intégrées](journeys-message.md)** - Envoyez des messages par e-mail, notifications push, SMS/MMS, in-app, web, expériences basées sur du code, etc., le tout directement dans Journey Optimizer
* **[Actions personnalisées](using-custom-actions.md)** - Intégrez des systèmes tiers pour envoyer des messages ou déclencher des workflows dans des plateformes externes.
* **[Activités d’orchestration](about-journey-activities.md)** - Ajoutez une logique, des conditions, des temps d’attente et un ciblage d’audience pour créer des expériences client complexes
* **[Conditions](condition-activity.md)** - Branchez votre parcours en fonction des attributs de profil, de l’appartenance à l’audience ou des événements en temps réel
* **[Expressions](expression/expressionadvanced.md)** - Créez une logique et une personnalisation avancées à l’aide de l’éditeur d’expression

Découvrez comment utiliser le concepteur de parcours [dans ces cas d’utilisation complets](jo-use-cases.md).

>[!NOTE]
>
>Les mécanismes de sécurisation et limitations des parcours sont détaillés dans [cette page](../start/guardrails.md).

## Vidéo pratique {#video}

Découvrez les composants d’un parcours et comprenez les principes de base de la création d’un parcours dans la zone de travail.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## Ressources supplémentaires {#additional-resources}

* **[Dépannage des Parcours client](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnostiquez et résolvez les problèmes d’exécution des parcours à l’aide d’outils, de codes d’erreur et des bonnes pratiques de débogage et d’optimisation
* **[Questions fréquentes sur les parcours](journey-faq.md)** : questions fréquentes sur les parcours.
* **[Alertes de Parcours](../reports/alerts.md)** - Configurez des alertes pour la surveillance des parcours et abonnez-vous aux notifications pour les mises à jour en temps réel
* **[Référence des codes d’erreur](error-codes-reference.md)** : codes d’erreur des parcours et étapes de dépannage.
* **[Dépannage](troubleshooting.md)** : problèmes courants des parcours et solutions.
* **[Tutoriels Parcours (vidéos)](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Découvrez la création de parcours au moyen de tutoriels vidéo pratiques couvrant les fonctionnalités, les capacités et les bonnes pratiques
