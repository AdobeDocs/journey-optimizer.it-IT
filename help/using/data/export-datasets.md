---
solution: Journey Optimizer
product: journey optimizer
title: Esportare i set di dati in percorsi di archiviazione cloud
description: Scopri come esportare i set di dati utilizzando le destinazioni di archiviazione cloud Adobe Experience Platform.
role: User
level: Beginner
keywords: piattaforma, data lake, creare, lago, set di dati, profilo
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 1%

---


# Esportare i set di dati in percorsi di archiviazione cloud {#export-datasets}

>[!AVAILABILITY]
>
>La funzione di esportazione dei set di dati è attualmente in versione beta e disponibile per tutti gli utenti di Adobe Journey Optimizer. Collabora con il tuo rappresentante Adobe per accedere alle destinazioni se non hai già accesso.

Journey Optimizer consente di stabilire una connessione live con le posizioni di archiviazione cloud per esportare il contenuto dei set di dati.

Esportando periodicamente i dati, puoi assicurarti di disporre di una registrazione completa e aggiornata delle interazioni dei tuoi clienti, utilizzare queste informazioni a scopo di reporting o analisi e mantenere la conformità ai requisiti legali.

## Destinazioni di archiviazione cloud disponibili {#destinations}

Puoi esportare i set di dati in 6 destinazioni di archiviazione cloud accessibili da **[!UICONTROL Destinazioni]** nel menu **[!UICONTROL Catalogo]** scheda .

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Queste destinazioni sono tutte disponibili in versione beta e soggette a modifiche.

Informazioni dettagliate su ciascuna destinazione sono disponibili nella documentazione di Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [BLOB di Azure](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Data Landing Zone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google Cloud Storage](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Prerequisiti {#prerequisites}

Prima di esportare i set di dati, verifica i seguenti prerequisiti:

* Per esportare i set di dati, è necessario **Gestire le destinazioni**, **Visualizzare le destinazioni**, **Attivare le destinazioni** e **Gestire e attivare le destinazioni del set di dati** [autorizzazioni di controllo accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). Leggi la sezione [panoramica sul controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) oppure contatta l’amministratore del prodotto per ottenere le autorizzazioni richieste.

* Questa funzione supporta solo l’esportazione di dati di prima generazione, ovvero di dati non elaborati come definiti nella [Descrizione del prodotto Real-time Customer Data Platform](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). Assicurati che il set di dati da esportare non contenga dati di seconda generazione.

## Passaggi principali per esportare i set di dati {#main-steps}

I passaggi principali per esportare un set di dati in un percorso di archiviazione cloud sono i seguenti:

![](assets/dataset-export-process.png)

Informazioni dettagliate su ciascun passaggio sono disponibili nella documentazione di Adobe Experience Platform: [Esportare i set di dati nelle destinazioni di archiviazione cloud](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **Configurare la destinazione di archiviazione cloud**. Se non lo hai già fatto, connettiti a una destinazione di archiviazione cloud dal catalogo delle destinazioni. [Scopri come creare una nuova connessione di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **Selezionare la destinazione di archiviazione cloud** dove esportare i set di dati. Nel catalogo delle destinazioni, fai clic sul pulsante **[!UICONTROL Esportare i set di dati]** sulla scheda desiderata e seleziona la connessione da utilizzare.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Se utilizzi Adobe Journey Optimizer insieme ai profili cliente in tempo reale, le schede di destinazione visualizzeranno un pulsante &quot;Attiva&quot;, che consente di esportare i set di dati e attivare i segmenti per questa destinazione, a seconda delle autorizzazioni abilitate.

1. **Selezionare i set di dati** da esportare nella destinazione selezionata.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Pianificare l’esportazione** del set di dati. Specifica quando deve iniziare l’esportazione e a quale frequenza dovrebbe verificarsi.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Rivedi e conferma l’esportazione** controllando il riepilogo visualizzato alla fine della configurazione.

   <!--![](assets/dataset-export-review.png)-->

Una volta completata l’esportazione, il contenuto del set di dati viene depositato nel percorso di archiviazione cloud in base alla pianificazione configurata. [Scopri come verificare l’esportazione dei set di dati di successo](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
