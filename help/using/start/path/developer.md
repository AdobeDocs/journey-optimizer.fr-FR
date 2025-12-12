---
title: Prise en main pour les développeurs
description: En tant que développeur, découvrez comment utiliser Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1891'
ht-degree: 2%

---

# Prise en main pour les développeurs {#get-started-developers}

En tant que **développeur**, vous êtes responsable de la mise en œuvre et de l’intégration des [!DNL Adobe Journey Optimizer] dans vos applications et systèmes. Vous pouvez commencer à utiliser [!DNL Adobe Journey Optimizer] une fois que l’[administrateur système](administrator.md) et l’[ingénieur de données](data-engineer.md) vous ont accordé l’accès et ont préparé votre environnement.

## Votre rôle dans l’écosystème Journey Optimizer

Tandis que d’autres membres de l’équipe configurent Journey Optimizer par le biais de l’interface utilisateur, vous vous concentrerez sur :

* **Mise en œuvre des SDK** dans les applications mobiles et web
* **Envoi d’événements** depuis vos applications pour déclencher des parcours
* **Création de points d’entrée d’API** que Journey Optimizer peut appeler via des actions personnalisées
* **Intégration** Journey Optimizer à vos systèmes et infrastructures existants
* **Test et débogage** vos implémentations

Votre [ingénieur de données](data-engineer.md) s’occupera des schémas de données, des configurations d’événement et des sources de données. Votre [administrateur](administrator.md) configurera les autorisations et les configurations de canal. Les [marketeurs](marketer.md) concevront les parcours et le contenu qui utilisent vos implémentations.

Ce guide décrit les étapes essentielles de mise en œuvre technique pour commencer à utiliser Journey Optimizer. Que vous créiez des applications mobiles, des expériences web ou des intégrations d’API, suivez les sections ci-dessous pour configurer votre implémentation.

## Conditions préalables {#prerequisites}

Avant de commencer l’implémentation, vérifiez que vous disposez des éléments suivants :

**Compétences techniques :**

* Expérience avec JavaScript (pour Web SDK) ou Swift/Kotlin (pour Mobile SDK)
* Compréhension des API RESTful et JSON
* Familiarité avec la programmation asynchrone et les architectures basées sur les événements
* Connaissance de l’architecture d’application de votre entreprise

**Accès et outils :**

* Accès à [Adobe Developer Console](https://developer.adobe.com){target="_blank"} pour les informations d’identification d’API
* Environnement de développement avec accès à la base de code de votre application.
* Test d’outils tels que Postman pour le test des API
* Outils de développement de navigateur ou outils de débogage mobile

**D’autres membres de l’équipe :**

* Accès à l’environnement accordé par votre [administrateur](administrator.md)
* Schémas XDM et définitions d’événement de votre [ingénieur de données](data-engineer.md)
* Exigences et cas d’utilisation de vos [marketeurs](marketer.md)

## Comprendre les bases techniques {#technical-foundation}

Avant de passer à la mise en œuvre, familiarisez-vous avec les concepts techniques de base :

1. **Intégration de Adobe Experience Platform** : Journey Optimizer est créé en mode natif sur Adobe Experience Platform. Comprendre l’architecture sous-jacente vous aidera à créer des implémentations plus efficaces. En savoir plus sur [le fonctionnement de Journey Optimizer](../understanding-ajo.md).

1. **Modèles de données XDM** : Journey Optimizer utilise le modèle de données d’expérience (XDM) pour structurer les données d’événement et de profil. En tant que développeur, vous devez comprendre comment envoyer des données conformes aux schémas configurés par votre [ingénieur de données](data-engineer.md). En savoir plus sur les [schémas XDM](../../data/get-started-schemas.md).

1. **Authentification et sécurité** : toutes les implémentations nécessitent une authentification appropriée. Découvrez comment configurer l’authentification pour les SDK et les API. En savoir plus sur l’[authentification API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configurer les intégrations d’applications mobiles {#mobile-integration}

### Configuration de Adobe Experience Platform Mobile SDK

Pour activer les notifications push, les messages in-app et d’autres fonctionnalités mobiles, intégrez Adobe Experience Platform Mobile SDK à vos applications mobiles.

1. **Installer et configurer Mobile SDK** : consultez la [documentation de Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} pour commencer à intégrer SDK.

1. **Créer une propriété mobile** : configurez une propriété mobile dans [!DNL Adobe Experience Platform Data Collection]. Découvrez comment [créer et configurer une propriété mobile](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurer les notifications push** :
   * Pour les **applications iOS** : enregistrez votre application auprès d’APNs (service de notification push Apple). En savoir plus dans la [documentation Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Pour les **applications Android** : configurez Firebase Cloud Messaging pour votre application Android. En savoir plus dans la documentation de [Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Tester votre intégration mobile** : utilisez le workflow de démarrage rapide de l’intégration mobile [mobile](../../push/mobile-onboarding-wf.md) pour configurer et tester rapidement votre configuration mobile.

Les étapes détaillées pour configurer les notifications push sont disponibles sur [&#x200B; cette page &#x200B;](../../push/push-configuration.md).

### Mise en œuvre d’expériences basées sur du code (Mobile SDK)

Pour la personnalisation des applications mobiles natives à l’aide d’expériences basées sur du code :

* Suivez [ce tutoriel](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} pour la mise en œuvre de Mobile SDK
* Examinez les exemples d’implémentation pour [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} et [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implémenter des expériences web {#web-implementation}

### Configurer le SDK Web Adobe Experience Platform

Pour les implémentations web, le Web SDK est votre principal point d’intégration :

1. **Installation de Web SDK** : suivez le [Guide de mise en œuvre de Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} pour configurer le SDK sur votre site Web.

1. **Configurer les flux de données** : créez et configurez un flux de données en [!DNL Adobe Experience Platform Data Collection] avec Journey Optimizer activé. Pour en savoir plus, consultez la [documentation sur les flux de données](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}.

1. **Activer les notifications push web** (facultatif) : configurez la propriété [pushNotifications](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} dans votre configuration Web SDK et utilisez la commande [sendPushSubscription](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} pour enregistrer les abonnements push.

### Implémenter des expériences basées sur du code (Web SDK)

Les expériences basées sur le code vous permettent de personnaliser n’importe quel point de contact numérique :

1. **Choisissez votre méthode d’implémentation** : côté client, côté serveur ou hybride. Examinez les [exemples d’implémentation](../../code-based/code-based-implementation-samples.md) pour chaque approche.

1. **Définir des surfaces** : identifiez les emplacements de votre application où vous souhaitez diffuser du contenu personnalisé. En savoir plus sur la [configuration de surface](../../code-based/code-based-surface.md).

1. **Implémenter le rendu du contenu** : utilisez le SDK Web pour récupérer et appliquer le contenu de personnalisation. Voir [tutoriels de mise en œuvre basés sur du code](../../code-based/code-based-decisioning-implementations.md).

1. **Envoyer des événements d’affichage et d’interaction** : suivez le moment où le contenu est affiché et le moment où les utilisateurs et utilisatrices interagissent avec celui-ci pour les analyses et l’optimisation.

Explorez [exemples d’implémentation sur GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} pour voir en action les expériences basées sur le code.

En savoir plus sur la [prise en main des expériences basées sur du code](../../code-based/get-started-code-based.md).

## Implémentation de la diffusion en continu d’événements {#event-streaming}

### Envoyer des événements pour déclencher des parcours

En tant que développeur, vous implémenterez le code pour envoyer des événements qui déclenchent des parcours. Votre [ingénieur de données](data-engineer.md) configure les schémas et les définitions d’événement dans Journey Optimizer.

1. **Présentation de la payload d’événement** : contactez l’ingénieur de données pour obtenir le schéma d’événement et la structure de payload requise. La payload doit être conforme au schéma XDM qu’ils ont configuré. Découvrez les [exigences relatives au schéma d’événement](../../event/experience-event-schema.md).

1. **Implémenter la diffusion en continu des événements** : envoyez des événements à Adobe Experience Platform à l’aide des [API d’ingestion en flux continu](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=fr){target="_blank"}. Découvrez les [étapes pour envoyer des événements](../../event/additional-steps-to-send-events-to-journey.md).

1. **Gérer les types d&#39;événements** :
   * **Événements unitaires** : implémentez l’envoi d’événement pour les actions spécifiques à une personne (par exemple, clic sur un bouton, achèvement de l’achat)
   * **Événements métier** : envoyez des événements métier (par exemple, des mises à jour d’inventaire, des modifications de prix).

1. **Tester la diffusion d’événement** : vérifiez que les événements sont correctement reçus et déclenchez les parcours comme prévu. En savoir plus sur la [résolution des problèmes d’événement](../../building-journeys/troubleshooting-inbound.md).

**Exemple d’implémentation** pour envoyer un événement via l’API :

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

En savoir plus sur [l’utilisation d’événements de parcours &#x200B;](../../event/about-events.md).

## Développement de points d’entrée d’action personnalisés {#custom-actions}

Les actions personnalisées permettent aux parcours d’appeler vos API. En tant que développeur, vous allez créer les points d’entrée d’API appelés par les actions personnalisées :

1. **Créer votre point d’entrée API** : créez des points d’entrée API RESTful que Journey Optimizer appellera lors de l’exécution du parcours. Votre point d’entrée doit :
   * Acceptation des payloads JSON
   * Requêtes d’authentification (OAuth, clé API ou JWT)
   * Traiter les demandes dans des délais impartis appropriés
   * Renvoyer les réponses au format attendu

1. **Comprendre les fonctionnalités d’action personnalisée** : les actions personnalisées peuvent se connecter à des systèmes tiers tels qu’Epsilon, Slack, Firebase ou vos propres services. En savoir plus sur les [actions personnalisées](../../action/action.md).

1. **Utiliser les configurations d’action** : votre [administrateur](administrator.md) ou [ingénieur de données](data-engineer.md) configure l’action personnalisée dans Journey Optimizer, en définissant l’URL du point d’entrée de l’API, la méthode d’authentification et les paramètres. Vous leur fournirez votre spécification d’API. En savoir plus sur la [configuration d’une action personnalisée](../../action/about-custom-action-configuration.md).

1. **Renvoyer des données exploitables** : concevez votre API pour renvoyer des données qui peuvent être utilisées dans les étapes de parcours suivantes. En savoir plus sur les [réponses d’action](../../action/action-response.md).

1. **Implémenter la limitation de débit** : assurez-vous que vos points d’entrée peuvent gérer le volume attendu. Journey Optimizer applique une limite de 5 000 appels/seconde, mais votre système doit être résilient. En savoir plus sur le [plafonnement et limitation](../../configuration/external-systems.md).

**Exemple de cas d’utilisation** : [écriture d’événements de parcours dans Experience Platform](../../building-journeys/custom-action-aep.md) utilisation d’actions personnalisées.

## Utiliser des API Journey Optimizer {#apis}

Journey Optimizer fournit des API REST complètes pour un accès programmatique :

1. **Comprendre les fonctionnalités de l’API** : les API Journey Optimizer vous permettent de créer, lire, mettre à jour et supprimer diverses ressources par programmation. En savoir plus sur les [API Journey Optimizer](../../configuration/ajo-apis.md).

1. **Authentification** : suivez [ce tutoriel](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} pour configurer l’authentification de l’API à l’aide de Adobe Developer Console.

1. **Explorer les références d’API** : parcourez la documentation complète de l’API et essayez les API directement dans la référence de l’API Adobe Journey Optimizer [&#128279;](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campagnes déclenchées par API** : créez des messages transactionnels avec des campagnes déclenchées par API. Pour les scénarios de volume élevé (jusqu’à 5 000 TPS), explorez le [mode Débit élevé](../../campaigns/api-triggered-high-throughput.md) (nécessite une licence de module complémentaire).

1. **API Decision Management** : utilisez des API spécialisées pour la gestion des offres et la prise de décisions. Pour en savoir plus, consultez le [guide de l’API Decision Management](../../offers/api-reference/getting-started.md).

## Tests et débogage {#testing}

1. **Implémentation de Debug SDK** : utilisez Adobe Experience Platform Assurance pour inspecter les événements SDK, valider la collecte de données et résoudre les problèmes d’intégration en temps réel. [En savoir plus sur Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=fr){target="_blank"}.

1. **Tester la diffusion d’événement** : vérifiez que les événements de votre application sont correctement reçus par Adobe Experience Platform et déclenchez les parcours comme prévu. Surveillez l’ingestion des événements et validez la structure de la payload.

1. **Valider les intégrations d’API** : testez vos points d’entrée d’action personnalisés pour vous assurer qu’ils gèrent correctement les requêtes Journey Optimizer, répondent dans les limites de délai d’expiration et renvoient les formats de données attendus.

1. **Utilisation du mode test avec des profils de test** : contactez votre [ingénieur de données](data-engineer.md) pour obtenir l’accès aux profils de test, puis validez votre implémentation à l’aide du mode test de parcours. Découvrez comment [tester des parcours &#x200B;](../../building-journeys/testing-the-journey.md).

1. **Surveiller les journaux SDK** : activez la journalisation du débogage dans votre implémentation de SDK pour résoudre les problèmes lors du développement :
   * **Mobile SDK** : activez la journalisation pour afficher les événements SDK et les appels API
   * **Web SDK** : utilisez la console du navigateur pour surveiller l’activité de SDK

1. **Vérifier la configuration du flux de données** : vérifiez que votre flux de données est correctement configuré pour envoyer des données à Journey Optimizer. Vérifiez que les événements traversent le flux de données vers les destinations correctes.

1. **Données de parcours de requête pour analyse** : utilisez des requêtes SQL sur le lac de données pour analyser les événements d’étape de parcours, les problèmes de débogage et surveiller les performances des actions personnalisées. Explorez [exemples de requêtes pour l’analyse de parcours &#x200B;](../../reports/query-examples.md) notamment :
   * Suivi des entrées/sorties du profil et raisons des rejets
   * Mesures de performances des actions personnalisées (latence, débit, erreurs)
   * Modèles de diffusion d’événements et d’erreurs
   * Parcours des états d’instance

## Rubriques de développement avancées {#advanced-topics}

### Utilisation des données contextuelles et de l’enrichissement

* **Itérer sur des tableaux** : utilisez la syntaxe Handlebars pour afficher des listes dynamiques à partir d’événements, de réponses d’action personnalisée et de recherches de jeux de données dans les messages. En savoir plus sur [l’itération des données contextuelles](../../personalization/iterate-contextual-data.md).
* **Recherche de jeu de données** : implémentez des recherches de jeu de données pour enrichir les données de parcours à partir des jeux de données Adobe Experience Platform. Contactez votre ingénieur de données pour la configuration. En savoir plus sur la [recherche de jeu de données](../../building-journeys/dataset-lookup.md).

### Utilisation du consentement et de la gouvernance

Mettez en œuvre des politiques de gouvernance des données et de consentement dans vos intégrations :

* **Gouvernance des données** : appliquez des politiques d’utilisation des données aux actions personnalisées. En savoir plus sur la [gouvernance des données](../../action/action-privacy.md).
* **Gestion du consentement** : gérez les préférences de consentement des clients dans vos implémentations. En savoir plus sur le [consentement](../../action/consent.md).

### Optimisation et bonnes pratiques

* **Plafonnement et limitation** : comprenez les limites de débit et implémentez un ralentissement approprié. En savoir plus sur les [systèmes externes](../../configuration/external-systems.md).
* **Optimisation des Parcours** : suivez les bonnes pratiques pour l’optimisation des parcours [&#128279;](../../building-journeys/optimize.md).
* **Gestion des erreurs** : implémentez une gestion des erreurs robuste. Consultez les [codes d’erreur](../../building-journeys/error-codes-reference.md) et [guides de dépannage](../../building-journeys/troubleshooting.md).

## Ressources supplémentaires {#additional-resources}

* **Developer Console** : accédez à [Adobe Developer Console](https://developer.adobe.com){target="_blank"} pour créer des intégrations et gérer les informations d’identification d’API.
* **Exemple de code** : explorez [exemples d’implémentation sur GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Tutoriels vidéo** : apprenez grâce à des tutoriels pratiques sur [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr){target="_blank"}.
* **Communauté des développeurs** : entrez en contact avec d’autres développeurs et développeuses et obtenez de l’aide sur les forums de la communauté Adobe.

## Collaboration entre les rôles {#next-steps}

Votre travail d’implémentation croise d’autres membres de l’équipe :

**Utilisation de [Ingénieurs de données](data-engineer.md):**

* Obtenez les schémas XDM et les structures d’événement que vous devez implémenter
* Identifiez les événements à envoyer et le format de payload requis
* Aligner sur les exigences de collecte de données et les normes de qualité des données
* Tester conjointement la diffusion d’événements et l’ingestion de données

**Utilisation de [Administrateurs](administrator.md):**

* Fournir les spécifications d’API pour les actions personnalisées qu’ils configureront
* Demander les autorisations nécessaires et les informations d’identification d’API
* Coordination des exigences de configuration des canaux (par exemple, certificats push)
* Alignement sur les environnements de test et la stratégie Sandbox

**Utiliser [Professionnels du marketing](marketer.md):**

* Identifier les interactions utilisateur qui doivent déclencher des événements
* Implémenter le suivi pour les performances du contenu et l’interaction client
* Prise en charge du test des parcours avec vos fonctionnalités implémentées
* Résolution des problèmes liés à la diffusion ou à la personnalisation des messages

## Restez à jour

Tenez-vous informé des dernières fonctionnalités et modifications techniques de Journey Optimizer :

* **[Notes de mise à jour](../../rn/release-notes.md)** : consultez les nouvelles fonctionnalités, les modifications d’API, les mises à jour de SDK et les correctifs de bugs publiés chaque mois
* **[Mises à jour de la documentation](../../rn/documentation-updates.md)** : suivez les modifications récentes apportées à la documentation technique, y compris les nouveaux guides d’implémentation et exemples de code
* **Notifications de produit** : activez les notifications dans votre profil [Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} pour recevoir des alertes sur :
   * Nouvelles versions de SDK et mises à jour des API
   * Rupture des modifications et des abandons
   * Fenêtres de maintenance affectant les intégrations
   * Mises à jour de sécurité critiques

  Pour activer les notifications, cliquez sur l’icône de votre profil en haut à droite de Adobe Experience Cloud, accédez à **Préférences > Notifications**, puis configurez vos préférences de notification Journey Optimizer.

## Commencer l’implémentation de

Prêt à commencer la création ? Sélectionnez votre première zone d’implémentation dans les sections ci-dessus :

1. **Application mobile ?** Commencer avec [intégration de Mobile SDK](#mobile-integration)
2. **Site Web ?** Commencer par [configuration de Web SDK](#web-implementation)
3. Intégration de l’API **?** à [Utilisation des API](#apis)
4. **Système personnalisé ?** Extraction [actions personnalisées](#custom-actions)

Chaque section comprend des liens vers une documentation technique détaillée, des exemples de code et des tutoriels pour vous guider dans la mise en œuvre.
