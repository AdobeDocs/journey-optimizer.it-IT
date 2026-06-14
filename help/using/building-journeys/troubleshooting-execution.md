---
solution: Journey Optimizer
product: journey optimizer
title: Risolvere i problemi relativi all’esecuzione live del percorso
description: Scopri come risolvere gli errori nell’esecuzione di un percorso live
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: risoluzione dei problemi, risoluzione dei problemi, percorso, controllo, errori
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/2YZ6Cjph9Le-HtwKdz4GBgEdhwIMPpVtj9yWKlV3hQ4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 2263
ht-degree: 11%

---

# Risolvere i problemi relativi all’esecuzione live del percorso {#troubleshooting-execution}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come risolvere i problemi relativi all&#39;esecuzione di un percorso live, tra cui la verifica dell&#39;invio degli eventi, la conferma dell&#39;immissione e dell&#39;avanzamento dei profili nel percorso e la verifica della consegna dei messaggi.

>[!ENDSHADEBOX]

In questa sezione, scopri come risolvere i problemi relativi agli eventi di percorso, verificare se i profili sono entrati nel percorso, come ci si sposta e se i messaggi vengono inviati.

È inoltre possibile risolvere gli errori prima di testare o pubblicare un percorso. Scopri come [in questa pagina](troubleshooting.md).

Se utilizzi azioni in entrata, scopri come risolverle [in questa pagina](troubleshooting-inbound.md).

## Verifica che gli eventi siano inviati correttamente {#checking-that-events-are-properly-sent}

Il punto di partenza di un percorso è sempre un evento. Puoi eseguire i test utilizzando strumenti come Postman.

Puoi verificare se la chiamata API inviata tramite questi strumenti viene inviata correttamente o meno. Se ricevi nuovamente un errore, significa che la chiamata presenta un problema. Controlla di nuovo il payload, l’intestazione (e in particolare l’ID organizzazione) e l’URL di destinazione. Puoi chiedere all’amministratore qual è l’URL corretto da utilizzare.

Gli eventi non vengono inviati direttamente dall’origine ai percorsi. I percorsi si basano infatti sulle API Streaming Ingestion di [!DNL Adobe Experience Platform]. Di conseguenza, in caso di problemi relativi agli eventi, puoi fare riferimento alla [[!DNL Adobe Experience Platform] documentazione](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} per la risoluzione dei problemi relativi alle API Streaming Ingestion.

Se il percorso non è in grado di abilitare la modalità di test con l&#39;errore `ERR_MODEL_RULES_16`, verificare che l&#39;evento utilizzato includa uno spazio dei nomi [identità](../audience/get-started-identity.md) quando si utilizza un&#39;azione del canale.

Lo spazio dei nomi dell’identità viene utilizzato per identificare in modo univoco i profili di test. Ad esempio, se per identificare i profili di test si utilizza l&#39;e-mail, deve essere selezionato lo spazio dei nomi dell&#39;identità **E-mail**. Se l&#39;identificatore univoco è il numero di telefono, deve essere selezionato lo spazio dei nomi dell&#39;identità **Telefono**.

## Controlla se le persone entrano nel percorso {#checking-if-people-enter-the-journey}

Il reporting percorso misura le entrate delle persone in un percorso in tempo reale.

Se l’invio dell’evento è stato completato con successo ma non viene visualizzata alcuna entrata nel percorso, significa che si sono verificati errori tra l’invio dell’evento e la ricezione dell’evento nel percorso.

Per iniziare la risoluzione dei problemi, consulta le domande seguenti:

* Hai la certezza che il percorso in cui prevedevi che arrivasse l’evento fosse in modalità di test o live?
* Hai salvato l’evento prima di copiare il payload dall’anteprima del payload?
* Il payload dell’evento contiene un ID evento?
* Hai raggiunto l’URL giusto?
* Hai seguito la struttura del payload delle API per l’acquisizione in streaming utilizzando l’anteprima della struttura del payload nel riquadro di configurazione dell’evento? Consulta [questa pagina](../event/about-creating.md#preview-the-payload).
* Hai utilizzato le coppie chiave-valore corrette nell’intestazione dell’evento?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

* **Condizione evento e tipi di dati dello schema** - Verificare che i tipi di dati utilizzati nella condizione evento (regola) corrispondano allo schema evento. I tipi non corrispondenti (ad esempio, stringa vs. numero intero) causano un errore di valutazione della regola e l’eliminazione degli eventi. Vedere [Verifica identità evento](#verify-event-identity-and-rule-data-types).

* **Evento ignorato - condizione di qualifica non soddisfatta** - Per gli eventi basati su regole, se la **condizione di qualifica** non è soddisfatta dal payload dell&#39;evento (ad esempio, se un campo obbligatorio è vuoto o mancante oppure una condizione come `isNotEmpty` in un campo non riesce), l&#39;evento è **ricevuto ma scartato** e il percorso non viene attivato. Registri e tracce Splunk possono mostrare che l&#39;evento è stato ricevuto ma scartato perché non soddisfa la condizione di qualifica, con codici di eliminazione come `notSuitableInitialEvent`. Questo è il comportamento previsto: se la condizione di qualifica non viene soddisfatta, l’evento verrà scartato e il percorso non verrà attivato per quel profilo. Verifica che il payload dell’evento contenga i campi e i valori previsti e che la regola nella configurazione dell’evento corrisponda ai dati inviati. Se l&#39;evento viene attivato da una **azione personalizzata** da un altro percorso, vedere [Gestione degli eventi di eliminazione e dei timeout di inattività](../action/troubleshoot-custom-action.md#handling-discard-events-and-idle-timeouts) nella risoluzione dei problemi relativi alle azioni personalizzate.

>>
**Per i percorsi di qualificazione del pubblico con pubblico in streaming**: se utilizzi un&#39;attività di qualificazione del pubblico come punto di ingresso del percorso, tieni presente che non tutti i profili idonei per il pubblico entreranno necessariamente nel percorso a causa di fattori di tempistica, uscite rapide dal pubblico o se i profili erano già presenti nel pubblico prima della pubblicazione. Ulteriori informazioni sulle [considerazioni sulla tempistica di qualificazione del pubblico in streaming](audience-qualification-events.md#streaming-entry-caveats).

### Verifica identità evento {#verify-event-identity-and-rule-data-types}

Durante la configurazione di un percorso basato su eventi, verifica che il campo di identità del payload corrisponda allo spazio dei nomi [ selezionato nell&#39;evento](../event/about-creating.md#select-the-namespace). Se l&#39;evento include campi per la corrispondenza del profilo, verificare la corrispondenza tra maiuscole e minuscole **lettere** e il tipo di dati **** nella condizione dell&#39;evento con i dati in entrata. Se, ad esempio, lo schema evento definisce `roStatus` come stringa, anche la regola di percorso deve valutarlo come stringa. I tipi di dati non corrispondenti (ad esempio, stringa vs. numero intero) causano un errore di valutazione della regola e l’eliminazione di eventi validi. Analogamente, se l&#39;evento ha una **condizione di qualifica** (ad esempio, un campo non deve essere vuoto), gli eventi che non soddisfano tale condizione vengono **scartati** e non attivano il percorso; i registri possono mostrare codici di eliminazione come `notSuitableInitialEvent`.

Per convalidare la condizione evento in [!DNL Journey Optimizer], utilizza l&#39;anteprima del payload nella configurazione dell&#39;evento e assicurati che i tipi e i valori nella regola corrispondano alla struttura del payload. Scopri come [visualizzare in anteprima il payload](../event/about-creating.md#preview-the-payload) e [configurare gli eventi basati su regole](../event/about-creating.md).

## Risolvere i problemi relativi alle transizioni della modalità di test {#troubleshooting-test-transitions}

Se i profili di test non riescono ad avanzare nel percorso in modalità di test o il flusso visivo non visualizza frecce verdi che indicano la progressione del passaggio, il problema può essere correlato alla convalida della transizione. Questa sezione fornisce indicazioni sulla diagnosi e la risoluzione di problemi comuni relativi alla modalità di test.

### Profili di test non in avanzamento

Se i profili di test entrano nel percorso ma non superano il passaggio iniziale, verifica quanto segue:

* **Data di inizio Percorso** - La causa più comune è quando la data di inizio del percorso è impostata in futuro. I profili di test vengono eliminati immediatamente se l&#39;ora corrente non rientra nella finestra [date/ore di inizio e fine](journey-properties.md#dates) configurata nel percorso. Per risolvere:
   * Verifica che la data di inizio del percorso non sia impostata in futuro
   * Assicurarsi che l&#39;ora corrente rientri nell&#39;intervallo di date attivo del percorso
   * Se necessario, aggiorna le proprietà del percorso per regolare la data di inizio

* **Configurazione profilo di test** - Verificare che il profilo sia contrassegnato correttamente come profilo di test in [!DNL Adobe Experience Platform]. Per ulteriori informazioni, vedere [come creare profili di test](../audience/creating-test-profiles.md).

* **Spazio dei nomi identità** - Verificare che lo spazio dei nomi identità utilizzato nella configurazione dell&#39;evento corrisponda allo spazio dei nomi del profilo di test.

### Indicatori di transizione nulli

Durante la risoluzione dei problemi tecnici, è possibile che nei dettagli tecnici del percorso venga rilevata una proprietà `isValidTransition` impostata su null. Questa proprietà di sola interfaccia utente non influisce sull’elaborazione back-end o sulle prestazioni del percorso. Tuttavia, un valore null può indicare:

* **Configurazione errata del Percorso** - La data di inizio del percorso è impostata in futuro, causando l&#39;eliminazione silenziosa degli eventi di test
* **Transizione danneggiata** - In rari casi, potrebbe essere necessario riconnettere i nodi del percorso

Se riscontri problemi di transizione persistenti:

1. Verifica che la data di inizio del percorso sia corrente
1. Disattivare e riattivare la modalità di test
1. Se il problema persiste, è consigliabile duplicare i nodi del percorso interessati e riconnetterli
1. Per i casi non risolti, [contatta il supporto](../start/user-interface.md#support-ticket-guidelines) con i registri di percorso, gli ID profilo interessati e i dettagli sulla transizione null

>[!NOTE]
>
>Ricorda che gli eventi inviati al di fuori della finestra della data attiva del percorso vengono automaticamente scartati senza alcun messaggio di errore. Verifica sempre la configurazione degli intervalli di percorso prima di risolvere i problemi relativi alla progressione del profilo di test.

## Controllare il modo in cui le persone si spostano nel percorso {#checking-how-people-navigate-through-the-journey}

Il reporting di percorso misura il progresso delle persone all&#39;interno di un percorso. È facile identificare in che punto una persona si è fermata e per quale motivo.

Di seguito sono riportati alcuni elementi da verificare:

* È dovuto a una condizione che esclude la persona? Ad esempio, la condizione è “genere = uomo” e la persona in oggetto è una donna. Questo controllo può essere eseguito da un utente aziendale, se la condizione non è troppo complessa.
* È dovuto a una chiamata a un’origine dati che non risponde? Quando il percorso è in modalità di test, queste informazioni possono essere visualizzate nei registri in modalità di test. Quando il percorso è live, un amministratore può testare le chiamate dirette all’origine dati e verificare la risposta ricevuta. Un amministratore può anche duplicare il percorso e testarlo.

## Eventi eliminati a causa di un&#39;istanza di percorso bloccata {#max-instance-stack-events-reached}

Se vengono visualizzati eventi scartati con il motivo `maxInstanceStackEventsReached`, il runtime di percorso ha raggiunto il limite interno di 10 eventi per stack di eventi per profilo per una versione di percorso specifica. Si tratta di un guardrail di sicurezza che impedisce l’accumulo di troppi eventi in sospeso mentre è ancora in corso l’elaborazione di un altro evento per lo stesso profilo.

**non** è un limite di intervallo di tempo o di velocità effettiva. Si verifica quando l’istanza di percorso del profilo è bloccata su un passaggio di lunga durata (ad esempio, un lungo periodo di attesa, un arricchimento o nuovi tentativi di azione personalizzati) e gli eventi per lo stesso profilo, utilizzati anche in quel percorso, si accumulano oltre il limite di 10 eventi.

Per identificarlo, eseguire una query sugli eventi dei passaggi del percorso in cui il motivo dell&#39;eliminazione è uguale a `maxInstanceStackEventsReached` (ad esempio, in `serviceEvents.stateMachine.eventType` o campi simili). Ulteriori informazioni sui tipi di evento eliminati sono disponibili nell&#39;elenco dei campi evento [passaggio](../reports/sharing-field-list.md#discarded-events).

**Operazioni possibili**

* Riduci le lunghe attese o i passaggi lenti sui percorsi che possono riattivarsi frequentemente.
* Deduplicare o annullare gli eventi a monte quando possibile.
* Suddividi gli scenari a lunga durata in più percorsi per evitare lo stacking.

## Verifica che i messaggi siano inviati correttamente {#checking-that-messages-are-sent-successfully}

Se gli individui si spostano nel modo giusto all’interno del percorso ma non ricevono i messaggi che dovrebbero ricevere, puoi verificare se:

* [!DNL Journey Optimizer] ha preso correttamente in considerazione la richiesta di invio del messaggio. Gli utenti aziendali possono accedere al messaggio che doveva essere stato inviato e verificare se l’ora dell’esecuzione più recente corrisponde all’orario di esecuzione del percorso. Può anche controllare le ultime chiamate/eventi API ricevuti.
* [!DNL Journey Optimizer] ha inviato correttamente il messaggio. Controlla la segnalazione del percorso per assicurarti che non ci siano errori.

Nel caso di un messaggio inviato tramite un’azione personalizzata, l’unica cosa che è possibile controllare durante il test di percorso è il fatto che la chiamata del sistema dell’azione personalizzata conduca o meno a un errore. Se la chiamata al sistema esterno associata all’azione personalizzata non genera un errore ma non causa l’invio di un messaggio, è necessario eseguire alcune indagini sul lato del sistema esterno.

## Informazioni sulle voci duplicate negli eventi dei passaggi del Percorso {#duplicate-step-events}

Utilizzare questa sezione per comprendere il motivo per cui le righe duplicate possono essere visualizzate negli Eventi dei passaggi del Percorso.

### Perché trovo più voci con lo stesso ID istanza, profilo, nodo e richiesta di percorso?

Quando si esegue una query sui dati degli eventi delle fasi del Percorso, è possibile osservare occasionalmente voci di registro duplicate per la stessa esecuzione del percorso. Queste voci condividono valori identici per:

* `profileID` - Identità del profilo
* `instanceID` - Identificatore dell&#39;istanza del percorso
* `nodeID` - Nodo percorso specifico
* `requestID` - Identificatore della richiesta

Tuttavia, queste voci hanno **valori `_id` diversi**, che è l&#39;indicatore chiave che distingue questo scenario dalla duplicazione effettiva dei dati.

### Da cosa deriva questo comportamento?

Ciò si verifica a causa di operazioni di ridimensionamento automatico back-end (detto anche &quot;ribilanciamento&quot;) nell&#39;architettura dei microservizi di [!DNL Adobe Journey Optimizer]. Durante i periodi di carico elevato o di ottimizzazione del sistema:

1. Un evento del passaggio di percorso inizia l’elaborazione e viene registrato nel set di dati Eventi del passaggio di Percorso
2. Un&#39;operazione di ridimensionamento automatico ridistribuisce il carico di lavoro tra le istanze del servizio
3. Lo stesso evento può essere rielaborato da un&#39;altra istanza del servizio, creando una seconda voce di registro con un `_id` diverso

Si tratta di un comportamento di sistema previsto e **funziona come previsto**.

### Vi è un impatto sull’esecuzione del percorso o sulla consegna dei messaggi?

**No** L’impatto è limitato solo alla registrazione. [!DNL Adobe Journey Optimizer] dispone di meccanismi di deduplicazione incorporati a livello di esecuzione dei messaggi che garantiscono:

* Un solo messaggio (e-mail, SMS, notifica push, ecc.) viene inviato a ogni profilo
* Le azioni vengono eseguite una sola volta
* L&#39;esecuzione del percorso procede correttamente

È possibile verificare questa situazione eseguendo una query su `ajo_message_feedback_event_dataset` o controllando i registri di esecuzione dell&#39;azione. Si noterà che è stato effettivamente inviato un solo messaggio, nonostante le voci di evento del passaggio di percorso duplicate.

### Come posso identificare questi casi nelle mie query?

Durante l’analisi dei dati degli eventi dei passaggi del Percorso:

1. **Controllare il campo `_id`**: i duplicati a livello di sistema effettivi avrebbero lo stesso `_id`. Valori `_id` diversi indicano voci di registro separate dallo scenario di ribilanciamento descritto sopra.

2. **Verifica recapito messaggi**: riferimento incrociato con i dati di feedback del messaggio per confermare che è stato inviato un solo messaggio:

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **Raggruppa per identificatori univoci**: durante il conteggio delle esecuzioni, utilizza `_id` per ottenere conteggi accurati:

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### Cosa devo fare se osservo questo?

Si tratta di un comportamento normale del sistema e **non è richiesta alcuna azione**. La registrazione duplicata non indica un problema nella configurazione del percorso o nella consegna del messaggio.

Se stai creando rapporti o analisi basati su eventi dei passaggi del Percorso:

* Usa `_id` come chiave primaria per il conteggio degli eventi univoci
* Riferimento incrociato con i set di dati di feedback dei messaggi durante l’analisi della consegna dei messaggi
* Tieni presente che l’analisi dei tempi può mostrare le voci raggruppate in pochi secondi l’una dall’altra

Per ulteriori informazioni sull&#39;esecuzione di query sugli eventi dei passaggi del Percorso, vedere [Esempi di query](../reports/query-examples.md).

## Risolvere i problemi relativi alle discrepanze nelle metriche del dashboard {#dashboard-metrics}

Se le metriche visualizzate nel dashboard **Panoramica** non corrispondono al numero effettivo di percorsi nella scheda **Sfoglia**, verificare quanto segue:

* Assicurati che i percorsi in questione abbiano avuto traffico nelle ultime 24 ore, in quanto i percorsi senza attività recente vengono esclusi dal dashboard.
* Verifica di disporre delle autorizzazioni di accesso appropriate per visualizzare tutti i percorsi dell’organizzazione.
* Attendi fino a 30 minuti per l’aggiornamento delle metriche dopo aver apportato modifiche ai percorsi.

Se le discrepanze persistono, [contatta il supporto Adobe](../start/user-interface.md#support-ticket-guidelines) con le schermate delle schede Panoramica e Sfoglia per ulteriori informazioni.

## Parametri di tracciamento che mostrano segnaposto vuoti nei percorsi chiusi {#tracking-parameters-closed-journeys}

Se gli URL di tracciamento nelle e-mail inviate contengono segnaposto vuoti come `cid=em-acou-adob{}`, potrebbe essere impossibile risolvere un campo di contesto come `context.system.source.actionId`. Ciò si verifica in genere quando un percorso viene chiuso e non viene ripubblicato dopo una modifica rilevante del prodotto; solo i percorsi ripubblicati compilano correttamente questi campi di contesto negli URL di tracciamento.

Per risolvere il problema, ripubblicare il percorso ([crea una nuova versione e pubblicarla](publish-journey.md#journey-create-new-version)) oppure rimuovere il riferimento al campo di contesto interessato dai [parametri di tracciamento URL](../email/url-tracking.md) nella configurazione del canale o nel contenuto dell&#39;e-mail.
