---
title: Prise en main pour les développeurs
description: En tant que développeur, découvrez comment utiliser Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: fd10a600cb54b8c35e2d195be7379b0dd120b6a7
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 93%

---

# Prise en main pour les développeurs {#get-started-developers}

En tant que **développeur ou développeuse**, vous êtes responsable de la mise en œuvre et de l’intégration d’[!DNL Adobe Journey Optimizer] dans vos applications et systèmes. Vous pouvez commencer à utiliser [!DNL Adobe Journey Optimizer] une fois que l’[administrateur ou administratrice système](administrator.md) et l’[ingénieur ou ingénieure de données](data-engineer.md) vous ont accordé l’accès et ont préparé votre environnement.

## Votre rôle dans l’écosystème Journey Optimizer

Tandis les autres membres de l’équipe configurent Journey Optimizer par le biais de l’interface d’utilisation, vous pouvez vous concentrer sur les éléments suivants :

* **Implémentation de SDK** dans des applications mobiles et web
* **Envoi d’événements** à partir de vos applications pour déclencher des parcours
* **Création de points d’entrée d’API** que Journey Optimizer peut appeler via des actions personnalisées
* **Intégration** de Journey Optimizer à vos systèmes et infrastructures existants
* **Test et débogage** de vos implémentations

Votre [ingénieur ou ingénieure de données](data-engineer.md) s’occupe des schémas de données, des configurations d’événement et des sources de données. Votre [administrateur ou administratrice](administrator.md) configure les autorisations et les configurations de canaux. Les [responsables marketing](marketer.md) conçoivent les parcours et le contenu utilisé dans vos implémentations.

Ce guide décrit les étapes techniques de base de mise en œuvre pour commencer à utiliser Journey Optimizer. Que vous créiez des applications mobiles, des expériences web ou des intégrations d’API, suivez les sections ci-dessous pour configurer votre implémentation.

## Conditions préalables {#prerequisites}

Avant de commencer votre implémentation, vérifiez que vous disposez des éléments suivants :

| Catégorie | Conditions requises |
|----------|-------------|
| **Compétences techniques** | * Expérience avec JavaScript (pour le SDK Web) ou Swift/Kotlin (pour le SDK mobile)<br>* Maîtrise des API RESTful et de JSON<br>* Connaissance de la programmation asynchrone et des architectures basées sur les événements<br>* Connaissance de l’architecture d’applications de votre organisation |
| **Accès et outils** | * Accès à [Adobe Developer Console](https://developer.adobe.com){target="_blank"} pour les informations d’identification d’API<br>* Environnement de développement avec accès à la base de code de votre application<br>* Outils de test tels que Postman pour le test des API<br>* Outils de développement de navigateur ou outils de débogage pour mobile |
| **Éléments provenant des autres membres de l’équipe** | * Accès à l’environnement accordé par votre [administrateur ou administratrice](administrator.md)<br>* Schémas XDM et définitions d’événement fournis par votre [ingénieur ou ingénieure de données](data-engineer.md)<br>* Exigences et cas pratiques fournis par vos [responsables marketing](marketer.md) |

## Comprendre les bases techniques {#technical-foundation}

Avant d’aborder plus en détail l’implémentation, familiarisez-vous avec les concepts techniques de base :

1. **Intégration d’Adobe Experience Platform** : Journey Optimizer est intégré nativement dans Adobe Experience Platform. Comprendre l’architecture sous-jacente vous aidera à créer des implémentations plus efficaces. En savoir plus sur [le fonctionnement de Journey Optimizer](../understanding-ajo.md).

1. **Modèles de données XDM** : Journey Optimizer utilise le modèle de données d’expérience (XDM) pour structurer les données d’événement et de profil. En tant que développeur ou développeuse, vous devez comprendre comment envoyer des données conformes aux schémas configurés par votre [ingénieur ou ingénieure de données](data-engineer.md). Découvrez les [schémas XDM](../../data/get-started-schemas.md).

1. **Authentification et sécurité** : toutes les implémentations nécessitent une authentification appropriée. Découvrez comment configurer l’authentification pour les SDK et les API. En savoir plus sur l’[authentification des API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configurer les intégrations aux applications mobiles {#mobile-integration}

### Configurer le SDK mobile Adobe Experience Platform

Pour activer les notifications push, les messages in-app et d’autres fonctionnalités mobiles, intégrez le SDK mobile Adobe Experience Platform à vos applications mobiles.

1. **Installer et configurer le SDK mobile** : consultez la [documentation du SDK mobile Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} pour commencer à intégrer le SDK.

1. **Créer une propriété mobile** : configurez une propriété mobile dans [!DNL Adobe Experience Platform Data Collection]. Découvrez comment [créer et configurer une propriété mobile](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurer les notifications push** :
   * Pour les **applications iOS** : enregistrez votre application auprès de l’APNs (service de notification push Apple). En savoir plus dans la [documentation Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Pour les **applications Android** : configurez Firebase Cloud Messaging pour votre application Android. En savoir plus dans la [documentation Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Tester votre intégration mobile** : utilisez le [workflow de démarrage rapide de l’intégration mobile](../../push/mobile-onboarding-wf.md) pour configurer et tester rapidement votre configuration mobile.

Les étapes détaillées pour configurer les notifications push sont disponibles sur [cette page](../../push/push-configuration.md).

### Implémenter des expériences basées sur du code (SDK mobile)

Pour la personnalisation d’applications mobiles natives à l’aide d’expériences basées sur du code :

* Suivez [ce tutoriel](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} pour l’implémentation du SDK mobile.
* Examinez les exemples d’implémentation pour [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} et [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}.

## Implémenter les expériences Web {#web-implementation}

### Configurer le SDK Web Adobe Experience Platform

Pour les implémentations web, le SDK Web est votre principal point d’intégration :

1. **Installer le SDK Web** : suivez le [guide d’implémentation du SDK Web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} pour installer le SDK sur votre site Web.

1. **Configurer les flux de données** : créez et configurez un train de données dans [!DNL Adobe Experience Platform Data Collection] avec Journey Optimizer activé. En savoir plus dans la [documentation sur les trains de données](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}.

1. **Activer les notifications push web** (facultatif) : les notifications push web sont désormais disponibles pour tous les utilisateurs. Configurez la propriété [pushNotifications](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} dans votre configuration Web SDK et utilisez la commande [sendPushSubscription](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} pour enregistrer les abonnements push. [En savoir plus sur la configuration des notifications push web](../../push/push-configuration-web.md).

### Implémenter des expériences basées sur du code (SDK Web)

Les expériences basées sur du code vous permettent de personnaliser n’importe quel point de contact numérique :

1. **Choisissez votre méthode d’implémentation** : côté client, côté serveur ou hybride. Examinez les [exemples d’implémentation](../../code-based/code-based-implementation-samples.md) pour chaque approche.

1. **Définir des surfaces** : identifiez les emplacements dans votre application où vous souhaitez diffuser du contenu personnalisé. En savoir plus sur la [configuration de surface](../../code-based/code-based-surface.md).

1. **Implémenter le rendu du contenu** : utilisez le SDK Web pour récupérer et appliquer le contenu de personnalisation. Consultez les [tutoriels d’implémentation basée sur du code](../../code-based/code-based-decisioning-implementations.md).

1. **Envoyer des événements d’affichage et d’interaction** : effectuez un suivi du moment où le contenu est affiché et du moment où les utilisateurs et les utilisatrices interagissent avec celui-ci, pour l’analyse et l’optimisation.

Explorez des [exemples d’implémentation sur GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} pour voir les expériences basées sur du code en action.

En savoir plus sur la [prise en main des expériences basées sur du code](../../code-based/get-started-code-based.md).

## Implémenter le streaming d’événements {#event-streaming}

### Envoyer des événements pour déclencher des parcours

En tant que développeur ou développeuse, vous implémentez le code pour envoyer des événements qui déclenchent des parcours. Votre [ingénieur ou ingénieure de données](data-engineer.md) configure les schémas et les définitions d’événement dans Journey Optimizer.

1. **Connaître la payload d’événement** : contactez l’ingénieur ou l’ingénieure de données pour obtenir le schéma d’événement et la structure de payload requise. La payload doit être conforme au schéma XDM configuré. Découvrez les [exigences relatives au schéma d’événement](../../event/experience-event-schema.md).

1. **Implémenter le streaming d’événements** : envoyez des événements à Adobe Experience Platform à l’aide des [API d’ingestion en streaming](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=fr){target="_blank"}. Découvrez les [étapes pour envoyer des événements](../../event/additional-steps-to-send-events-to-journey.md).

1. **Gérer les types d’événement** :
   * **Événements unitaires** : implémentez l’envoi d’événements pour des actions spécifiques à une personne (par exemple, clic sur un bouton, achat complété).
   * **Événements métier** : envoyez des événements métier (par exemple, des mises à jour d’inventaire, des modifications de prix).

1. **Tester la diffusion d’événement** : vérifiez que les événements sont correctement reçus et déclenchez les parcours comme prévu. Découvrez la [résolution des problèmes liés aux événements](../../building-journeys/troubleshooting-inbound.md).

**Exemple d’implémentation** pour envoyer un événement via une API :

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

En savoir plus sur [l’utilisation d’événements de parcours](../../event/about-events.md).

## Développer des points d’entrée d’actions personnalisées {#custom-actions}

Les actions personnalisées permettent aux parcours d’appeler vos API. En tant que développeur ou développeuse, vous allez créer les points d’entrée d’API appelés par les actions personnalisées :

1. **Créer votre point d’entrée d’API** : créez des points d’entrée d’API RESTful que Journey Optimizer appellera lors de l’exécution du parcours. Votre point d’entrée doit :
   * Accepter des payloads JSON
   * Authentifier les requêtes (OAuth, clé d’API ou JWT)
   * Traiter les requêtes dans des délais appropriés
   * Renvoyer les réponses au format attendu

1. **Comprendre les fonctionnalités des actions personnalisées** : les actions personnalisées peuvent se connecter à des systèmes tiers tels qu’Epsilon, Slack, Firebase, ou à vos propres services. En savoir plus sur les [actions personnalisées](../../action/action.md).

1. **Utiliser les configurations d’actions** : votre [administrateur ou administratrice](administrator.md) ou votre [ingénieur ou ingénieure de données](data-engineer.md) configure l’action personnalisée dans Journey Optimizer en définissant l’URL du point d’entrée d’API, la méthode d’authentification et les paramètres. Vous devez leur fournir les spécifications de votre API. En savoir plus sur la [configuration d’une action personnalisée](../../action/about-custom-action-configuration.md). Vous pouvez définir une **payload de réponse d’erreur** facultative pour une logique de secours plus riche dans les branches Temporisation/Erreur.

1. **Renvoyer des données activables** : concevez votre API afin qu’elle renvoie des données pouvant être utilisées dans les étapes de parcours postérieures. Découvrez les [réponses aux actions](../../action/action-response.md).

1. **Surveiller l’intégrité des actions personnalisées** : utilisez le tableau de bord de surveillance des actions personnalisées pour suivre les appels réussis, les erreurs, le débit, les temps de réponse et les temps d’attente dans la file d’attente. En savoir plus sur les [rapports d’action personnalisés](../../action/reporting.md).

1. **Implémenter une limitation de débit** : assurez-vous que vos points d’entrée peuvent gérer le volume attendu. Journey Optimizer applique une limite de 5 000 appels/seconde, mais votre système doit pouvoir la supporter. Découvrez le [capping et la limitation](../../configuration/external-systems.md).

**Exemple de cas d’utilisation** : [écriture d’événements de parcours dans Experience Platform](../../building-journeys/custom-action-aep.md) à l’aide d’actions personnalisées.

## Utiliser des API Journey Optimizer {#apis}

Journey Optimizer fournit des API REST complètes pour un accès par programmation :

1. **Comprendre les fonctionnalités des API** : les API Journey Optimizer vous permettent de créer, lire, mettre à jour et supprimer diverses ressources par programmation. Découvrez les [API Adobe Journey Optimizer](../../configuration/ajo-apis.md).

1. **Authentification** : suivez [ce tutoriel](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} pour configurer l’authentification des API à l’aide d’Adobe Developer Console.

1. **Explorer les références d’API** : parcourez la documentation complète des API et essayez les API directement dans la [référence des API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campagnes déclenchées par API** : créez des messages transactionnels avec des campagnes déclenchées par API. Pour les scénarios à volume élevé (jusqu’à 5 000 TPS), explorez le [mode à débit élevé](../../campaigns/api-triggered-high-throughput.md) (nécessite une licence de module complémentaire).

1. **API de gestion des décisions** : utilisez des API spécialisées pour la gestion des offres et la prise de décisions. Pour plus d’informations, consultez le [guide des API de gestion des décisions](../../offers/api-reference/getting-started.md).

1. **API de migration Decisioning** : migrez par programmation les entités de gestion des décisions vers Decisioning avec des portées flexibles, une validation automatisée et une prise en charge de la restauration. Pour en savoir plus, consultez le [guide de l’API de migration Decisioning](../../experience-decisioning/decisioning-migration-api.md).

1. **Webhooks SMS** : configurez les webhooks entrants pour capturer les messages entrants et les webhooks de retour afin de recevoir les accusés de réception de diffusion et les mises à jour de statut. [En savoir plus](../../sms/sms-webhook.md).

## Test et débogage {#testing}

1. **Débogage de l’implémentation du SDK** : utilisez Adobe Experience Platform Assurance pour inspecter les événements du SDK, valider la collecte des données et résoudre les problèmes d’intégration en temps réel. [En savoir plus sur Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=fr){target="_blank"}.

1. **Tester la diffusion des événements** : vérifiez que les événements de votre application sont correctement reçus par Adobe Experience Platform et déclenchez les parcours comme prévu. Surveillez l’ingestion des événements et validez la structure de la payload.

1. **Valider les intégrations d’API** : testez vos points d’entrée d’actions personnalisées pour vous assurer qu’ils gèrent correctement les requêtes Journey Optimizer, répondent dans les limites des délais d’expiration et renvoient les formats de données attendus.

1. **Utiliser le mode test avec des profils de test** : contactez votre [ingénieur ou ingénieure de données](data-engineer.md) pour obtenir l’accès aux profils de test, puis validez votre implémentation à l’aide du mode de test de parcours. Découvrez comment [tester des parcours](../../building-journeys/testing-the-journey.md).

1. **Surveiller les journaux du SDK** : activez la journalisation du débogage dans votre implémentation du SDK pour résoudre les problèmes lors du développement :
   * **SDK mobile** : activez la journalisation pour afficher les événements du SDK et les appels d’API.
   * **SDK Web** : utilisez la console du navigateur pour surveiller l’activité du SDK.

1. **Vérifier la configuration du train de données** : vérifiez que votre train de données est correctement configuré pour envoyer des données à Journey Optimizer. Vérifiez que les événements sont acheminés via le train de données vers les destinations correctes.

1. **Interroger les données de parcours pour analyse** : utilisez des requêtes SQL vers le lac de données pour analyser les événements d’étapes de parcours, résoudre les problèmes, et surveiller les performances des actions personnalisées. Explorez les [exemples de requêtes pour l’analyse de parcours](../../reports/query-examples.md), notamment :
   * Suivi des entrées et des sorties des profils et raisons des rejets
   * Mesures de performances des actions personnalisées (latence, débit, erreurs)
   * Diffusion des événements et modèles d’erreurs
   * États des instances de parcours

## Rubriques de développement avancées {#advanced-topics}

### Utilisation des données contextuelles et enrichissement

* **Effectuer une itération de tableaux** : utilisez la syntaxe Handlebars pour afficher dans les messages des listes dynamiques à partir d’événements, de réponses d’actions personnalisées et de recherches dans des jeux de données. Découvrez [l’itération de données contextuelles](../../personalization/iterate-contextual-data.md).
* **Recherche dans les jeux de données** : implémentez des recherches dans les jeux de données pour enrichir les données de parcours à partir de jeux de données Adobe Experience Platform. Collaborez avec votre ingénieur ou ingénieure de données pour la configuration. Découvrez la [recherche dans les jeux de données](../../building-journeys/dataset-lookup.md).

### Appliquer le consentement et la gouvernance

Implémentez des politiques de gouvernance des données et de consentement dans vos intégrations :

* **Gouvernance des données** : appliquez des politiques d’utilisation des données aux actions personnalisées. En savoir plus sur la [gouvernance des données](../../action/action-privacy.md).
* **Gestion du consentement** : gérez les préférences de consentement des clientes et des clients dans vos implémentations. En savoir plus sur le [consentement](../../action/consent.md).

### Optimisation et bonnes pratiques

* **Capping et limitation** : prenez connaissance des limites de débit et implémentez une limitation appropriée. Découvrez les [systèmes externes](../../configuration/external-systems.md).
* **Optimisation des parcours** : suivez les bonnes pratiques pour l’[optimisation des parcours](../../building-journeys/optimize.md).
* **Gestion des erreurs** : implémentez une gestion des erreurs robuste. Consultez les [codes d’erreur](../../building-journeys/error-codes-reference.md) et les [guides de résolution des problèmes](../../building-journeys/troubleshooting.md).

## Ressources supplémentaires {#additional-resources}

* **Developer Console** : accédez à [Adobe Developer Console](https://developer.adobe.com){target="_blank"} pour créer des intégrations et gérer les informations d’identification des API.
* **Exemple de code** : explorez les [exemples d’implémentation sur GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Tutoriels vidéo** : apprenez grâce à des tutoriels pratiques sur [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr){target="_blank"}.
* **Communauté de développement** : entrez en contact avec d’autres développeurs et développeuses et obtenez de l’aide sur les forums de la communauté Adobe.

## Collaboration entre les rôles {#next-steps}

Votre travail d’implémentation est lié aux autres membres de l’équipe :

>[!BEGINTABS]

>[!TAB Collaborer avec les ingénieurs et ingénieures de données]

Collaborez avec les [ingénieurs et ingénieures de données](data-engineer.md) sur les configurations de données et d’événements :

* Obtenez les schémas XDM et les structures d’événement que vous devez implémenter.
* Identifiez les événements que vous devez envoyer et leur format de payload requis.
* Alignez-vous sur les exigences en matière de collecte de données et les normes de qualité des données.
* Testez conjointement la diffusion des événements et l’ingestion des données.

>[!TAB Collaborer avec les administrateurs et administratrices]

Collaborez avec les [administrateurs et les administratrices](administrator.md) sur les accès et les configurations :

* Fournissez les spécifications des API pour les actions personnalisées qu’ils vont configurer.
* Demandez les autorisations nécessaires et les informations d’identification des API.
* Coordonnez-vous sur les exigences de configuration des canaux (par exemple, les certificats push).
* Alignez les environnements de test et la stratégie de sandbox.

>[!TAB Collaborer avec les responsables marketing]

Collaborez avec les [responsables marketing](marketer.md) sur les exigences et les tests des parcours :

* Identifiez les interactions utilisateur qui doivent déclencher des événements.
* Implémenter le suivi des performances du contenu et de l’interaction client
* Tester les parcours avec vos fonctionnalités implémentées
* Résolvez les problèmes liés à la diffusion ou à la personnalisation des messages.

>[!ENDTABS]

## Commencer l’implémentation

Vous souhaitez commencer à créer ? Sélectionnez votre premier domaine d’implémentation dans les sections ci-dessus :

1. **Application mobile ?** Commencez par l’[Intégration du SDK mobile](#mobile-integration).
2. **Site web ?** Commencez par la [Configuration du SDK Web](#web-implementation).
3. **Intégration d’API ?** Passez directement à [Utiliser des API](#apis).
4. **Système personnalisé ?** Consultez les [Actions personnalisées](#custom-actions).

Chaque section comprend des liens vers une documentation technique détaillée, des exemples de code et des tutoriels pour vous guider dans votre implémentation.
