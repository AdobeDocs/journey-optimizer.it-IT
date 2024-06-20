---
solution: Journey Optimizer
product: journey optimizer
title: Eseguire il piano di preparazione IP
description: Scopri come eseguire e monitorare un piano di riscaldamento IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, gruppo, sottodomini, recapito messaggi
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: cd95614329e6efdc7ac4b6e0a5c683757a14b379
workflow-type: tm+mt
source-wordcount: '2558'
ht-degree: 11%

---

# Eseguire il piano di preparazione IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Introduzione ai piani di preparazione IP](ip-warmup-gs.md)
* [Creare campagne di preparazione IP](ip-warmup-campaign.md)
* [Creare un piano di preparazione IP](ip-warmup-plan.md)
* **[Eseguire il piano di riscaldamento IP](ip-warmup-execution.md)**

>[!ENDSHADEBOX]

Una volta che [ha creato un piano di riscaldamento IP](ip-warmup-plan.md) e caricato il file preparato con il tuo consulente del team Deliverability, puoi definire le fasi ed eseguire nel piano.

Ogni fase è composta da più esecuzioni, alle quali si assegna una singola campagna.

## Definire le fasi {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Escludere i tipi di pubblico delle campagne"
>abstract="Seleziona le campagne per escludere i relativi tipi di pubblico dalla fase corrente. Questo impedisce ai profili contattati in precedenza di essere nuovamente oggetto di targeting; saranno esclusi solo quelli che hanno ricevuto una comunicazione tramite il percorso."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Escludere gruppi di dominio"
>abstract="Seleziona i domini da escludere dalla fase corrente. L’esclusione del dominio richiede una fase non eseguita, quindi potrebbe essere necessario dividere una fase in esecuzione per aggiungere esclusioni."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html?lang=it#split-phase" text="Suddividere una fase"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="Definire le fasi del piano"
>abstract="Ogni fase è composta da più esecuzioni, alle quali si assegna una singola campagna."

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. Seleziona la campagna da associare alla prima fase del piano di riscaldamento IP.

   >[!NOTE]
   >
   >Non puoi selezionare una campagna già in uso in un altro piano di riscaldamento IP. Tuttavia, la stessa campagna può essere utilizzata in una o più fasi dello stesso piano di riscaldamento IP.

   ![](assets/ip-warmup-plan-select-campaign.png)

   >[!IMPORTANT]
   >
   >* Solo le campagne con **[!UICONTROL Attivazione del piano di riscaldamento IP]** opzione abilitata sono disponibili per la selezione. [Ulteriori informazioni](#create-ip-warmup-campaign)
   >
   >* È possibile selezionare solo le campagne che utilizzano la stessa superficie del piano di riscaldamento IP selezionato.

1. Una volta selezionata una campagna per la fase corrente, vengono visualizzate le sezioni per escludere profili, tipi di pubblico della campagna e gruppi di dominio.

   >[!NOTE]
   >
   >Dopo l’attivazione di un’esecuzione, le esclusioni non possono più essere modificate a meno che non si: [dividere l’esecuzione](#split-phase) in una nuova fase.

   1. Dalla sezione **[!UICONTROL Gruppi di dominio esclusi]** , selezionare i domini che si desidera escludere da tale fase.

      >[!NOTE]
      >
      >L’esclusione del dominio richiede una fase non eseguita, quindi potrebbe essere necessario [dividere una fase in esecuzione](#split-phase) per aggiungere esclusioni.

      ![](assets/ip-warmup-plan-exclude-domains.png)

      Ad esempio, dopo aver eseguito il riscaldamento dell’IP per alcuni giorni, ti rendi conto che la reputazione dell’ISP con un dominio (ad Adobe) non è buona e desideri risolverla senza interrompere il piano di riscaldamento dell’IP. In questo caso, puoi escludere il gruppo di dominio Adobe.

      >[!NOTE]
      >
      >È possibile escludere solo un gruppo di dominio personalizzato aggiunto al [Modello di piano di riscaldamento IP](ip-warmup-plan.md#prepare-file). In caso contrario, aggiorna il modello con il gruppo di dominio personalizzato che desideri escludere e [ricarica il piano](#re-upload-plan).

   1. Dalla sezione **[!UICONTROL Campagna per l’esclusione dei profili]** , seleziona le campagne che i tipi di pubblico desideri escludere dalla fase corrente.

      ![](assets/ip-warmup-plan-exclude-campaigns.png)

      Ad esempio, durante l’esecuzione della fase 1, era necessario [dividilo](#split-phase) per qualsiasi motivo. Pertanto, puoi escludere la campagna utilizzata nella fase 1 in modo che i profili contattati in precedenza dalla fase 1 non siano inclusi nella fase 2. Puoi anche escludere le campagne da altri piani di riscaldamento dell’IP.

   1. Dalla sezione **[!UICONTROL Percorsi per l’esclusione dei profili]** , seleziona i percorsi con i tipi di pubblico che desideri escludere dalla fase corrente.

+++ Per utilizzare l’opzione Percorsi per l’esclusione dei profili, è necessario stabilire una relazione tra gli schemi Evento feedback messaggio AJO e Record entità AJO.

      1. Creare un **Namespace** che fungerà da tipo di identità per i passaggi seguenti.

      1. Accedere a Adobe Experience Platform, dalla **Schemi** , selezionare il **Schema record entità AJO** e imposta **_id** come identità primaria e selezionare lo spazio dei nomi creato in precedenza come **Spazio dei nomi dell’identità**.

      1. Dalla sezione **Schemi** , selezionare il **Schema evento feedback messaggio AJO**, e passare al **_messageID** campo. Seleziona **Aggiungi relazione** e scegli **Schema record entità AJO** come **Schema di riferimento** e lo spazio dei nomi creato in precedenza come **Spazio dei nomi dell’identità di riferimento**.
+++

   1. In **[!UICONTROL Profili di destinazione nelle esecuzioni precedenti]** sezione, puoi notare che i profili delle esecuzioni precedenti di quella fase sono sempre esclusi. Ad esempio, se in #1 di esecuzione un profilo è stato coperto dalle prime 4800 persone target, il sistema si assicurerà automaticamente che lo stesso profilo non riceva l’e-mail in #2. di esecuzione

      >[!NOTE]
      >
      >Questa sezione non è modificabile.

1. Se necessario, puoi sostituire la campagna utilizzando **[!UICONTROL Sostituisci]** pulsante. È inoltre possibile **[!UICONTROL Cancella]** la campagna selezionata utilizzando **[!UICONTROL Cancella]** pulsante. Questa azione cancella non solo la campagna, ma anche altre proprietà a livello di fase come Esclusione di gruppi di dominio, Campagna, Esclusione di Percorsi e altre. Dopo aver cancellato, puoi scegliere una nuova campagna immediatamente o in un secondo momento.

   ![](assets/ip-warmup-plan-replace-campaign.png)

   >[!NOTE]
   >
   >Questa azione è possibile solo prima di attivare la prima esecuzione della fase. Dopo l’attivazione di un’esecuzione, la campagna non può essere sostituita, a meno che tu non [dividere l’esecuzione](#split-phase) in una nuova fase.

1. Se necessario, puoi aggiungere una fase. Verrà aggiunto dopo l’ultima fase.

   ![](assets/ip-warmup-plan-add-phase.png)

1. Utilizza il **[!UICONTROL Elimina fase]** per rimuovere eventuali fasi indesiderate. Questa azione è disponibile solo se non viene eseguita alcuna esecuzione in una fase. <!--Once a run is executed, deletion is not allowed.-->

   >[!CAUTION]
   >
   >Non è possibile annullare **[!UICONTROL Elimina fase]** azione.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!NOTE]
   >
   >Se elimini tutte le fasi dal piano di riscaldamento IP, si consiglia di ricaricare un piano. [Ulteriori informazioni](#re-upload-plan)

## Definire le esecuzioni {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="Definire ogni esecuzione"
>abstract="Definisci e attiva ogni esecuzione per tutte le fasi."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="Filtra in base al coinvolgimento"
>abstract="Questa colonna è un filtro che esegue il targeting solo degli utenti coinvolti con il tuo marchio negli ultimi 20 giorni, ad esempio. È inoltre possibile modificare questa impostazione tramite l’opzione **Modifica esecuzione**."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="Impostare un intervallo di tempo"
>abstract="Puoi definire un intervallo di tempo durante il quale la campagna di preparaizone IP può essere eseguita in caso di ritardi nel processo di segmentazione."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="Annullare esecuzioni con errori del pubblico"
>abstract="Seleziona questa opzione per annullare un’esecuzione se i profili qualificati sono inferiori ai profili di destinazione una volta che il pubblico è stato valutato per tale esecuzione."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="Visualizzazione a 360° dei profili"
>abstract="Questa colonna mostra il numero di profili qualificati. Una volta che il pubblico è stato valutato per un’esecuzione, se sono presenti più profili target rispetto ai profili qualificati, l’esecuzione viene comunque eseguita, a meno che non sia abilitata l’opzione **Annulla esecuzioni attivate in caso di errori**. In questo caso, l’esecuzione viene annullata."

1. Seleziona una pianificazione per ogni esecuzione per assicurarti che venga eseguita all’ora specificata.

   ![](assets/ip-warmup-plan-send-time.png)

1. Facoltativamente, puoi definire un intervallo di tempo durante il quale la campagna di riscaldamento IP può essere eseguita in caso di ritardi nel [valutazione del pubblico](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"}. A tale scopo, fare clic sull&#39;icona Proprietà in alto a sinistra, accanto al nome del piano e utilizzare **[!UICONTROL Ritenta runtime]** per selezionare una durata - fino a 240 minuti (4 ore).

   >[!NOTE]
   >
   >I tentativi si verificano ogni 30 minuti fino alla fine dell’intervallo di tempo definito.

   ![](assets/ip-warmup-plan-retry-run-time.png)

   Ad esempio, se imposti un’ora di invio in un dato giorno alle 9 e selezioni 120 minuti come ora di esecuzione dei nuovi tentativi, ciò consente di eseguire una finestra di opportunità di 2 ore (9:00 - 11:00) per eventuali ritardi imprevisti nella valutazione del pubblico.

   >[!NOTE]
   >
   >Se non viene specificata alcuna finestra temporale, l’esecuzione viene tentata al momento dell’invio e avrà esito negativo se la valutazione del pubblico non viene completata.

1. Se necessario, seleziona **[!UICONTROL Modifica esecuzione]** dall’icona Altre azioni. È possibile aggiornare il numero di indirizzi in ogni colonna. È inoltre possibile aggiornare **[!UICONTROL Ultimo impegno]** campo per eseguire il targeting solo degli utenti che hanno utilizzato il tuo marchio negli ultimi 20 giorni, ad esempio.

   >[!NOTE]
   >
   >Si consiglia di modificare questi numeri consultando il tuo esperto di recapito messaggi.

   ![](assets/ip-warmup-plan-edit-run.png)

   >[!NOTE]
   >
   >Se non si desidera applicare alcun periodo di coinvolgimento a un&#39;esecuzione, immettere 0 nel campo **[!UICONTROL Ultimo impegno]** campo.

1. Seleziona la **[!UICONTROL Annulla esecuzioni attivate in caso di errori]** opzione per annullare un’esecuzione se i profili idonei sono inferiori ai profili target dopo che il pubblico è stato valutato per tale esecuzione. In tal caso, l’esecuzione richiede **[!UICONTROL Non riuscito]** stato.

   ![](assets/ip-warmup-plan-pause.png)

1. **[!UICONTROL Attiva]** la corsa. [Ulteriori informazioni](#activate-run)

1. Lo stato di questa esecuzione cambia in **[!UICONTROL Live]**, il che significa che il sistema ha accettato la richiesta di pianificare l&#39;esecuzione.

   >[!NOTE]
   >
   >I diversi stati di esecuzione sono elencati in [questa sezione](#monitor-plan).

1. Se l’esecuzione della campagna non è stata avviata, puoi annullare un’esecuzione live. Questa azione annulla effettivamente la pianificazione dell’esecuzione e non interrompe l’invio.

   ![](assets/ip-warmup-plan-stop-run.png)

1. Per duplicare una bozza, un’esecuzione live o completata, seleziona **[!UICONTROL Esecuzione duplicata]**. Dopo la duplicazione, viene visualizzato il menu Modifica esecuzione, che consente agli utenti di regolare **[!UICONTROL Profili target totali]** e **[!UICONTROL Ora di invio]** secondo necessità.

   ![](assets/ip-warmup-duplicate.png)

## Attiva esecuzioni {#activate-run}

Per attivare un&#39;esecuzione, selezionare **[!UICONTROL Attiva]** pulsante. Quindi puoi attivare le esecuzioni successive su base giornaliera.

Quando si eseguono più piani di riscaldamento IP simultaneamente, tutti rivolti agli stessi domini e pool IP, è fondamentale prevedere le potenziali conseguenze. Ad esempio, se un ISP applica un limite giornaliero di 100 e-mail, l’esecuzione di diversi piani destinati agli stessi domini potrebbe superare questa soglia.

Assicurati di aver pianificato abbastanza tempo per consentire l’esecuzione di [valutazione del pubblico](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"} da eseguire.

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>Ogni esecuzione deve essere attivata almeno 12 ore prima dell’ora di invio effettiva. In caso contrario, la valutazione del pubblico potrebbe non essere completata.

Quando attivi un’esecuzione, vengono creati automaticamente diversi tipi di pubblico.

* Se si attiva la prima esecuzione di una fase:

   * Un [pubblico](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=it){target="_blank"} viene creato per i tipi di pubblico della campagna esclusi (se presenti), con la seguente convenzione di denominazione: `<warmupName>-Phase<phaseNo>-Audience Exclusion `.

   * Viene creato un pubblico per i gruppi di dominio esclusi (se presenti), con la seguente convenzione di denominazione: `<warmupName>-Phase<phaseNo>-Domain Exclusion`.

   * Viene creato un altro pubblico per i tipi di pubblico di percorso esclusi (se presenti), con la seguente convenzione di denominazione: `<warmupName>-Phase<phaseNo>-Journey Audience Exclusion`.

  >[!NOTE]
  >
  >I tipi di pubblico vengono puliti dopo che il piano di riscaldamento è contrassegnato come completato.
  >
  >Il percorso non crea un nuovo pubblico se non vi è alcuna modifica nei tipi di pubblico della campagna esclusi, nei tipi di pubblico di gruppo esclusi o nei gruppi di dominio per le fasi successive.

* Quando si attiva un’esecuzione:

   * Viene creato un altro pubblico per l’ultimo filtro di coinvolgimento, con la seguente convenzione di denominazione: `<warmupName>-Phase<phaseNo>_Run<runNo>-Engagement Filter`.

     >[!NOTE]
     >
     >Il pubblico viene ripulito dopo che il piano di riscaldamento è contrassegnato come completato.
     >
     >Il sistema non crea un nuovo pubblico se non vi è alcuna modifica nell’ultimo filtro di coinvolgimento per le fasi successive.

   * Un [composizione del pubblico](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=it){target="_blank"} viene creato in base al pubblico a cui verrà inviata la campagna, con la seguente convenzione di denominazione: `<warmupName>-Phase<phaseNo>-Run<runNo>`.

     >[!NOTE]
     >
     >Per ogni esecuzione viene creata una nuova composizione di pubblico. Con un limite di 10, gli utenti che eseguono più campagne, percorsi e piani di riscaldamento IP simultaneamente utilizzando composizioni di pubblico pubblicate devono pianificare in anticipo per rimanere entro questo limite, per operazioni parallele.
     >
     >La composizione del pubblico (e quindi del pubblico di output) viene pulita quando viene attivata l’iterazione successiva.

   * Viene creato un pubblico di output con la seguente convenzione di denominazione: `IP Warmup Audience-<warmupName>-Phase<phaseNo>-Run<runNo>`.

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## Monitorare il piano {#monitor-plan}

Per eseguire correttamente il piano di riscaldamento IP, è necessario monitorare i rapporti, attivare le esecuzioni e verificarne lo stato su base giornaliera.

### Utilizzare la sezione Elementi di rilievo {#highlights}

Una volta attivata la prima esecuzione per una fase, **[!UICONTROL In evidenza]** viene visualizzata la sezione.

Offre una rapida panoramica dell’esecuzione corrente e di quella futura. Da questa sezione puoi anche modificare e attivare l’esecuzione successiva.

![](assets/ip-warmup-plan-highlights.png)

### Controllare gli stati di esecuzione {#run-statuses}

Lo stesso piano di riscaldamento dell’IP funge da rapporto consolidato in un’unica posizione. Puoi controllare elementi come il numero di **[!UICONTROL Live]** o **[!UICONTROL Completato]** viene eseguito per ogni fase e visualizza l’avanzamento del piano di riscaldamento IP.

>[!NOTE]
>
>Come best practice, si consiglia di monitorare il piano di riscaldamento IP su base giornaliera.

Un’esecuzione può avere i seguenti stati:

* **[!UICONTROL Bozza]** : ogni volta che viene creata un’esecuzione, quando [creazione di un nuovo piano](ip-warmup-plan.md) o [aggiunta di un&#39;esecuzione](#define-runs) dall&#39;interfaccia utente, accetta **[!UICONTROL Bozza]** stato.
* **[!UICONTROL Live]**: ogni volta che attivi un’esecuzione, vengono richiesti **[!UICONTROL Live]** stato. Significa che il sistema ha accettato la richiesta di pianificare l’esecuzione, non che l’invio sia iniziato. A questo punto puoi osservare lo stato dell’esecuzione live facendo clic sul pulsante **[!UICONTROL Visualizza stato]** nella tabella. Questo consente di tenere traccia di quanti profili di destinazione sono effettivamente qualificati.
* **[!UICONTROL Completato]**: l’esecuzione della campagna per questa esecuzione è completata. Per accedere a un rapporto di esecuzione dettagliato, fare clic sul pulsante **[!UICONTROL Visualizza rapporto]** nella tabella. Questa opzione consente di tenere traccia dello stato di consegna dell’e-mail, inclusi i raggruppamenti specifici dei gruppi di dominio per un monitoraggio avanzato. La campagna associata verrà impostata come Interrotta.[Ulteriori informazioni](#reports)
* **[!UICONTROL Annullato]**: a **[!UICONTROL Live]** esecuzione annullata utilizzando **[!UICONTROL Annulla]** pulsante.[Ulteriori informazioni](#define-runs)
* **[!UICONTROL Non riuscito]**: il sistema ha rilevato un errore, la campagna utilizzata per la fase corrente è stata interrotta oppure è stato abilitato **[!UICONTROL Annulla esecuzioni attivate in caso di errori]** e si è verificato un errore. Se un’esecuzione non riesce, puoi pianificarne un’altra per il giorno successivo.

### Utilizzare i rapporti {#reports}

Più in generale, per misurare l’impatto del piano, puoi controllare le prestazioni delle campagne di riscaldamento IP utilizzando [!DNL Journey Optimizer] rapporti sulle campagne. A questo scopo, per ogni esecuzione completata, puoi fare clic sul pulsante **[!UICONTROL Visualizzare i rapporti]** pulsante. Ulteriori informazioni sono disponibili nel messaggio e-mail della campagna [rapporto live](../reports/campaign-live-report.md#email-live) e [rapporto globale](../reports/campaign-global-report.md#email-global).

![](assets/ip-warmup-plan-reports.png)

Puoi anche accedere ai rapporti da [Menu Campagne](../campaigns/modify-stop-campaign.md#access) poiché il piano potrebbe utilizzare campagne diverse.


## Gestire il piano {#manage-plan}

In qualsiasi momento, se il piano di riscaldamento dell’IP non funziona come previsto, puoi intraprendere le azioni seguenti.

### Suddividere una fase {#split-phase}

Se desideri aggiungere una nuova fase a partire da un’esecuzione specifica, seleziona la **[!UICONTROL Dividi esegue una nuova fase]** dall&#39;icona Altre azioni.

![](assets/ip-warmup-plan-run-split-run.png)

Viene creata una nuova fase per le restanti esecuzioni della fase corrente.

Ad esempio, se selezioni questa opzione per Esegui #4, le esecuzioni #4 a #8 verranno spostate in una nuova fase subito dopo la fase corrente.

Segui i passaggi [sopra](#define-phases) per definire la nuova fase.

* È possibile utilizzare **[!UICONTROL Sostituisci]** o **[!UICONTROL Cancella]** opzioni per la nuova fase.

* Puoi anche escludere la campagna precedente o un dominio dalle prestazioni insoddisfacenti. Scopri come in [questa sezione](#define-phases).

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### Ricarica un piano di riscaldamento IP {#re-upload-plan}

Se il piano di riscaldamento dell’IP non funziona come previsto (ad esempio, se alcuni ISP contrassegnano i messaggi come spam), puoi chiedere al tuo esperto di recapito messaggi di configurare un altro file di piano di riscaldamento dell’IP e ricaricarlo utilizzando il pulsante corrispondente.

![](assets/ip-warmup-re-upload-plan.png)

Tutte le esecuzioni eseguite in precedenza saranno di sola lettura. Il nuovo piano viene visualizzato sotto il primo piano.

Segui i passaggi [sopra](#define-phases) definire le fasi del nuovo piano.

>[!NOTE]
>
>I dettagli del piano di riscaldamento IP cambiano in base al file appena caricato. Le esecuzioni eseguite in precedenza (indipendentemente dalla [stato](#monitor-plan)) non sono interessati.

Prendiamo un esempio:

* Con il piano di riscaldamento IP iniziale, la fase 2 aveva 9 esecuzioni.

* Sono state eseguite 4 esecuzioni (non importa se non riuscite, completate o annullate)<!--as long as a run has been attempted, it is an executed run-->).

* Se ricarichi un nuovo piano, la fase 2 con le prime 4 esecuzioni passerà in modalità di sola lettura.

* Le restanti 5 esecuzioni (che sono in stato di bozza) vengono spostate in una nuova fase (fase 3) che viene visualizzata come nel piano appena caricato.

### Contrassegna un piano come completato {#mark-as-completed}

Se gli IP sono stati riscaldati con il volume desiderato, o se il piano non funziona abbastanza bene o se desideri rilasciarlo per crearne un altro, puoi contrassegnarlo come completato.

A tale scopo, fare clic sul pulsante **[!UICONTROL Altro]** in alto a destra nel piano di riscaldamento dell&#39;IP e selezionare **[!UICONTROL Contrassegna come completato]**.

![](assets/ip-warmup-plan-mark-completed.png)

Questa opzione è disponibile solo se tutte le esecuzioni del piano sono in **[!UICONTROL Completato]** o **[!UICONTROL Bozza]** stato. Se un’esecuzione è **[!UICONTROL Live]**, l’opzione è disattivata.

I diversi stati di esecuzione sono elencati in [questa sezione](#monitor-plan).

