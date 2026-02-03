---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - Questions fréquentes
description: Questions fréquentes sur Journey Orchestration dans Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: parcours, questions, réponses, dépannage, aide, guide, orchestration
version: Journey Orchestration
source-git-commit: bf5d018fa6c3e88cf84345e892de72ada9f2c489
workflow-type: tm+mt
source-wordcount: '5231'
ht-degree: 99%

---


# Journey Orchestration - Questions fréquentes {#faq-journeys}

Découvrez les réponses aux questions le plus courantes sur Journey Orchestration dans Adobe Journey Optimizer.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la [communauté Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

## Concepts généraux

+++ Qu’est-ce qu’un parcours dans Adobe Journey Optimizer ?

Un parcours est une orchestration en plusieurs étapes qui vous permet de concevoir et d’exécuter des expériences clients en temps réel sur plusieurs canaux. Les parcours combinent des événements, des activités d’orchestration, des actions et des messages, en vue de créer des expériences contextuelles personnalisées basées sur le comportement de la clientèle et des événements métier.

En savoir plus sur les [parcours](journey.md).

+++

+++ Quels sont les différents types de parcours ?

Adobe Journey Optimizer prend en charge quatre types de parcours :

* **Parcours unitaires** : ils sont déclenchés individuellement par un événement (par exemple, un achat, une connexion à l’application). Les profils rejoignent le parcours un par un lorsque l’événement se produit.
* **Parcours de lecture d’audience** : ils démarrent avec une audience Adobe Experience Platform et envoient des messages par lots à tous les profils de cette audience.
* **Parcours de qualification d’audience** : ils sont déclenchés lorsque les profils sont qualifiés pour un segment ciblé spécifique (ou en sortent). Les profils rejoignent le parcours, car ils répondent aux critères de l’audience.
* **Parcours d’événement métier** : ils sont déclenchés par des événements métier (par exemple, les mises à jour de stocks, les alertes météorologiques) qui affectent plusieurs profils simultanément.

En savoir plus sur les [types de parcours](entry-management.md#types-of-journeys).

+++

+++ Quelle est la différence entre un parcours et une campagne ?

Les **[parcours](journey.md)** sont des orchestrations en plusieurs étapes qui réagissent aux événements ou aux audiences cibles, en tenant compte d’une logique complexe, des conditions, des temps d’attente et de plusieurs points de contact tout au long du cycle de vie de la clientèle.

Les **[campagnes](../campaigns/get-started-with-campaigns.md)** se divisent en trois types :

* **[Campagnes d’action](../campaigns/create-campaign.md)** : communications ponctuelles ou récurrentes envoyées à une audience spécifique, idéales pour les messages autonomes tels que les annonces promotionnelles ou les newsletters.
* **[Campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md)** : campagnes déclenchées par le biais d’appels API, permettant l’intégration à des systèmes externes pour envoyer des messages en fonction des événements en temps réel ou de la logique commerciale.
* **[Campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)** : campagnes à plusieurs étapes basées sur l’audience, créées sur une zone de travail qui peut inclure des conditions, des temps d’attente et plusieurs actions pour créer des expériences planifiées et coordonnées.

**Bonne pratique** : utilisez les [parcours](journey.md) pour un engagement complexe déclenché par un événement avec une orchestration avancée ; utilisez les [campagnes d’action](../campaigns/create-campaign.md) pour des communications planifiées basées sur une audience ; utilisez les [campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md) pour un déclenchement par programme à partir de systèmes externes ; utilisez les [campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) pour des communications à plusieurs étapes avec des exigences spécifiques à la campagne.

+++

+++ Quels sont les principaux composants d’un parcours ?

Un parcours comprend les éléments suivants :

* **Événements** : points d’entrée qui déclenchent le parcours (par exemple, qualification du profil, événements métier).
* **Activités d’orchestration** : composants logiques tels que les conditions, l’attente, la lecture d’audience et la fin.
* **Actions** : activités qui effectuent des tâches, comme envoyer des messages, mettre à jour des profils ou appeler des API externes.
* **Actions de canal intégrées** : fonctionnalités de messagerie natives pour les e-mails, SMS, notifications push et autres canaux.
* **Actions personnalisées** : intégration à des systèmes tiers.

En savoir plus sur les [activités de parcours](about-journey-activities.md).

+++

+++ Quels sont les types d’audiences pris en charge dans les parcours et quelles sont leurs limites ?

Adobe Journey Optimizer prend en charge quatre types d’audiences, chacun ayant des caractéristiques et des mécanismes de sécurisation différents :

**1. Audiences de streaming**

* **Description** : audiences évaluées en temps réel à mesure que les données de profil changent.
* **Évaluation** : évaluation continue lorsque les attributs ou les événements de profil correspondent à des critères de segment.
* **Utilisation du parcours** : pris en charge dans les activités Lecture d’audience, Qualification d’audience et Condition.
* **Idéal pour** : un engagement en temps réel basé sur des changements de comportement ou des mises à jour de profil.
* **Mécanismes de sécurisation** :
   * La taille maximale de l’audience dépend de votre licence Journey Optimizer.
   * La latence de l’évaluation est généralement inférieure à 5 minutes.
   * Une logique de segmentation complexe peut affecter les performances de l’évaluation.

**2. Audiences par lots**

* **Description** : audiences évaluées selon un calendrier défini (généralement quotidiennement).
* **Évaluation** : traitement par lots à intervalles planifiés.
* **Utilisation du parcours** : prise en charge dans les activités Lecture d’audience et Condition ; prise en charge limitée dans les parcours de qualification d’audience.
* **Idéal pour** : campagnes régulières, newsletters, communications planifiées.
* **Mécanismes de sécurisation** :
   * L’évaluation a lieu une fois par jour (par défaut) ou selon le planning configuré.
   * Les profils peuvent ne pas refléter les modifications en temps réel avant la prochaine évaluation.
   * L’activité Lecture d’audience peut traiter efficacement de grandes audiences par lots.

**3. Audiences avec chargement (chargement personnalisé)**

* **Description** : audiences créées en chargeant des fichiers CSV avec des identifiants de profil.
* **Évaluation** : liste statique mise à jour uniquement lorsque de nouveaux fichiers sont chargés.
* **Utilisation du parcours** : prise en charge dans les activités Lecture d’audience et Condition ; **non prise en charge** dans les parcours de qualification d’audience.
* **Idéal pour** : campagnes ponctuelles, importations de listes externes, communications ciblées.
* **Mécanismes de sécurisation** :
   * Des limites de taille pour les fichiers CSV s’appliquent (consultez la documentation du produit pour connaître les limites actuelles).
   * Les membres de l’audience restent statiques jusqu’à ce qu’ils soient actualisés lors d’un nouveau chargement.
   * L’espace de noms d’identité doit correspondre à l’espace de noms du parcours.
   * Les profils doivent exister dans Adobe Experience Platform.

**4. Audiences de composition d’audiences fédérées**

* **Description** : audiences créées à l’aide de données fédérées, ce qui vous permet d’interroger et de composer des audiences à partir d’entrepôts de données externes sans copier de données dans Adobe Experience Platform.
* **Évaluation** : la composition statique est mise à jour lors de l’exécution de la composition d’audiences fédérées.
* **Utilisation du parcours** : prise en charge dans les activités Lecture d’audience et Condition ; **non prise en charge** dans les parcours de qualification d’audience (similaire au audiences chargées du point de vue back-end).
* **Idéal pour** : l’intégration d’entrepôts de données d’entreprise, la composition d’audiences à l’aide de sources de données externes, les scénarios nécessitant que les données restent dans des systèmes externes.
* **Mécanismes de sécurisation** :
   * Les membres de l’audience restent statiques jusqu’à la prochaine exécution d’une composition fédérée.
   * L’espace de noms d’identité doit correspondre à l’espace de noms du parcours.
   * Les performances dépendent des fonctionnalités de requêtes de l’entrepôt de données externe.
   * Nécessite le module complémentaire de composition d’audiences fédérées.

**Audiences Customer Journey Analytics (CJA)** :

Bien que les audiences CJA ne soient pas directement prises en charge dans les parcours, vous pouvez utiliser une **solution de contournement** en « incorporant » une audience CJA dans une règle de segmentation. Cela crée une audience par lots du service de profils unifiés faisant référence à l’audience CJA, ce qui la rend disponible pour une utilisation dans des parcours en tant qu’audience par lots.

**Éléments à prendre en compte spécifiques aux parcours** :

* **Parcours de Lecture d’audience** : les quatre types d’audience sont pris en charge ; un export par lots est effectué lors de l’exécution du parcours.
* **Parcours de qualification d’audience** : audiences en streaming recommandées ; les audiences par lots ont une détection de la qualification retardée ; les audiences chargées et les audiences de composition d’audiences fédérées ne sont pas prises en charge.
* **Activités Condition** : tous les types d’audience peuvent être utilisés pour vérifier l’appartenance.
* **Alignement des espaces de noms** : l’espace de noms d’identité de l’audience doit correspondre à celui du parcours pour identifier correctement les profils.

**Bonnes pratiques** :

* Utilisez des **audiences en streaming** pour les parcours en temps réel pilotés par des événements et nécessitant une réponse immédiate.
* Utilisez des **audiences par lots** pour les communications planifiées lorsque l’évaluation quotidienne est suffisante.
* Utilisez des **audiences chargées** pour les campagnes ponctuelles ciblées avec des listes externes.
* Utilisez des **audiences de composition d’audiences fédérées** lorsque vous devez exploiter les fonctionnalités d’entrepôts de données d’entreprise sans dupliquer les données.
* Surveillez la taille de l’audience et les performances des évaluations dans les déploiements à grande échelle.
* Tenez compte des taux d’actualisation de l’audience lors de la conception du timing et des conditions d’entrée du parcours.

En savoir plus sur les [audiences](../audience/about-audiences.md), la [création de segments](../audience/creating-a-segment-definition.md), les [audiences chargées personnalisées](../audience/custom-upload.md) et la [composition d’audiences fédérées](../audience/federated-audience-composition.md).

+++

+++ Comment choisir entre un parcours unitaire et un parcours de lecture d’audience ?

Utilisez les **parcours unitaires** lorsque :

* Vous devez réagir en temps réel aux actions de chaque individu (par exemple, confirmation d’achat, abandon de panier).
* Chaque personne doit progresser à son propre rythme.
* Vous souhaitez un déclenchement en fonction d’événements spécifiques.

Utilisez les **Parcours de lecture d’audience** lorsque :

* Vous envoyez des communications par lots à un groupe (par exemple, newsletter mensuelle, campagnes promotionnelles).
* Toutes les personnes doivent recevoir le message à peu près au même moment.
* Vous ciblez un segment d’audience prédéfini.

+++

## Création de parcours

+++ Comment puis-je commencer à créer mon premier parcours ?

Suivez ces étapes clés :

1. **Configurer les conditions préalables** : configurez les événements, les sources de données et les actions selon les besoins.
2. **Créer le parcours** : accédez au menu Parcours et cliquez sur « Créer un parcours ».
3. **Définir les propriétés du parcours** : définissez le nom, la description et d’autres paramètres du parcours.
4. **Concevoir le parcours** : faites glisser et déposez des activités de la palette vers la zone de travail.
5. **Tester le parcours** : utilisez le mode test pour valider la logique de parcours.
6. **Tester à blanc le parcours** : utilisez le test à blanc pour tester le parcours à l’aide de données de production réelles sans contacter une vraie clientèle ni mettre à jour les informations de profil.
7. **Publier le parcours** : activez le parcours.

Suivez le [guide détaillé](journey-gs.md).

+++

+++ Quelles sont les conditions préalables requises avant de créer un parcours ?

Les conditions préalables requises dépendent du type de votre parcours :

* **Parcours déclenchés par un événement** : configurez les événements pour définir à quel moment les profils doivent rejoindre le parcours.
* **Parcours basés sur l’audience** : créez des audiences dans Adobe Experience Platform.
* **Enrichissement des données** : configurez les sources de données pour récupérer des informations supplémentaires.
* **Intégrations tierces** : configurez des actions personnalisées si vous utilisez des systèmes externes.

En savoir plus sur la [configuration de parcours](../configuration/about-data-sources-events-actions.md).

+++

+++ Puis-je utiliser des données provenant de systèmes externes dans mon parcours ?

Oui, il existe plusieurs approches pour utiliser les données externes :

**Bonnes pratiques** :

* **Actions personnalisées** : appelez des API externes par le biais d’actions personnalisées pour récupérer ou envoyer des données à des systèmes tiers. Il s’agit de l’approche recommandée pour les interactions en temps réel avec des systèmes externes.
* **Recherche de jeu de données** : si vous pouvez charger des données à partir de systèmes externes dans Adobe Experience Platform, utilisez la fonction de recherche de jeu de données pour récupérer les informations stockées dans les jeux de données Experience Platform.
* **Sources de données externes** : configurez les sources de données externes pour récupérer les informations des services d’API tiers (approche moins recommandée que celles ci-dessus).

Ces options vous permettent d’enrichir l’expérience client avec des données provenant de votre CRM, de vos systèmes de fidélité, de vos services météorologiques ou d’autres plateformes externes.

En savoir plus sur les [actions personnalisées](using-custom-actions.md) et la [recherche de jeu de données](dataset-lookup.md).

+++

+++ Comment ajouter des conditions à mon parcours ?

Vous pouvez ajouter des conditions à l’aide de l’**activité Condition** de la palette d’orchestration. Les conditions vous permettent de :

* créer des conditions simples ou avancées à l’aide de l’éditeur d’expression ;
* diviser le parcours en plusieurs chemins en fonction des attributs de profil, de l’appartenance à l’audience, des événements ou des données contextuelles ;
* définir des chemins de temporisation pour les profils qui ne remplissent pas la condition dans un délai spécifié.

En savoir plus sur les [conditions](condition-activity.md).

+++

+++ Puis-je envoyer des messages aux profils d’un parcours ?

Oui. Journey Optimizer comprend des **actions de canal intégrées** qui vous permettent d’envoyer des messages par e-mail, des notifications push, des SMS/MMS/RCS, des messages in-app, des expériences web, des expériences basées sur du code, des cartes de contenu, WhatsApp et LINE. Vous pouvez concevoir le contenu des messages directement dans Journey Optimizer et les ajouter en tant qu’activités d’action dans votre parcours.

Pour les canaux non pris en charge en mode natif, vous pouvez utiliser des **actions personnalisées** pour intégrer des plateformes de messagerie externes et envoyer des messages via n’importe quel canal tiers.

En savoir plus sur les [messages dans les parcours](journeys-message.md) et les [actions personnalisées](using-custom-actions.md).

+++

+++ Comment attendre un moment ou un événement spécifique dans un parcours ?

Utilisez l’**activité Attente** pour suspendre le parcours pendant une durée spécifiée ou jusqu’à une date/heure spécifique. Les activités d’attente sont utiles pour :

* envoyer des messages de relance après un délai (par exemple, 3 jours après l’achat) ;
* créer de campagnes de drip avec des envois espacés ;
* être combinées avec des conditions pour créer des scénarios de temporisation.

En savoir plus sur les [activités d’attente](wait-activity.md).

+++

+++ Puis-je mettre à jour les informations de profil au sein d’un parcours ?

Oui. Utilisez l’activité **Mettre à jour le profil** pour modifier les attributs de profil dans Adobe Experience Platform en fonction d’événements ou de conditions de parcours. Cela s’avère utile pour mettre à jour les points de fidélité, enregistrer les jalons du parcours, modifier les paramètres de préférences ou suivre les scores d’engagement des clientes et clients.

En savoir plus sur les [mises à jour de profil](update-profiles.md).

+++

+++ Comment envoyer un e-mail immédiatement après un achat ?

Créez un **parcours déclenché par un événement unitaire** :

1. Configurez un événement « Achat » avec les informations sur la commande.
2. Ajoutez l’événement comme point d’entrée de parcours.
3. Suivez immédiatement avec une action E-mail.
4. Concevez votre e-mail de confirmation de commande avec des informations personnalisées sur la commande.
5. Publiez le parcours.

Le parcours se déclenche automatiquement à chaque réception d’un événement d’achat, envoyant l’e-mail de confirmation en temps réel.

En savoir plus sur la [configuration d’événement](../event/about-events.md) et les [actions d’e-mail](journeys-message.md).

+++

+++ Puis-je renvoyer un message si quelqu’un ne l’ouvre pas ou ne clique pas dessus ?

Oui. Utilisez un événement de **[!UICONTROL réaction]** avec une **temporisation** :

1. Après avoir envoyé votre message, ajoutez un événement de **[!UICONTROL réaction]** **immédiatement** après l’action de canal (sans activité d’**[!UICONTROL attente]** entre les deux).
2. Configurez une période de temporisation (par exemple, 3 jours) sur l’événement de **[!UICONTROL réaction]** pour écouter les ouvertures d’e-mail ou les clics.
3. Créez deux chemins :
   * **Si vous l’avez ouvert/cliqué dessus** : passez aux étapes suivantes ou terminez le parcours.
   * **Chemin de temporisation (non ouvert/cliqué)** : envoyez un e-mail de rappel avec un objet différent.

**Bonne pratique** : limitez le nombre de renvois pour éviter d’apparaître comme indésirable (généralement 1 à 2 rappels au maximum).

En savoir plus sur les [événements de réaction](reaction-events.md).

+++

+++ Comment créer un parcours d’abandon de panier ?

Créez un parcours déclenché par un événement à l’aide d’un événement de **[!UICONTROL réaction]** avec une temporisation :

1. **Configurez un événement « Panier abandonné »** : déclenché lorsque des articles sont ajoutés, mais que le passage en caisse n’est pas terminé dans un délai donné.
2. **Envoyez un message initial** (facultatif) : e-mail accusant réception des articles du panier.
3. **Ajoutez un événement de [!UICONTROL réaction] immédiatement après l’action de canal** : configurez-le pour qu’il écoute un événement d’achat.
4. **Définissez une période de temporisation** : définissez une temporisation (par exemple, 1 à 2 heures) sur l’événement de **[!UICONTROL réaction]** pour donner au client ou à la cliente le temps de terminer le processus.
5. **Créez deux chemins** :
   * **Si l’événement d’achat se produit** : mettez fin au parcours ou continuez avec le flux après achat.
   * **Chemin de temporisation (pas d’achat)** : envoyez un e-mail de rappel d’abandon avec le contenu du panier.
6. **Facultatif** : ajoutez un autre événement de **[!UICONTROL réaction]** **immédiatement** après l’e-mail de rappel avec une temporisation (24 heures) et envoyez un deuxième rappel avec un avantage incitatif (par exemple, une remise de 10 %).

>[!IMPORTANT]
>
>Les événements de **[!UICONTROL réaction]** doivent être placés immédiatement après les [actions de canal](journeys-message.md). Ne placez pas d’activités d’**[!UICONTROL attente]** entre l’action de canal et l’activité de **[!UICONTROL réaction]**.

En savoir plus sur les [cas d’utilisation de parcours](jo-use-cases.md) et les [événements de réaction](reaction-events.md).

+++

+++ Comment répartir les clients dans différents chemins en fonction de leur historique d’achats ?

Utilisez une **activité de condition** avec des attributs de profil ou une appartenance à l’audience :

1. Ajoutez une activité de condition à votre parcours.
2. Créez plusieurs chemins en fonction de critères :
   * **Chemin 1** : clientes et clients de grande valeur (total des achats > 1 000 $)
   * **Chemin 2** : clientes et clients réguliers (total des achats entre 100 et 1 000 $)
   * **Chemin 3** : nouveaux clients et nouvelles clientes (total des achats &lt; 100 $)
3. Ajoutez des messages ou des offres différents pour chaque chemin.

En savoir plus sur les [conditions](condition-activity.md) et la [qualification d’audience](audience-qualification-events.md).

+++

+++ Comment gérer différents fuseaux horaires dans mon parcours ?

Journey Optimizer propose plusieurs options de gestion des fuseaux horaires :

* **Fuseau horaire du profil** : les messages sont envoyés en fonction du fuseau horaire de chaque individu stocké dans son profil.
* **Fuseau horaire fixe** : tous les messages utilisent un fuseau horaire spécifique que vous définissez.

En savoir plus sur la [gestion des fuseaux horaires](timezone-management.md).

+++

+++ Combien de temps dois-je attendre entre les messages dans mon parcours ?

**Bonnes pratiques relatives aux temps d’attente** :

* **Messages transactionnels** (confirmations de commande) : envoyer immédiatement
* **Série de bienvenue** : 1 à 3 jours entre les e-mails
* **Contenu éducatif** : 3 à 7 jours entre les messages
* **Campagnes promotionnelles** : au moins 7 jours entre les offres
* **Réengagement** : 14 à 30 jours pour les personnes inactives

**Facteurs à prendre en compte** :

* Normes du secteur et attentes de la clientèle
* Urgence et importance des messages
* Fréquence globale de vos messages sur tous les canaux
* Modèles d’engagement de la clientèle

**Conseil** : utilisez les règles de limitation de parcours pour limiter le nombre total de messages qu’un client ou une cliente reçoit sur tous les parcours.

En savoir plus sur les [activités d’attente](wait-activity.md) et la [limitation de parcours](../conflict-prioritization/journey-capping.md).

+++

## Tests et publication

+++ Comment tester mon parcours avant de le publier ?

Journey Optimizer propose deux approches de test :

* **Mode test** : simulez des profils individuels qui passent par le parcours étape par étape, ce qui vous permet de vérifier la logique, les conditions et les actions avant la publication.
* **Mode test à blanc** : exécutez votre parcours à l’aide de données de production réelles sans contacter la vraie clientèle ni mettre à jour les informations de profil. Vous aurez ainsi confiance dans le ciblage d’audience et la conception de parcours.

**Bonne pratique** : testez toujours les parcours avant de les publier pour vous assurer qu’ils fonctionnent comme prévu et pour identifier les problèmes le plus tôt possible.

En savoir plus sur le [mode test](testing-the-journey.md) et le [test à blanc](journey-dry-run.md).

+++

+++ Que se passe-t-il lorsque je publie un parcours ?

Lorsque vous publiez un parcours :

* Il devient **actif** et peut accepter de nouveaux profils.
* Les profils peuvent le rejoindre en fonction des critères d’entrée (événement ou audience).
* Les messages et les actions commencent à s’exécuter pour les profils qui se déplacent dans le parcours.
* Vous ne pouvez modifier que des éléments limités sur un parcours publié (vous devez créer une nouvelle version si vous souhaitez en modifier davantage).

En savoir plus sur la [publication des parcours](publish-journey.md).

+++

+++ Puis-je modifier un parcours déjà publié ?

Oui, mais avec certaines limites. Vous pouvez modifier certains éléments d’un parcours actif :

**Ce que vous pouvez modifier** :

* Propriétés du parcours (nom, description)
* Contenu des messages dans les activités de message existantes
* Certains paramètres de parcours

**Ce que vous ne pouvez pas modifier** :

* Structure du parcours (ajout/suppression d’activités)
* Conditions d’entrée
* Logique de la zone de travail des parcours

**Pour apporter des modifications structurelles** :

1. **Créer une version** : dupliquez le parcours publié pour créer un brouillon.
2. **Apporter vos modifications** : modifiez le brouillon selon vos besoins.
3. **Tester la nouvelle version** : utilisez le mode test pour valider les modifications.
4. **Publier la nouvelle version** : cela permet de fermer automatiquement la version précédente et d’activer la nouvelle.

Les profils déjà dans le parcours termineront la version originale, tandis que les nouveaux profils rejoindront la nouvelle version.

En savoir plus sur les [versions de parcours](journey-ui.md#journey-filter).

+++

+++ Comment arrêter un parcours ?

Vous pouvez gérer l’exécution du parcours de plusieurs manières :

* **Fermer le parcours aux nouvelles entrées** : empêchez les nouveaux profils de rejoindre le parcours tout en permettant aux profils existants de le terminer.
* **Arrêter immédiatement** : arrêtez le parcours et faites sortir tous les profils qu’il contient actuellement.
* **Mettre en pause** : interrompez temporairement le parcours et reprenez-le ultérieurement.

En savoir plus sur l’[arrêt des parcours](end-journey.md).

+++

+++ Quelle est la différence entre « Fermer le parcours aux nouvelles entrées » et « Arrêter » ?

**Fermer le parcours aux nouvelles entrées** :

* Les nouveaux profils ne peuvent pas rejoindre le parcours.
* Les profils déjà dans le parcours continuent et terminent leur chemin.
* Utilisez cette option lorsque vous souhaitez clôturer un parcours en douceur.
* Exemple : une campagne des fêtes de fin d’année terminée, mais vous souhaitez que la clientèle existante terminent son expérience.

**Arrêter** :

* Termine immédiatement le parcours pour tous les profils.
* Tous les profils actuellement dans le parcours sont sortis.
* Utilisez cette option pour les situations urgentes ou les erreurs critiques.
* Exemple : un rappel de produit nécessitant l’arrêt immédiat des messages promotionnels

En savoir plus sur l’[arrêt des parcours](end-journey.md) et la [publication des parcours](publish-journey.md).

+++

## Exécution et surveillance des parcours

+++ Comment suivre la progression des profils dans un parcours ?

Vous pouvez surveiller l’exécution d’un parcours à l’aide des éléments suivants :

* **Rapport dynamique de parcours** : affichez les mesures et les KPI en temps réel de votre parcours. Vous pouvez également consulter les résultats de l’exécution du test à blanc dans ce rapport.
* **Rapport complet de parcours** : analysez les performances d’un parcours à l’aide de Customer Journey Analytics. Vous pouvez également consulter les résultats de l’exécution du test à blanc dans ce rapport.
* **Événements d’étape de parcours** : accédez aux données d’exécution détaillées pour les rapports personnalisés.

En savoir plus sur les [rapports de parcours](report-journey.md).

+++

+++ Pourquoi un profil n’a-t-il pas rejoint mon parcours ?

Raisons courantes pour lesquelles les profils peuvent ne pas rejoindre un parcours :

* **Événement non reçu** : l’événement déclencheur n’a pas été envoyé ou correctement configuré.
* **Critères d’audience non remplis** : le profil n’est pas éligible à l’audience d’entrée.
* **Règles de rentrée** : le profil a récemment terminé le parcours et la reprise est bloquée.
* **Parcours non publié** : le parcours est en état de brouillon.
* **Espace de noms non valide** : l’espace de noms du parcours ne correspond pas à l’identité du profil.
* **Parcours fermé** : le parcours n’accepte plus de nouvelles entrées.
* **Durée de qualification des audiences en streaming** : pour les parcours utilisant la qualification d’audience avec les audiences en streaming, les profils peuvent ne pas rejoindre le parcours s’ils étaient déjà dans l’audience avant la publication du parcours ou si la période d’activation du parcours n’est pas terminée (jusqu’à 10 minutes après la publication)

En savoir plus sur la [gestion des entrées](entry-management.md) et les [considérations relatives à la durée de qualification des audiences de streaming](audience-qualification-events.md#streaming-entry-caveats).

+++

+++ Que sont les événements d’étape de parcours et comment les utiliser ?

Les événements d’étape de parcours sont des jeux de données générés automatiquement qui capturent des informations détaillées sur chaque étape d’un profil dans un parcours. Ils incluent les événements d’entrée et de sortie, l’exécution d’actions (messages envoyés, actions personnalisées appelées), les transitions de parcours (déplacement entre les activités), les erreurs et les temporisations.

**Cas d’utilisation** :

* Créer des rapports personnalisés dans Customer Journey Analytics ou les outils BI
* Déboguer les problèmes d’exécution du parcours
* Suivre le comportement détaillé du profil
* Créer des modèles d’analyse et d’attribution avancés

En savoir plus sur les [événements d’étape de parcours](../reports/sharing-overview.md).

+++

+++ Comment résoudre un problème lié à un parcours qui ne fonctionne pas comme prévu ?

Journey Optimizer fournit plusieurs ressources de dépannage :

* **Indicateurs d’erreur** : des alertes visuelles dans la zone de travail du parcours mettent en évidence les problèmes de configuration.
* **Mode test** : suivez le parcours pour identifier où les problèmes se produisent.
* **Mode test à blanc** : testez le parcours en utilisant des données de production réelles sans contacter les clientes et clients pour valider le ciblage et l’exécution.
* **Rapports de parcours** : consultez les mesures d’exécution pour identifier les goulots d’étranglement ou les erreurs.
* **Événements d’étape de parcours** : analysez les données d’exécution détaillées pour comprendre le comportement du profil.

**Problèmes courants** :

* Événements ou audiences configurés de manière incorrecte
* Connexions aux sources de données manquantes
* Expressions non valides dans les conditions ou la personnalisation
* Paramètres de temporisation trop courts

En savoir plus sur le [dépannage des parcours](troubleshooting.md).

+++

<!--
+++ What happens if an action fails in a journey?

When an action fails (e.g., API call timeout, message delivery error), the journey continues by default unless configured otherwise. You can define condition activities to handle failure scenarios, and errors are logged in journey reports and step events for monitoring.

**Best practice**: Set appropriate timeout values for external actions and define alternative paths for critical failure scenarios.

Learn more about [action responses](../action/action-response.md).

+++
-->

+++ Puis-je voir qui est actuellement dans mon parcours ?

Oui. Utilisez le **rapport dynamique de parcours** pour afficher les éléments suivants :

* Nombre de profils actuellement dans le parcours
* Nombre de profils à chaque activité
* Profils ayant rejoint le parcours au cours des dernières 24 heures
* Mesures d’exécution en temps réel

Pour afficher des profils individuels, utilisez les **événements d’étape de parcours** dans Customer Journey Analytics ou interrogez directement les jeux de données d’événement d’étape.

En savoir plus sur les [rapports dynamiques de parcours](report-journey.md).

+++

+++ Pourquoi mes messages ne sont-ils pas envoyés dans mon parcours ?

**Raisons et solutions courantes** :

* **Problèmes de consentement** : les destinataires n’ont pas choisi de recevoir des communications.
Solution : vérifiez les politiques de consentement et le statut d’opt-in.

* **Liste de suppression** : les adresses e-mail se trouvent dans la liste de suppression.
Solution : consultez la liste de suppression pour les rebonds ou les plaintes.

* **Coordonnées non valides** : adresses e-mail/numéros de téléphone manquants ou incorrects
Solution : validez la qualité des données de profil.

* **Parcours non publié** : le parcours est toujours en mode brouillon.
Solution : publiez le parcours pour l’activer.

<!-- 
* **Message not approved**: Message content requires approval before sending
  Solution: Submit for approval or check approval status-->

* **Problème de configuration du canal** : la configuration des e-mails/SMS est incorrecte.
Solution : vérifiez les configurations et l’authentification des canaux.

En savoir plus sur le [dépannage](troubleshooting.md) et la [gestion du consentement](../action/consent.md).

+++

+++ Comment personnaliser les messages dans mon parcours ?

Vous pouvez personnaliser vos messages à l’aide de l’**éditeur de personnalisation** :

**Données de personnalisation disponibles** :

* **Attributs de profil** : prénom, nom, e-mail, champs personnalisés
* **Données d’événement** : détails d’achat, comportement de navigation, activité de l’application
* **Données contextuelles** : variables de parcours, données d’API externes
* **Appartenance à une audience** : qualifications de segment
* **Attributs calculés** : valeurs précalculées

**Exemple de personnalisation** :

* « Bonjour `{{profile.firstName}}`, merci pour votre achat de `{{event.productName}}` »
* « En fonction de votre niveau de fidélité (`{{profile.loyaltyTier}}`), voici une offre spéciale »
* Blocs de contenu dynamique qui changent en fonction des préférences du client ou de la cliente

En savoir plus sur la [personnalisation](../personalization/personalize.md).

+++

+++ Puis-je envoyer différents messages en fonction du canal préféré ?

Oui. Utilisez une **[activité de condition](condition-activity.md)** pour acheminer les profils en fonction de leur canal préféré :

1. Ajoutez une [activité de condition](condition-activity.md) à votre parcours.
2. Créez un chemin pour chaque canal en vérifiant l’attribut de profil de canal préféré (par exemple, `profile.preferredChannel`).
3. Configurez les chemins spécifiques aux canaux :
   * **Chemin d’e-mail** : ajoutez une [action d’e-mail](../email/create-email.md) avec du contenu optimisé pour les e-mails.
   * **Chemin SMS** : ajoutez une [action SMS](../sms/create-sms.md) avec un message concis.
   * **Chemin de notification push** : ajoutez une [action de notification push](../push/create-push.md) avec du contenu court et activable.
   * **Chemin in-app** : ajoutez une [action de message in-app](../in-app/create-in-app.md) pour les utilisateurs et utilisatrices engagés de l’application.
4. Ajoutez un chemin par défaut pour les profils sans préférence, en les acheminant vers votre canal principal.

**Bonnes pratiques** :

* Vérifiez que les données de votre profil incluent des préférences de canal précises.
* Concevez du contenu adapté aux forces et limites de chaque canal.
* Utilisez des [surfaces de canal](../configuration/channel-surfaces.md) pour gérer les configurations de canal.
* Testez tous les chemins pour garantir une diffusion correcte des messages.

En savoir plus sur les [conditions](condition-activity.md), les [actions de message](journeys-message.md) et la [sélection de canal](../channels/gs-channels.md).

+++

+++ Puis-je exclure des clientes et des clients de mon parcours ?

Oui, il existe plusieurs façons d’exclure des clientes et des clients :

**À l’entrée du parcours** :

* Utilisez des [définitions d’audience](../audience/creating-a-segment-definition.md) avec des règles d’exclusion.
* Ajoutez des [conditions d’entrée](entry-management.md) qui filtrent des profils spécifiques.
* Configurez des [critères de sortie basés sur les attributs de profil](journey-properties.md) dans les propriétés de parcours pour exclure automatiquement des profils en fonction d’attributs spécifiques.

**Dans le parcours** :

* Ajoutez une [activité de condition](condition-activity.md) au début du parcours pour faire sortir les profils indésirables.
* Vérifiez les attributs d’exclusion (par exemple, statut de VIP, comptes de test).
* Utilisez la [qualification d’audience](audience-qualification-events.md) pour identifier les profils à exclure.

**Exemples de scénarios d’exclusion** :

* Exclure les clientes et clients qui ont récemment effectué un achat.
* Exclure les clientes et clients VIP des promotions standard.
* Exclure les personnes employées et les comptes de test.
* Exclure les clientes et clients de zones géographiques spécifiques.

+++

## Concepts avancés

+++ Qu’est-ce qu’un espace de noms de parcours et pourquoi est-ce important ?

Un **espace de noms** est un type d’identité (par exemple e-mail, ECID, numéro de téléphone) qui détermine la manière dont les profils sont identifiés dans le parcours. L’espace de noms définit l’identifiant utilisé pour faire correspondre les profils, doit être cohérent entre les événements, les audiences et les données de profil, et affecte le comportement d’entrée et de reprise dans le parcours.

**Bonne pratique** : choisissez un espace de noms qui identifie vos clientes et clients de manière fiable à tous les points de contact.

En savoir plus sur les [espaces de noms d’identité](../audience/get-started-identity.md).

+++

+++ Les profils peuvent-ils rejoindre plusieurs fois le même parcours ?

Oui, en fonction des **paramètres de reprise** :

* **Autoriser la reprise** : les profils peuvent rejoindre le parcours plusieurs fois après l’avoir terminé.
* **Période d’attente de reprise** : définissez un délai minimum entre les entrées de parcours (par exemple, 7 jours).
* **Forcer une reprise sur l’événement** : permet de déclencher une nouvelle instance de parcours même si le profil est déjà dans le parcours.
* **Identifiant supplémentaire** : utilisez un identifiant supplémentaire pour permettre aux profils de rejoindre à nouveau le parcours plusieurs fois pour différentes entités (par exemple, différentes commandes, réservations ou transactions), même s’ils sont déjà dans le parcours.

**Bonne pratique** : utilisez les règles de reprise pour éviter la lassitude liée aux messages et garantir une fréquence appropriée. Envisagez d’utiliser des identifiants supplémentaires pour les parcours transactionnels où les profils doivent les rejoindre plusieurs fois pour différentes transactions.

En savoir plus sur la [gestion des entrées](entry-management.md) et les [identifiants supplémentaires](supplemental-identifier.md).

+++

+++ Qu’est-ce que l’optimisation de l’heure d’envoi ?

L’**optimisation de l’heure d’envoi (STO)** utilise l’IA pour prédire le meilleur moment pour envoyer un message à chaque profil individuel, en maximisant les taux d’ouverture et d’engagement. Elle analyse les modèles d’engagement historiques afin de déterminer à quel moment chaque personne destinataire est la plus susceptible d’interagir avec votre message.

**Avantages** :

* Amélioration des taux d’ouverture et de clic
* Une meilleure expérience client grâce à des messages envoyés au moment opportun
* Taux de désabonnement réduits

En savoir plus sur l’[optimisation de l’heure d’envoi](send-time-optimization.md).

+++

+++ Que sont les règles de limitation de parcours ?

La **limitation de parcours** vous permet de contrôler la manière dont les profils interagissent avec les parcours, d’éviter la lassitude liée aux messages et d’assurer une expérience client optimale :

* **Limitation des entrées** : limitez le nombre de fois qu’un profil peut rejoindre des parcours au cours d’une période spécifiée.
* **Limitation de la simultanéité** : limitez le nombre de parcours dans lesquels un profil peut se trouver simultanément.

Vous pouvez définir le nombre maximal d’entrées ou de simultanéité par profil pour plusieurs parcours ou des parcours spécifiques, définir des fenêtres temporelles (quotidiennes, hebdomadaires, mensuelles) et donner la priorité aux parcours lorsque plusieurs parcours se disputent le même profil.

En savoir plus sur les [limitations de parcours](../conflict-prioritization/journey-capping.md).

+++

+++ Puis-je intégrer mon parcours à des systèmes externes ?

Oui. Utilisez des **actions personnalisées** pour appeler des API tierces (CRM, automatisation marketing, systèmes de fidélité), envoyer des données à des systèmes externes, récupérer des informations en temps réel pour la prise de décision et déclencher des workflows dans des plateformes externes.

Les actions personnalisées prennent en charge l’authentification (clé API, authentification personnalisée), la personnalisation de la payload de requête/réponse, la gestion des erreurs et les temporisations, ainsi que les paramètres dynamiques à partir du contexte du parcours.

En savoir plus sur les [actions personnalisées](using-custom-actions.md).

+++

+++ Comment utiliser Adobe Campaign avec les parcours?

Journey Optimizer s’intègre de manière native à Adobe Campaign pour tirer profit de ses fonctionnalités avancées :

* **Adobe Campaign Standard** : utilisez les actions de Campaign Standard pour envoyer des messages transactionnels.
* **Adobe Campaign v7/v8** : déclenchez des workflows Campaign et utilisez l’infrastructure de diffusion de Campaign.

**Bonne pratique** : utilisez cette intégration si vous disposez déjà de modèles Campaign ou de modèles de données, ou si vous avez besoin de fonctionnalités spécifiques à Campaign.

En savoir plus sur l’[intégration à Campaign](ajo-ac.md).

+++

+++ Qu’est-ce que l’activité Saut ?

L’**activité Saut** vous permet de faire passer des profils d’un parcours à un autre, en activant des modèles de parcours réutilisables. Elle permet aussi l’orchestration de parcours sur plusieurs parcours, une maintenance simplifiée des parcours et des stratégies d’engagement progressives.

Lorsqu’un profil atteint une activité Saut, il quitte le parcours en cours et rejoint le parcours cible à son point de départ.

En savoir plus sur l’[activité Saut](jump.md).

+++

+++ Comment créer un parcours de série de bienvenue ?

Une série de bienvenue classique comprend plusieurs points de contact sur plusieurs jours :

**Exemple de structure** :

1. **Entrée** : audience des nouvelles personnes abonnées ou de l’événement lorsqu’une personne s’inscrit.
2. **E-mail 1 – Bienvenue immédiat** : remerciements et présentation
3. **Attente** : 2 jours
4. **E-mail 2 – Prise en main** : tutoriel ou guide produit
5. **Attente** : 3 jours
6. **Condition** : un achat a-t-il été effectué par le client ou la cliente ?
   * **Oui** : terminer ou déplacer vers le parcours client
   * **Non** : continuer la série de bienvenue
7. **E-mail 3 – Avantage incitatif** : réduction spéciale pour le premier achat
8. **Attente** : 5 jours
9. **E-mail 4 – Engagement** : contenu populaire ou meilleures ventes

**Bonnes pratiques** :

* Limitez-vous à 3 à 5 e-mails sur 2 à 3 semaines.
* Chaque e-mail doit avoir un objectif et un appel à l’action clairs.
* Surveillez les taux d’ouverture et ajustez le timing/le contenu en conséquence.
* Faites sortir les clientes et clients plus tôt en cas de conversion ou d’engagement profond.

En savoir plus sur les [cas d’utilisation de parcours](jo-use-cases.md).

+++

+++ Puis-je tester différents chemins dans mon parcours ?

Oui. Utilisez l’**activité Optimiser** (disponibilité limitée) ou créez manuellement des tests de partage :

**Utilisation de l’activité Optimiser** avec la méthode Expérience :

* Répartit de manière aléatoire le trafic entre différents chemins pour déterminer celui qui est le plus performant.
* Teste différents messages, offres, temps d’attente ou chemins de parcours entiers.
* Mesure les performances en fonction de mesures de succès prédéfinies et déclare un chemin gagnant.

**Utilisation de l’activité Optimiser** avec la méthode Condition de source de données :

* Créez une condition qui répartit les profils de manière aléatoire (par exemple à l’aide d’une fonction de nombre aléatoire).
* Envoyez des expériences différentes à chaque partage.
* Mesurez les résultats à l’aide de rapports de parcours.

**Ce que vous pouvez tester** :

* Différentes lignes d’objet d’e-mail
* Contenu de message alternatif
* Différents temps d’attente
* Différents avantages incitatifs ou offres
* Chemins de parcours entièrement différents

En savoir plus sur l’[activité Optimiser](optimize.md) et les [expériences de contenu](../content-management/content-experiment.md).

+++

+++ Comment déclencher un parcours lorsque les stocks sont bas ?

Créez un **parcours d’événement métier** :

1. **Configurer un événement métier** : configurez un événement déclenché par votre système d’inventaire lorsque les stocks passent en dessous d’un certain seuil.
2. **Sélectionner l’audience cible** : sélectionnez les profils à avertir (par exemple, les clientes et clients qui ont consulté le produit, les personnes abonnées aux alertes de réapprovisionnement).
3. **Ajouter une action de message** : envoyez un e-mail ou une notification push.
4. **Personnaliser le contenu** : ajoutez les détails du produit, le niveau actuel des stocks, les messages d’urgence.

**Exemples d’événements métier** :

* Alerte de stock bas
* Notification de baisse de prix
* Produit de retour en stock
* Annonce de vente flash
* Promotions basées sur la météo

En savoir plus sur les [événements métier](general-events.md).

+++

+++ En quoi consistent les politiques de fusion et comment affectent-elles les parcours ?

Les **politiques de fusion** déterminent la manière dont Adobe Experience Platform combine les données provenant de plusieurs sources afin de créer une vue de profil unifiée. Elles définissent les règles de priorité des données et de rapprochement d’identités lorsque des fragments de profils existent dans plusieurs jeux de données différents.

**Impact sur les parcours** :

* Les parcours utilisent la politique de fusion associée à l’audience ou à l’événement pour déterminer quelles données de profil sont disponibles.
   * Dans les parcours Lecture d’audience ou Qualification d’audience : la politique de fusion de l’audience est utilisée.
   * Dans les parcours d’événements unitaires : la politique de fusion par défaut est utilisée.
   * Dans les parcours d’événements métier : la politique de fusion de l’audience ciblée dans l’activité Lecture d’audience suivante est utilisée.

* La politique de fusion affecte les attributs qui sont accessibles dans les conditions de parcours, la personnalisation et les actions.
* Des politiques de fusion différentes peuvent entraîner l’utilisation de données de profil différentes dans le parcours.

**Bonnes pratiques** :

* Assurez-vous que la politique de fusion utilisée par votre parcours est conforme à vos exigences en matière de gouvernance des données.
* Identifiez les jeux de données inclus dans votre politique de fusion pour connaître les données disponibles.
* Utilisez des politiques de fusion cohérentes pour les parcours et les audiences connexes afin d’obtenir des résultats prévisibles.

En savoir plus sur les [politiques de fusion](../audience/get-started-profiles.md) et la [gestion des identités](../audience/get-started-identity.md).

+++

+++ Quelle est la différence entre une condition et une activité d’attente ?

| | **Activité Condition** : | **Activité Attente** |
|---|---|---|
| **Rôle** | Crée différents chemins basés sur une logique (if/then). | Met le parcours en pause pendant une période donnée. |
| **Fonction** | Évalue les données et oriente les profils vers les différents chemins en conséquence. | Maintient les profils à un emplacement spécifique avant de poursuivre. |
| **Cas d’utilisation** | Segmenter une clientèle, vérifier les statuts, créer une branche en fonction du comportement. | Espacer le temps entre des messages, attendre jusqu’aux heures d’ouverture, créer des délais d’attente. |
| **Exemple** | S’il s’agit d’un client ou d’une cliente VIP, envoi d’une offre Premium. Sinon, envoi d’une offre standard. | Patientez 3 jours après l’e-mail de bienvenue avant d’envoyer le message suivant. |

**Elles peuvent être utilisées ensemble** :

* Patientez pendant un certain temps, puis utilisez une condition pour vérifier si un événement s’est produit pendant l’attente.
* Exemple : attendre pendant 7 jours, puis vérifier si le client ou la cliente a effectué un achat.

En savoir plus sur les [conditions](condition-activity.md) et les [activités d’attente](wait-activity.md).

+++

## Bonnes pratiques et limites

+++ Quelles sont les principales limites dont je dois tenir compte ?

Voici certains mécanismes de sécurisation importants :

* **Complexité du parcours** : nombre maximal d’activités, de chemins et de niveaux d’imbrication
* **Débit** : limites du taux d’envoi des messages et des appels API
* **Durée de vie** : durée maximale du parcours (par exemple, 91 jours)
* **Taille de l’audience** : limites des tailles de lots pour les lectures d’audience
* **Complexité de l’expression** : limites de caractères dans les conditions et la personnalisation

Consultez l’intégralité des [mécanismes de sécurisation et des limitations](../start/guardrails.md).

+++

+++ Quelles sont les bonnes pratiques en matière de conception de parcours ?

**Structure et organisation** :

* Centrez vos parcours sur des cas d’utilisation spécifiques.
* Utilisez des noms descriptifs pour les activités.
* Ajoutez des descriptions et des libellés pour les logiques complexes.
* Regroupez les parcours associés avec des balises.

**Performances** :

* Optimisez les temps d’attente pour équilibrer l’engagement et le volume.
* Limitez les appels API externes aux cas d’utilisation essentiels.
* Utilisez des règles de limitation pour éviter la lassitude liée aux messages.
* Surveillez régulièrement les mesures de parcours.

**Tests** :

* Testez toujours vos parcours avant de les publier.
* Utilisez le mode test pour valider la logique de parcours et explorer le parcours étape par étape.
* Utilisez le mode test à blanc pour effectuer des tests avec des données de production réelles sans contacter votre clientèle.
* Testez tous les chemins conditionnels et tous les scénarios.
* Utilisez des profils de test réalistes.
* Validez la personnalisation et le contenu dynamique.

**Maintenance** :

* Vérifiez régulièrement les performances du parcours.
* Arrêtez ou fermez les parcours inutilisés.
* Documentez la logique des parcours et vos règles métier.
* Planifiez des contrôles de versions pour vos parcours.

En savoir plus sur les [bonnes pratiques en matière de conception de parcours](using-the-journey-designer.md).

+++

+++ Combien d’activités puis-je ajouter à un parcours ?

Les parcours sont limités à un maximum de 50 activités. Cependant, nous vous recommandons de simplifier vos parcours pour faciliter leur maintenance et optimiser les performances.

Lorsque les parcours approchent de 50 activités, ils peuvent devenir très complexes et difficiles à gérer, à dépanner et à comprendre. Les longs parcours comprenant de nombreuses branches et conditions peuvent également avoir un impact sur le temps de traitement, la lisibilité, et la collaboration de l’équipe.

**Bonne pratique** : veillez à ce que vos parcours restent ciblés et gérables. Si votre parcours devient complexe, envisagez les points suivants :

* Divisez-le en plusieurs parcours à l’aide de l’activité Saut.
* Créez des modèles réutilisables pour des parcours plus simples.
* Simplifiez la logique avec des conditions plus efficaces.
* Vérifiez si toutes les activités sont nécessaires.

En savoir plus sur la [conception de parcours](using-the-journey-designer.md) et les [mécanismes de sécurisation et les limitations](../start/guardrails.md).

+++

+++ Comment puis-je m’assurer que mon parcours fonctionne bien à grande échelle ?

**Éléments de conception à prendre en compte** :

* Utilisez l’[entrée basée sur l’audience](read-audience.md) pour les communications par lots au lieu d’événements individuels.
* Implémentez des [temps d’attente](wait-activity.md) appropriés pour répartir le volume des messages.
* Utilisez des [règles de limitation](../conflict-prioritization/journey-capping.md) pour éviter une surcharge du système.
* Optimisez la [logique des conditions](condition-activity.md) pour réduire la complexité du traitement.

**Surveillance** :

* Effectuez régulièrement un suivi des [mesures du parcours](report-journey.md).
* Surveillez les performances de l’API pour les [actions personnalisées](using-custom-actions.md).
* Consultez les taux d’erreur et les occurrences de temporisation à l’aide des [outils de résolution de problèmes](troubleshooting.md).
* Abonnez-vous aux [alertes](../reports/alerts.md) d’échecs critiques de parcours.

**Optimisation** :

* Utilisez le [mode test](testing-the-journey.md) et le [test à blanc](journey-dry-run.md) pour valider les performances avant la publication.
* Minimisez les appels API externes par le biais d’[actions personnalisées](using-custom-actions.md) pour éviter de la latence et la dépendance à des systèmes tiers.
* Lorsque cela est possible, stockez les données fréquemment utilisées dans Adobe Experience Platform à l’aide de la [recherche de jeu de données](dataset-lookup.md) au lieu d’effectuer des appels externes.
* Examinez et optimisez les performances des [diffusions des messages](journeys-message.md).

En savoir plus sur les [mécanismes de sécurisation et les limitations](../start/guardrails.md).

+++

## Ressources supplémentaires

Pour des mises à jour et des formations supplémentaires, consultez les ressources suivantes :

* [Commencer les parcours](journey.md)
* [Créer votre premier parcours](journey-gs.md)
* [Guides de résolution des problèmes](troubleshooting.md)
* [Cas d’utilisation de parcours](jo-use-cases.md)
* [Description du produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
