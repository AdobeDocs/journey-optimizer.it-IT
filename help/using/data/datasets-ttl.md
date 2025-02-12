---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sul Time-to-live (TTL) e sulle modifiche della segmentazione in streaming
description: Modifiche al time-to-live e alla segmentazione in streaming in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: piattaforma, data lake, creare, lake, set di dati, profilo
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: ccb4cc944271fb197e7aee87f57b51c28cb3565f
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 13%

---

# Modifiche al time-to-live e alla segmentazione in streaming {#ttl-guardrail}

## Aggiornamenti della segmentazione in streaming {#segmentation-update}

A partire dal 1° novembre 2024, la segmentazione in streaming non supporterà più l’utilizzo di eventi di invio e apertura dal tracciamento e dai set di dati di feedback di Journey Optimizer. Questa modifica verrà applicata a tutte le sandbox e organizzazioni della clientela. Le informazioni sui motivi per cui questa pratica è stata scoraggiata in passato sono disponibili [qui](../audience/about-audiences.md#streaming-segmentation-events-guardrails).

**Domande frequenti**

+++ Queste modifiche influiranno sull’utilizzo di clic o altri eventi di tracciamento?

Questa modifica influisce solo sull’utilizzo degli eventi di invio e apertura; i clic e altri eventi di tracciamento possono ancora essere utilizzati in un segmento di streaming.

+++

+++ Questa modifica influisce sulla segmentazione batch?

Questa modifica influisce solo sulla segmentazione in streaming; gli eventi di invio e apertura possono ancora essere utilizzati in un segmento batch. Se vengono utilizzati in un segmento di streaming, verranno valutati in modo batch.

+++

+++ Questa modifica influirà sulla raccolta dei dati di tracciamento?

Questa modifica non influisce sulla raccolta dei dati di tracciamento. Gli eventi di invio e apertura continueranno a essere raccolti.

+++

+++ Questo cambiamento influisce sugli eventi di reazione?

Gli eventi di reazione nei Percorsi non sono influenzati da questo cambiamento.

+++

+++ Questa modifica verrà applicata solo alle sandbox di produzione oppure anche alle sandbox di sviluppo?

Questa modifica verrà applicata a tutti i tipi di sandbox.

+++

+++ La modifica interessa anche gli eventi di feedback derivanti dall’evento di invio?

Questa modifica si applica anche agli eventi di esclusione e agli eventi di mancato recapito/ritardo risultanti dall’invio.

+++

## Aggiornamento del time-to-live (TTL) per fasi {#ttl}

A partire da febbraio 2025, un guardrail time-to-live (TTL) verrà introdotto nei set di dati generati dal sistema Journey Optimizer in **nuove sandbox e nuove organizzazioni** come segue:

* 90 giorni per i dati nell’archivio dei profili
* 13 mesi per i dati nel data lake

Questa modifica verrà implementata in **sandbox cliente esistenti** in una fase successiva.

**Domande frequenti**

+++ Questa modifica verrà applicata solo alle sandbox di produzione oppure anche alle sandbox di sviluppo?

Questa modifica verrà applicata a tutti i tipi di sandbox.

+++

+++ Per il TTL di 90 giorni nell’archivio dei profili, sono interessati anche i profili?

I dati del set di dati generati dal sistema nel profilo vengono eliminati dopo 90 giorni, non i profili stessi.

+++

+++ Se i dati di un set di dati generato dal sistema vengono inviati al Customer Journey Analytics (CJA), anche i dati in CJA saranno interessati dal TTL?

I dati in CJA sono sincronizzati con quelli di Experience Platform. Pertanto, anche la rimozione dei dati a causa di un TTL sui dati del set di dati generato dal sistema influirà sui dati in CJA.

+++
