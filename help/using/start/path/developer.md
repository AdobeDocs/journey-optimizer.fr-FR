---
title: Prise en main pour les développeurs
description: En tant que développeur, découvrez comment utiliser Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2fid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: e9001ce2-5245-4a8e-8601-dd958009072fid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4c109a6021d46ee7290f09d9333892b42b5af3e2
workflow-type: tm+mt
source-wordcount: 3490
ht-degree: 54%

---

# Commencer en tant que développeurs et développeuses {#get-started-developers}

>[!BEGINSHADEBOX]

**Sur cette page :** Implémentez les SDK, la diffusion en continu d’événements, les points d’entrée d’actions personnalisées et les API qui connectent vos applications à Adobe Journey Optimizer afin que vos parcours puissent s’exécuter sur des données actives.

>[!ENDSHADEBOX]

En tant que **développeur ou développeuse**, vous êtes responsable de la mise en œuvre et de l’intégration d’[!DNL Adobe Journey Optimizer] dans vos applications et systèmes. Vous pouvez commencer à utiliser [!DNL Adobe Journey Optimizer] une fois que l’[administrateur ou administratrice système](administrator.md) et l’[ingénieur ou ingénieure de données](data-engineer.md) vous ont accordé l’accès et ont préparé votre environnement.

>[!NOTE]
>
>**Ordre d’implémentation :** [Administrateur](administrator.md) → [Ingénieur de données](data-engineer.md) → Vous êtes ici : **Développeur** → [Professionnel du marketing](marketer.md)
>
>Assurez-vous que les [schémas de données et événements](data-engineer.md) sont configurés avant de mettre en œuvre vos intégrations mobiles et web.

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

1. **Authentification et sécurité** : toutes les implémentations nécessitent une authentification appropriée. Découvrez comment configurer l’authentification pour les SDK et les API. En savoir plus sur l’[authentification des API](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Configurer les intégrations aux applications mobiles {#mobile-integration}

### Configurer le SDK mobile Adobe Experience Platform

Mobile SDK est un ensemble de bibliothèques que vous incorporez directement dans votre application iOS ou Android. Il agit comme la couche de communication entre votre application et Adobe Experience Platform : il identifie les utilisateurs, collecte des événements comportementaux et fournit des instructions à partir de Journey Optimizer, y compris des notifications push, des messages in-app et du contenu personnalisé. Sans cela, Journey Optimizer n’a aucune visibilité sur ce que font les utilisateurs de votre application et aucun moyen de les contacter.

1. **Installer et configurer le SDK mobile** : consultez la [documentation du SDK mobile Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"} pour commencer à intégrer le SDK.

1. **Créer une propriété mobile** : configurez une propriété mobile dans [!DNL Adobe Experience Platform Data Collection]. Découvrez comment [créer et configurer une propriété mobile](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}.

1. **Configurer les notifications push** :
   * Pour les **applications iOS** : enregistrez votre application auprès de l’APNs (service de notification push Apple). En savoir plus dans la [documentation Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Pour les **applications Android** : configurez Firebase Cloud Messaging pour votre application Android. En savoir plus dans la [documentation Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Tester votre intégration mobile** : utilisez le [workflow de démarrage rapide de l’intégration mobile](../../push/mobile-onboarding-wf.md) pour configurer et tester rapidement votre configuration mobile.

Les étapes détaillées pour configurer les notifications push sont disponibles sur [cette page](../../push/push-configuration.md).

### Implémenter des expériences basées sur du code (SDK mobile)

Les expériences basées sur le code vous permettent de diffuser du contenu personnalisé sur n’importe quelle surface de votre application mobile native (écrans d’intégration, pages de détails du produit, bannières intégrées et indicateurs de fonctionnalité) sans avoir à lancer de nouvelle application. Utilisez Mobile SDK pour récupérer et générer du contenu personnalisé au moment de l’exécution, ce qui permet à votre équipe de contrôler entièrement l’emplacement et la présentation :

* Suivez [ce tutoriel](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"} pour l’implémentation du SDK mobile.
* Examinez les exemples d’implémentation pour [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} et [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}.

## Implémenter les expériences Web {#web-implementation}

### Configurer le SDK Web Adobe Experience Platform

Web SDK (`alloy.js`) est une bibliothèque JavaScript unique qui remplace l’ensemble disparate de balises Adobe distinctes dont votre site pourrait avoir besoin autrement. Il collecte des données comportementales, les diffuse vers Adobe Experience Platform par le biais d’un flux de données que vous configurez et reçoit des instructions de personnalisation en retour, le tout en un seul aller-retour réseau. Une fois en place, Journey Optimizer peut identifier les visiteurs, déclencher des parcours à partir de leurs actions et diffuser immédiatement du contenu personnalisé sur vos pages.

1. **Installer le SDK Web** : suivez le [guide d’implémentation du SDK Web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} pour installer le SDK sur votre site Web.

1. **Configurer les flux de données** : créez et configurez un train de données dans [!DNL Adobe Experience Platform Data Collection] avec Journey Optimizer activé. En savoir plus dans la [documentation sur les trains de données](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target="_blank"}.

1. **Activer les notifications push web** (facultatif) : les notifications push web sont désormais disponibles. Configurez la [propriété pushNotifications](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} dans votre configuration du SDK web et utilisez la [commande sendPushSubscription](https://experienceleague.adobe.com/fr/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} pour enregistrer les abonnements aux notifications push. [En savoir plus sur la configuration de notifications push web](../../push/push-configuration-web.md).

### Implémenter des expériences basées sur du code (SDK Web)

Contrairement aux canaux visuels où les marketeurs contrôlent entièrement la mise en page, les expériences basées sur le code vous donnent une propriété totale sur la manière dont le contenu personnalisé est rendu sur la page. Journey Optimizer renvoie une payload JSON avec les données de personnalisation ; votre code décide où et comment l’afficher. Ce modèle fonctionne pour n’importe quelle surface web (bannières principales, carrousels de recommandation, classements de résultats de recherche, variantes de test A/B) sans avoir besoin d’un éditeur visuel ou d’un workflow de publication de page.

1. **Choisissez votre méthode d’implémentation** : côté client, côté serveur ou hybride. Examinez les [exemples d’implémentation](../../code-based/code-based-implementation-samples.md) pour chaque approche.

1. **Définir des surfaces** : identifiez les emplacements dans votre application où vous souhaitez diffuser du contenu personnalisé. En savoir plus sur la [configuration de surface](../../code-based/code-based-surface.md).

1. **Implémenter le rendu du contenu** : utilisez le SDK Web pour récupérer et appliquer le contenu de personnalisation. Consultez les [tutoriels d’implémentation basée sur du code](../../code-based/code-based-decisioning-implementations.md).

1. **Envoyer des événements d’affichage et d’interaction** : effectuez un suivi du moment où le contenu est affiché et du moment où les utilisateurs et les utilisatrices interagissent avec celui-ci, pour l’analyse et l’optimisation.

Explorez des [exemples d’implémentation sur GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} pour voir les expériences basées sur du code en action.

En savoir plus sur la [prise en main des expériences basées sur du code](../../code-based/get-started-code-based.md).

## Implémenter le streaming d’événements {#event-streaming}

### Envoyer des événements pour déclencher des parcours

Les parcours s’exécutent sur des événements : un utilisateur se connecte, ajoute un article à un panier, effectue un achat et abandonne un formulaire. Votre travail consiste à émettre ces événements à partir de votre application exactement au bon moment. Chaque événement est une payload JSON structurée par XDM envoyée à l’API d’ingestion en flux continu Experience Platform ; Journey Optimizer la récupère en quelques millisecondes et achemine le profil dans n’importe quel parcours correspondant. Le schéma d’événement et la structure de la payload sont définis par votre [ingénieur de données](data-engineer.md) ; assurez-vous de la coordination avec eux avant de commencer le codage.

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

Lorsqu’un parcours atteint une étape d’action personnalisée, Journey Optimizer effectue un appel HTTP sortant vers une URL que vous fournissez : votre serveur principal, un CRM, une plateforme de fidélité, n’importe quel point d’entrée REST. Votre tâche consiste à créer et exposer ce point d’entrée : définissez le contrat de requête (forme de payload, méthode d’authentification, format de réponse), implémentez la logique commerciale sous-jacente et assurez-vous qu’il peut gérer le volume d’appels généré par Journey Optimizer. Votre [administrateur](administrator.md) enregistre ensuite le point d’entrée dans Journey Optimizer afin que les marketeurs puissent l’utiliser comme une étape dans leurs parcours.

1. **Créer votre point d’entrée d’API** : créez des points d’entrée d’API RESTful que Journey Optimizer appellera lors de l’exécution du parcours. Votre point d’entrée doit :
   * Accepter des payloads JSON
   * Authentifier les requêtes (OAuth, clé d’API ou JWT)
   * Traiter les requêtes dans des délais appropriés
   * Renvoyer les réponses au format attendu

1. **Comprendre les fonctionnalités des actions personnalisées** : les actions personnalisées peuvent se connecter à des systèmes tiers tels qu’Epsilon, Slack, Firebase, ou à vos propres services. En savoir plus sur les [actions personnalisées](../../action/action.md).

1. **Utiliser les configurations d’actions** : votre [administrateur ou administratrice](administrator.md) ou votre [ingénieur ou ingénieure de données](data-engineer.md) configure l’action personnalisée dans Journey Optimizer en définissant l’URL du point d’entrée d’API, la méthode d’authentification et les paramètres. Vous devez leur fournir les spécifications de votre API. Découvrez la [configuration des actions personnalisées](../../action/about-custom-action-configuration.md). Vous pouvez définir une **payload de réponse d’erreur** facultative pour une logique de repli plus avancée dans les branches Délai d’expiration et Erreur.

1. **Renvoyer des données activables** : concevez votre API afin qu’elle renvoie des données pouvant être utilisées dans les étapes de parcours postérieures. Découvrez les [réponses aux actions](../../action/action-response.md).

1. **Surveiller l’intégrité des actions personnalisées** : utilisez le tableau de bord de surveillance des actions personnalisées pour suivre les appels réussis, les erreurs, le débit, les temps de réponse et les temps d’attente dans la file d’attente. En savoir plus sur le [reporting des actions personnalisées](../../action/reporting.md)

1. **Implémenter une limitation de débit** : assurez-vous que vos points d’entrée peuvent gérer le volume attendu. Journey Optimizer applique une limite de 5 000 appels/seconde, mais votre système doit pouvoir la supporter. Découvrez le [capping et la limitation](../../configuration/external-systems.md).

**Exemple de cas d’utilisation** : [écriture d’événements de parcours dans Experience Platform](../../building-journeys/custom-action-aep.md) à l’aide d’actions personnalisées.

## Utiliser des API Journey Optimizer {#apis}

Tout ne doit pas nécessairement se produire via l’interface utilisateur de Journey Optimizer. Parfois, vous devez déclencher une campagne à partir de votre propre serveur principal, supprimer une adresse e-mail après une demande d’accès à des informations personnelles ou synchroniser les modèles de contenu à partir d’un CMS externe. Les API REST Journey Optimizer vous donnent un accès programmatique aux principales fonctionnalités de la plateforme. Tous les appels utilisent l’authentification de serveur à serveur OAuth ; l’ancienne méthode JWT est obsolète.

1. **Comprendre les fonctionnalités des API** : les API Journey Optimizer vous permettent de créer, lire, mettre à jour et supprimer diverses ressources par programmation. Découvrez les [API Adobe Journey Optimizer](../../configuration/ajo-apis.md).

1. **Authentification** : suivez [ce tutoriel](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} pour configurer l’authentification des API à l’aide d’Adobe Developer Console.

1. **Explorer les références d’API** : parcourez la documentation complète des API et essayez les API directement dans la [référence des API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

1. **Campagnes déclenchées par API** : créez des messages transactionnels avec des campagnes déclenchées par API. Pour les scénarios à volume élevé (jusqu’à 5 000 TPS), explorez le [mode à débit élevé](../../campaigns/api-triggered-high-throughput.md) (nécessite une licence de module complémentaire).

1. **API de gestion des décisions** : utilisez des API spécialisées pour la gestion des offres et la prise de décisions. Pour plus d’informations, consultez le [guide des API de gestion des décisions](../../offers/api-reference/getting-started.md).

1. **API de migration Prise de décision** : migrez par programmation les entités de Gestion des décisions vers Prise de décision avec des portées flexibles, une validation automatique et une prise en charge de la restauration. Pour plus d’informations, consultez le [guide des API Gestion des décisions](../../experience-decisioning/decisioning-migration-api.md).

1. **Webhooks SMS** : configurez les webhooks entrants pour collecter les messages reçus et les webhooks de retour afin de recevoir les accusés de réception de diffusion et les mises à jour de statut. [En savoir plus](../../mobile/mobile-webhook.md).

## Test et débogage {#testing}

Avant la mise en œuvre, vous devez vous assurer que les événements se déclenchent au bon moment, que les parcours se déclenchent comme prévu, que les actions personnalisées se comportent avec une charge réaliste et que le contenu personnalisé s’affiche correctement. Cette section présente les outils et les techniques permettant de détecter les problèmes dès le début, depuis la journalisation de SDK de bas niveau jusqu’aux exécutions de test de parcours de bout en bout avec des profils réels.

1. **Implémentation de Debug SDK** : utilisez Adobe Experience Platform Assurance pour inspecter les événements SDK, valider la collecte de données et résoudre les problèmes d’intégration au fur et à mesure qu’ils se produisent. [En savoir plus sur Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=fr){target="_blank"}.

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

Une fois vos SDK, événements et API principaux en place, ces rubriques vous aident à aller plus loin : enrichir les données de parcours au moment de l’exécution sans surcharger le profil, gérer les signaux de consentement afin que les désinscriptions se propagent à chaque intégration et ajuster votre implémentation pour le débit et la fiabilité qu’exige l’échelle de production.

### Utilisation des données contextuelles et enrichissement

Les parcours ont souvent besoin de plus de données que ce qui arrive dans l’événement déclencheur : un nom de produit, un niveau de fidélité, une liste d’éléments de ligne de commande. Plutôt que de précharger tout cela dans chaque profil, l’enrichissement contextuel permet à votre parcours de le rechercher au moment de l’exécution à partir des jeux de données AEP ou de le transférer à partir d’une réponse d’action personnalisée. Vos messages et conditions de branche peuvent alors référencer ces données sans qu’elles ne soient jamais stockées de manière permanente sur le profil.

* **Effectuer une itération de tableaux** : utilisez la syntaxe Handlebars pour afficher dans les messages des listes dynamiques à partir d’événements, de réponses d’actions personnalisées et de recherches dans des jeux de données. Découvrez [l’itération de données contextuelles](../../personalization/iterate-contextual-data.md).
* **Recherche dans les jeux de données** : implémentez des recherches dans les jeux de données pour enrichir les données de parcours à partir de jeux de données Adobe Experience Platform. Collaborez avec votre ingénieur ou ingénieure de données pour la configuration. Découvrez la [recherche dans les jeux de données](../../building-journeys/dataset-lookup.md).

### Appliquer le consentement et la gouvernance

Journey Optimizer applique les politiques de gouvernance des données et de consentement au niveau de la plateforme, mais votre intégration doit également les respecter. Lorsqu’un client se désinscrit des communications marketing ou lorsqu’un libellé d’utilisation des données limite l’utilisation d’un champ, ces règles doivent se propager à travers vos actions personnalisées et vos recherches de jeux de données, et pas seulement bloquer les actions dans l’interface utilisateur.

* **Gouvernance des données** : appliquez des politiques d’utilisation des données aux actions personnalisées. En savoir plus sur la [gouvernance des données](../../action/action-privacy.md).
* **Gestion du consentement** : gérez les préférences de consentement des clientes et des clients dans vos implémentations. En savoir plus sur le [consentement](../../action/consent.md).

### Optimisation et bonnes pratiques

Les implémentations de Journey Optimizer de production gèrent régulièrement des millions d’événements et des milliers d’exécutions de parcours par seconde. Ces ressources vous aident à affiner votre intégration pour cette échelle : en comprenant les limites de taux avant de les atteindre, en évitant les pièges de conception de parcours courants qui font chuter silencieusement les profils et en créant une gestion des erreurs qui se dégrade de manière élégante plutôt que d’échouer de manière opaque.

* **Capping et limitation** : prenez connaissance des limites de débit et implémentez une limitation appropriée. Découvrez les [systèmes externes](../../configuration/external-systems.md).
* **Optimisation des parcours** : suivez les bonnes pratiques pour l’[optimisation des parcours](../../building-journeys/optimize.md).
* **Gestion des erreurs** : implémentez une gestion des erreurs robuste. Consultez les [codes d’erreur](../../building-journeys/error-codes-reference.md) et les [guides de résolution des problèmes](../../building-journeys/troubleshooting.md).

## Appel des API REST Journey Optimizer {#rest-apis}

Outre l’implémentation de SDK et de la diffusion d’événements en continu, vous pouvez également piloter Journey Optimizer par programmation à partir de vos propres systèmes. La référence complète de l’API, les spécifications OpenAPI et les exemples de code se trouvent sur le portail de développement [](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

>[!NOTE]
>
>Toutes les intégrations doivent utiliser l’authentification de serveur à serveur OAuth ; la méthode JWT est obsolète. [Configurer l’authentification](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### Exécuter des campagnes déclenchées par API {#api-triggered}

Déclenchez des messages transactionnels ou marketing à partir d’un système externe à l’aide de l’API REST d’exécution de message interactif. Avant d’appeler le point d’entrée :

* La campagne doit être **activée** avant que le point d’entrée accepte les appels.
* Les appels ont un **délai d’expiration de 60 secondes** ; les reprises internes gèrent les délais inattendus.
* Si les dates de début/fin de campagne sont configurées, les appels API en dehors de ces dates échoueront.
* Pour créer votre payload, récupérez l’exemple de requête cURL généré à partir de la section **requête cURL** de votre campagne active dans l’interface utilisateur de Journey Optimizer ; il inclut toutes les variables de personnalisation pour cette campagne.
* Les campagnes standard et [à débit élevé](../../campaigns/api-triggered-high-throughput.md) utilisent différents points d’entrée.

[Référence d’API](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [Exemples de code](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [Utiliser des campagnes déclenchées par API](../../campaigns/api-triggered-campaigns.md)

### Plafonnement et limitation des points d’entrée externes {#capping-throttling}

Lorsque des parcours appellent des systèmes externes par le biais d’actions personnalisées ou de sources de données, les API de plafonnement et de limitation protègent ces systèmes contre la surcharge. La limitation rejette les appels qui dépassent la limite configurée ; la limitation les met en file d’attente pendant 6 heures au maximum (sandbox de production, actions personnalisées uniquement).

[Référence de l’API de plafonnement](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [Utiliser l’API de plafonnement](../../configuration/capping.md) · [Utiliser l’API de limitation](../../configuration/throttling.md)

### Plus d’API REST {#more-rest-apis}

Au-delà de la messagerie et de la limitation, Journey Optimizer expose des points d’entrée REST pour la gestion de suppression, le modèle de contenu, la récupération des campagnes, la relecture et l’exécution orchestrée des campagnes. Utilisez-les lorsque vous devez automatiser des opérations qui nécessiteraient autrement des étapes manuelles dans l’interface utilisateur, par exemple la suppression en masse d’adresses après une extraction de données ou la synchronisation de modèles à partir d’un pipeline de contenu externe.

| Ce que vous devez faire | Référence d’API |
| ------------------- | ------------- |
| Exclure par programmation des adresses e-mail ou domaines de l’envoi | [API de suppression](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [Gérer la liste de suppression](../../configuration/manage-suppression-list.md) |
| Récupérer des métadonnées de parcours pour un audit ou une synchronisation externe | [API ](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| Créer et gérer des modèles et des fragments de contenu à partir d’un pipeline externe | [API de contenu](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [modèles](../../content-management/content-templates.md) · [fragments](../../content-management/fragments.md) |
| Récupération et filtrage des campagnes d’action | [API Campaign](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| Prévisualiser des campagnes et envoyer des BAT par programmation | [API Simulations](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |

>[!NOTE]
>
>L’API Simulations est disponible pour les campagnes déclenchées par l’API et les campagnes d’action (planifiées). Elle n’est **pas prise en charge pour les campagnes orchestrées** : utilisez plutôt le workflow d’aperçu et de BAT dans l’interface utilisateur des campagnes orchestrées.

| Valider les jeux de données et déclencher l’exécution de campagnes orchestrées | [Validation des jeux de données](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [Déclencheur](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [Activer les jeux de données](../../orchestrated/manual-schema.md) |

## Ressources supplémentaires {#additional-resources}

* **Developer Console** : accédez à [Adobe Developer Console](https://developer.adobe.com){target="_blank"} pour créer des intégrations et gérer les informations d’identification des API.
* **Exemple de code** : explorez les [exemples d’implémentation sur GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Tutoriels vidéo** : apprenez grâce à des tutoriels pratiques sur [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr){target="_blank"}.
* **Communauté de développement** : entrez en contact avec d’autres développeurs et développeuses et obtenez de l’aide sur les forums de la communauté Adobe.

## Collaboration entre les rôles {#next-steps}

Votre travail d’implémentation est lié aux autres membres de l’équipe :

>[!BEGINTABS]

>[!TAB Collaborer avec les ingénieurs et ingénieures de données]

Collaborez avec des [ingénieurs de données](data-engineer.md) sur les configurations de données et d’événements. Chaque parcours qui réagit au comportement de l’utilisateur dépend des événements que vous envoyez : l’ingénieur de données définit les schémas et vous implémentez le code qui les produit.

* Obtenez les [schémas XDM](../../data/get-started-schemas.md) et les structures d’événement que vous devez implémenter
* Identifiez les événements à envoyer et le format de payload requis. Voir [ Utilisation d’événements de parcours ](../../event/about-events.md)
* Confirmez les champs obligatoires ou facultatifs dans chaque payload d’événement et ce qui se passe dans les parcours lorsque les champs attendus sont manquants ou incorrects (voir [Exigences de schéma](../../event/experience-event-schema.md#schema-requirements)).
* Tester la diffusion d’événements et l’ingestion de données ensemble à l’aide d’[](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=fr){target="_blank"}

>[!TAB Collaborer avec les administrateurs et administratrices]

Collaborez avec les [administrateurs](administrator.md) sur les configurations d’accès et de canal. Parcours ne peut atteindre les utilisateurs et utilisatrices que par le biais des canaux configurés par l’administrateur ou l’administratrice. Coordonnez-les suffisamment tôt pour que votre travail SDK et leur configuration restent synchronisés.

* Fournissez les spécifications d’API pour les [actions personnalisées](../../action/about-custom-action-configuration.md) qu’ils configureront dans Journey Optimizer
* Demandez les autorisations nécessaires et les informations d’identification API via [](https://developer.adobe.com){target="_blank"}
* Coordonnez-vous sur les exigences de configuration des canaux : certificats push pour les points d’entrée [](../../push/push-configuration.md) et Android, [Web push](../../push/push-configuration-web.md), [SMS webhook](../../mobile/mobile-webhook.md).
* Alignez-vous sur la stratégie de sandbox et les environnements de test avant d’exécuter le mode test de parcours [](../../building-journeys/testing-the-journey.md)

>[!TAB Collaborer avec les responsables marketing]

Collaborez avec des [spécialistes marketing](marketer.md) sur la conception et les tests de parcours. Les marketeurs créent des parcours et du contenu qui dépendent entièrement des événements envoyés et des surfaces exposées. Plus vous vous alignez, plus les parcours sont activés rapidement.

* Examinez ensemble les conceptions de parcours dans [Journey Optimizer](../../building-journeys/journey.md) pour identifier les interactions utilisateur qui doivent déclencher des événements et les surfaces qui doivent être personnalisées
* Implémentez le suivi afin que les marketeurs puissent mesurer [les performances du contenu et l’interaction client](../../reports/report-gs-cja.md)
* Exécutez le mode test de parcours [](../../building-journeys/testing-the-journey.md) ensemble à l’aide des profils de test pour valider le flux complet de bout en bout.
* Résoudre les problèmes liés à la diffusion des messages, au rendu de la personnalisation ou aux réponses [action personnalisée](../../action/action.md)

>[!ENDTABS]

## Commencer l’implémentation

Vous souhaitez commencer à créer ? Sélectionnez votre premier domaine d’implémentation dans les sections ci-dessus :

1. **Application mobile ?** Commencez par l’[Intégration du SDK mobile](#mobile-integration).
2. **Site web ?** Commencez par la [configuration du SDK web](#web-implementation).
3. **Intégration d’API ?** Passez directement à [Utiliser des API](#apis).
4. **Système personnalisé ?** Consultez les [actions personnalisées](#custom-actions).

Chaque section comprend des liens vers une documentation technique détaillée, des exemples de code et des tutoriels pour vous guider dans votre implémentation.

## Autres guides de rôle {#other-role-guides}

| Rôle | Guide |
|------|-------|
| Administrateur | [Prise en main pour les administrateurs](administrator.md) |
| Ingénieur de données | [Prise en main pour les ingénieurs de données](data-engineer.md) |
| Développeur | [Prise en main pour les développeurs](developer.md) |
| Spécialiste marketing | [Commencer pour les spécialistes du marketing](marketer.md) |

Retour à [Présentation des rôles et des responsabilités](../quick-start.md) · Retour à [Commencer](../../../rp_landing_pages/get-started-landing-page.md)
