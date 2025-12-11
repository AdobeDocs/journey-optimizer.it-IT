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
source-git-commit: 578950270213177b4d4cc67bad8ae627e440ff44
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 16%

---

# Risolvere i problemi relativi all’esecuzione live del percorso {#troubleshooting-execution}

In questa sezione, scopri come risolvere i problemi relativi agli eventi di percorso, verificare se i profili sono entrati nel percorso, come ci si sposta e se i messaggi vengono inviati.

È inoltre possibile risolvere gli errori prima di testare o pubblicare un percorso. Scopri come [in questa pagina](troubleshooting.md).

Se utilizzi azioni in entrata, scopri come risolverle [in questa pagina](troubleshooting-inbound.md).

## Verifica che gli eventi siano inviati correttamente {#checking-that-events-are-properly-sent}

Il punto di partenza di un percorso è sempre un evento. Puoi eseguire i test utilizzando strumenti come Postman.

Puoi verificare se la chiamata API inviata tramite questi strumenti viene inviata correttamente o meno. Se ricevi nuovamente un errore, significa che la chiamata presenta un problema. Controlla di nuovo il payload, l’intestazione (e in particolare l’ID organizzazione) e l’URL di destinazione. Puoi chiedere all’amministratore qual è l’URL corretto da utilizzare.

Gli eventi non vengono inviati direttamente dall’origine ai percorsi. In effetti, i percorsi si basano sulle API Streaming Ingestion di Adobe Experience Platform. Di conseguenza, in caso di problemi relativi agli eventi, puoi fare riferimento alla [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=it){target="_blank"} per la risoluzione dei problemi relativi alle API Streaming Ingestion.

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

&#x200B;>>
**Per i percorsi di qualificazione del pubblico con pubblico in streaming**: se utilizzi un&#39;attività di qualificazione del pubblico come punto di ingresso del percorso, tieni presente che non tutti i profili idonei per il pubblico entreranno necessariamente nel percorso a causa di fattori di tempistica, uscite rapide dal pubblico o se i profili erano già presenti nel pubblico prima della pubblicazione. Ulteriori informazioni sulle [considerazioni sulla tempistica di qualificazione del pubblico in streaming](audience-qualification-events.md#streaming-entry-caveats).

## Risolvere i problemi relativi alle transizioni della modalità di test {#troubleshooting-test-transitions}

Se i profili di test non riescono ad avanzare nel percorso in modalità di test o il flusso visivo non visualizza frecce verdi che indicano la progressione del passaggio, il problema può essere correlato alla convalida della transizione. Questa sezione fornisce indicazioni sulla diagnosi e la risoluzione di problemi comuni relativi alla modalità di test.

### Profili di test non in avanzamento

Se i profili di test entrano nel percorso ma non superano il passaggio iniziale, verifica quanto segue:

* **Data di inizio Percorso** - La causa più comune è quando la data di inizio del percorso è impostata in futuro. I profili di test vengono eliminati immediatamente se l&#39;ora corrente non rientra nella finestra [date/ore di inizio e fine](journey-properties.md#dates) configurata nel percorso. Per risolvere:
   * Verifica che la data di inizio del percorso non sia impostata in futuro
   * Assicurarsi che l&#39;ora corrente rientri nell&#39;intervallo di date attivo del percorso
   * Se necessario, aggiorna le proprietà del percorso per regolare la data di inizio

* **Configurazione profilo di test** - Verificare che il profilo sia contrassegnato correttamente come profilo di test in Adobe Experience Platform. Per ulteriori informazioni, vedere [come creare profili di test](../audience/creating-test-profiles.md).

* **Spazio dei nomi identità** - Verificare che lo spazio dei nomi identità utilizzato nella configurazione dell&#39;evento corrisponda allo spazio dei nomi del profilo di test.

### Indicatori di transizione nulli

Durante la risoluzione dei problemi tecnici, è possibile che nei dettagli tecnici del percorso venga rilevata una proprietà `isValidTransition` impostata su null. Questa proprietà di sola interfaccia utente non influisce sull’elaborazione back-end o sulle prestazioni del percorso. Tuttavia, un valore null può indicare:

* **Configurazione errata del Percorso** - La data di inizio del percorso è impostata in futuro, causando l&#39;eliminazione silenziosa degli eventi di test
* **Transizione danneggiata** - In rari casi, potrebbe essere necessario riconnettere i nodi del percorso

Se riscontri problemi di transizione persistenti:

1. Verifica che la data di inizio del percorso sia corrente
1. Disattivare e riattivare la modalità di test
1. Se il problema persiste, è consigliabile duplicare i nodi del percorso interessati e riconnetterli
1. Per i casi non risolti, contatta il supporto con i registri del percorso, gli ID profilo interessati e i dettagli sulla transizione null

>[!NOTE]
>
>Ricorda che gli eventi inviati al di fuori della finestra della data attiva del percorso vengono automaticamente scartati senza alcun messaggio di errore. Verifica sempre la configurazione degli intervalli di percorso prima di risolvere i problemi relativi alla progressione del profilo di test.

## Controllare il modo in cui le persone si spostano nel percorso {#checking-how-people-navigate-through-the-journey}

Il reporting di percorso misura il progresso delle persone all&#39;interno di un percorso. È facile identificare in che punto una persona si è fermata e per quale motivo.

Di seguito sono riportati alcuni elementi da verificare:

* È dovuto a una condizione che esclude la persona? Ad esempio, la condizione è “genere = uomo” e la persona in oggetto è una donna. Questo controllo può essere eseguito da un utente aziendale, se la condizione non è troppo complessa.
* È dovuto a una chiamata a un’origine dati che non risponde? Quando il percorso è in modalità di test, queste informazioni possono essere visualizzate nei registri in modalità di test. Quando il percorso è live, un amministratore può testare le chiamate dirette all’origine dati e verificare la risposta ricevuta. Un amministratore può anche duplicare il percorso e testarlo.

## Verifica che i messaggi siano inviati correttamente {#checking-that-messages-are-sent-successfully}

Se gli individui si spostano nel modo giusto all’interno del percorso ma non ricevono i messaggi che dovrebbero ricevere, puoi verificare se:

* [!DNL Journey Optimizer] ha preso correttamente in considerazione la richiesta di invio del messaggio. Gli utenti aziendali possono accedere al messaggio che doveva essere stato inviato e verificare se l’ora dell’esecuzione più recente corrisponde all’orario di esecuzione del percorso. Può anche controllare le ultime chiamate/eventi API ricevuti.
* [!DNL Journey Optimizer] ha inviato correttamente il messaggio. Controlla la segnalazione del percorso per assicurarti che non ci siano errori.

Nel caso di un messaggio inviato tramite un’azione personalizzata, l’unica cosa che è possibile controllare durante il test di percorso è il fatto che la chiamata del sistema dell’azione personalizzata conduca o meno a un errore. Se la chiamata al sistema esterno associata all’azione personalizzata non genera un errore ma non causa l’invio di un messaggio, è necessario eseguire alcune indagini sul lato del sistema esterno.

## Informazioni sulle voci duplicate negli eventi dei passaggi del Percorso {#duplicate-step-events}

### Perché trovo più voci con gli stessi ID istanza, profilo, nodo e richiesta di percorso?

Quando si esegue una query sui dati degli eventi delle fasi del Percorso, è possibile osservare occasionalmente voci di registro duplicate per la stessa esecuzione del percorso. Queste voci condividono valori identici per:

* `profileID` - Identità del profilo
* `instanceID` - Identificatore dell&#39;istanza del percorso
* `nodeID` - Nodo percorso specifico
* `requestID` - Identificatore della richiesta

Tuttavia, queste voci hanno **valori `_id` diversi**, che è l&#39;indicatore chiave che distingue questo scenario dalla duplicazione effettiva dei dati.

### Da cosa deriva questo comportamento?

Ciò si verifica a causa delle operazioni di scalabilità automatica back-end (o &quot;ribilanciamento&quot;) nell’architettura dei microservizi di Adobe Journey Optimizer. Durante i periodi di carico elevato o di ottimizzazione del sistema:

1. Un evento del passaggio di percorso inizia l’elaborazione e viene registrato nel set di dati Eventi del passaggio di Percorso
2. Un&#39;operazione di ridimensionamento automatico ridistribuisce il carico di lavoro tra le istanze del servizio
3. Lo stesso evento può essere rielaborato da un&#39;altra istanza del servizio, creando una seconda voce di registro con un `_id` diverso

Si tratta di un comportamento di sistema previsto e **funziona come previsto**.

### Vi è un impatto sull’esecuzione del percorso o sulla consegna dei messaggi?

**No.** L&#39;impatto è limitato solo alla registrazione. Adobe Journey Optimizer dispone di meccanismi di deduplicazione incorporati a livello di esecuzione dei messaggi che garantiscono:

* A ciascun profilo viene inviato un solo messaggio (e-mail, SMS, notifica push, ecc.)
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

Se le discrepanze persistono, contatta il supporto Adobe con le schermate delle schede Panoramica e Sfoglia per ulteriori informazioni.
