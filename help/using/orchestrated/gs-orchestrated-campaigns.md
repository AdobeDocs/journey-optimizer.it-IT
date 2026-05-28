---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne orchestrate
description: Scopri come iniziare a utilizzare le campagne orchestrate
short-description: Scopri le funzioni chiave e i casi d’uso delle campagne orchestrate.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ePbw3PWwBuZl5A3bdBzM0gb4koCEH09WUX0P-g8z3VM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 910
ht-degree: 91%

---

# Introduzione alle campagne orchestrate {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orchestrazione campagna</b><br/>Dividere, combinare, arricchire e manipolare set di dati relazionali per definire il pubblico<br/><br/> <b>Sfruttare dati con entità multiple</b><br/>Scopri in che modo le campagne orchestrate possono sfruttare i set di dati relazionali per arricchire i dati per la segmentazione e la personalizzazione<br/><br/><b>Segmentazione ad hoc e conteggi esatti</b><br/>Crea un segmento dettagliato con conteggi esatti<br/><br/><b>Canali disponibili</b><br/>E-mail, SMS, notifiche push, direct mail"

L’orchestrazione delle campagne in [!DNL Adobe Journey Optimizer] potenzia campagne sofisticate e avviate dal brand su tutti i canali, sia di **marketing** che **transazionali**. Le campagne di marketing ti consentono di promuovere il coinvolgimento, i ricavi e la fidelizzazione clienti su larga scala. I messaggi transazionali non richiedono il consenso e sono adatti per comunicazioni sensibili al tempo come interruzioni, emergenze o cancellazioni.

>[!IMPORTANT]
>
>Per accedere all’orchestrazione della campagna, la licenza deve includere il pacchetto **Journey Optimizer - Campagne e Percorsi** o **Journey Optimizer - Campagne**. Contatta il tuo rappresentante Adobe per confermare la licenza e aggiornare, se necessario.

Anche se il marketing cross-channel è essenziale, le campagne orchestrate lo rendono semplice. Grazie a un’interfaccia visiva basata su un trascinamento, puoi progettare e automatizzare flussi di lavoro di marketing complessi, dalla segmentazione alla consegna dei messaggi, su più canali. Tutto avviene in un ambiente intuitivo, progettato per velocità, controllo ed efficienza.

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [Scopri le campagne orchestrate nel video](#video-oc)

## Funzionalità di base

L’orchestrazione delle campagne si basa su quattro pilastri chiave:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Tipi di pubblico on-demand" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>Tipi di pubblico on-demand</b><br/>Esegui una query istantanea tra set di dati per creare segmenti di pubblico utilizzando qualsiasi combinazione di tipi di dati e dimensioni.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentazione e invio di più entità" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentazione e invio di più entità</b><br/>Oltre alle campagne basate su persone, utilizza entità quali cataloghi di prodotti, posizioni di store o dati del servizio per eseguire il targeting con precisione.<br/><br/>
È supportato l’invio multilivello, in cui viene inviato un messaggio per profilo e per entità secondaria associata. Tali entità secondarie possono includere indirizzi di contatto, prenotazioni, abbonamenti, contratti o altri dati collegati. Ad esempio, questo consente di inviare le campagne a tutti gli indirizzi noti di un profilo o a ogni prenotazione associata a quel profilo.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilità e precisione pre-invio" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Visibilità e precisione pre-invio</b><br/>Ottieni conteggi di segmentazione esatti e l’ambito completo della campagna prima del lancio, garantendo precisione e affidabilità.</td></tr>
<tr style="border: 0;">
<td><img alt="Flussi di lavoro della campagna con più passaggi" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Flussi di lavoro della campagna con più passaggi</b><br/>Progetta campagne con più passaggi, dai messaggi giornalieri alle campagne complesse come le promozioni stagionali o i principali lanci di prodotti.</td></tr>
</table>

>[!NOTE]
>
>Per ulteriori informazioni sui canali supportati, consulta la tabella in questa sezione: [Canali nei percorsi e nelle campagne](../channels/gs-channels.md#channels).
>
>I canali disponibili variano in base al modello di licenza e ai componenti aggiuntivi.

## Percorsi e campagne orchestrate

Anche se la visualizzazione delle campagne orchestrate è simile ai percorsi, è adatta a diversi scopi e casi d’uso:

* **Percorsi**: da area di lavoro individuale in cui ogni profilo percorre i diversi passaggi al proprio ritmo. Lo stato di ciascun cliente viene mantenuto nel relativo contesto per attivare azioni in tempo reale.

* **Campagne orchestrate**: a differenza dei percorsi, le campagne orchestrate funzionano utilizzando un’area di lavoro batch per il calcolo dei segmenti. Tutti i profili vengono elaborati contemporaneamente.

Entrambe le aree di lavoro sono ottimizzate per i rispettivi casi d’uso: l’area di lavoro del percorso pubblica percorsi che tendono a durare per un periodo di tempo più lungo, mentre l’area di lavoro della campagna è progettata per esecuzioni iterative e incrementali di una campagna batch.

## Che cosa c’è all’interno di una campagna orchestrata? {#gs-ms-campaign-inside}

L’area di lavoro della campagna orchestrata è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![immagine che mostra un’area di lavoro della campagna orchestrata](assets/canvas-example.png)

Ogni campagna orchestrata contiene:

* **Attività**: un’attività è un’attività da eseguire. Le [varie attività](activities/about-activities.md) nell’area di lavoro sono rappresentate tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.

  In un’area di lavoro della campagna orchestrata, una determinata attività può produrre più attività, in particolare in presenza di un ciclo o di azioni ricorrenti.

* **Transizioni**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.

* **Tabelle di lavoro**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni campagna orchestrata utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della campagna orchestrata.

Una tipica campagna orchestrata di livello base segue questo pattern: **Crea pubblico → Fork → canale A + canale B**.

Questo approccio consente di indirizzare allo stesso pubblico due rami paralleli di una singola esecuzione della campagna, ad esempio un ramo che utilizza un’e-mail di marketing e un altro che utilizza un’e-mail transazionale. Ogni ramo è indipendente e può utilizzare una configurazione dei canali, un contenuto di messaggio o una categoria diversi.

➡️ [Scopri come utilizzare l’attività Fork](activities/fork.md)

➡️ [Comprendere messaggi di marketing e transazionali](activities/channels.md#marketing-vs-transactional)

## Video introduttivo {#video-oc}

Scopri i concetti chiave e le funzionalità disponibili con le campagne orchestrate.


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## Argomenti di approfondimento

Ora che sai che cosa sono le campagne orchestrate, è necessario approfondire le sezioni della documentazione per iniziare a utilizzare questa funzione.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Accedere e gestire le campagne" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Passaggi di configurazione</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Lead" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>Creare una campagna orchestrata</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Non frequente" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Utilizzare le attività</strong></a>
</div>
<p></td>
</tr></table>

## Risorse aggiuntive

* **[Creare la prima regola](build-query.md)**: padroneggia il generatore di regole per creare query mirate e segmentare i tipi di pubblico con precisione utilizzando i dati relazionali.
* **[Creare schemi relazionali](gs-schemas.md)**: scopri come impostare e configurare schemi relazionali per sfruttare i dati con più entità nelle campagne.
* **[Reporting per campagne orchestrate](reporting-campaigns.md)**: tieni traccia e analizza le prestazioni delle campagne con metriche di reporting e insight dettagliati.
* **[Avviare e monitorare le campagne](start-monitor-campaigns.md)**: scopri le best practice per avviare le campagne e monitorarne l’esecuzione in tempo reale.
* **[Guardrail e limitazioni](guardrails.md)**: esamina guardrail, limitazioni e best practice importanti per garantire prestazioni ottimali della campagna.
* **[Domande frequenti](orchestrated-campaigns-faq.md)**: trova le risposte alle domande comuni sulle funzioni, funzionalità e casi d’uso delle campagne orchestrate.
* **[Tutorial per le campagne orchestrate](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/create-campaigns/orchestrated-campaigns/introduction-to-orchestrated-campaigns){target="_blank"}**: esplora i tutorial video dettagliati che descrivono le funzioni e le best practice.
* **[Coinvolgi i clienti esplorando l&#39;attività](engage-customers-uc.md)** - Rivolgiti ai profili che hanno navigato ma non hanno acquistato, utilizzando una campagna orchestrata in più passaggi.
* **[Notifica agli utenti la disponibilità del prodotto](product-availability-uc.md)** - Avvisa i clienti quando un prodotto per cui hanno mostrato interesse è di nuovo disponibile.
* **[Invia aggiornamenti elemento elenco dei desideri](wishlist-uc.md)** - Attiva messaggi personalizzati quando gli elementi della lista dei desideri vengono messi in vendita o diventano disponibili.
