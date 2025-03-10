---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne con più passaggi con Adobe Journey Optimizer
description: Scopri come creare campagne con più passaggi con Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: f73d847c1d335260a0198e844d237a652e346729
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 20%

---

# Organizzazione di attività di campagna in più fasi {#orchestrate}

Dopo aver [creato una campagna con più passaggi](gs-campaign-creation.md), dal menu della campagna con più passaggi o all&#39;interno di una campagna, puoi iniziare a orchestrare le diverse attività che eseguirà. A questo scopo, viene fornita un’area di lavoro visiva che consente di creare un diagramma di una campagna in più passaggi. All’interno di questo diagramma, puoi aggiungere varie attività e collegarle in ordine sequenziale.

## Aggiungere attività {#add}

In questa fase della configurazione, il diagramma viene visualizzato con un’icona iniziale che rappresenta l’inizio della campagna in più passaggi. Per aggiungere la prima attività, fare clic sul pulsante **+** connesso all&#39;icona Start.

Viene visualizzato un elenco di attività che possono essere aggiunte al diagramma. Le attività disponibili dipendono dalla tua posizione all’interno del diagramma campagne in più passaggi. Ad esempio, quando aggiungi la prima attività, puoi avviare la tua campagna in più passaggi eseguendo il targeting di un pubblico, suddividendo il percorso della campagna in più passaggi o impostando un&#39;attività **Attendi** per ritardare l&#39;esecuzione della campagna in più passaggi. Al contrario, dopo un&#39;attività di **Generazione pubblico**, puoi perfezionare il target con le attività di targeting, inviare una consegna al pubblico con le attività del canale o organizzare il processo della campagna in più passaggi con le attività di controllo del flusso.

![](assets/workflow-start.png){zoomable="yes"}

Una volta aggiunta un’attività al diagramma, viene visualizzato un riquadro a destra che consente di configurare l’attività appena aggiunta con impostazioni specifiche. Informazioni dettagliate su come configurare ogni attività sono disponibili in [questa sezione](activities/about-activities.md).

![](assets/workflow-configure-activities.png){zoomable="yes"}

Ripeti questo processo per aggiungere tutte le attività desiderate, a seconda delle attività da eseguire per la campagna in più passaggi. Puoi anche inserire una nuova attività tra due attività. A tale scopo, fare clic sul pulsante **+** sulla transizione tra le attività, selezionare l&#39;attività desiderata e configurarla nel riquadro di destra.

Per rimuovere un&#39;attività, selezionarla nell&#39;area di lavoro e fare clic sull&#39;icona **Elimina** nelle proprietà dell&#39;attività.

>[!TIP]
>
>Hai la possibilità di personalizzare il nome delle transizioni tra ciascuna attività. A questo scopo, seleziona la transizione e modifica la relativa etichetta nel riquadro a destra.

## Barra degli strumenti {#toolbar}

La barra degli strumenti situata nell’angolo superiore destro dell’area di lavoro offre opzioni per manipolare facilmente le attività e navigare nell’area di lavoro:

* **Modalità di selezione multipla**: selezionare più attività per eliminarle tutte contemporaneamente oppure copiarle e incollarle. Consulta [questa sezione](#copy).
* **Ruota**: cambia l&#39;area di lavoro verticalmente.
* **Adatta allo schermo**: adatta il livello di zoom dell&#39;area di lavoro allo schermo.
* **Zoom indietro** / **Zoom avanti**: Zoom indietro o nell&#39;area di lavoro.
* **Mappa di visualizzazione**: apre uno snapshot dell&#39;area di lavoro che mostra che ci si trova.

![](assets/workflow-toolbar.png){zoomable="yes"}{width="50%"}

## Gestire le attività {#manage}

Quando si aggiungono attività, nel riquadro delle proprietà sono disponibili pulsanti di azione che consentono di eseguire più operazioni.

![](assets/activity-action.png){zoomable="yes"}

Puoi eseguire le seguenti operazioni:

* **Elimina** l’attività dall’area di lavoro.
* **Disattiva/Attiva** l’attività. Quando si esegue la campagna in più passaggi, le attività disabilitate e le attività seguenti sullo stesso percorso non vengono eseguite e la campagna in più passaggi viene interrotta.
* **Pausa/Riprendi** l’attività. Quando viene eseguita, la campagna con più passaggi viene sospesa in corrispondenza dell’attività in pausa. L’attività corrispondente e tutte quelle che la seguono nello stesso percorso non vengono eseguite.
* **Copia** l’attività. Consulta [questa sezione](#copy).
* **Sposta** un&#39;attività e tutti i relativi nodi figlio in un&#39;altra transizione. Vedi [questa sezione](#move)
* Accedi alle **opzioni di esecuzione** dell&#39;attività.
* Accedi a **Registri e attività**.

Diverse attività di **targeting**, come **Combina** o **Deduplicazione**, ti consentono di elaborare il gruppo rimanente e includerlo in un&#39;ulteriore transizione in uscita. Ad esempio, se utilizzi un&#39;attività **Split**, il complemento è costituito dal gruppo che non corrisponde a nessuno dei sottoinsiemi definiti in precedenza. Per utilizzare questa funzionalità, attivare l&#39;opzione **Genera complemento**.

![](assets/workflow-split-complement.png)

## Spostare o copiare attività {#move-copy}

### Attività di copia e incolla {#copy}

Puoi copiare le attività campagna in più passaggi e incollarle in qualsiasi flusso di lavoro. La campagna in più passaggi di destinazione può trovarsi in una scheda del browser diversa.

Per copiare le attività, puoi scegliere tra due opzioni:

* copia un’attività utilizzando il pulsante azione.

  ![](assets/workflow-copy.png){zoomable="yes"}{width="70%"}

* copia più attività utilizzando il pulsante della barra degli strumenti.

  ![](assets/workflow-copy-2.png){zoomable="yes"}{width="70%"}

Per incollare le attività copiate, fare clic sul pulsante **+** su una transizione e selezionare &quot;Incolla attività X&quot;.

![](assets/workflow-copy-3.png){zoomable="yes"}{width="50%"}

### Spostare le attività e i relativi nodi figlio {#move}

Journey Optimizer consente di spostare un’attività, insieme all’intero contenuto dei relativi nodi secondari (incluse tutte le transizioni e le attività al suo interno), alla fine di un’altra transizione all’interno della stessa campagna in più passaggi.

Questo processo disconnette l’attività e tutto ciò che si trova nella sua transizione in uscita dalla posizione iniziale, spostandola nella nuova transizione di destinazione.

Per spostare un’attività:

1. Seleziona l’attività da spostare.
1. Nel riquadro delle proprietà dell&#39;attività fare clic sul pulsante **Sposta**.
1. Seleziona la transizione in cui desideri inserire l’attività e la relativa transizione in uscita, quindi conferma.

![](assets/activity-move.png)

## Execution options {#execution}

Tutte le attività ti consentono di gestire le relative opzioni di esecuzione. Seleziona un&#39;attività e fai clic sul pulsante **Opzioni di esecuzione**. Questo ti consente di definire la modalità di esecuzione dell’attività e il comportamento in caso di errori.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}

### Proprietà

Il campo **Esecuzione** consente di definire l&#39;azione da eseguire all&#39;avvio dell&#39;attività.

Il campo **Durata massima esecuzione** consente di specificare una durata, ad esempio &quot;30s&quot; o &quot;1h&quot;. Se l’attività non viene completata dopo la scadenza della durata specificata, viene attivato un avviso. Questo non ha alcun impatto sul funzionamento della campagna in più passaggi.

Il campo **Fuso orario** consente di selezionare il fuso orario dell&#39;attività. Adobe Journey Optimizer consente di gestire le differenze di tempo tra più paesi nella stessa istanza. L’impostazione applicata viene configurata al momento della creazione dell’istanza.

**Il campo Affinità** consente di forzare l&#39;esecuzione di una campagna in più passaggi o di un&#39;attività campagna in più passaggi su un computer specifico. A questo scopo, devi specificare una o più affinità per la campagna o l’attività in più passaggi in questione.

Il campo **Comportamento** consente di definire la procedura da seguire se vengono utilizzate attività asincrone.

### Gestione degli errori

Il campo **In caso di errore** consente di specificare l&#39;azione da eseguire in caso di errore dell&#39;attività.

### Script di inizializzazione

Lo script di inizializzazione **** consente di inizializzare le variabili o modificare le proprietà dell&#39;attività. Fare clic sul pulsante **Modifica codice** e digitare il frammento di codice da eseguire. Lo script viene chiamato durante l’esecuzione dell’attività.

## Esempio {#example}

Di seguito è riportato un esempio di campagna in più passaggi progettata per inviare un’e-mail a tutti i clienti (diversi dai clienti VIP) con un’e-mail che sono interessati alle macchine da caffè.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

A questo scopo, sono state aggiunte le seguenti attività:

* Un&#39;attività **[!UICONTROL Fork]** che divide la campagna in più passaggi in tre percorsi (uno per ogni set di clienti),
* Attività **[!UICONTROL Creazione del pubblico]** per eseguire il targeting dei tre set clienti:

   * Clienti con un’e-mail,
   * Clienti appartenenti al pubblico “Interessati alle macchine da caffè” preesistente,
   * Clienti appartenenti al pubblico “VIP o premio” preesistente.

* Un’attività **[!UICONTROL Combina]** che raggruppa i clienti con un’e-mail e quelli interessati alle macchine da caffè,
* Un’attività **[!UICONTROL Combina]** che esclude clienti VIP,
* Un’attività **[!UICONTROL Consegna e-mail]** che invia un’e-mail ai clienti risultanti.

Dopo aver completato la campagna in più passaggi, aggiungi l&#39;attività en **[!UICONTROL End]** alla fine del diagramma. Questa attività ti consente di contrassegnare visivamente la fine di un flusso di lavoro e non ha alcun impatto funzionale.

Dopo aver progettato correttamente il diagramma campagne con più passaggi, puoi eseguire la campagna con più passaggi e tenere traccia dell’avanzamento delle relative varie attività. [Scopri come avviare una campagna con più passaggi e monitorarne l&#39;esecuzione](start-monitor-campaigns.md)
