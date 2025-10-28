---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes sur Parcours
description: Questions fréquentes sur les Parcours Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: parcours, questions, réponses, dépannage, aide, guide
version: Journey Orchestration
source-git-commit: fa4849cfbb43d74ab85437f00acf6da750080cca
workflow-type: tm+mt
source-wordcount: '5125'
ht-degree: 2%

---


# Questions fréquentes {#faq-journeys}

Vous trouverez ci-dessous les questions fréquentes sur les Parcours Adobe Journey Optimizer.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la [communauté Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

## Concepts généraux

+++ Qu’est-ce qu’un parcours dans Adobe Journey Optimizer ?

Un parcours est une orchestration en plusieurs étapes qui vous permet de concevoir et d’exécuter des expériences client en temps réel sur plusieurs canaux. Les parcours combinent des événements, des activités d’orchestration, des actions et des messages pour créer des expériences contextuelles personnalisées basées sur le comportement du client et des événements métier.

En savoir plus sur [parcours](journey.md).

+++

+++ Quels sont les différents types de parcours ?

Adobe Journey Optimizer prend en charge quatre types de parcours :

* **parcours unitaires** : ils sont déclenchés individuellement par un événement (par exemple, un achat, une connexion à l’application). Les profils rejoignent le parcours un par un lorsque l’événement se produit.
* **Lire les parcours d’audience** : commencez avec une audience de Adobe Experience Platform et envoyez des messages par lots à tous les profils de cette audience.
* **parcours de qualification d’audience** : déclenché lorsque les profils sont qualifiés pour un segment d’audience spécifique (ou en sortent). Les profils rejoignent le parcours car ils répondent aux critères d’audience.
* **parcours d’événement métier** : ils sont déclenchés par des événements métier (par exemple, les mises à jour de stocks, les alertes météorologiques) qui affectent plusieurs profils simultanément.

En savoir plus sur les [types de parcours ](entry-management.md#types-of-journeys).

+++

+++ Quelle est la différence entre un parcours et une campagne ?

Les **[Parcours](journey.md)** sont des orchestrations à plusieurs étapes qui réagissent aux événements ou aux audiences cibles, en tenant compte d’une logique complexe, des conditions, des temps d’attente et de plusieurs points de contact tout au long du cycle de vie du client.

Les **[campagnes](../campaigns/get-started-with-campaigns.md)** se divisent en trois types :

* **[Campagnes d’action](../campaigns/create-campaign.md)** : communications ponctuelles ou récurrentes envoyées à une audience spécifique, idéales pour les messages autonomes tels que les annonces promotionnelles ou les newsletters.
* **[Campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md)** : campagnes déclenchées par le biais d’appels d’API, ce qui permet l’intégration à des systèmes externes pour envoyer des messages en fonction des événements en temps réel ou de la logique commerciale.
* **[Campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)** : campagnes à plusieurs étapes basées sur l’audience, créées sur une zone de travail qui peut inclure des conditions, des temps d’attente et plusieurs actions pour créer des expériences planifiées et coordonnées.

**Bonne pratique** : utilisez [parcours](journey.md) pour un engagement complexe déclenché par un événement avec une orchestration avancée ; [campagnes d’action](../campaigns/create-campaign.md) pour des communications planifiées basées sur une audience ; [campagnes déclenchées par une API](../campaigns/api-triggered-campaigns.md) pour un déclenchement programmatique à partir de systèmes externes ; et [campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) pour des communications à plusieurs étapes avec des exigences spécifiques à la campagne.

+++

+++ Quels sont les principaux composants d’un parcours ?

Un parcours comprend :

* **Événements** : points d’entrée qui déclenchent le parcours (par exemple, qualification du profil, événements métier)
* **Activités d’orchestration** : composants logiques tels que les conditions, l’attente, la lecture d’audience et la fin
* **Actions** : activités qui effectuent des tâches, comme envoyer des messages, mettre à jour des profils ou appeler des API externes
* **Actions de canal intégrées** : fonctionnalités de messagerie natives pour les e-mails, SMS, notifications push et autres canaux
* **Actions personnalisées** : intégration à des systèmes tiers

En savoir plus sur les [activités de parcours ](about-journey-activities.md).

+++

+++ Quels types d’audiences sont pris en charge dans les parcours et quelles sont leurs limites ?

Adobe Journey Optimizer prend en charge quatre types d’audiences, chacune ayant des caractéristiques et des mécanismes de sécurisation différents :

**1. Audiences en flux continu**

* **Description** : audiences qui sont évaluées en temps réel à mesure que les données de profil changent
* **Évaluation** : évaluation continue lorsque les attributs ou les événements de profil correspondent aux critères du segment
* **Utilisation du Parcours** : pris en charge dans les activités Lecture d’audience, Qualification d’audience et Condition
* **Idéal pour** : engagement en temps réel basé sur des changements de comportement ou des mises à jour de profil.
* **Mécanismes de sécurisation** :
   * La taille maximale de l’audience dépend de votre licence Journey Optimizer
   * Latence d’évaluation généralement inférieure à 5 minutes
   * Une logique de segment complexe peut avoir un impact sur les performances d’évaluation

**2. Audiences par lots**

* **Description** : audiences évaluées selon un calendrier (généralement quotidien)
* **Évaluation** : traitement par lots à intervalles planifiés
* **Utilisation du Parcours** : prise en charge dans les activités Lecture d’audience et Condition ; prise en charge limitée dans les parcours de qualification d’audience
* **Idéal pour** : campagnes régulières, newsletters, communications planifiées
* **Mécanismes de sécurisation** :
   * L’évaluation a lieu une fois par jour (par défaut) ou selon le planning configuré
   * Les profils peuvent ne pas refléter les modifications en temps réel avant la prochaine évaluation
   * L’activité Lecture d’audience peut traiter efficacement de grandes audiences par lots

**3. Chargement d’audiences (chargement personnalisé)**

* **Description** : audiences créées en chargeant des fichiers CSV avec des identifiants de profil
* **Évaluation** : liste statique mise à jour uniquement lorsque de nouveaux fichiers sont chargés
* **Utilisation du Parcours** : pris en charge dans les activités Lecture d’audience et Condition ; **non pris en charge** dans les parcours de qualification d’audience
* **Idéal pour** : campagnes ponctuelles, importations de listes externes, communications ciblées.
* **Mécanismes de sécurisation** :
   * Des limites de taille de fichier CSV s’appliquent (consultez la documentation du produit pour connaître les limites actuelles).
   * Les membres de l’audience sont statiques jusqu’à ce qu’ils soient actualisés avec un nouveau chargement
   * L’espace de noms d’identité doit correspondre à l’espace de noms du parcours.
   * Les profils doivent exister dans Adobe Experience Platform

**4. Audiences de composition d’audiences fédérées (FAC)**

* **Description** : audiences créées à l’aide de données fédérées, ce qui vous permet d’interroger et de composer des audiences à partir d’entrepôts de données externes sans copier de données dans Adobe Experience Platform
* **Évaluation** : composition statique mise à jour lors de l’exécution de la composition de l’audience fédérée
* **Utilisation du Parcours** : pris en charge dans les activités Lecture d’audience et Condition ; **non pris en charge** dans les parcours de qualification d’audience (similaire au chargement d’audiences du point de vue du serveur principal)
* **Idéal pour** : intégration d’Enterprise Data Warehouse, composition de l’audience à l’aide de sources de données externes, scénarios nécessitant que les données restent dans des systèmes externes.
* **Mécanismes de sécurisation** :
   * Les membres de l’audience sont statiques jusqu’à la prochaine exécution de composition fédérée.
   * L’espace de noms d’identité doit correspondre à l’espace de noms du parcours.
   * Les performances dépendent des fonctionnalités de requête de l’entrepôt de données externe
   * Nécessite un module complémentaire de composition d’audience fédérée

**Audiences Customer Journey Analytics (CJA)**:

Bien que les audiences CJA ne soient pas directement prises en charge dans parcours, vous pouvez utiliser une **solution** en « enveloppant » une audience CJA dans une règle de segmentation. Cela crée une audience UPS (Unified Profile Service) par lots qui fait référence à l’audience CJA, ce qui la rend disponible pour une utilisation dans parcours en tant que type d’audience par lots.

**Remarques spécifiques au Parcours** :

* **Lire les parcours d’audience** : les quatre types d’audience pris en charge ; l’exportation par lots se produit lors de l’exécution du parcours
* **parcours de qualification d’audience** : audiences en flux continu recommandées ; les audiences par lots ont une détection de qualification retardée ; les audiences de chargement et d’analyse de contenu publicitaire ne sont pas prises en charge
* **Activités de condition** : tous les types d’audience peuvent être utilisés pour vérifier l’appartenance
* **Alignement des espaces de noms** : l’espace de noms d’identité d’audience doit correspondre à celui du parcours pour identifier correctement le profil

**Bonnes pratiques** :

* Utilisez des **audiences en flux continu** pour les parcours en temps réel pilotés par les événements et nécessitant une réponse immédiate
* Utilisez des **audiences par lots** pour les communications planifiées où l’évaluation quotidienne est suffisante
* Utilisez **charger des audiences** pour les campagnes ponctuelles ciblées avec des listes externes
* Utilisez les audiences **AEC** lorsque vous devez exploiter les fonctionnalités de Data Warehouse d’entreprise sans duplication des données
* Surveiller la taille de l’audience et les performances d’évaluation dans les déploiements à grande échelle
* Tenez compte des taux d’actualisation de l’audience lors de la conception du timing et des conditions d’entrée du parcours

En savoir plus sur les [audiences](../audience/about-audiences.md), [création de segments](../audience/creating-a-segment-definition.md), [audiences de chargement personnalisées](../audience/custom-upload.md) et [composition d’audiences fédérées](../audience/federated-audience-composition.md).

+++

+++ Comment choisir entre un parcours unitaire et un parcours Lecture d’audience ?

Utilisez **parcours unitaires** lorsque :

* Vous devez réagir en temps réel aux actions de chaque client (par exemple, confirmation d’achat, abandon de panier)
* Chaque client doit progresser à son propre rythme
* Vous souhaitez déclencher en fonction d’événements spécifiques

Utilisez **lire les parcours d’audience** lorsque :

* Vous envoyez des communications par lots à un groupe (par exemple, newsletter mensuelle, campagnes promotionnelles).
* Tous les clients doivent recevoir le message à peu près au même moment
* Vous ciblez un segment ciblé prédéfini

+++

## Création de parcours

+++ Comment puis-je commencer à créer mon premier parcours ?

Procédez comme suit :

1. **Configurer les conditions préalables** : configurez les événements, les sources de données et les actions selon les besoins
2. **Création du parcours** : accédez au menu Parcours et cliquez sur « Créer un Parcours ».
3. **Définir les propriétés du parcours** : définissez le nom, la description et d’autres paramètres du parcours
4. **Conception du parcours** : faites glisser et déposez les activités de la palette vers la zone de travail
5. **Tester le parcours** : utilisez le mode test pour valider la logique de parcours
6. **Exécution d’essai du parcours** : utilisez l’exécution d’essai pour tester le parcours à l’aide de données de production réelles sans contacter de vrais clients ni mettre à jour les informations de profil
7. **Publier le parcours** : activez le parcours pour le rendre actif

Suivez le [guide détaillé](journey-gs.md).

+++

+++ Quelles sont les conditions préalables requises avant de créer un parcours ?

Les prérequis dépendent de votre type de parcours :

* **parcours déclenchés par un événement** : configurez les événements pour définir quand les profils doivent entrer dans le parcours
* **parcours basés sur l’audience** : création d’audiences dans Adobe Experience Platform
* **Enrichissement des données** : configurez les sources de données pour récupérer des informations supplémentaires
* **Intégrations tierces** : configuration des actions personnalisées si vous utilisez des systèmes externes

En savoir plus sur la configuration du parcours [](../configuration/about-data-sources-events-actions.md).

+++

+++ Puis-je utiliser des données provenant de systèmes externes dans mon parcours ?

Oui, il existe plusieurs approches pour exploiter les données externes :

**Bonnes pratiques** :

* **Actions personnalisées** : appelez des API externes par le biais d’actions personnalisées pour récupérer ou envoyer des données à des systèmes tiers. Il s’agit de l’approche recommandée pour les interactions en temps réel avec des systèmes externes.
* **Recherche de jeu de données** : si vous pouvez charger des données à partir de systèmes externes dans Adobe Experience Platform, utilisez la fonction de recherche de jeu de données pour récupérer les informations stockées dans les jeux de données Experience Platform.
* **Sources de données externes** : configurez les sources de données externes pour récupérer les informations des services d’API tiers (moins recommandé que les approches ci-dessus).

Ces options vous permettent d’enrichir l’expérience client avec des données provenant de votre CRM, de vos systèmes de fidélité, de vos services météorologiques ou d’autres plateformes externes.

En savoir plus sur les [actions personnalisées](using-custom-actions.md) et [recherche de jeu de données](dataset-lookup.md).

+++

+++ Comment ajouter des conditions à mon parcours ?

Vous pouvez ajouter des conditions à l’aide de l’activité **Condition** de la palette d’orchestration. Les conditions vous permettent d’effectuer les opérations suivantes :

* Créer des conditions simples ou avancées à l’aide de l’éditeur d’expression
* Divisez le parcours en plusieurs chemins d’accès en fonction des attributs de profil, de l’appartenance à l’audience, des événements ou des données contextuelles
* Définir des chemins de temporisation pour les profils qui ne remplissent pas la condition dans un délai spécifié

En savoir plus sur les [ conditions ](condition-activity.md).

+++

+++ Puis-je envoyer des messages aux profils d&#39;un parcours ?

Oui. Journey Optimizer comprend des **actions de canal intégrées** qui vous permettent d’envoyer des messages par e-mail, des notifications push, des SMS/MMS/RCS, des messages in-app, des expériences web, des expériences basées sur du code, du courrier, des cartes de contenu, WhatsApp et LINE. Vous pouvez concevoir le contenu des messages directement dans Journey Optimizer et les ajouter en tant qu’activités d’action dans votre parcours.

Pour les canaux non pris en charge en mode natif, vous pouvez utiliser des **actions personnalisées** pour intégrer des plateformes de messagerie externes et envoyer des messages via n’importe quel canal tiers.

En savoir plus sur les [messages dans parcours](journeys-message.md) et les [actions personnalisées](using-custom-actions.md).

+++

+++ Comment puis-je attendre une heure ou un événement spécifique dans un parcours ?

Utilisez l’activité **Attente** pour suspendre le parcours pendant une durée spécifiée ou jusqu’à une date/heure spécifique. Les activités d’attente sont utiles pour :

* Envoyer des messages de relance après un délai (par exemple, 3 jours après l’achat)
* Création de campagnes goutte-à-goutte avec des intervalles temporels
* Combinaison avec des conditions pour créer des scénarios de temporisation

En savoir plus sur les [ activités d’attente ](wait-activity.md).

+++

+++ Puis-je mettre à jour les informations de profil au sein d’un parcours ?

Oui. Utilisez l&#39;activité **Mettre à jour le profil** pour modifier les attributs de profil dans Adobe Experience Platform en fonction d&#39;événements ou de conditions de parcours. Cela s’avère utile pour mettre à jour les points de fidélité, enregistrer les jalons du parcours, modifier les paramètres de préférences ou suivre les scores d’engagement des clients.

En savoir plus sur les [mises à jour de profil](update-profiles.md).

+++

+++ Comment envoyer un e-mail immédiatement après un achat ?

Créez un **parcours déclenché par un événement unitaire** :

1. Configurer un événement « Achat » avec les détails de la commande
2. Ajoutez l’événement comme point d’entrée de parcours
3. Suivez immédiatement avec une action E-mail .
4. Concevez votre e-mail de confirmation de commande avec des détails de commande personnalisés
5. Publier le parcours

Le parcours se déclenche automatiquement à chaque réception d’un événement d’achat, envoyant l’e-mail de confirmation en temps réel.

En savoir plus sur les [configuration d’événement](../event/about-events.md) et [actions d’e-mail](journeys-message.md).

+++

+++ Puis-je renvoyer un message si quelqu’un ne l’ouvre pas ou ne clique pas dessus ?

Oui. Utilisez un **Événement de réaction** avec un **Délai d’expiration** :

1. Après avoir envoyé votre message, ajoutez un événement Réaction qui écoute les ouvertures d’e-mail ou les clics
2. Configurez un délai d’expiration (par exemple, 3 jours) sur l’événement de réaction
3. Créez deux chemins d’accès :
   * **Si vous l’avez ouvert/cliqué** : passez aux étapes suivantes ou terminez le parcours
   * **Chemin de temporisation (non ouvert/cliqué)** : envoyez un e-mail de rappel avec un objet différent

**Bonne pratique** : limitez le nombre de renvois pour éviter d’apparaître comme indésirable (généralement 1 à 2 rappels au maximum).

En savoir plus sur les [événements de réaction](reaction-events.md).

+++

+++ Comment créer un parcours d’abandon de panier ?

Créez un parcours déclenché par un événement à l’aide d’un événement de réaction avec une temporisation :

1. **Configurer un événement « Panier abandonné »** : déclenché lorsque des éléments sont ajoutés, mais que le passage en caisse n’est pas terminé dans un délai donné
2. **Ajouter un événement de réaction** : configurez-le pour qu’il écoute un événement d’achat
3. **Définir un délai d’expiration** : définissez un délai d’expiration (par exemple, 1 à 2 heures) sur l’événement de réaction pour donner au client le temps de terminer naturellement
4. **Créez deux chemins** :
   * **Si l’événement d’achat se produit** : mettez fin au parcours ou continuez avec le flux après achat
   * **Chemin de temporisation (pas d’achat)** : envoyez un e-mail de rappel d’abandon avec le contenu du panier
5. **Facultatif** : ajoutez un autre événement de réaction avec une temporisation (24 heures) et envoyez un deuxième rappel avec un incentives (par exemple, une remise de 10 %)

En savoir plus sur les [cas d’utilisation de parcours ](jo-use-cases.md) et les [événements de réaction](reaction-events.md).

+++

+++ Comment diviser les clients en différents chemins d’accès en fonction de leur historique d’achats ?

Utilisez une **activité de condition** avec des attributs d’appartenance ou de profil d’audience :

1. Ajoutez une activité Condition à votre parcours
2. Créez plusieurs chemins d’accès en fonction de critères :
   * **Chemin 1** : clients à forte valeur ajoutée (total des achats > 1 000 $)
   * **Chemin 2** : clients réguliers (total des achats de 100 à 1 000 $)
   * **Chemin 3** : Nouveaux clients (total des achats &lt; 100 $)
3. Ajouter des messages ou des offres différents pour chaque chemin

En savoir plus sur les [conditions](condition-activity.md) et [qualification de l’audience](audience-qualification-events.md).

+++

+++ Comment gérer les différents fuseaux horaires dans mon parcours ?

Journey Optimizer propose plusieurs options de gestion des fuseaux horaires :

* **Fuseau horaire du profil** : les messages sont envoyés en fonction du fuseau horaire de chaque individu stocké dans son profil
* **Fuseau horaire fixe** : tous les messages utilisent un fuseau horaire spécifique que vous définissez

En savoir plus sur la [gestion des fuseaux horaires](timezone-management.md).

+++

+++ Combien de temps dois-je attendre entre les messages dans mon parcours ?

**Bonnes pratiques relatives aux temps d’attente** :

* **Messages transactionnels** (confirmations de commande) : envoyer immédiatement
* **Série de bienvenue** : 1 à 3 jours entre les e-mails
* **Contenu éducatif** : 3-7 jours entre les messages
* **Campagnes promotionnelles** : au moins 7 jours entre les offres
* **Réengagement** : 14 à 30 jours pour les utilisateurs inactifs

**Facteurs à prendre en compte** :

* Normes du secteur et attentes des clients
* Urgence et importance du message
* La fréquence globale des messages sur tous les canaux
* Modèles d’engagement client

**Conseil** : utilisez les règles de limitation du parcours pour limiter le nombre total de messages qu’un client ou une cliente reçoit sur tous les parcours.

En savoir plus sur les [activités d’attente](wait-activity.md) et la limitation du parcours [](../conflict-prioritization/journey-capping.md).

+++

## Tests et publication

+++ Comment tester mon parcours avant de le publier ?

Journey Optimizer propose deux approches de test :

* **Mode test** : simulez des profils individuels qui passent par le parcours étape par étape, ce qui vous permet de vérifier la logique, les conditions et les actions avant de passer en ligne.
* **Mode d’exécution d’essai** : exécutez votre parcours à l’aide de données de production réelles sans contacter les clients réels ou mettre à jour les informations de profil. Vous aurez ainsi confiance dans le ciblage d’audience et la conception de parcours.

**Bonne pratique** : testez toujours les parcours avant de les publier pour vous assurer qu’ils fonctionnent comme prévu et pour identifier les problèmes le plus tôt possible.

En savoir plus sur le [mode test](testing-the-journey.md) et le [exécution d’essai](journey-dry-run.md).

+++

+++ Que se passe-t-il lorsque je publie un parcours ?

Lorsque vous publiez un parcours :

* Le parcours devient **En ligne** et prêt à accepter de nouveaux profils
* Les profils peuvent saisir des données en fonction des critères d’entrée (événement ou audience)
* Les messages et les actions commencent à s’exécuter pour les profils qui se déplacent dans le parcours
* Vous ne pouvez modifier que des éléments limités sur un parcours publié (vous devez créer une nouvelle version si vous souhaitez en modifier davantage)

En savoir plus sur la [publication de parcours ](publishing-the-journey.md).

+++

+++ Puis-je modifier un parcours déjà publié ?

Oui, mais avec des limitations. Vous pouvez modifier certains éléments d’un parcours dynamique :

**Ce que vous pouvez modifier** :

* Propriétés du parcours (nom, description)
* Contenu du message dans les activités de message existantes
* Certains paramètres de parcours

**Ce que vous ne pouvez pas modifier** :

* Structure du parcours (ajout/suppression d’activités)
* Conditions d’entrée
* Parcours de la logique de la zone de travail

**Pour apporter des modifications structurelles** :

1. **Créer une version** : dupliquez le parcours publié pour créer un brouillon
2. **Apporter vos modifications** : modifiez le brouillon selon vos besoins.
3. **Tester la nouvelle version** : utilisez le mode test pour valider les modifications
4. **Publier la nouvelle version** : ferme automatiquement la version précédente et active la nouvelle

Les profils déjà dans le parcours termineront la version originale, tandis que les nouveaux profils entreront la nouvelle version.

En savoir plus sur les [versions de parcours ](journey-ui.md#journey-versions).

+++

+++ Comment arrêter un parcours ?

Vous pouvez gérer l’exécution du parcours de plusieurs manières :

* **Fermer aux nouvelles entrées** : empêcher les nouveaux profils de saisir tout en permettant aux profils existants de terminer leur parcours
* **Arrêter immédiatement** : arrêtez le parcours et quittez tous les profils qu’il contient actuellement.
* **Pause** : interrompt temporairement le parcours et le reprend ultérieurement

En savoir plus sur les [parcours d’envoi](end-journey.md).

+++

+++ Quelle est la différence entre « Fermer aux nouvelles entrées » et « Arrêter » ?

**Fermer aux nouvelles entrées** :

* Les nouveaux profils ne peuvent pas entrer dans le parcours
* Les profils déjà dans le parcours continuent et terminent leur chemin d’accès
* Utilisez cette option lorsque vous souhaitez réduire un parcours de manière élégante
* Exemple : campagne saisonnière terminée, mais pour laquelle vous souhaitez que les clients existants terminent leur expérience

**Arrêter** :

* Termine immédiatement le parcours pour tous les profils
* Tous les profils actuellement dans le parcours ont été fermés
* Utilisez cette option pour les situations urgentes ou les erreurs critiques
* Exemple : rappel de produit nécessitant l’arrêt immédiat des messages promotionnels

En savoir plus sur les [envoi de parcours ](end-journey.md) et [publication de parcours ](publishing-the-journey.md).

+++

## Exécution et surveillance des parcours

+++ Comment puis-je suivre la progression du profil via un parcours ?

Vous pouvez surveiller l’exécution du parcours à l’aide des éléments suivants :

* **Rapport dynamique sur les Parcours** : affichez les mesures et les KPI en temps réel pour votre parcours. Vous pouvez également consulter les résultats de l’exécution du test d’essai ici.
* **Rapport sur les Parcours à tout moment** : analysez les performances des parcours à l’aide de Customer Journey Analytics. Vous pouvez également consulter les résultats de l’exécution du test d’essai ici.
* **Événements d’étape de Parcours** : accédez aux données d’exécution détaillées pour les rapports personnalisés

En savoir plus sur les rapports de parcours [](report-journey.md).

+++

+++ Pourquoi un profil n&#39;a-t-il pas rejoint mon parcours ?

Raisons courantes pour lesquelles les profils peuvent ne pas entrer dans un parcours :

* **Événement non reçu** : l’événement déclencheur n’a pas été envoyé ou correctement configuré
* **Critères d’audience non remplis** : le profil n’est pas éligible à l’audience d’entrée
* **Règles de reprise** : le profil a récemment terminé le parcours et la reprise est bloquée
* **Parcours non publié** : le parcours est en version préliminaire
* **Espace de noms non valide** : l’espace de noms du parcours ne correspond pas à l’identité du profil
* **Parcours fermé** : le parcours n&#39;accepte plus de nouvelles entrées

En savoir plus sur la [gestion des entrées](entry-management.md).

+++

+++ Que sont les événements d’étape de parcours et comment les utiliser ?

Les événements d’étape de parcours sont des jeux de données générés automatiquement qui capturent des informations détaillées sur chaque étape d’un profil dans un parcours. Elles incluent les événements d’entrée et de sortie, l’exécution d’actions (messages envoyés, actions personnalisées appelées), les transitions de parcours (déplacement entre les activités), les erreurs et les délais d’expiration.

**Cas d’utilisation** :

* Créer des rapports personnalisés dans les outils Customer Journey Analytics ou BI
* Problèmes d’exécution du parcours de débogage
* Suivre le comportement détaillé du profil
* Création de modèles d’analyse et d’attribution avancés

En savoir plus sur les [événements d’étape de parcours ](../reports/sharing-overview.md).

+++

+++ Comment résoudre un problème lié à un parcours qui ne fonctionne pas comme prévu ?

Journey Optimizer fournit plusieurs ressources de dépannage :

* **Indicateurs d’erreur** : les alertes visuelles dans la zone de travail du parcours mettent en évidence les problèmes de configuration
* **Mode test** : suivez le parcours pour identifier où les problèmes se produisent
* **Mode d’exécution d’essai** : testez le parcours en utilisant des données de production réelles sans contacter les clients pour valider le ciblage et l’exécution
* **Rapports de Parcours** : consultez les mesures d’exécution pour identifier les goulets d’étranglement ou les erreurs
* **Événements d’étape de Parcours** : analyser les données d’exécution détaillées pour comprendre le comportement du profil

**Problèmes courants** :

* Événements ou audiences configurés de manière incorrecte
* Connexions à la source de données manquantes
* Expressions non valides dans les conditions ou la personnalisation
* Paramètres de temporisation trop courts

En savoir plus sur [résolution des problèmes liés aux parcours ](troubleshooting.md).

+++

<!--
+++ What happens if an action fails in a journey?

When an action fails (e.g., API call timeout, message delivery error), the journey continues by default unless configured otherwise. You can define condition activities to handle failure scenarios, and errors are logged in journey reports and step events for monitoring.

**Best practice**: Set appropriate timeout values for external actions and define alternative paths for critical failure scenarios.

Learn more about [action responses](../action/action-response.md).

+++
-->

+++ Puis-je voir qui est actuellement dans mon parcours ?

Oui. Utilisez le rapport dynamique sur les Parcours **** pour afficher :

* Nombre de profils actuellement dans le parcours
* Nombre de profils à chaque activité
* Profils entrés au cours des dernières 24 heures
* Mesures d’exécution en temps réel

Pour afficher des profils individuels, utilisez **événements d’étape de parcours** dans Customer Journey Analytics ou interrogez directement les jeux de données d’événement d’étape.

En savoir plus sur les rapports dynamiques de parcours [](report-journey.md).

+++

+++ Pourquoi mes messages ne sont-ils pas envoyés dans mon parcours ?

**Raisons et solutions courantes** :

* **Problèmes de consentement** : les destinataires n’ont pas choisi de recevoir des communications
Solution : vérifiez les politiques de consentement et le statut d’opt-in

* **Liste de suppression** : les adresses e-mail se trouvent dans la liste de suppression
Solution : consultez la liste de suppression pour les bounces ou les plaintes

* **Coordonnées non valides** : adresses e-mail/numéros de téléphone manquants ou incorrects
Solution : valider la qualité des données de profil

* **Parcours non publié** : le parcours est toujours en mode brouillon
Solution : publiez le parcours pour l’activer

<!-- 
* **Message not approved**: Message content requires approval before sending
  Solution: Submit for approval or check approval status-->

* **Problème de configuration du canal** : la configuration des e-mails/SMS est incorrecte
Solution : vérifiez les configurations et l’authentification des canaux

En savoir plus sur les [dépannage](troubleshooting.md) et [gestion du consentement](../action/consent.md).

+++

+++ Comment personnaliser les messages dans mon parcours ?

Vous pouvez personnaliser les messages à l’aide de l’**éditeur de personnalisation** :

**Données de personnalisation disponibles** :

* **Attributs de profil** : prénom, nom, e-mail, champs personnalisés
* **Données d’événement** : détails d’achat, comportement de navigation, activité de l’application
* **Données contextuelles** : variables de Parcours, données API externes
* **Appartenance à une audience** : qualifications de segment
* **Attributs calculés** : valeurs précalculées

**Exemple de personnalisation** :

* « Bonjour `{{profile.firstName}}`, merci pour votre achat de `{{event.productName}}` »
* « En fonction de votre niveau de fidélité (`{{profile.loyaltyTier}}`), voici une offre spéciale »
* Blocs de contenu dynamique qui changent en fonction des préférences du client

En savoir plus sur la [personnalisation](../personalization/personalize.md).

+++

+++ Puis-je envoyer différents messages en fonction du canal préféré ?

Oui. Utilisez une **[activité de condition](condition-activity.md)** pour acheminer les profils en fonction de leur canal préféré :

1. Ajoutez une [activité de condition](condition-activity.md) dans votre parcours
2. Créez un chemin pour chaque canal en vérifiant l’attribut de profil de canal préféré (par exemple, `profile.preferredChannel`)
3. Configurez les chemins spécifiques aux canaux :
   * **Chemin de l’e-mail** : ajoutez une [action e-mail](../email/create-email.md) avec du contenu optimisé pour les e-mails
   * **Chemin d’accès SMS** : ajoutez une [action SMS](../sms/create-sms.md) avec une messagerie concise
   * **Chemin push** : ajoutez une [action de notification push](../push/create-push.md) avec du contenu court et exploitable
   * **Chemin d’accès in-app** : ajoutez une [action de message in-app](../in-app/create-in-app.md) pour les utilisateurs et utilisatrices engagés de l’application
4. Ajoutez un chemin par défaut pour les profils sans préférence, en les acheminant vers votre canal principal

**Bonnes pratiques** :

* Assurez-vous que les données de votre profil incluent des préférences de canal précises
* Concevoir un contenu adapté aux forces et limites de chaque canal
* Utilisez [surfaces de canal](../configuration/channel-surfaces.md) pour gérer les configurations de canal
* Tester tous les chemins pour garantir une diffusion correcte des messages

En savoir plus sur les [conditions](condition-activity.md), [actions de message](journeys-message.md) et [sélection de canal](../channels/gs-channels.md).

+++

+++ Puis-je exclure certains clients de mon parcours ?

Oui, il existe plusieurs façons d’exclure les clients :

**À l’entrée du parcours** :

* Utiliser des [définitions d’audience](../audience/creating-a-segment-definition.md) avec des règles d’exclusion
* Ajoutez des [conditions d’entrée](entry-management.md) qui filtrent les profils spécifiques
* Configurez [critères de sortie basés sur les attributs de profil](journey-properties.md) dans les propriétés de parcours pour exclure automatiquement les profils en fonction d’attributs spécifiques

**Dans le parcours** :

* Ajoutez une [activité de condition](condition-activity.md) au début du parcours pour quitter les profils indésirables
* Vérifier les attributs d’exclusion (par exemple, statut de VIP, comptes de test)
* Utilisez [qualification d’audience](audience-qualification-events.md) pour identifier les profils à exclure

**Exemples de scénarios d’exclusion** :

* Exclure les clients qui ont récemment acheté
* Exclure les clients VIP des promotions standard
* Exclure les employés et les comptes de test
* Exclure les clients de régions spécifiques

+++

## Concepts avancés

+++ Qu’est-ce qu’un espace de noms de parcours et pourquoi est-ce important ?

Un **espace de noms** est un type d’identité (par exemple e-mail, ECID, numéro de téléphone) qui détermine la manière dont les profils sont identifiés dans le parcours. L’espace de noms définit l’identifiant utilisé pour faire correspondre les profils, doit être cohérent entre les événements, les audiences et les données de profil, et affecte le comportement d’entrée et de reprise sur le parcours.

**Bonne pratique** : choisissez un espace de noms qui identifie vos clients de manière fiable à tous les points de contact.

En savoir plus sur les [ espaces de noms d’identité ](../audience/get-started-identity.md).

+++

+++ Les profils peuvent-ils entrer plusieurs fois dans le même parcours ?

Oui, selon les **paramètres de rentrée** :

* **Autoriser une reprise** : les profils peuvent rejoindre le parcours plusieurs fois après l’avoir terminé
* **Période d’attente de reprise** : définissez un temps minimum entre les entrées de parcours (par exemple, 7 jours).
* **Forcer une reprise sur l’événement** : permet de déclencher une nouvelle instance de parcours même si le profil est déjà dans le parcours
* **Identifiant supplémentaire** : utilisez un identifiant supplémentaire pour permettre aux profils de rejoindre à nouveau le parcours plusieurs fois pour différentes entités (par exemple, différentes commandes, réservations ou transactions), même s’ils sont déjà dans le parcours

**Bonne pratique** : utilisez les règles de rentrée pour éviter la fatigue des messages et garantir une fréquence appropriée. Envisagez d’utiliser des identifiants supplémentaires pour les parcours transactionnels où les profils doivent saisir plusieurs fois différentes transactions.

En savoir plus sur la [gestion des entrées](entry-management.md) et les [identifiants supplémentaires](supplemental-identifier.md).

+++

+++ Qu’est-ce que l’optimisation de l’heure d’envoi ?

L’**optimisation de l’heure d’envoi (STO)** utilise l’IA pour prédire le meilleur moment pour envoyer un message à chaque profil individuel, en maximisant les taux d’ouverture et d’engagement. STO analyse les schémas d’engagement historiques afin de déterminer à quel moment chaque destinataire est le plus susceptible d’interagir avec votre message.

**Avantages** :

* Amélioration des taux d’ouverture et de clic
* Une meilleure expérience client grâce à des messages envoyés au moment optimal
* Taux de désabonnement réduits

En savoir plus sur l’[optimisation de l’heure d’envoi](send-time-optimization.md).

+++

+++ Que sont les règles de limitation du parcours ?

La limitation des Parcours **** vous permet de contrôler la manière dont les profils interagissent avec les parcours, d’éviter la fatigue des messages et d’assurer une expérience client optimale :

* **Limitation de l’entrée** : limitez le nombre de fois qu’un profil peut entrer des parcours au cours d’une période spécifiée
* **Limitation de la simultanéité** : limitez le nombre de parcours dans lesquels un profil peut se trouver simultanément

Vous pouvez définir le nombre maximal d’entrées ou la simultanéité par profil sur plusieurs parcours ou parcours spécifiques, définir des fenêtres temporelles (quotidiennes, hebdomadaires, mensuelles) et donner la priorité aux parcours lorsque plusieurs parcours se disputent le même profil.

En savoir plus sur la limitation du parcours [](../conflict-prioritization/journey-capping.md).

+++

+++ Puis-je intégrer mon parcours à des systèmes externes ?

Oui. Utilisez des **actions personnalisées** pour appeler des API tierces (CRM, automatisation marketing, systèmes de fidélité), envoyer des données à des systèmes externes, récupérer des informations en temps réel pour la prise de décision et déclencher des workflows dans des plateformes externes.

Les actions personnalisées prennent en charge l’authentification (clé API, authentification personnalisée), la personnalisation de la payload de requête/réponse, la gestion des erreurs et les délais d’expiration, ainsi que les paramètres dynamiques à partir du contexte du parcours.

En savoir plus sur les [actions personnalisées](using-custom-actions.md).

+++

+++ Comment utiliser Adobe Campaign avec parcours ?

Journey Optimizer s’intègre de manière native à Adobe Campaign pour tirer parti de ses fonctionnalités avancées :

* **Adobe Campaign Standard** : utilisez les actions de Campaign Standard pour envoyer des messages transactionnels
* **Adobe Campaign v7/v8** : déclenchez des workflows Campaign et utilisez l’infrastructure de diffusion de Campaign

**Bonne pratique** : utilisez cette intégration si vous disposez déjà de modèles Campaign ou de modèles de données, ou si vous avez besoin de fonctionnalités spécifiques à Campaign.

En savoir plus sur l’[intégration de Campaign](ajo-ac.md).

+++

+++ Qu’est-ce que l’activité Saut ?

L’activité **Saut** vous permet de faire passer des profils d’un parcours à un autre, en activant des modèles de parcours réutilisables, l’orchestration des parcours sur plusieurs parcours, une maintenance simplifiée des parcours et des stratégies d’engagement progressives.

Lorsqu’un profil atteint une activité Saut , il quitte le parcours en cours et entre dans le parcours cible à son point de départ.

En savoir plus sur [ l’activité Saut ](jump.md).

+++

+++ Comment créer un parcours de série de bienvenue ?

Une série de bienvenue type comprend plusieurs points de contact sur plusieurs jours :

**Exemple de structure** :

1. **Entrée** : audience des nouveaux abonnés ou de l’événement lorsqu’une personne s’inscrit
2. **E-mail 1 - Bienvenue immédiat** : Merci et présentation
3. **Attente** : 2 jours
4. **E-mail 2 - Prise en main** : tutoriel ou guide produit
5. **Attente** : 3 jours
6. **Condition** : le client a-t-il effectué un achat ?
   * **Oui** : terminer ou déplacer vers le parcours client
   * **Non** : continuer la série de bienvenue
7. **E-mail 3 - Incentive** : réduction spéciale pour le premier acheteur
8. **Attente** : 5 jours
9. **E-mail 4 - Engagement** : contenu populaire ou best-sellers

**Bonnes pratiques** :

* Conserver 3 à 5 e-mails sur 2 à 3 semaines
* Chaque e-mail doit avoir un objectif et un call-to-action clairs
* Surveillez les taux d’ouverture et ajustez la durée/le contenu en conséquence
* Quitter les clients plus tôt s’ils convertissent ou s’engagent profondément

En savoir plus sur les [cas d’utilisation de parcours ](jo-use-cases.md).

+++

+++ Puis-je tester différents chemins d’accès dans mon parcours ?

Oui. Utilisez l’activité **Optimiser** (disponibilité limitée) ou créez manuellement des divisions de test :

**Utilisation de l’activité Optimiser** avec la méthode Expérience :

* Divise le trafic de manière aléatoire entre différents chemins pour déterminer celui qui fonctionne le mieux
* Teste différents messages, offres, temps d’attente ou chemins de parcours entiers
* Mesure les performances en fonction de mesures de succès prédéfinies et déclare une expérience gagnante

**Utilisation de l’activité Optimiser** avec la méthode Condition de source de données :

* Créez une condition qui divise les profils de manière aléatoire (par exemple à l’aide d’une fonction de nombre aléatoire)
* Envoyer des expériences différentes à chaque partage
* Mesurer les résultats à l’aide de rapports de parcours

**Ce que vous pouvez tester** :

* Différentes lignes d’objet des e-mails
* Contenu alternatif du message
* Différents temps d’attente
* Diverses offres ou incentives
* Chemins de parcours entièrement différents

En savoir plus sur les [optimisation de l’activité](optimize.md) et [expériences de contenu](../content-management/content-experiment.md).

+++

+++ Comment déclencher un parcours lorsque l’inventaire est faible ?

Créez un **parcours d’événement métier** :

1. **Configurer un événement métier** : configurez un événement déclenché par votre système d&#39;inventaire lorsque le stock tombe sous un seuil
2. **Sélectionner l’audience cible** : sélectionnez les profils à avertir (par exemple, les clients qui ont consulté le produit, les abonnés aux alertes de réapprovisionnement).
3. **Action Ajouter un message** : envoyez un e-mail ou une notification push.
4. **Personnaliser le contenu** : inclure les détails du produit, le niveau d’inventaire actuel, la messagerie d’urgence

**Exemples d’événements métier** :

* Alerte de stock faible
* Notification de chute de prix
* Produit de nouveau en stock
* Annonce de vente Flash
* Promotions basées sur la météo

En savoir plus sur les [événements métier](general-events.md).

+++

+++ Que sont les politiques de fusion et comment affectent-elles les parcours ?

**Politiques de fusion** déterminez comment Adobe Experience Platform combine des données provenant de plusieurs sources afin de créer une vue de profil unifiée. Ils définissent des règles pour la hiérarchisation des données et la combinaison d’identités lorsque des fragments de profil existent dans différents jeux de données.

**Impact sur les parcours** :

* Les parcours utilisent la politique de fusion associée à l’audience ou à l’événement pour déterminer les données de profil disponibles
   * Dans les parcours Lecture d’audience ou Qualification d’audience : la politique de fusion de l’audience est utilisée
   * Dans les parcours d’événements unitaires : la politique de fusion par défaut est utilisée.
   * Dans les parcours d’événements métier : la politique de fusion de l’audience ciblée dans l’activité Lecture d’audience suivante est utilisée.

* La politique de fusion affecte les attributs accessibles dans des conditions de parcours, la personnalisation et les actions
* Différentes politiques de fusion peuvent entraîner l’utilisation de différentes données de profil dans le parcours

**Bonnes pratiques** :

* Assurez-vous que la politique de fusion utilisée par votre parcours est conforme à vos exigences de gouvernance des données
* Identifiez les jeux de données inclus dans votre politique de fusion pour connaître les données disponibles
* Utilisez des politiques de fusion cohérentes entre les audiences et les parcours associés pour obtenir des résultats prévisibles

En savoir plus sur les [ politiques de fusion ](../audience/get-started-profiles.md) et [ gestion des identités ](../audience/get-started-identity.md).

+++

+++ Quelle est la différence entre une condition et une activité d’attente ?

| | **Activité de condition** | **Activité d’attente** |
|---|---|---|
| **Rôle** | Crée différents chemins en fonction de la logique (if/then) | Suspend le parcours pendant un certain temps |
| **Fonction** | Évalue les données et achemine les profils en conséquence | Contient les profils à un moment donné avant de continuer |
| **Cas d’utilisation** | Segmenter les clients, vérifier le statut, créer une branche en fonction du comportement | Timing entre les messages, attente des heures de bureau, création de retards |
| **Exemple** | Si le client est VIP, envoyez une offre Premium ; sinon, envoyez une offre standard. | Patientez 3 jours après l’e-mail de bienvenue avant d’envoyer le message suivant |

**Ils travaillent ensemble** :

* Patientez pendant un certain temps, puis utilisez une condition pour vérifier si un événement s’est produit pendant l’attente
* Exemple : attendez 7 jours, puis vérifiez si le client a effectué un achat

En savoir plus sur les [conditions](condition-activity.md) et les [activités d’attente](wait-activity.md).

+++

## Bonnes pratiques et restrictions

+++ Quelles sont les principales limites dont je dois tenir compte ?

Les mécanismes de sécurisation importants sont les suivants :

* **Complexité du Parcours** : nombre maximal d’activités, de chemins et de niveaux d’imbrication
* **Débit** : taux d’envoi des messages et limites des appels API
* **Durée de vie** : durée maximale du parcours (par exemple, 91 jours).
* **Taille de l’audience** : limites des tailles de lot d’audience lue
* **Complexité de l’expression** : limites de caractères dans les conditions et la personnalisation

Affichage complet [mécanismes de sécurisation et limitations](../start/guardrails.md).

+++

+++ Quelles sont les bonnes pratiques en matière de conception de parcours ?

**Structure et organisation** :

* Concentrer les parcours sur des cas d’utilisation spécifiques
* Utiliser des noms descriptifs pour les activités
* Ajouter des descriptions et des libellés pour une logique complexe
* Regrouper les parcours associés avec des balises

**Performances** :

* Optimisez les temps d’attente pour équilibrer l’engagement et le volume
* Limiter les appels API externes aux cas d’utilisation essentiels
* Utilisation des règles de limitation pour éviter la fatigue des messages
* Surveiller régulièrement les mesures de parcours

**Test** :

* Toujours tester les parcours avant la publication
* Utilisez le mode test pour valider la logique de parcours et parcourir le parcours
* Utilisez le mode Exécution d’essai pour effectuer des tests avec des données de production réelles sans contacter les clients
* Tester tous les chemins et scénarios conditionnels
* Utiliser des profils de test réalistes
* Validation de la personnalisation et du contenu dynamique

**Maintenance** :

* Vérifier régulièrement les performances du parcours
* Arrêter ou fermer les parcours inutilisés
* Logique de parcours de document et règles de gestion
* Planifier le contrôle de version du parcours

En savoir plus sur les [bonnes pratiques de conception de parcours ](using-the-journey-designer.md).

+++

+++ Combien d’activités puis-je ajouter à un parcours ?

Les parcours sont limités à un maximum de 50 activités. Cependant, nous vous recommandons de simplifier vos parcours pour une meilleure maintenabilité et de meilleures performances.

Lorsque les parcours approchent 50 activités, elles peuvent devenir très complexes et difficiles à gérer, à dépanner et à comprendre. Les parcours volumineux avec de nombreuses branches et conditions peuvent également avoir un impact sur le temps de traitement, la lisibilité et la collaboration de l’équipe.

**Bonne pratique** : veillez à ce que vos parcours restent ciblés et gérables. Si votre parcours devient complexe, tenez compte des points suivants :

* La diviser en plusieurs parcours à l’aide de l’activité Saut
* Création de modèles réutilisables sur des parcours plus simples
* Simplifier la logique avec des conditions plus efficaces
* Vérifier si toutes les activités sont nécessaires

En savoir plus sur la conception du parcours [](using-the-journey-designer.md) et les [mécanismes de sécurisation et limitations](../start/guardrails.md).

+++

+++ Comment puis-je m’assurer que mon parcours fonctionne bien à grande échelle ?

**Considérations de conception** :

* Utilisez [entrée basée sur l’audience](read-audience.md) pour les communications par lots au lieu d’événements individuels
* Implémentez des [temps d’attente](wait-activity.md) appropriés pour répartir le volume des messages
* Utilisez les [ règles de limitation ](../conflict-prioritization/journey-capping.md) pour éviter la surcharge du système.
* Optimisez la [logique de condition](condition-activity.md) pour réduire la complexité du traitement

**Surveillance** :

* Effectuez régulièrement le suivi de [mesures de parcours ](report-journey.md)
* Surveillance des performances de l’API pour [actions personnalisées](using-custom-actions.md)
* Consultez les taux d’erreur et les occurrences de délai d’expiration à l’aide [outils de dépannage](troubleshooting.md)
* S’abonner à [des alertes de parcours ](../reports/alerts.md) des échecs de parcours critiques

**Optimisation** :

* Utilisez [mode test](testing-the-journey.md) et [exécution à sec](journey-dry-run.md) pour valider les performances avant la publication
* Réduisez les appels d’API externes par le biais d’[actions personnalisées](using-custom-actions.md) pour éviter la latence et la dépendance aux systèmes tiers
* Stocker les données fréquemment utilisées dans Adobe Experience Platform à l’aide de la [recherche de jeu de données](dataset-lookup.md) au lieu d’effectuer des appels externes, lorsque cela est possible
* Examiner et optimiser les performances de [diffusion des messages](journeys-message.md)

En savoir plus sur les [mécanismes de sécurisation et limitations](../start/guardrails.md).

+++

## Ressources supplémentaires

Pour des mises à jour et des formations supplémentaires, consultez les ressources suivantes :

* [Commencer les parcours](journey.md)
* [Créer votre premier parcours](journey-gs.md)
* [Guides de dépannage](troubleshooting.md)
* [Cas d’utilisation de parcours](jo-use-cases.md)
* [Description du produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
