---
solution: Journey Optimizer
product: journey optimizer
title: 'Percorsi e campagne: scegliere l’approccio giusto'
description: Confronta Percorsi, campagne d’azione e campagne attivate da API per scegliere l’approccio giusto per le tue esigenze di marketing in Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: percorso, campagna, confronto, scelta, decisione, flusso di lavoro, in tempo reale, batch, orchestrazione, in più passaggi, pianificato, attivato da API, basato su eventi
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
TQID: https://experienceleague.adobe.com/RWLVSULVO0idnCs5OVQR1yVvNv1G0JwP3y-3sNXQg50
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: addf009e-030a-4310-8534-776a3e62ed48id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: d23d6b78ef905135732c1df76bc263dafbc17d8f
workflow-type: tm+mt
source-wordcount: 2545
ht-degree: 2%

---

# Percorsi e campagne: scegli l’approccio giusto {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**In questa pagina:** Confronta i percorsi con campagne attivate da azioni e API in modo da poter scegliere l&#39;approccio corretto per ogni caso d&#39;uso di marketing in Adobe Journey Optimizer. Per le campagne orchestrate, vedere [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre due modi principali per raggiungere e coinvolgere i clienti: **Percorsi** e **Campagne**. I percorsi sono progettati per l’orchestrazione in tempo reale in più passaggi guidata dal comportamento del cliente, mentre le campagne sono più adatte per le trasmissioni una tantum o pianificate a un pubblico definito o per le attivazioni dei canali in entrata al limite per la personalizzazione a bassa latenza. Dopo aver deciso una campagna, puoi scegliere il tipo di campagna più adatto al tuo caso d’uso.

Questa guida ti aiuta a scegliere tra Percorsi, campagne d’azione e campagne attivate da API in base allo stile di esecuzione, alle esigenze di dati e al caso d’uso, con un confronto rapido, una struttura decisionale ed esempi concreti.

>[!NOTE]
>
>**Le campagne orchestrate** presentano caratteristiche architetturali distinte (esecuzione batch lato hub, dati relazionali con più entità) che richiedono una guida dedicata. Non sono incluse nelle tabelle di confronto riportate di seguito per evitare un’eccessiva semplificazione. [Ulteriori informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

## Panoramica sul confronto rapido {#quick-overview}

| Approccio | Ideale per | Stile di esecuzione |
|----------|----------|-----------------|
| **Percorsi** | Esperienze cliente in tempo reale con logica condizionale in più passaggi | Orchestrazione 1:1: ogni profilo al proprio ritmo |
| **Campagne con azioni** | Attivazioni pianificate o ricorrenti per tipi di pubblico | Esecuzione batch: pubblico elaborato insieme al momento dell’invio |
| **Campagne attivate da API** | Messaggi transazionali o basati su eventi da sistemi esterni | Esecuzione su richiesta - Attivata da chiamata API con payload |

>[!TIP]
>
>**Regola empirica rapida:** È necessario che ogni cliente si sposti secondo il proprio ritmo con la logica in tempo reale? Usa **Percorsi**. Inviare un messaggio a un pubblico in base a una pianificazione? Utilizza **Campagne di azione**. Attivare un singolo messaggio da un sistema esterno tramite API? Utilizza **campagne attivate da API** — o un **percorso di eventi unitario** se hai bisogno di orchestrazione in più passaggi dopo l&#39;evento inviato da API. Hai bisogno di una personalizzazione in entrata basata su Edge? Utilizza **Campagne di azione**.

## Confronto dettagliato {#detailed-comparison}

Utilizza questa tabella completa per comprendere le differenze principali:

| Funzione | Percorsi | Campagne con azioni | Campagne attivate da API |
|---------|----------|------------------|------------------------|
| **Scopo principale** | Orchestrazione in più passaggi 1:1 con contesto cliente in tempo reale | Consegna di messaggi una tantum o ricorrente al pubblico | Messaggi transazionali o basati su eventi avviati da sistemi esterni |
| **Tipo quadro** | 1:1 area di lavoro: ogni profilo viaggia secondo il proprio ritmo | Nessuna area di lavoro - esecuzione di una singola azione | Nessuna area di lavoro - esecuzione di una singola azione |
| **Flusso di esecuzione** | Azioni sequenziali, il profilo mantiene lo stato in tutto il percorso | Esecuzione simultanea all’intero pubblico | Esecuzione immediata per chiamata API |
| **Meccanismo di ingresso** | Eventi, pubblico, qualifiche, eventi aziendali | Attivazione e pianificazione manuali | Chiamata API da un sistema esterno |
| **Modello dati** | Profilo in tempo reale + dati evento | Dati profilo dai tipi di pubblico di Experience Platform | Dati payload API con ricerca profilo opzionale |
| **Segmentazione** | Pubblico predefinito + condizioni in tempo reale | Tipi di pubblico predefiniti di Experience Platform | Targeting basato sul payload (nessun pubblico pianificato) |
| **Elaborazione profilo** | Individuale, in tempo reale (quando si verificano gli eventi) | Batch, tutto in una volta | Per chiamata API, basata sul payload |
| **Personalizzazione** | Dati contestuali in tempo reale + attributi del profilo | Attributi del profilo | Dati payload + attributi di profilo facoltativi |
| **Complessità** | Più passaggi con diramazioni, tempi di attesa, condizioni | Azione singola o flusso di lavoro semplice | Singola azione con mappatura payload |
| **Ottimo per** | Percorsi del ciclo di vita del cliente, onboarding, abbandono del carrello | Campagne promozionali, newsletter, annunci | Conferme d&#39;ordine, avvisi di spedizione, reimpostazioni password |
| **Intervallo** | Continua, sempre attiva dopo la pubblicazione | Date di inizio/fine pianificate | On-demand, basato su eventi tramite API |
| **Gestione stato** | Gestisce lo stato del cliente per le azioni in tempo reale | Esecuzione senza stato | Esecuzione senza stato per chiamata |
| **Usa quando** | Sono necessari più punti di contatto con logica decisionale in tempo reale | Messaggio semplice a un pubblico in un momento specifico | Il sistema esterno deve attivare immediatamente un messaggio |
| **Funzionalità univoche** | Reazioni in tempo reale, attività di attesa, velocità basata su profili | Pianificazione, targeting di pubblico, controllo delle tariffe | Mappatura del payload API, attivazione da sistema a sistema |

## Guida alle decisioni {#decision-guide}

Segui questo albero decisionale per scegliere l’approccio corretto. Molti marchi utilizzano più di un tipo; scegli il più adatto per ogni caso d’uso.

### Passaggio 1: qual è il requisito di esecuzione?

**Risposte individuali in tempo reale al comportamento del cliente?→** Usa Percorsi **
* I profili devono spostarsi secondo il proprio ritmo
* Logica condizionale basata sul comportamento
* Il contesto in tempo reale è fondamentale

**Recapito semplice di messaggi a un pubblico in un orario pianificato?→** Utilizzare le campagne Azione **
* Tutti i profili ricevono il messaggio simultaneamente
* Invii pianificati o ricorrenti
* Non è necessaria alcuna logica complessa in più passaggi

**Messaggio immediato attivato da un sistema esterno?→** Utilizzare campagne attivate da API **(messaggio singolo)** o un percorso di eventi unitario **(orchestrazione in più passaggi)
* Attivato su richiesta tramite chiamata API: le campagne inviano un messaggio; i percorsi unitari acquisiscono l&#39;evento tramite [acquisizione Experience Platform](../event/additional-steps-to-send-events-to-journey.md) ed eseguono un flusso di percorso completo
* Personalizzazione basata sul payload
* Scegli le campagne quando non è necessaria una logica in più passaggi

**Flusso di lavoro batch complesso con segmentazione avanzata, dati di più entità o conteggi esatti pre-invio?→** Utilizzare le campagne orchestrate **. Per istruzioni dettagliate, vedere [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

>[!NOTE]
>
>* **Composizione ad hoc del pubblico**: le campagne orchestrate ti consentono di definire il pubblico di destinazione direttamente nell&#39;area di lavoro della campagna utilizzando il generatore di regole integrato, senza dover prima creare e valutare un pubblico Adobe Experience Platform. [Scopri come creare la tua prima regola](../orchestrated/build-query.md)
>* **Dati federati**: utilizza Federated Audience Composition per eseguire query nel data warehouse aziendale e creare o arricchire tipi di pubblico senza importare dati sensibili in Adobe Experience Platform. [Informazioni su Federated Audience Composition](../audience/federated-audience-composition.md)

### Passaggio 2: convalidare la scelta

| Le tue esigenze | Approccio consigliato | Perché |
|-----------|---------------------|-----|
| Benvenuti nei nuovi clienti con l’onboarding in più passaggi | Percorsi | Ingresso in tempo reale, punti di contatto multipli, percorsi condizionali |
| Invia newsletter mensile agli abbonati | Campagne con azioni | Semplice messaggio pianificato al pubblico |
| Abbandono del carrello con sequenza di promemoria | Percorsi | Trigger in tempo reale, tempi di attesa, follow-up condizionale |
| Annuncio promozionale a tutti i clienti | Campagne con azioni | Messaggio una tantum, consegna immediata |
| Coinvolgere nuovamente gli utenti inattivi in base al comportamento | Percorsi | Attivato da qualificazione del pubblico, percorso personalizzato |
| Vendita flash attivata da un evento aziendale | Percorsi (evento di business) | Trigger in tempo reale che interessa più clienti |
| Messaggio transazionale attivato da API (invio singolo) | Campagne attivate da API | Attivazione di un sistema esterno, consegna immediata di una sola ripresa |
| Flusso in più passaggi attivato da API | Percorsi (evento unitario) | Il sistema esterno invia un evento unitario tramite API; il percorso orchestra i passaggi di follow-up |
| Flusso di lavoro batch complesso con dati con più entità | Campagne orchestrate | Consulta [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md) |

## Spiegazione delle principali distinzioni {#key-distinctions}

### Percorsi: 1:1 orchestrazione in tempo reale

**Che cosa lo rende univoco:**
* Ogni profilo gestisce il singolo stato e contesto
* I profili entrano e progrediscono al proprio ritmo
* Processo decisionale in tempo reale basato su comportamenti ed eventi
* Le attività di attesa creano un intervallo personalizzato
* La diramazione condizionale crea percorsi univoci per profilo
* Ascolto attivo integrato: il mancato intervento per un periodo definito può anche attivare il passaggio successivo, non solo eventi espliciti. [Informazioni sulle attività di attesa](../building-journeys/wait-activity.md)
* Limitazione di frequenza: controlla la frequenza con cui un cliente può immettere o ricevere messaggi da un percorso. [Informazioni sui limiti di percorso](../conflict-prioritization/journey-capping.md)
* Suddivisione del pubblico per percentuale: divide i profili in gruppi casuali basati su percentuali per eseguire esperimenti A/B su percorsi di percorso. [Informazioni sulla suddivisione percentuale](../building-journeys/condition-activity.md)
* Modalità di test: convalida la logica di percorso e la consegna dei messaggi con i profili di test prima della pubblicazione live. [Informazioni sulla modalità di test](../building-journeys/testing-the-journey.md)

**Flusso di esempio:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Ogni cliente sperimenta la propria timeline di percorso in base alle proprie azioni.

[Ulteriori informazioni sui Percorsi](../building-journeys/journey.md) | [Tipi di Percorso: scegliere quello giusto](../building-journeys/journey-types-selection.md)

### Campagne: consegna semplice in batch o attivata

**Che cosa lo rende univoco:**
* Tutti i profili elaborati in modo identico e simultaneo
* Esecuzione senza stato - nessun contesto mantenuto
* Pianificazione semplice o attivazione API
* Ideale per le comunicazioni broadcast
* Consegna in entrata su più superfici: in una singola campagna puoi aggiungere fino a 10 azioni del canale in entrata (esperienza basata su codice, in-app, scheda di contenuto, web) utilizzando le regole di targeting per creare varianti di messaggio in base all’iscrizione al pubblico o agli attributi del profilo. [Ulteriori informazioni](../campaigns/campaign-action.md#multi-action)

**Flusso di esempio:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Tutti ricevono lo stesso messaggio in contemporanea.

**Tipi:**
* **Campagne di azione**: consegna pianificata per il pubblico (una tantum o ricorrente)
* **Campagne attivate da API**: consegna su richiesta attivata da una chiamata API con dati di payload

[Ulteriori informazioni sulle campagne](../campaigns/get-started-with-campaigns.md)

## Esempi di casi d’uso {#use-cases}

### Casi di utilizzo del percorso

* **Ripristino dell&#39;abbandono del carrello**: attivato dall&#39;evento di aggiunta al carrello, attendi l&#39;estrazione, invia promemoria se non viene effettuato alcun acquisto
* **Onboarding del cliente**: serie di benvenuto in più passaggi con contenuti personalizzati basati sui dati del profilo
* **Aggiornamento livello fedeltà**: attivato quando il cliente raggiunge un nuovo livello, invia congratulazioni e benefici
* **Campagne di compleanno**: ingresso basato sulla data di nascita, offerte personalizzate
* **Nuovo coinvolgimento**: attivato dalla qualifica del pubblico (inattività), dalla diffusione progressiva

### Casi di utilizzo delle campagne (attivati da azioni e API)

**Campagne di azione:**
* **Newsletter mensili**: consegna batch pianificata al segmento sottoscrittore
* **Annunci promozionali**: offerte sensibili al tempo per i tipi di pubblico di destinazione
* **Lanci di prodotti**: annuncio coordinato a tutti i clienti
* **Saluti stagionali**: messaggi di vacanza in date specifiche

**Campagne attivate da API:**
* **Conferme ordine**: attivato dal sistema di e-commerce dopo l&#39;acquisto
* **Notifiche di spedizione**: attivato dal sistema logistico
* **Avvisi account**: attivato dal sistema di rilevamento delle frodi
* **Reimpostazione password**: attivata dall&#39;azione dell&#39;utente nell&#39;applicazione

## Disponibilità delle funzioni {#feature-availability}

### Canali

| Canale | Percorsi | Campagne con azioni | Campagne attivate da API |
|---------|:--------:|:----------------:|:-----------------------:|
| E-mail | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ |
| In-app | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Basato su codice | ✅ | ✅ | ❌ |
| Schede contenuto | ✅ | ✅ | ❌ |
| Direct mail | ✅ | ✅ | ❌ |
| LINE | ✅ | ✅ | ✅ |
| WhatsApp | ✅ | ✅ | ✅ |

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
| Attivazione API | ✅ (solo evento unitario — evento inviato tramite API) | ❌ | ✅ |
| Dati di più entità | ❌ | ❌ | ❌ |
| Conteggi pre-invio esatti | ❌ | ❌ | ❌ |
| Segmentazione su richiesta | ❌ | ❌ | ❌ |
| Ottimizzazione del tempo di invio | ✅ | ❌ | ❌ |
| Test A/B | ✅ | ✅ | ❌ |
| Approvazione dei flussi di lavoro | ✅ | ✅ | ✅ |

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

+++ Quale approccio è più facile da creare?

Le campagne di azione sono in genere le più semplici (punto di contatto singolo o coinvolgimento distribuito a un pubblico), seguite da campagne attivate da API e quindi Percorsi (più complessi con logica in più passaggi).

+++

+++ Qual è la scala migliore per il pubblico di grandi dimensioni?

Tutti e tre possono scalare bene; la scelta giusta dipende dal tuo modello:

* **Percorsi di tipi di pubblico di lettura** e **Le campagne d&#39;azione** sono ottimizzate per i tipi di pubblico batch di grandi dimensioni (un messaggio o flusso verso più profili alla volta).
* **Percorsi unitari (basati su eventi)** elaborano i profili singolarmente quando si verificano gli eventi, pertanto la scalabilità dipende dal volume e dalla velocità effettiva degli eventi.

Per segmentazioni complesse con set di dati di grandi dimensioni e dati con più entità, consulta [Campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ Posso utilizzare lo stesso pubblico in più percorsi e campagne?

Sì. I tipi di pubblico creati in [!DNL Adobe Experience Platform] possono essere utilizzati in Percorsi, campagne di azione e campagne orchestrate. Le campagne attivate da API sono basate sul payload e non utilizzano allo stesso modo i tipi di pubblico predefiniti.

+++

## Passaggi successivi {#next-steps}

Tutto pronto per iniziare a creare? Esplora la documentazione dettagliata dell’approccio scelto:

* **[Introduzione ai Percorsi](../building-journeys/journey.md)** - Tipi di Percorso, finestra di progettazione e flusso di lavoro
* **[Tipi di Percorso: scegli quello giusto](../building-journeys/journey-types-selection.md)** - Evento unitario, lettura pubblico, qualificazione del pubblico ed evento di business
* **[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)** - Campagne attivate da azioni e API
* **[Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)** - Flussi di lavoro di aree di lavoro batch con dati con più entità (indicazioni separate)

>[!MORELIKETHIS]
>
>* [Tipi di Percorso: scegli quello giusto](../building-journeys/journey-types-selection.md)
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
