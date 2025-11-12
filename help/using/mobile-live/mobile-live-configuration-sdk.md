---
solution: Journey Optimizer
product: journey optimizer
title: Configuration du canal d’activité en direct
description: Découvrez comment configurer votre intégration Adobe Experience Platform Mobile SDK
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 1%

---


# Intégration d’une activité en direct à Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}

>[!BEGINSHADEBOX]

* [Prise en main de l’activité Live](get-started-mobile-live.md)
* [Configuration de l’activité en direct](mobile-live-configuration.md)
* **[Intégration d’une activité en direct à Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**
* [Créer une activité Live](create-mobile-live.md)
* [Questions fréquentes](mobile-live-faq.md)
* [Rapport de campagne d’activité dynamique](../reports/campaign-global-report-cja-activity.md)


>[!ENDSHADEBOX]

Adobe Experience Platform Mobile SDK offre une prise en charge intégrée des activités Apple Live . Cela permet à votre application d’afficher des mises à jour dynamiques en temps réel directement sur l’écran de verrouillage et l’île dynamique sans ouvrir l’application.

1. [Importer les modules requis](#import)

   Importez les modules suivants : **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

1. [Définir les attributs](#attributes)

   Respectez les `LiveActivityAttributes`, incluez les attributs `LiveActivityData` et a `ContentState`.

1. [Enregistrement des activités dynamiques](#register)

   Utilisez `Messaging.registerLiveActivity()` après l’initialisation de SDK.

1. [Créer une configuration de widget](#widget)

   Implémentez `ActivityConfiguration` pour l’écran de verrouillage et l’interface Dynamic Island.

1. [Démarrer une activité Live localement (facultatif)](#local)

   Les activités en direct peuvent être lancées à distance via Journey Optimizer ou localement dans le code de l’application.

1. [Ajouter la prise en charge du débogage (facultatif)](#debug)

   Implémentez `LiveActivityAssuranceDebuggable` pour Assurance.

Vérifiez que les versions minimales suivantes sont installées pour garantir une configuration et une compatibilité correctes.

>[!BEGINSHADEBOX]

**Conditions préalables requises:**

* **iOS:**
   * **iOS16.1 ou version ultérieure** : fonctionnalité basique d’activité en direct
   * **iOS 17.2+** : prise en charge push-to-start
   * **iOS 18+** : prise en charge des canaux de diffusion
* **Xcode:** 14.0 ou version ultérieure
* **Swift:** 5.7 ou version ultérieure
* **Dépendances :** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## Étape 1 : importer les modules requis {#import}

Pour commencer, vous devez d’abord importer les modules suivants : **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Étape 2 : définir les attributs de votre activité Live {#attributes}

Créez une structure conforme au protocole `LiveActivityAttributes`. Cela définit à la fois les données statiques et l’état du contenu dynamique pour votre activité en direct .

Les principaux composants sont les suivants :

* **`liveActivityData`** (obligatoire) contenant des données spécifiques à Adobe Experience Platform.
   * Pour les utilisateurs individuels : utilisez `LiveActivityData(liveActivityID: "unique-id")`
   * Pour la diffusion : utiliser `LiveActivityData(channelID: "channel-id")`

* Attributs statiques, propriétés personnalisées spécifiques à votre cas d’utilisation, par exemple `restaurantName`.

* **`ContentState`** qui définit les données dynamiques qui peuvent être mises à jour pendant le cycle de vie de l&#39;activité Live. Il doit être conforme à la `Codable` et à la `Hashable`.

* `LiveActivityOrigin` énumération spécifie si une activité a été initiée localement dans l’application ou à distance par le biais d’une notification push-to-start, prise en charge dans iOS 17.2 et versions ultérieures. Cette valeur permet au SDK de faire la distinction entre les activités en direct déclenchées localement et celles déclenchées à distance lors de la collecte de données.

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
     
    /// Unique identifier for individual Live activities
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activities
    public init(liveActivityID: String)   // For individual Live activities
}
```

Vous pouvez également enregistrer plusieurs types d’activités dynamiques pour votre application :

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Étape 3 : enregistrement des activités en direct {#register}

Enregistrez vos types d’activités dynamiques dans votre `AppDelegate` après l’initialisation de SDK. Vous pouvez ainsi :

* Active la collecte automatique des jetons push-to-start (iOS 17.2+)
* Collecte automatiquement les jetons de mise à jour des activités dynamiques
* Permet la gestion du cycle de vie et le suivi des événements

**Exemple pour une diffusion alimentaire Activité en direct :**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Étape 4 : créer des widgets d’activité en direct {#widgets}

Les activités en direct s’affichent par le biais de widgets. Vous devez créer un lot de widgets et une configuration :

**Exemple pour une diffusion alimentaire Activité en direct :**

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

## Étape 5 : démarrer une activité Live localement (facultatif) {#local}

Bien que Journey Optimizer puisse démarrer à distance des activités dynamiques, vous pouvez également les démarrer localement :

**Exemple pour une diffusion alimentaire Activité en direct :**

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

## Étape 6 : ajouter la prise en charge du débogage (facultatif) {#debug}

Si nécessaire, vous pouvez déboguer les schémas d’activité en direct dans Adobe Assurance :

**Exemple pour une diffusion alimentaire Activité en direct :**

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


