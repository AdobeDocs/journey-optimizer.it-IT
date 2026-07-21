---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui set di dati Guardrail Time-to-live (TTL)
description: Set di dati guardrail time-to-live in [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: piattaforma, data lake, creare, lake, set di dati, profilo
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
TQID: https://experienceleague.adobe.com/DvcQ6AcWhNIZXnTtmPozvSTp1Ait-oo-8wlo8hQ6xlI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2:
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: ef136412971fb3b0240d7d86f1698124495a868a
workflow-type: tm+mt
source-wordcount: 1226
ht-degree: 11%

---

# Guardrail TTL (Time-to-live) dei set di dati {#ttl-guardrail}

>[!BEGINSHADEBOX]

**In questa pagina:** Comprendere i limiti di conservazione del time-to-live nei set di dati generati dal percorso di Journey Optimizer in modo da pianificare per quanto tempo il tracciamento, il feedback e i dati di sistema rimangono disponibili e conservano i dati critici prima della scadenza.

>[!ENDSHADEBOX]

A febbraio 2025 è stato introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in **nuove sandbox e nuove organizzazioni** come segue:

* 90 giorni per i dati nell’archivio dei profili
* 13 mesi per i dati nel data lake

Questa modifica verrà applicata alle **sandbox cliente esistenti** a partire dal **1 ottobre 2026**.

## Set di dati interessati {#datasets}

La tabella seguente elenca tutti i set di dati interessati e il rispettivo Time-To-Live nel data lake e nell&#39;[archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it#profile-data-store){target="_blank"}.

| Set di dati | TTL del data lake | TTL archivio profili |
|------|-----|-----|
| Set di dati evento feedback messaggi di AJO | 13 mesi | 90 giorni |
| Set di dati sull’evento di tracciamento e-mail di AJO | 13 mesi | 90 giorni |
| Set di dati evento di tracciamento push di AJO | 13 mesi | 90 giorni |
| Set di dati superfici AJO | 13 mesi | n/d |
| Set di dati evento attività in entrata AJO | 13 mesi | 90 giorni |
| Set di dati evento feedback destinatario secondario AJO | 13 mesi | n/d |
| Set di dati evento entità | 13 mesi | n/d |
| Eventi passaggio percorso | 13 mesi | n/d |
| ODE DecisionEvents - Prod Decisioning | 13 mesi | n/d |

## Domande frequenti {#faq}

Di seguito sono riportate le domande frequenti sui set di dati Time-to-live (TTL).

Hai bisogno di altri dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}.

+++Quali tipi di set di dati sono soggetti a TTL?

Il TTL si applica solo ai set di dati di serie temporali. I set di dati di tipo record (come set di dati di entità, set di dati di classificazione e archivi di oggetti decisionali) non sono soggetti a TTL e pertanto non vengono visualizzati nella tabella dei set di dati interessati precedente.

+++

+++Questa modifica verrà applicata solo alle sandbox di produzione oppure anche alle sandbox di sviluppo?

Questa modifica verrà applicata a tutti i tipi di sandbox.

+++

+++Per il TTL di 90 giorni nell’archivio dei profili, sono interessati anche i profili?

I dati del set di dati generati dal sistema nel profilo vengono eliminati dopo 90 giorni, non i profili stessi.

+++

+++Se un set di dati generato dal sistema viene inviato a [!DNL Customer Journey Analytics] (CJA), anche i dati in CJA saranno interessati dal TTL?

I dati in [!DNL Customer Journey Analytics] sono sincronizzati con Experience Platform. Pertanto, anche la rimozione dei dati a causa di un TTL sui dati del set di dati generato dal sistema influirà sui dati in [!DNL Customer Journey Analytics].

+++

+++ I clienti possono aumentare il TTL per i dati del set di dati di sistema [!DNL Journey Optimizer] nell&#39;archivio profili? 

Le estensioni TTL non sono attualmente supportate. Tuttavia, sono previsti lavori per ottimizzare il processo TTL al fine di consentire tali richieste di estensione a partire dalla seconda metà del 2025.

>[!NOTE]
>
>I dati memorizzati nel profilo sono soggetti al diritto Volume di dati totale. Pertanto, qualsiasi aumento dell’archiviazione dei dati nel profilo a seguito di un’estensione TTL viene conteggiato nell’adesione al volume totale di dati. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=it){target="_blank"}

+++

+++I clienti possono aumentare il TTL per i dati del set di dati di sistema [!DNL Journey Optimizer] nel data lake? 

Le estensioni TTL non sono attualmente supportate. I clienti possono esportare i dati tramite Destinazioni per conservarli più a lungo. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=it){target="_blank"}. Inoltre, i clienti con un diritto **[!DNL Data Distiller]** possono creare set di dati derivati per memorizzare i dati nel data lake senza un TTL. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/query/data-distiller/derived-datasets/overview){target="_blank"}

+++

+++I TTL influiscono sulle seguenti funzionalità? 

* **Archivio ricerche**: no
* **Limitazione Percorsi**: No
* **Limite offerte**: No
* **Ottimizzazione dell&#39;ora di invio (STO)**: No
* **Limite di frequenza dei messaggi** (ad esempio, regole business): no
* **Generazione rapporti**: No

  >[!NOTE]
  >
  >Un TTL è già implementato nella connessione [!DNL Customer Journey Analytics] (CJA), che riduce a 13 mesi il periodo di look-back massimo effettivo dei dati del set di dati interessati.

* **Origine dati di Experience Platform**: non applicabile - Il recupero degli eventi di esperienza non è supportato tramite origini dati.
* **Attributi calcolati**: sì - Il calcolo della retrocompilazione iniziale sarà limitato agli ultimi 90 giorni di dati; l&#39;attributo calcolato verrà aggiornato in base agli eventi incrementali per gli aggiornamenti successivi. Non appena gli aggiornamenti successivi raggiungono il periodo di look-back (massimo 6 mesi), il TTL essenzialmente non influisce più sull’attributo calcolato. Scopri di più.
* **Segmentazione e retargeting**: sì - La segmentazione dipende dai dati nell&#39;archivio dei profili; pertanto, il lookback è limitato a 90 giorni sui dati del set di dati interessati.
* **Tracciamento**: sì - Riduce a 90 giorni il periodo di look-back massimo effettivo dei dati del set di dati interessati. I dati dei set di dati interessati rimangono per 13 mesi nel data lake.

+++

+++Quale marca temporale viene utilizzata per l’applicazione del TTL (ad esempio, per i casi di utilizzo di backfill)? 

Viene utilizzato il timestamp dell’evento (ovvero, non la data di acquisizione).

+++

+++In che modo il nuovo TTL influisce sui casi di utilizzo che richiedono una conservazione dei dati più lunga (ad esempio, escludendo i profili che hanno ricevuto un’e-mail negli ultimi 120 giorni o limitando le e-mail in un anno)?

Il nuovo criterio TTL limiterà il periodo di look-back per i dati del set di dati generati dal sistema nell’archivio dei profili a 90 giorni e nel data lake a 13 mesi. Saranno interessati i casi d’uso che richiedono l’accesso ai dati oltre tali periodi. Ad esempio, la segmentazione del pubblico o il limite di frequenza basato su eventi di età superiore a 90 giorni nell’archivio dei profili non sarà più possibile utilizzando i set di dati di sistema.

+++

+++Quali alternative sono disponibili per la conservazione dei dati più a lungo del TTL?

Per i clienti che richiedono una conservazione più lunga sono disponibili due opzioni:

* **Esporta nell&#39;archiviazione esterna**: esporta i dati rilevanti dai set di dati di AJO prima della scadenza del TTL. Adobe Journey Optimizer supporta l’esportazione dei set di dati in varie destinazioni di archiviazione cloud (Amazon S3, Azure Blob, Google Cloud Storage, ecc.). [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=it){target="_blank"}
* **Set di dati derivati da Data Distiller**: i clienti con un diritto a Data Distiller possono impostare query automatizzate per copiare dati critici in un set di dati derivato nel data lake, che può essere archiviato senza un TTL. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/query/data-distiller/derived-datasets/overview){target="_blank"}

+++

+++Cosa devono fare i clienti per prepararsi alla modifica del TTL?

* Esamina i tuoi casi d’uso e identifica quelli che richiedono la conservazione dei dati oltre i nuovi TTL.
* Imposta le query automatizzate per copiare i dati critici in set di dati derivati prima dell’eliminazione dei dati.
* Rivolgiti al tuo rappresentante Adobe per discutere di eventuali esigenze aggiuntive o potenziali estensioni TTL (pianificate per le versioni future).

+++

+++In che modo i clienti vengono informati prima che il TTL venga applicato alle sandbox esistenti?

Adobe avvisa i clienti interessati prima di applicare il TTL alle sandbox esistenti. Per questo rollout, Adobe ha inviato una notifica interna al prodotto e ha pubblicato questa modifica nelle note sulla versione del prodotto, dando ai clienti un preavviso di circa due mesi prima che il guardrail entri in vigore il 1° ottobre 2026.

+++

+++Posso eliminare i set di dati generati dal sistema di Journey Optimizer?

I set di dati generati dal sistema Journey Optimizer sono protetti e non possono essere eliminati tramite l’interfaccia utente standard di Adobe Experience Platform. Questi set di dati sono essenziali per la funzionalità di Journey Optimizer e sono gestiti dal sistema.

Se devi rimuovere definitivamente un set di dati di sistema Journey Optimizer (ad esempio, per ambienti di controllo qualità, pulizia della sandbox o requisiti specifici di igiene dei dati), contatta il team di progettazione Adobe o l’Assistenza clienti Adobe. Questi set di dati richiedono procedure di back-end specializzate per garantire la rimozione completa e sicura.

>[!NOTE]
>
>Per la pulizia di routine dei dati all&#39;interno di questi set di dati di sistema, utilizza le operazioni del **[!UICONTROL ciclo di vita dei dati]** disponibili tramite Privacy Service per eliminare record o identità specifici. [Ulteriori informazioni](../privacy/data-hygiene.md)


+++
