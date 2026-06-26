---
solution: Journey Optimizer
product: journey optimizer
title: 'Percorsi e campagne: scegliere l’approccio giusto'
description: Confronta Percorsi, campagne d’azione e campagne attivate da API per scegliere l’approccio giusto per le tue esigenze di marketing in Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
hide: true
keywords: percorso, campagna, confronto, scelta, decisione, flusso di lavoro, in tempo reale, batch, orchestrazione, in più passaggi, pianificato, attivato da API, basato su eventi
source-git-commit: ab31811861ccaab22fc787ce3c687204637fbd46
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 2%

---


# Percorsi e campagne: scegli l’approccio giusto {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**In questa pagina:** Confronta i percorsi con campagne attivate da azioni e API in modo da poter scegliere l&#39;approccio corretto per ogni caso d&#39;uso di marketing in Adobe Journey Optimizer. Per le campagne orchestrate, vedere [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre due modi principali per raggiungere e coinvolgere i clienti: **Percorsi** e **Campagne**. I percorsi sono progettati per l’orchestrazione in tempo reale in più passaggi guidata dal comportamento del cliente, mentre le campagne sono più adatte per le trasmissioni una tantum o pianificate a un pubblico definito o per le attivazioni dei canali in entrata al limite per la personalizzazione a bassa latenza.

>[!NOTE]
>
>**Le campagne orchestrate** presentano caratteristiche architetturali distinte (esecuzione batch lato hub, dati relazionali con più entità) che richiedono una guida dedicata. Non sono incluse nel confronto seguente per evitare un’eccessiva semplificazione. [Ulteriori informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

## Quale approccio utilizzare? {#decision-guide}

La risposta si riduce in genere a una domanda: *cosa deve accadere e per chi?*

Se hai bisogno che **ogni cliente si sposti secondo il proprio ritmo** — ricevendo messaggi in base a ciò che fa, aspettando, quindi reagendo all&#39;azione successiva — utilizza un **Percorso**. I percorsi tengono traccia di dove si trova ciascun profilo e di ciò che hanno fatto, rendendoli ideali per esperienze in più passaggi come sequenze di onboarding, flussi di abbandono del carrello o programmi fedeltà.

Se desideri **inviare un messaggio a un gruppo di persone secondo una pianificazione**, ovvero una newsletter, un annuncio di prodotto, una promozione stagionale, utilizza una **campagna d&#39;azione**. Tutti gli utenti del pubblico ricevono il messaggio contemporaneamente, senza bisogno di una logica per profilo. Le campagne di azione supportano anche le attivazioni dei canali in entrata (in-app, web, schede di contenuti, basate su codice) per la personalizzazione Edge a bassa latenza.

Se un **sistema esterno deve attivare immediatamente un messaggio**, ovvero una conferma dell&#39;ordine dalla piattaforma di e-commerce, un avviso di spedizione dal sistema logistico, una reimpostazione della password dall&#39;app, utilizzare una **campagna attivata da API** per un singolo messaggio on-demand o un **percorso di eventi unitario** se tale trigger deve avviare un flusso in più passaggi.

Se hai bisogno di un **flusso di lavoro batch complesso con segmentazione avanzata, dati con più entità o conteggi pre-invio esatti**, consulta [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

>[!TIP]
>
>**Non sei sicuro di dove iniziare?** La maggior parte dei team utilizza Percorsi per esperienze comportamentali basate su eventi e campagne di azione per comunicazioni pianificate. Questi due casi coprono la maggior parte dei casi d’uso.

## Come si confrontano {#quick-overview}

| Approccio | Ideale per | Stile di esecuzione |
|----------|----------|-----------------|
| **Percorsi** | Esperienze cliente in tempo reale con logica condizionale in più passaggi | Orchestrazione 1:1: ogni profilo al proprio ritmo |
| **Campagne con azioni** | Attivazioni pianificate o ricorrenti per tipi di pubblico | Esecuzione batch: pubblico elaborato insieme al momento dell’invio |
| **Campagne attivate da API** | Messaggi transazionali o basati su eventi da sistemi esterni | Esecuzione su richiesta — attivata da chiamata API con payload |

## Come funziona ogni approccio {#key-distinctions}

### Percorsi: 1:1 orchestrazione in tempo reale

Un Percorso è un’area di lavoro in cui ogni profilo percorre il proprio percorso al proprio ritmo. AJO tiene traccia di dove si trova ogni persona nel flusso e reagisce in tempo reale al suo comportamento, che si tratti di un’azione intrapresa, di un periodo di inattività o di una modifica nel suo profilo.

Le funzionalità chiave includono attività di attesa che creano intervalli personalizzati tra i passaggi, diramazioni condizionali che instradano i profili a percorsi diversi, limiti di frequenza per controllare la frequenza con cui un cliente riceve i messaggi e modalità di test per convalidare la logica prima della pubblicazione. I percorsi possono anche suddividere i profili in gruppi basati su percentuali per esperimenti A/B su percorsi diversi.

Un percorso di abbandono del carrello illustra chiaramente la differenza:

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Ogni cliente sperimenta una timeline diversa in base a ciò che fa effettivamente. [Ulteriori informazioni sui Percorsi](../building-journeys/journey.md)

### Campagne: consegna in batch o attivata

Una campagna esegue una singola azione, sia per tutti i tipi di pubblico contemporaneamente sia su richiesta quando viene chiamata da un sistema esterno. Non esistono aree di lavoro e stati per profilo: tutti i profili vengono elaborati in modo identico.

**Le campagne d&#39;azione** distribuiscono a un pubblico pianificato (una tantum o ricorrente) e supportano anche la consegna in entrata su più superfici: fino a 10 azioni di canale in entrata per campagna, con regole di targeting per creare varianti di messaggi in base all&#39;appartenenza al pubblico o agli attributi di profilo.

**Le campagne attivate da API** si attivano immediatamente quando un sistema esterno chiama l&#39;API, con la personalizzazione dei messaggi guidata dai dati di payload inviati in tale chiamata.

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

[Ulteriori informazioni sulle campagne](../campaigns/get-started-with-campaigns.md)

## Esempi di casi d’uso {#use-cases}

| Caso d’uso | Approccio consigliato | Perché |
|----------|---------------------|-----|
| Benvenuti nei nuovi clienti con l’onboarding in più passaggi | Percorsi | Ingresso in tempo reale, punti di contatto multipli, percorsi condizionali |
| Abbandono del carrello con sequenza di promemoria | Percorsi | Trigger in tempo reale, tempi di attesa, follow-up condizionale |
| Coinvolgere nuovamente gli utenti inattivi in base al comportamento | Percorsi | Attivato da qualificazione del pubblico, percorso personalizzato |
| Vendita flash attivata da un evento di business | Percorsi (evento di business) | Trigger in tempo reale che interessa più clienti |
| Newsletter mensile per gli abbonati | Campagne con azioni | Messaggio pianificato al pubblico |
| Annuncio promozionale a tutti i clienti | Campagne con azioni | Messaggio una tantum, consegna immediata |
| Conferma dell&#39;ordine o avviso di spedizione | Campagne attivate da API | Attivazione di un sistema esterno, consegna immediata di una sola ripresa |
| Flusso in più passaggi attivato da API | Percorsi (evento unitario) | Il sistema esterno invia l’evento tramite API; il percorso orchestra i passaggi di follow-up |
| Flusso di lavoro batch complesso con dati con più entità | Campagne orchestrate | Consulta [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md) |

## Disponibilità delle funzioni {#feature-availability}

### Canali

Tutti e tre gli approcci supportano l’intero set di canali in uscita di AJO: e-mail, push, SMS, LINE e WhatsApp. La tabella seguente mostra le differenze per i canali in entrata e digitali.

| Canale | Percorsi | Campagne con azioni | Campagne attivate da API |
|---------|:--------:|:----------------:|:-----------------------:|
| In-app | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Basato su codice | ✅ | ✅ | ❌ |
| Schede contenuto | ✅ | ✅ | ❌ |
| Direct mail | ✅ | ✅ | ❌ |

>[!NOTE]
>
>Per informazioni sulla disponibilità del canale per le campagne orchestrate, consulta [Canali in percorsi e campagne](../channels/gs-channels.md#channels).

### Funzionalità avanzate

| Funzionalità | Percorsi | Campagne con azioni | Campagne attivate da API |
|-----------|:--------:|:----------------:|:-----------------------:|
| Flussi di lavoro con più passaggi | ✅ | ❌ | ❌ |
| Trigger in tempo reale | ✅ | ❌ | ✅ |
| Attività di attesa | ✅ | ❌ | ❌ |
| Diramazione condizionale | ✅ | ❌ | ❌ |
| Esecuzione pianificata | ✅ | ✅ | ✅ |
| Attivazione API | ✅ (solo evento unitario) | ❌ | ✅ |
| Ottimizzazione del tempo di invio | ✅ | ❌ | ❌ |
| Test A/B | ✅ | ✅ | ❌ |
| Approvazione dei flussi di lavoro | ✅ | ✅ | ✅ |
| Dati di più entità | ❌ | ❌ | ❌ |
| Conteggi pre-invio esatti | ❌ | ❌ | ❌ |

>[!NOTE]
>
>Per i dettagli sulle funzionalità delle campagne orchestrate, inclusi esperimenti sui contenuti, attivazione di API batch e segmentazione di più entità, consulta [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

## Domande comuni {#common-questions}

+++ Posso combinare percorsi e campagne nella mia strategia di marketing?

Sì. Molte organizzazioni utilizzano tutti gli approcci per scenari diversi:

* **Percorsi** per coinvolgimento comportamentale e in tempo reale
* **Campagne di azione** per comunicazioni pianificate o attivazioni in entrata
* **Campagne attivate da API** per messaggi transazionali
* **Campagne orchestrate** per campagne batch complesse e a uso intensivo di dati. Vedere [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

Utilizza lo strumento giusto per ogni caso d’uso, anziché forzare un approccio per tutto.

+++

+++ Posso convertire una campagna in un percorso o viceversa?

No, devi ricreare l’esperienza nel formato appropriato. Tuttavia, puoi riutilizzare contenuti, tipi di pubblico e concetti logici.

+++

+++ Quale approccio è più semplice da creare?

Le campagne d’azione sono in genere le più semplici (un singolo punto di contatto inviato a un pubblico), seguite da campagne attivate dall’API e quindi da Percorsi, che richiedono un maggior numero di attività di progettazione a causa della logica in più passaggi.

+++

+++ Qual è la scala migliore per il pubblico di grandi dimensioni?

Tutti e tre possono scalare bene; la scelta giusta dipende dal tuo modello:

* **Le campagne Leggi pubblico** e **Leggi pubblico** sono ottimizzate per i Percorsi di pubblico in batch di grandi dimensioni.
* **Percorsi unitari (basati su eventi)** elaborano i profili singolarmente quando si verificano gli eventi, pertanto la scalabilità dipende dal volume e dalla velocità effettiva degli eventi.

Per segmentazioni complesse con set di dati di grandi dimensioni e dati con più entità, consulta [Campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ Posso utilizzare lo stesso pubblico in più percorsi e campagne?

Sì. I tipi di pubblico creati in [!DNL Adobe Experience Platform] possono essere utilizzati in Percorsi, campagne di azione e campagne orchestrate. Le campagne attivate da API sono basate sul payload e non utilizzano allo stesso modo i tipi di pubblico predefiniti.

+++

## Passaggi successivi {#next-steps}

Tutto pronto per iniziare a creare? Esplora la documentazione dettagliata dell’approccio scelto:

* **[Introduzione ai Percorsi](../building-journeys/journey.md)** - Tipi di Percorso, finestra di progettazione e flusso di lavoro
* **[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)** - Campagne attivate da azioni e API
* **[Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)** - Flussi di lavoro di aree di lavoro batch con dati con più entità (indicazioni separate)

>[!MORELIKETHIS]
>
>* [Confronto tipi Percorso](../building-journeys/journey.md#journey-types-comparison)
>* [Confronto dei tipi di campagna](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Domande frequenti sui Percorsi](../building-journeys/journey-faq.md)
>* [Domande frequenti sulle campagne orchestrate](../orchestrated/orchestrated-campaigns-faq.md)

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** Scegli tra Percorsi, campagne di azione e campagne attivate da API, a seconda che sia necessaria l&#39;orchestrazione in tempo reale 1:1, la consegna batch pianificata o in entrata o l&#39;esecuzione attivata da API su richiesta.

**Intenti:**
* Comprendere le differenze chiave tra Percorsi, campagne d’azione e campagne attivate da API
* Seleziona l’approccio corretto per un dato caso di utilizzo di marketing utilizzando la guida decisionale e le tabelle di confronto
* Comprendere quando le campagne d’azione supportano le attivazioni dei canali in entrata rispetto alle trasmissioni in uscita
* Scopri quando passare alle campagne orchestrate (composizione ad hoc, dati federati, più entità)
* Combinare efficacemente più approcci in una strategia di marketing

**Glossario:**
* **Percorso**: un flusso di orchestrazione in più passaggi e in tempo reale in cui ogni profilo procede al proprio ritmo in base al comportamento e agli eventi. *(specifico per prodotto)*
* **Campagna di azione**: una campagna che consegna attivazioni pianificate o ricorrenti al pubblico — trasmissioni in uscita o attivazioni di canali in entrata al server Edge per la personalizzazione a bassa latenza. *(specifico per prodotto)*
* **Campagna attivata da API**: campagna avviata da un sistema esterno tramite chiamata API per la distribuzione di un singolo messaggio on-demand con personalizzazione basata sul payload. *(specifico per prodotto)*
* **Campagna orchestrata**: campagna batch lato hub che supporta dati relazionali con più entità, composizione di tipi di pubblico ad hoc e origini dati federate. Non inclusa nelle tabelle di confronto in questa pagina. *(specifico per prodotto)*
* **percorso di eventi unitario**: percorso attivato da una singola azione di profilo in tempo reale; da utilizzare quando è necessaria l&#39;orchestrazione in più passaggi dopo un evento inviato dall&#39;API. *(specifico per prodotto)*
* **Attivazione canale in entrata**: consegna di esperienze personalizzate al server Edge (esperienza basata su codice, in-app, scheda contenuto, web) per il rendering a bassa latenza, supportata nelle campagne Azione. *(specifico per prodotto)*

**Guardrail:**
* Fino a 10 azioni del canale in entrata per campagna di azione (limite rigido): si applica solo ai canali in entrata: esperienza basata su codice, in-app, scheda di contenuto, web
* Le campagne orchestrate sono escluse dalle tabelle di confronto in questa pagina per evitare un’eccessiva semplificazione; per informazioni sull’architettura, consulta la documentazione dedicata alle campagne orchestrate

**Terminologia:**
* Nome canonico: Campagne d’azione — Varianti: &quot;Campagne pianificate&quot;, &quot;Campagne broadcast&quot;
* Nome canonico: campagne attivate da API — varianti: &quot;campagne transazionali&quot;, &quot;campagne guidate da eventi&quot;
* Non confondere: &quot;Campagne di azione&quot; (consegna pianificata/in entrata al pubblico) ≠ &quot;Campagne attivate da API&quot; (su richiesta, basate sul payload, senza pubblico predefinito) ≠ &quot;Campagne orchestrate&quot; (batch lato hub con dati relazionali)
* Non confondere: &quot;percorso di eventi unitario&quot; (attivato dall’azione in tempo reale di un profilo) ≠ &quot;percorso di eventi aziendali&quot; (attivato da un evento non di profilo che interessa più persone tramite un passaggio Read Audience interno)
* Sinonimi: &quot;attivazione canale in entrata&quot; = &quot;azione canale in entrata&quot; (utilizzato in modo intercambiabile in questa pagina per le esperienze consegnate Edge nelle campagne Azione)

**Domande frequenti:**
* **Q: quando dovrei usare un Percorso invece di una campagna Azione?** utilizzo di Percorsi in cui i clienti devono spostarsi secondo il proprio ritmo con logica condizionale in tempo reale su più punti di contatto; utilizzo di campagne di azione per la consegna pianificata o in entrata a un pubblico predefinito.
* **D: le campagne di azione possono essere distribuite ai canali in entrata?** Sì. Le campagne di azione supportano l’attivazione del canale in entrata (esperienza basata su codice, in-app, scheda di contenuto, web) al limite per la personalizzazione a bassa latenza, con un massimo di 10 azioni in entrata per campagna e regole di targeting per le varianti di messaggio.
* **D: cosa distingue le campagne orchestrate dalle campagne di azione?** esecuzione in batch lato hub di campagne orchestrate con dati relazionali su più entità, conteggi pre-invio esatti, composizione di tipi di pubblico ad hoc e supporto di dati federati; le campagne di azione sono consegne senza stato a esecuzione singola ai tipi di pubblico di Experience Platform.
* **Q: quando dovrei usare una campagna attivata da API rispetto a un percorso di eventi unitario?** campagna attivata da API quando un percorso esterno deve attivare immediatamente un singolo messaggio con i dati del payload; utilizza un sistema di eventi unitario quando è necessaria l’orchestrazione in più passaggi dopo l’evento inviato da API.
* **D: posso combinare Percorsi e campagne nella stessa strategia di marketing?** Sì. Utilizza Percorsi per il coinvolgimento comportamentale in tempo reale, campagne di azione per trasmissioni pianificate o attivazioni in entrata, campagne attivate da API per messaggi transazionali e campagne orchestrate per flussi di lavoro batch complessi.

+++
<!-- ai-accordion-version: 1 | source-hash: 873097f5 -->
