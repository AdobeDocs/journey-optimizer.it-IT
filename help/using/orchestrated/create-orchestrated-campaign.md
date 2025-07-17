---
solution: Journey Optimizer
product: journey optimizer
title: Creare e pianificare campagne orchestrate con Journey Optimizer
description: Scopri come creare e pianificare una campagna orchestrata con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 12%

---


# Creare e pianificare una campagna orchestrata {#create-first-campaign}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | <b>[Crea e pianifica la campagna](create-orchestrated-campaign.md)</b><br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++
<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Creare una campagna orchestrata in [!DNL Adobe Journey Optimizer] e configurarne la pianificazione di esecuzione per controllare quando viene avviata e con quale frequenza viene eseguita. Scegli di avviare la campagna immediatamente, a una data e un’ora specifiche o su base ricorrente utilizzando opzioni di pianificazione flessibili, ad esempio frequenze giornaliere, settimanali o mensili.

## Creare la campagna {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Elenco delle campagne orchestrate"
>abstract="Nella scheda **Orchestrazione** sono elencate tutte le campagne orchestrate. Fai clic sul nome di una campagna orchestrata per modificarla. Fai clic sul pulsante **Crea campagna orchestrata** per aggiungerne una nuova."

Per creare una campagna orchestrata, effettua le seguenti operazioni:

1. Vai al menu **[!UICONTROL Campagne]**, seleziona la scheda **[!UICONTROL Orchestrazione]** e fai clic su **[!UICONTROL Crea campagna]**.

   ![](assets/inventory-create.png)

1. Immetti un nome e una descrizione per la campagna.

1. *(facoltativo)* Utilizza il campo **[!UICONTROL Tag]** per assegnare alla campagna i tag unificati Adobe Experience Platform. Ciò ti consente di classificarli facilmente e di migliorare la ricerca dall’elenco delle campagne orchestrate. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags).

1. Fai clic su **[!UICONTROL Crea]**.

La campagna orchestrata viene ora creata e visualizzata nell’elenco delle campagne orchestrate. Puoi aggiornare queste proprietà in qualsiasi momento facendo clic sull&#39;icona ![Impostazioni campagna](assets/do-not-localize/campaign-settings.svg) nell&#39;area di lavoro della campagna.

## Pianificare la campagna {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Modulo di pianificazione"
>abstract="In qualità di manager della campagna, puoi pianificare il lancio automatico delle campagne in momenti specifici, abilitando un calendario e dati di targeting precisi per le comunicazioni di marketing."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validità del modulo di pianificazione"
>abstract="È possibile definire un periodo di validità per il modulo di pianificazione. Può essere permanente (impostazione predefinita) o valido fino a una data specifica."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Opzioni del modulo di pianificazione"
>abstract="Definisci la frequenza del modulo di pianificazione. Può essere eseguito in un determinato momento, una o più volte al giorno, alla settimana o al mese."

Per impostazione predefinita, le campagne orchestrate iniziano quando vengono attivate manualmente e terminano una volta eseguite le attività associate. Se preferisci ritardare l’esecuzione o eseguire una campagna di questo tipo su base ricorrente, puoi definire una pianificazione per la campagna.

Quando pianifichi campagne orchestrate per garantire prestazioni e comportamenti ottimali, considera le seguenti best practice:

* Non pianificare l’esecuzione di una campagna orchestrata per più di 15 minuti, in quanto potrebbe impedire le prestazioni complessive del sistema e creare blocchi nel database.
* Se desideri inviare un messaggio unico nella campagna orchestrata, puoi impostarlo per l&#39;esecuzione **Una volta**.
* Se desideri inviare un messaggio ricorrente nella campagna orchestrata, devi utilizzare le opzioni **Pianificazione** e impostare la frequenza di esecuzione. L’attività di consegna ricorrente non ti consente di definire una pianificazione.

Per configurare la pianificazione della campagna, effettua le seguenti operazioni:

1. Apri la campagna e fai clic sul pulsante **[!UICONTROL Appena possibile]**.

   ![](assets/create-schedule.png)

1. Seleziona una frequenza di esecuzione per la campagna, quindi configura le opzioni disponibili. Le impostazioni variano a seconda della frequenza selezionata:

   +++Una volta

   Esegui la campagna una sola volta a una data e un’ora specificate.

   * **[!UICONTROL Data]**: seleziona la data di esecuzione della campagna.
   * **[!UICONTROL Ora]**: seleziona l&#39;ora specifica di esecuzione della campagna.

+++

   +++Giornaliero

   Esegui la campagna ogni giorno o nei giorni selezionati.

   * **[!UICONTROL Ricorrenza giornaliera]**: scegli la frequenza di esecuzione della campagna:
      * **[!UICONTROL Ogni giorno]**: esegue la campagna ogni giorno della settimana, inclusi i fine settimana.
      * **[!UICONTROL Nei giorni feriali]**: esegue la campagna solo dal lunedì al venerdì.
      * **[!UICONTROL Fino a un periodo specifico]**: esegue la campagna ogni giorno entro un intervallo di date definito (ad esempio, dal 1° luglio al 15 luglio). La campagna non verrà eseguita al di fuori di questo intervallo.
      * **[!UICONTROL Nei giorni selezionati della settimana]**: esegue la campagna solo nei giorni specificati della settimana (ad esempio, lunedì, mercoledì, venerdì).

   * **[!UICONTROL Ora di inizio]**: definisci l&#39;ora in cui la campagna deve essere eseguita ogni giorno.

+++

   +++Più volte al giorno

   Esegui la campagna più volte nello stesso giorno. È possibile scegliere orari specifici o impostare una frequenza periodica.

   * **[!UICONTROL Ore selezionate]**: seleziona le ore specifiche in cui la campagna deve essere eseguita e configurane la ricorrenza giornaliera (eseguita ogni giorno della settimana o in alcuni giorni).
   * **[!UICONTROL Periodico]**: scegli di eseguire la campagna ogni n minuti o ore. Puoi anche definire l’intervallo di tempo all’interno del giorno in cui sono consentite le esecuzioni.

+++

   +++Settimanale

   Esegui la campagna su base settimanale, con opzioni per giorni specifici.

   * **[!UICONTROL Frequenza]**: scegli la frequenza di esecuzione della campagna (ad esempio, ogni settimana, ogni 2 settimane).
   * **[!UICONTROL A partire dalla data]**: selezionare la data di inizio della ricorrenza.
   * **[!UICONTROL Ricorrenza giornaliera]**: scegli giorni specifici della settimana per l&#39;esecuzione (ad esempio, ogni lunedì e giovedì).
   * **[!UICONTROL Ora di inizio]**: imposta l&#39;ora in cui la campagna deve essere eseguita nei giorni selezionati.

+++

   +++Mensile

   Esegui la campagna su base mensile, con opzioni per giorni specifici.

   * **[!UICONTROL Ricorrenza mensile]**: seleziona se la campagna viene eseguita ogni mese o solo durante mesi specifici.
   * **[!UICONTROL Ricorrenza giornaliera]**:
      * **[!UICONTROL Ogni giorno]**: esegue la campagna in ogni giorno del mese, inclusi i fine settimana.
      * **[!UICONTROL Ultimo giorno del mese]**: esegue la campagna solo nell&#39;ultimo giorno di calendario di ogni mese (ad esempio, 31 gennaio, 28/29 febbraio).
      * **[!UICONTROL Giorno specifico del mese (ad esempio, 15)]**: esegue la campagna in un giorno specificato (ad esempio, il 15 di ogni mese).
      * **[!UICONTROL Primo/Ultimo giorno della settimana]** (ad esempio, primo lunedì):      Esegue la campagna in un giorno feriale specificato (ad esempio, il 15 di ogni settimana).
      * **[!UICONTROL Giorni selezionati della settimana]**: esegue la campagna in un giorno specificato.

   * **[!UICONTROL Ora di inizio]**: imposta l&#39;ora di esecuzione della campagna.

+++

1. Utilizza l&#39;impostazione **[!UICONTROL Periodo di validità]** per definire una data di inizio e una data di fine specifiche, limitando l&#39;esecuzione della campagna a un intervallo di tempo limitato.

1. Per le pianificazioni ricorrenti, fai clic sul pulsante **[!UICONTROL Anteprima ore avvio]** per visualizzare in anteprima le date e le ore di esecuzione imminenti esatte in base alla configurazione corrente. Questo aiuta a convalidare la pianificazione prima dell’attivazione e garantisce che la campagna venga eseguita come previsto.

>[!NOTE]
>
>Quando pianifichi campagne in [!DNL Adobe Journey Optimizer], assicurati che la data/ora di inizio sia allineata alla prima consegna desiderata. Per le campagne ricorrenti, se l’ora pianificata iniziale è già passata, le campagne passeranno alla successiva fascia oraria disponibile in base alle relative regole di ricorrenza.

Nell’esempio seguente, l’attività è configurata in modo che la campagna orchestrata venga eseguita due volte al giorno alle 9 e alle 12, ogni giorno della settimana dal 1° ottobre 2025 al 1° gennaio 2026.

![Modulo di pianificazione configurato per eseguire la campagna due volte al giorno alle 9 e alle 12](assets/scheduler-sample.png){width="50%" align="left"}

## Passaggi successivi {#next}

Una volta configurate le impostazioni e la pianificazione della campagna, sei pronto per iniziare a orchestrare le diverse attività che eseguirà. [Scopri come orchestrare le attività della campagna](../orchestrated/orchestrate-activities.md)
