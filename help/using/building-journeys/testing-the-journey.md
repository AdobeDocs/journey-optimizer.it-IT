---
solution: Journey Optimizer
product: journey optimizer
title: Testa il percorso
description: Scopri come testare il percorso
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: test, percorso, controllo, errore, risoluzione dei problemi
exl-id: 9937d9b5-df5e-4686-83ac-573c4eba983a
version: Journey Orchestration
source-git-commit: 36c44728172313492898bf3374a37512e4c19789
workflow-type: tm+mt
source-wordcount: '1800'
ht-degree: 8%

---

# Testa il percorso{#testing_the_journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_test"
>title="Testa il percorso"
>abstract="Utilizza i profili di test per testare il percorso prima di pubblicarlo. Questo consente di analizzare il flusso dei singoli utenti nel percorso e risolvere eventuali problemi prima della pubblicazione."

Dopo aver creato il percorso, puoi testarlo prima di pubblicarlo. Journey Optimizer offre la &quot;modalità di test&quot; come modo per visualizzare i profili di test mentre si spostano lungo il percorso, rilevando potenziali errori prima dell’attivazione. L’esecuzione di test rapidi consente di verificare il corretto funzionamento dei percorsi e di pubblicarli in modo affidabile.

Solo i profili di test possono entrare in un percorso in modalità di test. Puoi creare nuovi profili di test o trasformare quelli esistenti in profili di test. Ulteriori informazioni sui profili di test in [questa sezione](../audience/creating-test-profiles.md).

>[!NOTE]
>
>Prima di eseguire il test del percorso, è necessario risolvere tutti gli eventuali errori. Scopri come controllare gli errori prima di eseguire il test in [questa sezione](../building-journeys/troubleshooting.md).

## Note importanti {#important_notes}

### Limitazioni generali

* **Solo profili di test** - Solo i singoli utenti contrassegnati come &quot;profili di test&quot; nel servizio Profilo cliente in tempo reale possono accedere a un percorso in modalità di test. [Scopri come creare profili di test](../audience/creating-test-profiles.md).
* **Requisito spazio dei nomi** - La modalità di test è disponibile solo per i percorsi bozza che utilizzano uno spazio dei nomi. La modalità di test deve verificare se una persona che entra nel percorso è un profilo di test o meno e quindi deve essere in grado di raggiungere Adobe Experience Platform.
* **Limite profilo** - Un massimo di 100 profili di test può entrare in un percorso durante una singola sessione di test.
* **Attivazione evento** - Gli eventi possono essere attivati solo dall&#39;interfaccia. Gli eventi non possono essere attivati da sistemi esterni che utilizzano un’API.
* **Tipi di pubblico per caricamento personalizzati** - La modalità di test Percorso non supporta l&#39;arricchimento degli attributi [Pubblico per caricamento personalizzato](../audience/custom-upload.md).

### Comportamento durante e dopo il test

* **Disabilitazione della modalità di test** - Quando si disabilita la modalità di test, tutti i profili attualmente presenti o precedentemente immessi nel percorso vengono rimossi e il reporting viene cancellato.
* **Flessibilità di riattivazione** - È possibile abilitare e disabilitare la modalità di test il numero di volte necessario.
* **Disattivazione automatica**: i Percorsi che rimangono inattivi in modalità di test per **per una settimana** tornano automaticamente allo stato Bozza per ottimizzare le prestazioni ed evitare l&#39;utilizzo di risorse obsolete.
* **Modifica e pubblicazione** - Se la modalità di test è attiva, non è possibile modificare il percorso. Tuttavia, puoi pubblicare direttamente il percorso, senza dover disattivare prima la modalità di test.

### Execution

* **Comportamento divisione** - Quando il percorso raggiunge una divisione, il ramo superiore è sempre selezionato. Riordinare i rami se si desidera testare un percorso diverso.
* **Tempistica evento** - Se il percorso include*più eventi, attiva ogni evento in sequenza.L&#39;invio di un evento troppo presto (prima del termine del primo nodo di attesa) o troppo tardi (dopo il timeout configurato) comporta l&#39;eliminazione dell&#39;evento e l&#39;invio del profilo a un percorso di timeout. Conferma sempre che qualsiasi riferimento ai campi del payload dell’evento rimanga valido inviando il payload all’interno della finestra definita
* **Intervallo date attivo** - Assicurarsi che la finestra [date/ore di inizio e fine](journey-properties.md#dates) configurata nel percorso includa l&#39;ora corrente all&#39;avvio della modalità di test. In caso contrario, gli eventi di test attivati vengono automaticamente scartati.
* **Eventi di reazione** - Per gli eventi di reazione con timeout, il tempo di attesa minimo e predefinito è di 40 secondi.
* **Set di dati di test** - Gli eventi attivati in modalità di test sono archiviati in set di dati dedicati etichettati come segue: `JOtestmode - <schema of your event>`

<!--
* Fields from related entities are hidden from the test mode.
-->

## Attiva la modalità di test

Per utilizzare la modalità di test, effettua le seguenti operazioni:

1. Per attivare la modalità di test, fare clic sul pulsante **[!UICONTROL Modalità di test]** nell&#39;angolo in alto a destra.

   ![](assets/journeytest1.png)

1. Se nel percorso è presente almeno un&#39;attività **Wait**, impostare il parametro **[!UICONTROL Wait time]** per definire la durata di ogni attività di attesa e di ogni timeout evento in modalità di test. Il tempo predefinito è di 10 secondi per attese e timeout di eventi. In questo modo potrai ottenere rapidamente i risultati del test.

   ![](assets/journeytest_wait.png)

   >[!NOTE]
   >
   >Quando in un percorso viene utilizzato un evento di reazione con timeout, il valore predefinito e minimo del tempo di attesa è di 40 secondi. Consulta [questa sezione](../building-journeys/reaction-events.md).

1. Utilizza il pulsante **[!UICONTROL Attiva un evento]** per configurare e inviare eventi al percorso.

   ![](assets/journeyuctest1.png)

1. Configura i diversi campi previsti. Nel campo **Identificatore profilo** immettere il valore del campo utilizzato per identificare il profilo di test. Ad esempio, può essere l’indirizzo e-mail. Assicurati di inviare eventi relativi ai profili di test. Consulta [questa sezione](#firing_events).

   ![](assets/journeyuctest1-bis.png)

1. Dopo aver ricevuto gli eventi, fare clic sul pulsante **[!UICONTROL Mostra registro]** per visualizzare i risultati del test e verificarli. Consulta [questa sezione](#viewing_logs).

   ![](assets/journeyuctest2.png)

1. In caso di errori, disattiva la modalità di test, modifica il percorso e verificalo di nuovo. Una volta completati i test, puoi pubblicare il percorso. Consulta [questa pagina](../building-journeys/publish-journey.md).

## Attivare gli eventi {#firing_events}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_configuration"
>title="Configurare la modalità di test"
>abstract="Se il percorso contiene più eventi, utilizza l’elenco a discesa per selezionare un evento. Quindi, per ogni evento, configura i campi passati e l’esecuzione dell’invio dell’evento."

Utilizza il pulsante **[!UICONTROL Attiva un evento]** per configurare un evento che farà entrare una persona nel percorso.


### Prerequisiti {#trigger-events-prerequisites}

Come prerequisito, è necessario sapere quali profili sono contrassegnati come profili di test in Adobe Experience Platform. In effetti, la modalità di test consente solo questi profili nel percorso.

L&#39;evento deve contenere un ID. L’ID previsto dipende dalla configurazione dell’evento. Ad esempio, può essere un ECID o un indirizzo e-mail. Il valore di questa chiave deve essere aggiunto nel campo **Identificatore profilo**.

Se il percorso non è in grado di abilitare la modalità di test con l&#39;errore `ERR_MODEL_RULES_16`, verificare che l&#39;evento utilizzato includa uno spazio dei nomi [identità](../audience/get-started-identity.md) quando si utilizza un&#39;azione del canale.

Lo spazio dei nomi dell’identità viene utilizzato per identificare in modo univoco i profili di test. Ad esempio, se per identificare i profili di test si utilizza l&#39;e-mail, deve essere selezionato lo spazio dei nomi dell&#39;identità **E-mail**. Se l&#39;identificatore univoco è il numero di telefono, deve essere selezionato lo spazio dei nomi dell&#39;identità **Telefono**.

>[!NOTE]
>
>* Quando si attiva un evento in modalità di test, viene generato un evento reale, che si verifica quindi anche in un altro percorso che ascolta l’evento.
>
>* Assicurati che ogni evento in modalità di test sia attivato nell’ordine corretto e all’interno della finestra di attesa configurata. Ad esempio, in caso di attesa di 60 secondi, il secondo evento deve essere attivato solo dopo che è trascorso tale attesa di 60 secondi e prima della scadenza del limite di timeout.
>

### Configurazione evento {#trigger-events-configuration}

Se il percorso contiene più eventi, utilizza l’elenco a discesa per selezionare un evento. Quindi, per ogni evento, configura i campi passati e l’esecuzione dell’invio dell’evento. L’interfaccia ti aiuta a trasmettere le informazioni corrette nel payload dell’evento e a verificare che il tipo di informazioni sia corretto. La modalità di test salva gli ultimi parametri utilizzati in una sessione di test per un utilizzo successivo.

![](assets/journeytest4.png)

L’interfaccia ti consente di trasmettere parametri evento semplici. Se si desidera passare raccolte o altri oggetti avanzati nell&#39;evento, è possibile selezionare **[!UICONTROL Vista Codice]** per visualizzare l&#39;intero codice del payload e modificarlo. Ad esempio, puoi copiare e incollare le informazioni sull’evento preparate da un utente tecnico.

![](assets/journeytest5.png)

Un utente tecnico può inoltre utilizzare questa interfaccia per comporre payload di eventi e attivare eventi senza dover utilizzare uno strumento di terze parti.

Quando si fa clic sul pulsante **[!UICONTROL Invia]**, inizia il test. La progressione dell&#39;individuo nel percorso è rappresentata da un flusso visivo. Il tracciato diventa verde man mano che l&#39;individuo si sposta attraverso il percorso. Se si verifica un errore, nel passaggio corrispondente viene visualizzato un simbolo di avviso. È possibile posizionare il cursore su di esso per visualizzare ulteriori informazioni sull&#39;errore e accedere ai dettagli completi (se disponibili).

![](assets/journeytest6.png)

Quando selezioni un profilo di test diverso nella schermata di configurazione dell’evento ed esegui di nuovo il test, il flusso visivo viene cancellato e mostra il percorso del nuovo individuo.

Quando si apre un percorso in un test, il percorso visualizzato corrisponde all’ultimo test eseguito.

## Modalità di test per percorsi basati su regole {#test-rule-based}

La modalità di test è disponibile anche per i percorsi che utilizzano un evento basato su regole. Per ulteriori informazioni sugli eventi basati su regole, consulta [questa pagina](../event/about-events.md).

Quando si attiva un evento, la schermata **Configurazione evento** consente di definire i parametri dell&#39;evento da passare nel test. Per visualizzare la condizione dell’ID evento, fai clic sull’icona con la descrizione comando nell’angolo in alto a destra. È inoltre disponibile una descrizione comando accanto a ogni campo che fa parte della valutazione delle regole.

![](assets/jo-event8.png)

## Modalità di test per gli eventi di business {#test-business}

Quando utilizzi un [evento di business](../event/about-events.md), utilizza la modalità di test per attivare un singolo ingresso del profilo di test nel percorso, simulare l&#39;evento e passare l&#39;ID profilo corretto. Devi trasmettere i parametri dell’evento e l’identificatore del profilo di test che entrerà nel percorso in test. In modalità di test, non è disponibile la modalità &quot;Visualizzazione codice&quot; per i percorsi basata su eventi di business.

Si noti che quando si attiva per la prima volta un evento business, non è possibile modificare la definizione dell&#39;evento business nella stessa sessione di test. È possibile fare in modo che lo stesso individuo o un individuo diverso entri nel percorso passando lo stesso identificatore o un altro identificatore. Se si desidera modificare i parametri degli eventi business, è necessario interrompere e riavviare la modalità di test.

## Visualizzare i registri {#viewing_logs}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_logs"
>title="Registri della modalità di test"
>abstract="Il pulsante **Mostra registro** visualizza i risultati dei test in formato JSON. Questi risultati mostrano il numero di singoli utenti all’interno del percorso e il loro stato."

Il pulsante **[!UICONTROL Mostra registro]** consente di visualizzare i risultati del test. In questa pagina vengono visualizzate le informazioni correnti del percorso in formato JSON. Un pulsante consente di copiare interi nodi. Per aggiornare i risultati del test del percorso, è necessario aggiornare manualmente la pagina.

![](assets/journeytest3.png)


>[!NOTE]
>
>Nei registri di test, in caso di errore durante la chiamata a un sistema di terze parti (origine dati o azione), vengono visualizzati il codice di errore e la risposta all’errore.

Viene visualizzato il numero di individui (tecnicamente denominati istanze) attualmente all’interno del percorso. Di seguito sono riportate informazioni utili visualizzate per ogni utente:

* _Id_: ID interno dell&#39;individuo nel percorso. Può essere utilizzato a scopo di debug.
* _currentstep_: il passaggio in cui si trova l&#39;utente nel percorso. È consigliabile aggiungere etichette alle attività per identificarle più facilmente.
* _currentstep_ > fase: lo stato del percorso dell&#39;utente (in esecuzione, terminato, errore o timeout). Per ulteriori informazioni, consulta di seguito.
* _currentstep_ > _extraInfo_: descrizione dell&#39;errore e altre informazioni contestuali.
* _currentstep_ > _fetchErrors_: informazioni sugli errori di recupero dati che si sono verificati durante questo passaggio.
* _externalKeys_: valore della formula chiave definita nell&#39;evento.
* _arricchedData_: i dati recuperati dal percorso se il percorso utilizza origini dati.
* _transitionHistory_: elenco dei passaggi seguiti dall&#39;utente. Per gli eventi, viene visualizzato il payload.
* _actionExecutionErrors_: informazioni sugli errori che si sono verificati.

Di seguito sono riportati i diversi stati del percorso di un singolo utente:

* _In esecuzione_: l&#39;individuo è attualmente nel percorso.
* _Fine_: l&#39;utente si trova alla fine del percorso.
* _Errore_: l&#39;utente è stato arrestato nel percorso a causa di un errore.
* _Timeout_: l&#39;utente è stato arrestato nel percorso a causa di un passaggio che ha richiesto troppo tempo.

Quando un evento viene attivato utilizzando la modalità di test, viene generato automaticamente un set di dati con il nome dell’origine.

La modalità di test crea automaticamente un evento esperienza e lo invia a Adobe Experience Platform. Il nome dell’origine di questo evento esperienza è &quot;Eventi di test di Journey Orchestration&quot;.

