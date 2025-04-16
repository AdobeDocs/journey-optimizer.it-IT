---
solution: Journey Optimizer
product: journey optimizer
title: Avviare e monitorare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come avviare e monitorare le campagne orchestrate con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 43%

---

# Avviare e monitorare le campagne orchestrate {#start-monitor}

<!--
<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio> -->

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Pubblica campagna orchestrata"
>abstract="Per avviare la campagna, devi pubblicarla. Assicurati che tutti gli avvisi siano cancellati prima della pubblicazione."


Dopo aver creato le attività orchestrate e progettate da eseguire nell’area di lavoro, puoi pubblicarle e monitorarne l’esecuzione.

## Avviare una campagna orchestrata {#start}

Per avviare una campagna orchestrata, passa alla scheda **[!UICONTROL Passaggi multipli]** del menu **[!UICONTROL Campagna]** e seleziona la campagna da avviare, quindi fai clic sul pulsante **[!UICONTROL Inizia]** nell&#39;angolo superiore destro dell&#39;area di lavoro.

Una volta eseguita la campagna orchestrata, ogni attività nell’area di lavoro viene eseguita in ordine sequenziale, fino al raggiungimento della fine della campagna orchestrata.

Puoi monitorare l’avanzamento dei profili target in tempo reale utilizzando un flusso visivo. Questo consente di identificare rapidamente lo stato di ciascuna attività e il numero di profili che passano da un’attività all’altra.

![](assets/workflow-execution.png){zoomable="yes"}

## Transizioni orchestrate per le campagne {#transitions}

Nelle campagne orchestrate, i dati trasportati da un’attività all’altra tramite transizioni vengono memorizzati in una tabella di lavoro temporanea. Questi dati possono essere visualizzati per ogni transizione. A questo scopo, seleziona una transizione per aprirne le proprietà sul lato destro dello schermo.

* Fai clic su **[!UICONTROL Anteprima schema]** per visualizzare lo schema della tabella di lavoro.
* Fai clic su **[!UICONTROL Anteprima risultati]** per visualizzare i dati trasportati nella transizione selezionata.

![](assets/transition.png){zoomable="yes"}

## Monitorare l’esecuzione dell’attività {#activities}

Gli indicatori visivi nell’angolo superiore a destra di ciascuna casella di attività ti consentono di controllarne l’esecuzione:

| Indicatore visivo | Descrizione |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’attività è attualmente in esecuzione. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’attività richiede la tua attenzione. Ciò potrebbe implicare la conferma dell’invio di una consegna o l’adozione di un’azione necessaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’attività ha rilevato un errore. Per risolvere il problema, apri i registri orchestrati della campagna per ulteriori informazioni. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’attività è stata eseguita correttamente. |

## Monitorare i registri e le attività {#logs-tasks}

Il monitoraggio dei registri e delle attività dei flussi di lavoro è un passaggio chiave per analizzare le campagne orchestrate e assicurarti che siano eseguite correttamente. Sono accessibili dall’icona **[!UICONTROL Registri]** disponibile nella barra degli strumenti delle azioni e nel riquadro delle proprietà di ogni attività.

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
