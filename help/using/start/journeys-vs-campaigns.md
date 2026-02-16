---
solution: Journey Optimizer
product: journey optimizer
title: 'Percorsi e campagne: scegliere l’approccio giusto'
description: Confronta Percorsi, campagne d’azione, campagne attivate da API e campagne orchestrate per scegliere l’approccio giusto per le tue esigenze di marketing in Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: percorso, campagna, orchestrato, confronto, scelta, decisione, flusso di lavoro, in tempo reale, batch, orchestrazione, con più passaggi, pianificato, attivato da API, basato su eventi
hide: true
hidefromtoc: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
source-git-commit: 4cf2b850561ef99dc8dc8300c41eeedd0cecfe32
workflow-type: tm+mt
source-wordcount: '1602'
ht-degree: 3%

---

# Percorsi e campagne: scegli l’approccio giusto {#journeys-vs-campaigns}

[!DNL Adobe Journey Optimizer] offre quattro modi principali per raggiungere e coinvolgere i clienti: **Percorsi**, **Campagne azione**, **Campagne attivate da API** e **Campagne orchestrate**. Scegliere quella giusta dipende dalla necessità di orchestrazione in tempo reale 1:1, trasmissioni pianificate, messaggi basati su eventi o flussi di lavoro batch complessi.

Questa guida ti aiuta a scegliere in base allo stile di esecuzione, alle esigenze di dati e al caso d’uso, con un confronto rapido, una struttura decisionale ed esempi concreti.

## Panoramica sul confronto rapido {#quick-overview}

| Approccio | Ideale per | Stile di esecuzione |
|----------|----------|-----------------|
| **Percorsi** | Esperienze cliente in tempo reale con logica condizionale in più passaggi | Orchestrazione 1:1: ogni profilo al proprio ritmo |
| **Campagne Azione** | Trasmissioni pianificate o ricorrenti al pubblico | Esecuzione batch: pubblico elaborato insieme al momento dell’invio |
| **Campagne attivate da API** | Messaggi transazionali o basati su eventi da sistemi esterni | Esecuzione su richiesta - Attivata da chiamata API con payload |
| **Campagne orchestrate** | Flussi di lavoro batch complessi con segmentazione multi-entità | Area di lavoro batch: tutti i profili elaborati insieme |

>[!TIP]
>
>**Regola empirica rapida:** È necessario che ogni cliente si sposti secondo il proprio ritmo con la logica in tempo reale? Usa **Percorsi**. Inviare un messaggio a un pubblico in base a una pianificazione? Utilizza **Campagne Azione**. Attivazione da un sistema esterno tramite API? Utilizza **Campagne attivate da API**. Hai bisogno di dati con più entità, conteggi esatti o un’area di lavoro batch? Utilizza **Campagne orchestrate**.

## Confronto dettagliato {#detailed-comparison}

Utilizza questa tabella completa per comprendere le differenze principali:

| Funzione | Percorsi | Campagne di azione | Campagne attivate da API | Campagne orchestrate |
|---------|----------|------------------|------------------------|----------------------|
| **Scopo principale** | Orchestrazione in più passaggi 1:1 con contesto cliente in tempo reale | Consegna di messaggi una tantum o ricorrente al pubblico | Messaggi transazionali o basati su eventi avviati da sistemi esterni | Campagne batch con più passaggi e flussi di lavoro di segmentazione complessi |
| **Tipo quadro** | 1:1 area di lavoro: ogni profilo viaggia secondo il proprio ritmo | Nessuna area di lavoro - esecuzione di una singola azione | Nessuna area di lavoro - esecuzione di una singola azione | Area di lavoro batch: tutti i profili elaborati insieme |
| **Flusso di esecuzione** | Azioni sequenziali, il profilo mantiene lo stato in tutto il percorso | Esecuzione simultanea all’intero pubblico | Esecuzione immediata per chiamata API | Flusso di lavoro batch con più passaggi con attività e transizioni |
| **Meccanismo di ingresso** | Eventi, pubblico, qualifiche, eventi aziendali | Attivazione e pianificazione manuali | Chiamata API da un sistema esterno | Esecuzione pianificata del flusso di lavoro batch |
| **Modello dati** | Profilo in tempo reale + dati evento | Dati profilo dai tipi di pubblico di Experience Platform | Dati payload API con ricerca profilo opzionale | Dati relazionali su più entità (profili, prodotti, negozi, prenotazioni) |
| **Segmentazione** | Pubblico predefinito + condizioni in tempo reale | Tipi di pubblico predefiniti di Experience Platform | Targeting basato sul payload (nessun pubblico pianificato) | Tipi di pubblico su richiesta generati nell’area di lavoro con conteggi esatti |
| **Elaborazione profilo** | Individuale, in tempo reale (quando si verificano gli eventi) | Batch, tutto in una volta | Per chiamata API, basata sul payload | Batch, tutti con supporto per più entità |
| **Personalizzazione** | Dati contestuali in tempo reale + attributi del profilo | Attributi del profilo | Dati payload + attributi di profilo facoltativi | Dati di più entità per il targeting di precisione |
| **Complessità** | Più passaggi con diramazioni, tempi di attesa, condizioni | Azione singola o flusso di lavoro semplice | Singola azione con mappatura payload | Flussi di lavoro in batch con più passaggi con segmentazione, arricchimento e divisioni |
| **Ottimo per** | Percorsi del ciclo di vita del cliente, onboarding, abbandono del carrello | Campagne promozionali, newsletter, annunci | Conferme d&#39;ordine, avvisi di spedizione, reimpostazioni password | Campagne stagionali complesse, promozioni in più passaggi, lanci di prodotti |
| **Intervallo** | Continua, sempre attiva dopo la pubblicazione | Date di inizio/fine pianificate | On-demand, basato su eventi tramite API | Esecuzione batch secondo pianificazione |
| **Gestione stato** | Gestisce lo stato del cliente per le azioni in tempo reale | Esecuzione senza stato | Esecuzione senza stato per chiamata | Elaborazione in batch con tabelle di lavoro |
| **Usa quando** | Sono necessari più punti di contatto con logica decisionale in tempo reale | Messaggio semplice a un pubblico in un momento specifico | Il sistema esterno deve attivare immediatamente un messaggio | Necessità di segmentazione complessa, dati di più entità o conteggi pre-invio esatti |
| **Funzionalità univoche** | Reazioni in tempo reale, attività di attesa, velocità basata su profili | Pianificazione, targeting di pubblico, controllo delle tariffe | Mappatura del payload API, attivazione da sistema a sistema | Set di dati relazionali, segmentazione di più entità, conteggi esatti, invio a più livelli |

## Guida alle decisioni {#decision-guide}

Segui questo albero decisionale per scegliere l’approccio corretto. Molti marchi utilizzano più di un tipo; scegli il più adatto per ogni caso d’uso.

### Passaggio 1: qual è il requisito di esecuzione?

**Risposte individuali in tempo reale al comportamento del cliente?**
→ **Usa Percorsi**
* I profili devono spostarsi secondo il proprio ritmo
* Logica condizionale basata sul comportamento
* Il contesto in tempo reale è fondamentale

**Recapito semplice di messaggi a un pubblico in un orario pianificato?**
→ **Utilizzare Campagne Azione**
* Tutti i profili ricevono il messaggio simultaneamente
* Invii pianificati o ricorrenti
* Non è necessaria alcuna logica complessa in più passaggi

**Messaggio immediato attivato da un sistema esterno?**
→ **Utilizzare campagne attivate da API**
* Attivazione on-demand tramite chiamata API
* Personalizzazione basata sul payload
* Non è necessaria alcuna logica complessa in più passaggi

**Flusso di lavoro batch complesso con segmentazione avanzata?**
→ **Utilizza campagne orchestrate**
* Sono necessari dati su più entità (prodotti, negozi, prenotazioni)
* Richiedi conteggi pre-invio esatti
* Elaborazione batch in più fasi con divisioni e arricchimento

### Passaggio 2: convalidare la scelta

| Le tue esigenze | Approccio consigliato | Perché |
|-----------|---------------------|-----|
| Benvenuti nei nuovi clienti con l’onboarding in più passaggi | Percorsi | Ingresso in tempo reale, punti di contatto multipli, percorsi condizionali |
| Invia newsletter mensile agli abbonati | Campagne di azione | Semplice messaggio pianificato al pubblico |
| Abbandono del carrello con sequenza di promemoria | Percorsi | Trigger in tempo reale, tempi di attesa, follow-up condizionale |
| Annuncio promozionale a tutti i clienti | Campagne di azione | Messaggio una tantum, consegna immediata |
| Coinvolgere nuovamente gli utenti inattivi in base al comportamento | Percorsi | Attivato da qualificazione del pubblico, percorso personalizzato |
| Vendita flash attivata da un evento aziendale | Percorsi (evento di business) | Trigger in tempo reale che interessa più clienti |
| Promozione stagionale con integrazione del catalogo dei prodotti | Campagne orchestrate | Dati di più entità, segmentazione complessa, conteggi esatti |
| Messaggio transazionale attivato da API | Campagne attivate da API | Attivazione del sistema esterno, consegna immediata |
| Invio multilivello per prenotazione | Campagne orchestrate | Relazioni tra più entità, un messaggio per prenotazione |

## Spiegazione delle principali distinzioni {#key-distinctions}

### Percorsi: 1:1 orchestrazione in tempo reale

**Che cosa lo rende univoco:**
* Ogni profilo gestisce il singolo stato e contesto
* I profili entrano e progrediscono al proprio ritmo
* Processo decisionale in tempo reale basato su comportamenti ed eventi
* Le attività di attesa creano un intervallo personalizzato
* La diramazione condizionale crea percorsi univoci per profilo

**Flusso di esempio:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Ogni cliente sperimenta la propria timeline di percorso in base alle proprie azioni.

[Ulteriori informazioni sui Percorsi](../building-journeys/journey.md)

### Campagne: consegna semplice in batch o attivata

**Che cosa lo rende univoco:**
* Tutti i profili elaborati in modo identico e simultaneo
* Esecuzione senza stato - nessun contesto mantenuto
* Pianificazione semplice o attivazione API
* Ideale per le comunicazioni broadcast

**Flusso di esempio:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Tutti ricevono lo stesso messaggio in contemporanea.

**Tipi:**
* **Campagne azione**: consegna pianificata per il pubblico (una tantum o ricorrente)
* **Campagne attivate da API**: consegna su richiesta attivata da una chiamata API con dati di payload

[Ulteriori informazioni sulle campagne](../campaigns/get-started-with-campaigns.md)

### Campagne orchestrate: flussi di lavoro dell’area di lavoro in batch

**Che cosa lo rende univoco:**
* Area di lavoro batch con attività e transizioni (simile all’area di lavoro percorso ma orientata ai batch)
* Supporto di dati relazionali per più entità (profili + prodotti + negozi + prenotazioni)
* Creazione di un pubblico on-demand all’interno dell’area di lavoro
* Conteggi esatti prima dell’invio (visibilità pre-invio)
* Invio multilivello (un messaggio per entità, ad esempio per prenotazione)
* Tutti i profili elaborati insieme in batch

**Flusso di esempio:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Combina la complessità del flusso di lavoro con l’esecuzione in batch delle campagne.

[Ulteriori informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

## Esempi di casi d’uso {#use-cases}

### Casi di utilizzo del percorso

* **Ripristino dell&#39;abbandono del carrello**: attivato dall&#39;evento di aggiunta al carrello, attendi l&#39;estrazione, invia promemoria se non viene effettuato alcun acquisto
* **Onboarding del cliente**: serie di benvenuto in più passaggi con contenuti personalizzati basati sui dati del profilo
* **Aggiornamento livello fedeltà**: attivato quando il cliente raggiunge un nuovo livello, invia congratulazioni e benefici
* **Campagne di compleanno**: ingresso basato sulla data di nascita, offerte personalizzate
* **Nuovo coinvolgimento**: attivato dalla qualifica del pubblico (inattività), dalla diffusione progressiva

### Casi di utilizzo delle campagne (attivati da Azione e API)

**Campagne azioni:**
* **Newsletter mensili**: consegna batch pianificata al segmento sottoscrittore
* **Annunci promozionali**: offerte sensibili al tempo per i tipi di pubblico di destinazione
* **Lanci di prodotti**: annuncio coordinato a tutti i clienti
* **Saluti stagionali**: messaggi di vacanza in date specifiche

**Campagne attivate da API:**
* **Conferme ordine**: attivato dal sistema di e-commerce dopo l&#39;acquisto
* **Notifiche di spedizione**: attivato dal sistema logistico
* **Avvisi account**: attivato dal sistema di rilevamento delle frodi
* **Reimpostazione password**: attivata dall&#39;azione dell&#39;utente nell&#39;applicazione

### Casi d’uso della campagna orchestrata

* **Promozione stagionale con integrazione catalogo**: esegui query sul catalogo dei prodotti, identifica i clienti idonei, segmenta per preferenze, invia consigli di prodotti personalizzati
* **Campagne specifiche per lo store**: rivolgiti a clienti vicini a posizioni specifiche dello store con dati di inventario dello store
* **Comunicazioni con più prenotazioni**: invia un messaggio per ogni prenotazione (prenotazioni di hotel e voli)
* **Orchestrazione dei segmenti complessa**: crea i tipi di pubblico in modo dettagliato con l&#39;arricchimento da più origini dati
* **Convalida pre-invio**: ottieni conteggi esatti dei destinatari prima di avviare campagne principali

## Disponibilità delle funzioni {#feature-availability}

### Canali

| Canale | Percorsi | Campagne di azione | Campagne attivate da API | Campagne orchestrate |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ |
| In-app | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Basato su codice | ✅ | ✅ | ❌ | ❌ |
| Schede contenuto | ✅ | ✅ | ❌ | ❌ |
| Direct mail | ✅ | ✅ | ❌ | ✅ |

### Funzionalità avanzate

| Funzionalità | Percorsi | Campagne di azione | Campagne attivate da API | Campagne orchestrate |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Flussi di lavoro con più passaggi | ✅ | ❌ | ❌ | ✅ |
| Trigger in tempo reale | ✅ | ❌ | ✅ | ❌ |
| Attività di attesa | ✅ | ❌ | ❌ | ✅ |
| Diramazione condizionale | ✅ | ❌ | ❌ | ✅ |
| Esecuzione pianificata | ✅ | ✅ | ✅ | ✅ |
| Attivazione API | ❌ | ❌ | ✅ | ❌ |
| Dati di più entità | ❌ | ❌ | ❌ | ✅ |
| Conteggi pre-invio esatti | ❌ | ❌ | ❌ | ✅ |
| Segmentazione su richiesta | ❌ | ❌ | ❌ | ✅ |
| Ottimizzazione del tempo di invio | ✅ | ✅ | ✅ | ✅ |
| Test A/B | ✅ | ✅ | ❌ | ❌ |
| Approvazione dei flussi di lavoro | ✅ | ✅ | ✅ | ❌ |

## Domande comuni {#common-questions}

+++ Posso combinare percorsi e campagne nella mia strategia di marketing?

Sì.  Molte organizzazioni utilizzano tutti e quattro gli approcci per scenari diversi:

* **Percorsi** per coinvolgimento comportamentale e in tempo reale
* **Campagne azioni** per le comunicazioni broadcast pianificate
* **Campagne attivate da API** per messaggi transazionali
* **Campagne orchestrate** per campagne batch complesse e a uso intensivo di dati

Utilizza lo strumento giusto per ogni caso d’uso, anziché forzare un approccio per tutto.

+++

+++ Posso convertire una campagna in un percorso o viceversa?

No, devi ricreare l’esperienza nel formato appropriato. Tuttavia, puoi riutilizzare contenuti, tipi di pubblico e concetti logici.

+++

+++ Quale approccio è più facile da creare?

Le campagne d’azione sono in genere le più semplici (messaggio singolo al pubblico), seguite da campagne attivate da API, Percorsi (più complessi con logica a più passaggi) e campagne orchestrate (più complessi a causa del flusso di lavoro dell’area di lavoro e delle funzionalità con più entità).

+++

+++ Qual è la scala migliore per il pubblico di grandi dimensioni?

Tutti e quattro possono essere scalati bene; la scelta giusta dipende dal tuo modello:

* percorsi **Le campagne Leggi pubblico** e **Campagne azione** sono ottimizzate per tipi di pubblico in batch di grandi dimensioni (un messaggio o flusso a più profili alla volta).
* **Campagne orchestrate** eccellono nella segmentazione complessa con set di dati di grandi dimensioni e dati di più entità.
* **Percorsi unitari (basati su eventi)** elaborano i profili singolarmente quando si verificano gli eventi, pertanto la scalabilità dipende dal volume e dalla velocità effettiva degli eventi.

+++

+++ Posso utilizzare lo stesso pubblico in più percorsi e campagne?

Sì.  I tipi di pubblico creati in [!DNL Adobe Experience Platform] possono essere utilizzati in Percorsi, campagne azioni e campagne orchestrate (in cui la logica del pubblico può essere generata anche su richiesta nell&#39;area di lavoro). Le campagne attivate da API sono basate sul payload e non utilizzano allo stesso modo i tipi di pubblico predefiniti.

+++

## Passaggi successivi {#next-steps}

Tutto pronto per iniziare a creare? Esplora la documentazione dettagliata dell’approccio scelto:

* **[Introduzione ai Percorsi](../building-journeys/journey.md)** - Tipi di Percorso, finestra di progettazione e flusso di lavoro
* **[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)** - Campagne attivate da azioni e API
* **[Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)** - Flussi di lavoro dell&#39;area di lavoro batch

>[!MORELIKETHIS]
>
>* [Confronto tipi Percorso](../building-journeys/journey.md#journey-types-comparison)
>* [Confronto dei tipi di campagna](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Domande frequenti sui Percorsi](../building-journeys/journey-faq.md)
>* [Domande frequenti sulle campagne orchestrate](../orchestrated/orchestrated-campaigns-faq.md)
>* [Best practice](best-practices.md) - Casi d&#39;uso in tempo reale e ridimensionamento con guardrail
