---
solution: Journey Optimizer
product: journey optimizer
title: Competenze Journey Optimizer in CX Coworker
description: Scopri le competenze Adobe Journey Optimizer disponibili in CX Collaborator, con istruzioni approfondite e prompt di esempio.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
source-git-commit: c5460f65413375aac7b76a0651c7ed94b0de6a9d
workflow-type: tm+mt
source-wordcount: '2902'
ht-degree: 8%

---


# Competenze Journey Optimizer in CX Coworker {#ajo-coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri le competenze Adobe Journey Optimizer disponibili in CX Coworker, dalla creazione e analisi di percorsi alla generazione di contenuti per il canale, con istruzioni dettagliate, prompt di esempio e best practice per ogni abilità.

>[!ENDSHADEBOX]

## Panoramica {#overview}

CX Coworker offre funzionalità basate sull&#39;intelligenza artificiale a Adobe Journey Optimizer. [CX Coworker](https://experienceleague.adobe.com/en/docs/cx-enterprise-coworker/content/home){target="_blank"} è l&#39;assistente di Adobe per l&#39;intelligenza artificiale conversazionale che si integra con le applicazioni aziendali per consentirti di lavorare in modo più efficiente.

Grazie alle sue competenze basate sull’intelligenza artificiale, CX Coworker consente agli utenti di Journey Optimizer di creare, analizzare e ottimizzare i percorsi di marketing utilizzando un’interfaccia in linguaggio naturale. Con le competenze di Percorso, i professionisti possono creare rapidamente percorsi, rilevare e risolvere conflitti di pianificazione o di pubblico, analizzare le prestazioni e i punti di abbandono e identificare percorsi dalle prestazioni migliori da replicare per le campagne future. Consente ai professionisti di prendere decisioni basate sui dati, migliorare il coinvolgimento dei clienti e semplificare l’orchestrazione del percorso.

CX Coworker offre diverse competenze per la gestione dei Percorsi e delle sfide legate alla fidelizzazione:

**abilità incentrate sul Percorso:**

* **Creazione Percorso**: crea e configura percorsi di marketing tramite messaggi in linguaggio naturale
* **Creazione di contenuti per il canale**: genera, modifica e gestisci contenuti specifici per il canale (e-mail, push, SMS) per percorsi che utilizzano la generazione di contenuti basati sull&#39;intelligenza artificiale
* **Analisi Percorso**: analisi dei percorsi, rilevamento di problemi, individuazione di informazioni e ottimizzazione delle prestazioni del percorso

**Competenze incentrate sulla fedeltà:**

* **Gestione delle richieste di fidelizzazione**: crea e gestisci le richieste di fidelizzazione utilizzando il linguaggio naturale

<!--
feedback from Ivan: Need to remove Simulate skill from docs until Nico confirms the release timeline.

In addition, **Journey Simulation** is a Journey Optimizer feature that includes [Journey Simulate](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs), an in-product agentic skill, non conversational, with three capabilities: 

* Generating simulated users
* Generating event values
* Quick simulation
-->

## Creazione percorso

La creazione di percorsi consente agli utenti di Journey Optimizer di creare e configurare percorsi di marketing utilizzando un’interfaccia in linguaggio naturale. Con la creazione di Percorsi, i professionisti possono creare rapidamente percorsi descrivendo i loro requisiti nei prompt conversazionali. L’abilità guida gli utenti attraverso le diverse opzioni per la creazione di un percorso, consentendo agli addetti al marketing di concentrarsi sulla strategia anziché sulla configurazione tecnica.

>[!AVAILABILITY]
>
>La funzione Creazione percorso è disponibile per i clienti che fanno parte del programma Agent Orchestrator Explorer. Per utilizzare completamente le funzioni di creazione dei Percorsi sono inoltre necessarie le seguenti autorizzazioni:
>
>**Gestisci Percorsi**: questa autorizzazione consente di creare nuovi percorsi direttamente nell&#39;Assistente IA.
>
>**Visualizza eventi di Percorso, origini dati e azioni**: questa autorizzazione garantisce che l&#39;Assistente AI possa eseguire ricerche tramite eventi di Percorso e azioni personalizzate.
>
>**Visualizza segmenti**: questa autorizzazione garantisce che l&#39;Assistente AI possa eseguire ricerche di segmenti di pubblico durante la creazione di un Percorso.
>
>**Gestisci segmenti**: questa autorizzazione consente di creare nuovi tipi di pubblico direttamente nell&#39;Assistente IA.

### Casi d’uso principali

Percorso Creazione di offerte funzionalità che possono essere utilizzate per accelerare l’esecuzione del marketing:

1. **Creazione percorso attivata da eventi**

   * Creazione di percorsi che si attivano in base a eventi cliente specifici.
   * Progetta risposte automatizzate alle azioni dei clienti in tempo reale.
   * Creare flussi di comunicazione personalizzati in base al comportamento del cliente.

   **percorso di visite al negozio:**
   &quot;Crea un percorso che inizia quando un utente accede alla posizione del mio negozio. Invia una notifica push per accogliere gli utenti nello store. Attendi 2 giorni e controlla se l’utente ha un indirizzo e-mail valido. Se l’utente dispone di un indirizzo e-mail valido, invia un sondaggio e-mail per chiedere informazioni sulla sua esperienza di negozio. Se l’utente non dispone di un indirizzo e-mail valido, invia una notifica push per richiedere la registrazione.&quot;

   **percorso post-acquisto:**
   &quot;Crea un percorso che inizia quando un cliente effettua un acquisto online. Invia una notifica push per ringraziarli dell’acquisto. Quindi, verifica se sono membri fedeltà. Se l’utente è un membro dei premi fedeltà, invia una seconda notifica push con un codice di sconto del 10%. Se l’utente non è un membro dei premi fedeltà, invia un messaggio push per invitarlo a iscriversi al programma fedeltà. Attendi 2 giorni e invia un messaggio push di follow-up con un sondaggio sulla loro esperienza di acquisto.&quot;

   **Promozione basata su eventi:**
   &quot;Crea un percorso attivato quando il punteggio di gioco raggiunge 50. Invia un messaggio SMS ai membri del premio fedeltà che dichiarano di poter usufruire di una fetta gratuita di pizza dallo sponsor partner.&quot;

1. **Creazione di percorsi con targeting di pubblico**

   * Crea percorsi rivolti a segmenti di pubblico specifici.
   * Progettazione di sequenze di comunicazione in più fasi con tempistiche strategiche.

   **Campagna stagionale:**
   &quot;Voglio creare un percorso che si rivolga ad un pubblico di escursionisti. Voglio inviare un messaggio e-mail per avvisare il pubblico della mia prossima vendita di vacanze che include una varietà di elementi essenziali per le escursioni. Attendi 3 giorni dopo l’invio della prima e-mail e invia una seconda e-mail con un coupon del 15% con spedizione gratuita. Attendi 1 settimana e poi invia un terzo messaggio e-mail per mostrare il nostro nuovo sacco a pelo e la collezione di tende. Pianifica il percorso per iniziare il 20/12.&quot;

   **Riconoscimento fedeltà:**
   &quot;Crea un percorso di apprezzamento della fedeltà per i proprietari di SUV, tra cui una notifica push di ringraziamento con un’offerta di carwash gratuita e un promemoria di notifica push di follow-up se la prima notifica non viene interagita entro 1 giorno.&quot;

1. **Creazione percorso attivata da un evento business**

   * Creazione di percorsi che si attivano in base a un particolare evento di business e si rivolgono a un pubblico specifico (ad esempio, il prodotto torna in magazzino o cambia il punteggio di gioco)
   * Messaggi tempestivi e contestuali da attivare quando cambiano le condizioni di business.

1. **Creazione del percorso di qualificazione del pubblico**

   * Crea percorsi che si attivano quando i profili entrano o escono da una definizione di segmento di pubblico.
   * Automatizza la messaggistica di entrata e uscita per supportare gli obiettivi di onboarding, conservazione e riconquista.

1. **Flussi percorso condizionale**

   * Crea rami decisionali in base agli attributi del cliente.
   * Progetta percorsi suddivisi in base alle preferenze del cliente.

1. **Crea percorso da immagine**

   * Carica un’immagine di riferimento in un collega e chiedi di creare un percorso utilizzando l’immagine come riferimento
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

1. **Specifica**: fornisci dettagli chiari sugli obiettivi del percorso, sul pubblico di destinazione e sulle azioni desiderate. Includi informazioni su canali, tempi e condizioni.
1. **Specificare l&#39;intervallo**: indicare chiaramente i periodi di attesa tra le azioni e l&#39;inizio del percorso.
1. **Definisci condizioni**: quando utilizzi la logica condizionale, spiega i criteri per ciascun percorso di diramazione.
1. **Includi canali**: specifica i canali di comunicazione da utilizzare (push, e-mail, SMS).
1. **Pianificazione menzione**: per i percorsi pianificati, fornisci la data e l&#39;ora di inizio desiderate.
1. **Azioni personalizzate**: se utilizzi azioni personalizzate nel flusso di lavoro, devi specificare che utilizzi un&#39;azione personalizzata insieme al nome esatto dell&#39;azione personalizzata. Esempio:
Quando un utente accede alla posizione del mio archivio, invia un messaggio di benvenuto utilizzando l’azione personalizzata ExternalPush. Attendi 2 giorni e invia un messaggio di follow-up utilizzando l’azione personalizzata ExternalEmail con un sondaggio sulla loro visita.
1. **Convalida espressioni**: assicurati di controllare e convalidare tutte le espressioni create dalle abilità di Percorso per garantire che vengano utilizzati i campi e i valori corretti.

### Best practice per l’impostazione

* **Definisci obiettivi chiari**: prima di creare percorsi, stabilisci obiettivi chiari (miglioramento della fidelizzazione, conversioni e coinvolgimento).
* **Prepara tipi di pubblico**: assicurati che i tipi di pubblico di destinazione siano già stati creati e correttamente segmentati.
* **Pianifica contenuto messaggio**: definire la strategia di messaggistica prima di creare il percorso.
* **Esperienza cliente**: progettare flussi di percorso che rispettino le preferenze del cliente ed evitino comunicazioni eccessive.

## Creazione di contenuti canale

<!--Ivan : Need to speak with Amar on new options for content generation as this skill has changed. -->

>[!AVAILABILITY]
>
>Questa funzione è disponibile per tutti i clienti con disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Creazione di contenuti per il canale consente agli utenti di Journey Optimizer di generare, modificare e gestire contenuti specifici per il canale per i percorsi utilizzando la generazione di contenuti basata sull’intelligenza artificiale.

### Casi d’uso principali

1. **Generazione di contenuti specifici per il canale**: genera contenuti per e-mail, notifiche push, SMS e altri canali utilizzando prompt in linguaggio naturale.

   &quot;Genera contenuti e-mail per il mio percorso di benvenuto. Crea un’e-mail di benvenuto per i nuovi clienti con un tono amichevole e includi un’offerta di sconto del 10%.&quot;

   &quot;Genera una notifica push per il percorso di visita del negozio. Crea un messaggio di benvenuto che incoraggi i clienti a effettuare il check-in e a ricevere un’offerta speciale.&quot;

   &quot;Genera contenuti SMS per il mio percorso attivato da eventi. Crea un breve messaggio per informare i clienti di una vendita flash con un call-to-action.&quot;

1. **Creazione di contenuti basati su modelli**: sfoglia e seleziona tra i modelli disponibili con funzionalità di anteprima.

   &quot;Mostra i modelli e-mail disponibili per il percorso della campagna stagionale&quot;

   &quot;Seleziona un modello per la mia e-mail con una progettazione moderna e pulita.&quot;

1. **Gestione dei contenuti multicanale**: genera e gestisci contenuti per più canali all&#39;interno dello stesso flusso di lavoro del percorso.

1. **Modifica del contenuto nel contesto**: apri il contenuto generato in Content Designer per la modifica e l&#39;ottimizzazione.

   &quot;Apri il contenuto dell’e-mail in Content Designer per personalizzare la progettazione.&quot;

1. **Ottimizzazione e iterazione del contenuto**: rigenera il contenuto con toni o stili diversi utilizzando l&#39;azione Rigenera.

   &quot;Rigenerare il contenuto delle notifiche push con un tono più informale.&quot;

   &quot;Aggiorna il contenuto dell’e-mail per includere un codice promozionale.&quot;

1. **Integrazione area di lavoro Percorsi**: selezionare i percorsi dall&#39;inventario e visualizzare i canali associati.

### Competenze in ambito

Le seguenti funzionalità sono supportate da Creazione di contenuti canale:

* **Generazione di contenuti basati sull&#39;intelligenza artificiale**: genera contenuti per e-mail, push, SMS e altri canali utilizzando prompt in linguaggio naturale.
* **Gestione modelli**: sfoglia e seleziona tra i modelli disponibili con funzionalità di anteprima.
* **Modifica nel contesto**: apri i contenuti generati in Content Designer per modificarli e perfezionarli.
* **Rigenerazione contenuto**: rigenera contenuto con toni, stili o messaggi diversi utilizzando l&#39;azione Rigenera.
* **Supporto multicanale**: genera e gestisci contenuti per più canali all&#39;interno dello stesso flusso di lavoro del percorso.
* **Accesso inventario Percorsi**: seleziona i percorsi dall&#39;inventario e visualizza i canali associati.

### Competenze al di fuori dell’ambito

Attualmente, le seguenti funzonalità non sono supportate:

* **Allineamento marchio e controlli di qualità dei contenuti**
* **Inserire nodi di contenuto direttamente nell&#39;area di lavoro del percorso**
* **Importazione modello**

### Best practice per la richiesta di informazioni

1. **Specifica**: fornisci dettagli chiari sul tipo di contenuto, il tono, il pubblico di destinazione e i messaggi chiave.
1. **Specifica canale**: indica chiaramente per quale canale stai creando contenuti (e-mail, push, SMS).
1. **Definisci tono**: specifica il tono desiderato (amichevole, formale, casuale, urgente).
1. **Itera e perfeziona**: utilizza l&#39;azione di rigenerazione per perfezionare il contenuto fino a quando non soddisfa i tuoi requisiti.

## Gestione delle sfide di fedeltà

>[!AVAILABILITY]
>
>Le competenze in materia di fidelizzazione sono disponibili in CX Collaborator per le organizzazioni idonee. I clienti con una licenza di fedeltà possono accedere a queste competenze, anche se non dispongono di una licenza CX aggiuntiva per il cliente.

Loyalty Challenge Management consente agli utenti di Journey Optimizer di creare e gestire le sfide di fidelizzazione in CX Coworker utilizzando messaggi in linguaggio naturale. Per la documentazione completa sulla creazione, la configurazione e la gestione delle sfide di fidelizzazione, incluse istruzioni di configurazione dettagliate, consulta la [guida sulle sfide di fidelizzazione](../loyalty-challenges/get-started.md).

### Casi d’uso principali

1. **Problema di onboarding in più passaggi**

   &quot;Crea una sfida denominata &quot;New Account Kickstart&quot; per i nuovi clienti iscritti che richiede di completare questi passaggi per: aprire un conto corrente, finanziarlo con almeno 500 $ e scaricare l’app mobile. Quando tutti i passaggi sono completati, premiali con 5.000 punti bonus. Esegui dal 1° settembre al 31 ottobre, fuso orario orientale.&quot;

1. **Richiesta soglia attività cumulativa**

   &quot;Crea una sfida denominata &quot;Spendi e guadagna l&#39;estate&quot; per i titolari di carte in cui i membri ottengono un credito di 50 $ una volta spesi 1.500 $ sulla loro carta di credito durante il terzo trimestre. Iniziate il 1 luglio, fuso orario orientale.&quot;

1. **Sfida per sequenza di frequenza**

   &quot;Crea una sfida denominata &quot;Frequent Flyer Sprint&quot; per i membri del livello elite che richiede 3 voli al mese per due mesi consecutivi. Premiare il completamento con un&#39;estensione di livello e 10.000 miglia bonus. Inizia il primo del prossimo mese, fuso orario del Pacifico.&quot;

1. **Sfida singola azione qualificata**

   &quot;Imposta una sfida denominata &quot;Go Paperless&quot; che premia gli abbonati pagati con 500 punti bonus dopo che si sono iscritti al pagamento automatico e sono passati alla fatturazione senza carta entro 30 giorni. Inizia il primo del prossimo mese, fuso orario centrale.&quot;

1. **Obiettivo di coinvolgimento/consumo**

   &quot;Creare una sfida denominata &quot;Badge Explorer&quot; per i membri che richiede di completare 5 attività in almeno 3 diverse categorie durante il mese di agosto. Premiali con 1.000 punti e un distintivo &quot;Explorer&quot; al termine. Inizia il 1° agosto, fuso orario Mountain.&quot;

1. **Azione giornaliera**

   &quot;Aiutatemi a creare una sfida per gli amanti del matcha che richiede loro di venire in negozio ogni giorno questa settimana e comprare un drink matcha. La loro ricompensa dovrebbe essere di 200 punti in più se completano la sfida. Chiamalo &quot;Mad about Matcha&quot;, usa SKU matcha-001, avvialo Lunedì prossima settimana, fuso orario orientale.&quot;

### Competenze in ambito

Le seguenti funzionalità sono supportate da Loyalty Challenge Management:

* **Creazione di una sfida**: crea la configurazione della sfida dal linguaggio naturale (pubblico, criteri di azione, tempistica, ricompensa, denominazione).
* **Aggiornamenti verifica**: modifica i dettagli della verifica tramite prompt iterativi.
* **Pubblicazione della richiesta di verifica**: pubblica le configurazioni di richiesta di verifica supportate direttamente dalla conversazione.
* **Visibilità del contesto di verifica**: recupera e rivedi le informazioni sulla verifica durante l&#39;iterazione.

### Competenze al di fuori dell’ambito

Attualmente, le seguenti funzonalità non sono supportate:

* Eliminazione della sfida
* Informazioni sulla fedeltà e competenze per i consigli
* Automazione completa dell’authoring dei contenuti per i messaggi di sfida in tutti i casi

### Best practice per la richiesta di informazioni

1. **Assegna un nome**: assegna alla sfida un titolo chiaro e facile da ricordare tra virgolette.
1. **Specifica il pubblico**: chi è idoneo (ad esempio, tutti i membri, un livello, un segmento, nuovi iscritti, titolari di carte, abbonati).
1. **Definire l&#39;azione e la quantità**: ciò che i membri devono fare e la frequenza, la soglia o la sequenza che conta come completamento.
1. **Impostare l&#39;intervallo di tempo**: una data di inizio (e una data di fine se di durata fissa) più il fuso orario.
1. **Dichiara il premio**: punti, miglia, crediti di rendiconto, estensioni di stato, voucher o privilegi concessi al completamento.
1. **Riferimento all&#39;evento qualificante**: puntare allo SKU specifico, al prodotto, all&#39;azione dell&#39;account o all&#39;evento di coinvolgimento tracciato dalla sfida.

## Analisi percorso

Grazie alle competenze di percorso, gli utenti di Journey Optimizer potranno analizzare e ottimizzare i percorsi mediante un&#39;interfaccia in linguaggio naturale. Con le abilità di Percorso, i professionisti possono identificare e risolvere rapidamente i conflitti di pianificazione e/o di pubblico, rilevare punti di abbandono degli utenti in un percorso e fornire informazioni approfondite o consigli. Consente ai professionisti di prendere decisioni basate sui dati, migliorare il coinvolgimento dei clienti e semplificare l’orchestrazione del percorso.

Per ulteriori informazioni e per scoprire subito l&#39;agente, consulta questa [panoramica](https://experienceleague.adobe.com/en/slides/journey-agent-overview).

>[!AVAILABILITY]
>
>Le abilità di percorso sono disponibili per tutti i clienti che hanno accesso all’Assistente all’intelligenza artificiale. Tuttavia, per utilizzare completamente le funzioni Abilità di Percorso sono necessarie le seguenti autorizzazioni:
>
>**Visualizza Percorsi**: questa autorizzazione ti consente di visualizzare approfondimenti sul percorso direttamente nell&#39;Assistente AI.
>
>**Gestisci Percorsi**: con autorizzazione consente di creare nuovi percorsi direttamente nell&#39;Assistente IA.
>
>**Visualizza segmenti**: questa autorizzazione ti consente di visualizzare approfondimenti sui tipi di pubblico direttamente nell&#39;Assistente AI.
>
>**Gestisci segmenti**: questa autorizzazione consente di creare nuovi tipi di pubblico direttamente nell&#39;Assistente IA.

### Casi d’uso principali

Analisi percorso offre una serie di funzionalità che possono essere utilizzate per ottimizzare le attività di marketing:

1. **Analisi fall-out del percorso**

   * Identifica il punto e il motivo per cui un percoso viene abbandonato dalla clientela.
   * Identifica schemi nel comportamento della clientela che portano a interrompere il coinvolgimento.
   * Utilizza gli insight per perfezionare i progetti di percorso e migliorare la conservazione.

   Prompt di esempio:
   * &quot;Voglio analizzare l’abbandono per nodo per la campagna del 4 luglio percorso.&quot;
   * &quot;Esegui un’analisi dell’abbandono per la campagna del 4 luglio percorso.&quot;
   * &quot;Cos’è la perdita di profilo nel corso della campagna del 4° percorso di luglio?&quot;
   * &quot;Mostra dove gli utenti abbandonano la campagna del 4 luglio percorso.&quot;

1. **Analisi della sovrapposizione del pubblico del percorso**

   * Analizza la sovrapposizione del pubblico in diversi percorsi.
   * Evita la stanchezza del pubblico causata da targeting eccessivo.
   * Ottimizza la segmentazione per garantire un coinvolgimento equilibrato.

   Prompt di esempio:
   * &quot;Quali tipi di pubblico vengono utilizzati in più di X percorsi?&quot;
   * &quot;Elenca tutti i percorsi che utilizzano il pubblico [nome pubblico].&quot;
   * &quot;Mostra conflitti di sovrapposizione del pubblico per il percorso [Nome Percorso].&quot;
   * &quot;Mostra tipi di pubblico sovrapposti per il percorso [Nome Percorso] e altri percorsi.&quot;

1. **Analisi della sovrapposizione della pianificazione del percorso**

   * Rileva conflitti temporali tra percorsi pianificati destinati allo stesso pubblico.
   * Evita l’eccessiva comunicazione e migliora l’efficienza della pianificazione.
   * Ottimizza l’impatto sul pubblico, garantendo che i percorsi vengano eseguiti nel momento migliore.

   Prompt di esempio:
   * &quot;Sono presenti conflitti di pianificazione per il percorso [Nome Percorso]?&quot;
   * &quot;Verificare la presenza di conflitti di pianificazione che interessano il percorso [Nome Percorso].&quot;
   * &quot;Evidenzia sovrapposizioni di pianificazione tra il percorso [Nome Percorso] e percorsi live.&quot;
   * &quot;Il percorso [Nome Percorso] è in esecuzione in conflitto con altri percorsi?&quot;

1. **Insight operativi**

   * Approfondimenti sul Percorso basati su prompt: visualizza informazioni operative sui percorsi, ad esempio &quot;mostrami tutti i percorsi live&quot;.

   Prompt di esempio:
   * &quot;Quando è stato pubblicato [Nome Percorso]?&quot;
   * &quot;Quando è stato interrotto [Nome Percorso]?&quot;
   * &quot;Elenca tutti i percorsi attualmente in modalità di test&quot;
   * &quot;Quanti percorsi di vita ho?&quot;
   * &quot;Dammi un elenco di tutti i percorsi ricorrenti pianificati e dei loro orari di esecuzione previsti.&quot;

## Competenze in ambito

Le seguenti funzionalità sono supportate da Analisi Percorso:

* **Query reattive**: consentono agli utenti di porre domande specifiche riguardanti le prestazioni del percorso, l’utilizzo del pubblico e i conflitti di pianificazione.
* **Integrazione con altri agenti**: collabora con Agente Audience e Agente Data Insights per analisi più approfondite.
* **Struttura della risposta dell&#39;agente**: ragionamento (spiegazione della logica), riepilogo dell&#39;analisi (evidenziazione dei punti chiave), dettagli del problema (descrizione del problema) e consiglio (proposta dei passaggi successivi).

### Competenze al di fuori dell’ambito

Attualmente, le seguenti funzonalità non sono supportate:

* **Creazione automatizzata del percorso**
* **Rilevamento di anomalie in tempo reale**
* **Sovrapposizione di canali**
* **Analisi dell’ingresso nel percorso**
* **Analisi di un problema tecnico**
* **Analisi della stanchezza**

### Prompt per le best practice

Per massimizzare l’efficacia di Analisi Percorso, segui queste best practice:

1. **Richieste specifiche**: utilizza prompt chiari e concisi per ottenere insight mirati. Ad esempio, invece di chiedere &quot;Quali sono i miei percorsi?&quot;, specificare &quot;Elenca tutti i percorsi creati nell&#39;ultimo mese&quot;.
1. **Combina gli insights**: integra gli insight di Agente Audience e Agente Data Insights per una vista olistica delle prestazioni del percorso.
1. **Miglioramento progressivo**: utilizza le analisi di fall-out e sovrapposizione per perfezionare in modo progressivo il progetto e la pianificazione del percorso.

### Impostare le best practice

* **Definisci obiettivi chiari**: prima di analizzare i percorsi, stabilisci obiettivi precisi (per esempio migliorare la conservazione, aumentare le conversioni).
* **Monitora regolarmente**: pianifica revisioni regolari delle prestazioni del percorso per identificare tendenze e anomalie.
* **Ottimizza la segmentazione**: assicurati che la segmentazione del pubblico sia equilibrata, per evitare stanchezza e ottimizzare il coinvolgimento.

<!--
Journey analysis new skills to document:

Journey Custom Action Error Analysis
- Identify when custom actions are failing or error rates spike within a journey.
- Diagnose root causes before failures cascade into broader journey disruption.
- Use specific remediation steps to restore custom action reliability quickly.

Journey Anomaly Detection
- Detect unexpected spikes or drops in journey sends and exits against historical baselines.
- Catch send or exit volume issues early, before they affect a large share of your audience.
- Use the insights to pinpoint the root cause and keep the journey performing as expected.
-->

<!--
Feedback from Ivan: Journey simulate is not ready as a skill

## Journey Simulate: Use Cases, Agentic Skills and User Guide

## Overview

>[!BEGINSHADEBOX]

Journey Simulation is available to all Journey Optimizer customers. Journey Simulate, the in-product agentic skill within Journey Simulation, is available to customers that are a part of the Agent Orchestrator Explorer program and requires at least one of the following permissions:

* **Simulate journeys**: Run simulation workflows from the journey canvas.

* **Publish journeys**: Publish journeys, including flows that use simulation before go-live.

* **Approve and Publish journeys**: Approve and publish journeys when your organization uses approval workflows.

To use AI in **[!UICONTROL Simulation]** (**[!UICONTROL Quick simulation]**, generating simulated users with AI, **[!UICONTROL Generate event values]**), users require **[!UICONTROL Generate Content]** permission from the **[!UICONTROL AI Assistant]** capability. 

[Learn more about permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/administration/permissions).

>[!ENDSHADEBOX]

Journey Simulation is a Journey Optimizer feature that enables Journey Optimizer users to safely test and validate marketing journeys before activation. Within Journey Simulation, Journey Simulate is an in-product agentic skill, not a conversational one, that automates and assists the testing process directly from the journey canvas.

Journey Simulate includes three capabilities:

* Generating simulated users
* Generating event values
* Quick simulation. 

Together, they bridge the gap between journey creation and activation, building confidence in journey logic and reducing the risk of post-launch errors.

## Use cases

### Key use cases for Journey Simulate

Journey Simulate offers three capabilities that can be leveraged to reduce testing time and improve journey quality before go-live:

**Generating simulated users**

* Generate simulated users automatically based on journey paths and required attributes.
* Create simulated users that cover all branches and conditions in a journey, including execution addresses (email, push, SMS).
* Update simulated user attributes on demand to refine test scenarios.
* Ensure all journey branches are covered by assigning the right simulated user to each path.

**Generating event values**

* Generate values for events used in a journey to drive test execution through specific paths.
* Define event attribute values that trigger the desired conditions and branches during simulation.

**Quick simulation**

* Start journey simulation and trigger test executions for all simulated users needed to test all paths of a journey, in a single interaction.
* Visualize how simulated users flow through a journey, step by step, including branching paths and conditional logic.
* Identify which simulated user flows through which path, and why, with detailed node-by-node traversal.
* Review simulation reporting at the end of a run in the Journey Optimizer UI to validate outcomes before activation.

## In scope skills and limitations

### **In scope**

The following capabilities are supported by the Journey Simulation feature:

* **Simulated user management**: View, edit, and update simulated user attributes, including execution addresses and personalization data.
* **Simulation control**: Start and stop journey simulation directly through the Journey Simulation in-product experience.
* **Test execution**: Trigger test executions for one or multiple simulated users.
* **Journey flow visualization**: View step-by-step traversal of simulated users through journey nodes, including branching, splits, and user status.
* **Simulation reporting**: View reporting at the end of a simulation run in the Journey Optimizer UI.
* **Multi-user testing**: Run and visualize tests for multiple simulated users simultaneously, covering all journey branches.

In addition to this, the following capabilities are supported by the Journey Simulate skill:

* **Simulated user generation**: Create simulated users based on journey paths, existing test profiles, or specified attributes.
* **Event value generation**: Generate and assign event attribute values to drive test execution through specific journey paths.
* **Quick simulation**: Run a full end-to-end simulation with minimal intervention. The skill automatically generates simulated users, event values, and pre-filled test settings, then executes the journey and surfaces results for review.

### **Limitations**

Simulation may not support every activity, channel, or integration that Test mode or a live journey supports, and behavior may change as the capability matures.

➡️ Learn more about [Simulation limitations](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs#limitations) in the Journey Optimizer documentation.

-->
