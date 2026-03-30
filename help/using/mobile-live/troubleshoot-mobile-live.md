---
solution: Journey Optimizer
product: journey optimizer
title: Résolution des problèmes liés aux activités en direct
description: Découvrez comment résoudre les problèmes liés aux activités en direct dans Journey Optimizer pour les cas d’utilisation unitaires et de diffusion, y compris les problèmes de jeton de profil, la configuration de la campagne et les échecs de diffusion
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
source-git-commit: 016d905840a3ccc05ca1d2a934130b53c1108e7c
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---

# Résolution des problèmes liés aux activités en direct {#troubleshoot-mobile-live}

Les activités en direct dans Adobe Journey Optimizer permettent des mises à jour dynamiques en temps réel sur les écrans de verrouillage iOS et les îles dynamiques. Ils ne peuvent être déclenchés et gérés que par le biais de campagnes déclenchées par API.

**Types de cas d’utilisation :**

* **Unitaire** : ciblé individuellement, transactionnel (campagnes transactionnelles déclenchées par API)
* **Diffusion** : diffusion en masse ciblée par l’audience (campagnes marketing déclenchées par API)

Un problème fréquent avec les activités dynamiques survient lorsque l’appel API pour déclencher ou mettre à jour une activité dynamique renvoie une **réponse réussie (200 OK)**, mais que l’activité dynamique ne parvient pas à s’afficher ou à se mettre à jour sur l’appareil de l’utilisateur. Cette déconnexion entre la confirmation de l’API et le comportement réel de l’appareil peut se produire à plusieurs points du pipeline de diffusion. Ce guide fournit une approche de dépannage systématique pour identifier où la diffusion échoue, en examinant chaque étape, de la validation de la requête API au rendu de l’appareil.

## Conditions préalables

Avant de procéder au dépannage, vérifiez les points suivants :

* 
  +++ Configuration d’une session Assurance

  Configurez une **session** pour capturer des événements SDK et inspecter le pipeline de diffusion. Assurance offre une visibilité sur les éléments suivants :

   * Requêtes et réponses d’Edge Network
   * Événements de qualification de profil
   * Enregistrement du jeton push
   * Événements du cycle de vie d’une activité en direct

  Découvrez comment configurer Assurance dans la [documentation d’Adobe Experience Platform Assurance](https://experienceleague.adobe.com/fr/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance).

  **Remarque** : pour l’activité iOS Live, assurez-vous que votre application s’exécute sur un appareil iOS physique (iOS 16.1 ou version ultérieure) ou sur un simulateur Xcode (iOS 16.1 ou version ultérieure).

  +++

* 
  +++ Collecter les détails de la campagne déclenchée par l’API

  Accédez à votre campagne déclenchée par l’API dans Journey Optimizer et récupérez les éléments suivants :

   * Nom de la campagne
   * Identifiant de campagne trouvé dans l’URL ou les propriétés de la campagne
   * Version de la campagne, le cas échéant
   * Configuration de la surface, surface de l’application iOS utilisée pour l’activité Live

  +++

* 
  +++ Collecter des informations sur les requêtes API

  Lors de l’appel API pour déclencher l’activité Live , enregistrez :

   * Payload de requête API, y compris les identifiants de profil et les données d’activité en direct
   * Réponse de l’API comprenant le code d’état, l’identifiant de message et l’identifiant de requête
   * Date et heure de l’appel de l’API
   * Point d’entrée utilisé, par exemple `/campaign/{CAMPAIGN_ID}/execute`

  +++

* 
  +++ Identification du profil de test

  À partir de votre requête API, récupérez les éléments suivants :

   * Espace de noms du profil, par exemple ECID, e-mail, ID de client
   * Identifiant de profil utilisé dans l’appel API

  Vérifiez que vous pouvez rechercher ce profil dans Adobe Experience Platform. Découvrez comment [rechercher un profil dans la documentation Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html).

  +++

* 
  +++ Informations sur l’appareil et l’application

  Collectez les éléments suivants à partir de votre appareil de test :

   * Modèle d’appareil, par exemple iPhone 14 Pro
   * Version d’iOS
   * Identifiant du bundle de l&#39;application
   * Jeton push APNS
   * État de la connectivité réseau au moment du test

  +++

## Scénarios courants

### Problèmes de profil ou de jeton push {#profile-issue}

[!BADGE S’applique aux cas d’utilisation unitaires et de diffusion]{type=Positive}

L’API renvoie un HTTP 200, mais l’activité Live n’apparaît pas. Causes fréquentes :

* Le profil n’existe pas dans Adobe Experience Platform.
* Le jeton push d’activité dynamique n’a pas été synchronisé avec le profil.
* Les détails des notifications push d’activité en direct sont synchronisés, mais contiennent une configuration incorrecte, par exemple un `appId` ou une `attributeType` incorrect.

**Remarque pour les cas d’utilisation de diffusion** : si certains profils de votre audience n’ont pas de jetons, seuls ces profils ne recevront pas l’activité Live. Échantillonnez plusieurs profils de votre audience pour diagnostiquer les problèmes de jeton. Cela s’applique uniquement aux événements de début distants, et non aux événements de mise à jour ou de fin.

#### Contrôles préalables

* Configuration requise pour l’application iOS :
   * iOS 16.1+
   * `NSSupportsLiveActivities` défini sur `YES` dans `Info.plist`
   * `ActivityAttributes` correctement implémentée.
* Intégration de Mobile SDK :
   * Adobe Experience Platform Mobile SDK (messagerie SDK 5.11.0+)
   * `Messaging.registerLiveActivities` implémenté et appelé avec le jeton push d’activité dynamique.

#### Étapes de débogage

1. 
   +++ Vérifier que le profil existe dans Adobe Experience Platform

   1. Dans Journey Optimizer, accédez à **Client** `>` **Profils**.
   1. Effectuez une recherche à l’aide de l’espace de noms et de la valeur d’identité de la requête API.
   1. Si le profil est introuvable, il n’existe pas ou l’ingestion n’est pas terminée. Créez le profil ou attendez l’ingestion avant de déclencher l’activité Live .
   1. Si un profil est trouvé, passez à l’étape 2 ci-dessous pour vérifier si le jeton push est synchronisé.

      +++

1. 
   +++ Vérifier si le jeton push d’activité dynamique est synchronisé

   Vous pouvez utiliser Assurance pour vérifier l’enregistrement des jetons :

   1. Dans Assurance, à partir de la liste **Événements**, filtrez ou recherchez des événements `eventType = "liveActivity.pushToStart"`.
   1. Sélectionnez l’événement **Event** et examinez la payload.
   1. Vérifiez que les valeurs token, appId et attributeType sont présentes.
   1. Vérifiez si l’événement a bien été envoyé.

   Vous pouvez également archiver le profil Adobe Experience Platform.

   1. Dans Adobe Experience Platform, à partir de votre **Profil**, accédez à l’onglet **Événements**.
   1. Recherchez des événements `liveActivity.pushToStart`.
   1. Vérifiez l’horodatage d’événement et la payload.

   Si aucun événement n’est trouvé, votre application mobile n’appelle pas `Messaging.registerLiveActivity` correctement. Vous devez corriger l’intégration de SDK.

   +++

1. 
   +++ Valider les détails du jeton sur le profil

   1. À partir de votre **Profil**, accédez à l’onglet **Attributs**.
   1. Localisez `liveActivityPushNotificationDetails`.
   1. Vérifiez la configuration du jeton :

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **Valider chaque champ :**

   | Champ | Exigence | Problème courant |
   |-|-|-|
   | `appId` | Doit correspondre exactement à l’identifiant du bundle iOS | Incompatibilité entre les ID de bundle de développement/production |
   | `attributeType` | Doit correspondre exactement au nom de la structure de `ActivityAttributes` Swift (sensible à la casse) | Frappe ou nom de structure incorrect |
   | `platform` | Doit être `"apns"` ou `"apnsSandbox"` | Valeur de plateforme incorrecte |
   | `denylisted` | Doit être `false` | Jeton marqué comme non valide ou désactivé par l’utilisateur |
   | `token` | Jeton push APNS valide | Jeton expiré ou application réinstallée |

   Si un champ est incorrect : Mettez à jour l’application mobile, réenregistrez-la à l’aide de l’`Messaging.registerLiveActivities`, patientez 5 à 10 minutes, puis vérifiez à nouveau.

   Si le `liveActivityPushNotificationDetails` est manquant : le jeton n’a pas encore été synchronisé. Patientez 5 à 10 minutes après avoir vu l’événement `liveActivity.pushToStart` dans Assurance.

   +++

### Problèmes liés à la configuration de Campaign et à la payload {#payload-issues}

[!BADGE S’applique aux cas d’utilisation unitaires et de diffusion]{type=Positive}

Le profil existe avec des jetons valides, mais l’activité Live n’apparaît pas. Cela peut être dû aux éléments suivants :

* Mauvaise configuration de surface ou de canal.
* Structure de la payload de l’API incorrecte.
* `content-state` et `attributes` ne correspondent pas à l’implémentation d’iOS `ActivityAttributes`.
* `timestamp` obsolètes (critiques pour la mise à jour/la fin).

**Remarque pour les cas d’utilisation de diffusion** : la campagne doit être **marketing déclenché par l’API** (et non transactionnel). La payload utilise `audience` au lieu de `profile` individuels. Reportez-vous à [cette section](#broadcast-config) pour la structure de payload spécifique à la diffusion et à [la documentation d’Adobe Developer](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) pour obtenir des spécifications d’API complètes.

#### Contrôles préalables

* Campaign est une option **Transactionnel déclenché par API** (unitaire) ou **Marketing déclenché par API** (diffusion). L’option **Débit élevé** doit être **non** activée, car elle est incompatible avec l’activité Live.
* Vérifiez que le profil existe et que les jetons sont correctement synchronisés à l’aide du [scénario ci-dessus](#profile-issue).

#### Étapes de débogage

1. 
   +++ Vérifier la configuration de la surface de campagne

   1. Dans Journey Optimizer, ouvrez votre **Campagne** et accédez au menu **Actions**.
   1. Vérifiez la **configuration de l’activité dynamique**. La surface doit être configurée pour l’application iOS avec un identifiant de lot correspondant à l’`appId` dans le `liveActivityPushNotificationDetails` de votre profil. Par exemple, si votre profil a `"appId": "com.example.myapp"`, la surface doit cibler cette même application.
   1. Vérifiez que le **type d’activité** dans votre configuration de campagne correspond exactement au `attributeType` dans le `liveActivityPushNotificationDetails` de votre profil. Par exemple, si votre profil a `"attributeType": "FoodDeliveryLiveActivityAttributes"`, la campagne doit spécifier le même type d’activité.

      +++

1. 
   +++Validation de la structure de la payload de l’API

   Lors de l’exécution de la campagne par le biais de l’API, assurez-vous que la payload suit la structure correcte.

   **Payload unitaire :**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **Problèmes courants de payload :**

   | Champ | Exigence | Problème courant |
   |-|-|-|
   | `attributes-type` | Doit correspondre au type d&#39;activité de campagne et au `attributeType` de profil | Incompatibilité ou faute de frappe |
   | `campaignId` | Doit correspondre à l’identifiant de campagne activé | Identifiant de campagne incorrect ou manquant |
   | `content-available` | Doit être `1` | Valeur manquante ou incorrecte |
   | `event` | Doit être `"start"`, `"update"` ou `"end"` | Type d’événement non valide |
   | `timestamp` | Doit toujours être l’heure Unix actuelle/la plus récente en secondes | Utilisation de l’ancien horodatage/de l’horodatage mis en cache |
   | `userId` / `namespace` | Doit correspondre à un profil existant dans AEP | Incompatibilité de l’identifiant du profil |

   **Critique : utilisez toujours la dernière date et heure**

   * Le champ `timestamp` doit **toujours** correspondre à l’**heure Unix actuelle** (en secondes) au moment où chaque appel API est effectué.
   * Cela s’applique à **tous les types d’événements** : `start`, `update` et **en particulier`end`**.
   * **Impact sur les mises à jour/requêtes de fin** : l’utilisation d’un horodatage obsolète ou ancien entraîne l’échec ou l’ignorance des requêtes de mise à jour et de fin par l’appareil.
   * Ne réutilisez **PAS** les horodatages des requêtes précédentes et n’utilisez pas de valeurs mises en cache.
   * Générer un nouvel horodatage pour chaque appel API.

   **Champs facultatifs (tous les types d’événements) :**

   * `requestId` : identifiant unique pour le tracking (recommandé).
   * `alert` : objet avec `title` et `body` pour la notification (utile pour attirer l’attention sur les mises à jour).

   **À propos de `dismissal-date`:**

   * Champ facultatif contenant l&#39;heure Unix epoch (secondes).
   * **Uniquement pertinent en cas de`event: "end"`**.
   * Indique à quel moment l’activité Live doit être automatiquement supprimée de l’appareil.
   * Si elle n’est pas fournie lors de l’événement de fin, l’activité Live reste visible jusqu’à ce que l’utilisateur la ferme.
   * Doit être un horodatage ultérieur (postérieur à `timestamp`).

     +++

1. 
   +++ Alignement de la payload sur l’implémentation d’iOS

   Assurez-vous que la payload de l’API correspond à la mise en œuvre `ActivityAttributes` de l’application iOS. Le protocole `LiveActivityAttributes` d’Adobe SDK étend la `ActivityAttributes` d’iOS et nécessite une propriété `liveActivityData`.

   **Validez le mappage :**

   1. Votre `ActivityAttributes` doit mettre en œuvre le protocole `LiveActivityAttributes` d’Adobe. Exemple :

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **Notez** que le champ `liveActivityData` est requis par Adobe SDK et doit être inclus dans toutes les implémentations.

   1. La payload de l’API doit refléter la structure d’iOS :

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **Liste de contrôle de validation :**

   * Incluez tous les champs `ContentState` dans `content-state` (obligatoire pour tous les types d’événements).
   * Incluez tous les champs `LiveActivityAttributes` dans `attributes` (événements de début uniquement), notamment :
      * `liveActivityData` (obligatoire ; contient généralement un identifiant `liveActivityID` ou similaire)
      * Tous les champs personnalisés de votre structure
   * Faire correspondre exactement les noms des champs (respect de la casse).
   * Faire correspondre les types de données (chaîne, entier, booléen, objets imbriqués).
   * Conserver la structure de l’objet imbriqué.

   **Erreurs courantes :**

   | Problème | Impact | Correction |
   |-------|--------|-----|
   | `liveActivityData` manquant dans les attributs | L’activité en direct ne démarrera pas | Toujours inclure `liveActivityData` objet dans l’événement de début |
   | Champ obligatoire manquant dans l’événement de début | L’activité en direct ne démarrera pas | Ajouter tous les champs de la structure iOS |
   | Nom de champ incorrect (faute de frappe/casse) | Champ ignoré ou erreur d’analyse | Correspondance exacte des noms de champ iOS |
   | Type de données incorrect | Erreur d’analyse | Correspondance des types de données iOS |
   | Objet imbriqué manquant | Données incomplètes | Inclure toutes les structures imbriquées |
   | Inclusion de `attributes` dans la mise à jour/fin | Inutile, mais généralement ignoré | Inclure uniquement les `attributes` dans l’événement de début |
   | Horodatage obsolète à la mise à jour/fin | Mise à jour/fin ignorée par l’appareil | Toujours générer un nouvel horodatage |

   Pour consulter d’autres exemples, consultez la page [Créer une activité en direct](create-mobile-live.md).

   +++

1. 
   +++ Tester avec Assurance

   Vérifiez l’exécution de l’API et la diffusion de la payload à l’aide d’Assurance :

   1. Ouvrez votre session Assurance.
   1. Exécutez l’appel API pour déclencher l’activité Live .
   1. Dans la **Liste des événements**, vérifiez les éléments suivants :
      * Événements d’exécution de campagne.
      * Événements de diffusion d’activité en direct.
      * Événements d’erreur de validation de la payload.
   1. Examinez les payloads d’événement pour vérifier les éléments suivants :
      * La payload a été traitée correctement.
      * Aucune erreur de validation ne s’est produite.
      * L&#39;activité en direct a été envoyée aux APNs.

      +++

### Échecs de diffusion et analyse des erreurs

[!BADGE S’applique aux cas d’utilisation unitaires et de diffusion]{type=Positive}

Dans ce scénario, toutes les vérifications précédentes ont réussi :

* Le profil existe avec des [jetons push d’activité actifs valides](#profile-issue).
* Campaign est correctement [configuré avec la payload appropriée](#payload-issues)
* [ Les jetons de mise à jour sont synchronisés ](#token-not-synced) (pour les événements de mise à jour/de fin, cas d’utilisation unitaire uniquement)

Mais l’activité Live ne s’affiche toujours pas, ne se met pas à jour ou ne se termine pas comme prévu. Le problème peut concerner le système de diffusion Adobe ou le fournisseur de services de notification push (APNs).

**Remarque pour les cas d’utilisation de diffusion** : les rapports affichent des mesures pour tous les membres de l’audience. Certains profils peuvent réussir tandis que d’autres échouent.

**Pré-contrôles**

* **Scénarios précédents validés :**
   * Le profil existe avec le `liveActivityPushNotificationDetails` correct
   * La surface de campagne et le type d’activité sont corrects
   * La payload de l’API est valide avec l’horodatage actuel.
   * Les jetons de mise à jour sont synchronisés (pour les événements de mise à jour/de fin).

* **Appel API confirmé :**

   * L’appel API a renvoyé HTTP 200 (succès)
   * L’identifiant de campagne et les détails du destinataire sont corrects

#### Étapes de débogage

1. 
   +++ Vérifier les rapports de campagne

   1. Accédez à votre **Campagne d’activité dynamique**.
   1. Cliquez sur le bouton **Rapports**.
   1. Sélectionnez **Afficher le rapport en tout temps**.
   1. Consultez les sections suivantes :

      1. Vérifiez les mesures **Statistiques d’envoi** pour comprendre le succès de la diffusion :

         | Mesure | Signification | Éléments à rechercher |
         |-|-|-|
         | Ciblé | Nombre de profils qualifiés pour l’audience | Doit inclure votre profil de test |
         | Envois | Nombre total de notifications push ayant fait l’objet d’une tentative | Doit correspondre à vos appels API |
         | Délivrés | Distribué avec succès sur les appareils | Comparer aux envois pour voir le taux de succès |
         | Erreurs d’envoi | Notifications push dont l’envoi a échoué | Nombres élevés |
         | Envoyer les exclusions | Profils exclus par Adobe Journey Optimizer | Vérifier si votre profil a été exclu |

      1. Si Envoyer les erreurs > 0, consultez le tableau **Causes des erreurs** pour obtenir des codes d’erreur et des messages spécifiques :

         | Erreur courante | Signification | Résolution |
         |-|-|-|
         | Jeton non valide | Jeton push non valide ou expiré | Réenregistrer les jetons d’activité dynamiques sur l’appareil |
         | Jeton introuvable | Aucun jeton valide associé au profil | Vérifier l`liveActivityPushNotificationDetails`existence |
         | APNs rejetés | Le service de notification push Apple a rejeté la notification push | Vérifier le certificat APNS, l’ID de lot, l’environnement |
         | Timeout réseau | Impossible d&#39;atteindre les APNs | Problème transitoire ; réessayez l’appel API |

      1. Si **Envoyer les exclusions** > 0, cochez le tableau **Causes d’exclusion** :

         | Exclusion Commune | Signification | Résolution |
         |-|-|-|
         | Profil désinscrit | L’utilisateur s’est opposé aux notifications | Vérifier le statut de consentement du profil |
         | Jeton placé sur la liste bloquée | Jeton marqué comme non valide | Réenregistrer le jeton ou vérifier le statut de la liste bloquée |
         | Profil non éligible | Le profil ne répond pas aux critères de la campagne. | Vérifier les règles d’audience de campagne |

   Pour en savoir plus, consultez la page [ Rapport de campagne d’activité dynamique ](../reports/campaign-global-report-cja-activity.md).

   +++

1. 
   +++ Vérifier les événements de retour de message dans le profil

   1. Accédez à **Client** > **Profils** dans Journey Optimizer.
   1. Recherchez et ouvrez le profil.
   1. Sélectionnez l’onglet **Événements**.
   1. Filtrez ou recherchez des événements avec `eventType = "message.feedback"`.
   1. Recherchez des événements de retour correspondant au type de `liveActivityID` et de `event` de votre activité Live.
   1. Examinez les champs clés suivants :

      | Champ | Valeurs possibles | Signification |
      |-|-|-|
      | `feedbackStatus` | `sent`, `error`, `denylist` | Résultat de diffusion du prestataire |
      | `serviceProvider` | `apns/apnsSandbox` | Doit être un APN pour les activités iOS Live |
      | `errorCode` | Code numérique ou `null` | Code d’erreur spécifique à APNS en cas d’échec |
      | `errorMessage` | Description ou `null` de l’erreur | Message d’erreur lisible par l’utilisateur |

   1. **If `feedbackStatus: "error"`:**
      * Vérifiez les `errorCode` et les `errorMessage` pour détecter les erreurs APNs spécifiques
      * Les erreurs APNs courantes incluent un jeton expiré, un certificat non valide, un ID de lot incorrect

   1. **Si aucun événement de retour n’a été trouvé :**
      * Il se peut que la notification push n’ait pas été tentée
      * Vérifiez si le profil a été exclu des rapports de campagne, comme décrit à l’étape 1 ci-dessus.

      +++

1. 
   +++ Vérifier la diffusion de l’activité en direct aux APNs dans Assurance

   1. Ouvrez votre session Assurance, elle doit être active pendant l’appel API.
   1. Exécutez l’appel API (début, mise à jour ou fin).
   1. Dans la **Liste des événements**, recherchez les événements de diffusion d’activité en direct .
   1. Recherchez des événements liés à la diffusion des notifications push APNS.
   1. Recherchez les indicateurs suivants :
      * **Requête push aux APNs** : confirme qu’Adobe a envoyé la notification push aux serveurs Apple.
      * **Réponse APNs** : indique si APNs a accepté ou rejeté la notification push.
      * **Statut de la diffusion** : indication de succès ou d&#39;échec
   1. Si des problèmes sont détectés, reportez-vous aux problèmes de diffusion APNS courants suivants :

      | Problème | Symptôme dans Assurance | Résolution |
      |-|-|-|
      | Certificat APNS expiré | Erreur d’authentification | Renouveler et charger un nouveau certificat APNS |
      | Mauvais environnement (développement ou production) | Erreur de correspondance de jeton | S’assurer que le certificat correspond au type de build de l’application |
      | Incompatibilité de l’ID de lot | Identifiant de lot non valide | Vérifier que l’ID de groupe de certificats correspond à l’application |
      | Jeton expiré | Erreur InvalidToken depuis APNS | Réenregistrer les jetons d’activité actifs |
      | Limitation de débit | Trop de requêtes | Réduire la fréquence des appels API |

      +++

1. 
   +++ Effectuer des vérifications de diagnostic supplémentaires

   1. Vérifiez les mesures de cycle de vie des activités dans le rapport de campagne.

      Dans le rapport de campagne, passez en revue la section **Cycle de vie des activités dynamiques** :

      | Mesure | Éléments à vérifier |
      |-|-|
      | Démarrages à distance | Doit afficher le nombre de démarrages déclenchés par l’API |
      | Mises à jour | Doit afficher le nombre d’événements de mise à jour |
      | Se termine | Doit afficher le nombre d’événements de fin |
      | Nombre de totaux | Volume global des événements d’activité en direct |

      Si ces mesures sont égales à zéro ou ne correspondent pas à vos appels API, il existe un problème de diffusion entre Adobe et APNS.

   1. Si Adobe affiche une diffusion réussie mais que l’appareil n’affiche pas l’activité Live :

      * Recherchez des erreurs d’activité en direct dans les journaux des appareils iOS.
      * Vérifiez que l’application est en premier plan ou en arrière-plan (non terminée).
      * Vérifiez que l’appareil dispose d’une connectivité réseau.
      * Testez plusieurs appareils pour exclure les problèmes spécifiques à l’appareil.
      * Vérifiez qu’iOS version 16.1 ou ultérieure.

      +++

1. 
   +++ Transmission à l’assistance Adobe

   Si vous avez terminé toutes les étapes et que le problème n’est pas résolu, contactez l’assistance clientèle d’Adobe à l’adresse suivante :

   **Informations requises :**

   * Identifiant et nom de campagne
   * Espace de noms et ID du profil
      * `liveActivityID` à partir de la payload de l’API
   * Horodatages des appels API
   * Captures d’écran de :
      * Rapports De Campagne (Statistiques D’Envoi, Raisons D’Erreur, Raisons D’Exclusion)
      * Événements de profil (`liveActivity.updateToken`, `message.feedback`)
      * Session Assurance présentant les événements de diffusion
   * Payload de requête API complète
   * Détails du certificat APNS (expiration, environnement, ID de lot)

     +++

## Scénarios spécifiques à une unité

### Jeton de mise à jour d’activité dynamique non synchronisé{#token-not-synced}

L’activité Live démarre correctement sur l’appareil, mais les appels d’API `update` ou `end` suivants (renvoyant le HTTP 200) ne parviennent pas à mettre à jour ou à ignorer l’activité Live. Cela se produit lorsque le **jeton de mise à jour de l’activité dynamique** n’est pas correctement synchronisé avec le système Adobe.

**Présentation des jetons de mise à jour**

Lorsqu’une activité Live démarre sur un appareil, iOS génère un jeton de mise à jour unique pour cette instance d’activité Live spécifique. Ce jeton est requis pour :

* Envoi de mises à jour à l&#39;activité Live
* Terminaison à distance de l’activité Live

Chaque instance d’activité active possède son propre jeton de mise à jour unique. Adobe a besoin de ce jeton pour diffuser les événements de mise à jour et de fin.

**Comportement attendu**

Pour que les événements de mise à jour et de fin fonctionnent, les événements suivants doivent se produire :

1. L’activité en direct démarre correctement sur l’appareil.
1. L’appareil génère un jeton de mise à jour pour cette instance d’activité active.
1. Mobile SDK capture et envoie le jeton de mise à jour à Adobe.
1. Le jeton de mise à jour est synchronisé et stocké dans le système Adobe.
1. Les appels API suivants pour la mise à jour/l’utilisation finale de ce jeton pour la diffusion.

**Pré-vérifications :**

* **Autorisation utilisateur** : la première fois qu’une activité Live démarre sur un appareil, iOS affiche une invite système indiquant « Autoriser [Nom de l’application] à fournir des mises à jour d’activité Live ? » L’utilisateur **doit appuyer sur « Autoriser »** pour que les jetons de mise à jour soient générés et synchronisés. Si l’utilisateur clique sur « Ne pas autoriser », aucun jeton de mise à jour n’est créé et les requêtes de mise à jour/fin échouent. Il s’agit d’une autorisation unique par application.
* **Validation des profils et des campagnes** : effectuez les vérifications [Scénario 1](#profile-issue) et [Scénario 2](#payload-issues) pour vous assurer que le profil, les jetons et la configuration de la campagne sont corrects.

#### Étapes de débogage

1. 
   +++ Vérification de la synchronisation des jetons de mise à jour dans Assurance

   1. Ouvrez votre session Assurance.
   1. Assurez-vous que la session était active lorsque l’activité En direct a démarré sur l’appareil.
   1. Filtrez ou recherchez des événements avec `eventType = "liveActivity.updateToken"`.
   1. Sélectionnez l’événement et examinez la payload :

      * Vérifiez que le champ `token` contient une chaîne de jeton de mise à jour valide.
      * Vérifiez que le `liveActivityID` correspond à votre instance d’activité active.
      * Vérifiez que la `activityType` correspond à votre `attributes-type`.

   1. Si l’événement est introuvable :

      * Le jeton de mise à jour n’a pas été généré ou capturé par le SDK.
      * Vérifiez si l’utilisateur a accordé des autorisations d’activité en direct.
      * Vérifiez que l’activité Live a démarré correctement sur l’appareil.
      * Vérifiez que le SDK mobile est correctement intégré pour capturer les jetons de mise à jour.

   1. Si l’événement est trouvé, passez à l’étape 2.

      +++

2. 
   +++ Vérifier le jeton de mise à jour dans les événements de profil

   1. Accédez à **Client** > **Profils** dans Journey Optimizer.
   1. Recherchez et ouvrez le profil.
   1. Sélectionnez l’onglet **Événements**.
   1. Recherchez les événements `liveActivity.updateToken`.
   1. Vérifiez les détails de l’événement :

      * Vérifiez que l’horodatage est récent (correspond au démarrage de l’activité Live ).
      * Vérifiez que les `token` et les `liveActivityID` sont présents.
      * Assurez-vous que la `activityType` est correcte.

   1. Si l’événement est introuvable dans le profil :

      * L’événement de jeton de mise à jour n’a peut-être pas encore été ingéré dans le profil.
      * Patientez 5 à 10 minutes et vérifiez à nouveau.
      * S’il manque toujours après 15 minutes, il peut y avoir un problème d’ingestion d’événement.

   1. Si l’événement est trouvé, le jeton de mise à jour a été synchronisé. Vous pouvez passer à l’étape 3.

      +++

3. 
   +++ Vérifier les événements de diffusion des activités en direct dans Assurance

   1. Au cours de votre session Assurance, exécutez une mise à jour ou terminez un appel API.
   1. Dans la **Liste des événements**, recherchez les événements de diffusion d’activité en direct (événements push APNs).
   1. Recherchez des événements indiquant :
      * Notification push envoyée aux APNs.
      * Réponse des APNs (succès ou erreur).
      * Confirmation de diffusion.
   1. Si un événement de diffusion APNS est présent : la notification push a été envoyée. Si l’appareil n’est toujours pas mis à jour, le problème peut concerner l’appareil (l’application ne gère pas la notification push, problèmes réseau, etc.).
   1. Si l&#39;événement de diffusion APNs est manquant : le jeton de mise à jour peut ne pas être correctement stocké ou associé au profil dans le système Adobe.
   1. Si des événements d’erreur sont présents : examinez les détails de l’erreur pour des raisons d’échec spécifiques (jeton non valide, APN rejetés, etc.).

      +++

## Scénarios spécifiques à la diffusion

### Problèmes liés à la configuration des campagnes de diffusion et à la payload{#broadcast-config}

Cette section aborde les scénarios de dépannage spécifiques aux activités de diffusion en direct, qui nécessitent des approches de débogage différentes de celles des campagnes unitaires.

Lorsque les profils disposent de jetons valides mais que l’activité Live n’apparaît pas, ne met pas à jour ou ne se comporte pas comme prévu pour les membres de l’audience, le problème provient généralement de l’un des éléments suivants :

* La campagne n’est pas configurée en tant que marketing déclenché par l’API.
* La payload de l’API utilise une structure de diffusion incorrecte (`audience` ou `input-push-channel` manquant).
* Les champs `content-state` et `attributes` ne correspondent pas à l’implémentation d’iOS `ActivityAttributes`.
* Le `input-push-channel` n’a pas été créé correctement sur le portail Apple Developer.

Ce scénario de dépannage s’applique à tous les événements d’activité Live dans les campagnes de diffusion : `start`, `update` et `end`.

**Pré-vérifications :**

* **Type de campagne** :
   * Vérifiez que la campagne est créée en tant que marketing déclenché par l’API (obligatoire pour les campagnes diffusées/basées sur l’audience).
   * Vérifiez qu’une audience est définie dans la configuration de la campagne.
* **Validation des profils et des jetons** : échantillonnez plusieurs profils de l’audience pour vérifier qu’ils disposent de `liveActivityPushNotificationDetails` valides. Pour obtenir des étapes de validation détaillées, suivez [Scénario 1](#profile-issue).

#### Étapes de débogage

1. 
   +++ Vérifier la configuration de l’audience de la campagne

   1. Ouvrez votre **campagne marketing déclenchée par API** dans Journey Optimizer.
   1. Accédez à la section **Audience** et vérifiez les éléments suivants :
      * Une audience est sélectionnée pour la campagne.
      * L’ID d’audience correspond à celui utilisé dans votre payload d’API.
      * L’audience contient les profils attendus.
   1. Accédez à la section **Actions**.
   1. Vérifiez la **Configuration de l&#39;activité dynamique** :
      * La configuration doit être définie pour l’application iOS avec l’identifiant de lot approprié.
      * Le type d’activité doit correspondre à la `attributes-type` de votre payload API. Par exemple, si votre payload contient des `"attributes-type": "AirplaneTrackingAttributes"`, la campagne doit spécifier le même type d’activité.

      +++

1. 
   +++ Validation de la structure de la payload de l’API de diffusion

   La structure de la payload de diffusion diffère des campagnes unitaires. Vérifiez que la payload respecte le format de diffusion approprié.

   **Champs obligatoires pour la diffusion :**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **Problèmes courants de payload :**

   | Champ | Exigence | Problème courant |
   |-|-|-|
   | `campaignId` | Doit correspondre à l’identifiant de campagne marketing activé | Mauvais identifiant de campagne ou utilisation de la campagne transactionnelle |
   | `audience.id` | Doit correspondre à une audience existante dans AEP | ID d’audience incorrect ou audience inexistante |
   | `input-push-channel` | Obligatoire pour la diffusion - Identifiant unique de cette instance de diffusion | Il manque ou ne correspond pas au `channelID` dans `liveActivityData` |
   | `timestamp` | Doit toujours être l’heure Unix actuelle/la plus récente en secondes | Utilisation de l’ancien horodatage/de l’horodatage mis en cache |
   | `event` | Doit être `"start"`, `"update"` ou `"end"` | Type d’événement non valide |
   | `attributes-type` | Doit correspondre au type d&#39;activité de campagne | Incompatibilité ou faute de frappe |
   | `content-available` | Doit être `1` | Valeur manquante ou incorrecte |

   **Champs critiques spécifiques à la diffusion :**

   * **`input-push-channel`** :
      * Obligatoire pour toutes les activités de diffusion en direct.
      * Sert d’identifiant unique pour cette instance de diffusion spécifique.
      * Tous les profils de l’audience reçoivent des activités en direct liées à ce canal.
      * Doit correspondre à la `channelID` dans `liveActivityData.channelID` (voir Étape 3).
      * Doit être créé pour le `appID` sur le portail Apple Developer Portal par le client.
      * Seuls les canaux créés pour l’`appID` spécifique peuvent être utilisés pour la diffusion d’activités en direct sur cette application.

   * **`audience.id`** :
      * Un segment d’audience valide créé dans Adobe Experience Platform doit être référencé.
      * Tous les profils de cette audience sont ciblés pour l’activité En direct .
      * L’audience doit être activée et contenir des profils avec des `liveActivityPushNotificationDetails` valides.

   **Utilisez toujours la dernière date et heure :**

   * Le champ `timestamp` doit toujours correspondre à l’heure Unix actuelle (en secondes) pour chaque appel API.
   * Cette exigence s’applique à tous les types d’événements : `start`, `update` et `end`.
   * **Critique pour les mises à jour/fin** : l’utilisation d’horodatages obsolètes entraîne l’échec des demandes de mise à jour et de fin.
   * Générez un nouvel horodatage pour chaque appel API de diffusion.

   **Champs facultatifs :**

   * `dismissal-date` : époque Unix pour le rejet automatique (pertinent uniquement pour les événements `end`)
   * `alert` : objet avec `title` et `body` pour la notification

   Consultez la documentation de l’API de messagerie Adobe Journey Optimizer [](https://developer.adobe.com/journey-optimizer-apis/references/messaging) pour obtenir des spécifications d’API complètes.

   +++

1. 
   +++ Alignement de l’état du contenu, des attributs et du canal push d’entrée avec l’implémentation d’iOS

   Assurez-vous que les champs de payload correspondent à l’implémentation `ActivityAttributes` de votre application iOS et que le `input-push-channel` correspond au `channelID` dans `liveActivityData`.

   1. Vérifiez votre définition d’Attributs d’activité iOS.

   Votre structure de `ActivityAttributes` personnalisée doit implémenter le protocole `LiveActivityAttributes` d’Adobe :

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. Mappez les champs iOS à la payload de l’API de diffusion.

   Pour tous les événements, incluez les `attributes` et les `content-state` :

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **Critique : `input-push-channel` doit correspondre à`channelID`**

   * La valeur `input-push-channel` à la racine de `aps` doit correspondre exactement à la `channelID` dans `liveActivityData`.
   * Dans l’exemple ci-dessus, les deux valeurs sont `"FEt0NgvLEfEAAOqA6AXdIQ=="`.
   * Cette correspondance associe l’instance de diffusion aux données d’activité en direct.
   * Une incohérence entraîne des échecs de diffusion.

   **Points clés de validation :**

   * Incluez tous les champs `ContentState` dans `content-state` pour tous les types d’événements.
   * Incluez tous les champs de `LiveActivityAttributes` personnalisés dans `attributes` pour les événements de début uniquement.
   * Pour les événements de début, les `liveActivityData.channelID` doivent correspondre aux `input-push-channel`.
   * Les noms des champs sont sensibles à la casse et doivent correspondre exactement.
   * Les types de données doivent correspondre (chaîne, entier, booléen, objets imbriqués, etc.).
   * Pour les événements de mise à jour/fin, utilisez le même `input-push-channel` que l’événement de début d’origine.

   **Erreurs courantes :**

   | Problème | Impact | Correction |
   |-|-|-|
   | `input-push-channel` manquant | La diffusion ne fonctionnera pas | Ajouter un identifiant de canal unique pour chaque diffusion |
   | `input-push-channel` ne correspond pas à `channelID` | L’activité en direct ne démarrera pas | Assurez-vous que les deux valeurs sont identiques |
   | Différents `input-push-channel` pour la mise à jour/fin | La mise à jour/la fin n’atteindra pas les activités actives | Utiliser le même identifiant de canal tout au long du cycle de vie |
   | `liveActivityData.channelID` manquant | L’activité en direct ne sera pas liée à la diffusion. | Inclure les `channelID` dans les attributs pour l’événement de début |
   | Champ obligatoire manquant dans l’événement de début | L’activité en direct ne démarrera pas | Ajouter tous les champs de la structure iOS |
   | Nom de champ incorrect (faute de frappe/casse) | Champ ignoré ou erreur d’analyse | Correspondance exacte des noms de champ iOS |
   | Horodatage obsolète à la mise à jour/fin | Mise à jour/fin ignorée par les appareils | Toujours générer un nouvel horodatage |

   +++

1. 
   +++ Tester avec Assurance

   Vérifiez l’exécution de l’API et la diffusion de la payload à l’aide d’Assurance :

   1. Ouvrez votre session Assurance sur un appareil de test qui fait partie de l’audience.
   1. Exécutez l’appel API de diffusion.
   1. Dans la **Liste des événements**, recherchez :
      * Événements d’exécution de campagne.
      * Événements de diffusion d’activité en direct.
      * Événements d’erreur indiquant les échecs de validation de la payload.
   1. Inspectez les payloads d’événement pour confirmer :
      * La payload a été traitée correctement.
      * Le `input-push-channel` est présent.
      * Aucune erreur de validation ne s’est produite.
      * Des activités en direct ont été envoyées aux APNs pour les membres de l&#39;audience.

      +++

### Profil non présent dans l’audience ou instantané d’audience obsolète

Dans ce scénario, la campagne et la payload sont correctement configurées, mais des profils spécifiques ne reçoivent pas l’activité En direct . Cela se produit généralement lorsque :

* Le profil n’est pas membre de l’audience liée à la campagne.
* L’audience est une audience par lots et contient un instantané obsolète des données de profil.
* Les jetons d’activité en direct du profil ont été ajoutés récemment, mais n’ont pas encore été reflétés dans l’instantané d’audience.

Ce scénario de dépannage s’applique spécifiquement aux campagnes de diffusion utilisant le ciblage basé sur l’audience.

**Comprendre l’évaluation des audiences**

Adobe Experience Platform utilise différentes méthodes d’évaluation d’audience qui déterminent à quel moment les mises à jour de profil sont répercutées dans l’audience :

| Méthode | Fréquence d’évaluation | Actualisation des données | Idéal pour |
|-|-|-|--|
| Lot | Une fois par jour (planifié) | Peut être périmé jusqu’à 24 heures. | Audiences volumineuses, non sensibles à l’heure |
| Diffusion en continu | Temps réel (lors des modifications de profil) | En temps quasi réel pour les profils mis à jour | Sensible à l’heure, nécessite des mises à jour de profil |

**Pré-vérifications :**

* **Validation des campagnes et des payload** :
   * Effectuez les vérifications dans [ce scénario](#broadcast-config) pour vous assurer que la campagne et la payload sont correctes.
   * Vérifiez que la `audience.id` dans la payload de l’API correspond à la configuration de la campagne.
* **Le profil existe** : vérifiez que le profil existe dans AEP avec des `liveActivityPushNotificationDetails` valides.

#### Étapes de débogage

1. 
   +++ Vérifier que le profil est dans l’audience

   Tout d’abord, vérifiez si le profil qui doit recevoir l’activité En direct fait réellement partie de l’audience.

   1. Accédez à **Audiences** dans Adobe Experience Platform.
   1. Recherchez et ouvrez l’audience à l’aide du `audience.id` de votre campagne.
   1. Cliquez sur **Parcourir** ou **Exemples de profils** pour afficher les membres de l’audience.
   1. Recherchez votre profil de test à l’aide de l’espace de noms et de la valeur d’identité.
   1. **Si le profil est introuvable dans l’audience :**
      * Le profil ne répond pas aux critères d’audience ou aux règles de segment.
      * Consultez la définition de l’audience pour comprendre les exigences d’appartenance.
      * Mettez à jour les données de profil ou la définition d’audience pour inclure le profil.
      * Attendez la fin de l’évaluation de l’audience (voir Étape 2).
   1. **Si le profil est trouvé dans l’audience :** passez à l’étape 2 pour vérifier l’actualisation des données.

      +++

2. 
   +++ Vérifier le type et le planning d’évaluation des audiences

   Déterminez si l’audience utilise une évaluation par lots ou par flux, car cela détermine l’actualisation des données.

   1. Sur la page **Détails de l’audience**, vérifiez la méthode **Évaluation** :
      * **Lot** : évalué une fois par jour selon un planning.
      * **Streaming** : évalué en temps réel lorsque des mises à jour de profil se produisent.
      * **** : évalué aux emplacements Edge en temps réel.

   Suivez les étapes de dépannage appropriées en fonction de la méthode d’évaluation :

   **Si l’audience utilise l’évaluation par lots :**

   1. **Comprendre les limites des audiences par lots :**
      * Les audiences par lots sont évaluées une fois par jour (généralement le soir).
      * L’instantané d’audience peut avoir jusqu’à 24 heures.
      * Si un profil a récemment enregistré des jetons d’activité Dynamique , ces jetons peuvent ne pas se trouver dans l’instantané actuel.
      * Les mises à jour apportées aux profils ne seront reflétées que lors de la prochaine évaluation par lots.

   1. **Vérifier à quel moment s’est produite la dernière évaluation :**
      * Dans les détails de l’audience, recherchez l’horodatage **Dernière évaluation**.
      * Si les `liveActivityPushNotificationDetails` du profil ont été mises à jour après cet horodatage, l’audience contient des données obsolètes.

   1. **Résoudre les données obsolètes :**
      1. **Option 1 : attendre l’évaluation par lots planifiée**
         * La prochaine évaluation par lot inclura les données de profil mises à jour.
         * Cela se produit automatiquement une fois par jour.
         * Idéal pour les scénarios non urgents.

      1. **Option 2 : déclencher l’évaluation des audiences à la demande**
         1. Accédez à **Audiences** dans AEP.
         1. Sélectionnez votre audience.
         1. Cliquez sur **Évaluer maintenant** ou **Activer à la demande**.
         1. Attendez la fin de l’évaluation (cela peut prendre de quelques minutes à plusieurs heures selon la taille de l’audience).
         1. Vérifiez que le profil contient désormais des données mises à jour dans l’instantané d’audience.
         1. Réessayez l’appel API de diffusion.

   **Si l’audience utilise l’évaluation par flux :**

   1. **Comprendre le comportement de l’audience de diffusion en continu :**
      * Les audiences en flux continu sont évaluées en temps réel lorsque des mises à jour de profil se produisent.
      * **Nouveaux profils** : remplissez les conditions peu de temps après leur création s’ils répondent aux critères du segment.
      * **Profils mis à jour** : qualifiez-vous ou disqualifiez-vous peu de temps après la mise à jour.
      * **Profils inchangés existants** : ne sont pas réévalués, sauf si une mise à jour est effectuée.

   1. **Identifier le problème :**
      * Si un profil existe déjà et répond aux critères du segment, mais qu’aucune mise à jour n’a lieu sur ce profil, il ne peut pas être ajouté à une audience de diffusion en continu nouvellement créée.
      * Le profil doit recevoir une mise à jour (toute modification d’attribut) pour déclencher une réévaluation.

   1. **Résolvez le problème :**
      * **Pour les nouveaux profils** : ils sont automatiquement qualifiés si les critères sont remplis. Aucune action n’est nécessaire.
      * **Pour les profils existants sans mises à jour récentes :**
         * Apportez une mise à jour mineure au profil (par exemple, mettez à jour un champ d’horodatage).
         * Cela déclenche l’évaluation en flux continu et ajoute le profil à l’audience.
         * Alternative : utilisez une audience par lots ou une audience Edge pour les profils existants.

      +++
