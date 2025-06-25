---
solution: Journey Optimizer
product: journey optimizer
title: Pianificare e avviare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come pianificare e avviare campagne orchestrate con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 50386efbb639031bfc41a0aa67f4f3b49603f03a
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 36%

---

# Pianificare e avviare le campagne orchestrate {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Pubblicare una campagna orchestrata"
>abstract="Per avviare la campagna, è necessario pubblicarla. Assicurati che tutti gli avvisi siano cancellati prima della pubblicazione."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/>&lt;br/[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con campagne orchestrate](send-messages.md)<br/><br/><b>[Avviare e monitorare la campagna](start-monitor-campaigns.md)</b><br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Dopo aver creato le attività orchestrate e progettate da eseguire nell’area di lavoro, puoi pubblicarle e monitorarne l’esecuzione.

## Pianificare campagne orchestrate {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Modulo di pianificazione"
>abstract="In qualità di manager della campagna, puoi pianificare il lancio automatico delle campagne in momenti specifici, consentendo un calendario preciso e dati di targeting precisi per le comunicazioni di marketing."

In qualità di manager della campagna, puoi pianificare il lancio automatico delle campagne in momenti specifici, consentendo un calendario preciso e dati di targeting precisi per le comunicazioni di marketing.

### Best practice {#scheduler-best-practices}

* Non pianificare l’esecuzione di una campagna orchestrata per più di 15 minuti, in quanto potrebbe impedire le prestazioni complessive del sistema e creare blocchi nel database.
* Se desideri inviare un messaggio unico nella campagna orchestrata, puoi impostarlo per l&#39;esecuzione **Una volta**.
* Se desideri inviare un messaggio ricorrente nella campagna orchestrata, devi utilizzare le opzioni **Pianificazione** e impostare la frequenza di esecuzione. L’attività di consegna ricorrente non ti consente di definire una pianificazione.

### Configurare la pianificazione della campagna {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validità del modulo di pianificazione"
>abstract="È possibile definire un periodo di validità per il modulo di pianificazione. Può essere permanente (impostazione predefinita) o valido fino a una data specifica."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Opzioni del modulo di pianificazione"
>abstract="Definisci la frequenza del modulo di pianificazione. Può essere eseguito in un determinato momento, una o più volte al giorno, alla settimana o al mese."

![Schermata Scheduler con opzioni mensili](assets/scheduler-screen.png)

Segui questi passaggi per configurare la **pianificazione orchestrata della campagna**:

1. Seleziona il pulsante **Appena possibile** nella parte superiore dell&#39;area di lavoro della campagna orchestrata.

1. Configura la **Frequenza di esecuzione**:

   * **Una volta**: la campagna orchestrata viene eseguita una sola volta.

   * **Giornaliero**: la campagna orchestrata viene eseguita a un&#39;ora specifica, una volta al giorno.

   * **Più volte al giorno:** la campagna orchestrata viene eseguita regolarmente più volte al giorno. Puoi impostare esecuzioni in orari specifici o periodicamente.

   * **Settimanale**: la campagna orchestrata viene eseguita in un determinato momento, una o più volte alla settimana.

   * **Mensile**: la campagna orchestrata viene eseguita in un determinato momento, una o più volte al mese. Puoi selezionare i mesi, quando è necessario eseguire la campagna orchestrata. Puoi anche impostare le esecuzioni in un giorno feriale specifico del mese, ad esempio il secondo martedì del mese.

     ![Schermata del modulo di pianificazione con esempio di esecuzione giornaliera](assets/scheduler-daily-sample.png){width="50%" align="left"}

1. Definisci i dettagli di esecuzione in base alla frequenza selezionata. I campi dettagliati variano a seconda della frequenza utilizzata (tempo, frequenza di ripetizione, giorni specificati, ecc.).

1. Fai clic su **Anteprima orari di lancio** per verificare la pianificazione delle prossime dieci esecuzioni della campagna orchestrata.

1. Definisci il periodo di validità del modulo di pianificazione:

   * **Permanente (non scade mai)**: la campagna orchestrata viene eseguita, in base alla frequenza specificata, senza alcun limite all&#39;intervallo di tempo o al numero di iterazioni.

   * **Periodo di validità**: la campagna orchestrata viene eseguita in base alla frequenza specificata, fino a una data specifica. È necessario specificare le date di inizio e di fine.

1. Seleziona **Conferma** per salvare le impostazioni. La frequenza di esecuzione viene visualizzata sopra l’area di lavoro della campagna orchestrata.

>[!TIP]
>
>Se desideri avviare subito la campagna orchestrata, mantieni il valore predefinito **Appena possibile**.

### Esempio {#scheduler-example}

Nell’esempio seguente, l’attività è configurata in modo che la campagna orchestrata venga eseguita due volte al giorno alle 9 e alle 12, ogni giorno della settimana dal 1° ottobre 2025 al 1° gennaio 2026.

![Modulo di pianificazione configurato per eseguire la campagna due volte al giorno alle 9 e alle 12](assets/scheduler-sample.png){width="50%" align="left"}

## Avviare una campagna orchestrata {#start}

Per avviare una campagna orchestrata, passa alla scheda **[!UICONTROL Orchestrazione]** del menu **[!UICONTROL Campagne]** e seleziona la campagna da avviare, quindi fai clic sul pulsante **[!UICONTROL Riproduci]** nell&#39;angolo superiore destro dell&#39;area di lavoro.

Una volta eseguita la campagna orchestrata, ogni attività nell’area di lavoro viene eseguita in ordine sequenziale, fino al raggiungimento della fine della campagna orchestrata.

Puoi monitorare l’avanzamento dei profili target in tempo reale utilizzando un flusso visivo. Questo consente di identificare rapidamente lo stato di ciascuna attività e il numero di profili che passano da un’attività all’altra.

![](assets/workflow-execution.png){zoomable="yes"}

Nelle campagne orchestrate, i dati trasportati da un’attività all’altra tramite transizioni vengono memorizzati in una tabella di lavoro temporanea. Questi dati possono essere visualizzati per ogni transizione. A questo scopo, seleziona una transizione per aprirne le proprietà sul lato destro dello schermo.

* Fai clic su **[!UICONTROL Anteprima schema]** per visualizzare lo schema della tabella di lavoro.
* Fai clic su **[!UICONTROL Anteprima risultati]** per visualizzare i dati trasportati nella transizione selezionata.

![](assets/transition.png){zoomable="yes"}

## Monitorare l’esecuzione della campagna

### Monitorare l’esecuzione dell’attività {#activities}

Gli indicatori visivi nell’angolo superiore a destra di ciascuna casella di attività ti consentono di controllarne l’esecuzione:

| Indicatore visivo | Descrizione |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’attività è attualmente in esecuzione. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’attività richiede la tua attenzione. Ciò potrebbe implicare la conferma dell’invio di una consegna o l’adozione di un’azione necessaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’attività ha rilevato un errore. Per risolvere il problema, apri i registri orchestrati della campagna per ulteriori informazioni. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’attività è stata eseguita correttamente. |

### Monitorare i registri e le attività {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Registri e attività"
>abstract="La schermata **Registri e attività** fornisce una cronologia dell’esecuzione della campagna orchestrata, registrando tutte le azioni dell’utente e gli errori riscontrati."

Monitorare registri e attività è un passaggio chiave per analizzare le campagne orchestrate e assicurarti che vengano eseguite correttamente. Sono accessibili dall’icona **[!UICONTROL Registri]** disponibile nella barra degli strumenti delle azioni e nel riquadro delle proprietà di ogni attività.

Il menu **[!UICONTROL Registri e attività]** fornisce una cronologia dell&#39;esecuzione della campagna orchestrata, registrando tutte le azioni utente e gli errori riscontrati.

![](assets/workflow-logs.png){zoomable="yes"}

Sono disponibili due tipi di informazioni:

* La scheda **[!UICONTROL Registro]** contiene la cronologia di esecuzione di tutte le attività della campagna orchestrate. Questi registri indicizzano in ordine cronologico le operazioni effettuate e gli errori di esecuzione.
* Nella scheda **[!UICONTROL Attività]** viene illustrata la sequenza di esecuzione delle attività.

In entrambe le schede, puoi scegliere le colonne visualizzate e il loro ordine, applicare filtri e utilizzare il campo di ricerca per trovare rapidamente le informazioni desiderate.

## Comandi orchestrati per l’esecuzione della campagna {#execution-commands}

La barra delle azioni nell’angolo in alto a destra fornisce i comandi che consentono di gestire l’esecuzione della campagna orchestrata. Puoi eseguire le seguenti operazioni:

* **[!UICONTROL Avvia]** / **[!UICONTROL Riprendi]** l&#39;esecuzione del   orchestrata, che assume quindi lo stato In corso. Se la campagna orchestrata è stata sospesa, viene ripresa, altrimenti viene avviata e le attività iniziali vengono quindi attivate.

* **[!UICONTROL Sospendi]** l&#39;esecuzione della campagna orchestrata, che assume quindi lo stato In pausa. Non verranno attivate nuove attività finché non viene ripresa, ma le operazioni in corso non vengono sospese.

* **[!UICONTROL Interrompi]** una campagna orchestrata in esecuzione, che assumerà lo stato Finished. Se possibile, le operazioni in corso vengono interrotte. Non è possibile riprendere dalla campagna orchestrata dalla stessa posizione in cui è stata interrotta.
