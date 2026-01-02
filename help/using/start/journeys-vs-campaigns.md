---
solution: Journey Optimizer
product: journey optimizer
title: 'Percorsi e campagne: scegliere l’approccio giusto'
description: Confronta percorsi, campagne e campagne orchestrate per scegliere l’approccio giusto per le tue esigenze di marketing in Adobe Journey Optimizer
feature: Journeys, Campaigns, Get Started, Overview
role: User
level: Beginner
keywords: percorso, campagna, orchestrato, confronto, scelta, decisione, flusso di lavoro, in tempo reale, batch, orchestrazione, con più passaggi, pianificato, attivato da API, basato su eventi
hide: true
hidefromtoc: true
source-git-commit: 5c842eb5d744380b462c6830af0838aa3329e9f7
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 3%

---


# Percorsi e campagne: scegli l’approccio giusto {#journeys-vs-campaigns}

Adobe Journey Optimizer offre tre potenti approcci per raggiungere e coinvolgere i clienti. Per creare esperienze di marketing efficaci, è fondamentale capire quando utilizzarle.

Questa guida ti aiuta a scegliere tra **Percorsi**, **Campagne** (attivate da azioni e API) e **Campagne orchestrate** in base alle tue esigenze di marketing specifiche.

## Panoramica sul confronto rapido {#quick-overview}

| Approccio | Ideale per | Stile di esecuzione |
|----------|----------|-----------------|
| **Percorsi** | Esperienze cliente in tempo reale con logica condizionale in più passaggi | Orchestrazione 1:1: ogni profilo al proprio ritmo |
| **Campagne (Azione e API)** | Consegna di messaggi semplice, pianificata o attivata | Batch o attivati da API - tutti i profili simultaneamente |
| **Campagne orchestrate** | Flussi di lavoro batch complessi con segmentazione multi-entità | Area di lavoro batch: tutti i profili elaborati insieme |

## Confronto dettagliato {#detailed-comparison}

Utilizza questa tabella completa per comprendere le differenze principali:

| Funzione | Percorsi | Campagne (attivate da azioni e API) | Campagne orchestrate |
|---------|----------|-----------------------------------|----------------------|
| **Scopo principale** | Orchestrazione in più passaggi 1:1 con contesto cliente in tempo reale | Consegna di messaggi una tantum o ricorrente al pubblico | Campagne batch con più passaggi e flussi di lavoro di segmentazione complessi |
| **Tipo quadro** | 1:1 area di lavoro: ogni profilo viaggia secondo il proprio ritmo | Nessuna area di lavoro - esecuzione di una singola azione | Area di lavoro batch: tutti i profili elaborati insieme |
| **Flusso di esecuzione** | Azioni sequenziali, il profilo mantiene lo stato in tutto il percorso | Esecuzione simultanea all’intero pubblico | Flusso di lavoro batch con più passaggi con attività e transizioni |
| **Meccanismo di ingresso** | Eventi, pubblico, qualifiche, eventi aziendali | Attivazione manuale, pianificata o API | Esecuzione pianificata del flusso di lavoro batch |
| **Modello dati** | Profilo in tempo reale + dati evento | Dati profilo + Payload API | Dati relazionali su più entità (profili, prodotti, negozi, prenotazioni) |
| **Segmentazione** | Pubblico predefinito + condizioni in tempo reale | Tipi di pubblico predefiniti di Experience Platform | Tipi di pubblico su richiesta generati nell’area di lavoro con conteggi esatti |
| **Elaborazione profilo** | Individuale, in tempo reale (quando si verificano gli eventi) | Batch, tutto in una volta | Batch, tutti con supporto per più entità |
| **Personalizzazione** | Dati contestuali in tempo reale + attributi del profilo | Attributi del profilo + dati del payload API | Dati di più entità per il targeting di precisione |
| **Complessità** | Più passaggi con diramazioni, tempi di attesa, condizioni | Azione singola o flusso di lavoro semplice | Flussi di lavoro in batch con più passaggi con segmentazione, arricchimento e divisioni |
| **Ottimo per** | Percorsi del ciclo di vita del cliente, onboarding, abbandono del carrello | Campagne promozionali, newsletter, annunci e messaggi transazionali | Campagne stagionali complesse, promozioni in più passaggi, lanci di prodotti |
| **Intervallo** | Continua, sempre attiva dopo la pubblicazione | Date di inizio/fine pianificate o attivate da API | Esecuzione batch secondo pianificazione |
| **Gestione stato** | Gestisce lo stato del cliente per le azioni in tempo reale | Esecuzione senza stato | Elaborazione in batch con tabelle di lavoro |
| **Usa quando** | Sono necessari più punti di contatto con logica decisionale in tempo reale | Messaggio semplice al pubblico in un momento specifico | Necessità di segmentazione complessa, dati di più entità o conteggi pre-invio esatti |
| **Funzionalità univoche** | Reazioni in tempo reale, attività di attesa, velocità basata su profili | Pianificazione semplice, attivazione API, controllo della tariffa | Set di dati relazionali, segmentazione di più entità, conteggi esatti, invio a più livelli |

## Guida alle decisioni {#decision-guide}

Segui questo albero decisionale per scegliere l’approccio corretto:

### Passaggio 1: qual è il requisito di esecuzione?

**Risposte individuali in tempo reale al comportamento del cliente?**
→ **Usa Percorsi**
- I profili devono spostarsi secondo il proprio ritmo
- Logica condizionale basata sul comportamento
- Il contesto in tempo reale è fondamentale

**Recapito semplice di messaggi a un pubblico?**
→ **Utilizzare campagne attivate da azioni o API**
- Tutti i profili ricevono il messaggio simultaneamente
- Pianificato o attivato tramite API
- Non è necessaria alcuna logica complessa in più passaggi

**Flusso di lavoro batch complesso con segmentazione avanzata?**
→ **Utilizza campagne orchestrate**
- Sono necessari dati su più entità (prodotti, negozi, prenotazioni)
- Richiedi conteggi pre-invio esatti
- Elaborazione batch in più fasi con divisioni e arricchimento

### Passaggio 2: convalidare la scelta

| Le tue esigenze | Approccio consigliato | Perché |
|-----------|---------------------|-----|
| Benvenuti nei nuovi clienti con l’onboarding in più passaggi | Percorsi | Ingresso in tempo reale, punti di contatto multipli, percorsi condizionali |
| Invia newsletter mensile agli abbonati | Campagna di azione | Semplice messaggio pianificato al pubblico |
| Abbandono del carrello con sequenza di promemoria | Percorsi | Trigger in tempo reale, tempi di attesa, follow-up condizionale |
| Annuncio promozionale a tutti i clienti | Campagna di azione | Messaggio una tantum, consegna immediata |
| Coinvolgere nuovamente gli utenti inattivi in base al comportamento | Percorsi | Attivato da qualificazione del pubblico, percorso personalizzato |
| Vendita flash attivata da un evento aziendale | Percorsi (evento di business) | Trigger in tempo reale che interessa più clienti |
| Promozione stagionale con integrazione del catalogo dei prodotti | Campagna orchestrata | Dati di più entità, segmentazione complessa, conteggi esatti |
| Messaggio transazionale attivato da API | Campagna attivata da API | Attivazione del sistema esterno, consegna immediata |
| Invio multilivello per prenotazione | Campagna orchestrata | Relazioni tra più entità, un messaggio per prenotazione |

## Spiegazione delle principali distinzioni {#key-distinctions}

### Percorsi: 1:1 orchestrazione in tempo reale

**Che cosa lo rende univoco:**
- Ogni profilo gestisce il singolo stato e contesto
- I profili entrano e progrediscono al proprio ritmo
- Processo decisionale in tempo reale basato su comportamenti ed eventi
- Le attività di attesa creano un intervallo personalizzato
- La diramazione condizionale crea percorsi univoci per profilo

**Flusso di esempio:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Ogni cliente sperimenta la propria timeline di percorso in base alle proprie azioni.

[Ulteriori informazioni sui Percorsi](../building-journeys/journey.md)

### Campagne: consegna semplice in batch o attivata

**Che cosa lo rende univoco:**
- Tutti i profili elaborati in modo identico e simultaneo
- Esecuzione senza stato - nessun contesto mantenuto
- Pianificazione semplice o attivazione API
- Ideale per le comunicazioni broadcast

**Flusso di esempio:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Tutti ricevono lo stesso messaggio in contemporanea.

**Tipi:**
- **Campagne azione**: consegna pianificata (una tantum o ricorrente)
- **Campagne attivate da API**: attivate tramite chiamata API da sistemi esterni

[Ulteriori informazioni sulle campagne](../campaigns/get-started-with-campaigns.md)

### Campagne orchestrate: flussi di lavoro dell’area di lavoro in batch

**Che cosa lo rende univoco:**
- Area di lavoro batch con attività e transizioni (simile all’area di lavoro percorso ma orientata ai batch)
- Supporto di dati relazionali per più entità (profili + prodotti + negozi + prenotazioni)
- Creazione di un pubblico on-demand all’interno dell’area di lavoro
- Conteggi esatti prima dell’invio (visibilità pre-invio)
- Invio multilivello (un messaggio per entità, ad esempio per prenotazione)
- Tutti i profili elaborati insieme in batch

**Flusso di esempio:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Combina la complessità del flusso di lavoro con l’esecuzione in batch delle campagne.

[Ulteriori informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

## Esempi di casi d’uso {#use-cases}

### Casi di utilizzo del percorso

- **Ripristino dell&#39;abbandono del carrello**: attivato dall&#39;evento di aggiunta al carrello, attendi l&#39;estrazione, invia promemoria se non viene effettuato alcun acquisto
- **Onboarding del cliente**: serie di benvenuto in più passaggi con contenuti personalizzati basati sui dati del profilo
- **Aggiornamento livello fedeltà**: attivato quando il cliente raggiunge un nuovo livello, invia congratulazioni e benefici
- **Campagne di compleanno**: ingresso basato sulla data di nascita, offerte personalizzate
- **Nuovo coinvolgimento**: attivato dalla qualifica del pubblico (inattività), dalla diffusione progressiva

### Casi di utilizzo delle campagne (attivati da Azione e API)

**Campagne azioni:**
- **Newsletter mensili**: consegna batch pianificata al segmento sottoscrittore
- **Annunci promozionali**: offerte sensibili al tempo per i tipi di pubblico di destinazione
- **Lanci di prodotti**: annuncio coordinato a tutti i clienti
- **Saluti stagionali**: messaggi di vacanza in date specifiche

**Campagne attivate da API:**
- **Conferme ordine**: attivato dal sistema di e-commerce dopo l&#39;acquisto
- **Notifiche di spedizione**: attivato dal sistema logistico
- **Avvisi account**: attivato dal sistema di rilevamento delle frodi
- **Reimpostazione password**: attivata dall&#39;azione dell&#39;utente nell&#39;applicazione

### Casi d’uso della campagna orchestrata

- **Promozione stagionale con integrazione catalogo**: esegui query sul catalogo dei prodotti, identifica i clienti idonei, segmenta per preferenze, invia consigli di prodotti personalizzati
- **Campagne specifiche per lo store**: rivolgiti a clienti vicini a posizioni specifiche dello store con dati di inventario dello store
- **Comunicazioni con più prenotazioni**: invia un messaggio per ogni prenotazione (prenotazioni di hotel e voli)
- **Orchestrazione dei segmenti complessa**: crea i tipi di pubblico in modo dettagliato con l&#39;arricchimento da più origini dati
- **Convalida pre-invio**: ottieni conteggi esatti dei destinatari prima di avviare campagne principali

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
| Schede di contenuto | ✅ | ✅ | ❌ | ❌ |
| Direct mail | ✅ | ✅ | ❌ | ❌ |

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

**D: posso combinare percorsi e campagne nella mia strategia di marketing?**

R: Assolutamente! La maggior parte delle organizzazioni utilizza tutti e tre gli approcci per scenari diversi:
- Percorsi di coinvolgimento comportamentale in tempo reale
- Campagne di azione per le comunicazioni broadcast pianificate
- Campagne attivate da API per i messaggi transazionali
- Campagne orchestrate per campagne batch complesse e a uso intensivo di dati

**Q: posso convertire una campagna in un percorso o viceversa?**

R: No, devi ricreare l’esperienza nel formato appropriato. Tuttavia, puoi riutilizzare contenuti, tipi di pubblico e concetti logici.

**Q: quale approccio è più semplice da compilare?**

R: Le campagne d’azione sono in genere le più semplici (messaggio singolo al pubblico), seguite da campagne attivate da API, Percorsi (più complessi con logica a più passaggi) e campagne orchestrate (più complessi a causa del flusso di lavoro dell’area di lavoro e delle funzionalità con più entità).

**Q: quali sono le migliori proporzioni per i tipi di pubblico di grandi dimensioni?**

R: Tutti e tre possono avere una buona scalabilità, ma:
- **Percorsi di pubblico di lettura** e **Le campagne d&#39;azione** sono ottimizzate per i tipi di pubblico batch di grandi dimensioni
- **Campagne orchestrate** eccellono nella segmentazione complessa con set di dati di grandi dimensioni
- **Percorsi unitari** elaborano i profili singolarmente, quindi la scalabilità dipende dal volume dell&#39;evento

**Q: posso utilizzare lo stesso pubblico in percorsi e campagne?**

R: Sì, i tipi di pubblico creati in Adobe Experience Platform possono essere utilizzati con tutti e tre gli approcci.

## Passaggi successivi {#next-steps}

Pronto per iniziare a creare? Esplora la documentazione dettagliata dell’approccio scelto:

- **[Introduzione ai Percorsi](../building-journeys/journey.md)** - Informazioni sui tipi di percorso, sulla progettazione e sul flusso di lavoro
- **[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)** - Esplora le campagne attivate da API e azioni
- **[Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)** - Esplorazione dei flussi di lavoro dell&#39;area di lavoro batch

**Ulteriori informazioni sulla decisione?**
- [Confronto dei tipi di percorso](../building-journeys/journey.md#journey-types-comparison)
- [Confronto dei tipi di campagna](../campaigns/get-started-with-campaigns.md#campaign-types)
- [Domande frequenti sul percorso](../building-journeys/journey-faq.md)
- [Domande frequenti sulle campagne orchestrate](../orchestrated/orchestrated-campaigns-faq.md)

