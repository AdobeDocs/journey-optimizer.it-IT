---
solution: Journey Optimizer
product: journey optimizer
title: Aree funzionali
description: Aree funzionali in AJO
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Concetti di base

Adobe Journey Optimizer (AJO) include diverse aree funzionali chiave che funzionano perfettamente insieme. Questa guida descrive ogni area e descrive come queste si combinano per creare esperienze cliente significative. Comprendere queste aree funzionali ti consente di sfruttare AJO per fornire esperienze personalizzate e omnicanale in modo efficiente.

## Panoramica delle aree funzionali

| Area funzionale | Vantaggio principale | Analogia |
|-------------------------|--------------------------------------------------|------------------------|
| Gestione dati | Organizzare i dati giusti del cliente | La fondazione |
| Gestione clienti | Chi sono i clienti | Conoscere il pubblico |
| Gestione dei contenuti | Creare e gestire messaggi coerenti e personalizzati | Creare il messaggio |
| Gestione delle decisioni | Seleziona il messaggio/offerta migliore in tempo reale | Il cervello |
| Journey Management | Progettare e automatizzare esperienze cliente ottimizzate | Direttore d&#39;orchestra |
| Connessioni | Collegare le origini dati e distribuirle tramite i canali del cliente | Le tubazioni |
| Amministrazione e privacy | Controllo della configurazione, dell&#39;accesso e della conformità dei dati | Il Rulebook |

## Aree funzionali dettagliate

### Gestione dei dati: The Foundation

**Scopo**: acquisire, strutturare e gestire i dati che alimentano la personalizzazione. Questo processo include la definizione delle strutture di dati (Schemi), la creazione di contenitori di archiviazione (Set di dati) e l’importazione di dati da vari sistemi.

Considera la gestione dei dati come il fondamento del coinvolgimento di tutti i clienti. Una base dati ben strutturata garantisce che ogni decisione, messaggio e percorso utilizzi informazioni accurate e organizzate.

**Componenti chiave**:

- **Creazione e gestione dello schema**: definisci la struttura dei dati del cliente.
   - Esempio: crea uno schema che delinea campi come &quot;Nome&quot;, &quot;Indirizzo e-mail&quot; e &quot;Cronologia acquisti&quot;.
- **Configurazione set di dati**: organizza i dati in contenitori logici.
   - Esempio: raggruppa i dati delle transazioni in un set di dati &quot;Transazioni di vendita&quot; per facilitarne l’analisi.
- **Flussi di lavoro di acquisizione dati**: importa i dati nella piattaforma in modo efficiente.
   - Esempio: utilizza connettori Source predefiniti per importare i dati dei clienti da un sistema di gestione delle relazioni con i clienti (CRM).
- **Strumenti per la qualità dei dati**: mantieni la precisione e la completezza dei dati.

**Vantaggio**: garantisce che i dati dei clienti siano affidabili, organizzati e accessibili, costituendo la base per tutte le attività di AJO. I connettori Source predefiniti semplificano l’acquisizione dei dati da piattaforme comuni.



### Gestione dei clienti: conoscere il tuo pubblico

**Scopo**: creare e mantenere una conoscenza approfondita di ciascun cliente. Ciò comporta l’utilizzo di Real-time Customer Profile di Adobe Experience Platform (AEP) per unire in una visualizzazione unificata i dati di tutti i punti di contatto. Inoltre, gestisce le identità tra dispositivi e canali, consentendo il raggruppamento di singoli utenti in tipi di pubblico mirabili in base ad attributi o comportamenti condivisi.

Gli strumenti di gestione dei clienti collegano diversi punti dati per fornire un quadro coerente di ciascun cliente. In questo modo potrai fornire esperienze pertinenti e personalizzate.

**Componenti chiave**:

- **Profilo cliente in tempo reale**: visualizzazione unificata di ciascun cliente.
   - Esempio: combina la cronologia di navigazione web, le interazioni tra app e gli acquisti offline in un unico profilo.
- **Risoluzione identità**: collega i dati dei clienti tra dispositivi e canali.
   - Esempio: abbina l’indirizzo e-mail di un cliente ai dati di utilizzo dell’app utilizzando il grafico delle identità.
- **Creazione e gestione del pubblico**: definisci i gruppi in base agli attributi e ai comportamenti.
   - Esempio: crea un pubblico per &quot;Clienti fedeli&quot; che hanno effettuato più di cinque acquisti nell’ultimo anno.
- **Segmentazione**: applica le regole per l&#39;iscrizione al pubblico dinamico.
   - Esempio: imposta un segmento per &quot;acquirenti di valore elevato&quot; che si aggiorna automaticamente quando i clienti spendono più di 500 $.

**Vantaggio**: consente un targeting e una personalizzazione precisi grazie a una comprensione dinamica delle preferenze individuali, della cronologia e delle appartenenze ai segmenti.



### Gestione dei contenuti: creare il messaggio

**Scopo**: creare, gestire, personalizzare e riutilizzare contenuti di marketing su più canali. Ciò include la gestione delle risorse digitali, la creazione di messaggi con editor visivi o codice, l’utilizzo di modelli di contenuto e frammenti riutilizzabili, la creazione di pagine di destinazione e l’utilizzo dell’intelligenza artificiale (IA) per la generazione di contenuti.

Gli strumenti di gestione dei contenuti assicurano che i team creino e distribuiscano messaggi personalizzati in modo efficiente, mantenendo coerenza e rilevanza in ogni punto di contatto.

**Componenti chiave**:

- **Editor contenuti**: crea e formatta i messaggi visivamente o con il codice.
   - Esempio: utilizza l’editor visivo per progettare una campagna e-mail che promuova le vendite durante le feste.
- **Gestione delle risorse digitali**: organizza e utilizza immagini e altri supporti.
   - Esempio: archivia le immagini dei prodotti in una libreria centralizzata per facilitarne il riutilizzo nelle campagne.
- **Modelli e frammenti**: crea componenti di contenuto riutilizzabili.
   - Esempio: crea un modello di &quot;Messaggio di benvenuto&quot; che inserisce dinamicamente i nomi dei clienti.
- **Strumenti di Personalization**: personalizzazione dinamica dei contenuti per singoli utenti.
   - Esempio: mostra consigli di prodotti personalizzati in base alla cronologia di navigazione.
- **Generatore di pagine di destinazione**: crea destinazioni Web per le campagne.

**Vantaggio**: semplifica la creazione di contenuti, garantisce la coerenza del brand e facilita la distribuzione efficiente di messaggi altamente personalizzati.



### Gestione delle decisioni: il cervello di Personalization

**Scopo**: seleziona il messaggio o l&#39;offerta migliore per ciascun cliente al momento giusto, in base al profilo in tempo reale, al contesto e alle regole aziendali o ai modelli di IA predefiniti. La gestione delle decisioni prevede la gestione di una libreria centrale di offerte, la definizione delle regole di idoneità, l’applicazione di vincoli (come il limite di frequenza) e la definizione della logica di classificazione.

La gestione delle decisioni garantisce che la personalizzazione funzioni su larga scala offrendo il massimo valore tramite l’automazione intelligente.

**Componenti chiave**:

- **Libreria di offerte**: archivio centrale delle offerte di marketing.
   - Esempio: store offre come &quot;20% Off Coupon&quot; o &quot;Spedizione gratuita&quot; in una libreria condivisa.
- **Regole di decisione**: logica per la selezione del contenuto ottimale.
   - Esempio: mostrare uno &quot;Sconto fedeltà&quot; solo ai clienti nel segmento &quot;Clienti fedeli&quot;.
- **Vincoli e idoneità**: controlla chi riceve cosa e quando.
   - Esempio: applica un limite di frequenza per evitare che un cliente riceva la stessa offerta due volte in una settimana.
- **Strategie di classificazione**: assegna priorità alle offerte in base agli obiettivi aziendali o all&#39;intelligenza artificiale.
   - Esempio: classifica le offerte per redditività, mostrando prima i prodotti con margini elevati.
- **Strumenti di simulazione**: verifica e convalida delle strategie decisionali.

**Vantaggio**: automatizza e ottimizza la personalizzazione, assicurando che le esperienze rilevanti e di impatto vengano distribuite in ogni punto di contatto.



### Gestione del percorso: Direttore dell&#39;Orchestra

**Scopo**: progettare, orchestrare e automatizzare le esperienze dei clienti in più passaggi e canali. I percorsi reagiscono ai comportamenti e agli eventi dei clienti in tempo reale, guidando gli utenti attraverso percorsi personalizzati. AJO supporta anche le campagne per la distribuzione di messaggi pianificati una tantum a tipi di pubblico specifici.

La gestione dei percorsi assicura che le esperienze si sentano adattive e fluide, guidando gli individui in base alle loro preferenze e azioni.

**Componenti chiave**:

- **Progettazione Percorsi**: area di lavoro visiva per la creazione di percorsi cliente.
   - Esempio: progetta un percorso che invia un’e-mail di benvenuto quando un cliente si iscrive.
- **Trigger Percorso**: eventi che avviano o anticipano percorsi.
   - Esempio: attiva un SMS di follow-up dopo che un cliente abbandona il carrello.
- **Passaggi della condizione**: utilizzare la diramazione basata su logica.
   - Esempio: invia un messaggio diverso a seconda che un cliente apra un’e-mail.
- **Attività di attesa**: controlla la progressione con ritardi di tempo.
   - Esempio: attendi tre giorni prima di inviare un promemoria e-mail.
- **Gestione campagne**: strumenti per la messaggistica pianificata una tantum.

**Vantaggio**: crea esperienze senza soluzione di continuità e connesse che si adattano alle singole interazioni, favorendo le relazioni e guidando i risultati desiderati.



### Connessioni: le tubazioni

**Scopo**: gestire il flusso di dati in AJO (origini) e la consegna di messaggi o dati da AJO (canali e destinazioni). Le origini inseriscono i dati in Adobe Experience Platform (AEP). I canali distribuiscono i messaggi (tramite e-mail, SMS, push, web, ecc.). Le destinazioni consentono al pubblico o ai set di dati di fluire sulle piattaforme esterne.

Le connessioni garantiscono che i dati entrino in AJO in modo efficace e raggiungano i clienti in modo affidabile attraverso i punti di contatto giusti.

**Componenti chiave**:

- **Connettori Source**: importa dati nella piattaforma.
   - Esempio: utilizza un connettore per portare i dati di acquisto da una piattaforma di e-commerce.
- **Configurazione canale**: configurare e gestire i meccanismi di consegna.
   - Esempio: configurare la consegna di SMS per i messaggi promozionali.
- **Configurazione della destinazione**: connessione a sistemi di attivazione esterni.
   - Esempio: condividi i dati sul pubblico con una piattaforma pubblicitaria per social media.
- **Gestione del flusso di dati**: controlla lo spostamento delle informazioni.

**Vantaggio**: assicura l&#39;acquisizione efficiente dei dati e la distribuzione affidabile dei messaggi tra i canali, consentendo al contempo l&#39;attivazione in sistemi esterni.



### Amministrazione e privacy: la regolamentazione

**Scopo**: configurare le impostazioni di sistema, gestire l&#39;accesso e le autorizzazioni degli utenti, impostare i canali di comunicazione, definire i parametri di percorso e garantire la conformità con le policy sulla privacy e la governance dei dati. Ciò include la gestione del consenso, l’applicazione delle regole di utilizzo dei dati e la gestione delle richieste di accesso o cancellazione dei dati.

Gli strumenti di amministrazione e privacy garantiscono la protezione dell’integrità dei dati e il rispetto di tutte le politiche legali e organizzative.

**Componenti chiave**:

- **Gestione degli utenti e degli accessi**: controllare l&#39;accesso e le autorizzazioni.
   - Esempio: assegna autorizzazioni specifiche ai team di marketing e IT.
- **Configurazione sandbox**: ambienti separati per sviluppo e test.
   - Esempio: utilizza una sandbox per testare le nuove progettazioni del percorso prima di distribuirle in tempo reale.
- **Configurazione canale**: configurare le impostazioni tecniche per la consegna.
   - Esempio: configura i dettagli del server e-mail per la messaggistica della campagna.
- **Strumenti per la privacy**: gestisci il consenso e le preferenze per la privacy.
   - Esempio: gestisci in modo efficiente le richieste di cancellazione dei dati in conformità al RGPD (General Data Protection Regulation, regolamento generale sulla protezione dei dati).
- **Controlli di governance**: applica criteri di utilizzo dati.

**Vantaggio**: garantisce il funzionamento sicuro della piattaforma, la conformità alle normative e l&#39;allineamento con i criteri organizzativi.



## Collegamento dei punti: come funziona il tutto insieme

Queste aree funzionali operano in un ciclo continuo per fornire e ottimizzare esperienze cliente personalizzate:

1. **Acquisizione dati**: i dati fluiscono in AEP, strutturati in base alla gestione dati.
2. **Informazioni sui clienti**: i profili cliente in tempo reale unificano questi dati, mentre la gestione clienti perfeziona le informazioni tramite profili e tipi di pubblico.
3. **Strategia per contenuti e offerte**: la gestione dei contenuti crea messaggi e risorse. Gestione delle decisioni definisce le offerte e la logica per selezionare quella migliore.
4. **Orchestrazione**: Gestione Percorso esegue il mapping delle interazioni tra canali diversi, sfruttando la comprensione, il contenuto e le decisioni dei clienti.
5. **Consegna**: le connessioni facilitano la consegna dei messaggi tramite i canali scelti o la condivisione dei dati con i sistemi esterni.
6. **Misurazione e ottimizzazione**: i dati sulle prestazioni e le interazioni dei clienti reindirizzano gli approfondimenti al sistema per perfezionare tipi di pubblico, contenuti, decisioni e percorsi.
7. **Governance**: l&#39;amministrazione e i controlli sulla privacy garantiscono la conformità e la corretta configurazione del sistema.

Questo processo iterativo consente alle organizzazioni di apprendere e migliorare continuamente le strategie di coinvolgimento dei clienti.
