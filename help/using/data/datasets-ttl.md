---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui set di dati Guardrail Time-to-live (TTL)
description: Set di dati guardrail time-to-live in [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: piattaforma, data lake, creare, lake, set di dati, profilo
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: fbd0280d293cef3548b48c2992b4f9f2793a7e1f
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 18%

---

# Guardrail TTL (Time-to-live) dei set di dati {#ttl-guardrail}

A febbraio 2025 è stato introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in **nuove sandbox e nuove organizzazioni** come segue:

* 90 giorni per i dati nell’archivio dei profili
* 13 mesi per i dati nel data lake

Questa modifica verrà implementata in **sandbox cliente esistenti** in una fase successiva.

## Set di dati interessati {#datasets}

La tabella seguente elenca tutti i set di dati interessati e il rispettivo Time-To-Live nel data lake e nell’archivio profili.

| Set di dati | TTL del data lake | TTL archivio profili |
|------|-----|-----|
| Set di dati evento feedback messaggi di AJO | 13 mesi | 90 giorni |
| Set di dati sull’evento di tracciamento e-mail di AJO | 13 mesi | 90 giorni |
| Set di dati evento di tracciamento push di AJO | 13 mesi | 90 giorni |
| Set di dati di entità AJO | 13 mesi | 90 giorni |
| Set di dati superfici AJO | 13 mesi | n/d |
| Set di dati evento attività in entrata AJO | 13 mesi | 90 giorni |
| Set di dati di classificazione AJO | 13 mesi | n/d |
| Set di dati evento feedback Ccn e-mail AJO | 13 mesi | n/d |
| Set di dati evento acpEntity | 13 mesi | n/d |
| Percorsi | 13 mesi | n/d |
| Eventi passaggio percorso | 13 mesi | n/d |
| Archivio di oggetti decisionali - Offerte personalizzate | 13 mesi | n/d |
| Archivio oggetti decisione - Offerte di fallback | 13 mesi | n/d |
| Archivio oggetti decisione - Posizionamenti | 13 mesi | n/d |
| Archivio oggetti decisione - Attività | 13 mesi | n/d |
| Archivio di oggetti Experience Decisioning - Elementi di offerta personalizzati | 13 mesi | n/d |
| ODE DecisionEvents - Prod Decisioning | 13 mesi | n/d |

## Domande frequenti {#faq}

Di seguito è riportato un elenco di risposte alle domande più frequenti sui set di dati TLL.

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
>I dati memorizzati nel profilo sono soggetti al diritto Volume di dati totale. Pertanto, qualsiasi aumento dell’archiviazione dei dati nel profilo a seguito di un’estensione TTL viene conteggiato nell’adesione al volume totale di dati. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=it){target=_blank}

+++

+++I clienti possono aumentare il TTL per i dati del set di dati di sistema [!DNL Journey Optimizer] nel data lake? 

Le estensioni TTL non sono attualmente supportate. I clienti possono esportare i dati tramite Destinazioni per conservarli più a lungo. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=it){target=_blank}. Inoltre, i clienti con un diritto **[!DNL Data Distiller]** possono creare set di dati derivati per memorizzare i dati nel data lake senza un TTL. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

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
