---
solution: Journey Optimizer
product: journey optimizer
title: Avviare e monitorare le campagne orchestrate con Adobe Journey Optimizer
description: Scopri come avviare e monitorare le campagne orchestrate con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 11%

---

# Creazione di query di retargeting {#retarget}

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/><b>[Retargeting](retarget.md)</b> | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Il retargeting ti consente di monitorare i destinatari in base al modo in cui hanno risposto a una campagna orchestrata precedente. Ad esempio, puoi inviare una seconda e-mail ai destinatari che hanno ricevuto ma non hanno fatto clic sul primo.

**[!UICONTROL La campagna orchestrata]** fornisce due attributi principali:

* **[!UICONTROL Feedback messaggio]**: acquisisce eventi relativi alla consegna, ad esempio messaggi inviati, aperti, non recapitati e così via.
* **[!UICONTROL Tracciamento e-mail]**: acquisisce le azioni dell&#39;utente, ad esempio clic e aperture.

![](assets/do-not-localize/retarget-schema.png){zoomable="yes"}


## Creare una regola di retargeting basata sul feedback {#feedback-retarget}

La regola di retargeting basata sul feedback consente di eseguire il retargeting dei destinatari in base agli eventi di consegna dei messaggi acquisiti nell&#39;attributo **[!UICONTROL Feedback messaggio]**. Questi eventi includono risultati quali messaggi inviati, aperti, non recapitati o contrassegnati come spam.

Utilizzando questi dati, puoi definire regole per identificare i destinatari che hanno ricevuto un messaggio precedente, abilitando la comunicazione di follow-up in base a stati di consegna specifici.

1. Crea una nuova **[!UICONTROL campagna orchestrata]**.

1. Aggiungi un&#39;attività **[!UICONTROL Genera pubblico]** e imposta la dimensione di targeting su **[!UICONTROL Destinatario (caas)]**.

1. Nel **[!UICONTROL Generatore regole]**, fai clic su **[!UICONTROL Aggiungi condizione]** e seleziona **[!UICONTROL Feedback messaggio]** dal **[!UICONTROL Selettore attributi]**. Fai clic su **[!UICONTROL Conferma]** per creare **Il feedback del messaggio esiste, ad esempio** condizione.

   ![](assets/retarget_1.png){zoomable="yes"}

1. Scegli l&#39;attributo **[!UICONTROL Stato feedback]** per eseguire il targeting degli eventi di consegna dei messaggi.

+++ Dettagliato passo dopo passo

   1. Aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Feedback messaggio]**.

   1. Cerca l&#39;attributo **[!UICONTROL Stato feedback]** e fai clic su **[!UICONTROL Conferma]**.

      ![](assets/retarget_3.png){zoomable="yes"}

   1. Nel menu **[!UICONTROL Condizione personalizzata]**, scegli lo stato di consegna da tracciare nel menu a discesa **[!UICONTROL Valore]**.

      ![](assets/retarget_4.png){zoomable="yes"}

+++

1. Scegli l&#39;attributo **[!UICONTROL Nome campagna orchestrata]** per eseguire il targeting di una campagna orchestrata specifica.

+++ Dettagliato passo dopo passo

   1. Aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Feedback messaggio]**, cerca **[!UICONTROL entità]** e passa a:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Seleziona **[!UICONTROL Nome campagna orchestrata]**.

      ![](assets/retarget_5.png){zoomable="yes"}

   1. Nel menu **[!UICONTROL Condizione personalizzata]**, specifica il nome della campagna nel campo **[!UICONTROL Valore]**.

+++

1. Scegli l&#39;attributo **[!UICONTROL Nome azione campagna orchestrata]** per eseguire il targeting di un messaggio o un&#39;attività specifica all&#39;interno di una campagna orchestrata.

+++ Dettagliato passo dopo passo

   1. Aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Feedback messaggio]**, cerca **[!UICONTROL entità]** e passa a:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Selezionare **[!UICONTROL Nome azione campagna orchestrata]**.

      ![](assets/retarget_6.png){zoomable="yes"}

   1. Nel menu **[!UICONTROL Condizione personalizzata]**, specifica il nome dell&#39;azione della campagna nel campo **[!UICONTROL Valore]**.

      Per trovare i nomi delle azioni, fai clic sull&#39;![icona Informazioni](assets/do-not-localize/info-icon.svg) accanto al campo Etichetta dell&#39;attività.

+++

1. In alternativa, puoi anche filtrare in base al **[!UICONTROL ID campagna]** (UUID), che si trova nelle proprietà della campagna.

Ora hai configurato una regola di retargeting basata sul feedback per identificare i destinatari in base allo stato di consegna di un messaggio precedente, ad esempio inviato, aperto, non recapitato o contrassegnato come spam. Una volta definito questo pubblico, puoi aggiungere un&#39;e-mail di follow-up o perfezionare ulteriormente il targeting [configurando una regola di retargeting basata sul tracciamento](#tracking-based), che utilizza i dati di interazione dell&#39;utente.

![](assets/retarget_9.png){zoomable="yes"}


## Creare una regola di retargeting basata sul tracciamento {#tracking-based}

La regola di retargeting basata sul tracciamento è destinata ai destinatari in base alle loro interazioni con un messaggio, utilizzando i dati dell&#39;attributo **[!UICONTROL Tracciamento e-mail]**. Acquisisce le azioni dell’utente, ad esempio le aperture delle e-mail e i clic sui collegamenti.

Per eseguire il retargeting dei destinatari in base alle interazioni con i messaggi (ad esempio, apri o fai clic su di essi), utilizza l&#39;entità **[!UICONTROL Tracciamento e-mail]** come segue:

1. Crea una nuova **[!UICONTROL campagna orchestrata]**.

1. Aggiungi un&#39;attività **[!UICONTROL Genera pubblico]** e imposta la dimensione di targeting su **[!UICONTROL Destinatario (caas)]** per concentrarsi sui destinatari della campagna orchestrata precedente.

1. Nel **[!UICONTROL Generatore regole]**, fai clic su **[!UICONTROL Aggiungi condizione]** e seleziona **[!UICONTROL Verifica e-mail]** dal **[!UICONTROL Selettore attributi]**.

   Fai clic su **[!UICONTROL Conferma]** per creare **Verifica e-mail esistente come** condizione.

   ![](assets/retarget_2.png){zoomable="yes"}

1. Per eseguire il targeting delle interazioni dei destinatari con un messaggio, aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Tracciamento e-mail]** e cerca l&#39;attributo **[!UICONTROL Tipo di interazione]**.

   ![](assets/retarget_7.png){zoomable="yes"}

1. Dalle opzioni di condizione personalizzate, utilizza **[!UICONTROL Incluso in]** come operatore e seleziona uno o più valori a seconda del caso d&#39;uso, ad esempio **[!UICONTROL Messaggio aperto]** o **[!UICONTROL Messaggio link fatto clic]**.

   ![](assets/retarget_8.png){zoomable="yes"}

Hai configurato una regola di retargeting basata sul tracciamento per eseguire il targeting dei destinatari in base alle loro interazioni con un messaggio precedente, ad esempio aperture di e-mail o clic sui collegamenti, utilizzando i dati dell&#39;attributo **[!UICONTROL Tracciamento e-mail]**. Una volta definito questo pubblico, puoi aggiungere un&#39;azione di follow-up o perfezionare ulteriormente il targeting combinandolo con una [regola di retargeting basata sul feedback](#feedback-retarget) per includere i risultati dei messaggi, ad esempio inviati, non recapitati o contrassegnati come spam.


![](assets/retarget_10.png){zoomable="yes"}
