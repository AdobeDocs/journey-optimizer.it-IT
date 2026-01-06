---
title: Introduzione per gli sviluppatori
description: In qualità di sviluppatore, scopri di più su come utilizzare Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: ht
source-wordcount: '1816'
ht-degree: 100%

---

# Introduzione per gli sviluppatori {#get-started-developers}

In qualità di **sviluppatore**, sei responsabile dell’implementazione e dell’integrazione di [!DNL Adobe Journey Optimizer] nelle applicazioni e nei sistemi. Una volta che l’[amministratore di sistema](administrator.md) e il [data engineer](data-engineer.md) ti avranno concesso l’accesso e avranno preparato il tuo ambiente, potrai iniziare a utilizzare [!DNL Adobe Journey Optimizer].

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

1. **Autenticazione e sicurezza**: tutte le implementazioni richiedono la corretta autenticazione. Scopri come configurare l’autenticazione per SDK e API. Scopri [l’autenticazione API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Impostare le integrazioni delle app per dispositivi mobili {#mobile-integration}

### Configurare Adobe Experience Platform Mobile SDK

Per abilitare le notifiche push, i messaggi in-app e altre funzionalità mobili, integra Adobe Experience Platform Mobile SDK nelle tue applicazioni per dispositivi mobili.

1. **Installa e configura Mobile SDK**: segui la [documentazione di Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} per iniziare a utilizzare l’integrazione con SDK.

1. **Creare una proprietà mobile**: imposta una proprietà mobile in [!DNL Adobe Experience Platform Data Collection]. Scopri come [creare e configurare una proprietà mobile](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurare le notifiche push**:
   * Per **app iOS**: registra l’app con APN (Apple Push Notification Service). Per ulteriori informazioni consulta la [documentazione di Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Per **app Android**: imposta Firebase Cloud Messaging per la tua app Android. Per ulteriori informazioni consulta la [documentazione di Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testa l’integrazione per dispositivi mobili**: utilizza il [flusso di lavoro di avvio rapido per l’onboarding su dispositivi mobili](../../push/mobile-onboarding-wf.md) per configurarne e testarne rapidamente la configurazione.

I passaggi dettagliati per la configurazione delle notifiche push sono disponibili in [questa pagina](../../push/push-configuration.md).

### Implementare esperienze basate su codice (Mobile SDK)

Per la personalizzazione nativa delle app per dispositivi mobili tramite esperienze basate su codice:

* Segui [questo tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} per l’implementazione di Mobile SDK
* Rivedi le implementazioni di esempio per [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} e [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementare le esperienze web {#web-implementation}

### Impostare Adobe Experience Platform Web SDK

Per le implementazioni basate su web, il Web SDK è il punto di integrazione principale:

1. **Installare il Web SDK**: segui la [guida all’implementazione del Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} per impostare SDK sul tuo sito web.

1. **Configurare stream di dati**: crea e configura uno stream di dati in [!DNL Adobe Experience Platform Data Collection] con Journey Optimizer abilitato. Per ulteriori informazioni consulta la [documentazione degli stream di dati](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}.

1. **Abilitare le notifiche push web** (facoltativo): configura la [proprietà pushNotifications](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} nella configurazione del Web SDK e utilizza il [comando sendPushSubscription](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} per registrare gli abbonamenti push.

### Implementare esperienze basate su codice (Web SDK)

Le esperienze basate su codice ti consentono di personalizzare qualsiasi punto di contatto digitale:

1. **Scegliere il metodo di implementazione**: lato client, lato server o ibrido. Rivedi gli [esempi di implementazione](../../code-based/code-based-implementation-samples.md) per ogni approccio.

1. **Definire le superfici**: identifica le posizioni nell’applicazione in cui desideri distribuire contenuti personalizzati. Scopri la [configurazione della superficie](../../code-based/code-based-surface.md).

1. **Implementare il rendering del contenuto**: utilizza il Web SDK per recuperare e applicare contenuti di personalizzazione. Consulta i [tutorial sull’implementazione basata su codice](../../code-based/code-based-decisioning-implementations.md).

1. **Inviare eventi di visualizzazione e interazione**: tieni traccia di quando il contenuto viene visualizzato e quando gli utenti interagiscono con esso per l’analisi e l’ottimizzazione.

Esplora le [implementazioni di esempio su GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} per vedere in azione le esperienze basate su codice.

Ulteriori informazioni sull’[introduzione alle esperienze basate su codice](../../code-based/get-started-code-based.md).

## Implementare lo streaming evento {#event-streaming}

### Inviare eventi per attivare i percorsi

In qualità di sviluppatore, implementerai il codice per inviare eventi che attivano i percorsi. Il [data engineer](data-engineer.md) configurerà gli schemi e le definizioni degli eventi in Journey Optimizer.

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

Le azioni personalizzate consentono ai percorsi di richiamare le API. In qualità di sviluppatore, creerai gli endpoint API richiamati dalle azioni personalizzate:

1. **Generare l’endpoint API**: crea endpoint API RESTful che Journey Optimizer chiamerà durante l’esecuzione del percorso. L’endpoint deve:
   * Accettare i payload JSON
   * Autenticare le richieste (OAuth, chiave API o JWT)
   * Elaborare le richieste entro i limiti di timeout appropriati
   * Restituire risposte nel formato previsto

1. **Informazioni sulle funzionalità delle azioni personalizzate**: le azioni personalizzate possono connettersi a sistemi di terze parti come Epsilon, Slack, Firebase o ai tuoi servizi. Ulteriori informazioni sulle [azioni personalizzate](../../action/action.md).

1. **Utilizza le configurazioni delle azioni**: l’[amministratore](administrator.md) o il [data engineer](data-engineer.md) configurerà l’azione personalizzata in Journey Optimizer, definendo l’URL dell’endpoint API, il metodo di autenticazione e i parametri. Fornirai loro le tue specifiche API. Informazioni sulla [configurazione delle azioni personalizzate](../../action/about-custom-action-configuration.md).

1. **Restituire dati actionable**: progetta l’API per restituire dati che possono essere utilizzati nei passaggi successivi del percorso. Scopri le [risposte alle azioni](../../action/action-response.md).

1. **Implementare la limitazione della frequenza**: assicurati che gli endpoint possano gestire il volume previsto. Journey Optimizer applica un limite di 5000 chiamate/secondo, ma il sistema deve essere resiliente. Scopri il [capping e throttling](../../configuration/external-systems.md).

**Caso d’uso di esempio**: [Scrittura di eventi del percorso in Experience Platform](../../building-journeys/custom-action-aep.md) mediante azioni personalizzate.

## Utilizzare le API di Journey Optimizer {#apis}

Journey Optimizer fornisce API REST complete per l’accesso programmatico:

1. **Informazioni sulle funzionalità API**: le API di Journey Optimizer ti consentono di creare, leggere, aggiornare ed eliminare varie risorse a livello di programmazione. Scopri le [API di Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticazione**: segui [questo tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} per configurare l’autenticazione API tramite Adobe Developer Console.

1. **Esplorare i riferimenti API**: sfoglia la documentazione API completa e prova le API direttamente nel [riferimento API di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campagne attivate da API**: crea messaggistica transazionale con campagne attivate da API. Per scenari con volumi elevati (fino a 5000 TPS), esplora la [modalità velocità effettiva elevata](../../campaigns/api-triggered-high-throughput.md) (richiede una licenza aggiuntiva).

1. **API per la gestione delle decisioni**: utilizza API specializzate per la gestione delle offerte e delle decisioni. Per ulteriori informazioni consulta la [guida API per la gestione delle decisioni](../../offers/api-reference/getting-started.md).

## Test e debug {#testing}

1. **Debug dell’implementazione SDK**: utilizza Adobe Experience Platform Assurance per ispezionare gli eventi SDK, convalidare la raccolta dati e risolvere in tempo reale i problemi di integrazione. [Scopri Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=it){target="_blank"}.

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

### Utilizzo dei dati contestuali e arricchimento

* **Iterazione su array**: utilizza la sintassi Handlebars per visualizzare elenchi dinamici da eventi, risposte di azioni personalizzate e ricerche nei set di dati nei messaggi. Scopri come [iterare dati contestuali](../../personalization/iterate-contextual-data.md).
* **Ricerca nei set di dati**: implementa le ricerche nei set di dati per arricchire i dati del percorso dai set di dati di Adobe Experience Platform. Collabora con il data engineer sulla configurazione. Scopri la [ricerca nei set di dati](../../building-journeys/dataset-lookup.md).

### Lavorare con il consenso e la governance

Implementa la governance dei dati e i criteri di consenso nelle integrazioni:

* **Governance dei dati**: applica i criteri di utilizzo dei dati alle azioni personalizzate. Ulteriori informazioni sulla [governance dei dati](../../action/action-privacy.md).
* **Gestione del consenso**: gestisci le preferenze del consenso della clientela nelle tue implementazioni. Scopri il [consenso](../../action/consent.md).

### Ottimizzazione e best practice

* **Capping e throttling**: comprendi i limiti di frequenza e implementa il throttling appropriato. Scopri i [sistemi esterni](../../configuration/external-systems.md).
* **Ottimizzazione del percorso**: segui le best practice per l’[ottimizzazione del percorso](../../building-journeys/optimize.md).
* **Gestione degli errori**: implementa una solida gestione degli errori. Rivedi i [codici di errore](../../building-journeys/error-codes-reference.md) e le [guide alla risoluzione dei problemi](../../building-journeys/troubleshooting.md).

## Risorse aggiuntive {#additional-resources}

* **Developer Console**: accedi ad [Adobe Developer Console](https://developer.adobe.com){target="_blank"} per creare integrazioni e gestire le credenziali API.
* **Codice di esempio**: esplora le [implementazioni di esempio su GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Video tutorial**: scopri i tutorial pratici in [Experience League](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
* **Community sviluppatori**: contatta altri sviluppatori e ottieni supporto nei forum della community Adobe.

## Collaborare tra ruoli {#next-steps}

Il tuo lavoro di implementazione si interseca con altri membri del gruppo:

>[!BEGINTABS]

>[!TAB Lavorare con i data enginner]

Collabora con i [data engineer](data-engineer.md) sulle configurazioni di dati ed eventi:

* Ottieni gli schemi XDM e le strutture di eventi necessari per l’implementazione
* Scopri quali eventi devi inviare e il formato del payload richiesto
* Allinea i requisiti di raccolta dati e agli standard di qualità dei dati
* Testa la consegna di eventi insieme all’acquisizione di dati

>[!TAB Lavorare con gli amministratori]

Collabora con gli [amministratori](administrator.md) per l’accesso e le configurazioni:

* Fornisci le specifiche API per le azioni personalizzate che configureranno
* Richiedi le autorizzazioni e le credenziali API necessarie
* Coordina i requisiti di configurazione dei canali (ad esempio, certificati push)
* Allinea gli ambienti di test e strategia sandbox

>[!TAB Lavorare con i marketer]

Collabora con i [marketer](marketer.md) sui requisiti del percorso e sui test:

* Scopri quali interazioni utente devono attivare gli eventi
* Implementa il tracciamento per le prestazioni dei contenuti e il coinvolgimento utente
* Test di supporto dei percorsi con funzioni implementate
* Risolvere i problemi relativi alla consegna o alla personalizzazione dei messaggi

>[!ENDTABS]

## Iniziare l’implementazione

Tutto pronto per iniziare a creare? Scegli la tua prima area di implementazione dalle sezioni precedenti:

1. **App per dispositivi mobili?** Inizia con [Integrazione di Mobile SDK](#mobile-integration)
2. **Sito web?** Inizia con [Configurazione di Web SDK](#web-implementation)
3. **Integrazione dell’API?** Vai a [Utilizzo delle API](#apis)
4. **Sistema personalizzato?** Consulta [Azioni personalizzate](#custom-actions)

Ogni sezione include collegamenti alla documentazione tecnica dettagliata, esempi di codice e tutorial per guidare l’implementazione.
