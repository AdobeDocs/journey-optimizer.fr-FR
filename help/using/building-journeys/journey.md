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
source-git-commit: 87351e845c7a6267cc78c26c838e69e77325f2b8
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 5%

---


# Prise en main des parcours{#jo-general-principle}

Adobe Journey Optimizer vous permet de créer des parcours clients personnalisés et à plusieurs étapes qui s’adaptent en temps réel au comportement et aux besoins de votre audience. Grâce à une zone de travail intuitive par glisser-déposer, vous pouvez orchestrer des messages et des actions sur plusieurs canaux, en exploitant les données contextuelles et le ciblage des audiences pour un impact maximal.

Ce guide fournit une feuille de route claire pour vous aider à comprendre les principes de base du parcours, à choisir le type de parcours approprié à votre cas d’utilisation et à concevoir en toute confiance des parcours qui offrent des expériences client significatives et opportunes.

## Que sont les parcours ?

Les **Parcours** sont des expériences client automatisées à plusieurs étapes qui orchestrent des interactions personnalisées entre les canaux en réponse au comportement des clients, aux événements métier ou aux campagnes planifiées.

Utilisez [!DNL Journey Optimizer] pour :

* Créer **cas d’utilisation d’orchestration en temps réel** à l’aide de données contextuelles stockées dans des événements ou des sources de données
* Concevez des **scénarios avancés à plusieurs étapes** qui répondent dynamiquement au comportement des clients et aux événements métier.
* Diffusez des expériences personnalisées **1:1** à grande échelle par e-mail, notification push, SMS, in-app, web, etc

![Interface du concepteur de parcours avec la palette, la zone de travail et le volet Propriétés](assets/journey38.png)

➡️ **Prêt à commencer la création ?** [Créez votre premier parcours &#x200B;](journey-gs.md) en 5 minutes.

## Choisissez votre type de parcours {#journey-types}

**Avant de commencer la création**, il est important de savoir quel type de parcours correspond à votre cas d’utilisation. Adobe Journey Optimizer prend en charge quatre types de parcours, chacun conçu pour différents mécanismes d’entrée et scénarios métier :

>[!BEGINTABS]

>[!TAB parcours unitaires ]

**Quand utiliser :** expériences déclenchées par un événement en temps réel

Les **parcours unitaires** sont déclenchés individuellement lorsqu’une action spécifique se produit (achat, connexion à l’application, envoi du formulaire). Les profils entrent un par un en temps réel, ce qui en fait l’outil idéal pour des réponses immédiates basées sur le comportement.

**Parfait pour :**

* Confirmations de commande après achat
* E-mails de bienvenue lorsque quelqu’un s’abonne
* Abandon de panier déclenché par la navigation
* Notifications de réinitialisation du mot de passe

➡️ [En savoir plus sur les événements](../event/about-events.md) | [Cas pratique Message aux abonnés](message-to-subscribers-uc.md)

>[!TAB Lire les parcours d’audience]

**Utilisation :** Campagnes planifiées aux segments d’audience

**Lisez parcours d’audience** commencez par une audience Adobe Experience Platform et envoyez des messages par lots à tous les profils simultanément. Ce type de parcours est idéal pour les communications planifiées à grande échelle.

**Parfait pour :**

* Newsletters mensuelles
* Campagnes promotionnelles vers les segments cibles
* Annonces de produit
* Campagnes marketing saisonnières

➡️ [En savoir plus sur la lecture d’audience](read-audience.md) | [Prise en main des audiences](../audience/about-audiences.md)

>[!TAB parcours de qualification d’audience]

**Utilisation :** réponses en temps réel aux modifications de l’appartenance à l’audience

**parcours de qualification d’audience** se déclenchent lorsque les profils sont qualifiés pour une audience spécifique (ou en sortent). Les profils entrent individuellement lorsqu’ils répondent à des critères en temps réel, ce qui permet un engagement immédiat lorsque le comportement des clients change.

**Parfait pour :**

* Notifications de mise à niveau du niveau VIP
* Réengagement lorsque les clients deviennent inactifs
* Messages de célébration du premier achat
* Ciblage géographique lors du déplacement des clients

➡️ [En savoir plus sur la qualification de l’audience](audience-qualification-events.md) | [Création d’audiences](../audience/creating-a-segment-definition.md)

>[!TAB parcours d’événement métier]

**Utilisation :** conditions commerciales affectant plusieurs clients et clientes

Les **parcours d’événement métier** sont déclenchés par des événements au niveau de l’entreprise (mises à jour de stocks, alertes météorologiques, changements de prix) qui affectent plusieurs profils simultanément. Ils répondent à des conditions commerciales plus larges plutôt qu&#39;à des actions individuelles.

**Parfait pour :**

* Alertes de faible stock aux clients intéressés
* Annonces de vente Flash
* Promotions basées sur la météo
* Notifications de chute de prix
* Alertes de retour de stock de produit

➡️ [En savoir plus sur les événements métier](../event/about-creating-business.md) | [Gestion des entrées](entry-management.md)

>[!ENDTABS]

>[!NOTE]
>
>Vous ne savez pas quel type choisir ? Commencez par les **parcours unitaires** pour les expériences basées sur un événement ou les **parcours de lecture d’audience** pour les campagnes planifiées. Ils couvrent la plupart des cas d’utilisation courants.

## Créer avec le concepteur de parcours {#journey-designer}

Le concepteur de parcours **[&#128279;](using-the-journey-designer.md)** est votre zone de travail visuelle pour la création d’expériences client. Grâce à une interface intuitive par glisser-déposer, vous pouvez orchestrer chaque étape de votre parcours sans avoir à écrire de code.

![Interface du concepteur de parcours avec la palette, la zone de travail et le volet Propriétés](assets/journey38.png)

### Ce que vous pouvez faire dans le concepteur :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=fr)

**Définir des points d’entrée**

Choisissez le mode de participation des clients : par le biais d’un événement, d’un segment d’audience ou d’une qualification d’audience.

[En savoir plus sur la gestion des entrées](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

**Envoi de messages**

Utilisez des actions de canal intégrées pour les e-mails, les notifications push, les SMS/MMS, les messages in-app, les messages web, etc., le tout conçu dans Journey Optimizer.

[Envoi de messages dans des parcours](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=fr)

**Ajouter une logique et des conditions**

Branchement de votre parcours en fonction des attributs de profil, de l’appartenance à l’audience ou des événements en temps réel.

[Conditions d’utilisation](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=fr)

**Exploiter les données**

Utilisez des données contextuelles issues d’événements, de Adobe Experience Platform ou de services d’API tiers.

[Utilisation des sources de données](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=fr)

**Connecter des systèmes externes**

Créez des actions personnalisées pour intégrer des systèmes tiers afin d&#39;envoyer des messages ou de déclencher des workflows.

[Configurer des actions personnalisées](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=fr)

**Ajouter des activités d’orchestration**

Utilisez les temps d’attente, les sauts, les mises à jour de profil et la gestion de l’audience pour créer des flux sophistiqués.

[Explorer toutes les activités](about-journey-activities.md)
:::

::::

➡️ **Formation pratique :** [Regardez la vidéo du concepteur de parcours &#x200B;](#video) ou [explorez des cas d’utilisation de bout en bout](jo-use-cases.md)

## Workflow de création de parcours {#workflow}

La création de parcours réussis suit un processus clair et reproductible. Votre workflow détaillé est le suivant :

**1. Plan** → **2. Conception** → **3. Test** → **4. Publication** → **5. Moniteur** → **6. Optimiser**

### &#x200B;1. **Planifier votre parcours** {#plan}

Avant d’ouvrir le concepteur, clarifiez vos objectifs :

* **Quel est l&#39;objectif ?** (par exemple, intégration de nouveaux clients, réengagement des utilisateurs inactifs)
* **Qui est l&#39;audience ?** (segment spécifique, individus pilotés par un événement)
* **Quel type de parcours convient ?** (voir [types de parcours &#x200B;](#journey-types) ci-dessus)
* **Quels canaux allez-vous utiliser ?** (e-mail, notification push, SMS, etc.)

### &#x200B;2. **Conception dans la zone de travail** {#design}

Utilisez le concepteur de parcours pour créer votre flux :

1. **Définir des conditions d’entrée** - Définir comment les profils entrent (événement, audience, qualification)
2. **Ajouter une logique d’orchestration** - Incluez les temps d’attente, les conditions et les points de décision
3. **Configurer les messages** - Concevez vos communications ou utilisez des modèles existants
4. **Configurer des actions** - Configurez les actions intégrées ou personnalisées à exécuter.
5. **Définir les critères de sortie** - Spécifier quand et comment les profils terminent le parcours

[Découvrir comment utiliser le concepteur de parcours →](using-the-journey-designer.md)

### &#x200B;3. **Tester avant la mise en ligne** {#test}

Testez toujours votre parcours pour détecter les problèmes avant que les clients ne les rencontrent :

* Utilisez le **mode test** pour simuler le parcours avec des profils de test
* Utilisez **exécution d’essai** pour prévisualiser l’exécution du parcours sans affecter les données réelles ou envoyer des messages
* Vérifiez que toutes les conditions, tous les messages et toutes les actions fonctionnent comme prévu
* Vérifier la synchronisation, les flux de données et la personnalisation

[Tester votre → de parcours &#x200B;](testing-the-journey.md) | [En savoir plus sur les → d’essai](journey-dry-run.md)

### &#x200B;4. **Publier votre parcours** {#publish}

Une fois le test terminé, publiez pour rendre votre parcours actif :

* Vérifier les paramètres et propriétés finaux
* Publier pour activer pour les clients réels
* Remarque : les parcours en direct peuvent être arrêtés, mais pas modifiés (vous devez en créer une nouvelle version)

[Publier votre → de parcours](publish-journey.md)

### &#x200B;5. **Surveillance des performances** {#monitor}

Suivez les performances réelles de votre parcours :

* Affichage des rapports et des analyses de parcours
* Surveiller les taux d’entrée, de fin et d’erreur
* Configurer des alertes pour les problèmes critiques

[Surveillance et → de rapports](report-journey.md) | [Configurer les alertes →](../reports/alerts.md)

### &#x200B;6. **Optimiser et itérer** {#optimize}

Utilisez les informations pour améliorer :

* Analyse des mesures d’engagement et des taux de conversion
* Test de l’optimisation de l’heure d’envoi
* Création de nouvelles versions de parcours avec des améliorations
* Utiliser les recommandations optimisées par l’IA

[Optimiser vos parcours →](optimize.md) | [→ d’optimisation de l’heure d’envoi](send-time-optimization.md)

➡️ **Prêt à démarrer ?** [Créer votre premier parcours maintenant →](journey-gs.md)

## Cas d’utilisation réels {#use-cases}

Découvrez des exemples pratiques qui montrent comment appliquer des concepts de parcours pour résoudre des problèmes marketing courants :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

**Bienvenue aux nouveaux abonnés**

Lorsqu’un client s’abonne à votre service, déclenchez un parcours de bienvenue qui l’encourage à effectuer les étapes d’intégration.

[Afficher les → de cas d’utilisation](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=fr)

**Optimisation de l’heure d’envoi**

Utilisez l’IA pour diffuser des e-mails lorsque chaque client est le plus susceptible d’interagir, en maximisant les taux d’ouverture et de clics.

[Afficher les → de cas d’utilisation](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

**Accélérer les diffusions**

Augmentez progressivement le volume des messages pour réchauffer votre réputation d&#39;envoi et éviter les problèmes de délivrabilité.

[Afficher les → de cas d’utilisation](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=fr)

**Cible par jour de la semaine**

Envoyez un contenu différent en fonction du jour de la semaine où les clients entrent dans votre parcours pour une meilleure pertinence.

[Afficher les → de cas d’utilisation](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=fr)

**Campagnes multicanaux**

Orchestrez des expériences transparentes sur les canaux e-mail, push, SMS et web dans un seul parcours.

[Afficher les → de cas d’utilisation](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=fr)

**Tous les cas d’utilisation**

Explorez la bibliothèque complète de cas d’utilisation de parcours avec des implémentations détaillées.

[Parcourir toutes les →](jo-use-cases.md) | [Bibliothèque de cas d’utilisation →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explorer les fonctionnalités du parcours {#capabilities}

À mesure que vous vous familiarisez avec la création de parcours, explorez ces puissantes fonctionnalités pour créer des expériences client sophistiquées :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

**Expressions avancées**

Créez des conditions dynamiques et une personnalisation à l’aide de l’éditeur d’expression pour la manipulation de données et une logique complexe.

[Découvrir les expressions](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=fr)

**Gestion des fuseaux horaires**

Gérez les audiences globales avec des ajustements de fuseau horaire automatiques et des heures d’envoi optimales.

[Gérer les fuseaux horaires](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=fr)

**Mode test et essai**

Validez les parcours avec des profils de test avant la mise en ligne et prévisualisez l’exécution sans affecter les données réelles.

[Utiliser le cycle d’essai](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=fr)

**Copier dans le sandbox**

Dupliquez des parcours dans les sandbox pour rationaliser les workflows de test et de déploiement.

[Copier les parcours](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=fr)

**Balises et organisation**

Utilisez les balises pour catégoriser et filtrer les parcours afin d’améliorer la gestion à grande échelle.

[Organiser avec des balises](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=fr)

**Contrôle de débit**

Limitez le débit des messages pour gérer la réputation des envois et éviter de surcharger les systèmes.

[Contrôle du débit](limit-throughput.md)
:::

::::

[Afficher toutes les fonctionnalités du parcours →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Apprendre en regardant {#video}

Obtenez une présentation visuelle des composants de parcours et découvrez les principes de base de la création de parcours dans la zone de travail :

>[!VIDEO](https://video.tv.adobe.com/v/3430351?captions=fre_fr&quality=12)

➡️ **Vous voulez plus de vidéos ?** [Découvrir les tutoriels vidéo parcours &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Besoin d&#39;aide ? {#help}

### Liens rapides pour les tâches courantes

* **[Créer votre premier parcours](journey-gs.md)** - Guide détaillé pour les débutants
* **[FAQ Parcours](journey-faq.md)** - Questions courantes traitées
* **[Dépannage](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnostiquer et résoudre les problèmes
* **[Référence des codes d’erreur](error-codes-reference.md)** - Comprendre les messages d’erreur
* **[Mécanismes de sécurisation et limitations](../start/guardrails.md)** - Limites techniques et bonnes pratiques

### Recevoir des notifications sur les problèmes

Configurez **[les alertes de parcours](../reports/alerts.md)** pour recevoir des notifications en temps réel lorsque les parcours rencontrent des erreurs ou des modèles inhabituels.

### Ressources supplémentaires

* **[hub de gestion des Parcours](/help/rp_landing_pages/manage-journey-landing-page.md)** - Outils de filtrage, d&#39;optimisation et de gestion des profils
* **[Référence des activités de Parcours](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Guide complet de tous les types d’activités
* **[Résolution des problèmes d’exécution](troubleshooting-execution.md)** - Débogage des problèmes d’exécution du parcours
* **[Résolution des problèmes d’activités entrantes](troubleshooting-inbound.md)** - Correction des problèmes d’entrée et de qualification

**Prêt à créer votre premier parcours ?** [Prise en main →](journey-gs.md)
