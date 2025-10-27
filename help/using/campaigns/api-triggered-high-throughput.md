---
solution: Journey Optimizer
product: journey optimizer
title: Attiva la modalità High Throughput per le campagne attivate dall’API
description: Scopri come attivare la modalità Alta velocità per le campagne attivate dall’API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
source-git-commit: 4521990a02092365f996a81299ada55433639fb7
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 2%

---


# Attiva la modalità High Throughput per le campagne attivate dall’API {#high-throughput}

La modalità High Throughput è progettata per le organizzazioni che necessitano di **messaggi transazionali su vasta scala e in tempo reale** (fino a 5000 transazioni al secondo). A differenza delle normali campagne attivate da API, le campagne a throughput elevato operano in modo indipendente dai profili di Adobe e richiedono un modello di configurazione diverso.

Questa pagina spiega come le campagne a throughput elevato differiscono dalle campagne attivate dall’API standard, dai requisiti di configurazione e da quando scegliere ogni modalità.

## Guardrail e limitazioni

* **Accesso** - Disponibile solo negli Stati Uniti per le organizzazioni con licenza del componente aggiuntivo Messaggistica transazionale ad alta velocità.

* **Canali**: attualmente disponibile solo per la posta elettronica.

* **Personalization**:

   * Tutte le personalizzazioni devono essere incluse nel payload API come **dati contestuali**. [Scopri come personalizzare il contenuto utilizzando i dati contestuali](../campaigns/api-triggered-campaign-action.md#contextual)
   * La personalizzazione basata su profili non è supportata. Se si utilizzano variabili di profilo, si verificheranno errori di convalida.

* **Configurazioni di canale personalizzate** - Le configurazioni di canale che utilizzano [personalizzazione basata su profilo](../email/surface-personalization.md) non possono essere utilizzate con campagne con throughput elevato. È possibile utilizzare solo superfici senza personalizzazione del profilo.

* **Endpoint API** - Le campagne con throughput elevato utilizzano un endpoint diverso dalle campagne attivate dall&#39;API standard. Per ulteriori dettagli, vedere [Eseguire una campagna attivata da API](../campaigns/trigger-campaigns.md#trigger).

* **Esclusività campagna** - Le campagne a velocità elevata non utilizzano i profili di Adobe. I messaggi vengono consegnati indipendentemente dal fatto che esista o meno un profilo.

  Inoltre, non è possibile utilizzare una campagna sia per i casi di utilizzo abilitati che per quelli non abilitati per il profilo. Se ti servono entrambe, crea due campagne separate e assicurati che il sistema chiamante decida quale attivare in base al contesto.

* **Set di dati per il feedback e il tracciamento** - I dati di feedback e tracciamento per le campagne con throughput elevato vengono memorizzati in set di dati dedicati che non sono abilitati per i profili. Di conseguenza, questi eventi non vengono uniti ai profili, anche se esiste un profilo corrispondente.

  I set di dati utilizzati sono:

   * **Set Di Dati Evento Feedback Messaggio Di AJO - Non Profilo**
   * **Set Di Dati Evento Esperienza Tracciamento E-Mail AJO - Non Profilo**

* **Allocazione throughput** - Il throughput fornito con il componente aggiuntivo High Throughput è riservato esclusivamente alle campagne con throughput elevato. Non esiste alcuna condivisione della velocità effettiva tra le campagne attivate dall’API a velocità standard e quella ad alta velocità.

## Scelta tra campagne standard e campagne a throughput elevato

Utilizza questa tabella per decidere quale tipo di campagna attivata da API è adatto al tuo caso d’uso:

| Funzionalità/Requisiti | Campagna attivata da API standard | Campagna a throughput elevato |
|------------------------|---------------------------------|---------------------------|
| **Disponibilità** | Incluso nell&#39;offerta base | Richiede il componente aggiuntivo High Throughput per la messaggistica transazionale. |
| **Velocità effettiva** | Fino a 500 transazioni al secondo | Fino a 5000 transazioni al secondo |
| **Canali** | Messaggi e-mail, SMS e push | E-mail |
| **Personalizzazione** | Profilo + contestuale nel payload API | Contestuale solo nel payload API |
| **Profilo e unione** | Esiste o viene creato con eventi uniti al profilo | Nessun profilo |
| **Volume messaggi** | Adesione standard e pacchetti di messaggi | Volumi di messaggi separati su più livelli |
| **Infrastruttura** | Standard | Avanzato |
| **Tempo di attività** | 99.9% | 99.99% |
| **API verifica stato** | Sì | Sì |

In altre parole:

* Scegli **le campagne API standard attivate** se:
   * Non hai un contratto per il throughput elevato.
   * Il throughput richiesto è &lt;500 TPS.
   * È necessaria la personalizzazione basata sui profili Adobe.
   * Desideri che i dati della campagna siano uniti ai profili per il targeting futuro.
   * Desideri utilizzare un canale diverso da E-mail.

* Scegli **Alta velocità** campagne se:
   * Hai bisogno di un throughput > 500 TPS.
   * Non è necessaria l’unione di profili.
   * Puoi trasmettere tutte le personalizzazioni nel payload API.
   * Desideri utilizzare il canale e-mail.

## Linee guida per l’installazione

Per configurare correttamente le campagne High Throughput, segui queste linee guida:

1. Crea un nuovo pool IP. [Scopri come creare pool IP](../configuration/ip-pools.md)
1. Crea una nuova configurazione di canale. [Scopri come impostare le configurazioni dei canali](../configuration/channel-surfaces.md)
1. Contatta l’Assistenza clienti Adobe per richiedere che la superficie attivata sia mappata sulla funzionalità High throughput (Alta velocità effettiva). Specifica la configurazione del canale e i dettagli del pool IP, insieme all’ID organizzazione.

>[!IMPORTANT]
>
>Le configurazioni del pool IP e del canale designate per i messaggi transazionali ad alta velocità devono essere utilizzate esclusivamente a tale scopo e non con la messaggistica transazionale standard utilizzando campagne o percorsi attivati dall’API.
