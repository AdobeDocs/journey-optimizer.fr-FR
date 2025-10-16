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
hide: true
hidefromtoc: true
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '2363'
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

Adobe Journey Optimizer prend en charge trois types de parcours :

* **parcours unitaires** : ils sont déclenchés individuellement par un événement (par exemple, un achat, une connexion à l’application). Les profils rejoignent le parcours un par un lorsque l’événement se produit.
* **Lire les parcours d’audience** : commencez avec une audience de Adobe Experience Platform et envoyez des messages par lots à tous les profils de cette audience.
* **parcours d’événement métier** : ils sont déclenchés par des événements métier (par exemple, les mises à jour de stocks, les alertes météorologiques) qui affectent plusieurs profils simultanément.

En savoir plus sur les [types de parcours &#x200B;](entry-management.md#types-of-journeys).

+++

+++ Quelle est la différence entre un parcours et une campagne ?

Les **Parcours** sont des orchestrations à plusieurs étapes qui réagissent aux événements ou aux audiences cibles, en tenant compte d’une logique complexe, des conditions, des temps d’attente et de plusieurs points de contact tout au long du cycle de vie du client.

Les **campagnes** sont des communications ponctuelles ou récurrentes envoyées à une audience spécifique. Elles sont idéales pour les messages autonomes tels que les annonces promotionnelles ou les newsletters.

**Bonne pratique** : utilisez des parcours pour un engagement continu et à plusieurs étapes, ainsi que des campagnes pour des communications ciblées et autonomes.

+++

+++ Quels sont les principaux composants d’un parcours ?

Un parcours comprend :

* **Événements** : points d’entrée qui déclenchent le parcours (par exemple, qualification du profil, événements métier)
* **Activités d’orchestration** : composants logiques tels que les conditions, l’attente, la lecture d’audience et la fin
* **Actions** : activités qui effectuent des tâches, comme envoyer des messages, mettre à jour des profils ou appeler des API externes
* **Actions de canal intégrées** : fonctionnalités de messagerie natives pour les e-mails, SMS, notifications push et autres canaux
* **Actions personnalisées** : intégration à des systèmes tiers

En savoir plus sur les [activités de parcours &#x200B;](about-journey-activities.md).

+++

## Création de parcours

+++ Comment puis-je commencer à créer mon premier parcours ?

Procédez comme suit :

1. **Configurer les conditions préalables** : configurez les événements, les sources de données et les actions selon les besoins
2. **Création du parcours** : accédez au menu Parcours et cliquez sur « Créer un Parcours ».
3. **Définir les propriétés du parcours** : définissez le nom, la description, l’espace de noms du parcours et d’autres paramètres
4. **Conception du parcours** : faites glisser et déposez les activités de la palette vers la zone de travail
5. **Tester le parcours** : utilisez le mode test pour valider la logique de parcours
6. **Publier le parcours** : activez le parcours pour le rendre actif

Suivez le [guide détaillé](journey-gs.md).

+++

+++ Quelles sont les conditions préalables requises avant de créer un parcours ?

Les prérequis dépendent de votre type de parcours :

* **parcours déclenchés par un événement** : configurez les événements pour définir quand les profils doivent entrer dans le parcours
* **parcours basés sur l’audience** : création d’audiences dans Adobe Experience Platform
* **Enrichissement des données** : configurez les sources de données pour récupérer des informations supplémentaires
* **Intégrations tierces** : configuration des actions personnalisées si vous utilisez des systèmes externes

En savoir plus sur la configuration du parcours [&#128279;](../configuration/about-data-sources-events-actions.md).

+++

+++ Puis-je utiliser des données provenant de systèmes externes dans mon parcours ?

Oui. Vous pouvez configurer **sources de données externes** pour récupérer des informations à partir de services d’API tiers et les utiliser dans vos conditions de parcours, personnalisation ou actions. Vous pouvez ainsi enrichir l’expérience client avec des données en temps réel provenant de votre CRM, de vos systèmes de fidélité, de vos services météorologiques ou d’autres plateformes externes.

En savoir plus sur les [sources de données externes](../datasource/external-data-sources.md).

+++

+++ Comment ajouter des conditions à mon parcours ?

Vous pouvez ajouter des conditions à l’aide de l’activité **Condition** de la palette d’orchestration. Les conditions vous permettent d’effectuer les opérations suivantes :

* Créer des conditions simples ou avancées à l’aide de l’éditeur d’expression
* Divisez le parcours en plusieurs chemins d’accès en fonction des attributs de profil, de l’appartenance à l’audience, des événements ou des données contextuelles
* Définir des chemins de temporisation pour les profils qui ne remplissent pas la condition dans un délai spécifié

En savoir plus sur les [&#x200B; conditions &#x200B;](condition-activity.md).

+++

+++ Puis-je envoyer des messages aux profils d&#39;un parcours ?

Oui. Journey Optimizer comprend des **actions de canal intégrées** qui vous permettent d’envoyer des messages par e-mail, des notifications push, des SMS/MMS/RCS, des messages in-app, des expériences web, des expériences basées sur du code, du courrier, des cartes de contenu, WhatsApp et LINE. Vous pouvez concevoir le contenu des messages directement dans Journey Optimizer et les ajouter en tant qu’activités d’action dans votre parcours.

En savoir plus sur les [messages dans parcours](journeys-message.md).

+++

+++ Comment puis-je attendre une heure ou un événement spécifique dans un parcours ?

Utilisez l’activité **Attente** pour suspendre le parcours pendant une durée spécifiée ou jusqu’à une date/heure spécifique. Les activités d’attente sont utiles pour :

* Envoyer des messages de relance après un délai (par exemple, 3 jours après l’achat)
* Patientez pendant heures ouvrables avant d’effectuer une action
* Création de campagnes goutte-à-goutte avec des intervalles temporels
* Combinaison avec des conditions pour créer des scénarios de temporisation

En savoir plus sur les [&#x200B; activités d’attente &#x200B;](wait-activity.md).

+++

+++ Puis-je mettre à jour les informations de profil au sein d’un parcours ?

Oui. Utilisez l&#39;activité **Mettre à jour le profil** pour modifier les attributs de profil dans Adobe Experience Platform en fonction d&#39;événements ou de conditions de parcours. Cela s’avère utile pour mettre à jour les points de fidélité, enregistrer les jalons du parcours, modifier les paramètres de préférences ou suivre les scores d’engagement des clients.

En savoir plus sur les [mises à jour de profil](update-profiles.md).

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

* Le parcours devient **actif** prêt à accepter de nouveaux profils
* Les profils peuvent saisir des données en fonction des critères d’entrée (événement ou audience)
* Les messages et les actions commencent à s’exécuter pour les profils qui se déplacent dans le parcours
* Vous ne pouvez pas modifier directement un parcours publié (vous devez créer une version)

En savoir plus sur la [publication de parcours &#x200B;](publishing-the-journey.md).

+++

+++ Puis-je modifier un parcours déjà publié ?

Vous ne pouvez pas modifier directement un parcours dynamique. Pour apporter des modifications :

1. **Créer une version** : dupliquez le parcours publié pour créer un brouillon
2. **Apporter vos modifications** : modifiez le brouillon selon vos besoins.
3. **Tester la nouvelle version** : utilisez le mode test pour valider les modifications
4. **Publier la nouvelle version** : ferme automatiquement la version précédente et active la nouvelle

Les profils déjà dans le parcours termineront la version originale, tandis que les nouveaux profils entreront la nouvelle version.

En savoir plus sur les [versions de parcours &#x200B;](journey-ui.md#journey-versions).

+++

+++ Comment arrêter un parcours ?

Vous pouvez gérer l’exécution du parcours de plusieurs manières :

* **Fermer aux nouvelles entrées** : empêcher les nouveaux profils de saisir tout en permettant aux profils existants de terminer leur parcours
* **Arrêter immédiatement** : arrêtez le parcours et quittez tous les profils qu’il contient actuellement.
* **Pause** : interrompt temporairement le parcours et le reprend ultérieurement (disponible pour certains types de parcours).

En savoir plus sur les [parcours d’envoi](end-journey.md).

+++

## Exécution et surveillance des parcours

+++ Comment puis-je suivre la progression du profil via un parcours ?

Vous pouvez surveiller l’exécution du parcours à l’aide des éléments suivants :

* **Rapport dynamique sur les Parcours** : affichez les mesures et les KPI en temps réel pour votre parcours
* **Rapport sur les Parcours à tout moment** : analyser les performances des parcours à l’aide de Customer Journey Analytics
* **Événements d’étape de Parcours** : accédez aux données d’exécution détaillées pour les rapports personnalisés
* **Tableau de bord d’exécution d’essai de Parcours** : vérifiez les résultats de l’exécution de test avant la mise en ligne

En savoir plus sur les rapports de parcours [&#128279;](report-journey.md).

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

En savoir plus sur les [événements d’étape de parcours &#x200B;](../reports/sharing-overview.md).

+++

+++ Comment résoudre un problème lié à un parcours qui ne fonctionne pas comme prévu ?

Journey Optimizer fournit plusieurs ressources de dépannage :

* **Indicateurs d’erreur** : les alertes visuelles dans la zone de travail du parcours mettent en évidence les problèmes de configuration
* **Mode test** : suivez le parcours pour identifier où les problèmes se produisent
* **Rapports de Parcours** : consultez les mesures d’exécution pour identifier les goulets d’étranglement ou les erreurs
* **Événements d’étape de Parcours** : analyser les données d’exécution détaillées pour comprendre le comportement du profil

**Problèmes courants** :

* Événements ou audiences configurés de manière incorrecte
* Connexions à la source de données manquantes
* Expressions non valides dans les conditions ou la personnalisation
* Paramètres de temporisation trop courts

En savoir plus sur [résolution des problèmes liés aux parcours &#x200B;](troubleshooting.md).

+++

+++ Que se passe-t-il si une action échoue dans un parcours ?

Lorsqu’une action échoue (par exemple, délai d’appel de l’API, erreur de diffusion du message), le parcours se poursuit par défaut, sauf configuration contraire. Vous pouvez définir des activités de condition pour gérer les scénarios d’échec. Les erreurs sont consignées dans les rapports de parcours et les événements d’étape pour la surveillance.

**Bonne pratique** : définissez des valeurs de délai d’expiration appropriées pour les actions externes et définissez des chemins alternatifs pour les scénarios d’échec critique.

En savoir plus sur les [&#x200B; réponses d’action &#x200B;](../action/action-response.md).

+++

## Concepts avancés

+++ Qu’est-ce qu’un espace de noms de parcours et pourquoi est-ce important ?

Un **espace de noms** est un type d’identité (par exemple e-mail, ECID, numéro de téléphone) qui détermine la manière dont les profils sont identifiés dans le parcours. L’espace de noms définit l’identifiant utilisé pour faire correspondre les profils, doit être cohérent entre les événements, les audiences et les données de profil, et affecte le comportement d’entrée et de reprise sur le parcours.

**Bonne pratique** : choisissez un espace de noms qui identifie vos clients de manière fiable à tous les points de contact.

En savoir plus sur les [&#x200B; espaces de noms d’identité &#x200B;](../audience/get-started-identity.md).

+++

+++ Les profils peuvent-ils entrer plusieurs fois dans le même parcours ?

Oui, selon les **paramètres de rentrée** :

* **Autoriser une reprise** : les profils peuvent rejoindre le parcours plusieurs fois après l’avoir terminé
* **Période d’attente de reprise** : définissez un temps minimum entre les entrées de parcours (par exemple, 7 jours).
* **Forcer une reprise sur l’événement** : permet de déclencher une nouvelle instance de parcours même si le profil est déjà dans le parcours

**Bonne pratique** : utilisez les règles de rentrée pour éviter la fatigue des messages et garantir une fréquence appropriée.

En savoir plus sur la [gestion des entrées](entry-management.md).

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

La limitation des Parcours **&#x200B;**&#x200B;vous permet de limiter le nombre de fois qu’un profil peut entrer des parcours au cours d’une période spécifiée, ce qui évite la fatigue des messages et garantit une expérience client optimale. Vous pouvez définir le nombre maximal d’entrées par profil sur plusieurs parcours ou parcours spécifiques, définir des fenêtres temporelles (quotidiennes, hebdomadaires, mensuelles) et donner la priorité aux parcours lorsque plusieurs parcours se disputent le même profil.

En savoir plus sur la limitation du parcours [&#128279;](../conflict-prioritization/journey-capping.md).

+++

+++ Puis-je intégrer mon parcours à des systèmes externes ?

Oui. Utilisez des **actions personnalisées** pour appeler des API tierces (CRM, automatisation marketing, systèmes de fidélité), envoyer des données à des systèmes externes, récupérer des informations en temps réel pour la prise de décision et déclencher des workflows dans des plateformes externes.

Les actions personnalisées prennent en charge l’authentification (clé API, OAuth 2.0), la personnalisation de la payload de requête/réponse, la gestion des erreurs et les délais d’expiration, ainsi que les paramètres dynamiques à partir du contexte du parcours.

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

En savoir plus sur [&#x200B; l’activité Saut &#x200B;](jump.md).

+++

## Bonnes pratiques et restrictions

+++ Quelles sont les principales limites dont je dois tenir compte ?

Les mécanismes de sécurisation importants sont les suivants :

* **Complexité du Parcours** : nombre maximal d’activités, de chemins et de niveaux d’imbrication
* **Débit** : taux d’envoi des messages et limites des appels API
* **Durée de vie** : durée maximale du parcours (par exemple, 91 jours pour les parcours unitaires).
* **Taille de l’audience** : limites des tailles de lot d’audience lue
* **Complexité de l’expression** : limites de caractères dans les conditions et la personnalisation

Affichage complet [mécanismes de sécurisation et limitations](../start/guardrails.md).

+++

+++ Quelles sont les bonnes pratiques en matière de conception de parcours ?

**Structure et organisation** :

* Concentrer les parcours sur des cas d’utilisation spécifiques
* Utiliser des noms descriptifs pour les activités
* Ajout de notes et de libellés pour une logique complexe
* Regrouper les parcours associés avec des balises

**Performances** :

* Optimisez les temps d’attente pour équilibrer l’engagement et le volume
* Limiter les appels API externes aux cas d’utilisation essentiels
* Utilisation des règles de limitation pour éviter la fatigue des messages
* Surveiller régulièrement les mesures de parcours

**Test** :

* Toujours tester les parcours avant la publication
* Tester tous les chemins et scénarios conditionnels
* Utiliser des profils de test réalistes
* Validation de la personnalisation et du contenu dynamique

**Maintenance** :

* Vérifier régulièrement les performances du parcours
* Archiver ou fermer les parcours inutilisés
* Logique de parcours de document et règles de gestion
* Planifier le contrôle de version du parcours

En savoir plus sur les [bonnes pratiques de conception de parcours &#x200B;](using-the-journey-designer.md).

+++

+++ Combien d’activités puis-je ajouter à un parcours ?

Bien qu’il n’y ait pas de limite stricte au nombre d’activités, des parcours très complexes (plus de 50 activités) peuvent devenir difficiles à gérer et à résoudre. Les parcours volumineux avec de nombreuses branches et conditions peuvent avoir un impact sur le temps de traitement et la lisibilité.

**Bonne pratique** : si votre parcours devient trop complexe, pensez à le diviser en plusieurs parcours à l’aide de l’activité Saut , à créer des sous-parcours réutilisables ou à simplifier la logique avec des conditions plus efficaces.

En savoir plus sur la conception de parcours [&#128279;](using-the-journey-designer.md).

+++

+++ Comment puis-je m’assurer que mon parcours fonctionne bien à grande échelle ?

**Considérations de conception** :

* Utilisez une entrée basée sur l’audience pour les communications par lots au lieu d’événements individuels.
* Mettre en œuvre des temps d’attente appropriés pour répartir le volume des messages
* Utiliser les règles de limitation pour éviter la surcharge du système
* Optimisation de la logique des conditions pour réduire la complexité du traitement

**Surveillance** :

* Effectuer régulièrement le suivi des mesures de parcours
* Surveillance des performances de l’API pour les actions personnalisées
* Consulter les taux d’erreur et les occurrences de dépassement de délai
* Configurer des alertes pour les échecs de parcours critiques

**Optimisation** :

* Utilisez le mode test et exécution d’essai pour valider les performances avant la publication.
* Limiter les appels de sources de données externes aux scénarios essentiels
* Mettre en cache les données fréquemment consultées lorsque cela est possible
* Examiner et optimiser les performances de diffusion des messages

En savoir plus sur l’[optimisation des parcours &#x200B;](../start/guardrails.md).

+++

## Ressources supplémentaires

Pour des mises à jour et des formations supplémentaires, consultez les ressources suivantes :

* [Commencer les parcours](journey.md)
* [Créer votre premier parcours](journey-gs.md)
* [Guides de dépannage](troubleshooting.md)
* [Cas d’utilisation de parcours](jo-use-cases.md)
* [Description du produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
