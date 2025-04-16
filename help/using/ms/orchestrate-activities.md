---
solution: Journey Optimizer
product: journey optimizer
title: Crea campagne orchestrate con Adobe Systems Journey Optimizer
description: Scopri come versione campagne orchestrate con Adobe Systems Journey Optimizer
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 20%

---

# Orchestrare le attività delle campagne orchestrate {#orchestrate}

Dopo aver [creato una campagna orchestrata](gs-campaign-creation.md), dal menu della campagna orchestrata o all&#39;interno di una campagna, puoi iniziare a orchestrare le diverse attività che eseguirà. A questo scopo, viene fornita un’area di lavoro visiva che consente di creare un diagramma orchestrato per una campagna. All’interno di questo diagramma, puoi aggiungere varie attività e collegarle in ordine sequenziale.

## Aggiungere attività {#add}

In questa fase della configurazione, il diagramma viene visualizzato con un&#39;icona iniziale che rappresenta l&#39;inizio della campagna orchestrata. Per aggiungere la **prima attività, fai clic sul segno +** pulsante collegato all&#39;icona iniziale.

Viene visualizzato un elenco di attività che possono essere aggiunte al diagramma. Le attività disponibili dipendono dalla posizione all&#39;interno del diagramma della campagna orchestrato. Ad esempio, quando aggiungi la tua prima attività, puoi avviare la campagna orchestrata targeting un pubblico, dividendo il percorso della campagna orchestrata o impostando un&#39;attività **di attesa** per ritardare l&#39;esecuzione della campagna orchestrata. D&#39;altra parte, dopo un&#39;attività **di creazione del pubblico** , puoi perfezionare il tuo destinazione con le attività targeting, inviare una consegna al tuo pubblico con le attività del canale o organizzare il processo della campagna orchestrato con le attività di controllo del flusso.

![](assets/workflow-start.png){zoomable="yes"}

Una volta aggiunta un’attività al diagramma, viene visualizzato un riquadro a destra che consente di configurare l’attività appena aggiunta con impostazioni specifiche. Informazioni dettagliate su come configurare ogni attività sono disponibili in [questa sezione](activities/about-activities.md).

![](assets/workflow-configure-activities.png){zoomable="yes"}

Ripeti questo processo per aggiungere tutte le attività desiderate, a seconda delle attività da eseguire per la campagna orchestrata. Puoi anche inserire una nuova attività tra due attività. A tale scopo, fare clic sul pulsante **+** sulla transizione tra le attività, selezionare l&#39;attività desiderata e configurarla nel riquadro di destra.

Per rimuovere un&#39;attività, selezionarla nell&#39;area di lavoro e fare clic sull&#39;icona **Elimina** nelle proprietà dell&#39;attività.

>[!TIP]
>
>Hai la possibilità di personalizzare il nome delle transizioni tra ciascuna attività. A questo scopo, seleziona la transizione e modifica la relativa etichetta nel riquadro a destra.

## Barra degli strumenti {#toolbar}

La barra degli strumenti situata nell’angolo superiore destro dell’area di lavoro offre opzioni per manipolare facilmente le attività e navigare nell’area di lavoro:

* **Modalità di selezione multipla**: selezionare più attività per eliminarle tutte contemporaneamente oppure copiarle e incollarle. Consulta [questa sezione](#copy).
* **Ruota**: cambia l&#39;area di lavoro verticalmente.
* **Adatta allo schermo**: adatta il livello di zoom dell&#39;area di lavoro allo schermo.
* **Zoom out** / **Zoom in**: Zoom out o nella tela.
* **Visualizza mappa**: apre un&#39;istantanea dell&#39;area di lavoro che mostra la tua posizione.

![](assets/workflow-toolbar.png){zoomable="yes"}{width="50%"}

## Gestire le attività {#manage}

Quando si aggiungono attività, nel riquadro delle proprietà sono disponibili pulsanti di azione che consentono di eseguire più operazioni.

![](assets/activity-action.png){zoomable="yes"}

Puoi eseguire le seguenti operazioni:

* **Elimina** l’attività dall’area di lavoro.
* **Disattiva/Attiva** l’attività. Quando viene eseguita la campagna orchestrata, le attività disabilitate e le attività seguenti sullo stesso percorso non vengono eseguite e la campagna orchestrata viene interrotta.
* **Pausa/Riprendi** l’attività. Quando la campagna orchestrata viene eseguita, viene messa in pausa in corrispondenza dell&#39;attività messa in pausa. L’attività corrispondente e tutte quelle che la seguono nello stesso percorso non vengono eseguite.
* **Copia** l’attività. Consulta [questa sezione](#copy).
* **Sposta** un&#39;attività e tutti i relativi nodi figlio in un&#39;altra transizione. Vedi [questa sezione](#move)
* Accedi alle **opzioni di esecuzione** dell&#39;attività.
* Accedi a **Registri e attività**.

Diverse attività di **targeting**, come **Combina** o **Deduplicazione**, ti consentono di elaborare il gruppo rimanente e includerlo in un&#39;ulteriore transizione in uscita. Ad esempio, se utilizzi un&#39;attività **Split**, il complemento è costituito dal gruppo che non corrisponde a nessuno dei sottoinsiemi definiti in precedenza. Per utilizzare questa funzionalità, attivare l&#39;opzione **Genera complemento**.

![](assets/workflow-split-complement.png)

## Spostare o copiare attività {#move-copy}

### Attività di copia e incolla {#copy}

Puoi copiare le attività della campagna orchestrate e incollarle in qualsiasi flusso di lavoro. La campagna orchestrata di destinazione può trovarsi in una scheda del browser diversa.

Per copiare le attività, puoi scegliere tra due opzioni:

* copia un’attività utilizzando il pulsante azione.

  ![](assets/workflow-copy.png){zoomable="yes"}{width="70%"}

* Copia più attività utilizzando la barra degli strumenti pulsante.

  ![](assets/workflow-copy-2.png){zoomable="yes"}{width="70%"}

Per incollare le attività copiate, fare clic sul pulsante **+** su una transizione e selezionare &quot;Incolla attività X&quot;.

![](assets/workflow-copy-3.png){zoomable="yes"}{width="50%"}

### Spostare le attività e i relativi nodi figlio {#move}

Journey Optimizer consente di spostare un’attività, insieme all’intero contenuto dei relativi nodi secondari (incluse tutte le transizioni e le attività al suo interno), alla fine di un’altra transizione all’interno della stessa campagna orchestrata.

Questo processo disconnette l’attività e tutto ciò che si trova nella sua transizione in uscita dalla posizione iniziale, spostandola nella nuova transizione di destinazione.

Per spostare un&#39;attività:

1. Seleziona l’attività da spostare.
1. Nel riquadro delle proprietà dell&#39;attività fare clic sul pulsante **Sposta**.
1. Seleziona la transizione in cui desideri inserire l’attività e la relativa transizione in uscita, quindi conferma.

![](assets/activity-move.png)

## Execution options {#execution}

Tutte le attività ti consentono di gestire le relative opzioni di esecuzione. Seleziona un&#39;attività e fai clic sul pulsante **Opzioni di esecuzione**. Questo ti consente di definire la modalità di esecuzione dell’attività e il comportamento in caso di errori.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}

### Proprietà

Il campo **Esecuzione** consente di definire l&#39;azione da eseguire all&#39;avvio dell&#39;attività.

Il campo **Durata massima esecuzione** consente di specificare una durata, ad esempio &quot;30s&quot; o &quot;1h&quot;. Se l’attività non viene completata dopo la scadenza della durata specificata, viene attivato un avviso. Questo non ha alcun impatto sul funzionamento della campagna orchestrata.

Il **campo Fuso** orario consente di selezionare il fuso orario dell&#39;attività. Adobe Systems Journey Optimizer consente di gestire le differenze di fuso orario tra più paesi sullo stesso istanza. L&#39;impostazione applicata viene configurata al momento della creazione del istanza.

**Il campo Affinità** consente di forzare l&#39;esecuzione di una campagna orchestrata o di un&#39;attività di campagna orchestrata su un determinato computer. A tale scopo, è necessario specificare una o più affinità per la campagna o l&#39;attività orchestrata in questione.

Il campo **Comportamento** consente di definire la procedura da seguire se vengono utilizzate attività asincrone.

### Gestione degli errori

Il **campo In caso di errore** consente di specificare l&#39;azione da eseguire nel caso in cui l&#39;attività subisca un errore.

### Script di inizializzazione

Lo **script** Initialization consente di inizializzare variabili o modificare le proprietà dell&#39;attività. Fare clic sull&#39;pulsante **del codice** Modifica e digitare lo snippet di codice da eseguire. Lo script viene chiamato quando l&#39;attività viene eseguita.

## Esempio {#example}

Ecco un esempio di campagna orchestrata progettata per inviare un&#39;e-mail a tutti i clienti (diversi dai clienti VIP) con un&#39;e-mail interessata alle macchine da caffè.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

A questo scopo, sono state aggiunte le seguenti attività:

* Un&#39;attività **[!UICONTROL Fork]** che divide la campagna orchestrata in tre percorsi (uno per ogni set di clienti),
* Attività **[!UICONTROL Creazione del pubblico]** per eseguire il targeting dei tre set clienti:

   * Clienti con un’e-mail,
   * Clienti appartenenti al pubblico “Interessati alle macchine da caffè” preesistente,
   * Clienti appartenenti al pubblico “VIP o premio” preesistente.

* Un’attività **[!UICONTROL Combina]** che raggruppa i clienti con un’e-mail e quelli interessati alle macchine da caffè,
* Un’attività **[!UICONTROL Combina]** che esclude clienti VIP,
* Un’attività **[!UICONTROL Consegna e-mail]** che invia un’e-mail ai clienti risultanti.

Dopo aver completato la campagna orchestrata, aggiungi l&#39;attività en **[!UICONTROL End]** alla fine del diagramma. Questa attività ti consente di contrassegnare visivamente la fine di un flusso di lavoro e non ha alcun impatto funzionale.

Dopo aver progettato correttamente il diagramma della campagna orchestrata, è possibile eseguire la campagna orchestrata e tenere traccia dello stato di avanzamento delle varie attività. [Scopri come avviare una campagna orchestrata e monitorarne l&#39;esecuzione](start-monitor-campaigns.md)
