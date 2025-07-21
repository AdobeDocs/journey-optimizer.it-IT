---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Read audience
description: Scopri come utilizzare l’attività Read audience in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 19%

---

# Leggi pubblico {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Attività Crea pubblico"
>abstract="L’attività **Leggi pubblico** ti consente di selezionare il pubblico che entrerà nella campagna orchestrata. Questo pubblico può essere un pubblico esistente di Adobe Experience Platform o uno estratto da un file CSV. Quando si inviano messaggi nel contesto di una campagna orchestrata, il pubblico del messaggio non è definito nell’attività del canale, ma nell’attività **Leggi pubblico** o **Crea pubblico**."


+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L&#39;attività **[!UICONTROL Read audience]** ti consente di recuperare un pubblico esistente, salvato o importato in precedenza, e di riutilizzarlo all&#39;interno di una campagna orchestrata. Questa attività è particolarmente utile per il targeting di un set predefinito di profili senza la necessità di eseguire un nuovo processo di segmentazione.

Una volta caricato il pubblico, puoi facoltativamente perfezionarlo selezionando un campo di identità univoco e arricchendo il pubblico con attributi di profilo aggiuntivi a scopo di targeting, personalizzazione o reporting.

## Configurare l’attività Read audience {#read-audience-configuration}

Segui questi passaggi per configurare l&#39;attività **[!UICONTROL Read audience]**:

1. Aggiungi un&#39;attività **[!UICONTROL Read audience]** alla campagna orchestrata.

   ![](../assets/read-audience-1.png)

1. Immetti un&#39;etichetta **[!UICONTROL Label]** per l&#39;attività.

1. Fai clic su ![icona di ricerca cartella](../assets/do-not-localize/folder-search.svg) per selezionare il pubblico a cui desideri rivolgerti per la tua campagna orchestrata.

   ![](../assets/read-audience-2.png)

1. Seleziona l&#39;**[!UICONTROL entità]** utilizzata per identificare in modo univoco i profili nel pubblico.

   ![](../assets/read-audience-3.png)

1. Seleziona **[!UICONTROL Aggiungi attributo profilo]** per arricchire il pubblico selezionato con dati aggiuntivi. Il pubblico risultante conterrà un elenco di destinatari, ciascuno arricchito con gli attributi di profilo selezionati.

1. Scegli gli **[!UICONTROL Attributi]** da aggiungere al pubblico.

   ![](../assets/read-audience-4.png)

## Esempio

Nell&#39;esempio seguente, l&#39;attività **[!UICONTROL Read audience]** viene utilizzata per recuperare un pubblico creato e salvato in precedenza dai profili abbonati alla newsletter. Il pubblico viene quindi arricchito con l&#39;attributo **Iscrizione fedeltà** per abilitare il targeting degli utenti che sono membri registrati del programma fedeltà.

![](../assets/read-audience-5.png)
