---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Salva pubblico
description: Scopri come utilizzare l’attività Save audience in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Salva pubblico {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Salvare l’attività del pubblico"
>abstract="L&#39;attività **Save audience** è un&#39;attività **Targeting** che consente di aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione generata in precedenza nella campagna orchestrata. Una volta creati, questi tipi di pubblico vengono aggiunti all’elenco dei tipi di pubblico dell’applicazione e sono accessibili dal menu **Tipi di pubblico**."


+++ Sommario

| Benvenuto in Campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - [Crea pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - <b>[Salva pubblico](save-audience.md)</b> - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L&#39;attività **[!UICONTROL Save audience]** è un&#39;attività **[!UICONTROL Targeting]** utilizzata per creare un nuovo pubblico o aggiornarne uno esistente in base alla popolazione generata in precedenza nella campagna orchestrata. Una volta salvato, il pubblico viene aggiunto all&#39;elenco dei tipi di pubblico dell&#39;applicazione e diventa accessibile dal menu **[!UICONTROL Tipi di pubblico]**.

Viene comunemente utilizzato per acquisire segmenti di pubblico generati nello stesso flusso di lavoro della campagna, rendendoli disponibili per il riutilizzo in campagne future. In genere, è connesso ad altre attività di targeting, come **[!UICONTROL Genera pubblico]** o **[!UICONTROL Combina]**, per salvare la popolazione di destinazione finale.

## Configurare l’attività Salva pubblico {#save-audience-configuration}

Per configurare l’attività **[!UICONTROL Salva pubblico]**, segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Save audience]** alla tua campagna orchestrata.

1. Immetti un’**[!UICONTROL etichetta del pubblico]** che identificherà il pubblico salvato.

1. Scegli un **[!UICONTROL campo di mappatura profilo&#x200B;]** dalla dimensione di targeting della campagna.

   ➡️ [Segui i passaggi descritti in questa pagina per creare la tua dimensione di targeting delle campagne](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Fai clic su **[!UICONTROL Aggiungi mappature pubblico]** per associare il pubblico salvato ad altri campi di identità.

   ![](../assets/save-audience-2.png)

1. Completa la configurazione salvando e pubblicando la campagna orchestrata. Questo genererà e archivierà il tuo pubblico.

Il contenuto del pubblico salvato è quindi disponibile nella relativa visualizzazione dettagliata, accessibile dal menu **[!UICONTROL Tipi di pubblico]** oppure può essere selezionato quando si esegue il targeting di un pubblico, ad esempio con un&#39;attività **[!UICONTROL Read audience]**.

![](../assets/save-audience-4.png)


## Esempio {#save-audience-example}

L’esempio seguente illustra come creare un pubblico semplice utilizzando il targeting. Una query identifica tutti i destinatari che hanno prenotato un viaggio negli ultimi 30 giorni filtrando questa popolazione nella campagna orchestrata. Scegliendo **Destinatari - CRMID** come **dimensione di targeting**, il pubblico esegue il targeting di ogni singolo evento di prenotazione anziché del solo destinatario nel suo insieme. L’attività **[!UICONTROL Salva pubblico]** acquisisce quindi questi profili per creare un pubblico riutilizzabile di acquirenti recenti.

![](../assets/save-audience-3.png)
