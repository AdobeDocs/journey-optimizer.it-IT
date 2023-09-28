---
solution: Journey Optimizer
product: journey optimizer
title: Esporta i set di dati nelle posizioni di archiviazione cloud
description: Scopri come esportare i set di dati utilizzando le destinazioni dell’archiviazione cloud di Adobe Experience Platform.
role: User
level: Beginner
keywords: piattaforma, data lake, creare, lake, set di dati, profilo
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: 08f24547237c01c581248d675c55c834c261b173
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 6%

---

# Esporta i set di dati nelle posizioni di archiviazione cloud {#export-datasets}

Journey Optimizer consente di stabilire una connessione live con le posizioni di archiviazione cloud per esportare il contenuto dei set di dati.

Esportando periodicamente i dati, è possibile assicurarsi di disporre di un record completo e aggiornato delle interazioni con i clienti, rendendolo facilmente disponibile per scopi di reporting, archiviazione o analisi dei dati.

## Destinazioni di archiviazione cloud disponibili {#destinations}

Puoi esportare i set di dati in 6 destinazioni di archiviazione cloud accessibili dall’ **[!UICONTROL Destinazioni]** nel menu **[!UICONTROL Catalogo]** scheda.

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Queste destinazioni sono tutte disponibili in versione beta e soggette a modifiche.

Informazioni dettagliate su ciascuna destinazione sono disponibili nella documentazione di Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [BLOB di Azure](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Data Landing Zone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Archiviazione cloud Google](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Set di dati di Journey Optimizer disponibili per l’esportazione {#datasets}

Scopri dalla tabella seguente quali set di dati Journey Optimizer puoi esportare a seconda del livello di prodotto (consulta [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}) |Set di dati|Descrizione|Livello| | ------- | ------- | ------- | | Set di dati evento feedback CCN AJO | Set di dati evento feedback CCN AJO | Prime | | Set di dati di classificazione AJO | Set di dati per l’acquisizione di eventi di feedback di applicazioni e-mail e push da Journey Optimizer. Creato tramite SDK. | Prime | | Set di dati del servizio di consenso AJO | Memorizza le informazioni sul consenso di un profilo. | Prime | | Set di dati evento esperienza tracciamento e-mail AJO | Registri di interazione per il canale e-mail utilizzato a scopo di reporting e creazione di pubblico.  | Prime | | Set di dati entità AJO | Set di dati per memorizzare i metadati di entità per i messaggi inviati all’utente finale.  | Prime | | Set di dati evento attività in entrata AJO | Set di dati per canali web e inApp Journey Optimizer per eventi di consegna e interazione. | Prime | | Set di dati profilo messaggi interattivi AJO | Memorizza i profili creati per supportare le campagne attivate da API | Prime | | Set di dati evento feedback messaggio AJO | Registri di consegna dei messaggi. Informazioni su tutte le consegne di messaggi da Journey Optimizer a scopo di generazione rapporti e creazione di pubblico. Anche il feedback dagli ISP dell’e-mail sui mancati recapiti viene registrato in questo set di dati. | Prime | | Estensione contatori profilo AJO | Contiene una mappa di oggetti contenente counter_value e expiryDate, con chiave counter_id | Prime | | Set di dati profilo push AJO | Memorizza i token di push di un profilo. | Prime | | Set di dati evento tracciamento push AJO | Registri di interazione per il canale push utilizzato a scopo di reporting e creazione di pubblico.  | Prime | | Set di dati superfici AJO | Set di dati vuoto relativo allo schema Journey Optimizer Inbound Surfaces | Prime | | AOAutputForUPSDataset | Contiene tutte le appartenenze al pubblico AO da riscrivere su UPS | Prime | | Set di dati profilo orchestrazione pubblico | Generato da audience composition per i tipi di pubblico di Audience Composition. Contiene tutti i tipi di pubblico di Audience Composition, i relativi attributi e i dati di arricchimento | Prime | | Archivio oggetti decisione - Attività | noto anche come Decisioni nell’interfaccia utente di. Ma questi sono gli oggetti che un utente crea che mettono insieme tutti i blocchi predefiniti, inclusa la logica decisionale. Ad esempio, per un particolare posizionamento (posizione), quali offerte devono essere considerate (raccolta di offerte) e quale metodo di classificazione utilizzare su tali offerte. | Ultimate | | Archivio oggetti decisione - Offerte di fallback | questo è l’archivio per l’altro tipo di offerta creato da un utente. In particolare, se non sono idonei a visualizzare un’offerta personalizzata e hanno bisogno di vedere qualcosa, vedranno almeno l’offerta di fallback. Questo set di dati contiene gli attributi per questo tipo di offerta | Ultimate | | Archivio oggetti decisione - Offerte personalizzate | questo è l’archivio per un tipo di offerta creato da un utente. Questo set di dati contiene gli attributi di questo tipo di offerta | Ultimate | | Archivio oggetti decisione - Posizionamenti | questo è l’archivio degli oggetti che definiscono la posizione in cui deve essere visualizzata un’offerta. | Ultimate | | Eventi passaggio Percorso | Acquisisce tutti gli eventi di esperienza delle fasi del Percorso generati da Journey Optimizer e destinati a essere utilizzati da servizi come Reporting. | Prime | | PERCORSI | Set di dati metadati contenente le informazioni relative a ciascuna fase di un percorso | Prime | | ODE DecisionEvents - Prod decisioning | Ogni volta che prendiamo una decisione sulla base di una richiesta, lo contiamo come un evento decisionale | Ultimate |

## Prerequisiti {#prerequisites}

Per esportare i set di dati, è necessario [autorizzazioni di controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions) elencate di seguito. Leggi le [panoramica sul controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) oppure contatta l’amministratore del prodotto per ottenere le autorizzazioni necessarie.

| Categoria | Autorizzazione |
|--|--|
| Destinazioni | Gestire e attivare le destinazioni dei set di dati |
| Gestione dati | Visualizzare i set di dati |
| Destinazioni | Visualizza destinazioni |

## Passaggi principali per esportare i set di dati {#main-steps}

I passaggi principali per esportare un set di dati in una posizione di archiviazione cloud sono i seguenti:

![](assets/dataset-export-process.png)

Informazioni dettagliate su ciascun passaggio sono disponibili nella documentazione di Adobe Experience Platform: [Esportare i set di dati nelle destinazioni dell’archiviazione cloud](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html).

1. **Configurare la destinazione dell’archiviazione cloud**. Se non lo hai già fatto, connettiti a una destinazione di archiviazione cloud dal catalogo delle destinazioni. [Scopri come creare una nuova connessione di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **Seleziona la destinazione dell’archiviazione cloud** dove desideri esportare i set di dati. Nel catalogo delle destinazioni, fai clic su **[!UICONTROL Esportare i set di dati]** sulla scheda desiderata e selezionare la connessione da utilizzare.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Se utilizzi Adobe Journey Optimizer insieme ai profili cliente in tempo reale, le schede di destinazione visualizzano un pulsante &quot;Attiva&quot; che consente di esportare set di dati e attivare tipi di pubblico per questa destinazione, a seconda delle autorizzazioni abilitate.

1. **Seleziona i set di dati** che desideri esportare nella destinazione selezionata. [Ulteriori informazioni sui set di dati di Journey Optimizer disponibili per l’esportazione](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Pianificare l’esportazione** del set di dati. Specifica quando deve iniziare l’esportazione e con quale frequenza.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Rivedi e conferma l’esportazione** controllando il riepilogo visualizzato alla fine della configurazione.

   <!--![](assets/dataset-export-review.png)-->

Una volta completata l’esportazione, il contenuto del set di dati viene depositato nella posizione di archiviazione cloud in base alla pianificazione configurata. [Scopri come verificare l’esportazione corretta del set di dati](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
