---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo dei client MCP (Beta)
description: Scopri come collegare Adobe Journey Optimizer ai client MCP utilizzando il server MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
subfeature_v2: []
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 05ad3d2af373c7eeb26bb8c789edfb2c864f5bca
workflow-type: tm+mt
source-wordcount: 1552
ht-degree: 1%

---

# Utilizzo dei client MCP {#ajo-mcp}

>[!BEGINSHADEBOX]

**In questa pagina:** Ottieni una panoramica dettagliata del server MCP [!DNL Adobe Journey Optimizer], dalle nozioni di base di Model Context Protocol e dai client supportati, agli strumenti disponibili, ai prompt di esempio, ai prerequisiti di configurazione, ai passaggi di connessione e alle risposte alle domande comuni.

>[!ENDSHADEBOX]

L&#39;integrazione MCP [!DNL Adobe Journey Optimizer] consente di eseguire query su campagne, percorsi e offerte utilizzando prompt in linguaggio semplice, senza scrivere chiamate API o navigare tra le schermate dei prodotti. Questa pagina spiega come funziona l’integrazione, cosa puoi farci e come iniziare.

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile in **Claude Web**, **Claude Desktop** e **Cursor**. Il supporto per ulteriori applicazioni compatibili con MCP verrà aggiunto nelle prossime versioni.

## Beta, sicurezza e note legali {#mcp-notices}

**Avviso di documentazione di Beta:** questa documentazione riguarda una funzionalità di Beta e non costituisce documentazione finale. Il contenuto qui descritto si riferisce a una versione di Beta ed è soggetto a modifiche prima della disponibilità generale. Adobe non fornisce alcuna dichiarazione sulla completezza o sull’accuratezza di questa documentazione.

Utilizzando Adobe Journey Optimizer MCP Server (Beta) (&quot;Beta&quot;), l&#39;utente riconosce che il Beta è fornito **&quot;così com&#39;è&quot; senza alcuna garanzia**. Adobe non ha alcun obbligo di mantenere, correggere, aggiornare, modificare, modificare o supportare in altro modo Beta. Si consiglia di usare cautela e di non fare affidamento in alcun modo sul corretto funzionamento o sulle prestazioni di tale Beta e/o dei materiali di accompagnamento. Beta è considerata un&#39;informazione riservata di Adobe. Qualsiasi &quot;Feedback&quot; (informazioni relative a Beta, compresi, a titolo esemplificativo e non esaustivo, problemi o difetti riscontrati durante l’utilizzo di Beta, suggerimenti, miglioramenti e raccomandazioni) fornito dall’Utente a Adobe viene assegnato ad Adobe, inclusi tutti i diritti, i titoli e gli interessi relativi a tale Feedback.

>[!WARNING]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione selezionata dal cliente. I clienti sono responsabili della valutazione della sicurezza e dell&#39;idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Qual è il protocollo di contesto del modello? {#mcp-overview}

I team di marketing ed esperienza del cliente si affidano sempre di più ad applicazioni basate su chat e a strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Journey Optimizer] ora fornisce un server MCP che mette in primo piano le operazioni della campagna e della sandbox direttamente all&#39;interno di qualsiasi applicazione compatibile con MCP. Con l&#39;integrazione MCP [!DNL Adobe Journey Optimizer], utenti tipo diversi possono collaborare agli stessi dati di orchestrazione, senza scrivere query sull&#39;API REST [!DNL Adobe Journey Optimizer] o navigare in più schermate dell&#39;interfaccia utente. I clienti possono descrivere il proprio intento conversazionalmente e consentire al LLM di richiamare gli strumenti MCP appropriati.

## Funzionalità principali {#mcp-capabilities}

Il server MCP [!DNL Adobe Journey Optimizer] ti consente di esaminare, riepilogare e risolvere i problemi relativi a campagne, percorsi e offerte direttamente dall&#39;assistente AI. Tutte le operazioni sono **di sola lettura**. Le superfici del server MCP recuperano le API come risposte in linguaggio semplice per consentire di:

* **Comprendere la logica di percorso**: ottieni un riepilogo leggibile dei rami, delle condizioni e delle azioni di qualsiasi percorso.
* **Ottieni visibilità immediata della campagna**: chiedi informazioni sugli stati delle campagne e sulle configurazioni dei canali in linguaggio semplice e ottieni risposte istantaneamente, senza navigare nei menu o richiamare i report manualmente.
* **Problemi spot in anticipo**: campagne interrotte, bozze orfane e problemi di configurazione dei canali nel momento in cui lo chiedi, in modo che il tuo team possa agire rapidamente.
* **Collabora con i dati live**: gli addetti al marketing, i manager delle campagne e le parti interessate possono eseguire query sugli stessi dati live [!DNL Adobe Journey Optimizer] tramite il proprio assistente AI, semplificando l&#39;allineamento, la decisione e lo spostamento.
* **Controlla il tuo portfolio di orchestrazioni**: controlla lo stato completo delle campagne senza analizzare JSON o passare da uno schermo all&#39;altro del prodotto.
* **Verifica i dettagli di configurazione del canale** — Controlla i domini del mittente, le impostazioni di annullamento dell&#39;abbonamento e i pool IP prima di utilizzare una configurazione del canale in un percorso o in una campagna.
* **Conferma criteri di governance** — scopri quali azioni di marketing e criteri di governance sono associati a una configurazione di canale.

## Strumenti disponibili {#mcp-tools}

I seguenti strumenti sono esposti dal server MCP [!DNL Adobe Journey Optimizer]:

**Strumenti per Campaign**

| Strumento | Descrizione |
|---|---|
| **Elenca campagne** | Sfoglia le tue campagne marketing di [!DNL Adobe Journey Optimizer]. Supporta il filtraggio per stato (BOZZA, LIVE, INTERROTTO, COMPLETATO). |
| **Ottieni campagna** | Recupera i dettagli e la configurazione completi per una campagna specifica per ID, incluse le impostazioni di targeting del pubblico, pianificazione, canale e contenuto. |

**Strumenti di Percorso**

| Strumento | Descrizione |
|---|---|
| **Ottieni tutti i Percorsi** | Sfoglia tutti i percorsi nella tua sandbox [!DNL Adobe Journey Optimizer]. |
| **Ottieni Percorso** | Recupera i dettagli completi di un percorso specifico per ID, inclusi rami, condizioni e azioni. |
| **Visualizza i tuoi percorsi** | Esegui il rendering dei percorsi con strumenti interattivi per esplorarne visivamente la struttura e il flusso. |

**Strumenti di configurazione canale**

| Strumento | Descrizione |
|---|---|
| **Elenca configurazioni canale** | Filtra le configurazioni del canale per nome, stato (bozza, attivo, archiviato, disattivato) o tipo di canale, su tutti i canali di AJO: e-mail, messaggio mobile, notifica push, WhatsApp, direct mailing, messaggistica in-app, web, esperienza basata su codice, schede di contenuto, LINE, attività live. |
| **Ottieni configurazione canale** | Recupera i dettagli di configurazione completi per una configurazione di canale specifica, inclusi indirizzi di mittente/risposta, sottodomini, pool IP e impostazioni di annullamento dell’abbonamento. |
| **Elenca risorse configurazione** | Elenca le risorse di supporto a cui fanno riferimento le configurazioni di canale, ad esempio le credenziali push, i sottodomini e-mail, i pool IP, le credenziali SMS, le credenziali WhatsApp, l’indirizzamento direct mail, le impostazioni del canale LINE e il registro delle attività live. |
| **Ottieni risorsa configurazione** | Recupera i dettagli completi di una singola risorsa di configurazione per tipo e ID. |
| **Elencare azioni di marketing** | Elencare le azioni di marketing disponibili per l’applicazione dei criteri di governance dei dati. |

>[!NOTE]
>
>Tutti gli strumenti sono di sola lettura. Le operazioni di scrittura (creazione, aggiornamento o eliminazione di oggetti) non sono supportate nella versione corrente di Beta.

## Casi d’uso {#mcp-use-cases}

Gli esempi seguenti mostrano come interagire con il server MCP [!DNL Adobe Journey Optimizer] utilizzando il linguaggio naturale:

| Obiettivo | Esempio di prompt |
|---|---|
| **Panoramica campagna e percorso** | Mostra tutte le campagne/percorsi Journey Optimizer / Quante campagne/percorsi sono impostati in Journey Optimizer? |
| **Controllo dello stato** | Quali campagne/percorsi sono attualmente live? / Elenca tutte le campagne/percorsi sospesi o interrotti. |
| **Dettagli campagna e percorso** | Ottieni i dettagli completi della campagna [ID] / Visualizza tutti gli elementi configurati nella campagna [ID]. / Ottieni i dettagli completi del percorso [ID] / Visualizza tutte le impostazioni configurate nel percorso [ID]. |
| **Pubblico e targeting** | A quale pubblico è destinata la campagna/percorso [ID]? / Quali regole di idoneità sono impostate sulla campagna/percorso [ID]? |
| **Pianificazione e tempistica** | Quando è pianificata l&#39;esecuzione della campagna [ID]? / La campagna [ID] è una campagna inviata una tantum o ricorrente? |
| **Risoluzione dei problemi** | Perché la campagna [ID] non può essere inviata? / Per eventuali problemi, controlla la configurazione della campagna [ID]. |
| **Configurazione canale** | Quali predefiniti di canale sono disponibili nella sandbox? / Mostra tutte le configurazioni del canale e-mail. / Sono configurate configurazioni WhatsApp? / Quale indirizzo del mittente e risposta-a sono configurati per la configurazione dell’e-mail di marketing? |
| **Controllo del canale** | Quali configurazioni di canale sono mancanti o incomplete? / Quante configurazioni di canale sono disponibili su tutti i canali? |
| **Governance** | Quali azioni di marketing sono disponibili nella sandbox? |

## Prerequisiti {#mcp-prerequisites}

Prima di collegare il server MCP [!DNL Adobe Journey Optimizer] al client MCP, verificare quanto segue:

* Hai una licenza di [!DNL Adobe Journey Optimizer] attiva.
* È possibile accedere a un&#39;applicazione compatibile con MCP supportata (attualmente Claude Web, Claude Desktop o Cursore).
* In [!DNL Adobe Journey Optimizer] si dispone delle autorizzazioni necessarie per visualizzare campagne, percorsi e offerte.

## Connetti il server MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Questa integrazione è in Beta.

È possibile connettere il server MCP [!DNL Adobe Journey Optimizer] tramite il client MCP preferito, inclusi **Claude Web**, **Claude Desktop** e **Cursore**.

**Connetti tramite un client MCP**

Durante la configurazione del server MCP nel client MCP, utilizza il seguente URL dell’endpoint del server:

`https://ajo-mcp.adobe.io/mcp`

**Connessione tramite Claude Web o Claude Desktop**

Per configurare il server MCP in Claude Web o Claude Desktop, passare a **Connettori** e selezionare **Adobe Journey Optimizer**.

## Domande frequenti {#mcp-faq}

+++Quali client MCP sono supportati?

Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile per **Claude Web**, **Claude Desktop** e **Cursor**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
+++

+++A quali [!DNL Adobe Journey Optimizer] oggetti posso accedere tramite MCP?

Puoi accedere a campagne, percorsi, offerte, configurazioni di canale, risorse di configurazione e informazioni sandbox. Le operazioni sono di sola lettura (recupero API); le operazioni di scrittura non sono supportate nella versione corrente.
+++

+++È necessario l&#39;accesso per sviluppatori per utilizzare il server MCP [!DNL Adobe Journey Optimizer]?

No. Il server MCP è progettato sia per utenti tecnici che di marketing. Gli addetti al marketing possono interagire con esso utilizzando prompt in linguaggio naturale in qualsiasi client MCP supportato, mentre gli sviluppatori possono utilizzarlo anche in strumenti per sviluppatori che supportano MCP.
+++

+++I dati vengono inviati al provider client MCP?

Quando si invia una richiesta, il client MCP può inviare il contesto rilevante (inclusi i dati [!DNL Adobe Journey Optimizer] restituiti dal server MCP) al proprio modello per l&#39;elaborazione. Rivedi le politiche sulla privacy e la gestione dei dati del provider client MCP prima di connetterti ai dati di produzione.
+++

+++Di quali autorizzazioni ho bisogno in [!DNL Adobe Journey Optimizer]?

Sono necessarie almeno le autorizzazioni **Visualizza** per gli oggetti di cui si desidera eseguire la query: campagne, percorsi o offerte. Non sono necessarie autorizzazioni di scrittura perché il server MCP esegue solo operazioni di lettura. Contattare l&#39;amministratore [!DNL Adobe Journey Optimizer] in caso di dubbi sul livello di accesso corrente.
+++

+++Posso utilizzare il server MCP in ambienti sandbox?

Sì. Il server MCP rispetta la configurazione sandbox [!DNL Adobe Journey Optimizer]. Puoi eseguire query sui dati specifici della sandbox specificando la sandbox nel prompt o connettendoti con le credenziali con ambito a una particolare sandbox.
+++

