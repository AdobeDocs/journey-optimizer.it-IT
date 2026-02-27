---
solution: Journey Optimizer
product: journey optimizer
title: Domande frequenti
description: Domande frequenti sulle attività live
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e7e994ca-aa0c-4e86-8710-c87430b74188
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Domande frequenti {#mobile-live-faq}

## Domande generali

+++Qual è la differenza tra un’attività live e una notifica push?

L’attività live fornisce aggiornamenti persistenti e in tempo reale sullo schermo di blocco e su Dynamic Island senza richiedere agli utenti di sbloccare il dispositivo. Le notifiche push sono avvisi temporanei che scompaiono una volta ignorate. L’attività live rimane visibile e può essere aggiornata più volte fino alla sua scadenza esplicita.

+++

+++Quante istanze di attività live possono essere attive contemporaneamente?

Un&#39;app iOS può eseguire più istanze di attività Live simultaneamente, comprese quelle che utilizzano lo stesso tipo `ActivityAttributes`.

Non esiste alcun limite imposto dagli sviluppatori sul numero di istanze di attività Live di un determinato tipo di attributo che possono esistere. Puoi iniziare tutti i passaggi necessari per la logica dell’app, ad esempio uno per consegna o corsa in corso. Tuttavia, iOS applica un limite a livello di sistema sul numero di istanze di attività Live che possono essere attive o visibili contemporaneamente.

In pratica:

* In genere, iOS supporta fino a cinque istanze di attività live simultanee per app.

* Se superi questo numero, il sistema potrebbe interrompere la visualizzazione di alcune istanze di attività o terminare quelle precedenti per risparmiare risorse.

* Ogni istanza di attività Live ha un `Activity.id` univoco, che consente di aggiornarlo o terminarlo singolarmente.

+++

+++Gli utenti devono avere l’app aperta per ricevere aggiornamenti dell’attività live?

No. L’attività live può essere avviata, aggiornata e terminata in remoto anche quando l’app è completamente chiusa, uno dei principali vantaggi della funzione.

+++

+++Quali versioni di iOS supportano l’attività live?

* iOS 16.1+: supporto di base per le attività live
* iOS 17.2+: funzionalità push-to-start (avvio in remoto senza aprire l’app)
* iOS 18+: supporto dei canali di trasmissione per attività live basate sul pubblico
+++

+++Per quanto tempo un’attività Live può rimanere attiva?

Apple limita l&#39;attività Live a **8 ore di aggiornamenti attivi**. Dopo di che, il sistema termina automaticamente l&#39;attività, anche se può rimanere visibile in uno stato statico per un massimo di **12 ore aggiuntive** prima della rimozione. Puoi anche terminare un&#39;attività Live prima impostando un `dismissalDate` o chiamando esplicitamente `activity.end()` nell&#39;app.

+++

### Domande per sviluppatori

+++Devo creare un’estensione widget separata per l’attività Live?

Sì.  L&#39;attività live viene visualizzata tramite WidgetKit, pertanto devi creare un&#39;estensione widget nel progetto Xcode e implementare `ActivityConfiguration`.
[Ulteriori informazioni sulla configurazione dei widget](mobile-live-configuration-sdk.md)

+++

+++È possibile utilizzare la stessa classe `LiveActivityAttributes` per le attività Live locali e remote?

Sì.  La stessa classe di attributi funziona sia per l’attività Live avviata in locale che per quella avviata in remoto (push-to-start). È necessario assicurarsi di registrarlo con `Messaging.registerLiveActivity()`.

+++

+++Cosa succede se invio un aggiornamento per un’attività Live che non esiste?

Se si invia un evento di aggiornamento o di fine per un `liveActivityID` o un `channelID` inesistente, la richiesta non riuscirà nel dispositivo. Assicurati sempre di tenere traccia delle istanze di attività live attive per ogni utente.

+++

+++Posso testare l’attività Live nel simulatore iOS?

Sì, puoi testare l’attività Live avviata in locale o in remoto in iOS Simulator.

* **Locale**: ciò include la creazione, l&#39;aggiornamento e la fine dell&#39;attività Live direttamente dall&#39;app tramite **API ActivityKit**.

* **Remoto**: per testare la funzionalità delle attività live in remoto, integra il SDK di messaggistica nell&#39;app e utilizza le API di esecuzione fornite per inviare l&#39;avvio, l&#39;aggiornamento e la fine remoti al dispositivo di prova o al simulatore iOS. Allo stesso modo in cui le notifiche push possono essere testate al momento con l’integrazione degli SDK di Adobe.

+++

+++Come posso gestire gli aggiornamenti quando l’app è in background?

Il SDK gestisce questo processo automaticamente. Una volta registrata, l’attività Live riceve gli aggiornamenti anche quando l’app viene terminata. Non sono necessarie modalità di sfondo aggiuntive.
+++

+++Differenza tra `liveActivityID` e `channelID`

* `liveActivityID`: utilizzato per singole attività live (unitarie) mirate a utenti specifici. Ogni ID rappresenta un’istanza di attività Live univoca.
* `channelID`: utilizzato per la trasmissione di attività Live inviate al pubblico. Tutti gli utenti del pubblico ricevono gli stessi aggiornamenti sullo stesso canale.
+++

+++È possibile personalizzare l’aspetto di Dynamic Island separatamente dalla schermata di blocco?

Sì.  `ActivityConfiguration` dispone di chiusure separate per il contenuto Schermo di blocco e per il contenuto Isola dinamica (stati espansi, compatti e minimi), ciascuna progettazione in modo indipendente.
+++

+++È necessario memorizzare manualmente i token di push?

No. Quando si registra un tipo di attività Live con `Messaging.registerLiveActivity()`, SDK raccoglie e gestisce automaticamente i token push.
+++

+++Ci sono limiti agli avvii remoti dell’attività Live?

Sì.  Gli avvii remoti tramite `ActivityKit` sono soggetti ai limiti imposti dal sistema. Se tenti più richieste di avvio in rapida successione, iOS potrebbe rifiutare ulteriori avvii a causa di quote di attività live o vincoli di budget. Dopo circa 5 tentativi di avvio consecutivi, le richieste successive iniziano a non riuscire fino al trascorrere di un breve periodo di raffreddamento.

+++

+++Qual è il budget per gli aggiornamenti con priorità alta?

Apple non specifica un limite numerico esatto per gli aggiornamenti delle attività Live `(priority: 10)` ad alta priorità. Il sistema mantiene un budget interno dinamico che limita la frequenza con cui tali aggiornamenti possono essere inviati. Se vengono rilasciati troppi aggiornamenti ad alta priorità in un breve arco di tempo, iOS potrebbe limitare o ritardare quelli successivi.

Per ridurre al minimo la limitazione:

* **Livelli di priorità del saldo**: combinare gli aggiornamenti standard `(priority: 5)` e alti `(priority: 10)` a seconda della rilevanza.
* **Utilizza con moderazione la priorità alta**: prendi in considerazione la priorità alta per gli aggiornamenti critici in termini di tempo, ad esempio l&#39;avanzamento della consegna, lo stato dell&#39;ordine o i punteggi sportivi live.
* **Supporto aggiornamenti frequenti**: includi `NSSupportsLiveActivitiesFrequentUpdates` in `Info.plist` dell&#39;app e impostalo su **SÌ** se hai bisogno di aggiornamenti frequenti.

+++

### Domande dell’addetto marketing

+++Posso personalizzare il contenuto delle attività live per ogni utente in una campagna di trasmissione?

Le campagne di trasmissione inviano lo stesso contenuto a tutti gli utenti del pubblico. Per i contenuti personalizzati, utilizza campagne unitarie (transazionali) indirizzate a singoli utenti.
+++

+++Come posso sapere se la mia attività Live è stata consegnata correttamente?

[Monitora le analisi delle campagne](../reports/campaign-global-report-cja-activity.md) in Adobe Journey Optimizer. Puoi tenere traccia delle percentuali di consegna, degli errori e delle metriche di coinvolgimento. Inoltre, considera l’implementazione di eventi di analisi personalizzati nell’app.
+++

+++Posso pianificare l’attività Live in anticipo?

La chiamata API attiva immediatamente l’attività Live. Tuttavia, puoi pianificare le chiamate API attraverso i sistemi back-end o utilizzare le funzionalità di orchestrazione di Journey Optimizer per temporizzarle in modo appropriato.
+++

+++Cosa succede se invio un evento &quot;start&quot; per un’attività Live già esistente?

Quando si avvia in remoto un’attività Live tramite le API di esecuzione di Adobe:

* È possibile includere un&#39;intestazione `x-request-id` nella richiesta. Idealmente dovrebbe esserci una relazione uno-a-uno tra ogni `liveActivityID` e il corrispondente `x-request-id`. In questo modo, se vengono effettuate più richieste con la stessa combinazione di `x-request-id` e `liveActivityID`, sul dispositivo verrà avviata una sola istanza di attività Live e le richieste duplicate verranno ignorate.

* Se l&#39;intestazione `x-request-id` viene omessa, ogni richiesta viene trattata in modo indipendente, il che può comportare la creazione di più istanze di attività Live con lo stesso `liveActivityID`. In questi casi, gli aggiornamenti futuri potrebbero non riuscire o applicarsi solo a una delle istanze attive.

* Il valore `x-request-id` non deve essere riutilizzato in `liveActivityIDs` diversi in richieste API separate.

+++

+++Posso testare A/B diverse esperienze di attività live?

Sì.  Crea più campagne con diverse strutture di contenuto e utilizza le funzioni di sperimentazione di Adobe Journey Optimizer per verificare quale funziona meglio. Assicurati che l&#39;app supporti tutte le varianti di stato del contenuto.

+++

+++Con quale frequenza devo aggiornare un’attività Live?

Aggiorna solo quando cambiano informazioni significative, poiché aggiornamenti troppo frequenti possono svuotare la batteria e ridurre la qualità dell’esperienza utente. Per scenari in tempo reale, come il tracciamento delle consegne, in genere è accettabile ogni 30-60 secondi. Per contenuti che cambiano più lentamente, come i punteggi sportivi, aggiorna solo gli eventi significativi.

+++

+++Posso indirizzare gli utenti in base al fatto che abbiano o meno l’attività Live abilitata?

Sarà necessario collaborare con il team di sviluppo per tenere traccia e trasmettere questa preferenza a Adobe Experience Platform come attributo utente, quindi per segmentare in base a tale attributo.

+++

### Domande API

+++Differenza tra `timestamp` e `dismissal-date`

* `timestamp`: l&#39;epoca corrente in cui si verifica l&#39;evento, necessaria per tutti gli eventi.
* `dismissal-date`: un&#39;epoca futura in cui l&#39;attività Live dovrebbe essere chiusa automaticamente, necessaria solo per gli eventi di &quot;fine&quot;.

+++

+++Devo inviare tutti i campi `attributes` in ogni chiamata di aggiornamento?

Sì, in base alla classe `LiveActivityAttribute`.

* Tutti i campi dell&#39;oggetto attributi, incluso `liveActivityData`, devono essere inclusi in ogni chiamata, per l&#39;inizio, gli aggiornamenti o la fine.
* Solo i campi `content-state` rappresentano le modifiche effettive in modo dinamico in un&#39;attività live in esecuzione.
* Includi anche un oggetto avviso, in modo che venga trattato come una notifica visibile all’utente e non come una notifica di sfondo invisibile all’utente. Obbligatorio solo per i casi &quot;start&quot; e altrimenti facoltativo.

+++

+++In quale formato dovrebbero essere le marche temporali dell’epoca?

Utilizza il tempo dell&#39;epoca Unix in **secondi** non millisecondi. Ad esempio: `1759937682`

+++

+++Posso usare lo stesso `requestId` per più chiamate API?

No. Ogni richiesta API deve avere un `requestId` univoco per garantire l&#39;idempotenza e il tracciamento corretto. Utilizza UUID o identificatori univoci simili.

+++

+++Qual è l’autenticazione necessaria per l’API headless?

Per informazioni sui requisiti di autenticazione, inclusi token OAuth e chiavi API, consulta la [documentazione sulle campagne attivate dall&#39;API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/).

+++

+++Cosa succede se la chiamata API non riesce?

Implementa la logica retry con backoff esponenziale. Controlla la risposta API per verificare la presenza di codici di errore e messaggi per diagnosticare i problemi. Gli errori comuni includono ID campagna non validi, payload non validi o problemi di autenticazione.

+++

+++Posso inviare aggiornamenti delle attività live dai miei server back-end?

Sì, questo è il comportamento previsto. Il backend chiama l’API Adobe Journey Optimizer Headless per attivare eventi di attività live quando la logica di business lo richiede.

+++

+++È necessaria una campagna diversa per gli eventi di inizio, aggiornamento e fine?

No. Puoi utilizzare la stessa campagna e modificare il campo `event` nel payload. Tuttavia, alcune organizzazioni preferiscono campagne separate per un migliore tracciamento delle analisi.

+++

### Domande sulla risoluzione dei problemi

+++La mia attività Live viene avviata ma non viene aggiornata. Quale potrebbe essere il problema?

Cause comuni:

* Mancata corrispondenza di `liveActivityID` o `channelID` tra le chiamate di avvio e di aggiornamento.
* I campi `content-state` non corrispondono allo struct `ContentState`.
* L’attività Live è già terminata.
* Problemi di connettività di rete sul dispositivo.
* L’ora dell’epoca utilizzata come marca temporale non è aggiornata.

+++

+++Impossibile riconoscere il campo `attributes-type`. Cosa devo controllare?

* Assicurati che il nome della classe corrisponda esattamente a **1} (distinzione maiuscole/minuscole) con il nome dello struct Swift**
* Verificare che la struttura sia definita e registrata correttamente
* Verifica la presenza di errori di battitura nel payload JSON
* Conferma che la versione dell&#39;app installata abbia l&#39;implementazione Live Activity

+++

+++Gli utenti visualizzano solo l’aggiornamento dell’attività Live e non la notifica di avviso. Si tratta di un problema noto?

No. Il campo `alert` è facoltativo e può essere soppresso da iOS in determinate condizioni, ad esempio in modalità Non disturbare. L’attività live può essere aggiornata in modo silenzioso, che spesso è il comportamento previsto. Il campo di avviso è obbligatorio per l’invio di avvii remoti, altrimenti Apple lo tratta come una notifica in background silenziosa.

+++

+++Posso eliminare o cancellare tutte le istanze di attività live di un utente?

Devi inviare un evento &quot;finale&quot; per ogni istanza di attività Live attiva. Tieni traccia delle istanze di attività live attive per ogni utente nei tuoi sistemi, in modo da poterle pulire correttamente.

+++

+++Il mio widget mostra &quot;Nessun dato&quot; anche se ho inviato un aggiornamento. Quale potrebbe essere il problema?

* Verificare che l&#39;implementazione del widget acceda correttamente a `context.state` e `context.attributes`.
* Controlla che i valori predefiniti o gli stati di errore siano gestiti nell&#39;interfaccia del widget.
* Utilizzare il protocollo `LiveActivityAssuranceDebuggable` per eseguire il debug dello schema.
* Esegui il test con Adobe Assurance per verificare se i dati vengono ricevuti.
+++
