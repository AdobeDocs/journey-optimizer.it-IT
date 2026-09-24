---
solution: Journey Optimizer
product: journey optimizer
title: Collaboratore per percorsi
description: Scopri le competenze CX Enterprise Coworker disponibili per la creazione, la generazione di contenuti e l’analisi di percorsi in Adobe Journey Optimizer, con istruzioni approfondite e prompt di esempio.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 932218c2-64c1-466e-afc4-120b6d8fe37f
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
    internal-label: Journey management
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
    internal-label: Journey design
source-git-commit: d645b6528fa7a1ae5169f129613f9085672e2ebb
workflow-type: tm+mt
source-wordcount: '2593'
ht-degree: 7%
---

# Collaboratore per percorsi {#journeys-coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le competenze CX Enterprise Coworker disponibili per i percorsi in Adobe Journey Optimizer, con indicazioni dettagliate, prompt di esempio e best practice per ogni competenza, per la creazione di percorsi dal linguaggio naturale, la generazione di contenuti del canale e l&#39;analisi delle prestazioni del percorso.

Ulteriori informazioni:

* [Competenze del collaboratore per Journey Optimizer](../start/ai-features.md#cx-coworker-skills): panoramica delle competenze del collaboratore tra Percorsi, fidelizzazione e gestione dei contenuti in Journey Optimizer.
* [Documentazione di Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: panoramica delle funzionalità Campagne, Chat e Progetti di Coworker.
* [Guida all&#39;interfaccia utente di Chat con i collaboratori](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: come accedere e navigare in Chat con i collaboratori.

>[!ENDSHADEBOX]

## Creazione percorso {#journey-create}

La creazione di percorsi consente agli utenti di Journey Optimizer di creare e configurare percorsi di marketing utilizzando un’interfaccia in linguaggio naturale. Con la creazione di Percorsi, i professionisti possono creare rapidamente percorsi descrivendo i loro requisiti nei prompt conversazionali. L’abilità guida gli utenti attraverso le diverse opzioni per la creazione di un percorso, consentendo agli addetti al marketing di concentrarsi sulla strategia anziché sulla configurazione tecnica.

>[!AVAILABILITY]
>
>Per utilizzare completamente le funzioni di creazione dei Percorsi, è necessario disporre delle seguenti autorizzazioni:
>
>**Gestisci Percorsi**: questa autorizzazione consente di creare nuovi percorsi direttamente in Coworker.
>
>**Visualizza eventi di Percorso, origini dati e azioni**: questa autorizzazione garantisce che il collaboratore possa eseguire ricerche tramite eventi di Percorso e azioni personalizzate.
>
>**Visualizza segmenti**: questa autorizzazione garantisce che il collaboratore possa cercare i segmenti di pubblico durante la creazione di un Percorso.
>
>**Gestisci segmenti**: questa autorizzazione ti consente di creare nuovi tipi di pubblico direttamente in Coworker.

### Casi d’uso principali

Percorso Creazione di offerte funzionalità che possono essere utilizzate per accelerare l’esecuzione del marketing:

* **Creazione percorso attivata da eventi**

  * Creazione di percorsi che si attivano in base a eventi cliente specifici.
  * Progetta risposte automatizzate alle azioni dei clienti in tempo reale.
  * Creare flussi di comunicazione personalizzati in base al comportamento del cliente.

  **percorso di visite al negozio:**
  &quot;Crea un percorso che inizia quando un utente accede alla posizione del mio negozio. Invia una notifica push per accogliere gli utenti nello store. Attendi 2 giorni e controlla se l’utente ha un indirizzo e-mail valido. Se l’utente dispone di un indirizzo e-mail valido, invia un sondaggio e-mail per chiedere informazioni sulla sua esperienza di negozio. Se l’utente non dispone di un indirizzo e-mail valido, invia una notifica push per richiedere la registrazione.&quot;

  **percorso post-acquisto:**
  &quot;Crea un percorso che inizia quando un cliente effettua un acquisto online. Invia una notifica push per ringraziarli dell’acquisto. Quindi, verifica se sono membri fedeltà. Se l’utente è un membro dei premi fedeltà, invia una seconda notifica push con un codice di sconto del 10%. Se l’utente non è un membro dei premi fedeltà, invia un messaggio push per invitarlo a iscriversi al programma fedeltà. Attendi 2 giorni e invia un messaggio push di follow-up con un sondaggio sulla loro esperienza di acquisto.&quot;

  **Promozione basata su eventi:**
  &quot;Crea un percorso attivato quando il punteggio di gioco raggiunge 50. Invia un messaggio SMS ai membri del premio fedeltà che dichiarano di poter usufruire di una fetta gratuita di pizza dallo sponsor partner.&quot;

* **Creazione di percorsi con targeting di pubblico**

  * Crea percorsi rivolti a segmenti di pubblico specifici.
  * Progettazione di sequenze di comunicazione in più fasi con tempistiche strategiche.

  **Campagna stagionale:**
  &quot;Voglio creare un percorso che si rivolga ad un pubblico di escursionisti. Voglio inviare un messaggio e-mail per avvisare il pubblico della mia prossima vendita di vacanze che include una varietà di elementi essenziali per le escursioni. Attendi 3 giorni dopo l’invio della prima e-mail e invia una seconda e-mail con un coupon del 15% con spedizione gratuita. Attendi 1 settimana e poi invia un terzo messaggio e-mail per mostrare il nostro nuovo sacco a pelo e la collezione di tende. Pianifica il percorso per iniziare il 20/12.&quot;

  **Riconoscimento fedeltà:**
  &quot;Crea un percorso di apprezzamento della fedeltà per i proprietari di SUV, tra cui una notifica push di ringraziamento con un’offerta di carwash gratuita e un promemoria di notifica push di follow-up se la prima notifica non viene interagita entro 1 giorno.&quot;

* **Creazione percorso attivata da un evento business**

  * Creazione di percorsi che si attivano in base a un particolare evento di business e si rivolgono a un pubblico specifico (ad esempio, il prodotto torna in magazzino o cambia il punteggio di gioco)
  * Messaggi tempestivi e contestuali da attivare quando cambiano le condizioni di business.

* **Creazione del percorso di qualificazione del pubblico**

  * Crea percorsi che si attivano quando i profili entrano o escono da una definizione di segmento di pubblico.
  * Automatizza la messaggistica di entrata e uscita per supportare gli obiettivi di onboarding, conservazione e riconquista.

* **Flussi percorso condizionale**

  * Crea rami decisionali in base agli attributi del cliente.
  * Progetta percorsi suddivisi in base alle preferenze del cliente.

* **Crea percorso da immagine**

  * Carica un’immagine di riferimento in Collaborator e chiedi di creare un percorso utilizzando l’immagine come riferimento
  * L’abilità di creazione del percorso estrae un prompt modificabile dall’immagine di riferimento

Con questa abilità, i requisiti del linguaggio naturale sono tradotti in configurazioni di percorso strutturate.

### Competenze in ambito

Le seguenti funzionalità sono supportate da Creazione Percorso:

* **Creazione di un percorso in linguaggio naturale**: consente agli utenti di descrivere il flusso di percorso in linguaggio di conversazione.
* **percorsi basati su eventi e su pubblico**: supporta sia i tipi di percorso basati su attivatori che quelli pianificati, nonché la qualificazione di eventi di business e pubblico.
* **Logica condizionale**: gestisce le suddivisioni e le diramazioni delle decisioni in base agli attributi del cliente.
* **Messaggistica multicanale**: supporta notifiche push, e-mail e canali SMS.
* **Pianificazione Percorsi**: configura le date di inizio e gli orari per i percorsi pianificati.

### Competenze al di fuori dell’ambito

Attualmente, le seguenti funzonalità non sono supportate:

* Analisi avanzata del percorso
* Orchestrazione tra percorsi
* Configurazione test A/B
* Generazione di espressioni InAudience
* Nodi di ricerca del set di dati
* Impostazioni invio ondata
* Opzioni di ricorrenza pianificazione
* Selezione dello spazio dei nomi per i tipi di pubblico
* Mappatura campo Azione personalizzata
* Trasformazioni complesse dei dati

### Best practice per la richiesta di informazioni

Per massimizzare l’efficacia della creazione di Percorsi, segui queste best practice:

* **Specifica**: fornisci dettagli chiari sugli obiettivi del percorso, sul pubblico di destinazione e sulle azioni desiderate. Includi informazioni su canali, tempi e condizioni.
* **Specificare l&#39;intervallo**: indicare chiaramente i periodi di attesa tra le azioni e l&#39;inizio del percorso.
* **Definisci condizioni**: quando utilizzi la logica condizionale, spiega i criteri per ciascun percorso di diramazione.
* **Includi canali**: specifica i canali di comunicazione da utilizzare (push, e-mail, SMS).
* **Pianificazione menzione**: per i percorsi pianificati, fornisci la data e l&#39;ora di inizio desiderate.
* **Azioni personalizzate**: se utilizzi azioni personalizzate nel flusso di lavoro, devi specificare che utilizzi un&#39;azione personalizzata insieme al nome esatto dell&#39;azione personalizzata. Esempio:
Quando un utente accede alla posizione del mio archivio, invia un messaggio di benvenuto utilizzando l’azione personalizzata ExternalPush. Attendi 2 giorni e invia un messaggio di follow-up utilizzando l’azione personalizzata ExternalEmail con un sondaggio sulla loro visita.
* **Convalida espressioni**: assicurati di controllare e convalidare tutte le espressioni create dalle abilità di Percorso per garantire che vengano utilizzati i campi e i valori corretti.

### Best practice per l’impostazione

* **Definisci obiettivi chiari**: prima di creare percorsi, stabilisci obiettivi chiari (miglioramento della fidelizzazione, conversioni e coinvolgimento).
* **Prepara tipi di pubblico**: assicurati che i tipi di pubblico di destinazione siano già stati creati e correttamente segmentati.
* **Pianifica contenuto messaggio**: definire la strategia di messaggistica prima di creare il percorso.
* **Esperienza cliente**: progettare flussi di percorso che rispettino le preferenze del cliente ed evitino comunicazioni eccessive.

## Creazione di contenuti canale {#channel-content-create}

>[!AVAILABILITY]
>
>Questa funzione è disponibile per tutti i clienti con disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Creazione di contenuti per il canale consente agli utenti di Journey Optimizer di generare, modificare e gestire contenuti specifici per il canale per i percorsi utilizzando la generazione di contenuti basata sull’intelligenza artificiale.

### Casi d’uso principali

* **Generazione di contenuti specifici per il canale**: genera contenuti per e-mail, notifiche push, SMS e altri canali utilizzando prompt in linguaggio naturale.

  &quot;Genera contenuti e-mail per il mio percorso di benvenuto. Crea un’e-mail di benvenuto per i nuovi clienti con un tono amichevole e includi un’offerta di sconto del 10%.&quot;

  &quot;Genera una notifica push per il percorso di visita del negozio. Crea un messaggio di benvenuto che incoraggi i clienti a effettuare il check-in e a ricevere un’offerta speciale.&quot;

  &quot;Genera contenuti SMS per il mio percorso attivato da eventi. Crea un breve messaggio per informare i clienti di una vendita flash con un call-to-action.&quot;

* **Creazione di contenuti basati su modelli**: sfoglia e seleziona tra i modelli disponibili con funzionalità di anteprima.

  &quot;Mostra i modelli e-mail disponibili per il percorso della campagna stagionale&quot;

  &quot;Seleziona un modello per la mia e-mail con una progettazione moderna e pulita.&quot;

* **Gestione dei contenuti multicanale**: genera e gestisci contenuti per più canali all&#39;interno dello stesso flusso di lavoro del percorso.

* **Modifica del contenuto nel contesto**: apri il contenuto generato in Content Designer per la modifica e l&#39;ottimizzazione.

  &quot;Apri il contenuto dell’e-mail in Content Designer per personalizzare la progettazione.&quot;

* **Ottimizzazione e iterazione del contenuto**: rigenera il contenuto con toni o stili diversi utilizzando l&#39;azione Rigenera.

  &quot;Rigenerare il contenuto delle notifiche push con un tono più informale.&quot;

  &quot;Aggiorna il contenuto dell’e-mail per includere un codice promozionale.&quot;

* **Integrazione area di lavoro Percorsi**: selezionare i percorsi dall&#39;inventario e visualizzare i canali associati.

### Best practice per la richiesta di informazioni

* **Specifica**: fornisci dettagli chiari sul tipo di contenuto, il tono, il pubblico di destinazione e i messaggi chiave.
* **Specifica canale**: indica chiaramente per quale canale stai creando contenuti (e-mail, push, SMS).
* **Definisci tono**: specifica il tono desiderato (amichevole, formale, casuale, urgente).
* **Itera e perfeziona**: utilizza l&#39;azione di rigenerazione per perfezionare il contenuto fino a quando non soddisfa i tuoi requisiti.

## Analisi percorso {#journey-analyze}

Grazie alle competenze di percorso, gli utenti di Journey Optimizer potranno analizzare e ottimizzare i percorsi mediante un&#39;interfaccia in linguaggio naturale. Con le abilità di Percorso, i professionisti possono identificare e risolvere rapidamente i conflitti di pianificazione e/o di pubblico, rilevare punti di abbandono degli utenti in un percorso e fornire informazioni approfondite o consigli. Consente ai professionisti di prendere decisioni basate sui dati, migliorare il coinvolgimento dei clienti e semplificare l’orchestrazione del percorso.

>[!AVAILABILITY]
>
>Le abilità di percorso sono disponibili per tutti i clienti che hanno accesso a Collaboratore. Tuttavia, per utilizzare completamente le funzioni Abilità di Percorso sono necessarie le seguenti autorizzazioni:
>
>**Visualizza Percorsi**: questa autorizzazione ti consente di visualizzare approfondimenti sul percorso direttamente in Coworker.
>
>**Gestisci Percorsi**: questa autorizzazione consente di creare nuovi percorsi direttamente in Coworker.
>
>**Visualizza segmenti**: questa autorizzazione ti consente di visualizzare approfondimenti sui tipi di pubblico direttamente in Coworker.
>
>**Gestisci segmenti**: questa autorizzazione ti consente di creare nuovi tipi di pubblico direttamente in Coworker.

### Casi d’uso principali

Analisi percorso offre una serie di funzionalità che possono essere utilizzate per ottimizzare le attività di marketing:

* **Analisi fall-out del percorso**

  * Identifica il punto e il motivo per cui un percoso viene abbandonato dalla clientela.
  * Identifica schemi nel comportamento della clientela che portano a interrompere il coinvolgimento.
  * Utilizza gli insight per perfezionare i progetti di percorso e migliorare la conservazione.

  Prompt di esempio:
  * &quot;Voglio analizzare l’abbandono per nodo per la campagna del 4 luglio percorso.&quot;
  * &quot;Esegui un’analisi dell’abbandono per la campagna del 4 luglio percorso.&quot;
  * &quot;Cos’è la perdita di profilo nel corso della campagna del 4° percorso di luglio?&quot;
  * &quot;Mostra dove gli utenti abbandonano la campagna del 4 luglio percorso.&quot;

* **Analisi della sovrapposizione del pubblico del percorso**

  * Analizza la sovrapposizione del pubblico in diversi percorsi.
  * Evita la stanchezza del pubblico causata da targeting eccessivo.
  * Ottimizza la segmentazione per garantire un coinvolgimento equilibrato.

  Prompt di esempio:
  * &quot;Quali tipi di pubblico vengono utilizzati in più di X percorsi?&quot;
  * &quot;Elenca tutti i percorsi che utilizzano il pubblico [nome pubblico].&quot;
  * &quot;Mostra conflitti di sovrapposizione del pubblico per il percorso [Nome Percorso].&quot;
  * &quot;Mostra tipi di pubblico sovrapposti per il percorso [Nome Percorso] e altri percorsi.&quot;

* **Analisi della sovrapposizione della pianificazione del percorso**

  * Rileva conflitti temporali tra percorsi pianificati destinati allo stesso pubblico.
  * Evita l’eccessiva comunicazione e migliora l’efficienza della pianificazione.
  * Ottimizza l’impatto sul pubblico, garantendo che i percorsi vengano eseguiti nel momento migliore.

  Prompt di esempio:
  * &quot;Sono presenti conflitti di pianificazione per il percorso [Nome Percorso]?&quot;
  * &quot;Verificare la presenza di conflitti di pianificazione che interessano il percorso [Nome Percorso].&quot;
  * &quot;Evidenzia sovrapposizioni di pianificazione tra il percorso [Nome Percorso] e percorsi live.&quot;
  * &quot;Il percorso [Nome Percorso] è in esecuzione in conflitto con altri percorsi?&quot;

* **Insight operativi**

  * Approfondimenti sul Percorso basati su prompt: visualizza informazioni operative sui percorsi, ad esempio &quot;mostrami tutti i percorsi live&quot;.

  Prompt di esempio:
  * &quot;Quando è stato pubblicato [Nome Percorso]?&quot;
  * &quot;Quando è stato interrotto [Nome Percorso]?&quot;
  * &quot;Elenca tutti i percorsi attualmente in modalità di test&quot;
  * &quot;Quanti percorsi di vita ho?&quot;
  * &quot;Dammi un elenco di tutti i percorsi ricorrenti pianificati e dei loro orari di esecuzione previsti.&quot;

* **Analisi degli errori dell&#39;azione personalizzata del Percorso**

  * Identifica quando le azioni personalizzate hanno esito negativo o i tassi di errore si sono impennati all’interno di un percorso.
  * La diagnosi delle cause principali prima che gli errori si trasformino in un&#39;interruzione più ampia del percorso.
  * Utilizza passaggi di correzione specifici per ripristinare rapidamente l’affidabilità delle azioni personalizzate.

  Prompt di esempio:
  * &quot;Perché le azioni personalizzate non riescono nel percorso [Nome Percorso]?&quot;
  * &quot;Qual è il tasso di errore per l&#39;azione personalizzata [Nome azione personalizzata] nel percorso [Nome Percorso]?&quot;
  * &quot;Visualizza la causa principale degli errori delle azioni personalizzate nel percorso [Nome Percorso].&quot;
  * &quot;Esistono errori di azioni personalizzate che interessano il percorso [Nome Percorso] al momento?&quot;

* **Analizzare le anomalie del Percorso**

  * Rileva picchi, cadute o linee piatte imprevisti nei conteggi di entrata, uscita o invio di messaggi di un percorso rispetto alle linee di base storiche, compreso il momento in cui la domanda è formulata attorno al numero di profili che entrano, escono o completano il percorso.
  * Conferma se una modifica segnalata è un’anomalia reale utilizzando un controllo statistico deterministico, anziché affidarsi esclusivamente al flag di anomalia non elaborato.
  * Esegui una diagnostica limitata di sola lettura rispetto ai dati di esecuzione del percorso per identificare una probabile causa principale, evidenziando ciò che ogni controllo ha cercato e trovato insieme al consiglio.
  * Analizza gli avvisi di anomalie che fanno riferimento a una versione e a una marca temporale specifiche del percorso.

  Prompt di esempio:
  * &quot;Perché sono scesi i biglietti per il percorso di benvenuto di ieri?&quot;
  * &quot;Questo percorso di abbandono del carrello ha registrato un picco nelle uscite?&quot;
  * &quot;Sembra basso per il percorso di Promemoria Rinnovamento oggi — cos&#39;è successo?&quot;
  * &quot;Perché c’è stato un calo improvviso nel numero di profili che sono entrati nel percorso di ringraziamento dell’anniversario del mio membro negli ultimi 30 giorni?&quot;
  * &quot;Questo mese, meno profili completeranno il percorso Promemoria per il rinnovo - perché?&quot;
  * &quot;È stato attivato un avviso di anomalia per il percorso [ID versione Percorso] in [timestamp]. Eseguire un&#39;analisi.&quot;

* **Confronto versioni Percorso**

  * Puoi confrontare due versioni di percorso qualsiasi in Chat con collaboratori.
  * Rivedi una differenze strutturata di nodi aggiunti, rimossi, modificati e spostati con dettagli a livello di campo.
  * Identificare le connessioni modificate, le modifiche delle proprietà a livello di percorso e i conteggi di rollup senza aprire Journey Optimizer.

  >[!NOTE]
  >
  >Il confronto a livello di attività dell’azione per il contenuto del canale non è attualmente supportato. Le modifiche al contenuto del canale vengono contrassegnate come **Non verificato** finché questa funzionalità non sarà disponibile.

  Per ulteriori dettagli su come gestire le versioni di percorso, vedere [Versioni di Percorso](publish-journey.md#journey-versions).

  Prompt di esempio:
  * &quot;Confronta le versioni [Versione A] e [Versione B] del percorso [Nome Percorso].&quot;
  * &quot;Cosa è cambiato tra queste due versioni del percorso [Nome Percorso]?&quot;
  * &quot;Visualizza i nodi e le proprietà di percorso che sono cambiate tra le versioni [Versione A] e [Versione B].&quot;

### Best practice per la richiesta di informazioni

Per massimizzare l’efficacia di Analisi Percorso, segui queste best practice:

* **Richieste specifiche**: utilizza prompt chiari e concisi per ottenere insight mirati. Ad esempio, invece di chiedere &quot;Quali sono i miei percorsi?&quot;, specificare &quot;Elenca tutti i percorsi creati nell&#39;ultimo mese&quot;.
* **Combina approfondimenti**: integra gli approfondimenti dalle funzionalità di Audience e Data Insights per una visualizzazione olistica delle prestazioni del percorso.
* **Miglioramento progressivo**: utilizza le analisi di fall-out e sovrapposizione per perfezionare in modo progressivo il progetto e la pianificazione del percorso.

### Best practice per l’impostazione

* **Definisci obiettivi chiari**: prima di analizzare i percorsi, stabilisci obiettivi precisi (per esempio migliorare la conservazione, aumentare le conversioni).
* **Monitora regolarmente**: pianifica revisioni regolari delle prestazioni del percorso per identificare tendenze e anomalie.
* **Ottimizza la segmentazione**: assicurati che la segmentazione del pubblico sia equilibrata, per evitare stanchezza e ottimizzare il coinvolgimento.

## Simulazione del percorso {#journey-simulation}

L’abilità di simulazione di percorso porta la simulazione rapida basata sull’intelligenza artificiale nell’interfaccia di chat, consentendo agli utenti di convalidare la logica di un percorso a livello di conversazione. Tramite Coworker, gli utenti possono generare dati di test simulati, eseguire e gestire una simulazione ed esaminare i risultati.

### Casi d’uso principali

1. **Genera dati di prova simulati**

   * Genera il numero minimo di utenti simulati necessari per esercitare i rami del percorso.
   * Genera dati evento per percorsi attivati da eventi, in modo da attivare ogni ramo.

1. **Esegui e gestisci simulazioni**

   * Avvia un&#39;esecuzione di simulazione.
   * Reimpostare un&#39;esecuzione di simulazione.
   * Controllare lo stato di un&#39;esecuzione di simulazione.
   * Elencare gli utenti simulati inclusi in un&#39;esecuzione.
   * Recupera i registri di esecuzione.

1. **Risultati simulazione revisione**

   * Restituisci risultati dettagliati, incluso l’attraversamento del percorso passo dopo passo.
   * Restituisce i risultati del ramo per l’esecuzione simulata.

### Limitazioni

Questa funzione attualmente supporta solo il flusso di simulazione rapida e non sostituisce completamente l’esperienza di simulazione manuale di Journey Optimizer.

Utilizza la simulazione rapida per un controllo della sanità rapido e automatico della logica di un percorso. Per un controllo granulare su utenti e scenari simulati, utilizzare l&#39;esperienza di simulazione manuale [in Journey Optimizer](simulate-journey-gs.md).

Come parte di questa esperienza di simulazione rapida, gli utenti non possono:

* Scegliere un utente simulato salvato esistente per un&#39;esecuzione.
* Modificare un utente simulato prima di eseguire nuovamente una simulazione.
* Crea, sfoglia, aggiorna o elimina utenti simulati persistenti tramite chat.
* Esegui il targeting di un percorso specifico o di un caso di test personalizzato.


{{$include /help/_includes/do-not-localize/start/ai-augmented-journeys-coworker-skills.md}}
