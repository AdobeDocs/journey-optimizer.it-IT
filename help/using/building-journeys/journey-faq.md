---
solution: Journey Optimizer
product: journey optimizer
title: Domande frequenti sui percorsi
description: Domande frequenti sui Percorsi Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: percorso, domande, risposte, risoluzione dei problemi, guida, guida
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '2363'
ht-degree: 1%

---


# Domande frequenti {#faq-journeys}

Di seguito sono riportate le domande frequenti sui Percorsi Adobe Journey Optimizer.

Hai bisogno di ulteriori dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## Concetti generali

+++ Che cos’è un percorso in Adobe Journey Optimizer?

Un percorso è un’orchestrazione in più passaggi che consente di progettare ed eseguire esperienze cliente in tempo reale su più canali. I percorsi combinano eventi, attività di orchestrazione, azioni e messaggi per creare esperienze personalizzate e contestuali basate sul comportamento dei clienti e su eventi di business.

Ulteriori informazioni su [percorsi](journey.md).

+++

+++ Quali sono i diversi tipi di percorsi?

Adobe Journey Optimizer supporta tre tipi di percorsi:

* **percorsi unitari**: attivato singolarmente da un evento (ad esempio, un acquisto, l&#39;accesso all&#39;app). I profili entrano nel percorso uno alla volta quando si verifica l’evento.
* **Leggi percorsi di pubblico**: inizia con un pubblico da Adobe Experience Platform e invia messaggi in batch a tutti i profili del pubblico.
* **percorsi di eventi di business**: attivati da eventi di business (ad esempio, aggiornamenti azionari, avvisi meteo) che interessano più profili contemporaneamente.

Ulteriori informazioni sui [tipi di percorso](entry-management.md#types-of-journeys).

+++

+++ Qual è la differenza tra un percorso e una campagna?

**Percorsi** sono orchestrazioni con più passaggi che reagiscono agli eventi o ai tipi di pubblico di destinazione, consentendo logiche complesse, condizioni, tempi di attesa e più punti di contatto nel ciclo di vita del cliente.

**Le campagne** sono comunicazioni occasionali o ricorrenti inviate a un pubblico specifico, ideali per messaggi autonomi come annunci promozionali o newsletter.

**Best practice**: utilizza i percorsi per un coinvolgimento continuo in più passaggi e campagne per comunicazioni mirate e autonome.

+++

+++ Quali sono i componenti principali di un percorso?

Un percorso è costituito da:

* **Eventi**: punti di ingresso che attivano il percorso (ad esempio, qualifica del profilo, eventi di business)
* **Attività di orchestrazione**: componenti logici come condizioni, attesa, lettura pubblico e fine
* **Azioni**: attività che eseguono attività quali l&#39;invio di messaggi, l&#39;aggiornamento di profili o la chiamata di API esterne
* **Azioni canale incorporate**: funzionalità di messaggistica native per e-mail, SMS, push e altri canali
* **Azioni personalizzate**: integrazione con sistemi di terze parti

Ulteriori informazioni sulle [attività di percorso](about-journey-activities.md).

+++

## Creazione di percorsi

+++ Come si inizia a creare il primo percorso?

Segui questi passaggi chiave:

1. **Imposta prerequisiti**: configura eventi, origini dati e azioni in base alle esigenze
2. **Creazione del percorso**: passare al menu Percorsi e fare clic su &quot;Crea Percorso&quot;
3. **Definisci le proprietà del percorso**: imposta il nome del percorso, la descrizione, lo spazio dei nomi e altre impostazioni
4. **Progetta il percorso**: trascina le attività dalla palette all&#39;area di lavoro
5. **Verifica il percorso**: utilizza la modalità di test per convalidare la logica del percorso
6. **Pubblica il percorso**: attiva il percorso per attivarlo

Segui la [guida dettagliata](journey-gs.md).

+++

+++ Quali prerequisiti sono necessari prima di creare un percorso?

I prerequisiti dipendono dal tipo di percorso:

* **percorsi attivati da eventi**: configura gli eventi per definire quando i profili devono entrare nel percorso
* **percorsi basati sul pubblico**: creazione di tipi di pubblico in Adobe Experience Platform
* **Arricchimento dati**: configurare le origini dati per il recupero di informazioni aggiuntive
* **Integrazioni di terze parti**: configurare azioni personalizzate se si utilizzano sistemi esterni

Ulteriori informazioni sulla [configurazione percorso](../configuration/about-data-sources-events-actions.md).

+++

+++ È possibile utilizzare dati provenienti da sistemi esterni del percorso?

Sì.  Puoi configurare **origini dati esterne** per recuperare informazioni dai servizi API di terze parti e utilizzarle nelle condizioni del percorso, nella personalizzazione o nelle azioni. Questo ti consente di arricchire l’esperienza del cliente con dati in tempo reale provenienti dal tuo sistema CRM, sistemi fedeltà, servizi meteo o altre piattaforme esterne.

Ulteriori informazioni sulle [origini dati esterne](../datasource/external-data-sources.md).

+++

+++ Come aggiungere condizioni al percorso?

Puoi aggiungere condizioni utilizzando l&#39;**attività Condizione** dalla palette di orchestrazione. Le condizioni consentono di:

* Creare condizioni semplici o avanzate utilizzando l’editor di espressioni
* Dividi il percorso in più percorsi in base agli attributi di profilo, all’iscrizione al pubblico, agli eventi o ai dati contestuali
* Definire i percorsi di timeout per i profili che non soddisfano la condizione entro un tempo specificato

Ulteriori informazioni sulle [condizioni](condition-activity.md).

+++

+++ Posso inviare messaggi ai profili in un percorso?

Sì.  Journey Optimizer include **azioni di canale integrate** che consentono di inviare messaggi tramite e-mail, notifiche push, SMS/MMS/RCS, messaggi in-app, esperienze Web, esperienze basate su codice, direct mailing, schede di contenuto, WhatsApp e LINE. Puoi progettare il contenuto dei messaggi direttamente in Journey Optimizer e aggiungerlo come attività di azione nel percorso.

Ulteriori informazioni su [messaggi nei percorsi](journeys-message.md).

+++

+++ Come posso attendere un orario o un evento specifico in un percorso?

Utilizza l&#39;**attività Attendi** per sospendere il percorso per una durata specificata o fino a una data/ora specifica. Le attività Attendi sono utili per:

* Invio di messaggi di follow-up dopo un ritardo (ad esempio, 3 giorni dopo l’acquisto)
* In attesa dell’orario di lavoro prima di intervenire
* Creazione di campagne drip con intervalli temporizzati
* Combinazione di condizioni per creare scenari di timeout

Ulteriori informazioni sulle [attività attendi](wait-activity.md).

+++

+++ Posso aggiornare le informazioni del profilo all’interno di un percorso?

Sì.  Utilizza l&#39;attività **Aggiorna profilo** per modificare gli attributi del profilo in Adobe Experience Platform in base a eventi o condizioni di percorso. È utile per aggiornare i punti fedeltà, registrare le milestone del percorso, modificare le impostazioni delle preferenze o tenere traccia dei punteggi di coinvolgimento dei clienti.

Ulteriori informazioni su [aggiornamenti del profilo](update-profiles.md).

+++

## Test e pubblicazione

+++ Come si verifica il percorso prima di pubblicarlo?

Journey Optimizer offre due approcci di test:

* **Modalità di test**: simula singoli profili che si spostano nel percorso passo dopo passo, consentendo di verificare logica, condizioni e azioni prima di andare &quot;live&quot;.
* **Modalità di esecuzione a secco**: esegui il percorso utilizzando dati di produzione reali senza contattare i clienti effettivi o aggiornare le informazioni del profilo. Questo ti dà fiducia nel targeting del pubblico e nella progettazione del percorso.

**Best practice**: verifica sempre i percorsi prima della pubblicazione per assicurarti che funzionino come previsto e per identificare tempestivamente eventuali problemi.

Ulteriori informazioni sulla [modalità di test](testing-the-journey.md) e sulla [esecuzione in prova](journey-dry-run.md).

+++

+++ Cosa succede quando si pubblica un percorso?

Quando pubblichi un percorso:

* Il percorso diventa **attivo** e pronto ad accettare nuovi profili
* I profili possono entrare in base ai criteri di ingresso (evento o pubblico)
* I messaggi e le azioni iniziano l’esecuzione per i profili che si spostano nel percorso
* Impossibile modificare direttamente un percorso pubblicato (è necessario creare una nuova versione)

Ulteriori informazioni su [percorsi di pubblicazione](publishing-the-journey.md).

+++

+++ Posso modificare un percorso già pubblicato?

Non è possibile modificare direttamente un percorso live. Per apportare modifiche:

1. **Crea una nuova versione**: Duplica il percorso pubblicato per creare una bozza di versione
2. **Apporta le modifiche**: modifica la bozza in base alle esigenze
3. **Verifica la nuova versione**: utilizza la modalità di test per convalidare le modifiche
4. **Pubblica la nuova versione**: la versione precedente viene chiusa automaticamente e la nuova viene attivata

I profili già presenti nel percorso completeranno la versione originale, mentre i nuovi profili entreranno nella nuova versione.

Ulteriori informazioni sulle [versioni di percorso](journey-ui.md#journey-versions).

+++

+++ Come si ferma un percorso?

È possibile gestire l&#39;esecuzione del percorso in diversi modi:

* **Chiusura di nuovi ingressi**: impedisci l&#39;accesso di nuovi profili mentre consenti il completamento del percorso di profili esistenti
* **Interrompi immediatamente**: termina il percorso ed esci da tutti i profili che contiene
* **Pausa**: arresta temporaneamente il percorso e lo riprende in un secondo momento (disponibile per tipi di percorso specifici)

Ulteriori informazioni su [percorsi finali](end-journey.md).

+++

## Esecuzione e monitoraggio del percorso

+++ Come posso tenere traccia dell’avanzamento del profilo attraverso un percorso?

Puoi monitorare l’esecuzione del percorso utilizzando:

* **Report live del Percorso**: visualizza metriche e KPI in tempo reale per il tuo percorso
* **Rapporto Percorso intero**: Analizzare le prestazioni del percorso tramite Customer Journey Analytics
* **Eventi passaggio Percorso**: accedere ai dati di esecuzione dettagliati per i rapporti personalizzati
* **Dry Run Dashboard per Percorsi**: rivedi i risultati dell&#39;esecuzione dei test prima della pubblicazione

Ulteriori informazioni sui [rapporti sui percorsi](report-journey.md).

+++

+++ Perché un profilo non è entrato nel mio percorso?

I profili dei motivi comuni non possono entrare in un percorso:

* **Evento non ricevuto**: l&#39;evento di attivazione non è stato inviato o non è stato configurato correttamente
* **Criteri di pubblico non soddisfatti**: il profilo non è idoneo per il pubblico di ingresso
* **Regole di rientro**: il profilo ha completato di recente il percorso e il rientro è bloccato
* **Percorso non pubblicato**: il percorso è in stato Bozza
* **Spazio dei nomi non valido**: lo spazio dei nomi del percorso non corrisponde all&#39;identità del profilo
* **Percorso chiuso**: il percorso non accetta più nuovi ingressi

Ulteriori informazioni sulla gestione delle [voci](entry-management.md).

+++

+++ Cosa sono gli eventi dei passaggi di percorso e come posso utilizzarli?

Gli eventi delle fasi di percorso sono set di dati generati automaticamente che acquisiscono informazioni dettagliate su ogni fase di un profilo in un percorso. Includono eventi di entrata e uscita, esecuzione di azioni (messaggi inviati, azioni personalizzate chiamate), transizioni di percorso (spostamento tra attività), errori e timeout.

**Casi d&#39;uso**:

* Creare rapporti personalizzati in strumenti di Customer Journey Analytics o BI
* Problemi di esecuzione del debug del percorso
* Tracciare il comportamento dettagliato del profilo
* Creare modelli avanzati di analisi e attribuzione

Ulteriori informazioni sugli [eventi dei passaggi del percorso](../reports/sharing-overview.md).

+++

+++ Come posso risolvere un percorso che non funziona come previsto?

Journey Optimizer fornisce diverse risorse per la risoluzione dei problemi:

* **Indicatori di errore**: avvisi visivi nell&#39;area di lavoro di percorso evidenziano problemi di configurazione
* **Modalità di test**: scorri il percorso per identificare dove si verificano i problemi
* **Rapporti Percorso**: controlla le metriche di esecuzione per individuare colli di bottiglia o errori
* **Eventi del passaggio del Percorso**: analizza dati di esecuzione dettagliati per comprendere il comportamento del profilo

**Problemi comuni**:

* Eventi o tipi di pubblico non configurati correttamente
* Connessioni all&#39;origine dati mancanti
* Espressioni non valide nelle condizioni o nella personalizzazione
* Impostazioni di timeout troppo brevi

Ulteriori informazioni su [risoluzione dei problemi dei percorsi](troubleshooting.md).

+++

+++ Cosa succede se un’azione non riesce in un percorso?

Quando un’azione non riesce (ad esempio, timeout della chiamata API, errore di consegna del messaggio), il percorso continua per impostazione predefinita a meno che non venga configurato diversamente. È possibile definire attività di condizione per gestire gli scenari di errore e gli errori vengono registrati nei rapporti di percorso e negli eventi dei passaggi per il monitoraggio.

**Best practice**: imposta i valori di timeout appropriati per le azioni esterne e definisci percorsi alternativi per gli scenari di errore critici.

Ulteriori informazioni sulle [risposte alle azioni](../action/action-response.md).

+++

## Concetti avanzati

+++ Cos’è uno spazio dei nomi di percorso e perché è importante?

Uno **spazio dei nomi** è un tipo di identità (ad esempio e-mail, ECID, numero di telefono) che determina il modo in cui i profili vengono identificati nel percorso. Lo spazio dei nomi definisce l’identificatore utilizzato per far corrispondere i profili, deve essere coerente tra eventi, tipi di pubblico e dati di profilo e influisce sul comportamento di ingresso e rientro del percorso.

**Best practice**: scegli uno spazio dei nomi che identifichi in modo affidabile i clienti in tutti i punti di contatto.

Ulteriori informazioni su [spazi dei nomi di identità](../audience/get-started-identity.md).

+++

+++ I profili possono entrare più volte nello stesso percorso?

Sì, a seconda delle **impostazioni per il rientro**:

* **Consenti rientro**: i profili possono entrare nel percorso più volte dopo averlo completato
* **Periodo di attesa per il rientro**: definire un intervallo di tempo minimo tra le voci del percorso (ad esempio, 7 giorni)
* **Forza il rientro all&#39;evento**: attiva una nuova istanza di percorso anche se il profilo è già presente nel percorso

**Best practice**: utilizza le regole per il rientro per evitare l&#39;affaticamento dei messaggi e garantire il ritmo adeguato.

Ulteriori informazioni sulla gestione delle [voci](entry-management.md).

+++

+++ Cos’è l’ottimizzazione dell’ora di invio?

**STO (Send-Time Optimization)** utilizza l&#39;intelligenza artificiale per prevedere il momento migliore per inviare un messaggio a ogni singolo profilo, massimizzando i tassi di apertura e il coinvolgimento. STO analizza i pattern di coinvolgimento storici per determinare quando è più probabile che ogni destinatario interagisca con il messaggio.

**Vantaggi**:

* Percentuali di apertura e clic migliorate
* Migliore esperienza del cliente grazie a messaggi ottimizzati
* Tariffe ridotte per l’annullamento degli abbonamenti

Ulteriori informazioni sull&#39;[ottimizzazione in fase di invio](send-time-optimization.md).

+++

+++ Cosa sono le regole di limitazione dei percorsi?

**Limitazione Percorsi** consente di limitare il numero di volte in cui un profilo può entrare in percorsi entro un periodo di tempo specificato, evitando l&#39;affaticamento dei messaggi e garantendo un&#39;esperienza cliente ottimale. Puoi impostare il numero massimo di voci per profilo, per percorsi o percorsi specifici, definire gli intervalli di tempo (giornalieri, settimanali, mensili) e assegnare la priorità ai percorsi quando più percorsi competono per lo stesso profilo.

Ulteriori informazioni sulla limitazione di [percorsi](../conflict-prioritization/journey-capping.md).

+++

+++ È possibile integrare il percorso con sistemi esterni?

Sì.  Utilizza **azioni personalizzate** per richiamare API di terze parti (CRM, automazione marketing, sistemi fedeltà), inviare dati a sistemi esterni, recuperare informazioni in tempo reale per il processo decisionale e attivare flussi di lavoro in piattaforme esterne.

Le azioni personalizzate supportano l’autenticazione (chiave API, OAuth 2.0), la personalizzazione del payload di richiesta/risposta, la gestione e i timeout degli errori e i parametri dinamici dal contesto del percorso.

Ulteriori informazioni sulle [azioni personalizzate](using-custom-actions.md).

+++

+++ Come posso utilizzare Adobe Campaign con i percorsi?

Journey Optimizer si integra in modo nativo con Adobe Campaign per sfruttare le sue funzionalità avanzate:

* **Adobe Campaign Standard**: utilizza le azioni di Campaign Standard per inviare messaggi transazionali
* **Adobe Campaign v7/v8**: attiva i flussi di lavoro di Campaign e utilizza l’infrastruttura di consegna di Campaign

**Best practice**: utilizza questa integrazione se disponi di modelli di Campaign, modelli di dati o se hai bisogno di funzionalità specifiche per Campaign.

Ulteriori informazioni sull&#39;[integrazione di Campaign](ajo-ac.md).

+++

+++ Cos’è l’attività Salta?

L&#39;**attività Salta** ti consente di cambiare i profili da un percorso all&#39;altro, abilitando modelli di percorso riutilizzabili, orchestrazione del percorso in più percorsi, manutenzione semplificata del percorso e strategie di coinvolgimento progressive.

Quando un profilo raggiunge un’attività Jump (Salta), esce dal percorso corrente e entra nel percorso target nel punto iniziale.

Ulteriori informazioni sull&#39;[attività Salta](jump.md).

+++

## Best practice e limitazioni

+++ Quali sono i limiti principali di cui devo essere a conoscenza?

Le protezioni importanti includono:

* **Complessità del Percorso**: numero massimo di attività, percorsi e livelli di nidificazione
* **Throughput**: tariffe di invio dei messaggi e limiti delle chiamate API
* **Durata**: durata massima del percorso (ad esempio, 91 giorni per percorsi unitari)
* **Dimensione pubblico**: limiti alle dimensioni batch del pubblico di lettura
* **Complessità dell&#39;espressione**: limiti dei caratteri nelle condizioni e nella personalizzazione

Visualizza [guardrail e limitazioni](../start/guardrails.md) completati.

+++

+++ Quali sono le best practice per la progettazione di percorsi?

**Struttura e organizzazione**:

* Mantieni i percorsi concentrati su casi d’uso specifici
* Utilizzare la denominazione descrittiva per le attività
* Aggiungere note ed etichette per la logica complessa
* Raggruppa percorsi correlati con tag

**Prestazioni**:

* Ottimizzare i tempi di attesa per bilanciare coinvolgimento e volume
* Limitare le chiamate API esterne ai casi d’uso essenziali
* Utilizza le regole di limite per evitare l’eccesso di messaggi
* Monitorare regolarmente le metriche del percorso

**Test**:

* Verifica sempre i percorsi prima di pubblicare
* Verifica tutti i percorsi e gli scenari condizionali
* Utilizzare profili di test realistici
* Convalidare la personalizzazione e il contenuto dinamico

**Manutenzione**:

* Verifica periodica delle prestazioni del percorso
* Archiviare o chiudere i percorsi inutilizzati
* Logica del percorso di documenti e regole di business
* Piano per il controllo delle versioni di percorso

Ulteriori informazioni sulle [best practice per la progettazione di percorsi](using-the-journey-designer.md).

+++

+++ Quante attività posso aggiungere a un percorso?

Anche se non esiste un limite al numero di attività, percorsi molto complessi (oltre 50 attività) possono diventare difficili da mantenere e risolvere i problemi. Percorsi di grandi dimensioni con numerosi rami e condizioni possono influire sui tempi di elaborazione e sulla leggibilità.

**Best practice**: se il percorso diventa troppo complesso, prova a suddividerlo in più percorsi utilizzando l&#39;attività Salta, creando percorsi secondari riutilizzabili o semplificando la logica con condizioni più efficienti.

Ulteriori informazioni sulla progettazione di [percorsi](using-the-journey-designer.md).

+++

+++ Come posso garantire che il mio percorso funzioni bene su larga scala?

**Considerazioni sulla progettazione**:

* Utilizza voce basata sul pubblico per le comunicazioni batch anziché per singoli eventi
* Implementare tempi di attesa appropriati per distribuire il volume dei messaggi
* Sfruttare le regole di limite per evitare il sovraccarico del sistema
* Ottimizzare la logica delle condizioni per ridurre la complessità di elaborazione

**Controllo**:

* Tracciare regolarmente le metriche del percorso
* Monitorare le prestazioni API per azioni personalizzate
* Rivedere le percentuali di errore e le occorrenze di timeout
* Configurazione degli avvisi per errori critici di percorso

**Ottimizzazione**:

* Utilizza la modalità di test ed esegui a secco per convalidare le prestazioni prima della pubblicazione
* Limitare le chiamate a origini dati esterne a scenari essenziali
* Memorizza nella cache i dati ad accesso frequente quando possibile
* Rivedere e ottimizzare le prestazioni di consegna dei messaggi

Ulteriori informazioni sull&#39;[ottimizzazione percorso](../start/guardrails.md).

+++

## Risorse aggiuntive

Per ulteriori informazioni e aggiornamenti, consulta le risorse seguenti:

* [Introduzione ai percorsi](journey.md)
* [Creare il primo percorso](journey-gs.md)
* [Guide alla risoluzione dei problemi](troubleshooting.md)
* [Casi di utilizzo del percorso](jo-use-cases.md)
* [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
