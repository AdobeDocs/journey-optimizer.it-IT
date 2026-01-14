---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - Domande frequenti
description: Domande frequenti su Journey Orchestration in Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: percorso, domande, risposte, risoluzione dei problemi, guida, orchestrazione
version: Journey Orchestration
source-git-commit: bf5d018fa6c3e88cf84345e892de72ada9f2c489
workflow-type: tm+mt
source-wordcount: '5231'
ht-degree: 1%

---


# Journey Orchestration - Domande frequenti {#faq-journeys}

Trova le risposte alle domande più frequenti su Journey Orchestration in Adobe Journey Optimizer.

Hai bisogno di altri dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}.

## Concetti generali

+++ Che cos’è un percorso in Adobe Journey Optimizer?

Un percorso è un’orchestrazione in più passaggi che consente di progettare ed eseguire esperienze cliente in tempo reale su più canali. I percorsi combinano eventi, attività di orchestrazione, azioni e messaggi per creare esperienze personalizzate e contestuali basate sul comportamento dei clienti e su eventi di business.

Ulteriori informazioni su [percorsi](journey.md).

+++

+++ Quali sono i diversi tipi di percorsi?

Adobe Journey Optimizer supporta quattro tipi di percorsi:

* **percorsi unitari**: attivato singolarmente da un evento (ad esempio, un acquisto, l&#39;accesso all&#39;app). I profili entrano nel percorso uno alla volta quando si verifica l’evento.
* **Leggi percorsi di pubblico**: inizia con un pubblico da Adobe Experience Platform e invia messaggi in batch a tutti i profili del pubblico.
* **percorsi di qualificazione del pubblico**: attivato quando i profili si qualificano per (o escono da) un segmento di pubblico specifico. I profili entrano nel percorso quando soddisfano i criteri di pubblico.
* **percorsi di eventi di business**: attivati da eventi di business (ad esempio, aggiornamenti azionari, avvisi meteo) che interessano più profili contemporaneamente.

Ulteriori informazioni sui [tipi di percorso](entry-management.md#types-of-journeys).

+++

+++ Qual è la differenza tra un percorso e una campagna?

**[Percorsi](journey.md)** sono orchestrazioni con più passaggi che reagiscono agli eventi o ai tipi di pubblico di destinazione, consentendo logiche complesse, condizioni, tempi di attesa e più punti di contatto nel ciclo di vita del cliente.

**[Le campagne](../campaigns/get-started-with-campaigns.md)** sono disponibili in tre tipi:

* **[Campagne di azione](../campaigns/create-campaign.md)**: comunicazioni una tantum o ricorrenti inviate a un pubblico specifico, ideali per messaggi autonomi come annunci promozionali o newsletter.
* **[Campagne attivate da API](../campaigns/api-triggered-campaigns.md)**: campagne attivate tramite chiamate API, che consentono l&#39;integrazione con sistemi esterni per l&#39;invio di messaggi in base a eventi in tempo reale o alla logica di business.
* **[Campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)**: campagne basate su pubblico e con più passaggi create su un&#39;area di lavoro che può includere condizioni, tempi di attesa e più azioni per creare esperienze pianificate e coordinate.

**Best practice**: utilizza [percorsi](journey.md) per un coinvolgimento complesso attivato da eventi con orchestrazione avanzata; [campagne di azione](../campaigns/create-campaign.md) per comunicazioni pianificate basate su pubblico; [campagne attivate da API](../campaigns/api-triggered-campaigns.md) per l&#39;attivazione programmatica da sistemi esterni; [campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md) per comunicazioni in più passaggi con requisiti specifici per le campagne.

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

+++ Quali tipi di pubblico sono supportati nei percorsi e quali sono i loro limiti?

Adobe Journey Optimizer supporta quattro tipi di pubblico, ciascuno con caratteristiche e protezioni diverse:

**1. Tipi di pubblico in streaming**

* **Descrizione**: tipi di pubblico che vengono valutati in tempo reale in base alle modifiche apportate ai dati del profilo
* **Valutazione**: valutazione continua quando gli attributi o gli eventi del profilo corrispondono ai criteri del segmento
* **Utilizzo Percorso**: supportato nelle attività Read Audience, Audience Qualification e Condition
* **Ideale per**: coinvolgimento in tempo reale basato su modifiche comportamentali o aggiornamenti del profilo
* **Guardrail**:
   * La dimensione massima del pubblico dipende dalla licenza Journey Optimizer
   * Latenza di valutazione generalmente inferiore a 5 minuti
   * Una logica dei segmenti complessa può influire sulle prestazioni di valutazione

**2. Pubblico in batch**

* **Descrizione**: tipi di pubblico valutati su base pianificata (in genere ogni giorno)
* **Valutazione**: elaborati in processi batch a intervalli pianificati
* **Utilizzo Percorso**: supportato nelle attività Read Audience e Condition; supporto limitato nei percorsi di qualificazione del pubblico
* **Ideale per**: campagne regolari, newsletter, comunicazioni pianificate
* **Guardrail**:
   * La valutazione viene eseguita una volta al giorno (impostazione predefinita) o secondo la pianificazione configurata
   * I profili non possono riflettere le modifiche in tempo reale fino alla valutazione successiva
   * L’attività Read Audience può elaborare in modo efficiente tipi di pubblico in batch di grandi dimensioni

**3. Carica tipi di pubblico (caricamento personalizzato)**

* **Descrizione**: tipi di pubblico creati caricando file CSV con identificatori di profilo
* **Valutazione**: elenco statico aggiornato solo quando vengono caricati nuovi file
* **Utilizzo Percorso**: supportato nelle attività Read Audience e Condition; **non supportato** nei percorsi Audience Qualification
* **Ideale per**: campagne una tantum, importazioni di elenchi esterni, comunicazioni mirate
* **Guardrail**:
   * Si applicano i limiti per la dimensione del file CSV (consulta la documentazione del prodotto per conoscere i limiti attuali)
   * I membri del pubblico sono statici fino a quando non vengono aggiornati con un nuovo caricamento
   * Lo spazio dei nomi dell’identità deve corrispondere allo spazio dei nomi del percorso
   * I profili devono esistere in Adobe Experience Platform

**4. Pubblico di Federated Audience Composition (FAC)**

* **Descrizione**: tipi di pubblico creati utilizzando dati federati, che consentono di eseguire query e comporre tipi di pubblico da data warehouse esterni senza copiare i dati in Adobe Experience Platform
* **Valutazione**: composizione statica aggiornata quando viene eseguita la composizione del pubblico federato
* **Utilizzo Percorso**: supportato nelle attività Read Audience and Condition; **non supportato** nei percorsi di qualificazione del pubblico (simile al caricamento di tipi di pubblico da una prospettiva di back-end)
* **Ideale per**: integrazione di data warehouse aziendale, composizione del pubblico tramite origini dati esterne, scenari che richiedono la conservazione dei dati in sistemi esterni
* **Guardrail**:
   * I membri del pubblico sono statici fino alla successiva esecuzione della composizione federata
   * Lo spazio dei nomi dell’identità deve corrispondere allo spazio dei nomi del percorso
   * Le prestazioni dipendono dalle funzionalità di query del data warehouse esterno
   * Richiede il componente aggiuntivo Federated Audience Composition

**Tipi di pubblico di Customer Journey Analytics (CJA)**:

Anche se i tipi di pubblico di CJA non sono direttamente supportati nei percorsi, puoi utilizzare una **soluzione alternativa** &quot;racchiudendo&quot; un pubblico di CJA in una regola di segmentazione. In questo modo viene creato un pubblico UPS (Unified Profile Service) batch che fa riferimento al pubblico CJA, rendendolo disponibile per l’utilizzo in percorsi come tipo di pubblico batch.

**considerazioni specifiche per il Percorso**:

* **Leggi percorsi di pubblico**: tutti e quattro i tipi di pubblico supportati; l&#39;esportazione batch viene eseguita quando viene eseguito il percorso
* **percorsi di qualificazione del pubblico**: i tipi di pubblico in streaming sono consigliati; i tipi di pubblico in batch hanno un rilevamento di qualificazione ritardato; il caricamento e i tipi di pubblico FAC non sono supportati
* **Attività condizionali**: tutti i tipi di pubblico possono essere utilizzati per verificare l&#39;appartenenza
* **Allineamento dello spazio dei nomi**: lo spazio dei nomi dell&#39;identità del pubblico deve corrispondere allo spazio dei nomi del percorso per l&#39;identificazione corretta del profilo

**Best practice**:

* Utilizza **tipi di pubblico in streaming** per percorsi basati su eventi in tempo reale che richiedono una risposta immediata
* Utilizza **tipi di pubblico in batch** per le comunicazioni pianificate in cui è sufficiente la valutazione giornaliera
* Utilizza **carica tipi di pubblico** per campagne una tantum mirate con elenchi esterni
* Utilizza **tipi di pubblico FAC** quando devi sfruttare le funzionalità di data warehouse aziendale senza duplicazione dei dati
* Monitorare le dimensioni del pubblico e le prestazioni di valutazione in implementazioni su larga scala
* Considera le percentuali di aggiornamento del pubblico durante la progettazione della tempistica del percorso e delle condizioni di immissione

Ulteriori informazioni su [tipi di pubblico](../audience/about-audiences.md), [creazione di segmenti](../audience/creating-a-segment-definition.md), [tipi di pubblico per caricamento personalizzati](../audience/custom-upload.md) e [Composizione pubblico federata](../audience/federated-audience-composition.md).

+++

+++ Come posso scegliere tra un percorso unitario e un percorso di pubblico lettura?

Utilizza **percorsi unitari** quando:

* Devi reagire alle azioni dei singoli clienti in tempo reale (ad es. conferma di acquisto, abbandono del carrello)
* Ogni cliente deve progredire al proprio ritmo
* Desideri attivare in base a eventi specifici

Utilizza **percorsi di pubblico lettura** quando:

* Stai inviando comunicazioni in batch a un gruppo (ad es. newsletter mensile, campagne promozionali)
* Tutti i clienti devono ricevere il messaggio circa nello stesso momento
* Stai eseguendo il targeting di un segmento di pubblico predefinito

+++

## Creazione di percorsi

+++ Come si inizia a creare il primo percorso?

Segui questi passaggi chiave:

1. **Imposta prerequisiti**: configura eventi, origini dati e azioni in base alle esigenze
2. **Creazione del percorso**: passare al menu Percorsi e fare clic su &quot;Crea Percorso&quot;
3. **Definisci le proprietà del percorso**: imposta il nome del percorso, la descrizione e altre impostazioni
4. **Progetta il percorso**: trascina le attività dalla palette all&#39;area di lavoro
5. **Verifica il percorso**: utilizza la modalità di test per convalidare la logica del percorso
6. **Esegui il percorso in modalità provvisoria**: utilizza l&#39;esecuzione in modalità provvisoria per testare il percorso utilizzando dati di produzione reali senza contattare clienti reali o aggiornare le informazioni sul profilo
7. **Pubblica il percorso**: attiva il percorso per attivarlo

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

Sì, esistono diversi approcci per sfruttare i dati esterni:

**Best practice**:

* **Azioni personalizzate**: chiama API esterne tramite azioni personalizzate per recuperare o inviare dati a sistemi di terze parti. Questo è l’approccio consigliato per le interazioni in tempo reale con i sistemi esterni.
* **Ricerca set di dati**: se è possibile caricare dati da sistemi esterni in Adobe Experience Platform, utilizzare la funzione di ricerca set di dati per recuperare le informazioni archiviate nei set di dati di Experience Platform.
* **Origini dati esterne**: configura origini dati esterne per recuperare informazioni da servizi API di terze parti (meno consigliato rispetto agli approcci di cui sopra).

Queste opzioni ti consentono di arricchire l’esperienza del cliente con dati provenienti dal CRM, dai sistemi di fidelizzazione, dai servizi meteo o da altre piattaforme esterne.

Ulteriori informazioni sulle [azioni personalizzate](using-custom-actions.md) e sulla [ricerca set di dati](dataset-lookup.md).

+++

+++ Come aggiungere condizioni al percorso?

Puoi aggiungere condizioni utilizzando l&#39;**attività Condizione** dalla palette di orchestrazione. Le condizioni consentono di:

* Creare condizioni semplici o avanzate utilizzando l’editor di espressioni
* Dividi il percorso in più percorsi in base agli attributi di profilo, all’iscrizione al pubblico, agli eventi o ai dati contestuali
* Definire i percorsi di timeout per i profili che non soddisfano la condizione entro un tempo specificato

Ulteriori informazioni sulle [condizioni](condition-activity.md).

+++

+++ Posso inviare messaggi ai profili in un percorso?

Sì.  Journey Optimizer include **azioni di canale integrate** che consentono di inviare messaggi tramite e-mail, notifiche push, SMS/MMS/RCS, messaggi in-app, esperienze web, esperienze basate su codice, schede di contenuto, WhatsApp e LINE. Puoi progettare il contenuto dei messaggi direttamente in Journey Optimizer e aggiungerlo come attività di azione nel percorso.

Per i canali non supportati in modalità nativa, puoi utilizzare **azioni personalizzate** per integrarle con piattaforme di messaggistica esterne e inviare messaggi tramite qualsiasi canale di terze parti.

Ulteriori informazioni su [messaggi nei percorsi](journeys-message.md) e [azioni personalizzate](using-custom-actions.md).

+++

+++ Come posso attendere un orario o un evento specifico in un percorso?

Utilizza l&#39;**attività Attendi** per sospendere il percorso per una durata specificata o fino a una data/ora specifica. Le attività Attendi sono utili per:

* Invio di messaggi di follow-up dopo un ritardo (ad esempio, 3 giorni dopo l’acquisto)
* Creazione di campagne drip con intervalli temporizzati
* Combinazione di condizioni per creare scenari di timeout

Ulteriori informazioni sulle [attività attendi](wait-activity.md).

+++

+++ Posso aggiornare le informazioni del profilo all’interno di un percorso?

Sì.  Utilizza l&#39;attività **Aggiorna profilo** per modificare gli attributi del profilo in Adobe Experience Platform in base a eventi o condizioni di percorso. È utile per aggiornare i punti fedeltà, registrare le milestone del percorso, modificare le impostazioni delle preferenze o tenere traccia dei punteggi di coinvolgimento dei clienti.

Ulteriori informazioni su [aggiornamenti del profilo](update-profiles.md).

+++

+++ Come posso inviare un’e-mail immediatamente dopo che qualcuno ha effettuato un acquisto?

Crea un **percorso unitario attivato da eventi**:

1. Configurare un evento &quot;Acquisto&quot; con i dettagli dell’ordine
2. Aggiungere l&#39;evento come punto di ingresso del percorso
3. Segui immediatamente con un’azione E-mail
4. Crea un messaggio e-mail di conferma dell’ordine con dettagli personalizzati
5. Pubblicare il percorso

Il percorso si attiva automaticamente ogni volta che viene ricevuto un evento di acquisto, inviando l’e-mail di conferma in tempo reale.

Ulteriori informazioni sulla [configurazione evento](../event/about-events.md) e sulle [azioni e-mail](journeys-message.md).

+++

+++ Posso inviare di nuovo un messaggio se qualcuno non lo apre o non fa clic?

Sì.  Utilizza un evento **[!UICONTROL Reazione]** con **Timeout**:

1. Dopo aver inviato il messaggio, aggiungi un evento **[!UICONTROL Reazione]** **immediatamente** dopo l&#39;azione del canale (senza alcuna attività **[!UICONTROL Attendi]** nel mezzo)
2. Configura un periodo di timeout (ad esempio, 3 giorni) sull&#39;evento **[!UICONTROL Reaction]** per l&#39;ascolto delle aperture delle e-mail o dei clic
3. Creare due percorsi:
   * **Se aperto/selezionato**: procedere con i passaggi successivi o terminare il percorso
   * **Percorso timeout (non aperto/non selezionato)**: invia un messaggio e-mail di promemoria con un oggetto diverso

**Best practice**: limita il numero di invii per evitare di apparire come spammy (in genere un massimo di 1-2 promemoria).

Ulteriori informazioni su [Eventi di reazione](reaction-events.md).

+++

+++ Come si crea un percorso di abbandono del carrello?

Crea un percorso attivato da un evento utilizzando un evento **[!UICONTROL Reazione]** con timeout:

1. **Configura un evento &quot;Carrello abbandonato&quot;**: attivato quando vengono aggiunti elementi ma l&#39;estrazione non viene completata in un intervallo di tempo
2. **Invio di un messaggio iniziale** (facoltativo): messaggio e-mail di conferma degli elementi del carrello
3. **Aggiungi un evento [!UICONTROL Reazione] immediatamente dopo l&#39;azione del canale**: configuralo per l&#39;ascolto di un evento di acquisto
4. **Imposta un periodo di timeout**: definisci un timeout (ad esempio, 1-2 ore) nell&#39;evento **[!UICONTROL Reaction]** per dare al cliente il tempo di completare in modo naturale
5. **Creare due percorsi**:
   * **Se si verifica un evento di acquisto**: termina il percorso o continua con il flusso successivo all&#39;acquisto
   * **Percorso timeout (nessun acquisto)**: invia un messaggio e-mail di promemoria per l&#39;abbandono con il contenuto del carrello
6. **Facoltativo**: aggiungi un altro evento **[!UICONTROL Reazione]** **immediatamente dopo** l&#39;e-mail di promemoria con timeout (24 ore) e invia un secondo promemoria con un incentivo (ad esempio, sconto del 10%)

>[!IMPORTANT]
>
>**[!UICONTROL Reazione]** eventi devono essere inseriti immediatamente dopo [azioni canale](journeys-message.md). Non inserire attività **[!UICONTROL Wait]** tra l&#39;azione del canale e l&#39;attività **[!UICONTROL Reaction]**.

Ulteriori informazioni su [Casi d&#39;uso percorsi](jo-use-cases.md) e [eventi di reazione](reaction-events.md).

+++

+++ Come posso suddividere i clienti in percorsi diversi in base alla cronologia degli acquisti?

Utilizza un&#39;attività **Condizione** con appartenenza a un pubblico o attributi di profilo:

1. Aggiungere un’attività Condizione al percorso
2. Crea più percorsi in base ai criteri:
   * **Percorso 1**: clienti di alto valore (acquisti totali > $1000)
   * **Percorso 2**: clienti regolari (acquisti totali compresi tra $ 100 e $ 1000)
   * **Percorso 3**: nuovi clienti (acquisti totali &lt; $ 100)
3. Aggiungere messaggi o offerte diversi per ciascun percorso

Ulteriori informazioni su [condizioni](condition-activity.md) e [qualificazione del pubblico](audience-qualification-events.md).

+++

+++ Come posso gestire diversi fusi orari nel mio percorso?

Journey Optimizer offre diverse opzioni per la gestione del fuso orario:

* **Fuso orario del profilo**: i messaggi vengono inviati in base al fuso orario di ciascun utente memorizzato nel suo profilo
* **Fuso orario fisso**: tutti i messaggi utilizzano un fuso orario specifico definito dall&#39;utente

Ulteriori informazioni sulla gestione del fuso orario [&#128279;](timezone-management.md).

+++

+++ Quanto tempo devo aspettare tra i messaggi nel mio percorso?

**Procedure consigliate per i tempi di attesa**:

* **Messaggi transazionali** (conferme ordine): invia immediatamente
* **Serie di benvenuto**: 1-3 giorni tra le e-mail
* **Contenuto formativo**: 3-7 giorni tra i messaggi
* **Campagne promozionali**: almeno 7 giorni tra le offerte
* **Nuovo coinvolgimento**: 14-30 giorni per gli utenti inattivi

**Fattori da considerare**:

* Standard di settore e aspettative dei clienti
* Urgenza e importanza del messaggio
* Frequenza complessiva dei messaggi su tutti i canali
* Modelli di coinvolgimento dei clienti

**Suggerimento**: utilizza le regole di limitazione dei percorsi per limitare il numero totale di messaggi ricevuti da un cliente in tutti i percorsi.

Ulteriori informazioni sulle [attività attendi](wait-activity.md) e sui [limiti di percorso](../conflict-prioritization/journey-capping.md).

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

* Il percorso diventa **Live** e pronto ad accettare nuovi profili
* I profili possono entrare in base ai criteri di ingresso (evento o pubblico)
* I messaggi e le azioni iniziano l’esecuzione per i profili che si spostano nel percorso
* Puoi modificare solo elementi limitati su un percorso pubblicato (per modificarne altri devi creare una nuova versione)

Ulteriori informazioni su [percorsi di pubblicazione](publish-journey.md).

+++

+++ Posso modificare un percorso già pubblicato?

Sì, ma con limitazioni. Puoi modificare alcuni elementi di un percorso live:

**Elementi modificabili**:

* Proprietà percorso (nome, descrizione)
* Contenuto del messaggio nelle attività di messaggio esistenti
* Alcune impostazioni di percorso

**Elementi che non è possibile modificare**:

* Struttura del percorso (aggiunta/rimozione di attività)
* Condizioni di ingresso
* Logica area di lavoro percorso

**Per apportare modifiche strutturali**:

1. **Crea una nuova versione**: Duplica il percorso pubblicato per creare una bozza di versione
2. **Apporta le modifiche**: modifica la bozza in base alle esigenze
3. **Verifica la nuova versione**: utilizza la modalità di test per convalidare le modifiche
4. **Pubblica la nuova versione**: la versione precedente viene chiusa automaticamente e la nuova viene attivata

I profili già presenti nel percorso completeranno la versione originale, mentre i nuovi profili entreranno nella nuova versione.

Ulteriori informazioni sulle [versioni di percorso](journey-ui.md#journey-filter).

+++

+++ Come si ferma un percorso?

È possibile gestire l&#39;esecuzione del percorso in diversi modi:

* **Chiusura di nuovi ingressi**: impedisci l&#39;accesso di nuovi profili mentre consenti il completamento del percorso di profili esistenti
* **Interrompi immediatamente**: termina il percorso ed esci da tutti i profili che contiene
* **Pausa**: arresta temporaneamente il percorso e lo riprende in un secondo momento

Ulteriori informazioni su [percorsi finali](end-journey.md).

+++

+++ Qual è la differenza tra &quot;Vicino ai nuovi ingressi&quot; e &quot;Fermo&quot;?

**Chiudi ai nuovi ingressi**:

* I nuovi profili non possono entrare nel percorso
* I profili già nel percorso continuano e completano il loro percorso
* Utilizzalo quando vuoi chiudere un percorso con facilità
* Esempio: campagna stagionale terminata ma desideri che i clienti esistenti completino la loro esperienza

**Interrompi**:

* Termina immediatamente il percorso per tutti i profili
* Tutti i profili attualmente nel percorso sono usciti
* Utilizzalo per situazioni urgenti o errori critici
* Esempio: ritiro del prodotto che richiede l&#39;interruzione immediata dei messaggi promozionali

Ulteriori informazioni su [percorsi finali](end-journey.md) e [percorsi di pubblicazione](publish-journey.md).

+++

## Esecuzione e monitoraggio del percorso

+++ Come posso tenere traccia dell’avanzamento del profilo attraverso un percorso?

Puoi monitorare l’esecuzione del percorso utilizzando:

* **Report live del Percorso**: visualizza le metriche e i KPI in tempo reale per il tuo percorso. È inoltre possibile esaminare i risultati dell’esecuzione di test a secco qui.
* **Rapporto Percorso intero**: Analizzare le prestazioni del percorso utilizzando Customer Journey Analytics. È inoltre possibile esaminare i risultati dell’esecuzione di test a secco qui.
* **Eventi passaggio Percorso**: accedere ai dati di esecuzione dettagliati per i rapporti personalizzati

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
* **Tempistica per la qualifica del pubblico in streaming**: per i percorsi che utilizzano la qualifica del pubblico con tipi di pubblico in streaming, i profili non possono entrare se facevano già parte del pubblico prima che il percorso fosse pubblicato o se il percorso non ha completato il periodo di attivazione (fino a 10 minuti dopo la pubblicazione)

Ulteriori informazioni sulla [gestione delle voci](entry-management.md) e sulle [considerazioni sulla tempistica di qualificazione del pubblico in streaming](audience-qualification-events.md#streaming-entry-caveats).

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
* **Modalità di esecuzione a secco**: verifica il percorso utilizzando dati di produzione reali senza contattare i clienti per convalidare il targeting e l&#39;esecuzione
* **Rapporti Percorso**: controlla le metriche di esecuzione per individuare colli di bottiglia o errori
* **Eventi del passaggio del Percorso**: analizza dati di esecuzione dettagliati per comprendere il comportamento del profilo

**Problemi comuni**:

* Eventi o tipi di pubblico non configurati correttamente
* Connessioni all&#39;origine dati mancanti
* Espressioni non valide nelle condizioni o nella personalizzazione
* Impostazioni di timeout troppo brevi

Ulteriori informazioni su [risoluzione dei problemi dei percorsi](troubleshooting.md).

+++

<!--
+++ What happens if an action fails in a journey?

When an action fails (e.g., API call timeout, message delivery error), the journey continues by default unless configured otherwise. You can define condition activities to handle failure scenarios, and errors are logged in journey reports and step events for monitoring.

**Best practice**: Set appropriate timeout values for external actions and define alternative paths for critical failure scenarios.

Learn more about [action responses](../action/action-response.md).

+++
-->

+++ Posso vedere chi si trova attualmente nel mio percorso?

Sì.  Utilizza il **rapporto live del Percorso** per visualizzare:

* Numero di profili attualmente nel percorso
* Numero di profili per ogni attività
* Profili immessi nelle ultime 24 ore
* Metriche di esecuzione in tempo reale

Per visualizzare i singoli profili, utilizza **eventi di passaggio di percorso** in Customer Journey Analytics o esegui una query diretta sui set di dati dell&#39;evento di passaggio.

Ulteriori informazioni sui [rapporti live di percorso](report-journey.md).

+++

+++ Perché i messaggi non vengono inviati nel percorso?

**Motivi e soluzioni comuni**:

* **Problemi di consenso**: i destinatari non hanno acconsentito alla ricezione di comunicazioni
Soluzione: controllare i criteri di consenso e lo stato di consenso

* **Elenco di soppressione**: gli indirizzi e-mail sono inclusi nell&#39;elenco di soppressione
Soluzione: controlla l’elenco di soppressione per i mancati recapiti o i reclami

* **Informazioni di contatto non valide**: indirizzi e-mail/numeri di telefono mancanti o in formato non valido
Soluzione: convalidare la qualità dei dati del profilo

* **Percorso non pubblicato**: il percorso è ancora in modalità bozza
Soluzione: pubblicare il percorso per attivarlo

<!-- 
* **Message not approved**: Message content requires approval before sending
  Solution: Submit for approval or check approval status-->

* **Problema di configurazione del canale**: la configurazione di e-mail/SMS non è corretta
Soluzione: verificare le configurazioni dei canali e l’autenticazione

Ulteriori informazioni sulla [risoluzione dei problemi](troubleshooting.md) e sulla [gestione del consenso](../action/consent.md).

+++

+++ Come posso personalizzare i messaggi nel mio percorso?

Puoi personalizzare i messaggi utilizzando l&#39;**editor di personalizzazione**:

**Dati di personalizzazione disponibili**:

* **Attributi del profilo**: nome, cognome, e-mail, campi personalizzati
* **Dati evento**: dettagli di acquisto, comportamento di navigazione, attività app
* **Dati contestuali**: variabili di Percorso, dati API esterni
* **Iscrizione al pubblico**: qualifiche del segmento
* **Attributi calcolati**: valori precalcolati

**Esempio di personalizzazione**:

* &quot;Salve `{{profile.firstName}}`, grazie per aver acquistato `{{event.productName}}`&quot;
* &quot;In base al livello di fedeltà (`{{profile.loyaltyTier}}`), ecco un&#39;offerta speciale&quot;
* Blocchi di contenuto dinamici che cambiano in base alle preferenze del cliente

Ulteriori informazioni sulla [personalizzazione](../personalization/personalize.md).

+++

+++ Posso inviare messaggi diversi in base al canale preferito?

Sì.  Utilizza un&#39;attività **[Condizione](condition-activity.md)** per instradare i profili in base al loro canale preferito:

1. Aggiungi un&#39;attività [Condizione](condition-activity.md) nel percorso
2. Creare un percorso per ogni canale controllando l&#39;attributo di profilo canale preferito (ad esempio, `profile.preferredChannel`)
3. Configurare percorsi specifici per il canale:
   * **Percorso e-mail**: aggiungi [azione e-mail](../email/create-email.md) con contenuto ottimizzato per e-mail
   * **Percorso SMS**: aggiungi [azione SMS](../sms/create-sms.md) con messaggi concisi
   * **Percorso push**: aggiungi [azione notifica push](../push/create-push.md) con contenuto breve e actionable
   * **Percorso in-app**: aggiungi [azione messaggio in-app](../in-app/create-in-app.md) per gli utenti dell&#39;app interessati
4. Aggiungi un percorso predefinito per i profili senza preferenze, indirizzandoli al canale principale

**Best practice**:

* Assicurati che i dati del profilo includano preferenze di canale precise
* Progettare contenuti appropriati per i punti di forza e i limiti di ogni canale
* Utilizza [superfici di canale](../configuration/channel-surfaces.md) per gestire le configurazioni di canale
* Verifica tutti i percorsi per garantire la corretta consegna dei messaggi

Ulteriori informazioni su [condizioni](condition-activity.md), [azioni messaggio](journeys-message.md) e [selezione canale](../channels/gs-channels.md).

+++

+++ Posso escludere alcuni clienti dal mio percorso?

Sì, esistono diversi modi per escludere i clienti:

**Alla voce percorso**:

* Usa [definizioni pubblico](../audience/creating-a-segment-definition.md) con regole di esclusione
* Aggiungi [condizioni di ingresso](entry-management.md) che escludono profili specifici
* Configura i criteri di uscita [basati sull&#39;attributo del profilo](journey-properties.md) nelle proprietà del percorso per escludere automaticamente i profili in base ad attributi specifici

**Nel percorso**:

* Aggiungi un&#39;attività [Condizione](condition-activity.md) all&#39;inizio del percorso per uscire dai profili indesiderati
* Verifica la presenza di attributi di esclusione (ad esempio, stato VIP, account di test)
* Usa [qualifica pubblico](audience-qualification-events.md) per identificare i profili da escludere

**Scenari di esclusione di esempio**:

* Escludi i clienti che hanno acquistato di recente
* Escludere i clienti VIP dalle promozioni standard
* Escludi dipendenti e verifica account
* Escludere i clienti in aree geografiche specifiche

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
* **Identificatore supplementare**: utilizza un ID supplementare per consentire ai profili di rientrare nel percorso più volte per entità diverse (ad esempio, ordini, prenotazioni o transazioni diversi), anche se sono già nel percorso

**Best practice**: utilizza le regole per il rientro per evitare l&#39;affaticamento dei messaggi e garantire il ritmo adeguato. Valuta l’utilizzo di identificatori supplementari per i percorsi transazionali in cui i profili devono essere immessi più volte per diverse transazioni.

Ulteriori informazioni sulla [gestione delle voci](entry-management.md) e [identificatori supplementari](supplemental-identifier.md).

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

**Limitazione Percorsi** consente di controllare il modo in cui i profili interagiscono con i percorsi, evitando l&#39;eccesso di messaggi e garantendo un&#39;esperienza ottimale per il cliente:

* **Limite di ingresso**: limita il numero di volte in cui un profilo può entrare in percorsi entro un periodo di tempo specificato
* **Limite di concorrenza**: limita il numero di percorsi in cui un profilo può trovarsi simultaneamente

Puoi impostare il numero massimo di voci o la concorrenza per profilo in percorsi o percorsi specifici, definire intervalli di tempo (giornalieri, settimanali, mensili) e assegnare la priorità ai percorsi quando più percorsi competono per lo stesso profilo.

Ulteriori informazioni sulla limitazione di [percorsi](../conflict-prioritization/journey-capping.md).

+++

+++ È possibile integrare il percorso con sistemi esterni?

Sì.  Utilizza **azioni personalizzate** per richiamare API di terze parti (CRM, automazione marketing, sistemi fedeltà), inviare dati a sistemi esterni, recuperare informazioni in tempo reale per il processo decisionale e attivare flussi di lavoro in piattaforme esterne.

Le azioni personalizzate supportano l’autenticazione (chiave API, autenticazione personalizzata), la personalizzazione del payload di richieste/risposte, la gestione degli errori e i timeout, nonché i parametri dinamici dal contesto del percorso.

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

+++ Come si crea un percorso di serie di benvenuto?

Una tipica serie di benvenuto include più punti di contatto nell’arco di diversi giorni:

**Struttura di esempio**:

1. **Voce**: pubblico di nuovi abbonati o evento quando qualcuno si iscrive
2. **E-mail 1 - Benvenuto immediato**: grazie e introduzione
3. **Attendi**: 2 giorni
4. **E-mail 2 - Guida introduttiva**: tutorial o guida del prodotto
5. **Attendi**: 3 giorni
6. **Condizione**: il cliente ha effettuato un acquisto?
   * **Sì**: termina o passa al percorso clienti
   * **No**: continua serie di benvenuto
7. **E-mail 3 - Incentivo**: sconto speciale per il primo acquirente
8. **Attendi**: 5 giorni
9. **E-mail 4 - Coinvolgimento**: best-seller o contenuti popolari

**Best practice**:

* Conserva fino a 3-5 e-mail in 2-3 settimane
* Ogni e-mail deve avere uno scopo chiaro e call-to-action
* Monitorare i tassi di apertura e regolare di conseguenza i tempi e i contenuti
* Esci anticipatamente dai clienti se si convertono o si impegnano a fondo

Ulteriori informazioni sui [casi d&#39;uso percorsi](jo-use-cases.md).

+++

+++ È possibile eseguire test A/B su percorsi diversi nel percorso?

Sì.  Utilizza l&#39;attività **Ottimizza** (disponibilità limitata) o crea manualmente le suddivisioni di test:

**Utilizzo dell&#39;attività Ottimizza** con il metodo di esperimento:

* Suddivide in modo casuale il traffico tra percorsi diversi per determinare quale funziona meglio
* Verifica diversi messaggi, offerte, tempi di attesa o percorsi di percorso interi
* Misura le prestazioni in base a metriche di successo predefinite e dichiara un vincitore

**Utilizzo dell&#39;attività Ottimizza** con il metodo di condizione Origine dati:

* Crea una condizione per la suddivisione casuale dei profili (ad esempio, utilizzando una funzione numerica casuale)
* Invia diverse esperienze a ogni suddivisione
* Misurare i risultati utilizzando i rapporti di percorso

**Elementi da verificare**:

* Diverse righe oggetto e-mail
* Contenuto alternativo del messaggio
* Tempi di attesa diversi
* Varie offerte o incentivi
* Percorsi di percorso completamente diversi

Ulteriori informazioni su [ottimizza attività](optimize.md) e [esperimenti di contenuto](../content-management/content-experiment.md).

+++

+++ Come si attiva un percorso quando l&#39;inventario è basso?

Crea un **percorso di eventi aziendali**:

1. **Configura un evento di business**: imposta un evento attivato dal sistema di inventario quando le scorte scendono al di sotto di una soglia
2. **Seleziona il pubblico di destinazione**: scegli i profili da notificare (ad esempio, i clienti che hanno visualizzato il prodotto, gli abbonati agli avvisi di riassortimento)
3. **Aggiungi azione messaggio**: invia e-mail o push di notifica
4. **Personalizza contenuto**: include dettagli prodotto, livello di inventario corrente, messaggi di urgenza

**Eventi aziendali di esempio**:

* Avviso inventario ridotto
* Notifica di riduzione prezzo
* Prodotto di nuovo disponibile
* Annuncio vendita flash
* Promozioni in base al tempo

Ulteriori informazioni su [eventi aziendali](general-events.md).

+++

+++ Cosa sono i criteri di unione e come influiscono sui percorsi?

**I criteri di unione** determinano il modo in cui Adobe Experience Platform combina dati provenienti da più origini per creare una visualizzazione di profilo unificata. Definiscono regole per la definizione delle priorità dei dati e l’unione delle identità quando esistono frammenti di profilo in set di dati diversi.

**Impatto sui percorsi**:

* I percorsi utilizzano il criterio di unione associato al pubblico o all’evento per determinare quali dati di profilo sono disponibili
   * In percorsi di lettura del pubblico o di qualificazione del pubblico: viene utilizzato il criterio di unione del pubblico
   * Nei percorsi di eventi unitari: viene utilizzato il criterio di unione predefinito
   * Nei percorsi di eventi aziendali: viene utilizzato il criterio di unione del pubblico di destinazione nella seguente attività Read audience

* Il criterio di unione influisce sugli attributi accessibili in condizioni di percorso, personalizzazione e azioni
* Criteri di unione diversi possono causare l’utilizzo di dati di profilo diversi nel percorso

**Best practice**:

* Assicurati che il criterio di unione utilizzato dal percorso sia allineato ai requisiti di governance dei dati
* Scopri quali set di dati sono inclusi nel criterio di unione per conoscere i dati disponibili
* Utilizzare criteri di unione coerenti tra tipi di pubblico e percorsi correlati per ottenere risultati prevedibili

Ulteriori informazioni su [criteri di unione](../audience/get-started-profiles.md) e [gestione identità](../audience/get-started-identity.md).

+++

+++ Qual è la differenza tra una condizione e un’attività Attendi?

| | **Attività condizione** | **Attività Attendi** |
|---|---|---|
| **Finalità** | Crea percorsi diversi in base alla logica (if/then) | Sospende il percorso per un periodo di tempo |
| **Funzione** | Valuta i dati e instrada i profili di conseguenza | Mantiene i profili in un punto specifico prima di continuare |
| **Caso d’uso** | Segmentazione clienti, verifica stato, ramo in base al comportamento | Intervallo tra i messaggi, attesa dell’orario di lavoro, creazione di ritardi |
| **Esempio** | Se il cliente è VIP, invia un’offerta premium; in caso contrario invia un’offerta standard | Attendi 3 giorni dall’e-mail di benvenuto prima di inviare il messaggio successivo |

**Lavorano insieme**:

* Attendi un periodo, quindi utilizza una condizione per verificare se si è verificato un errore durante l’attesa
* Esempio: attendi 7 giorni, quindi verifica se il cliente ha effettuato un acquisto

Ulteriori informazioni sulle [condizioni](condition-activity.md) e sulle [attività di attesa](wait-activity.md).

+++

## Best practice e limitazioni

+++ Quali sono i limiti principali di cui devo essere a conoscenza?

Le protezioni importanti includono:

* **Complessità del Percorso**: numero massimo di attività, percorsi e livelli di nidificazione
* **Throughput**: tariffe di invio dei messaggi e limiti delle chiamate API
* **Durata**: durata massima del percorso (ad esempio, 91 giorni)
* **Dimensione pubblico**: limiti alle dimensioni batch del pubblico di lettura
* **Complessità dell&#39;espressione**: limiti dei caratteri nelle condizioni e nella personalizzazione

Visualizza [guardrail e limitazioni](../start/guardrails.md) completati.

+++

+++ Quali sono le best practice per la progettazione di percorsi?

**Struttura e organizzazione**:

* Mantieni i percorsi concentrati su casi d’uso specifici
* Utilizzare la denominazione descrittiva per le attività
* Aggiungere descrizioni ed etichette per la logica complessa
* Raggruppa percorsi correlati con tag

**Prestazioni**:

* Ottimizzare i tempi di attesa per bilanciare coinvolgimento e volume
* Limitare le chiamate API esterne ai casi d’uso essenziali
* Utilizza le regole di limite per evitare l’eccesso di messaggi
* Monitorare regolarmente le metriche del percorso

**Test**:

* Verifica sempre i percorsi prima di pubblicare
* Utilizza la modalità di test per convalidare la logica di percorso e analizzare il percorso
* Utilizza la modalità di esecuzione in prova per testare i dati di produzione reali senza contattare i clienti
* Verifica tutti i percorsi e gli scenari condizionali
* Utilizzare profili di test realistici
* Convalidare la personalizzazione e il contenuto dinamico

**Manutenzione**:

* Verifica periodica delle prestazioni del percorso
* Interrompi o chiudi percorsi inutilizzati
* Logica del percorso di documenti e regole di business
* Piano per il controllo delle versioni di percorso

Ulteriori informazioni sulle [best practice per la progettazione di percorsi](using-the-journey-designer.md).

+++

+++ Quante attività posso aggiungere a un percorso?

I percorsi sono limitati a un massimo di 50 attività. Tuttavia, consigliamo di mantenere i percorsi più semplici per migliorare la manutenzione e le prestazioni.

Quando i percorsi si avvicinano a 50 attività, possono diventare molto complesse e difficili da mantenere, risolvere i problemi e capire. Percorsi di grandi dimensioni con molti rami e condizioni possono inoltre influire sui tempi di elaborazione, sulla leggibilità e sulla collaborazione tra team.

**Best practice**: mantieni i tuoi percorsi concentrati e gestibili. Se il tuo percorso sta diventando complesso, considera:

* Suddividerlo in più percorsi utilizzando l’attività Salta
* Creazione di pattern riutilizzabili in percorsi più semplici
* Semplificare la logica con condizioni più efficienti
* Verifica della necessità di tutte le attività

Ulteriori informazioni su [Progettazione percorso](using-the-journey-designer.md) e [guardrail e limitazioni](../start/guardrails.md).

+++

+++ Come posso garantire che il mio percorso funzioni bene su larga scala?

**Considerazioni sulla progettazione**:

* Utilizza [voce basata su pubblico](read-audience.md) per le comunicazioni batch invece di singoli eventi
* Implementa [tempi di attesa](wait-activity.md) appropriati per distribuire il volume dei messaggi
* Sfrutta [regole di limitazione](../conflict-prioritization/journey-capping.md) per evitare un sovraccarico del sistema
* Ottimizza [logica della condizione](condition-activity.md) per ridurre la complessità di elaborazione

**Controllo**:

* Tieni traccia di [metriche di percorso](report-journey.md) regolarmente
* Monitora le prestazioni API per [azioni personalizzate](using-custom-actions.md)
* Rivedi le percentuali di errore e le occorrenze di timeout utilizzando [strumenti per la risoluzione dei problemi](troubleshooting.md)
* Iscriviti a [avvisi di percorso](../reports/alerts.md) errori critici di percorso

**Ottimizzazione**:

* Utilizza la [modalità di test](testing-the-journey.md) e la [esecuzione completa](journey-dry-run.md) per convalidare le prestazioni prima della pubblicazione
* Riduci al minimo le chiamate API esterne tramite [azioni personalizzate](using-custom-actions.md) per evitare latenza e dipendenza da sistemi di terze parti
* Archivia i dati utilizzati di frequente in Adobe Experience Platform utilizzando [ricerca set di dati](dataset-lookup.md) invece di eseguire chiamate esterne, quando possibile
* Rivedi e ottimizza le prestazioni della [consegna messaggi](journeys-message.md)

Ulteriori informazioni su [guardrail e limitazioni](../start/guardrails.md).

+++

## Risorse aggiuntive

Per ulteriori informazioni e aggiornamenti, consulta le risorse seguenti:

* [Introduzione ai percorsi](journey.md)
* [Creare il primo percorso](journey-gs.md)
* [Guide alla risoluzione dei problemi](troubleshooting.md)
* [Casi di utilizzo del percorso](jo-use-cases.md)
* [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
