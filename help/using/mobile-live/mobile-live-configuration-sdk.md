---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal d’activité en direct
description: Découvrez comment configurer votre intégration au SDK mobile Adobe Experience Platform.
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 02ca7c8e-105a-4e77-9aad-2381904255d0
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 76%

---

# Intégration d’une activité en direct à Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}


Adobe Experience Platform Mobile SDK offre une prise en charge intégrée de l’activité Apple Live. Cela permet à votre application d’afficher des mises à jour dynamiques en temps réel directement sur l’écran de verrouillage et Dynamic Island sans ouvrir l’application.

1. [Importer les modules requis](#import)

   Importez les modules suivants : **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**

1. [Définir les attributs](#attributes)

   Respectez les `LiveActivityAttributes`, incluez des `LiveActivityData` et des attributs `ContentState`.

1. [Enregistrer l’activité dynamique](#register)

   Utilisez `Messaging.registerLiveActivity()` après l’initialisation du SDK.

1. [Créer une configuration de widget](#widget)

   Implémentez `ActivityConfiguration` pour l’écran de verrouillage et l’interface de Dynamic Island.

1. [Démarrer une activité en direct localement (facultatif)](#local)

   L’activité active peut être lancée à distance via Journey Optimizer ou localement dans le code de l’application.

1. [Ajouter la prise en charge du débogage (facultatif)](#debug)

   Implémentez `LiveActivityAssuranceDebuggable` pour Assurance.

Vérifiez que les versions minimales suivantes sont installées pour garantir une configuration et une compatibilité correctes.

>[!BEGINSHADEBOX]

**Conditions préalables requises :**

* **iOS :**
   * **iOS 16.1 ou version ultérieure** : fonctionnalité de base d’activité en direct
   * **iOS 17.2+** : prise en charge du démarrage par notification push
   * **iOS 18+** : prise en charge des canaux de diffusion
* **Xcode :** 14.0 ou version ultérieure
* **Swift :** 5.7 une version ultérieure
* **Dépendances :** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit
* **AEP Mobile SDK version** : iOS Messaging 5.11.0 ou ultérieure

>[!ENDSHADEBOX]

## Étape 1 : importer les modules requis {#import}

Pour commencer, vous devez d’abord importer les modules suivants : **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Étape 2 : définir les attributs de votre activité en direct {#attributes}

Créez une structure conforme au protocole `LiveActivityAttributes`. Cela définit à la fois les données statiques et l’état du contenu dynamique pour votre activité en direct.

Les principaux composants sont les suivants :

* **`liveActivityData`** (obligatoire) contenant des données spécifiques à Adobe Experience Platform.
   * Pour les utilisateurs et utilisatrices individuels : utiliser `LiveActivityData(liveActivityID: "unique-id")`
   * Pour la diffusion : utiliser `LiveActivityData(channelID: "channel-id")`

* Attributs statiques, propriétés personnalisées spécifiques à votre cas d’utilisation, par exemple `restaurantName`.

* **`ContentState`** qui définit les données dynamiques qui peuvent être mises à jour pendant le cycle de vie de l’activité en direct. Il doit être conforme à `Codable` et `Hashable`.

* L’énumération `LiveActivityOrigin` spécifie si une activité a été lancée localement dans l’application ou à distance par le biais d’un démarrage par notification push, pris en charge dans iOS 17.2 et les versions ultérieures. Cette valeur permet au SDK de faire la distinction entre l’activité active déclenchée localement et l’activité active déclenchée à distance pendant la collecte de données.

**Exemples**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activity
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activity
    public init(liveActivityID: String)   // For individual Live activity
}
```

Vous pouvez également enregistrer plusieurs types d’activités en direct pour votre application :

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Étape 3 : Enregistrement de l’activité Live {#register}

Enregistrez vos types d’activités en direct dans votre `AppDelegate` après l’initialisation du SDK. Vous pouvez ainsi :

* Active la collecte automatique des jetons push-to-start (iOS 17.2+)
* Collecte automatiquement les jetons de mise à jour des activités en direct.
* Permet la gestion du cycle de vie et le suivi des événements.

**Exemple pour une activité en direct de livraison de repas :**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Étape 4 : créer des widgets d’activité en direct {#widgets}

L’activité en direct s’affiche par le biais de widgets. Vous devez créer un lot de widgets et une configuration :

**Exemple pour une activité en direct de livraison de repas :**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## Étape 5 : démarrer une activité en direct localement (facultatif) {#local}

Journey Optimizer peut démarrer l’activité en direct à distance, mais vous pouvez également la démarrer localement :

**Exemple pour une activité en direct de livraison de repas :**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## Étape 6 : ajouter la prise en charge du débogage (facultatif) {#debug}

Si nécessaire, vous pouvez déboguer les schémas d’activité en direct dans Adobe Assurance :

**Exemple pour une activité en direct de livraison de repas :**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```
