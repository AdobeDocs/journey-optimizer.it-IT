---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 2%

---
Il file non esiste nell’archivio della pipeline, è un file di documentazione fornito come contesto. Scrivo il markdown completo aggiornato direttamente come indicato (restituisce solo il file, senza spiegazioni).

&#x200B;---

soluzione: Journey Optimizer
product: percorsi optimizer
title: Attivare la modalità High Throughput per le campagne attivate dall’API
description: Scopri come attivare la modalità Alta velocità effettiva per le campagne attivate dall&#39;API.
funzione: Campagne, API
topic: Gestione dei contenuti
ruolo: Sviluppatore
livello: esperienza
parole chiave: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: 2b3e87dc-097a-4d05-873c-f421d11338c3
TQID: https://experienceleague.adobe.com/SwmK1epuhZUf4EWnaLRHTBH-eE1hEV02Z8nqXGtMb6U
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label: Journey Optimizer
feature_v2:
- id: d556b755-390a-43f0-be32-a08cf6236126
internal-label: Configuration
- id: a653cc2e-bc85-4353-a306-399e5b247978
internal-label: campagne Journey Optimizer
subfeature_v2:
- id: f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label: campagne attivate dall’API
- id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label: Gestione delle campagne
role_v2:
- id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Developer
topic_v2:
- id: e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label: Personalization
---
# Modalità di velocità effettiva elevata per campagne attivate da API {#high-throughput}

>[!BEGINSHADEBOX]

**In questa pagina:** attiva la modalità High Throughput per le campagne attivate dall&#39;API in modo da poter inviare messaggi transazionali in tempo reale su grande scala fino a 5000 transazioni al secondo (e-mail) o fino a 1500 transazioni al secondo (push) senza affidarsi ai profili.

>[!ENDSHADEBOX]

La modalità High Throughput è progettata per le organizzazioni che necessitano di **messaggi transazionali su larga scala e in tempo reale**. A differenza delle normali campagne attivate da API, le campagne a throughput elevato operano in modo indipendente dai profili di Adobe e richiedono un modello di configurazione diverso.

Questa pagina spiega come le campagne a throughput elevato differiscono dalle campagne attivate dall’API standard, dai requisiti di configurazione e da quando scegliere ogni modalità.

## Guardrail e limitazioni

&#x200B;* **Accesso** - Disponibile solo negli Stati Uniti per le organizzazioni con licenza del componente aggiuntivo Messaggistica transazionale ad alta velocità.

&#x200B;* **Canali**: disponibile per le notifiche e-mail e push.

&#x200B;* **Velocità effettiva**:

   &#x200B;* **E-mail** - Fino a 5000 transazioni al secondo.
   &#x200B;* **Push** - Fino a 1500 transazioni al secondo. Sono disponibili i seguenti livelli di throughput su più livelli: 500 TPS (base), 1000 TPS e 1500 TPS. I livelli superiori richiedono il diritto al componente aggiuntivo appropriato.

&#x200B;* **Personalization**:

   &#x200B;* Tutte le personalizzazioni devono essere incluse nel payload API come **dati contestuali**. [Scopri come personalizzare il contenuto utilizzando i dati contestuali](../campaigns/api-triggered-campaign-content.md#contextual)
   &#x200B;* La personalizzazione basata su profili non è supportata. Se si utilizzano variabili di profilo, si verificheranno errori di convalida.

&#x200B;* **Configurazioni di canale personalizzate** - Le configurazioni di canale che utilizzano [personalizzazione basata su profilo](../email/surface-personalization.md) non possono essere utilizzate con campagne con throughput elevato. È possibile utilizzare solo superfici senza personalizzazione del profilo.

&#x200B;* **Endpoint API** - Le campagne con throughput elevato utilizzano un endpoint diverso dalle campagne attivate dall&#39;API standard. Per ulteriori dettagli, vedere [Eseguire una campagna attivata da API](../campaigns/trigger-campaigns.md#trigger).

&#x200B;* **Esclusività campagna** - Le campagne a velocità elevata non utilizzano i profili di Adobe. I messaggi vengono consegnati indipendentemente dal fatto che esista o meno un profilo.

  Inoltre, non è possibile utilizzare una campagna sia per i casi di utilizzo abilitati che per quelli non abilitati per il profilo. Se ti servono entrambe, crea due campagne separate e assicurati che il sistema chiamante decida quale attivare in base al contesto.

&#x200B;* **Set di dati per il feedback e il tracciamento** - I dati di feedback e tracciamento per le campagne con throughput elevato vengono memorizzati in set di dati dedicati che non sono abilitati per i profili. Di conseguenza, questi eventi non vengono uniti ai profili, anche se esiste un profilo corrispondente.

  I set di dati utilizzati sono:

   &#x200B;* **Set Di Dati Evento Feedback Messaggio Di AJO - Non Profilo**
   &#x200B;* **Set Di Dati Evento Esperienza Tracciamento E-Mail AJO - Non Profilo**

&#x200B;* **Allocazione throughput** - Il throughput fornito con il componente aggiuntivo High Throughput è riservato esclusivamente alle campagne con throughput elevato. Non esiste alcuna condivisione della velocità effettiva tra le campagne attivate dall’API a velocità standard e quella ad alta velocità.

## Scelta tra campagne standard e campagne a throughput elevato

Utilizza questa tabella per decidere quale tipo di campagna attivata da API è adatto al tuo caso d’uso:

| Funzionalità/Requisiti | Campagna attivata da API standard | Campagna a throughput elevato |
|------------------------|---------------------------------|---------------------------|
| **Disponibilità** | Incluso nell&#39;offerta base | Richiede il componente aggiuntivo High Throughput per la messaggistica transazionale. |
| **Velocità effettiva** | Fino a 500 transazioni al secondo | Fino a 5.000 TPS (e-mail); fino a 1.500 TPS (push) |
| **Canali** | Messaggi e-mail, SMS e push | E-mail, push |
| **Personalizzazione** | Profilo + contestuale nel payload API | Contestuale solo nel payload API |
| **Profilo e unione** | Esiste o viene creato con eventi uniti al profilo | Nessun profilo |
| **Volume messaggi** | Adesione standard e pacchetti di messaggi | Volumi di messaggi separati su più livelli |
| **Infrastruttura** | Standard | Avanzato |
| **Tempo di attività** | 99,9% | 99,99% |
| **API verifica stato** | Sì | Sì |

In altre parole:

&#x200B;* Scegli **le campagne API standard attivate** se:
   &#x200B;* Non si dispone di un contratto per il throughput elevato.
   &#x200B;* Il throughput richiesto è ≤500 TPS.
   &#x200B;* È necessaria la personalizzazione basata sui profili Adobe.
   &#x200B;* Desideri che i dati della campagna siano uniti ai profili per il targeting futuro.
   &#x200B;* Hai bisogno di messaggi SMS.

&#x200B;* Scegli **Alta velocità** campagne se:
   &#x200B;* Hai bisogno di un throughput > 500 TPS.
   &#x200B;* Non è necessario unire i profili.
   &#x200B;* Puoi trasmettere tutte le personalizzazioni nel payload API.
   &#x200B;* Desideri utilizzare il canale e-mail o push.

## Linee guida per l’installazione

Per configurare correttamente le campagne High Throughput, segui queste linee guida:

1. **Solo per throughput elevato e-mail** - Crea un nuovo pool IP. [Scopri come creare pool IP](../configuration/ip-pools.md)
1. Crea una nuova configurazione di canale. [Scopri come impostare le configurazioni dei canali](../configuration/channel-surfaces.md)
1. Contatta l’Assistenza clienti Adobe per richiedere che la superficie attivata sia mappata sulla funzionalità High throughput (Alta velocità effettiva). Specifica la configurazione del canale e i dettagli del pool IP (per e-mail) insieme all’ID organizzazione.

>[!IMPORTANT]
>
>Le configurazioni di canale designate per i messaggi transazionali ad alta velocità devono essere utilizzate esclusivamente a tale scopo e non con la messaggistica transazionale standard utilizzando campagne o percorsi attivati dall’API. Per l’elevato throughput delle e-mail, anche il pool IP designato a questo scopo deve essere utilizzato esclusivamente per l’invio di messaggi ad alto throughput.