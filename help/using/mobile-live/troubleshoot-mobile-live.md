---
solution: Journey Optimizer
product: journey optimizer
title: Risolvere i problemi delle attività live
description: Scopri come risolvere i problemi relativi alle attività live in Journey Optimizer per i casi d’uso sia unitari che broadcast, compresi i problemi dei token di profilo, la configurazione della campagna e gli errori di consegna
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
feature_v2: id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909id: ed2fba79-65cb-4680-96d2-2ad5d851714d
source-git-commit: 8d7aea9c58b0f7622f3b11c21db55536ffe1cb66
workflow-type: tm+mt
source-wordcount: 5964
ht-degree: 1%

---

# Risolvere i problemi delle attività live {#troubleshoot-mobile-live}

>[!BEGINSHADEBOX]

**In questa pagina:** esegui una diagnosi sistematica del motivo per cui le attività Live non vengono visualizzate, aggiornate o terminate, in modo da poter risolvere i problemi relativi al token di profilo, alla configurazione della campagna, al payload e alla consegna sia nei casi di utilizzo unitari che in quelli di trasmissione.

>[!ENDSHADEBOX]

Le attività live in Adobe Journey Optimizer consentono aggiornamenti dinamici in tempo reale su schermi di blocco iOS e Isole dinamiche. Possono essere attivati e gestiti solo tramite Campagne attivate da API.

**Tipi di casi d&#39;uso:**

* **Unitario**: con targeting individuale, transazionale (campagne transazionali attivate da API)
* **Trasmissione**: recapito di massa mirato al pubblico (campagne di marketing attivate da API)

Una sfida frequente con le attività Live si verifica quando la chiamata API per attivare o aggiornare un&#39;attività Live restituisce una **risposta corretta (200 OK)**, ma l&#39;attività Live non viene visualizzata o aggiornata sul dispositivo dell&#39;utente. Questa disconnessione tra la conferma API e il comportamento effettivo del dispositivo può verificarsi in più punti della pipeline di consegna. Questa guida fornisce un approccio sistematico alla risoluzione dei problemi per identificare dove la consegna non riesce, esaminando ogni fase dalla convalida delle richieste API fino al rendering del dispositivo.

## Problemi più comuni

| Sintomo | Caso d’uso | Vai a |
|---------|----------|-------|
| L’API restituisce 200 OK, ma l’attività Live non viene mai visualizzata sul dispositivo | Entrambi | [Scenario 1: problemi relativi al profilo o al token push](#scenario-1-profile-or-push-token-issues) |
| L’attività live viene visualizzata ma non viene aggiornata né terminata | Unitario (1:1) | [Scenario 4: token di aggiornamento non sincronizzato](#scenario-4-live-activity-update-token-not-synced) |
| La campagna e i token sembrano corretti, ma la consegna non riesce | Entrambi | [Scenario 3: errori di consegna e analisi degli errori](#scenario-3-delivery-failures-and-error-analysis) |
| Configurazione del payload o struttura API non chiara | Entrambi | [Scenario 2: problemi relativi alla configurazione e al payload della campagna](#scenario-2-campaign-configuration-and-payload-issues) |
| Membri di un pubblico specifico che non ricevono la trasmissione | Trasmissione | [Scenario 7: profilo non presente nello snapshot del pubblico o non aggiornato](#scenario-7-profile-not-in-audience-or-stale-audience-snapshot) |
| È necessario confermare lo stato di esecuzione a livello di programmazione | Unitario (1:1) | [Scenario 5: controllo dello stato di esecuzione tramite API](#scenario-5-checking-execution-status-via-the-api) |
| Nessun accesso ad Assurance; è necessario il debug a livello di produzione | Entrambi | [Avanzate: debug tramite query del set di dati](#advanced-debugging-via-dataset-queries) |

## Informazioni sui due casi d’uso

Prima di eseguire il debug, conferma quale caso di utilizzo si applica alla campagna. La causa principale e il percorso di debug differiscono in modo significativo tra di essi.

| | Unitario (1:1) | Trasmissione |
|---|---|---|
| **Tipo di campagna AJO** | Transazionale attivato da API | Marketing attivato da API |
| **Targeting** | Profilo individuale tramite `recipients[].userId` | Segmento di pubblico tramite `audience.id` |
| **Token per iniziare** | Token push-to-start (per profilo) | `input-push-channel` (per istanza di trasmissione) |
| **Token da aggiornare/terminare** | Aggiorna token (per istanza di attività Live) | Uguale a `input-push-channel` come avvio |
| **Rischio di aggiornamento del pubblico** | Non applicabile | Fino a 24 ore non aggiornate (valutazione batch) |

## Glossario terminologico

| Termine | Definizione |
|------|------------|
| **Token push-to-start** | Token APNs generato da iOS 17+ che consente ad AJO di avviare in remoto un&#39;attività Live su un dispositivo senza che l&#39;app sia aperta. Registrato dal SDK mobile e memorizzato sul profilo AEP. |
| **Aggiorna token** | Token APN per istanza generato all&#39;avvio di un&#39;attività Live su un dispositivo. Obbligatorio per eventi unitari `update` e `end`. Ogni istanza di attività Live ha un proprio token di aggiornamento univoco. |
| **input-push-channel** | Un identificatore di canale univoco creato sul portale per sviluppatori di Apple per le attività di trasmissione Live. Agisce come token di aggiornamento della trasmissione. Tutti i dispositivi abbonati a questo canale ricevono gli stessi eventi di attività live. |
| **liveActivityData** | Proprietà obbligatoria nel protocollo `LiveActivityAttributes` di Adobe SDK. Per la trasmissione unitaria, contiene `liveActivityID`; per la trasmissione, contiene `channelID`. Deve essere incluso nel campo `attributes` dei payload dell&#39;evento di inizio. |
| **ID canale di trasmissione** | Il valore di `input-push-channel`. Deve corrispondere esattamente a `liveActivityData.channelID` nel payload della trasmissione. |
| **attributeType / attributes-type** | Nome dello struct Swift `ActivityAttributes`. Memorizzato come `attributeType` (camelCase) negli attributi del profilo AEP e inviato come `attributes-type` (sillabato) nei payload JSON APS. Sono lo stesso valore in rappresentazioni diverse. |
| **liveActivityPushNotificationDetails** | Attributo del profilo AEP che memorizza il token push-to-start di un dispositivo, `appId`, `platform` e `attributeType`. Deve essere presente e valido per il funzionamento dell&#39;avvio remoto. |
| **Payload APS** | La struttura JSON inviata all&#39;interno della richiesta API in `context.requestPayload.aps`. Contiene i campi evento attività live, `content-state`, `attributes` e di controllo. |
| **Assurance** | Adobe Experience Platform Assurance, uno strumento di debug in tempo reale per i dispositivi di test connessi. Non disponibile per i dispositivi degli utenti finali di produzione. |

## Prerequisiti

Prima di risolvere il problema, assicurati di disporre di:

+++ Plug-in Assurance per attività live

La vista Attività live in Adobe Experience Platform Assurance convalida la configurazione dell’app, controlla gli eventi di attività e consente di avviare, aggiornare o terminare le attività in remoto da una sessione di test.

>[!IMPORTANT]
>
> Le sessioni di Assurance sono solo per dispositivi di test e controllo qualità. I dispositivi di produzione dell’utente finale non sono collegati ad Assurance. Per la diagnostica di produzione, utilizzare la sezione [Avanzate: debug tramite query del set di dati](#advanced-debugging-via-dataset-queries) alla fine di questa guida.

### Requisiti

| Requisito | Dettagli |
|---|---|
| dispositivo iOS | Dispositivo fisico con iOS 16.1 o versione successiva |
| Simulatore Xcode | iOS 16.1 o versione successiva **solo avvio locale**, il push remoto tramite APN non è supportato nel simulatore |
| Avvio remoto da Assurance | iOS 17.1 o versione successiva, token push-to-start valido e configurazione di canale valida |
| Mobile SDK | Adobe Experience Platform Mobile SDK 5.11.0 o versione successiva |
| Session | Una sessione Assurance attiva |

### Tre schede

| Scheda | Cosa mostra |
|-----|---------------|
| **Informazioni client** | Credenziali di dispositivo, profilo e App Store. Controllo verde = configurato correttamente; avviso in linea = problema con una correzione suggerita. Viene mappato direttamente sui pre-controlli in ogni scenario sottostante. |
| **Attività** | Attività live per il client selezionato: tipo (unitario/broadcast), ID, stato e conteggio eventi. Schede secondarie: Panoramica (informazioni di base + pulsante Invia aggiornamento), Flusso di attività (timeline del ciclo di vita con payload ispezionabili), Dettagli evento (ispezione del payload completo per evento). |
| **Eventi** | Tutti gli eventi Assurance per il client, inclusi gli eventi di inizio, aggiornamento e fine dell’attività Live. |

### Avvio, aggiornamento e fine da Assurance

**Avvia attività live**. apre una finestra di dialogo per scegliere il tipo di attività registrato, scegliere Unitario o Trasmissione, immettere un ID canale di trasmissione (solo trasmissione) e modificare un payload APS JSON precompilato. Il pulsante è disattivato o restituisce un errore se i requisiti di configurazione del token push-to-start, della versione di iOS o del canale non sono soddisfatti.

**Invia aggiornamento**. dalla scheda Panoramica di un’attività esistente, invia un evento Update (push di nuovo contenuto) o End. Per l’attività unitaria, il plug-in utilizza automaticamente il token di aggiornamento dell’attività. Per la trasmissione, esegue il targeting di tutti i dispositivi abbonati allo stesso ID canale di trasmissione. I payload devono essere JSON validi e corrispondere allo schema di attributi dell’attività; in caso contrario, la richiesta viene rifiutata.

Consulta la [documentazione di Adobe Experience Platform Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home.html) per i passaggi di configurazione e connessione alla sessione.

+++

+++ Raccogliere i dettagli della campagna attivata dall’API

Passa alla campagna attivata da API in Journey Optimizer e recupera:

* Nome e ID della campagna
* Versione della campagna (se applicabile)
* Tipo di campagna: **Transazionale** (unitario) o **Marketing** (broadcast)
* Configurazione della superficie: la superficie dell’app iOS utilizzata per l’attività Live
* Tipo di attività: il nome struct `AttributeType` configurato nella campagna

+++

+++ Raccogli informazioni richiesta API

Quando effettui la chiamata API per attivare l’attività Live, salva:

* Payload della richiesta API, inclusi gli identificatori di profilo e i dati delle attività live
* Risposta API che include codice di stato, ID messaggio, ID richiesta
* Timestamp di quando è stata chiamata l’API
* Endpoint utilizzato, ad esempio `/campaign/{CAMPAIGN_ID}/execute`

+++

+++ Identificare il profilo di test

Dalla richiesta API, recupera:

* Spazio dei nomi del profilo, ad esempio ECID, e-mail, ID cliente
* ID profilo utilizzato nella chiamata API

Assicurati di poter cercare questo profilo in Adobe Experience Platform. Scopri come [cercare un profilo nella documentazione di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html).

+++

+++ Informazioni su dispositivo e app

Raccogli quanto segue dal dispositivo di prova:

* Modello del dispositivo, ad esempio iPhone 14 Pro
* Versione iOS
* Identificatore del bundle dell’app
* Token push APN
* Stato della connettività di rete al momento del test

+++

## Scenari comuni

### Scenario 1: problemi relativi al profilo o ai token push {#scenario-1-profile-or-push-token-issues}

[!BADGE Applicabile a casi di utilizzo sia unitari che broadcast]{type=Positive}

L’API restituisce HTTP 200, ma l’attività Live non viene visualizzata. Cause comuni:

* Il profilo non esiste in Adobe Experience Platform.
* Il token push di attività live non è stato sincronizzato con il profilo.
* I dettagli push dell&#39;attività live sono sincronizzati ma contengono una configurazione errata. Esempio: `appId` o `attributeType` errati.

**Nota per i casi di utilizzo relativi alla trasmissione**: se in alcuni profili del pubblico mancano token, solo tali profili non riceveranno l&#39;attività Live. Campiona diversi profili dal tuo pubblico per diagnosticare problemi di token. Questo vale solo per gli eventi di avvio remoto, non per gli eventi di aggiornamento o di fine.

#### Controlli preliminari

* Requisiti dell’app iOS:
   * iOS 16.1+
   * `NSSupportsLiveActivities` impostato su `YES` in `Info.plist`
   * `ActivityAttributes` implementato correttamente.
* Integrazione di Mobile SDK:
   * Adobe Experience Platform Mobile SDK (messaggistica SDK 5.11.0+)
   * `Messaging.registerLiveActivities` implementato e chiamato con il token push di attività Live.

#### Passaggi di debug

+++ &#x200B;1. Verifica dell&#39;esistenza del profilo in Adobe Experience Platform

1. In Journey Optimizer, passa a **Cliente** `>` **Profili**.
1. Cerca utilizzando lo spazio dei nomi e il valore di identità della richiesta API.
1. Se il profilo non viene trovato, non esiste o l’acquisizione non viene completata. Crea il profilo o attendi l’acquisizione prima di attivare l’attività Live.
1. Se il profilo viene trovato, procedi al passaggio 2 seguente per verificare se il token push è sincronizzato.

+++

+++ &#x200B;2. Controlla se il token push di attività live è sincronizzato

Puoi utilizzare Assurance per verificare la registrazione del token:

1. In Assurance, dall&#39;elenco **Eventi**, filtrare o cercare gli eventi `eventType = "liveActivity.pushToStart"`.
1. Seleziona **Evento** e controlla il payload.
1. Verifica che siano presenti i valori token, appId e attributeType.
1. Conferma se l’evento è stato inviato correttamente.

Puoi anche effettuare il check-in del profilo Adobe Experience Platform.

1. In Adobe Experience Platform, dal tuo **Profilo**, accedi alla scheda **Eventi**.
1. Cerca `liveActivity.pushToStart` eventi.
1. Controlla il timestamp e il payload pari.

Se non viene trovato alcun evento, l&#39;app mobile non chiama `Messaging.registerLiveActivity` correttamente. È necessario correggere l’integrazione di SDK.

+++

+++ &#x200B;3. Convalidare i dettagli del token sul profilo

1. Dal tuo **Profilo**, accedi alla scheda **Attributi**.
1. Individuare `liveActivityPushNotificationDetails`.
1. Verifica la configurazione del token:

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

**Convalida ogni campo:**

| Campo | Requisito | Problema comune |
|-|-|-|
| `appId` | Deve corrispondere esattamente all’identificatore del bundle di iOS | Mancata corrispondenza tra ID bundle di sviluppo/produzione |
| `attributeType` | Deve corrispondere esattamente al nome struct Swift `ActivityAttributes` (distinzione maiuscole/minuscole) | Digita o nome struct errato |
| `platform` | Deve essere `"apns"` o `"apnsSandbox"` | Valore piattaforma errato |
| `denylisted` | Deve essere `false` | Token contrassegnato come non valido o utente rifiutato |
| `token` | Token push APNs valido | Token scaduto o app reinstallata |

Se un campo non è corretto: aggiorna l&#39;app mobile, registrati di nuovo utilizzando `Messaging.registerLiveActivities`, attendi 5-10 minuti, quindi ricontrolla.

Se manca `liveActivityPushNotificationDetails`: il token non è ancora stato sincronizzato. Attendere 5-10 minuti dopo la visualizzazione dell&#39;evento `liveActivity.pushToStart` in Assurance.

+++

### Scenario 2: problemi di configurazione e payload di Campaign {#scenario-2-campaign-configuration-and-payload-issues}

[!BADGE Applicabile a casi di utilizzo sia unitari che broadcast]{type=Positive}

Il profilo esiste con token validi, ma l’attività Live non viene visualizzata. Ciò può essere causato da:

* Configurazione della superficie o del canale errata.
* Struttura del payload API errata.
* `content-state` e `attributes` non corrispondono all&#39;implementazione di iOS `ActivityAttributes`.
* `timestamp` non aggiornato (critico per aggiornamento/fine).

**Nota per i casi d&#39;uso relativi alla trasmissione**: la campagna deve essere **Marketing attivato da API** (non transazionale). Il payload utilizza `audience` invece dei singoli `profile`. Consulta [questa sezione](#broadcast-config) per la struttura del payload specifica per la trasmissione e la [documentazione di Adobe Developer](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) per informazioni sulle specifiche API complete.

#### Controlli preliminari

* La campagna è **Transazionale attivato da API** (unitaria) o **Marketing attivato da API** (broadcast) e l&#39;opzione **Alta velocità effettiva** deve essere **non** abilitata in quanto incompatibile con l&#39;attività Live.
* Assicurati che il profilo esista e che i token siano sincronizzati correttamente utilizzando lo [scenario precedente](#scenario-1-profile-or-push-token-issues).

#### Passaggi di debug

+++ &#x200B;1. Verificare la configurazione della superficie della campagna

1. In Journey Optimizer, apri **Campaign** e passa al menu **Azioni**.
1. Controlla la **configurazione attività Live**. La superficie deve essere configurata per l&#39;app iOS con un identificatore bundle che corrisponde a `appId` nel `liveActivityPushNotificationDetails` del tuo profilo. Ad esempio, se il tuo profilo ha `"appId": "com.example.myapp"`, la superficie deve avere come destinazione la stessa app.
1. Verifica che il **tipo di attività** nella configurazione della campagna corrisponda esattamente al `attributeType` nel `liveActivityPushNotificationDetails` del tuo profilo. Ad esempio, se il tuo profilo ha `"attributeType": "FoodDeliveryLiveActivityAttributes"`, la campagna deve specificare lo stesso tipo di attività.

+++

+++ &#x200B;2. Convalidare la struttura del payload API

Durante l’esecuzione della campagna tramite API, assicurati che il payload segua la struttura corretta.

**Payload unitario:**

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

**Problemi comuni relativi al payload:**

| Campo | Requisito | Problema comune |
|-|-|-|
| `attributes-type` | Deve corrispondere al profilo e al tipo di attività della campagna `attributeType` | Mancata corrispondenza o errore di battitura |
| `campaignId` | Deve corrispondere all’ID campagna attivato | ID campagna errato o mancante |
| `content-available` | Deve essere `1` | Valore mancante o errato |
| `event` | Deve essere `"start"`, `"update"` o `"end"` | Tipo di evento non valido |
| `timestamp` | Deve sempre essere il tempo dell’epoca Unix corrente/più recente in secondi | Utilizzo di timestamp vecchi/memorizzati nella cache |
| `userId` / `namespace` | Deve corrispondere a un profilo esistente in AEP | Identificatore profilo non corrispondente |

**Critico: utilizza sempre la marca temporale più recente**

* Il campo `timestamp` deve **always** essere l&#39;**ora Unix corrente** (in secondi) nel momento in cui viene effettuata ogni chiamata API.
* Questo vale per **tutti i tipi di evento**: `start`, `update` e **in particolare`end`**.
* **Impatto su aggiornamenti/richieste di fine**: l&#39;utilizzo di un timestamp non aggiornato o precedente causerà errori nelle richieste di aggiornamento e di fine o verrà ignorato dal dispositivo.
* **NOT** riutilizza i timestamp da richieste precedenti o utilizza valori memorizzati nella cache.
* Genera una nuova marca temporale per ogni chiamata API.

**Campi facoltativi (tutti i tipi di eventi):**

* `requestId`: identificatore univoco per il tracciamento (consigliato).
* `alert`: oggetto con `title` e `body` per la notifica (utile per richiamare l&#39;attenzione sugli aggiornamenti).

**Informazioni su `dismissal-date`:**

* Campo facoltativo contenente il tempo dell’epoca Unix (secondi).
* **Rilevante solo quando`event: "end"`**.
* Specifica quando l’attività Live deve essere rimossa automaticamente dal dispositivo.
* Se non viene fornito per l’evento finale, l’attività Live rimane visibile fino a quando l’utente non la chiude.
* Deve essere una marca temporale futura (successiva a `timestamp`).

+++

+++ &#x200B;3. Allineare il payload all’implementazione di iOS

Assicurati che il payload API corrisponda all&#39;implementazione `ActivityAttributes` dell&#39;app iOS. Il protocollo `LiveActivityAttributes` di Adobe SDK estende iOS `ActivityAttributes` e richiede una proprietà `liveActivityData`.

**Convalida mapping:**

1. `ActivityAttributes` deve implementare il protocollo `LiveActivityAttributes` di Adobe. Esempio:

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

   **Nota** che il campo `liveActivityData` è richiesto da Adobe SDK e deve essere incluso in tutte le implementazioni.

1. Il payload API deve rispecchiare la struttura di iOS:

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

**Elenco di controllo convalida:**

* Includi tutti i campi `ContentState` in `content-state` (obbligatorio per tutti i tipi di evento).
* Includi tutti i campi `LiveActivityAttributes` in `attributes` (solo eventi di inizio), inclusi:
   * `liveActivityData` (obbligatorio; in genere contiene `liveActivityID` o un identificatore simile)
   * Tutti i campi personalizzati dalla struttura
* Fai corrispondere esattamente i nomi dei campi (distinzione maiuscole/minuscole).
* Tipi di dati corrispondenti (String, Int, Bool, oggetti nidificati).
* Mantieni struttura oggetto nidificata.

**Errori comuni:**

| Problema | Impatto | Correggi |
|-------|--------|-----|
| `liveActivityData` mancante negli attributi | L’attività live non verrà avviata | Includi sempre l&#39;oggetto `liveActivityData` nell&#39;evento di avvio |
| Campo richiesto mancante nell’evento di avvio | L’attività live non verrà avviata | Aggiungi tutti i campi da iOS struct |
| Nome campo errato (errore di battitura/maiuscole/minuscole) | Campo ignorato o errore di analisi | Corrispondenza esatta dei nomi dei campi di iOS |
| Tipo di dati errato | Errore di analisi | Corrispondenza con i tipi di dati di iOS |
| Oggetto nidificato mancante | Dati incompleti | Includi tutte le strutture nidificate |
| Inclusione di `attributes` in aggiornamento/fine | Non necessario, ma generalmente ignorato | Includi solo `attributes` nell&#39;evento di inizio |
| Timestamp non aggiornato al momento dell’aggiornamento/della fine | Aggiornamento/fine ignorato dal dispositivo | Genera sempre una nuova marca temporale |

Per ulteriori esempi, consulta [Crea pagina di attività Live](create-mobile-live.md).

+++

+++ &#x200B;4. Test con Assurance

Verifica dell’esecuzione dell’API e della consegna del payload tramite Assurance:

1. Apri la sessione di Assurance.
1. Esegui la chiamata API per attivare l&#39;attività Live.
1. Nell&#39;**Elenco eventi**, verificare che:
   * Eventi di esecuzione della campagna.
   * Eventi di consegna di attività live.
   * Eventi di errore di convalida del payload.
1. Esamina i payload degli eventi per verificare:
   * Il payload è stato elaborato correttamente.
   * Non si sono verificati errori di convalida.
   * L’attività live è stata inviata ai numeri APN.

+++

### Scenario 3: errori di consegna e analisi degli errori {#scenario-3-delivery-failures-and-error-analysis}

[!BADGE Applicabile a casi di utilizzo sia unitari che broadcast]{type=Positive}

In questo scenario, tutti i controlli precedenti sono stati superati:

* Il profilo esiste con [token di push attività live validi](#scenario-1-profile-or-push-token-issues)
* Campaign è [configurato correttamente con payload corretto](#scenario-2-campaign-configuration-and-payload-issues)
* [I token di aggiornamento sono sincronizzati](#scenario-4-live-activity-update-token-not-synced) (solo per eventi di aggiornamento/fine, caso d&#39;uso unitario)

Tuttavia, l’attività Live non viene ancora visualizzata, aggiornata o terminata come previsto. Il problema può verificarsi a livello di sistema di consegna Adobe o con il provider di servizi di notifica push (APN).

**Nota per i casi di utilizzo relativi alla trasmissione**: i report mostrano metriche per tutti i membri del pubblico. Alcuni profili possono avere esito positivo, mentre altri hanno esito negativo.

**Controlli preliminari**

* **Scenari precedenti convalidati:**
   * Il profilo esiste con `liveActivityPushNotificationDetails` corretto
   * La superficie della campagna e il tipo di attività sono corretti
   * Il payload API è valido con la marca temporale corrente
   * I token di aggiornamento sono sincronizzati (per eventi di aggiornamento/fine)

* **Chiamata API confermata:**

   * La chiamata API ha restituito HTTP 200 (operazione riuscita)
   * L’ID della campagna e i dettagli del destinatario sono corretti

#### Passaggi di debug

+++ &#x200B;1. Controllare i rapporti delle campagne

1. Passa alla **campagna attività live**.
1. Fai clic sul pulsante **Rapporti**.
1. Selezionare **Visualizza report completo**.
1. Consulta le sezioni seguenti:

   1. Controlla le metriche **Statistiche di invio** per comprendere il successo della consegna:

      | Metrica | Che cosa significa | Cosa cercare |
      |-|-|-|
      | Target | Numero di profili qualificati per il pubblico | Deve includere il profilo di test |
      | Invia | Totale notifiche push tentate | Deve corrispondere alle chiamate API |
      | Consegnate | Distribuito correttamente ai dispositivi | Confronta con invii per visualizzare il tasso di successo |
      | Inviare errori | Notifiche push non inviate | Numeri elevati |
      | Inviare esclusioni | Profili esclusi da Adobe Journey Optimizer | Controlla se il tuo profilo è stato escluso |

   1. Se Invia errori > 0, controllare la tabella **Motivi di errore** per i codici di errore e i messaggi specifici:

      | Errore comune | Significato | Risoluzione |
      |-|-|-|
      | Token non valido | Token push non valido o scaduto | Registra nuovamente i token di attività live dal dispositivo |
      | Token non trovato | Nessun token valido associato al profilo | Verifica che `liveActivityPushNotificationDetails` esista |
      | APN rifiutati | Il servizio di notifica push di Apple ha rifiutato il push | Verifica certificato APNs, ID bundle, ambiente |
      | Timeout di rete | Impossibile raggiungere gli APN | Problema transitorio; riprova la chiamata API |

   1. Se **Invia esclusioni** > 0, controlla la tabella **Motivi esclusi**:

      | Esclusione comune | Significato | Risoluzione |
      |-|-|-|
      | Profilo rifiutato | L’utente ha rinunciato alle notifiche | Verifica lo stato del consenso del profilo |
      | Token | Token contrassegnato come non valido | Registra di nuovo il token o controlla lo stato di inserisce nell&#39;elenco Bloccati della |
      | Profilo non idoneo | Il profilo non soddisfa i criteri della campagna | Rivedere le regole del pubblico della campagna |

Ulteriori informazioni sono disponibili nella [pagina del report della campagna di attività live](../reports/campaign-global-report-cja-activity.md).

+++

+++ &#x200B;2. Controllare gli eventi di feedback dei messaggi nel profilo

1. Passa a **Cliente** > **Profili** in Journey Optimizer.
1. Cerca e apri il profilo.
1. Selezionare la scheda **Eventi**.
1. Filtra o cerca eventi con `eventType = "message.feedback"`.
1. Cerca eventi di feedback corrispondenti al tipo `liveActivityID` e `event` della tua attività Live.
1. Esamina i seguenti campi chiave:

   | Campo | Valori possibili | Che cosa significa |
   |---|---|---|
   | `feedbackStatus` | `sent`, `error`, `denylist` | Risultato della consegna dal provider di servizi |
   | `serviceProvider` | `apns/apnsSandbox` | Deve essere un APN per le attività iOS Live |
   | `errorCode` | Codice numerico o `null` | Codice di errore specifico per APNs, se non riuscito |
   | `errorMessage` | Descrizione errore o `null` | Messaggio di errore leggibile |

1. **Se `feedbackStatus: "error"`:**
   * Controlla `errorCode` e `errorMessage` per errori APN specifici
   * Gli errori APN comuni includono token scaduto, certificato non valido, ID bundle errato

1. **Se non è stato trovato alcun evento di feedback:**
   * È possibile che la notifica push non sia stata tentata
   * Verifica se il profilo è stato escluso nei Rapporti di Campaign come descritto nel passaggio 1 precedente.

+++

+++ &#x200B;3. Verificare la consegna delle attività live ai numeri APN in Assurance

1. Apri la sessione Assurance; deve essere attiva durante la chiamata API.
1. Esegui la chiamata API (inizio, aggiornamento o fine).
1. Nell&#39;**Elenco eventi**, cerca gli eventi di consegna delle attività live.
1. Cerca gli eventi relativi alla consegna push APN.
1. Controllare la presenza dei seguenti indicatori:
   * **Invia la richiesta al servizio APN**: conferma l&#39;invio del messaggio push ai server di Apple da parte di Adobe
   * **Risposta APNs**: indica se APNs ha accettato o rifiutato il messaggio push
   * **Stato consegna**: indicazione di esito positivo o negativo
1. Se vengono rilevati problemi, consulta i seguenti problemi comuni relativi alla consegna di APN:

   | Problema | Sintomo in Assurance | Risoluzione |
   |-|-|-|
   | Certificato APNs scaduto | Errore di autenticazione | Rinnovare e caricare un nuovo certificato APN |
   | Ambiente errato (sviluppo e produzione) | Errore di mancata corrispondenza del token | Assicurati che il certificato corrisponda al tipo di build dell’app |
   | Mancata corrispondenza ID bundle | Identificatore bundle non valido | Verifica che l’ID del bundle di certificati corrisponda all’app |
   | Token scaduto | Errore InvalidToken da APNs | Registra nuovamente i token di attività live |
   | Limitazione di velocità | Troppe richieste | Ridurre la frequenza delle chiamate API |

+++

+++ &#x200B;4. Procedi a ulteriori controlli diagnostici

1. Verifica le metriche del ciclo di vita delle attività live nel rapporto della campagna.

   Nel rapporto della campagna, controlla la sezione **Ciclo di vita attività in tempo reale**:

   | Metrica | Cosa controllare |
   |-|-|
   | Avvii remoti | Deve mostrare il numero di avvii attivati da API |
   | Aggiornamenti | Deve mostrare il conteggio degli eventi di aggiornamento |
   | Termina | Deve mostrare il conteggio degli eventi finali |
   | Conteggio totali | Volume evento attività live complessivo |

   Se queste metriche sono pari a zero o non corrispondono alle chiamate API, si verifica un problema di consegna tra Adobe e APN.

1. Se Adobe mostra una consegna corretta ma il dispositivo non mostra l’attività Live:

   * Controlla i registri del dispositivo iOS per verificare la presenza di errori di attività live.
   * Verifica che l’app sia in primo piano o in background (non terminata).
   * Conferma connettività di rete per il dispositivo.
   * Esegui il test su più dispositivi per escludere problemi specifici del dispositivo.
   * Verifica che la versione di iOS sia 16.1 o successiva.

+++

+++ &#x200B;5. Escalation al supporto Adobe

Se hai completato tutti i passaggi e il problema rimane non risolto, contatta l’Assistenza clienti Adobe con:

**Informazioni richieste:**

* ID e nome della campagna
* Spazio dei nomi e ID del profilo
* `liveActivityID` dal payload API
* Marca temporale delle chiamate API
* Schermate di:
* Rapporti sulle campagne (statistiche di invio, motivi di errore, motivi di esclusione)
* Eventi profilo (`liveActivity.updateToken`, `message.feedback`)
* Sessione Assurance che mostra gli eventi di consegna
* Payload completo della richiesta API
* Dettagli del certificato APNs (scadenza, ambiente, ID bundle)

+++

## Scenari unitari specifici

### Scenario 4: token di aggiornamento dell&#39;attività live non sincronizzato {#scenario-4-live-activity-update-token-not-synced}

L&#39;attività Live viene avviata correttamente sul dispositivo, ma le successive chiamate API `update` o `end` (che restituiscono HTTP 200) non riescono ad aggiornare o chiudere l&#39;attività Live. Ciò si verifica quando il token di aggiornamento dell&#39;attività **Live** non è sincronizzato correttamente nel sistema di Adobe.

**Informazioni sui token di aggiornamento**

Quando un’attività Live viene avviata su un dispositivo, iOS genera un token di aggiornamento univoco per tale istanza di attività Live specifica. Questo token è necessario per:

* Invio di aggiornamenti all’attività Live
* Terminazione dell’attività Live in remoto

Ogni istanza di attività Live ha un proprio token di aggiornamento univoco. Adobe necessita di questo token per distribuire eventi di aggiornamento e fine.

**Comportamento previsto**

Affinché gli eventi di aggiornamento e fine funzionino, si devono verificare i seguenti eventi:

1. L’attività live viene avviata correttamente sul dispositivo.
1. Il dispositivo genera un token di aggiornamento per l’istanza dell’attività Live.
1. Mobile SDK acquisisce e invia il token di aggiornamento ad Adobe.
1. Il token di aggiornamento viene sincronizzato e memorizzato nel sistema di Adobe.
1. Le successive chiamate API per l’aggiornamento o la fine utilizzano questo token per la consegna.

**Controlli preliminari:**

* **Autorizzazione utente**: la prima volta che un&#39;attività Live viene avviata su un dispositivo, iOS visualizza un prompt di sistema: &quot;Consenti a [Nome app] di fornire aggiornamenti dell&#39;attività Live?&quot; L&#39;utente **deve toccare &quot;Consenti&quot;** per generare e sincronizzare i token di aggiornamento. Se l’utente tocca &quot;Non consentire&quot;, non vengono creati token di aggiornamento e le richieste di aggiornamento/fine non riusciranno. Si tratta di un’autorizzazione una tantum per app.
* **Convalida profilo e campagna**: completa [i controlli dello scenario 1](#scenario-1-profile-or-push-token-issues) e [dello scenario 2](#scenario-2-campaign-configuration-and-payload-issues) per verificare che la configurazione del profilo, dei token e della campagna sia corretta.

#### Passaggi di debug

+++ Verificare la sincronizzazione del token di aggiornamento in Assurance

1. Apri la sessione di Assurance.
1. Assicurati che la sessione sia stata attiva quando l’attività Live è stata avviata sul dispositivo.
1. Filtra o cerca eventi con `eventType = "liveActivity.updateToken"`.
1. Seleziona l’evento e controlla il payload:

   * Verificare che il campo `token` contenga una stringa token di aggiornamento valida.
   * Controlla che `liveActivityID` corrisponda alla tua istanza di attività Live.
   * Conferma che `activityType` corrisponda al tuo `attributes-type`.

1. Se l’evento non viene trovato:

   * Il token di aggiornamento non è stato generato o acquisito da SDK.
   * Controlla se l&#39;utente ha concesso le autorizzazioni per l&#39;attività live.
   * Verifica che l&#39;attività Live sia stata effettivamente avviata sul dispositivo.
   * Verifica che il SDK mobile sia correttamente integrato per acquisire i token di aggiornamento.

1. Se viene trovato un evento, procedere al passaggio 2.

+++

+++ &#x200B;2. Verificare il token di aggiornamento negli eventi del profilo

1. Passa a **Cliente** > **Profili** in Journey Optimizer.
1. Cerca e apri il profilo.
1. Selezionare la scheda **Eventi**.
1. Cerca `liveActivity.updateToken` eventi.
1. Controlla i dettagli dell’evento:

   * Verifica che il timestamp sia recente (corrisponde all’avvio dell’attività Live).
   * Verificare che `token` e `liveActivityID` siano presenti.
   * Verificare che `activityType` sia corretto.

1. Se l’evento non viene trovato nel profilo:

   * L’evento del token di aggiornamento potrebbe non essere ancora stato acquisito nel profilo.
   * Attendere 5-10 minuti e ricontrollare.
   * Se manca ancora dopo 15 minuti, potrebbe esserci un problema di acquisizione dell’evento.

1. Se viene trovato un evento, il token di aggiornamento è stato sincronizzato. Procedere al passaggio 3.

+++

+++ &#x200B;3. Controllare gli eventi di consegna delle attività live in Assurance

1. Nella sessione di Assurance, esegui una chiamata API di aggiornamento o di fine.
1. Nell&#39;**Elenco eventi**, cerca eventi di consegna attività live (eventi push APN).
1. Verifica la presenza di eventi che indicano:
   * Notifica push inviata ai numeri APN.
   * Risposta da APN (riuscita o errore).
   * Conferma della consegna.
1. Se è presente un evento di consegna APN: è stata inviata la notifica push. Se il dispositivo non viene ancora aggiornato, il problema potrebbe essere sul lato dispositivo (app che non gestisce il push, problemi di rete, ecc.).
1. Se manca l’evento di consegna APN: il token di aggiornamento potrebbe non essere memorizzato correttamente o associato al profilo nel sistema di Adobe.
1. Se sono presenti eventi di errore: controlla i dettagli dell’errore per specifici motivi di errore (token non valido, APN rifiutati, ecc.).

+++

### Scenario 5: controllo dello stato di esecuzione tramite l’API {#scenario-5-checking-execution-status-via-the-api}

[!BADGE Si applica solo ai casi d&#39;uso unitari (1:1)]{type=Informative}

Dopo aver attivato un&#39;attività Live unitaria, l&#39;**API di esecuzione dei messaggi GET** restituisce lo stato corrente dell&#39;esecuzione. Utilizzala per confermare se un’esecuzione è in coda, in corso, completata o non riuscita, senza attendere che l’evento di feedback arrivi al set di dati.

`executionId` è l&#39;ID del messaggio restituito nella risposta del trigger. Per le esecuzioni unitarie, ha il prefisso `HUOC-`.

#### Richiesta endpoint e esempio

**Endpoint**: `GET https://cjm.adobe.io/imp/message/executions/{executionId}`

```bash
curl --location 'https://cjm.adobe.io/imp/message/executions/HUOC-123456' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
  --header 'Authorization: Bearer <ACCESS_TOKEN>' \
  --header 'x-sandbox-name: <SANDBOX_NAME>' \
  --header 'x-sandbox-id: <SANDBOX_UUID>' \
  --header 'x-api-key: <API_KEY>'
```

#### Codici di risposta HTTP

| Codice | Significato |
|------|---------|
| 200 OK | Esecuzione trovata e restituita correttamente |
| 401 Non autorizzato | Token Bearer mancante o non valido |
| 403 - Non consentito | Token valido ma autorizzazioni insufficienti |
| 404 Non trovato | L’ID di esecuzione non esiste |

#### Valori dello stato di esecuzione

Il campo `status` in una risposta 200 indica lo stato di avanzamento dell&#39;esecuzione:

| Stato | Descrizione |
|--------|-------------|
| `PENDING` | Esecuzione in coda ma non ancora avviata |
| `INPROGRESS` | Esecuzione in fase di elaborazione |
| `COMPLETED` | Esecuzione completata |
| `FAILED` | L’esecuzione ha riscontrato un errore |

La risposta 200 restituisce anche `executionType` (`unitary` o `batch`), `executionRunMode` (`default` o `test`) e un blocco `source` con metadati (`campaignId`, `journeyId`, `batchInstanceId`, informazioni risorsa) che lega l&#39;esecuzione alla campagna o al percorso di attivazione.

## Scenari specifici per la trasmissione

### Scenario 6: problemi relativi alla configurazione e al payload della campagna di trasmissione{#broadcast-config}

[!BADGE Si applica solo ai casi d&#39;uso di trasmissione]{type=Informative}

Questa sezione descrive gli scenari di risoluzione dei problemi specifici per le attività di trasmissione Live, che richiedono approcci di debug diversi rispetto alle campagne unitarie.

Quando i profili hanno token validi ma l’attività Live non viene visualizzata, aggiornata o si comporta come previsto per i membri del pubblico, il problema in genere deriva da uno dei seguenti elementi:

* La campagna non è configurata come marketing attivato da API.
* Il payload API utilizza una struttura di trasmissione non corretta (mancano `audience` o `input-push-channel`).
* I campi `content-state` e `attributes` non corrispondono all&#39;implementazione di iOS `ActivityAttributes`.
* `input-push-channel` non è stato creato correttamente nel portale per sviluppatori di Apple.

Questo scenario di risoluzione dei problemi si applica a tutti gli eventi di attività Live nelle campagne di trasmissione: `start`, `update` e `end`.

**Controlli preliminari:**

* **Tipo di campagna**:
   * Verifica che la campagna sia creata come Marketing attivato da API (necessario per campagne broadcast/basate su pubblico).
   * Conferma che un pubblico sia definito nella configurazione della campagna.
* **Convalida profilo e token**: prova più profili dal pubblico per verificare che dispongano di `liveActivityPushNotificationDetails` validi. Per i passaggi di convalida dettagliati, segui [Scenario 1](#scenario-1-profile-or-push-token-issues).

#### Passaggi di debug

+++ &#x200B;1. Verificare la configurazione del pubblico della campagna

1. Apri la **campagna di marketing con attivazione API** in Journey Optimizer.
1. Passa alla sezione **Pubblico** e verifica:
   * Per la campagna viene selezionato un pubblico.
   * L’ID del pubblico corrisponde a quello utilizzato nel payload API.
   * Il pubblico contiene i profili previsti.
1. Passa alla sezione **Azioni**.
1. Controlla la **configurazione attività in tempo reale**:
   * La configurazione deve essere impostata per l’app iOS con l’identificatore del bundle corretto.
   * Il tipo di attività deve corrispondere a `attributes-type` nel payload API. Ad esempio, se il payload contiene `"attributes-type": "AirplaneTrackingAttributes"`, la campagna deve specificare lo stesso tipo di attività.

+++

+++ &#x200B;2. Convalidare la struttura del payload dell’API di trasmissione

La struttura del payload della trasmissione è diversa dalle campagne unitarie. Verifica che il payload segua il formato di trasmissione corretto.

**Campi obbligatori per la trasmissione:**

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

**Problemi comuni relativi al payload:**

| Campo | Requisito | Problema comune |
|-|-|-|
| `campaignId` | Deve corrispondere all’ID campagna di marketing attivato | ID campagna errato o utilizzo di una campagna transazionale |
| `audience.id` | Deve corrispondere a un pubblico esistente in AEP | L’ID o il pubblico errato non esiste |
| `input-push-channel` | Obbligatorio per la trasmissione: identificatore univoco per questa istanza di trasmissione | Manca o non corrisponde a `channelID` in `liveActivityData` |
| `timestamp` | Deve sempre essere il tempo dell’epoca Unix corrente/più recente in secondi | Utilizzo di timestamp vecchi/memorizzati nella cache |
| `event` | Deve essere `"start"`, `"update"` o `"end"` | Tipo di evento non valido |
| `attributes-type` | Deve corrispondere al tipo di attività della campagna | Mancata corrispondenza o errore di battitura |
| `content-available` | Deve essere `1` | Valore mancante o errato |

**Campi critici specifici per la trasmissione:**

* **`input-push-channel`**:
   * Obbligatorio per tutte le attività di trasmissione in diretta.
   * Funge da identificatore univoco per questa istanza di broadcast specifica.
   * Tutti i profili del pubblico ricevono attività live collegate a questo canale.
   * Deve corrispondere a `channelID` in `liveActivityData.channelID` (vedere il passaggio 3).
   * Deve essere creato per `appID` sul portale Apple Developer dal client.
   * Solo i canali creati per l&#39;elemento `appID` specifico possono essere utilizzati per trasmettere le attività Live su tale app.

* **`audience.id`**:
   * Deve fare riferimento a un segmento di pubblico valido creato in Adobe Experience Platform.
   * Tutti i profili in questo pubblico sono destinati all’attività Live.
   * Il pubblico deve essere attivato e contenere profili con `liveActivityPushNotificationDetails` validi.

**Usa sempre la marca temporale più recente:**

* Il campo `timestamp` deve essere sempre l&#39;ora Unix corrente (in secondi) per ogni chiamata API.
* Questo requisito si applica a tutti i tipi di evento: `start`, `update` e `end`.
* **Critico per aggiornamenti/fine**: l&#39;utilizzo di marche temporali non aggiornate causa errori nelle richieste di aggiornamento e fine.
* Genera una nuova marca temporale per ogni chiamata API di trasmissione.

**Campi facoltativi:**

* `dismissal-date`: tempo epoca Unix per il licenziamento automatico (pertinente solo per eventi `end`)
* `alert`: oggetto con `title` e `body` per la notifica

Per informazioni sulle specifiche API complete, consulta la [documentazione API di messaggistica Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/messaging).

+++

+++ &#x200B;3. Allinea lo stato dei contenuti, gli attributi e il canale di input-push con l’implementazione di iOS

Assicurati che i campi del payload corrispondano all&#39;implementazione `ActivityAttributes` dell&#39;app iOS e che `input-push-channel` corrisponda a `channelID` in `liveActivityData`.

1. Rivedi la definizione degli Attributi di attività di iOS.

Lo struct `ActivityAttributes` personalizzato deve implementare il protocollo `LiveActivityAttributes` di Adobe:

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

1. Mappa i campi di iOS sul payload API della trasmissione.

Per tutti gli eventi, includere `attributes` e `content-state`:

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

**Critico: `input-push-channel` deve corrispondere a`channelID`**

* Il valore `input-push-channel` nella radice di `aps` deve corrispondere esattamente a `channelID` in `liveActivityData`.
* Nell&#39;esempio precedente, entrambi i valori sono `"FEt0NgvLEfEAAOqA6AXdIQ=="`.
* Questa corrispondenza collega l’istanza di trasmissione ai dati dell’attività Live.
* Una mancata corrispondenza causa errori di consegna.

**Punti di convalida chiave:**

* Includi tutti i campi `ContentState` in `content-state` per tutti i tipi di evento.
* Includi tutti i campi `LiveActivityAttributes` personalizzati in `attributes` solo per gli eventi di inizio.
* Per gli eventi di inizio, `liveActivityData.channelID` deve corrispondere a `input-push-channel`.
* I nomi dei campi fanno distinzione tra maiuscole e minuscole e devono corrispondere esattamente.
* I tipi di dati devono corrispondere (String, Int, Bool, oggetti nidificati, ecc.).
* Per gli eventi di aggiornamento/fine, utilizzare lo stesso `input-push-channel` dell&#39;evento iniziale originale.

**Errori comuni:**

| Problema | Impatto | Correggi |
|-|-|-|
| Manca `input-push-channel` | La trasmissione non funzionerà | Aggiungi un ID canale univoco per ogni trasmissione |
| `input-push-channel` non corrisponde a `channelID` | L’attività live non verrà avviata | Assicurati che entrambi i valori siano identici |
| `input-push-channel` diverso per aggiornamento/fine | Update/end non raggiungerà le attività live | Usa lo stesso ID canale per tutto il ciclo di vita |
| Manca `liveActivityData.channelID` | L&#39;attività live non verrà collegata alla trasmissione | Includi `channelID` negli attributi per l&#39;evento di inizio |
| Campo richiesto mancante nell’evento di avvio | L’attività live non verrà avviata | Aggiungi tutti i campi da iOS struct |
| Nome campo errato (errore di battitura/maiuscole/minuscole) | Campo ignorato o errore di analisi | Corrispondenza esatta dei nomi dei campi di iOS |
| Timestamp non aggiornato al momento dell’aggiornamento/della fine | Aggiornamento/fine ignorato dai dispositivi | Genera sempre una nuova marca temporale |

+++

+++ &#x200B;4. Test con Assurance

Verifica dell’esecuzione dell’API e della consegna del payload tramite Assurance:

1. Apri la sessione di Assurance su un dispositivo di prova che fa parte del pubblico.
1. Esegui la chiamata API di trasmissione.
1. Nell&#39;**Elenco eventi** cercare:
   * Eventi di esecuzione della campagna.
   * Eventi di consegna di attività live.
   * Eventi di errore che indicano errori di convalida del payload.
1. Ispeziona i payload degli eventi per confermare:
   * Il payload è stato elaborato correttamente.
   * `input-push-channel` è presente.
   * Non si sono verificati errori di convalida.
   * Le attività live sono state inviate ai numeri APN per i membri del pubblico.

+++

### Scenario 7: profilo non presente nello snapshot del pubblico o non aggiornato {#scenario-7-profile-not-in-audience-or-stale-audience-snapshot}

In questo scenario, la campagna e il payload sono configurati correttamente, ma profili specifici non ricevono l’attività Live. Ciò si verifica in genere quando:

* Il profilo non è un membro del pubblico collegato alla campagna.
* Il pubblico è un pubblico batch e contiene un’istantanea obsoleta dei dati di profilo.
* I token di attività Live del profilo sono stati aggiunti di recente, ma non sono ancora stati riflessi nello snapshot del pubblico.

Questo scenario di risoluzione dei problemi si applica in modo specifico alle campagne di trasmissione che utilizzano un targeting basato sul pubblico.

**Informazioni sulla valutazione del pubblico**

Adobe Experience Platform utilizza diversi metodi di valutazione del pubblico che determinano quando gli aggiornamenti del profilo vengono rispecchiati nel pubblico:

| Metodo | Frequenza di valutazione | Aggiornamento dei dati | Ideale per |
|-|-|-|--|
| Batch | Una volta al giorno (pianificato) | Può essere non aggiornato fino a 24 ore | Pubblico numeroso, senza distinzione temporale |
| Streaming | In tempo reale (in caso di modifiche al profilo) | Profilo aggiornato quasi in tempo reale | Sensibile al tempo, richiede aggiornamenti del profilo |

**Controlli preliminari:**

* **Convalida campagna e payload**:
   * Completa i controlli in [questo scenario](#broadcast-config) per verificare che la campagna e il payload siano corretti.
   * Verifica che `audience.id` nel payload API corrisponda alla configurazione della campagna.
* **Profilo esistente**: verificare che il profilo esista in AEP con `liveActivityPushNotificationDetails` valido.

#### Passaggi di debug

+++ &#x200B;1. Verifica che il profilo sia nel pubblico

In primo luogo, conferma se il profilo che deve ricevere l’attività Live fa effettivamente parte del pubblico.

1. Passa a **Tipi di pubblico** in Adobe Experience Platform.
1. Cerca e apri il pubblico utilizzando `audience.id` della tua campagna.
1. Fai clic su **Sfoglia** o **Profili campione** per visualizzare i membri del pubblico.
1. Cerca il profilo di test utilizzando lo spazio dei nomi e il valore di identità.
1. **Se il profilo non è stato trovato nel pubblico:**
   * Il profilo non soddisfa i criteri di pubblico o le regole dei segmenti.
   * Rivedi la definizione del pubblico per comprendere i requisiti di iscrizione.
   * Aggiorna i dati del profilo o la definizione del pubblico per includere il profilo.
   * Attendi il completamento della valutazione del pubblico (vedi il passaggio 2).
1. **Se il profilo viene trovato nel pubblico:** Procedi al passaggio 2 per verificare l&#39;aggiornamento dei dati.

+++

+++ &#x200B;2. Controllare il tipo e la pianificazione di valutazione del pubblico

Identifica se il pubblico utilizza la valutazione in batch o in streaming, in quanto questa determina l’aggiornamento dei dati.

1. Nella pagina **Dettagli pubblico**, controlla il **Metodo di valutazione**:
   * **Batch**: valutato una volta al giorno secondo una pianificazione.
   * **Streaming**: valutato in tempo reale quando si verificano aggiornamenti del profilo.
   * **Edge**: valutato in tempo reale nelle posizioni edge.

Segui i passaggi appropriati per la risoluzione dei problemi in base al metodo di valutazione:

**Se il pubblico utilizza la valutazione batch:**

1. **Comprendere le limitazioni del pubblico batch:**
   * I tipi di pubblico in batch vengono valutati una volta al giorno (in genere durante la notte).
   * Lo snapshot del pubblico può risalire a un massimo di 24 ore.
   * Se un profilo ha registrato di recente token di attività Live, è possibile che tali token non siano presenti nell’istantanea corrente.
   * Gli aggiornamenti ai profili verranno rispecchiati solo nella successiva valutazione batch.

1. **Controlla quando si è verificata l&#39;ultima valutazione:**
   * Nei dettagli del pubblico, cerca il timestamp **Ultima valutazione**.
   * Se `liveActivityPushNotificationDetails` del profilo è stato aggiornato dopo questa marca temporale, il pubblico contiene dati non aggiornati.

1. **Risolvi dati non aggiornati:**
   1. **Opzione 1: attesa della valutazione batch pianificata**
      * La successiva valutazione batch includerà i dati di profilo aggiornati.
      * Questo accade automaticamente una volta al giorno.
      * Consigliato per scenari non urgenti.

   1. **Opzione 2: attivare la valutazione del pubblico su richiesta**
      1. Passa a **Tipi di pubblico** in AEP.
      1. Seleziona il pubblico.
      1. Fai clic su **Valuta ora** o **Attiva su richiesta**.
      1. Attendi il completamento della valutazione (l’operazione può richiedere da diversi minuti ad ore, a seconda delle dimensioni del pubblico).
      1. Verifica che il profilo disponga ora di dati aggiornati nello snapshot del pubblico.
      1. Riprova la chiamata API di trasmissione.

**Se il pubblico utilizza la valutazione in streaming:**

1. **Comprendere il comportamento del pubblico in streaming:**
   * I tipi di pubblico in streaming valutano in tempo reale quando si verificano aggiornamenti del profilo.
   * **Nuovi profili**: dopo la creazione, puoi qualificarti se soddisfano i criteri del segmento.
   * **Profili aggiornati**: dopo l&#39;aggiornamento è possibile qualificarsi o annullare la qualifica.
   * **Profili non modificati esistenti**: non vengono rivalutati a meno che non si verifichi un aggiornamento.

1. **Identificare il problema:**
   * Se un profilo esiste già e soddisfa i criteri del segmento, ma non si verifica alcun aggiornamento su tale profilo, potrebbe non essere aggiunto a un pubblico in streaming appena creato.
   * Il profilo deve ricevere un aggiornamento (qualsiasi modifica all’attributo) per attivare la rivalutazione.

1. **Risolvi il problema:**
   * **Per i nuovi profili**: sono qualificati automaticamente se i criteri sono soddisfatti. Non è necessaria alcuna azione.
   * **Per i profili esistenti senza aggiornamenti recenti:**
      * Effettua un aggiornamento minore al profilo (ad esempio, aggiorna un campo timestamp).
      * Questo attiva la valutazione in streaming e aggiunge il profilo al pubblico.
      * Alternativa: utilizza un pubblico batch o Edge per i profili esistenti.

+++

## Avanzate: debug tramite query di set di dati {#advanced-debugging-via-dataset-queries}

>[!BEGINSHADEBOX]

**Pubblico**: sviluppatori e data engineer. Richiede l’accesso SQL ai set di dati di Journey Optimizer tramite Adobe Experience Platform Query Service.

**Quando utilizzare**: Assurance è limitato ai dispositivi di prova connessi durante una sessione attiva. Utilizza le query sui set di dati per esaminare i problemi segnalati dagli utenti finali di produzione o per controllare la cronologia delle consegne dopo il fatto. Il set di dati espone le stesse informazioni sul ciclo di vita e sugli errori del plug-in Assurance.

>[!ENDSHADEBOX]

### Individuazione del set di dati

1. In Journey Optimizer passa a **Gestione dati** `>` **Set di dati**.

1. Attiva l&#39;interruttore **Mostra set di dati di sistema** e apri **Set di dati evento feedback messaggi di AJO**.

Osserva il nome esatto della tabella mostrato nella pagina dei dettagli. Nelle query seguenti viene utilizzato `ajo_message_feedback_event_dataset`, sostituirlo con il nome effettivo della tabella, se diverso.

### Query per ID attività live

Usa questa opzione quando conosci l’ID attività live (ad esempio, un UUID di ordine o di tracciamento della spedizione) e vuoi che ogni evento di feedback sia associato ad esso durante l’intero ciclo di vita.

```sql
SELECT
  timestamp,
  identitymap,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.feedbackStatus AS status,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.messageFailure.reason AS failure_reason,
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.event AS la_event,
  _experience.customerJourneyManagement
    .messageExecution.campaignID AS campaign_id,
  _experience.customerJourneyManagement
    .messageExecution.batchInstanceID AS batch_id,
  _id
FROM ajo_message_feedback_event_dataset
WHERE
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.liveActivityID
    = '<YOUR_LIVE_ACTIVITY_ID>'
  AND eventtype = 'message.feedback'
ORDER BY timestamp ASC
```

### Query eseguita da ECID

Utilizzalo quando è noto l’ECID del profilo interessato. Sostituisci `<YOUR_ECID>` con il valore ECID recuperato dal profilo.

```sql
SELECT
  timestamp,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.feedbackStatus AS status,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.messageFailure.reason AS failure_reason,
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.event AS la_event,
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.liveActivityID AS la_id,
  _experience.customerJourneyManagement
    .messageExecution.campaignID AS campaign_id,
  _id
FROM ajo_message_feedback_event_dataset
WHERE
  identityMap['ECID'][0].id = '<YOUR_ECID>'
  AND eventtype = 'message.feedback'
ORDER BY timestamp ASC
```

>[!NOTE]
>
> `identityMap` è un tipo MAP strutturato, non una stringa. Utilizza la sintassi della funzione di accesso array e struct mostrata sopra. Le funzioni stringa come `LIKE` restituiranno un errore `DATATYPE_MISMATCH`.
>
></br>
&gt; Il set di dati dell’evento Feedback messaggio memorizza solo ECID nella sua "identityMap". Se il profilo interessato è identificato da uno spazio dei nomi personalizzato anziché da ECID, devi prima risolvere l’ECID: passa a **Profiles** in AEP, cerca il profilo utilizzando lo spazio dei nomi e il valore di identità personalizzati, e recupera l’ECID dai dettagli di identità del profilo. Utilizza quel valore ECID nella query precedente.

### valori feedbackStatus

| Elemento “value” | Significato |
|-------|---------|
| `sent` | Consegnato ai numeri APN — non conferma il rendering del dispositivo (vedi nota sotto) |
| `error` | Errore di consegna. Controllare `failure_reason` per i dettagli |
| `exclude` | Profilo escluso prima dell’invio (token mancante, problema di consenso o regole di tipologia) |
| `delay` | Consegna ritardata; verrà eseguito un nuovo tentativo |

>[!NOTE]
>
> Per il campo `la_event`, il set di dati registra `remotestart`, non `start`, per gli eventi di consegna iniziali. Filtra di conseguenza la query per tipo di evento.

### Interpretazione dello stato inviato

Un `feedbackStatus` di `sent` conferma che Journey Optimizer ha trasmesso correttamente la notifica ai numeri APN. **not** conferma che l&#39;attività Live è stata sottoposta a rendering sul dispositivo.

iOS non fornisce callback una volta che una notifica lascia gli APN. Gli errori lato dispositivo, come una restrizione del sistema operativo, un calo di rete tra i numeri APN e il dispositivo o il raggiungimento del limite di durata dell’attività live di 8 ore, non sono osservabili dal set di dati. Se `feedbackStatus` è `sent` ma sul dispositivo non viene visualizzata alcuna attività Live, il problema si trova all&#39;esterno della pipeline di Journey Optimizer. Utilizza il plug-in Assurance o la registrazione a livello di app per diagnosticare il comportamento sul lato dispositivo.

