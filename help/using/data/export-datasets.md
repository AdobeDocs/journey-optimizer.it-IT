---
solution: Journey Optimizer
product: journey optimizer
title: Esporta i set di dati nelle posizioni di archiviazione cloud
description: Scopri come esportare i set di dati utilizzando le destinazioni dell’archiviazione cloud di Adobe Experience Platform.
role: User
level: Beginner
badge: label="Beta" type="Informative"
keywords: piattaforma, data lake, creare, lake, set di dati, profilo
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: 98957bfff8fdc719dc81d3064eb3332c3f9f2cc4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Esporta i set di dati nelle posizioni di archiviazione cloud {#export-datasets}

>[!AVAILABILITY]
>
>La funzione di esportazione dei set di dati è attualmente in versione beta e disponibile per tutti gli utenti di Adobe Journey Optimizer. Collabora con il tuo rappresentante Adobe per accedere alle destinazioni se non hai già accesso.

Journey Optimizer consente di stabilire una connessione live con le posizioni di archiviazione cloud per esportare il contenuto dei set di dati.

Esportando periodicamente i dati, è possibile assicurarsi di disporre di una registrazione completa e aggiornata delle interazioni con i clienti, utilizzare tali informazioni a scopo di reporting o analisi e mantenere la conformità con i requisiti legali.

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

## Prerequisiti {#prerequisites}

Prima di iniziare a esportare i set di dati, verifica i seguenti prerequisiti:

* Per esportare i set di dati, è necessario **Gestire le destinazioni**, **Visualizza destinazioni**, **Attivare le destinazioni**, e **Gestire e attivare le destinazioni dei set di dati** [autorizzazioni di controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). Leggi le [panoramica sul controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) oppure contatta l’amministratore del prodotto per ottenere le autorizzazioni necessarie.

* Assicurati che il set di dati da esportare non contenga dati di seconda generazione. Questa funzione supporta solo l’esportazione di dati di prima generazione, ovvero di dati non elaborati definiti nella [Descrizione del prodotto Real-time Customer Data Platform](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). I dati di prima generazione includono set di dati introdotti tramite origini Adobe Experience Platform o set di dati raccolti utilizzando soluzioni Adobe come Connettore dati di Analytics e set di dati di registri/rapporti di Journey Optimizer.

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
   >Se utilizzi Adobe Journey Optimizer insieme ai profili cliente in tempo reale, le schede di destinazione visualizzano un pulsante &quot;Attiva&quot; che consente di esportare i set di dati e attivare segmenti per questa destinazione, a seconda delle autorizzazioni abilitate.

1. **Seleziona i set di dati** che desideri esportare nella destinazione selezionata.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Pianificare l’esportazione** del set di dati. Specifica quando deve iniziare l’esportazione e con quale frequenza.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Rivedi e conferma l’esportazione** controllando il riepilogo visualizzato alla fine della configurazione.

   <!--![](assets/dataset-export-review.png)-->

Una volta completata l’esportazione, il contenuto del set di dati viene depositato nella posizione di archiviazione cloud in base alla pianificazione configurata. [Scopri come verificare l’esportazione corretta del set di dati](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
