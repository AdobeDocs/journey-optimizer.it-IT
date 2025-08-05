---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come creare campagne orchestrate con Adobe Journey Optimizer
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 56%

---


# Attività di campagne orchestrate {#orchestrate}

Dopo aver [creato una campagna orchestrata](gs-campaign-creation.md), puoi iniziare a orchestrare le diverse attività che eseguirà. A questo scopo, viene fornita un’area di lavoro visiva che consente di creare un diagramma orchestrato per una campagna. All’interno di questo diagramma, puoi aggiungere varie attività e collegarle in ordine sequenziale.

## Aggiungere attività {#add}

In questa fase della configurazione, il diagramma viene visualizzato con un’icona iniziale che rappresenta l’inizio della campagna orchestrata. Per aggiungere la prima attività, fai clic sul pulsante **+** collegato all’icona di avvio.

Viene visualizzato un elenco di attività che possono essere aggiunte al diagramma. Le attività disponibili dipendono dalla posizione all’interno del diagramma Orchestrated Campaign. Ad esempio, quando aggiungi la prima attività, puoi avviare la campagna orchestrata eseguendo il targeting di un pubblico, suddividendo il percorso della campagna orchestrata o impostando un&#39;attività **Attendi** per ritardare l&#39;esecuzione della campagna orchestrata. Al contrario, dopo un&#39;attività di **Generazione pubblico**, puoi perfezionare il target con le attività di targeting, inviare una consegna al pubblico con le attività del canale o organizzare il processo della campagna orchestrata con le attività di controllo del flusso.

![](assets/orchestrated-start.png){zoomable="yes"}

Una volta aggiunta un’attività al diagramma, viene visualizzato un riquadro a destra che consente di configurarla con impostazioni specifiche. Informazioni dettagliate su come configurare ogni attività sono disponibili in [questa sezione](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Ripeti questo processo per aggiungere tutte le attività desiderate, a seconda delle attività da eseguire per la campagna orchestrata. Puoi anche inserire una nuova attività tra due attività. A questo scopo, fai clic sul pulsante **+** sulla transizione tra le attività, seleziona l’attività desiderata e configurala nel riquadro a destra.

Puoi personalizzare il nome delle transizioni tra ciascuna attività. A questo scopo, seleziona la transizione e modifica la relativa etichetta nel riquadro a destra.

![](assets/canvas-transition.png)

### Barra degli strumenti dell’area di lavoro {#toolbar}

La barra degli strumenti dell’area di lavoro offre opzioni per gestire facilmente le attività e navigare nell’area di lavoro:

![](assets/orchestrated-toolbar.png)

![Icona Modalità di selezione multipla](assets/do-not-localize/canvas-multiple.svg) Seleziona più attività per eliminarle tutte contemporaneamente o copiarle e incollarle. [Scopri come copiare e incollare le attività](#copy)

![Icona Ruota](assets/do-not-localize/canvas-rotate.svg) Passa all’area di lavoro verticalmente.

![Icona Adatta allo schermo](assets/do-not-localize/canvas-fit.svg) Adatta il livello di zoom dell’area di lavoro allo schermo.

![Icona Riduci](assets/do-not-localize/canvas-zoomout.svg) ![Icona Ingrandisci](assets/do-not-localize/canvas-zoomin.svg) Riduce o ingrandisce l’area di lavoro.

![Icona Impostazioni campagna](assets/do-not-localize/canvas-map.svg) Apre un’istantanea dell’area di lavoro che mostra la tua posizione.

### Gestire le attività {#manage}

Quando si aggiungono delle attività, nel riquadro delle proprietà sono disponibili pulsanti di azione che consentono di eseguire più operazioni.

![](assets/activity-action.png)

![Icona Elimina](assets/do-not-localize/activity-delete.svg) Elimina l’attività dall’area di lavoro.

![Icona Disabilita](assets/do-not-localize/activity-disable.svg) ![Icona Abilita](assets/do-not-localize/activity-enable.svg) Disabilita/Abilita l’attività. Quando viene eseguita la campagna orchestrata, le attività disabilitate e le attività seguenti sullo stesso percorso non vengono eseguite e la campagna orchestrata viene interrotta.

![Icona Pausa](assets/do-not-localize/activity-pause.svg) ![Icona Riprendi](assets/do-not-localize/activity-resume.svg) Sospendi/Riprendi l’attività. Quando viene eseguita, la campagna orchestrata si interrompe all’attività in pausa. L’attività corrispondente e tutte quelle che la seguono nello stesso percorso non vengono eseguite.

Puoi utilizzare qualsiasi attività nell’area di lavoro come punto di interruzione per mettere in pausa l’esecuzione della campagna. Ciò significa che la campagna verrà eseguita solo fino a questa attività, quindi sospendi l’esecuzione. Durante la sospensione dell’esecuzione, il motore di segmentazione mantiene disponibili i dati temporanei per l’anteprima. Per visualizzare i dati trasportati, puoi selezionare la transizione in entrata immediatamente prima dell’attività in pausa. Ulteriori informazioni su questa sezione: [Monitoraggio del flusso visivo](../orchestrated/start-monitor-campaigns.md#flow)

![Icona Copia](assets/do-not-localize/activity-copy.svg) Copia l’attività. [Scopri come copiare e incollare le attività](#copy)

![Icona Registri e attività](assets/do-not-localize/activity-logs.svg) Accesso ai registri e alle attività.

Diverse attività di **targeting**, come **Combina** o **Deduplica**, ti consentono di elaborare la popolazione rimanente e includerla in un’ulteriore transizione in uscita. Ad esempio, se utilizzi un’attività **Dividi**, il complemento è costituito dalla popolazione che non corrisponde a nessuno dei sottoinsiemi definiti in precedenza. Per utilizzare questa funzionalità, attiva l’opzione **[!UICONTROL Genera complemento]**.

### Attività di copia e incolla {#copy}

Puoi copiare le attività e incollarle in qualsiasi area di lavoro della campagna orchestrata. La campagna di destinazione può trovarsi in una scheda del browser diversa.

* Per copiare un’attività, fai clic sul pulsante ![icona Copia](assets/do-not-localize/activity-copy.svg) nel riquadro delle proprietà dell’attività.
* Per copiare più attività, fai clic sull’ ![icona Modalità di selezione multipla](assets/do-not-localize/canvas-multiple.svg) nella barra degli strumenti dell’area di lavoro.

| Copiare un’attività | Copiare più attività |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Per incollare le attività, fai clic sul pulsante **+** su una transizione e seleziona “Incolla x attività”.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Esempio di diagramma {#example}

Di seguito è riportato un esempio di campagna orchestrata progettata per inviare un’e-mail a tutti i clienti che hanno effettuato un acquisto di almeno 100$, escludendo al contempo tutti i clienti che hanno meno di 50 punti fedeltà.

![](assets/canvas-example-diagram.png){zoomable="yes"}

A questo scopo, sono state aggiunte le seguenti attività:

* Un&#39;attività **[!UICONTROL Fork]** divide la campagna orchestrata in tre percorsi.
* Le attività **[!UICONTROL Crea pubblico]** eseguono il targeting dei tre set di clientela:

   * Clientela con un’e-mail,
   * Clientela che ha acquistato almeno 100 $,
   * Clientela con meno di 50 punti fedeltà.

* Un’attività **[!UICONTROL Combina]** raggruppa la clientela con un’e-mail e quella che ha effettuato un acquisto di almeno 100 $,
* Un’attività **[!UICONTROL Combina]** esclude la clientela con meno di 50 punti fedeltà,
* Un’attività **[!UICONTROL Consegna e-mail]** invia un’e-mail alla clientela risultante.

## Passaggi successivi {#next}

Dopo aver progettato correttamente il diagramma della campagna orchestrata, puoi eseguire la campagna orchestrata e tenere traccia dell’avanzamento delle sue varie attività. [Scopri come avviare una campagna orchestrata e monitorarne l&#39;esecuzione](start-monitor-campaigns.md)
