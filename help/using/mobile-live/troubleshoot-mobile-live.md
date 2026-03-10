---
solution: Journey Optimizer
product: journey optimizer
title: Risolvere i problemi relativi alle attività live
description: Scopri come risolvere i problemi relativi alle attività live in Journey Optimizer per casi d’uso sia unitari che broadcast, inclusi problemi di token di profilo, configurazione della campagna e errori di consegna
role: User
level: Intermediate
source-git-commit: b71dbb0e4987cfc879a7b153d5c1453d6c220bf9
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---


# Risolvere i problemi relativi alle attività live {#troubleshoot-mobile-live}

Le attività live in Adobe Journey Optimizer consentono aggiornamenti dinamici e in tempo reale sugli schermi dei lucchetti di iOS e sulle isole dinamiche. Possono essere attivati e gestiti solo tramite Campagne attivate da API.

**Tipi di casi d&#39;uso:**

* **Unitario**: con targeting individuale, transazionale (campagne transazionali attivate da API)
* **Trasmissione**: recapito di massa mirato al pubblico (campagne di marketing attivate da API)

Una sfida frequente con le attività live si verifica quando la chiamata API per attivare o aggiornare un&#39;attività live restituisce una **risposta corretta (200 OK)**, ma l&#39;attività live non viene visualizzata o aggiornata sul dispositivo dell&#39;utente. Questa disconnessione tra la conferma API e il comportamento effettivo del dispositivo può verificarsi in più punti della pipeline di consegna. Questa guida fornisce un approccio sistematico alla risoluzione dei problemi per identificare dove la consegna non riesce, esaminando ogni fase dalla convalida delle richieste API fino al rendering del dispositivo.

## Prerequisiti

Prima di risolvere il problema, assicurati di disporre di:

* &#x200B;
  +++ Configurare una sessione di Assurance

  Configura una **sessione Assurance** per acquisire eventi SDK e ispezionare la pipeline di consegna. Assurance fornisce visibilità su:

   * Richieste e risposte di Edge Network
   * Eventi di qualificazione del profilo
   * Registrazione token push
   * Eventi del ciclo di vita dell’attività live

  Scopri come configurare Assurance nella [documentazione di Adobe Experience Platform Assurance](https://experienceleague.adobe.com/it/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance).

  **Nota**: per iOS Live Activity, assicurati che l&#39;app sia in esecuzione su un dispositivo iOS fisico (iOS 16.1 o versione successiva) o su un simulatore Xcode (iOS 16.1 o versione successiva).

  +++

* &#x200B;
  +++ Raccogliere i dettagli della campagna attivata dall’API

  Passa alla campagna attivata da API in Journey Optimizer e recupera:

   * Nome campagna
   * ID campagna trovato nell’URL o nelle proprietà della campagna
   * Versione della campagna, se applicabile
   * Configurazione della superficie, superficie dell’app iOS utilizzata per l’attività live

  +++

* &#x200B;
  +++ Raccogli informazioni richiesta API

  Quando effettui la chiamata API per attivare l&#39;attività Live, salva:

   * Payload della richiesta API, inclusi gli identificatori di profilo e i dati di Live Activity
   * Risposta API che include codice di stato, ID messaggio, ID richiesta
   * Timestamp di quando è stata chiamata l’API
   * Endpoint utilizzato, ad esempio `/campaign/{CAMPAIGN_ID}/execute`

  +++

* &#x200B;
  +++ Identificare il profilo di test

  Dalla richiesta API, recupera:

   * Spazio dei nomi del profilo, ad esempio ECID, e-mail, ID cliente
   * ID profilo utilizzato nella chiamata API

  Assicurati di poter cercare questo profilo in Adobe Experience Platform. Scopri come [cercare un profilo nella documentazione di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html).

  +++

* &#x200B;
  +++ Informazioni su dispositivo e app

  Raccogli quanto segue dal dispositivo di prova:

   * Modello del dispositivo, ad esempio iPhone 14 Pro
   * Versione iOS
   * Identificatore del bundle dell’app
   * Token push APN
   * Stato della connettività di rete al momento del test

  +++

## Scenari comuni

### Problemi relativi a profili o token push {#profile-issue}

[!BADGE Applicabile a casi di utilizzo sia unitari che broadcast]{type=Positive}

L’API restituisce HTTP 200, ma l’attività live non viene visualizzata. Cause comuni:

* Il profilo non esiste in Adobe Experience Platform.
* Il token push di attività live non è stato sincronizzato con il profilo.
* I dettagli push delle attività live sono sincronizzati ma contengono una configurazione errata. Esempio: `appId` o `attributeType` errati.

**Nota per i casi di utilizzo relativi alla trasmissione**: se in alcuni profili del pubblico mancano token, solo tali profili non riceveranno l&#39;attività live. Campiona diversi profili dal tuo pubblico per diagnosticare problemi di token. Questo vale solo per gli eventi di avvio remoto, non per gli eventi di aggiornamento o di fine.

#### Controlli preliminari

* Requisiti dell’app iOS:
   * iOS 16.1+
   * `NSSupportsLiveActivities` impostato su `YES` in `Info.plist`
   * `ActivityAttributes` implementato correttamente.
* Integrazione di Mobile SDK:
   * Adobe Experience Platform Mobile SDK (messaggistica SDK 5.11.0+)
   * `Messaging.registerLiveActivities` implementato e chiamato con il token push Live Activity.

#### Passaggi di debug

1. &#x200B;
   +++ Verifica dell&#39;esistenza del profilo in Adobe Experience Platform

   1. In Journey Optimizer, passa a **Cliente** `>` **Profili**.
   1. Cerca utilizzando lo spazio dei nomi e il valore di identità della richiesta API.
   1. Se il profilo non viene trovato, non esiste o l’acquisizione non viene completata. Crea il profilo o attendi l’acquisizione prima di attivare l’attività Live.
   1. Se il profilo viene trovato, procedi al passaggio 2 seguente per verificare se il token push è sincronizzato.

      +++

1. &#x200B;
   +++ Controlla se il token push di attività live è sincronizzato

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

1. &#x200B;
   +++ Convalidare i dettagli del token sul profilo

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

### Problemi di configurazione e payload di Campaign {#payload-issues}

[!BADGE Applicabile a casi di utilizzo sia unitari che broadcast]{type=Positive}

Esiste un profilo con token validi, ma l’attività live non viene visualizzata. Ciò può essere causato da:

* Configurazione della superficie o del canale errata.
* Struttura del payload API errata.
* `content-state` e `attributes` non corrispondono all&#39;implementazione di iOS `ActivityAttributes`.
* `timestamp` non aggiornato (critico per aggiornamento/fine).

**Nota per i casi d&#39;uso relativi alla trasmissione**: la campagna deve essere **Marketing attivato da API** (non transazionale). Il payload utilizza `audience` invece dei singoli `profile`. Consulta [questa sezione](#broadcast-config) per la struttura del payload specifica per la trasmissione e la [documentazione di Adobe Developer](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) per informazioni sulle specifiche API complete.

#### Controlli preliminari

* La campagna è **Transazionale attivato da API** (unitaria) o **Marketing attivato da API** (broadcast) e l&#39;opzione **Alta velocità effettiva** deve essere **non** abilitata in quanto incompatibile con Live Activity.
* Assicurati che il profilo esista e che i token siano sincronizzati correttamente utilizzando lo [scenario precedente](#profile-issue).

#### Passaggi di debug

1. &#x200B;
   +++ Verificare la configurazione della superficie della campagna

   1. In Journey Optimizer, apri **Campaign** e passa al menu **Azioni**.
   1. Controlla la **configurazione attività Live**. La superficie deve essere configurata per l&#39;app iOS con un identificatore bundle che corrisponde a `appId` nel `liveActivityPushNotificationDetails` del tuo profilo. Ad esempio, se il tuo profilo ha `"appId": "com.example.myapp"`, la superficie deve avere come destinazione la stessa app.
   1. Verifica che il **tipo di attività** nella configurazione della campagna corrisponda esattamente al `attributeType` nel `liveActivityPushNotificationDetails` del tuo profilo. Ad esempio, se il tuo profilo ha `"attributeType": "FoodDeliveryLiveActivityAttributes"`, la campagna deve specificare lo stesso tipo di attività.

      +++

1. &#x200B;
   +++Convalidare la struttura del payload API

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
   * Specifica quando l&#39;attività live deve essere rimossa automaticamente dal dispositivo.
   * Se non viene fornito per l’evento finale, l’attività live rimane visibile fino a quando l’utente non la chiude.
   * Deve essere una marca temporale futura (successiva a `timestamp`).

     +++

1. &#x200B;
   +++ Allineare il payload all’implementazione di iOS

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

   | Problema | Impatto | Correzione |
   |-------|--------|-----|
   | `liveActivityData` mancante negli attributi | L&#39;attività live non verrà avviata | Includi sempre l&#39;oggetto `liveActivityData` nell&#39;evento di avvio |
   | Campo richiesto mancante nell’evento di avvio | L&#39;attività live non verrà avviata | Aggiungi tutti i campi da iOS struct |
   | Nome campo errato (errore di battitura/maiuscole/minuscole) | Campo ignorato o errore di analisi | Corrispondenza esatta dei nomi dei campi di iOS |
   | Tipo di dati errato | Errore di analisi | Corrispondenza con i tipi di dati di iOS |
   | Oggetto nidificato mancante | Dati incompleti | Includi tutte le strutture nidificate |
   | Inclusione di `attributes` in aggiornamento/fine | Non necessario, ma generalmente ignorato | Includi solo `attributes` nell&#39;evento di inizio |
   | Timestamp non aggiornato al momento dell’aggiornamento/della fine | Aggiornamento/fine ignorato dal dispositivo | Genera sempre una nuova marca temporale |

   Per ulteriori esempi, consulta [Crea pagina di attività Live](create-mobile-live.md).

   +++

1. &#x200B;
   +++ Test con Assurance

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
      * L&#39;attività live è stata inviata ai numeri APN.

      +++

### Errori di consegna e analisi degli errori

[!BADGE Applicabile a casi di utilizzo sia unitari che broadcast]{type=Positive}

In questo scenario, tutti i controlli precedenti sono stati superati:

* Il profilo esiste con [token push di attività live validi](#profile-issue)
* Campaign è [configurato correttamente con payload corretto](#payload-issues)
* [I token di aggiornamento sono sincronizzati](#token-not-synced) (solo per eventi di aggiornamento/fine, caso d&#39;uso unitario)

Tuttavia, l’attività live non viene ancora visualizzata, aggiornata o terminata come previsto. Il problema può verificarsi a livello di sistema di consegna Adobe o con il provider di servizi di notifica push (APN).

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

1. &#x200B;
   +++ Controllare i rapporti delle campagne

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
         | Inserire nell&#39;elenco Bloccati Token | Token contrassegnato come non valido | Registra di nuovo il token o controlla lo stato di inserisce nell&#39;elenco Bloccati della |
         | Profilo non idoneo | Il profilo non soddisfa i criteri della campagna | Rivedere le regole del pubblico della campagna |

   Ulteriori informazioni sono disponibili nella [pagina del report della campagna di attività live](../reports/campaign-global-report-cja-activity.md).

   +++

1. &#x200B;
   +++ Controllare gli eventi di feedback dei messaggi nel profilo

   1. Passa a **Cliente** > **Profili** in Journey Optimizer.
   1. Cerca e apri il profilo.
   1. Selezionare la scheda **Eventi**.
   1. Filtra o cerca eventi con `eventType = "message.feedback"`.
   1. Cerca eventi di feedback corrispondenti al tipo `liveActivityID` e `event` della tua attività live.
   1. Esamina i seguenti campi chiave:

      | Campo | Valori possibili | Che cosa significa |
      |-|-|-|
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

1. &#x200B;
   +++ Verificare la consegna di attività live ai numeri APN in Assurance

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

1. &#x200B;
   +++ Procedi a ulteriori controlli diagnostici

   1. Verifica le metriche del ciclo di vita dell’attività live nel rapporto della campagna.

      Nel rapporto della campagna, controlla la sezione **Ciclo di vita attività in tempo reale**:

      | Metrica | Cosa controllare |
      |-|-|
      | Avvii remoti | Deve mostrare il numero di avvii attivati da API |
      | Aggiornamenti | Deve mostrare il conteggio degli eventi di aggiornamento |
      | Termina | Deve mostrare il conteggio degli eventi finali |
      | Conteggio totali | Volume evento attività live globale |

      Se queste metriche sono pari a zero o non corrispondono alle chiamate API, si verifica un problema di consegna tra Adobe e APN.

   1. Se Adobe mostra una consegna corretta ma il dispositivo non mostra l’attività live:

      * Controlla i registri del dispositivo iOS per individuare eventuali errori di attività live.
      * Verifica che l’app sia in primo piano o in background (non terminata).
      * Conferma connettività di rete per il dispositivo.
      * Esegui il test su più dispositivi per escludere problemi specifici del dispositivo.
      * Verifica che la versione di iOS sia 16.1 o successiva.

      +++

1. &#x200B;
   +++ Escalation al supporto Adobe

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

### Token di aggiornamento attività live non sincronizzato{#token-not-synced}

L&#39;attività Live viene avviata correttamente sul dispositivo, ma le successive chiamate API `update` o `end` (che restituiscono HTTP 200) non riescono ad aggiornare o chiudere l&#39;attività Live. Ciò si verifica quando il token di aggiornamento **Live Activity** non è sincronizzato correttamente nel sistema di Adobe.

**Informazioni sui token di aggiornamento**

Quando un’attività Live viene avviata su un dispositivo, iOS genera un token di aggiornamento univoco per tale istanza di attività Live specifica. Questo token è necessario per:

* Invio di aggiornamenti all&#39;attività live
* Cessazione dell’attività live in remoto

Ogni istanza di Live Activity dispone di un proprio token di aggiornamento univoco. Adobe necessita di questo token per distribuire eventi di aggiornamento e fine.

**Comportamento previsto**

Affinché gli eventi di aggiornamento e fine funzionino, si devono verificare i seguenti eventi:

1. L&#39;attività live viene avviata correttamente sul dispositivo.
1. Il dispositivo genera un token di aggiornamento per tale istanza di Live Activity.
1. Mobile SDK acquisisce e invia il token di aggiornamento ad Adobe.
1. Il token di aggiornamento viene sincronizzato e memorizzato nel sistema di Adobe.
1. Le successive chiamate API per l’aggiornamento o la fine utilizzano questo token per la consegna.

**Controlli preliminari:**

* **Autorizzazione utente**: la prima volta che un&#39;attività Live viene avviata su un dispositivo, iOS visualizza un prompt di sistema: &quot;Consenti a [Nome app] di fornire aggiornamenti dell&#39;attività Live?&quot; L&#39;utente **deve toccare &quot;Consenti&quot;** per generare e sincronizzare i token di aggiornamento. Se l’utente tocca &quot;Non consentire&quot;, non vengono creati token di aggiornamento e le richieste di aggiornamento/fine non riusciranno. Si tratta di un’autorizzazione una tantum per app.
* **Convalida profilo e campagna**: completa [i controlli dello scenario 1](#profile-issue) e [dello scenario 2](#payload-issues) per verificare che la configurazione del profilo, dei token e della campagna sia corretta.

#### Passaggi di debug

1. &#x200B;
   +++ Verificare la sincronizzazione del token di aggiornamento in Assurance

   1. Apri la sessione di Assurance.
   1. Assicurati che la sessione fosse attiva quando l&#39;attività live è stata avviata sul dispositivo.
   1. Filtra o cerca eventi con `eventType = "liveActivity.updateToken"`.
   1. Seleziona l’evento e controlla il payload:

      * Verificare che il campo `token` contenga una stringa token di aggiornamento valida.
      * Controlla che `liveActivityID` corrisponda alla tua istanza di Live Activity.
      * Conferma che `activityType` corrisponda al tuo `attributes-type`.

   1. Se l’evento non viene trovato:

      * Il token di aggiornamento non è stato generato o acquisito da SDK.
      * Controlla se l&#39;utente ha concesso le autorizzazioni per l&#39;attività live.
      * Verifica che l&#39;attività live sia stata effettivamente avviata sul dispositivo.
      * Verifica che il SDK mobile sia correttamente integrato per acquisire i token di aggiornamento.

   1. Se viene trovato un evento, procedere al passaggio 2.

      +++

2. &#x200B;
   +++ Verificare il token di aggiornamento negli eventi del profilo

   1. Passa a **Cliente** > **Profili** in Journey Optimizer.
   1. Cerca e apri il profilo.
   1. Selezionare la scheda **Eventi**.
   1. Cerca `liveActivity.updateToken` eventi.
   1. Controlla i dettagli dell’evento:

      * Verifica che il timestamp sia recente (corrisponde all’avvio di Attività live).
      * Verificare che `token` e `liveActivityID` siano presenti.
      * Verificare che `activityType` sia corretto.

   1. Se l’evento non viene trovato nel profilo:

      * L’evento del token di aggiornamento potrebbe non essere ancora stato acquisito nel profilo.
      * Attendere 5-10 minuti e ricontrollare.
      * Se manca ancora dopo 15 minuti, potrebbe esserci un problema di acquisizione dell’evento.

   1. Se viene trovato un evento, il token di aggiornamento è stato sincronizzato. Procedere al passaggio 3.

      +++

3. &#x200B;
   +++ Controllare gli eventi di consegna di attività live in Assurance

   1. Nella sessione di Assurance, esegui una chiamata API di aggiornamento o di fine.
   1. Nell&#39;**Elenco eventi**, cerca gli eventi di consegna delle attività live (eventi push APN).
   1. Verifica la presenza di eventi che indicano:
      * Notifica push inviata ai numeri APN.
      * Risposta da APN (riuscita o errore).
      * Conferma della consegna.
   1. Se è presente un evento di consegna APN: è stata inviata la notifica push. Se il dispositivo non viene ancora aggiornato, il problema potrebbe essere sul lato dispositivo (app che non gestisce il push, problemi di rete, ecc.).
   1. Se manca l’evento di consegna APN: il token di aggiornamento potrebbe non essere memorizzato correttamente o associato al profilo nel sistema di Adobe.
   1. Se sono presenti eventi di errore: controlla i dettagli dell’errore per specifici motivi di errore (token non valido, APN rifiutati, ecc.).

      +++

## Scenari specifici per la trasmissione

### Problemi di configurazione e payload della campagna di trasmissione{#broadcast-config}

Questa sezione descrive gli scenari di risoluzione dei problemi specifici delle attività live di trasmissione che richiedono approcci di debug diversi rispetto alle campagne unitarie.

Quando i profili hanno token validi ma l’attività live non viene visualizzata, aggiornata o si comporta come previsto per i membri del pubblico, il problema in genere deriva da uno dei seguenti elementi:

* La campagna non è configurata come marketing attivato da API.
* Il payload API utilizza una struttura di trasmissione non corretta (mancano `audience` o `input-push-channel`).
* I campi `content-state` e `attributes` non corrispondono all&#39;implementazione di iOS `ActivityAttributes`.
* `input-push-channel` non è stato creato correttamente nel portale per sviluppatori di Apple.

Questo scenario di risoluzione dei problemi si applica a tutti gli eventi di attività live nelle campagne di trasmissione: `start`, `update` e `end`.

**Controlli preliminari:**

* **Tipo di campagna**:
   * Verifica che la campagna sia creata come Marketing attivato da API (necessario per campagne broadcast/basate su pubblico).
   * Conferma che un pubblico sia definito nella configurazione della campagna.
* **Convalida profilo e token**: prova più profili dal pubblico per verificare che dispongano di `liveActivityPushNotificationDetails` validi. Per i passaggi di convalida dettagliati, segui [Scenario 1](#profile-issue).

#### Passaggi di debug

1. &#x200B;
   +++ Verificare la configurazione del pubblico della campagna

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

1. &#x200B;
   +++ Convalidare la struttura del payload dell’API di trasmissione

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

   * **`input-push-channel`**
      * Obbligatorio per tutte le attività di trasmissione in diretta.
      * Funge da identificatore univoco per questa istanza di broadcast specifica.
      * Tutti i profili del pubblico ricevono attività live collegate a questo canale.
      * Deve corrispondere a `channelID` in `liveActivityData.channelID` (vedere il passaggio 3).
      * Deve essere creato per `appID` sul portale Apple Developer dal client.
      * Solo i canali creati per l&#39;elemento `appID` specifico possono essere utilizzati per la trasmissione di attività live nell&#39;app.

   * **`audience.id`**
      * Deve fare riferimento a un segmento di pubblico valido creato in Adobe Experience Platform.
      * Tutti i profili in questo pubblico sono destinati all&#39;attività live.
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

1. &#x200B;
   +++ Allinea lo stato dei contenuti, gli attributi e il canale di input-push con l’implementazione di iOS

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
   * Questa corrispondenza collega l’istanza di trasmissione ai dati dell’attività live.
   * Una mancata corrispondenza causa errori di consegna.

   **Punti di convalida chiave:**

   * Includi tutti i campi `ContentState` in `content-state` per tutti i tipi di evento.
   * Includi tutti i campi `LiveActivityAttributes` personalizzati in `attributes` solo per gli eventi di inizio.
   * Per gli eventi di inizio, `liveActivityData.channelID` deve corrispondere a `input-push-channel`.
   * I nomi dei campi fanno distinzione tra maiuscole e minuscole e devono corrispondere esattamente.
   * I tipi di dati devono corrispondere (String, Int, Bool, oggetti nidificati, ecc.).
   * Per gli eventi di aggiornamento/fine, utilizzare lo stesso `input-push-channel` dell&#39;evento iniziale originale.

   **Errori comuni:**

   | Problema | Impatto | Correzione |
   |-|-|-|
   | Manca `input-push-channel` | La trasmissione non funzionerà | Aggiungi un ID canale univoco per ogni trasmissione |
   | `input-push-channel` non corrisponde a `channelID` | L&#39;attività live non verrà avviata | Assicurati che entrambi i valori siano identici |
   | `input-push-channel` diverso per aggiornamento/fine | Update/end non raggiungerà le attività live | Usa lo stesso ID canale per tutto il ciclo di vita |
   | Manca `liveActivityData.channelID` | L&#39;attività live non verrà collegata alla trasmissione | Includi `channelID` negli attributi per l&#39;evento di inizio |
   | Campo richiesto mancante nell’evento di avvio | L&#39;attività live non verrà avviata | Aggiungi tutti i campi da iOS struct |
   | Nome campo errato (errore di battitura/maiuscole/minuscole) | Campo ignorato o errore di analisi | Corrispondenza esatta dei nomi dei campi di iOS |
   | Timestamp non aggiornato al momento dell’aggiornamento/della fine | Aggiornamento/fine ignorato dai dispositivi | Genera sempre una nuova marca temporale |

   +++

1. &#x200B;
   +++ Test con Assurance

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

### Profilo non presente nello snapshot del pubblico o non aggiornato

In questo scenario, la campagna e il payload sono configurati correttamente, ma profili specifici non ricevono l’attività live. Ciò si verifica in genere quando:

* Il profilo non è un membro del pubblico collegato alla campagna.
* Il pubblico è un pubblico batch e contiene un’istantanea obsoleta dei dati di profilo.
* I token di attività live del profilo sono stati aggiunti di recente ma non sono ancora stati riflessi nello snapshot del pubblico.

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

1. &#x200B;
   +++ Verifica che il profilo sia nel pubblico

   In primo luogo, conferma se il profilo che deve ricevere l’attività live fa effettivamente parte del pubblico.

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

2. &#x200B;
   +++ Controllare il tipo e la pianificazione di valutazione del pubblico

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
      * Se un profilo ha registrato di recente token di attività live, è possibile che tali token non siano presenti nello snapshot corrente.
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
