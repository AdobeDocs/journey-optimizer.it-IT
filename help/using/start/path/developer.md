---
title: Introduzione per gli sviluppatori
description: In qualità di sviluppatore, scopri di più su come utilizzare Journey Optimizer
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
source-git-commit: e5e8545bef077219ff91428c9048c978184b57ec
workflow-type: tm+mt
source-wordcount: 3456
ht-degree: 54%

---

# Introduzione per sviluppatori {#get-started-developers}

>[!BEGINSHADEBOX]

**In questa pagina:** implementa gli SDK, lo streaming di eventi, gli endpoint di azione personalizzati e le API che connettono le applicazioni a Adobe Journey Optimizer in modo che i tuoi percorsi possano essere eseguiti su dati live.

>[!ENDSHADEBOX]

In qualità di **sviluppatore**, sei responsabile dell’implementazione e dell’integrazione di [!DNL Adobe Journey Optimizer] nelle applicazioni e nei sistemi. Una volta che l’[amministratore di sistema](administrator.md) e il [data engineer](data-engineer.md) ti avranno concesso l’accesso e avranno preparato il tuo ambiente, potrai iniziare a utilizzare [!DNL Adobe Journey Optimizer].

>[!NOTE]
>
>**Ordine di implementazione:** [Amministratore](administrator.md) → [Ingegnere dati](data-engineer.md) → Sei qui: **Sviluppatore** → [Addetto marketing](marketer.md)
>
>Assicurati che [schemi ed eventi di dati](data-engineer.md) siano configurati prima di implementare le integrazioni mobile e web.

## Il tuo ruolo nell’ecosistema Journey Optimizer

Mentre altri membri del team configurano Journey Optimizer tramite l’interfaccia utente, potrai concentrarti su:

* **Implementazione degli SDK** nelle applicazioni per dispositivi mobili e web
* **Invio di eventi** dalle applicazioni per attivare i percorsi
* **Creazione di endpoint API** che Journey Optimizer può richiamare tramite azioni personalizzate
* **Integrazione** di Journey Optimizer con i sistemi e l’infrastruttura esistenti
* **Test e debug** delle implementazioni

Il [data engineer](data-engineer.md) gestirà schemi di dati, configurazioni di eventi e origini dati. L’[amministratore](administrator.md) configurerà le autorizzazioni e le configurazioni dei canali. I [marketer](marketer.md) progetteranno percorsi e contenuti che utilizzano le tue implementazioni.

Questa guida descrive i passaggi di implementazione tecnica essenziali per iniziare a utilizzare Journey Optimizer. Per la creazione di app per dispositivi mobili, esperienze web o integrazioni API, segui le sezioni di seguito per impostare la tua implementazione.

## Prerequisiti {#prerequisites}

Prima di iniziare l’implementazione, assicurati di disporre di:

| Categoria | Requisiti |
|----------|-------------|
| **Competenze tecniche** | * Esperienza con JavaScript (per Web SDK) o Swift/Kotlin (per Mobile SDK)<br>* Informazioni sulle API RESTful e JSON<br>* Familiarità con la programmazione asincrona e le architetture basate su eventi<br>* Conoscenza dell’architettura delle applicazioni della tua organizzazione |
| **Accesso e autorizzazioni** | * Accesso ad [Adobe Developer Console](https://developer.adobe.com){target="_blank"} per le credenziali API<br>* Ambiente di sviluppo con accesso alla base di codice dell’applicazione<br>* Strumenti di test come Postman per i test delle API<br>* Strumenti per sviluppatori browser o di debug per dispositivi mobili |
| **Da altri membri del team** | * Accesso all’ambiente concesso dall’[amministratore](administrator.md)<br>* Schemi XDM e definizioni di eventi dal [data engineer](data-engineer.md)<br>* Requisiti e casi d’uso dai [marketer](marketer.md) |

## Informazioni sulle basi tecniche {#technical-foundation}

Prima di iniziare a implementare, acquisisci familiarità con i concetti tecnici di base:

1. **Integrazione Adobe Experience Platform**: Journey Optimizer è stato creato nativamente in Adobe Experience Platform. Comprendere l’architettura di base ti aiuterà a creare implementazioni più efficaci. Ulteriori informazioni sul funzionamento di [Journey Optimizer](../understanding-ajo.md).

1. **Modelli dati XDM**: Journey Optimizer utilizza Experience Data Model (XDM) per strutturare i dati di eventi e profili. In qualità di sviluppatore, devi capire come inviare dati conformi agli schemi configurati dal tuo [data engineer](data-engineer.md). Scopri gli [schemi XDM](../../data/get-started-schemas.md).

1. **Autenticazione e sicurezza**: tutte le implementazioni richiedono la corretta autenticazione. Scopri come configurare l’autenticazione per SDK e API. Scopri [l’autenticazione API](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Impostare le integrazioni delle app per dispositivi mobili {#mobile-integration}

### Configurare Adobe Experience Platform Mobile SDK

Il Mobile SDK è una raccolta di librerie da incorporare direttamente nell’app iOS o Android. Agisce come livello di comunicazione tra l’app e Adobe Experience Platform: identifica gli utenti, raccoglie eventi comportamentali e fornisce istruzioni da Journey Optimizer, tra cui notifiche push, messaggi in-app e contenuti personalizzati. Senza di esso, Journey Optimizer non ha alcuna visibilità su ciò che gli utenti della tua app stanno facendo e nessun modo per raggiungerli.

1. **Installa e configura Mobile SDK**: segui la [documentazione di Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"} per iniziare a utilizzare l’integrazione con SDK.

1. **Creare una proprietà mobile**: imposta una proprietà mobile in [!DNL Adobe Experience Platform Data Collection]. Scopri come [creare e configurare una proprietà mobile](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}.

1. **Configurare le notifiche push**:
   * Per **app iOS**: registra l’app con APN (Apple Push Notification Service). Per ulteriori informazioni consulta la [documentazione di Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Per **app Android**: imposta Firebase Cloud Messaging per la tua app Android. Per ulteriori informazioni consulta la [documentazione di Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testa l’integrazione per dispositivi mobili**: utilizza il [flusso di lavoro di avvio rapido per l’onboarding su dispositivi mobili](../../push/mobile-onboarding-wf.md) per configurarne e testarne rapidamente la configurazione.

I passaggi dettagliati per la configurazione delle notifiche push sono disponibili in [questa pagina](../../push/push-configuration.md).

### Implementare esperienze basate su codice (Mobile SDK)

Le esperienze basate su codice ti consentono di distribuire contenuti personalizzati a qualsiasi superficie dell’app mobile nativa, da schermate di onboarding e pagine di dettaglio del prodotto a banner in-app e flag di funzioni, senza richiedere una nuova versione dell’app. Utilizza Mobile SDK per recuperare ed eseguire il rendering di contenuti personalizzati in fase di runtime, dando al team il controllo completo su posizionamento e presentazione:

* Segui [questo tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"} per l’implementazione di Mobile SDK
* Rivedi le implementazioni di esempio per [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} e [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementare le esperienze web {#web-implementation}

### Impostare Adobe Experience Platform Web SDK

Il Web SDK (`alloy.js`) è un&#39;unica libreria JavaScript che sostituisce il patchwork di tag Adobe separati di cui il sito potrebbe avere bisogno. Raccoglie dati comportamentali, li invia a Adobe Experience Platform tramite un flusso di dati configurato e riceve nuovamente istruzioni di personalizzazione, il tutto in un unico round trip in rete. Una volta implementato, Journey Optimizer può identificare i visitatori, attivare i percorsi dalle loro azioni e distribuire immediatamente contenuti personalizzati alle tue pagine.

1. **Installare il Web SDK**: segui la [guida all’implementazione del Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} per impostare SDK sul tuo sito web.

1. **Configurare stream di dati**: crea e configura uno stream di dati in [!DNL Adobe Experience Platform Data Collection] con Journey Optimizer abilitato. Per ulteriori informazioni consulta la [documentazione degli stream di dati](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}.

1. **Abilitare le notifiche push web** (facoltativo): le notifiche push web sono ora in disponibilità generale. Configura la [proprietà pushNotifications](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} nella configurazione del Web SDK e utilizza il [comando sendPushSubscription](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} per registrare le iscrizioni push. [Informazioni sulla configurazione web push](../../push/push-configuration-web.md).

### Implementare esperienze basate su codice (Web SDK)

A differenza dei canali visivi in cui gli addetti al marketing controllano completamente il layout, le esperienze basate su codice ti danno la piena proprietà del modo in cui il contenuto personalizzato viene riprodotto sulla pagina. Journey Optimizer restituisce un payload JSON con i dati di personalizzazione; il codice decide dove e come visualizzarlo. Questo modello funziona per qualsiasi superficie web: banner hero, caroselli di consigli, classificazioni dei risultati di ricerca, varianti di test A/B, senza bisogno di un editor visivo o di un flusso di lavoro di pubblicazione delle pagine.

1. **Scegliere il metodo di implementazione**: lato client, lato server o ibrido. Rivedi gli [esempi di implementazione](../../code-based/code-based-implementation-samples.md) per ogni approccio.

1. **Definire le superfici**: identifica le posizioni nell’applicazione in cui desideri distribuire contenuti personalizzati. Scopri la [configurazione della superficie](../../code-based/code-based-surface.md).

1. **Implementare il rendering del contenuto**: utilizza il Web SDK per recuperare e applicare contenuti di personalizzazione. Consulta i [tutorial sull’implementazione basata su codice](../../code-based/code-based-decisioning-implementations.md).

1. **Inviare eventi di visualizzazione e interazione**: tieni traccia di quando il contenuto viene visualizzato e quando gli utenti interagiscono con esso per l’analisi e l’ottimizzazione.

Esplora le [implementazioni di esempio su GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} per vedere in azione le esperienze basate su codice.

Ulteriori informazioni sull’[introduzione alle esperienze basate su codice](../../code-based/get-started-code-based.md).

## Implementare lo streaming evento {#event-streaming}

### Inviare eventi per attivare i percorsi

Percorsi eseguiti in base a eventi: un utente effettua l’accesso, aggiunge un elemento al carrello, completa un acquisto e abbandona un modulo. Il tuo lavoro consiste nell’emettere tali eventi dall’applicazione esattamente al momento giusto. Ogni evento è un payload JSON strutturato in XDM inviato all’API Streaming Ingestion di Experience Platform; Journey Optimizer lo raccoglie in pochi millisecondi e instrada il profilo in qualsiasi percorso corrispondente. Lo schema dell&#39;evento e la struttura del payload sono definiti dal [Data Engineer](data-engineer.md), che si coordina con loro prima di iniziare la codifica.

1. **Informazioni sul payload evento**: collabora con il data engineer per ottenere lo schema evento e la struttura del payload richiesto. Il payload deve essere conforme allo schema XDM configurato. Scopri i [requisiti dello schema evento](../../event/experience-event-schema.md).

1. **Implementare lo streaming evento**: invia eventi ad Adobe Experience Platform utilizzando le [API di acquisizione in streaming](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=it){target="_blank"}. Scopri i [passaggi per inviare eventi](../../event/additional-steps-to-send-events-to-journey.md).

1. **Gestire tipi di evento**:
   * **Eventi unitari**: implementa l’invio di eventi in base ad azioni specifiche della persona (ad esempio, clic sul pulsante, completamento dell’acquisto)
   * **Eventi di business**: invia eventi correlati all’azienda (ad esempio, aggiornamenti dell’inventario, modifiche dei prezzi)

1. **Testare la consegna evento**: verifica che gli eventi siano ricevuti correttamente e attivino i percorsi come previsto. Scopri la [risoluzione dei problemi degli eventi](../../building-journeys/troubleshooting-inbound.md).

**Implementazione di esempio** per l’invio di un evento tramite API:

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

Ulteriori informazioni [sull’utilizzo di eventi del percorso](../../event/about-events.md).

## Sviluppare endpoint di azione personalizzate {#custom-actions}

Quando un percorso raggiunge un passaggio di azione personalizzato, Journey Optimizer effettua una chiamata HTTP in uscita a un URL fornito: il tuo back-end, un CRM, una piattaforma fedeltà, qualsiasi endpoint REST. Il tuo lavoro consiste nel generare ed esporre tale endpoint: definire il contratto di richiesta (forma payload, metodo di autenticazione, formato di risposta), implementare la logica di business sottostante e assicurarti che possa gestire il volume di chiamata che verrà generato da Journey Optimizer. L&#39;[Amministratore](administrator.md) registra quindi l&#39;endpoint in Journey Optimizer in modo che gli addetti al marketing possano utilizzarlo come passaggio nei propri percorsi.

1. **Generare l’endpoint API**: crea endpoint API RESTful che Journey Optimizer chiamerà durante l’esecuzione del percorso. L’endpoint deve:
   * Accettare i payload JSON
   * Autenticare le richieste (OAuth, chiave API o JWT)
   * Elaborare le richieste entro i limiti di timeout appropriati
   * Restituire risposte nel formato previsto

1. **Informazioni sulle funzionalità delle azioni personalizzate**: le azioni personalizzate possono connettersi a sistemi di terze parti come Epsilon, Slack, Firebase o ai tuoi servizi. Ulteriori informazioni sulle [azioni personalizzate](../../action/action.md).

1. **Utilizza le configurazioni delle azioni**: l’[amministratore](administrator.md) o il [data engineer](data-engineer.md) configurerà l’azione personalizzata in Journey Optimizer, definendo l’URL dell’endpoint API, il metodo di autenticazione e i parametri. Fornirai loro le tue specifiche API. Informazioni sulla [configurazione delle azioni personalizzate](../../action/about-custom-action-configuration.md). Puoi definire un **payload di risposta di errore** facoltativo per una logica di fallback più avanzata nei rami di timeout/errore.

1. **Restituire dati actionable**: progetta l’API per restituire dati che possono essere utilizzati nei passaggi successivi del percorso. Scopri le [risposte alle azioni](../../action/action-response.md).

1. **Monitorare lo stato delle azioni personalizzate**: utilizza la dashboard di monitoraggio delle azioni personalizzate per tenere traccia le chiamate andate a buon fine, gli errori, la velocità effettiva, i tempi di risposta e tempi di attesa delle code. Informazioni sul [reporting delle azioni personalizzate](../../action/reporting.md).

1. **Implementare la limitazione della frequenza**: assicurati che gli endpoint possano gestire il volume previsto. Journey Optimizer applica un limite di 5000 chiamate/secondo, ma il sistema deve essere resiliente. Scopri il [capping e throttling](../../configuration/external-systems.md).

**Caso d’uso di esempio**: [Scrittura di eventi del percorso in Experience Platform](../../building-journeys/custom-action-aep.md) mediante azioni personalizzate.

## Utilizzare le API di Journey Optimizer {#apis}

Non è necessario che tutto accada tramite l’interfaccia utente di Journey Optimizer. A volte è necessario attivare una campagna dal proprio backend, eliminare un indirizzo e-mail dopo una richiesta di privacy o sincronizzare modelli di contenuto da un CMS esterno. Le API REST di Journey Optimizer consentono di accedere in modo programmatico alle funzionalità di base della piattaforma. Tutte le chiamate utilizzano l&#39;autenticazione server-to-server OAuth: il metodo JWT precedente è obsoleto.

1. **Informazioni sulle funzionalità API**: le API di Journey Optimizer ti consentono di creare, leggere, aggiornare ed eliminare varie risorse a livello di programmazione. Scopri le [API di Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticazione**: segui [questo tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} per configurare l’autenticazione API tramite Adobe Developer Console.

1. **Esplorare i riferimenti API**: sfoglia la documentazione API completa e prova le API direttamente nel [riferimento API di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

1. **Campagne attivate da API**: crea messaggistica transazionale con campagne attivate da API. Per scenari con volumi elevati (fino a 5000 TPS), esplora la [modalità velocità effettiva elevata](../../campaigns/api-triggered-high-throughput.md) (richiede una licenza aggiuntiva).

1. **API per la gestione delle decisioni**: utilizza API specializzate per la gestione delle offerte e delle decisioni. Per ulteriori informazioni consulta la [guida API per la gestione delle decisioni](../../offers/api-reference/getting-started.md).

1. **API per la migrazione della funzione Decisioni**: esegui la migrazione programmatica delle entità di Gestione decisioni nella funzione Decisioni con ambiti flessibili, convalida automatizzata e supporto del rollback. Per ulteriori informazioni consulta la [guida API per la migrazione della funzione Decisioni](../../experience-decisioning/decisioning-migration-api.md).

1. **Webhook SMS**: configura i webhook in entrata per acquisire i messaggi in arrivo e i webhook di feedback per ricevere le conferme di consegna e gli aggiornamenti dello stato. [Ulteriori informazioni](../../mobile/mobile-webhook.md).

## Test e debug {#testing}

Prima che l’implementazione venga pubblicata, devi essere sicuro che gli eventi si attivino al momento giusto, che i percorsi si attivino come previsto, che le azioni personalizzate si comportino con un carico realistico e che il rendering dei contenuti personalizzati venga eseguito correttamente. Questa sezione descrive gli strumenti e le tecniche per rilevare i problemi in anticipo, dalla registrazione SDK di basso livello alle esecuzioni di test di percorso end-to-end con profili reali.

1. **Implementazione debug di SDK**: utilizza Adobe Experience Platform Assurance per verificare gli eventi di SDK, convalidare la raccolta dati e risolvere eventuali problemi di integrazione non appena si verificano. [Scopri Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=it){target="_blank"}.

1. **Testa la consegna evento**: verifica che gli eventi dall’applicazione siano ricevuti correttamente da Adobe Experience Platform e attivino i percorsi nel modo previsto. Monitora l’acquisizione degli eventi e convalida la struttura del payload.

1. **Convalidare le integrazioni API**: testa gli endpoint dell’azione personalizzata per garantire che gestiscano correttamente le richieste di Journey Optimizer, rispondano entro i limiti di timeout e restituiscano i formati dati previsti.

1. **Utilizza la modalità test con i profili di test**: collabora con il tuo [data engineer](data-engineer.md) per accedere ai profili di test, quindi convalida l’implementazione utilizzando la modalità di test del percorso. Scopri come [testare i percorsi](../../building-journeys/testing-the-journey.md).

1. **Monitorare i registri SDK**: abilita la registrazione di debug nell’implementazione SDK per risolvere i problemi durante lo sviluppo:
   * **Mobile SDK**: abilita la registrazione per vedere gli eventi SDK e le chiamate API
   * **Web SDK**: usa la console browser per monitorare l’attività SDK

1. **Verificare la configurazione dello stream di dati**: assicurati che lo stream di dati sia configurato correttamente per l’invio di dati a Journey Optimizer. Verifica che gli eventi fluiscano attraverso lo stream di dati verso le destinazioni corrette.

1. **Query dei dati del percorso per l’analisi**: utilizza le query SQL nel data lake per analizzare gli eventi dei passaggi del percorso, eseguire il debug dei problemi e monitorare le prestazioni delle azioni personalizzate. Esplora gli [esempi di query per l’analisi del percorso](../../reports/query-examples.md), tra cui:
   * Tracciamento di entrata/uscita del profilo e motivi di eliminazione
   * Metriche delle prestazioni delle azioni personalizzate (latenza, velocità effettiva, errori)
   * Modelli di consegna degli eventi e di errore
   * Stati dell’istanza del percorso

## Argomenti per sviluppatori avanzati {#advanced-topics}

Una volta implementati gli SDK, gli eventi e le API principali, questi argomenti ti aiutano ad andare oltre: arricchire i dati del percorso in fase di runtime senza gonfiare il profilo, gestire i segnali di consenso in modo che le rinunce si propaghino attraverso ogni integrazione e ottimizzare l’implementazione per il throughput e l’affidabilità richiesti dalla scala di produzione.

### Utilizzo dei dati contestuali e arricchimento

I percorsi spesso necessitano di più dati rispetto a quelli che arrivano nell&#39;evento scatenante: un nome di prodotto, un livello fedeltà, un elenco di voci dell&#39;ordine. Invece di precaricare tutto questo in ogni profilo, l’arricchimento contestuale consente al percorso di esaminarlo in fase di esecuzione dai set di dati di AEP o di portarlo avanti da una risposta di azione personalizzata. I messaggi e le condizioni del ramo possono quindi fare riferimento a tali dati senza mai essere memorizzati in modo permanente sul profilo.

* **Iterazione su array**: utilizza la sintassi Handlebars per visualizzare elenchi dinamici da eventi, risposte di azioni personalizzate e ricerche nei set di dati nei messaggi. Scopri come [iterare dati contestuali](../../personalization/iterate-contextual-data.md).
* **Ricerca nei set di dati**: implementa le ricerche nei set di dati per arricchire i dati del percorso dai set di dati di Adobe Experience Platform. Collabora con il data engineer sulla configurazione. Scopri la [ricerca nei set di dati](../../building-journeys/dataset-lookup.md).

### Lavorare con il consenso e la governance

Journey Optimizer applica la governance dei dati e i criteri di consenso a livello di piattaforma, ma anche la tua integrazione deve rispettarli. Quando un cliente rinuncia alle comunicazioni di marketing, o quando un’etichetta di utilizzo dei dati limita la modalità di utilizzo di un campo, queste regole devono propagarsi tramite azioni personalizzate e ricerche di set di dati, non solo bloccando le azioni nell’interfaccia utente.

* **Governance dei dati**: applica i criteri di utilizzo dei dati alle azioni personalizzate. Ulteriori informazioni sulla [governance dei dati](../../action/action-privacy.md).
* **Gestione del consenso**: gestisci le preferenze del consenso della clientela nelle tue implementazioni. Scopri il [consenso](../../action/consent.md).

### Ottimizzazione e best practice

Le implementazioni Journey Optimizer di produzione gestiscono regolarmente milioni di eventi e migliaia di esecuzioni di percorso al secondo. Queste risorse consentono di ottimizzare l&#39;integrazione in base a tale scala: comprendere i limiti di velocità prima di raggiungerli, evitare le comuni insidie di progettazione del percorso che causano la caduta silenziosa dei profili e creare una gestione degli errori che si riduca gradualmente anziché fallire in modo poco trasparente.

* **Capping e throttling**: comprendi i limiti di frequenza e implementa il throttling appropriato. Scopri i [sistemi esterni](../../configuration/external-systems.md).
* **Ottimizzazione del percorso**: segui le best practice per l’[ottimizzazione del percorso](../../building-journeys/optimize.md).
* **Gestione degli errori**: implementa una solida gestione degli errori. Rivedi i [codici di errore](../../building-journeys/error-codes-reference.md) e le [guide alla risoluzione dei problemi](../../building-journeys/troubleshooting.md).

## Chiama API REST di Journey Optimizer {#rest-apis}

Oltre all’implementazione degli SDK e allo streaming di eventi, puoi anche gestire Journey Optimizer a livello di programmazione dai tuoi sistemi. Il riferimento API completo, le specifiche OpenAPI e gli esempi di codice si trovano nel [portale per sviluppatori di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

>[!NOTE]
>
>Tutte le integrazioni devono utilizzare l’autenticazione server-to-server OAuth: il metodo JWT è obsoleto. [Configura autenticazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### Eseguire campagne attivate da API {#api-triggered}

Attivare messaggi transazionali o di marketing da un sistema esterno utilizzando l’API REST di esecuzione interattiva dei messaggi. Prima di chiamare l&#39;endpoint:

* La campagna deve essere **attivata** prima che l&#39;endpoint accetti le chiamate.
* Le chiamate hanno un **timeout di 60 secondi**; i nuovi tentativi interni gestiscono timeout imprevisti.
* Se sono configurate le date di inizio/fine della campagna, le chiamate API al di fuori di tali date non riusciranno.
* Per generare il payload, recupera la richiesta cURL di esempio generata dalla sezione **richiesta cURL** della tua campagna live nell&#39;interfaccia utente di Journey Optimizer, contenente tutte le variabili di personalizzazione per tale campagna.
* Le campagne Standard e [High-Throughput](../../campaigns/api-triggered-high-throughput.md) utilizzano endpoint diversi.

[Riferimento API](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [Esempi di codice](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [Utilizzo di campagne attivate da API](../../campaigns/api-triggered-campaigns.md)

### Limitazione e limitazione per gli endpoint esterni {#capping-throttling}

Quando i percorsi chiamano sistemi esterni tramite azioni personalizzate o origini dati, le API di limitazione e limitazione proteggono tali sistemi dal sovraccarico. Il limite rifiuta le chiamate che superano il limite configurato; la limitazione le mette in coda per un massimo di 6 ore (solo sandbox di produzione, azioni personalizzate).

[Riferimento API di limitazione](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [Utilizzare l&#39;API di limitazione](../../configuration/capping.md) · [Utilizzare l&#39;API di limitazione](../../configuration/throttling.md)

### Altre API REST {#more-rest-apis}

Oltre ai messaggi e ai limiti, Journey Optimizer espone endpoint REST per la gestione dell’eliminazione, la creazione di modelli di contenuto, il recupero delle campagne, la verifica e l’esecuzione orchestrata delle campagne. Utilizzali quando devi automatizzare operazioni che altrimenti richiederebbero passaggi manuali nell’interfaccia utente, ad esempio la soppressione in blocco degli indirizzi dopo un richiamo di dati o la sincronizzazione di modelli da una pipeline di contenuto esterna.

| Operazioni da eseguire | Documentazione delle API |
| ------------------- | ------------- |
| Escludere in modo programmatico indirizzi e-mail o domini dall’invio | [API di eliminazione](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [Gestione dell&#39;elenco di soppressione](../../configuration/manage-suppression-list.md) |
| Recuperare i metadati di percorso per il controllo o la sincronizzazione esterna | API [Percorsi](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| Creare e gestire modelli di contenuto e frammenti da una pipeline esterna | [API contenuto](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [Modelli](../../content-management/content-templates.md) · [Frammenti](../../content-management/fragments.md) |
| Recuperare e filtrare le campagne d’azione | [API campagne](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| Visualizzare l’anteprima delle campagne e inviare le bozze a livello di programmazione | [API simulazioni](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |
| Convalidare i set di dati e attivare l’esecuzione di una campagna orchestrata | [Convalida set di dati](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [Trigger](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [Abilita set di dati](../../orchestrated/manual-schema.md) |

## Risorse aggiuntive {#additional-resources}

* **Developer Console**: accedi ad [Adobe Developer Console](https://developer.adobe.com){target="_blank"} per creare integrazioni e gestire le credenziali API.
* **Codice di esempio**: esplora le [implementazioni di esempio su GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Video tutorial**: scopri i tutorial pratici in [Experience League](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
* **Community sviluppatori**: contatta altri sviluppatori e ottieni supporto nei forum della community Adobe.

## Collaborare tra ruoli {#next-steps}

Il tuo lavoro di implementazione si interseca con altri membri del gruppo:

>[!BEGINTABS]

>[!TAB Lavorare con i data enginner]

Collabora con [Data Engineer](data-engineer.md) sulle configurazioni di dati ed eventi. Ogni percorso che reagisce al comportamento dell’utente dipende dagli eventi inviati: il Data Engineer definisce gli schemi, si implementa il codice che li produce.

* Ottieni gli [schemi XDM](../../data/get-started-schemas.md) e le strutture di eventi necessari per implementare
* Scopri quali eventi devi inviare e il formato del payload richiesto. Vedi [utilizzo degli eventi di percorso](../../event/about-events.md)
* Conferma quali campi sono obbligatori rispetto a facoltativi in ogni payload dell&#39;evento e cosa accade nei percorsi in cui i campi previsti sono mancanti o in formato non valido. Vedi [requisiti dello schema](../../event/experience-event-schema.md#schema-requirements)
* Verifica della consegna degli eventi e dell&#39;acquisizione dei dati insieme tramite [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=it){target="_blank"}

>[!TAB Lavorare con gli amministratori]

Collabora con [Amministratori](administrator.md) per le configurazioni di accesso e canale. I percorsi possono raggiungere gli utenti solo tramite i canali impostati dall&#39;amministratore, coordinati in anticipo in modo che il SDK funzioni e la relativa configurazione rimangano sincronizzati.

* Specifica le API per [azioni personalizzate](../../action/about-custom-action-configuration.md) che configureranno in Journey Optimizer
* Richiedi le autorizzazioni e le credenziali API necessarie tramite [Adobe Developer Console](https://developer.adobe.com){target="_blank"}
* Coordinare i requisiti di configurazione del canale: certificati push per [iOS](../../push/push-configuration.md) e Android, [impostazioni web push](../../push/push-configuration-web.md), [endpoint webhook SMS](../../mobile/mobile-webhook.md)
* Allinea alla strategia sandbox e agli ambienti di test prima di eseguire la modalità di test [percorso](../../building-journeys/testing-the-journey.md)

>[!TAB Lavorare con i marketer]

Collabora con [addetti al marketing](marketer.md) per la progettazione e il test del percorso. Gli addetti al marketing creano percorsi e contenuti che dipendono interamente dagli eventi inviati e dalle superfici esposte: più si allinea, più velocemente i percorsi vengono pubblicati.

* Rivedi le progettazioni del percorso in [Journey Optimizer](../../building-journeys/journey.md) insieme per capire quali interazioni utente devono attivare gli eventi e quali superfici necessitano di personalizzazione
* Implementa il tracciamento in modo che gli addetti al marketing possano misurare le prestazioni dei contenuti [ e il coinvolgimento degli utenti](../../reports/report-gs-cja.md)
* Esegui [modalità di test percorso](../../building-journeys/testing-the-journey.md) insieme utilizzando i profili di test per convalidare il flusso completo end-to-end
* Risolvere i problemi relativi alla consegna dei messaggi, al rendering della personalizzazione o alle risposte di [azione personalizzata](../../action/action.md)

>[!ENDTABS]

## Iniziare l’implementazione

Tutto pronto per iniziare a creare? Scegli la tua prima area di implementazione dalle sezioni precedenti:

1. **App mobile?** Inizia con [Integrazione Mobile SDK](#mobile-integration)
2. **Sito web?** Inizia con [Configurazione Web SDK](#web-implementation)
3. **Integrazione dell’API?** Passa a [Utilizzare le API](#apis)
4. **Sistema personalizzato?** Scopri le [Azioni personalizzate](#custom-actions)

Ogni sezione include collegamenti alla documentazione tecnica dettagliata, esempi di codice e tutorial per guidare l’implementazione.

## Altre guide ruolo {#other-role-guides}

| Ruolo | Guida |
|------|-------|
| Amministratore | [Introduzione per gli amministratori](administrator.md) |
| Ingegnere dati | [Introduzione per gli ingegneri dati](data-engineer.md) |
| Sviluppatore | [Introduzione per sviluppatori](developer.md) |
| Addetto marketing | [Introduzione per i marketer](marketer.md) |

Torna a [Panoramica su ruoli e responsabilità](../quick-start.md) · Torna a [Inizia](../../../rp_landing_pages/get-started-landing-page.md)
