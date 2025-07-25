---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come creare campagne orchestrate con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 87%

---

# Attività di campagne orchestrate {#orchestrate}

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/><b>[Orchestrare le attività](orchestrate-activities.md)</b><br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Dopo aver [creato una campagna orchestrata](gs-campaign-creation.md), puoi iniziare a orchestrare le diverse attività da eseguire. A questo scopo, viene fornita un’area di lavoro visiva che consente di creare un diagramma della campagna orchestrata. All’interno di questo diagramma, puoi aggiungere varie attività e collegarle in ordine sequenziale.

## Aggiungere attività {#add}

In questa fase della configurazione, il diagramma viene visualizzato con un’icona di avvio che rappresenta l’inizio della campagna orchestrata. Per aggiungere la prima attività, fai clic sul pulsante **+** collegato all’icona di avvio.

Viene visualizzato un elenco di attività che possono essere aggiunte al diagramma. Le attività disponibili dipendono dalla posizione all’interno del diagramma della campagna orchestrata. Ad esempio, quando aggiungi la prima attività, puoi avviare la campagna orchestrata eseguendo il targeting di un pubblico, dividendo il percorso della campagna orchestrata o impostando un’attività **Attendi** per ritardare l’esecuzione della campagna orchestrata. D’altra parte, dopo un’attività **Crea pubblico**, puoi perfezionare il target con le attività di targeting, inviare una consegna al pubblico con le attività del canale o organizzare il processo della campagna orchestrata con le attività di controllo del flusso.

![](assets/orchestrated-start.png){zoomable="yes"}

Una volta aggiunta un’attività al diagramma, viene visualizzato un riquadro a destra che consente di configurarla con impostazioni specifiche. Informazioni dettagliate su come configurare ogni attività sono disponibili in [questa sezione](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Ripeti questa procedura aggiungendo tutte le attività desiderate in base alle attività che desideri siano eseguite dalla campagna orchestrata. Puoi anche inserire una nuova attività tra due attività. A questo scopo, fai clic sul pulsante **+** sulla transizione tra le attività, seleziona l’attività desiderata e configurala nel riquadro a destra.

Hai la possibilità di personalizzare il nome delle transizioni tra ciascuna attività. A questo scopo, seleziona la transizione e modifica la relativa etichetta nel riquadro a destra.

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

![Icona Disabilita](assets/do-not-localize/activity-disable.svg) ![Icona Abilita](assets/do-not-localize/activity-enable.svg) Disabilita/Abilita l’attività. Quando la campagna orchestrata viene eseguita, le attività disabilitate e le attività successive sullo stesso percorso non vengono eseguite e la campagna orchestrata viene interrotta.

![Icona Pausa](assets/do-not-localize/activity-pause.svg) ![Icona Riprendi](assets/do-not-localize/activity-resume.svg) Sospendi/Riprendi l’attività. Quando la campagna orchestrata viene eseguita, viene messa in pausa in corrispondenza dell’attività in pausa. L’attività corrispondente e tutte quelle che la seguono nello stesso percorso non vengono eseguite.

    È possibile utilizzare qualsiasi attività nell&#39;area di lavoro come punto di interruzione per sospendere l&#39;esecuzione della campagna. Ciò significa che la campagna verrà eseguita solo fino a questa attività, quindi sospendi l’esecuzione. Durante la sospensione dell’esecuzione, il motore di segmentazione mantiene disponibili i dati temporanei per l’anteprima. Per visualizzare i dati trasportati, puoi selezionare la transizione in entrata immediatamente prima dell’attività in pausa. Ulteriori informazioni su questa sezione: [Monitoraggio del flusso visivo](../orchestrated/start-monitor-campaigns.md#flow).

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

Di seguito è riportato un esempio di campagna orchestrata progettata per inviare un messaggio e-mail a tutta la clientela che ha effettuato un acquisto di almeno 100 $, escludendo al contempo tutta quella che ha meno di 50 punti fedeltà.

![](assets/canvas-example-diagram.png){zoomable="yes"}

A questo scopo, sono state aggiunte le seguenti attività:

* Un’attività **[!UICONTROL Fork]** divide la campagna orchestrata in tre percorsi.
* Le attività **[!UICONTROL Crea pubblico]** eseguono il targeting dei tre set di clientela:

   * Clientela con un’e-mail,
   * Clientela che ha acquistato almeno 100 $,
   * Clientela con meno di 50 punti fedeltà.

* Un’attività **[!UICONTROL Combina]** raggruppa la clientela con un’e-mail e quella che ha effettuato un acquisto di almeno 100 $,
* Un’attività **[!UICONTROL Combina]** esclude la clientela con meno di 50 punti fedeltà,
* Un’attività **[!UICONTROL Consegna e-mail]** invia un’e-mail alla clientela risultante.

## Passaggi successivi {#next}

Dopo aver progettato correttamente il diagramma della campagna orchestrata, puoi eseguirla e tenere traccia dell’avanzamento delle varie attività. [Scopri come avviare una campagna orchestrata e monitorarne l’esecuzione](start-monitor-campaigns.md)
