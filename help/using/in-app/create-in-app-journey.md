---
title: Creazione di una notifica in-app in un Percorso
description: Scopri come aggiungere un messaggio in-app in un percorso
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 4ecaf60923f32e7bc2363981a1d7c0874b3b7e94
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 2%

---


# Creare un messaggio in-app in un Percorso {#create-in-app-journey}

Per aggiungere un messaggio in-app in un percorso, effettua le seguenti operazioni:

1. Apri il percorso, quindi trascina e rilascia una **[!UICONTROL In-app]** attività da **[!UICONTROL Azioni]** nella palette.

   Quando un profilo raggiunge la fine del percorso, tutti i messaggi in-app visualizzati scadranno automaticamente. Per questo motivo, dopo l’attività in-app viene aggiunta automaticamente un’attività Attendi per garantire la tempistica corretta.

   ![](assets/in_app_journey_1.png)

1. Immetti un **[!UICONTROL Etichetta]** e **[!UICONTROL Descrizione]** per il messaggio.

1. Scegli la [Superficie in-app](inapp-configuration.md) da utilizzare.

   ![](assets/in_app_journey_2.png)

1. Ora puoi iniziare a progettare il contenuto con **[!UICONTROL Modifica contenuto]** pulsante. [Ulteriori informazioni](design-in-app.md)

1. Clic **[!UICONTROL Modifica trigger]** per configurare il trigger.

   ![](assets/in_app_journey_4.png)

1. Dalla sezione **[!UICONTROL Attivatore messaggio in-app]** , scegli gli eventi e i criteri che attiveranno il messaggio:

   1. Clic **[!UICONTROL Aggiungi condizione]** se desideri che il trigger consideri più eventi o criteri.
   1. Dalla sezione **[!UICONTROL Seleziona un evento]** , selezionare il tipo di evento per il trigger.
   1. Seleziona la modalità di collegamento degli eventi, ad esempio scegli **[!UICONTROL E]** se vuoi **entrambi** i trigger devono essere true per consentire la visualizzazione di un messaggio o la scelta **[!UICONTROL Oppure]** se desideri che venga visualizzato il messaggio se **o** dei trigger sono true.
   1. Clic **[!UICONTROL Crea gruppo]** per raggruppare i trigger.

   ![](assets/in_app_journey_3.png)

1. Scegli la frequenza di attivazione quando il messaggio in-app è attivo:

   * **[!UICONTROL Ogni volta]**: mostra sempre il messaggio quando gli eventi selezionati nel **[!UICONTROL Attivatore app mobile]** a discesa.
   * **[!UICONTROL Una volta]**: mostra questo messaggio solo la prima volta che gli eventi selezionati nel **[!UICONTROL Attivatore app mobile]** a discesa.
   * **[!UICONTROL Fino al click-through]**: mostra questo messaggio quando gli eventi selezionati nel **[!UICONTROL Attivatore app mobile]** Questo si verifica finché un evento di interazione non viene inviato dall’SDK con l’azione &quot;clicked&quot;.
   * **[!UICONTROL X numero di volte]**: mostra il messaggio solo per un numero specifico di volte, determinato dal valore impostato in **[!UICONTROL Tempi di visualizzazione]** campo.

1. Seleziona il giorno della settimana e l’ora specifica in cui desideri che il messaggio in-app venga attivato, quindi fai clic su **[!UICONTROL Salva]**.

1. Se necessario, completa il flusso di percorso trascinando altre azioni o eventi. [Ulteriori informazioni](../building-journeys/about-journey-activities.md)

1. Una volta che il messaggio in-app è pronto, finalizza la configurazione e pubblica il percorso per attivarlo.

Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md).

## Limitazioni delle attività in-app {#in-app-activity-limitations}

* Questa funzione non è attualmente disponibile per i clienti del settore sanitario.

* La personalizzazione può contenere solo attributi di profilo.

* La visualizzazione in-app è legata alla durata del percorso, il che significa che quando il percorso termina per un profilo, tutti i messaggi in-app all’interno di quel percorso cesseranno di essere visualizzati per quel profilo.  Di conseguenza, non è possibile interrompere un messaggio in-app direttamente da un’attività del percorso. Al contrario, per impedire la visualizzazione dei messaggi in-app nel profilo, devi terminare l’intero percorso.

* In modalità di test, la visualizzazione in-app dipende dalla durata del percorso. Per evitare che il percorso termini troppo presto durante il test, regolare il **[!UICONTROL Tempo di attesa]** valore per il **[!UICONTROL Wait]** attività.

* **[!UICONTROL Reazione]** Le attività non possono essere utilizzate per reagire a un clic o a un’apertura in-app.

* Un ritardo di attivazione può verificarsi tra il momento in cui un profilo utente raggiunge un’attività in-app nell’area di lavoro e il momento in cui inizia a visualizzare tale messaggio in-app.

## Rapporto in-app {#inapp-report}

Dal tuo Percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL In-app]** Questa scheda contiene le informazioni principali relative alle consegne in-app inviate nei tuoi percorsi.

Ulteriori informazioni su [Rapporto globale percorso](../reports/journey-global-report.md).

![](assets/in-app-journey-report.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

Il **[!UICONTROL Prestazioni in-app]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stato recapitato il messaggio in-app.

* **[!UICONTROL Impression]**: numero totale di messaggi in-app consegnati a tutti gli utenti.

* **[!UICONTROL Percentuale di clic]**: percentuale di utenti che hanno interagito con i pulsanti inclusi nel messaggio in-app rispetto agli utenti che hanno visualizzato il messaggio.

* **[!UICONTROL Percentuale ignorati]**: percentuale di messaggi in-app ignorati dai destinatari.

Il **[!UICONTROL Riepilogo in-app]** Il grafico mostra l’evoluzione delle impression in-app per il periodo in questione.

Il **[!UICONTROL Clic per pulsante]** i grafici e le tabelle contengono i dati disponibili per il comportamento dei destinatari per pulsante:

* **[!UICONTROL Clic]**: numero totale di destinatari che hanno interagito con i pulsanti inclusi nel messaggio in-app.

* **[!UICONTROL Percentuale di clic]**: percentuale di utenti che hanno interagito con i pulsanti inclusi nel messaggio in-app rispetto agli utenti che hanno visualizzato il messaggio.
+++

**Argomenti correlati:**

* [Progettare un messaggio in-app](design-in-app.md)
* [Testare e inviare il messaggio in-app](send-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)
* [Configurazione in-app](inapp-configuration.md)
