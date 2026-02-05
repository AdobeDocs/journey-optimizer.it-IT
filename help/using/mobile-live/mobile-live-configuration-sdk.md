---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale dell’attività live
description: Scopri come configurare l’integrazione di Adobe Experience Platform Mobile SDK
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 6%

---


# Integrazione dell’attività live con Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}

>[!BEGINSHADEBOX]

* [Introduzione alle attività live](get-started-mobile-live.md)
* [Configurazione dell’attività live](mobile-live-configuration.md)
* Integrazione di **[Attività live con Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**
* [Creare un’attività live](create-mobile-live.md)
* [Domande frequenti](mobile-live-faq.md)
* [Rapporto campagna attività live](../reports/campaign-global-report-cja-activity.md)


>[!ENDSHADEBOX]

Adobe Experience Platform Mobile SDK fornisce supporto integrato per le attività Live di Apple. Questo consente all’app di visualizzare aggiornamenti dinamici in tempo reale direttamente sullo schermo di blocco e su Dynamic Island senza aprire l’app.

1. [Importa moduli richiesti](#import)

   Importare i seguenti moduli: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

1. [Definisci attributi](#attributes)

   Conforme a `LiveActivityAttributes`, includi `LiveActivityData` e gli attributi `ContentState`.

1. [Registra attività live](#register)

   Utilizzare `Messaging.registerLiveActivity()` dopo l&#39;inizializzazione di SDK.

1. [Crea configurazione widget](#widget)

   Implementare `ActivityConfiguration` sia per l&#39;interfaccia schermata di blocco che per l&#39;interfaccia dell&#39;isola dinamica.

1. [Avviare un’attività Live localmente (facoltativo)](#local)

   Le attività live possono essere avviate in remoto tramite Journey Optimizer o in locale all’interno del codice dell’applicazione.

1. [Aggiunta del supporto per il debug (facoltativo)](#debug)

   Implementare `LiveActivityAssuranceDebuggable` per Assurance.

Verifica che siano installate le seguenti versioni minime per garantire la corretta configurazione e compatibilità.

>[!BEGINSHADEBOX]

**Prerequisiti:**

* **iOS:**
   * **iOS16.1 o versione successiva**: funzionalità di base delle attività live
   * **iOS 17.2+**: supporto push-to-start
   * **iOS 18+**: supporto canale di trasmissione
* **Xcode:** 14.0 o versione successiva
* **Swift:** versione 5.7 o successiva
* **Dipendenze:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## Passaggio 1: importare i moduli richiesti {#import}

Per iniziare, è innanzitutto necessario importare i seguenti moduli: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Passaggio 2: definire gli attributi dell’attività live {#attributes}

Creare uno struct conforme al protocollo `LiveActivityAttributes`. Questo definisce sia i dati statici che lo stato del contenuto dinamico per la tua attività Live.

I componenti chiave includono:

* **`liveActivityData`** (obbligatorio) che contiene dati specifici di Adobe Experience Platform.
   * Per singoli utenti: utilizzare `LiveActivityData(liveActivityID: "unique-id")`
   * Per la trasmissione: utilizzare `LiveActivityData(channelID: "channel-id")`

* Attributi statici, proprietà personalizzate specifiche del caso d&#39;uso, ad esempio `restaurantName`.

* **`ContentState`** che definisce i dati dinamici che possono essere aggiornati durante il ciclo di vita dell&#39;attività Live. Deve essere conforme a `Codable` e `Hashable`.

* L&#39;enumerazione `LiveActivityOrigin` specifica se un&#39;attività è stata avviata localmente all&#39;interno dell&#39;app o in remoto tramite una notifica push-to-start, supportata in iOS 17.2 e versioni successive. Questo valore consente a SDK di distinguere tra attività Live avviate localmente e attivate in remoto durante la raccolta dei dati.

**Esempi**

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

Puoi anche registrare più tipi di attività Live per la tua app:

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Passaggio 3: registrare le attività live {#register}

Registra i tipi di attività Live in `AppDelegate` dopo l&#39;inizializzazione di SDK per:

* Abilita la raccolta di token push-to-start automatica (iOS 17.2+)
* Raccoglie automaticamente i token di aggiornamento dell&#39;attività live
* Gestione del ciclo di vita e tracciamento degli eventi

**Esempio di attività Live di consegna di cibo:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Passaggio 4: creare widget di attività live {#widgets}

Le attività live vengono visualizzate tramite widget. È necessario creare un bundle e una configurazione di widget:

**Esempio di attività Live di consegna di cibo:**

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

## Passaggio 5: avviare localmente un’attività Live (facoltativo) {#local}

Journey Optimizer può avviare le attività live in remoto, ma puoi anche avviarle localmente:

**Esempio di attività Live di consegna di cibo:**

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

## Passaggio 6: aggiungere il supporto di debug (facoltativo) {#debug}

Se necessario, puoi eseguire il debug degli schemi di attività live in Adobe Assurance:

**Esempio di attività Live di consegna di cibo:**

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


