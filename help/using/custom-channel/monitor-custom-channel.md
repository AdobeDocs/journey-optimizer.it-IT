---
title: Gestire e monitorare i canali personalizzati
description: Scopri come gestire il ciclo di vita dei canali personalizzati e delle configurazioni dei canali e monitorare le prestazioni di consegna tramite la generazione di rapporti di Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 1%

---


# Monitorare i canali personalizzati {#monitor-custom-channel}

Una volta creato e attivato un canale personalizzato, puoi [gestirne il ciclo di vita](create-custom-channel.md#access-channel-builder) e monitorare le prestazioni di consegna tramite l&#39;interfaccia [!DNL Journey Optimizer].

## Utilizzo dei rapporti sulle campagne e sul percorso {#reporting}

[!DNL Journey Optimizer] fornisce rapporti predefiniti per i canali personalizzati.

Le metriche seguenti sono disponibili per i canali personalizzati nei rapporti live (24h) e globali (CJA).<!--TBC and add or replace with CJA link when available-->

| Metrica | Descrizione |
|--------|-------------|
| **Consegne tentate** | Numero totale di messaggi inviati all’endpoint esterno. |
| **Consegne riuscite** | Messaggi per i quali l’endpoint ha restituito una risposta HTTP 2xx. |
| **Profili target** | Numero di profili univoci raggiunto. |
| **Clic** | Numero di clic del collegamento tracciati nel payload. Richiede un sottodominio delegato per i canali personalizzati. |
| **Errori / Errori** | Numero di tentativi di consegna non riusciti, con suddivisione per motivo dell’errore. |

Ulteriori informazioni sui [report live](../reports/live-report.md) e sui [report globali](../reports/report-gs-cja.md). Per informazioni dettagliate sulle funzionalità di reporting, consulta [questa documentazione](../reports/report-cja-manage.md).

<!--
### Journey reports {#journey-reports}

To view delivery data for a custom channel action in a journey:

1. Open the journey from the **[!UICONTROL Journeys]** list.
1. Click **[!UICONTROL View report]** in the top-right area.
   * **[!UICONTROL Live report]** – Data for the last 24 hours.
   * **[!UICONTROL All time]** – Full lifetime data via Customer Journey Analytics (CJA).

### Campaign reports {#campaign-reports}

To view delivery data for a custom channel campaign:

1. Open the campaign from the **[!UICONTROL Campaigns]** list.
1. Click **[!UICONTROL Reports]** in the top-right area.

The campaign report includes execution count, successful deliveries, errors, and click data (if link tracking is enabled).
-->

## Monitorare le prestazioni delle consegne {#monitoring}

Oltre ai rapporti sulle campagne e sul percorso, [!DNL Journey Optimizer] fornisce un dashboard dedicato e personalizzato per il monitoraggio dei canali. Accedi a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Generatore canali]** > **[!UICONTROL Monitoraggio canali personalizzati]**.

![Dashboard di monitoraggio del canale personalizzato](assets/custom_channel_monitoring_dashboard.png){width="100%"}

Questa dashboard consente di monitorare l&#39;affidabilità e le prestazioni delle chiamate API [!DNL Journey Optimizer] effettuate agli endpoint esterni durante la distribuzione dei messaggi di canale personalizzati. Utilizzala per individuare rapidamente i problemi di integrazione, la latenza e i limiti di limitazione.

Il dashboard **[!UICONTROL Monitoraggio dei canali personalizzati]** funziona come altri report di tutti i tempi in [!DNL Journey Optimizer]. Puoi selezionare un intervallo di tempo, filtrare per canale o endpoint ed eseguire un drill-down per visualizzare le campagne e i percorsi che si basano su ciascun canale personalizzato. [Ulteriori informazioni](../reports/report-cja-manage.md)

### Metriche di canale personalizzate {#monitoring-kpis}

La sezione **[!UICONTROL Metriche del canale personalizzate]** fornisce una visualizzazione consolidata dello stato operativo e dell&#39;affidabilità delle chiamate al canale personalizzate.

![Metriche di canale personalizzate](assets/custom_channel_metrics.png){width="100%"}

+++ Ulteriori informazioni sulle metriche del canale personalizzate

* **[!UICONTROL Chiamate riuscite]**: numero totale di chiamate HTTP che hanno restituito una risposta valida senza errori.

* **[!UICONTROL Errori 4xx/5xx]**: numero di chiamate non riuscite a causa di errori lato client (4xx) o lato server (5xx), evidenziando problemi di configurazione o errori endpoint.

* **[!UICONTROL Chiamate di timeout]**: numero di chiamate non riuscite perché hanno superato il tempo di risposta massimo. Questo aiuta a far emergere problemi di latenza o prestazioni con gli endpoint esterni.

* **[!UICONTROL Errori pre-chiamata]**: numero di invii di canali personalizzati non riusciti prima che la chiamata HTTP fosse stata effettuata all&#39;endpoint esterno. Questi errori si verificano nel livello di infrastruttura di [!DNL Journey Optimizer], non nel sistema esterno. Sono disponibili tre categorie:

  | Categoria | Descrizione |
  |----------|-------------|
  | **Errori di autenticazione** (`AUTH_*`) | [!DNL Journey Optimizer]: impossibile ottenere o aggiornare il token OAuth o le credenziali necessarie per chiamare l&#39;endpoint. Verifica che le credenziali API collegate alla configurazione del canale siano valide e non siano scadute. |
  | **Errori di generazione richieste** (`REQUEST_GENERATION_ERROR`) | [!DNL Journey Optimizer] non è in grado di creare una richiesta HTTP valida, ad esempio perché non è stato possibile risolvere un modello URL o manca un campo di personalizzazione richiesto. |
  | **Errori di analisi HTTP** (`HTTP_PARSE_ERROR`) | [!DNL Journey Optimizer] ha ricevuto una risposta dall&#39;endpoint, ma non è stato possibile analizzarla in una struttura utilizzabile. |

  >[!TIP]
  >
  >Gli errori pre-chiamata indicano un problema sul lato [!DNL Journey Optimizer] o nella configurazione del canale, invece di un problema con l&#39;endpoint esterno. Inizia la risoluzione dei problemi esaminando le credenziali API e i campi payload richiesti.

* **[!UICONTROL Latenza media]**: tempo medio di risposta end-to-end (in millisecondi) per tutte le chiamate HTTP, incluse le chiamate riuscite, gli errori e i timeout.

<!--
* **[!UICONTROL Capped calls]**: Number of calls that were blocked due to capping limits, ensuring downstream systems are not overloaded.

* **[!UICONTROL Average RPS]**: Number of requests per second processed by the custom channel over the selected time range.

* **[!UICONTROL Average successful latency]**: Average end-to-end response time (in milliseconds) for successful calls only, excluding failed requests and timeouts.

* **[!UICONTROL Average queue time]**: Average time (in milliseconds) calls spent waiting in the execution queue before being sent. This only applies to throttled endpoints, where [!DNL Journey Optimizer] queues calls when the throughput limit is reached.
-->

+++

### Risultati dei canali personalizzati nel tempo {#outcomes-overtime}

![Risultati di canale personalizzati nel tempo](assets/custom_channel_metrics.png){width="100%"}

Il grafico **[!UICONTROL Risultati dei canali personalizzati nel tempo]** mostra la tendenza dell&#39;indicatore KPI per le chiamate HTTP nel periodo di tempo selezionato. La granularità della serie temporale dipende dall’intervallo temporale selezionato:

* Per un rapporto di 7 giorni, ogni punto dati mostra i KPI per un giorno.
* Per un intervallo di tempo di 1 giorno, il grafico mostra i KPI all’ora.
* Per un intervallo di tempo di 1 ora, il grafico mostra i KPI al minuto.

### Latenza nel tempo {#latency-overtime}

![Latenza del canale personalizzata nel tempo](assets/custom_channel_latency.png){width="100%"}

Il grafico **[!UICONTROL Latenza nel tempo]** visualizza la tendenza delle metriche di latenza nel periodo di tempo selezionato. Questa vista della serie temporale consente di tenere traccia dei modelli di prestazioni, identificare i periodi di latenza di picco e monitorare l’impatto delle ottimizzazioni o dei cambiamenti del sistema nel tempo.

### Analisi stratificata risultati canale personalizzato {#outcome-breakdown}

![Analisi stratificata risultati canale personalizzato](assets/custom_channel_latency.png){width="100%"}

La tabella **[!UICONTROL Analisi stratificata risultati canale personalizzato]** fornisce una suddivisione gerarchica delle metriche delle chiamate HTTP, dalle metriche globali per endpoint al livello principale alle metriche per canale personalizzato che utilizzano tale endpoint, fino alle campagne e ai percorsi che si basano su di essi al livello inferiore.

### Suddivisione latenza {#latency-breakdown}

La tabella **[!UICONTROL Analisi stratificata latenza]** fornisce una suddivisione dettagliata delle metriche di latenza per i canali personalizzati. Questa vista consente di identificare gli endpoint o i canali specifici che riscontrano problemi di prestazioni, consentendo di individuare e risolvere efficacemente i colli di bottiglia di latenza.

### Insight Builder {#insight-builder}

Utilizza **[!UICONTROL Insight Builder]** per creare visualizzazioni e dashboard personalizzati in base alle metriche di canale personalizzate. Questo strumento consente di combinare più KPI, applicare filtri e creare viste personalizzate in linea con le tue esigenze di monitoraggio e reporting. [Ulteriori informazioni](../reports/report-cja-manage.md#insight-builder)

## Risoluzione dei problemi {#troubleshooting}

Se riscontri problemi con il tuo canale personalizzato, la tabella seguente elenca i sintomi comuni, le possibili cause e le risoluzioni consigliate.

| Sintomo | Possibile causa | Risoluzione |
|---------|----------------|------------|
| **HTTP 401 / 403 errori** | Errore di autenticazione: credenziali scadute o non corrette. | Aggiorna le credenziali in **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Credenziali API]**. |
| **Errori HTTP 429** | L&#39;endpoint esterno sta limitando le richieste da [!DNL Journey Optimizer]. | Esamina i limiti di velocità dell’endpoint. Riduci l’impostazione di limitazione nella configurazione dei criteri di Channel Builder. |
| **Errori HTTP 5xx** | Il sistema esterno è inattivo o restituiscono errori del server. | Controlla il dashboard di integrità del sistema esterno. Configura i percorsi di errore nell’attività di azione del percorso per gestire in modo corretto gli errori transitori. |
| **Token di personalizzazione non risolti** | L’espressione fa riferimento a un attributo non presente nel profilo. | Verifica che il percorso dell’attributo XDM sia corretto. Aggiungere un valore predefinito di fallback: `{{profile.person.name.firstName \| default("Valued Customer")}}`. |
| **Errore di convalida campo obbligatorio** | Un campo payload richiesto non ha alcun valore al momento dell’authoring. | Assicurati che tutti i campi obbligatori siano compilati nell’editor di contenuti. In alternativa, rimuovi il vincolo richiesto nel Channel Builder se il campo è veramente facoltativo. |

<!--
## Related resources {#related}

* [Get started with custom channels](get-started-custom-channel.md)
* [Configure a custom channel](custom-channel-configuration.md)
* [Global report overview](../reports/report-gs-cja.md)
* [Journey live report](../reports/live-report.md
-->