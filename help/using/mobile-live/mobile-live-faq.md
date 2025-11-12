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
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '1603'
ht-degree: 1%

---

# Domande frequenti {#mobile-live-faq}

>[!BEGINSHADEBOX]

* [Introduzione all’attività live](get-started-mobile-live.md)
* [Configurazione attività live](mobile-live-configuration.md)
* [Integrazione di Live Activity con Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* [Creare un’attività Live](create-mobile-live.md)
* **[Domande frequenti](mobile-live-faq.md)**
* [Rapporto campagna attività live](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

## Domande generali

+++Qual è la differenza tra un’attività live e una notifica push?

Le attività live forniscono aggiornamenti persistenti in tempo reale sullo schermo di blocco e su Dynamic Island senza richiedere agli utenti di sbloccare il dispositivo. Le notifiche push sono avvisi temporanei che scompaiono una volta ignorate. Le attività live rimangono visibili e possono essere aggiornate più volte fino alla loro scadenza esplicita.

+++

+++Quante attività live possono essere attive contemporaneamente?

Un&#39;app iOS può eseguire più attività live simultaneamente, comprese quelle che utilizzano lo stesso tipo `ActivityAttributes`.

Non esiste alcun limite imposto dagli sviluppatori sul numero di attività live di un determinato tipo di attributo che possono esistere. Puoi iniziare tutti i passaggi necessari per la logica dell’app, ad esempio uno per consegna o corsa in corso. Tuttavia, iOS applica un limite a livello di sistema sul numero di attività live che possono essere attive o visibili contemporaneamente.

In pratica:

* In genere iOS supporta fino a cinque attività live simultanee per app.

* Se superi questo numero, il sistema potrebbe interrompere la visualizzazione di alcune attività o terminare quelle precedenti per risparmiare risorse.

* Ogni attività Live ha un `Activity.id` univoco, che consente di aggiornarlo o terminarlo singolarmente.

+++

+++Gli utenti devono avere l’app aperta per ricevere gli aggiornamenti delle attività live?

No. Le attività live possono essere avviate, aggiornate e terminate in remoto anche quando l’app è completamente chiusa, uno dei principali vantaggi della funzione.

+++

+++Quali versioni di iOS supportano le attività live?

* iOS 16.1+: supporto di base per le attività live
* iOS 17.2+: funzionalità push-to-start (avvio in remoto senza aprire l’app)
* iOS 18+: supporto dei canali di trasmissione per attività live basate sul pubblico
+++

+++Per quanto tempo un’attività live può rimanere attiva?

Apple limita le attività live a **8 ore di aggiornamenti attivi**. Dopo di che, il sistema termina automaticamente l&#39;attività, anche se può rimanere visibile in uno stato statico per un massimo di **12 ore aggiuntive** prima della rimozione. Puoi anche terminare un&#39;attività live prima impostando un `dismissalDate` o chiamando esplicitamente `activity.end()` nell&#39;app.

+++

### Domande per sviluppatori

+++Devo creare un’estensione widget separata per le attività live?

Sì.  Le attività live vengono visualizzate tramite WidgetKit, pertanto devi creare un&#39;estensione widget nel progetto Xcode e implementare `ActivityConfiguration`.
[Ulteriori informazioni sulla configurazione dei widget](mobile-live-configuration-sdk.md)

+++

+++È possibile utilizzare la stessa classe `LiveActivityAttributes` per le attività Live locali e remote?

Sì.  La stessa classe di attributi funziona sia per le attività live avviate in locale che per quelle avviate in remoto (push-to-start). È necessario assicurarsi di registrarlo con `Messaging.registerLiveActivity()`.

+++

+++Cosa succede se invio un aggiornamento per un’attività live che non esiste?

Se si invia un evento di aggiornamento o di fine per un `liveActivityID` o un `channelID` inesistente, la richiesta non riuscirà nel dispositivo. Assicurati sempre di tenere traccia delle attività live attive per ogni utente.

+++

+++Posso testare le attività live nel simulatore iOS?

Sì, puoi testare le attività live avviate in locale o in remoto in iOS Simulator.

* **Locale**: ciò include la creazione, l&#39;aggiornamento e la fine delle attività live direttamente dall&#39;app tramite **API ActivityKit**.

* **Remoto**: per testare la funzionalità delle attività live in remoto, integra il SDK di messaggistica nell&#39;app e utilizza le API di esecuzione fornite per inviare l&#39;avvio, l&#39;aggiornamento e la fine remoti al dispositivo di prova o al simulatore iOS. Allo stesso modo in cui le notifiche push possono essere testate al momento con l’integrazione degli SDK di Adobe.

+++

+++Come posso gestire gli aggiornamenti quando l’app è in background?

Il SDK gestisce questo processo automaticamente. Una volta registrata, le attività live ricevono gli aggiornamenti anche quando l’app viene terminata. Non sono necessarie modalità di sfondo aggiuntive.
+++

+++Differenza tra `liveActivityID` e `channelID`

* `liveActivityID`: utilizzato per singole attività live (unitarie) mirate a utenti specifici. Ogni ID rappresenta un’istanza Live Activity univoca.
* `channelID`: utilizzato per le attività di trasmissione Live inviate al pubblico. Tutti gli utenti del pubblico ricevono gli stessi aggiornamenti sullo stesso canale.
+++

+++È possibile personalizzare l’aspetto di Dynamic Island separatamente dalla schermata di blocco?

Sì.  `ActivityConfiguration` dispone di chiusure separate per il contenuto Schermo di blocco e per il contenuto Isola dinamica (stati espansi, compatti e minimi), ciascuna progettazione in modo indipendente.
+++

+++È necessario memorizzare manualmente i token di push?

No. Quando si registra un tipo di attività Live con `Messaging.registerLiveActivity()`, SDK raccoglie e gestisce automaticamente i token push.
+++

### Domande dell’addetto marketing

+++Posso personalizzare il contenuto di un’attività live per ogni utente in una campagna di trasmissione?

Le campagne di trasmissione inviano lo stesso contenuto a tutti gli utenti del pubblico. Per i contenuti personalizzati, utilizza campagne unitarie (transazionali) indirizzate a singoli utenti.
+++

+++Come posso sapere se la mia attività live è stata consegnata correttamente?

[Monitora le analisi delle campagne](../reports/campaign-global-report-cja-activity.md) in Adobe Journey Optimizer. Puoi tenere traccia delle percentuali di consegna, degli errori e delle metriche di coinvolgimento. Inoltre, considera l’implementazione di eventi di analisi personalizzati nell’app.
+++

+++Posso pianificare le attività live in anticipo?

La chiamata API attiva immediatamente l’attività live. Tuttavia, puoi pianificare le chiamate API attraverso i sistemi back-end o utilizzare le funzionalità di orchestrazione di Journey Optimizer per temporizzarle in modo appropriato.
+++

+++Cosa succede se invio un evento &quot;start&quot; per un’attività live già esistente?

Quando avvii attività live in remoto tramite le API di esecuzione di Adobe:

* È possibile includere un&#39;intestazione `x-request-id` nella richiesta. Idealmente dovrebbe esserci una relazione uno-a-uno tra ogni `liveActivityID` e il corrispondente `x-request-id`. In questo modo, se vengono effettuate più richieste con la stessa combinazione di `x-request-id` e `liveActivityID`, sul dispositivo verrà avviata una sola attività Live e le richieste duplicate verranno ignorate.

* Se l&#39;intestazione `x-request-id` viene omessa, ogni richiesta viene trattata in modo indipendente, il che può comportare la creazione di più attività live con lo stesso `liveActivityID`. In questi casi, gli aggiornamenti futuri potrebbero non riuscire o applicarsi solo a una delle istanze attive.

* Il valore `x-request-id` non deve essere riutilizzato in `liveActivityIDs` diversi in richieste API separate.

+++

+++Posso testare A/B diverse esperienze di attività live?

Sì.  Crea più campagne con diverse strutture di contenuto e utilizza le funzioni di sperimentazione di Adobe Journey Optimizer per verificare quale funziona meglio. Assicurati che l&#39;app supporti tutte le varianti di stato del contenuto.

+++

+++Con quale frequenza devo aggiornare un’attività live?

Aggiorna solo quando cambiano informazioni significative, poiché aggiornamenti troppo frequenti possono svuotare la batteria e ridurre la qualità dell’esperienza utente. Per scenari in tempo reale, come il tracciamento delle consegne, in genere è accettabile ogni 30-60 secondi. Per contenuti che cambiano più lentamente, come i punteggi sportivi, aggiorna solo gli eventi significativi.

+++

+++Posso indirizzare gli utenti in base al fatto che abbiano Attività live abilitate?

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

+++Posso inviare aggiornamenti di attività live dai miei server back-end?

Sì, questo è il comportamento previsto. Il backend chiama l’API Adobe Journey Optimizer Headless per attivare eventi di attività live quando la logica di business lo richiede.

+++

+++È necessaria una campagna diversa per gli eventi di inizio, aggiornamento e fine?

No. Puoi utilizzare la stessa campagna e modificare il campo `event` nel payload. Tuttavia, alcune organizzazioni preferiscono campagne separate per un migliore tracciamento delle analisi.

+++

### Domande sulla risoluzione dei problemi

+++La mia attività live viene avviata ma non viene aggiornata. Quale potrebbe essere il problema?

Cause comuni:

* Mancata corrispondenza di `liveActivityID` o `channelID` tra le chiamate di avvio e di aggiornamento.
* I campi `content-state` non corrispondono allo struct `ContentState`.
* L&#39;attività live è già terminata.
* Problemi di connettività di rete sul dispositivo.

+++

+++Impossibile riconoscere il campo `attributes-type`. Cosa devo controllare?

* Assicurati che il nome della classe corrisponda esattamente a **1&rbrace; (distinzione maiuscole/minuscole) con il nome dello struct Swift**
* Verificare che la struttura sia definita e registrata correttamente
* Verifica la presenza di errori di battitura nel payload JSON
* Conferma che la versione dell&#39;app installata abbia l&#39;implementazione Live Activity

+++

+++Gli utenti visualizzano solo l’aggiornamento dell’attività live e non la notifica di avviso; si tratta di un problema noto?

No. Il campo `alert` è facoltativo e può essere soppresso da iOS in determinate condizioni, ad esempio in modalità Non disturbare. Le attività live possono essere aggiornate in modo silenzioso, che spesso corrisponde al comportamento previsto. Il campo di avviso è obbligatorio per l’invio di avvii remoti, altrimenti Apple lo tratta come una notifica in background silenziosa.

+++

+++Posso eliminare o cancellare tutte le attività live di un utente?

Devi inviare un evento &quot;finale&quot; per ogni attività live attiva. Tieni traccia delle attività live attive per ogni utente nei tuoi sistemi, in modo da poterle pulire correttamente.

+++

+++Il mio widget mostra &quot;Nessun dato&quot; anche se ho inviato un aggiornamento. Quale potrebbe essere il problema?

* Verificare che l&#39;implementazione del widget acceda correttamente a `context.state` e `context.attributes`.
* Controlla che i valori predefiniti o gli stati di errore siano gestiti nell&#39;interfaccia del widget.
* Utilizzare il protocollo `LiveActivityAssuranceDebuggable` per eseguire il debug dello schema.
* Esegui il test con Adobe Assurance per verificare se i dati vengono ricevuti.
+++
