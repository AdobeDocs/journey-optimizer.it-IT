---
solution: Journey Optimizer
product: journey optimizer
title: Avviare e monitorare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come avviare e monitorare le campagne orchestrate con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 02270bddf988e8a722e78d0b63fe157c74b586e4
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 17%

---

# Avviare e monitorare le campagne orchestrate {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Pubblicare una campagna orchestrata"
>abstract="Per avviare la campagna, è necessario pubblicarla. Assicurati che tutti gli avvisi siano cancellati prima della pubblicazione."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accedere e gestire le campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con campagne orchestrate](send-messages.md)<br/><br/><b>[Avviare e monitorare la campagna](start-monitor-campaigns.md)</b><br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Dopo aver creato le attività orchestrate e progettate da eseguire nell’area di lavoro, puoi pubblicarle e monitorarne l’esecuzione.

Puoi anche eseguire la campagna in modalità di test per verificarne l’esecuzione e il risultato delle diverse attività.

## Test della campagna prima della pubblicazione {#test}

Journey Optimizer consente di testare le campagne orchestrate prima di andare &quot;live&quot;. In modalità di test, tutte le attività nell&#39;area di lavoro vengono eseguite ad eccezione delle attività **[!UICONTROL Salva pubblico]** e attività del canale. Non esiste alcun impatto funzionale sui dati o sul pubblico.

Per testare una campagna:

1. Apri la campagna orchestrata.
2. Fare clic su **[!UICONTROL Inizio]**.

![](assets/campaign-start.png){zoomable="yes"}

Ogni attività nella campagna viene eseguita in sequenza fino al raggiungimento della fine del diagramma. Durante l’esecuzione del test, puoi gestire la campagna utilizzando la barra delle azioni nell’area di lavoro. Da qui è possibile:

* **Interrompi** l&#39;esecuzione in qualsiasi momento.
* **Avvia** di nuovo l&#39;esecuzione.
* **Riprendi** l&#39;esecuzione se è stata precedentemente sospesa a causa di un problema.

Se si verifica un errore o un avviso durante l&#39;esecuzione, viene inviata una notifica tramite l&#39;icona **[!UICONTROL Avvisi]** / **[!UICONTROL Avviso]** nella barra degli strumenti dell&#39;area di lavoro.

![](assets/campaign-warning.png){zoomable="yes"}

Puoi anche identificare rapidamente le attività non riuscite utilizzando gli [indicatori di stato visivi](#activities) visualizzati direttamente su ogni attività. Per una risoluzione dettagliata dei problemi, apri i [registri della campagna](#logs-tasks), che forniscono informazioni approfondite sull&#39;errore e sul relativo contesto.

## Pubblica la campagna {#publish}

Una volta testata e pronta la campagna, fai clic su **[!UICONTROL Pubblica]** per renderla disponibile.

![](assets/campaign-publish.png){zoomable="yes"}

Il flusso visivo si riavvia e i profili reali iniziano a scorrere nel percorso in tempo reale.

## Monitorare l’esecuzione della campagna {#monitor}

### Monitoraggio del flusso visivo {#flow}

Durante l’esecuzione (in modalità di test o live), il flusso visivo mostra come i profili si spostano nel percorso in tempo reale. Viene visualizzato il numero di profili che passano da un’attività all’altra.

![](assets/workflow-execution.png){zoomable="yes"}

1. Seleziona una transizione.
1. Nel pannello di destra:
- Fare clic su **[!UICONTROL Anteprima schema]** per visualizzare lo schema della tabella di lavoro.
- Fai clic su **[!UICONTROL Anteprima risultati]** per visualizzare i dati trasportati.

![](assets/transition.png){zoomable="yes"}

I dati trasportati da un’attività all’altra tramite transizioni vengono memorizzati in una tabella di lavoro temporanea. Questi dati possono essere visualizzati per ogni transizione. Per verificare i dati passati tra le attività:

1. Seleziona una transizione.
1. Nel riquadro delle proprietà fare clic su **[!UICONTROL Anteprima schema]** per visualizzare lo schema della tabella di lavoro. Seleziona **[!UICONTROL Anteprima risultati]** per visualizzare i dati trasportati.

![](assets/transition.png){zoomable="yes"}

### Indicatori di esecuzione delle attività {#activities}

Gli indicatori visivi di stato consentono di comprendere le prestazioni di ogni attività:

| Indicatore visivo | Descrizione |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’attività è attualmente in esecuzione. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’attività richiede la tua attenzione. Ciò potrebbe implicare la conferma dell’invio di una consegna o l’adozione di un’azione necessaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’attività ha rilevato un errore. Per risolvere il problema, apri i registri orchestrati della campagna per ulteriori informazioni. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’attività è stata eseguita correttamente. |

### Registri e attività {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Registri e attività"
>abstract="La schermata **Registri e attività** fornisce una cronologia dell&#39;esecuzione della campagna orchestrata, registrando tutte le azioni dell&#39;utente e gli errori riscontrati."

Monitorare registri e attività è un passaggio chiave per analizzare le campagne orchestrate e assicurarti che vengano eseguite correttamente. I registri e le attività sono accessibili dal pulsante **[!UICONTROL Registri]** disponibile sia in modalità di test che in modalità live nella barra degli strumenti dell&#39;area di lavoro o nel riquadro delle proprietà di ogni attività.

La schermata **[!UICONTROL Registri e attività]** fornisce una cronologia completa dell&#39;esecuzione della campagna, registrando tutte le azioni dell&#39;utente e gli errori riscontrati.

![](assets/workflow-logs.png){zoomable="yes"}

Sono disponibili due tipi di informazioni:

* La scheda **[!UICONTROL Registro]** contiene la cronologia di tutte le operazioni e degli errori.
* La scheda **[!UICONTROL Attività]** descrive la sequenza di esecuzione dettagliata delle attività.

In entrambe le schede, puoi scegliere le colonne visualizzate e il loro ordine, applicare filtri e utilizzare il campo di ricerca per trovare rapidamente le informazioni desiderate.
