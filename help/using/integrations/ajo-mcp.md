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
hide: true
source-git-commit: 4b56f4531d169e224f92fd08e6e2d03f7b1365a7
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 1%

---

# Utilizzo dei client MCP (Beta) {#ajo-mcp}

>[!CAUTION]
>
>**Avviso di documentazione di Beta:** questa documentazione riguarda una funzionalità di Beta e non costituisce documentazione finale. Il contenuto qui descritto si riferisce a una versione di Beta ed è soggetto a modifiche prima della disponibilità generale. Adobe non fornisce alcuna dichiarazione sulla completezza o sull’accuratezza di questa documentazione.
>
>© Adobe Inc. Tutti i diritti riservati. Adobe, il logo Adobe e Adobe Journey Optimizer sono marchi o marchi registrati di Adobe negli Stati Uniti e/o in altri paesi.
>
>Utilizzando Adobe Journey Optimizer MCP Server (Beta) (&quot;Beta&quot;), l&#39;utente riconosce che il Beta è fornito **&quot;così com&#39;è&quot; senza alcuna garanzia**. Adobe non ha alcun obbligo di mantenere, correggere, aggiornare, modificare, modificare o supportare in altro modo Beta. Si consiglia di usare cautela e di non fare affidamento in alcun modo sul corretto funzionamento o sulle prestazioni di tale Beta e/o dei materiali di accompagnamento. Beta è considerata un&#39;informazione riservata di Adobe. Qualsiasi &quot;Feedback&quot; (informazioni relative a Beta, compresi, a titolo esemplificativo e non esaustivo, problemi o difetti riscontrati durante l’utilizzo di Beta, suggerimenti, miglioramenti e raccomandazioni) fornito dall’Utente a Adobe viene assegnato ad Adobe, inclusi tutti i diritti, i titoli e gli interessi relativi a tale Feedback.

L&#39;integrazione MCP [!DNL Adobe Journey Optimizer] consente di eseguire query su campagne e offerte utilizzando prompt in linguaggio semplice, senza scrivere chiamate API o navigare tra le schermate dei prodotti. Questa pagina spiega come funziona l’integrazione, cosa puoi farci e come iniziare.

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile solo in **Claude Web** e **Claude Desktop**. Il supporto per ulteriori applicazioni compatibili con MCP verrà aggiunto nelle prossime versioni.

## Qual è il protocollo di contesto del modello? {#mcp-overview}

I team di marketing ed esperienza del cliente si affidano sempre di più ad applicazioni basate su chat e a strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Journey Optimizer] ora fornisce un server MCP che riunisce le operazioni di campagna, fidelizzazione e sandbox direttamente in qualsiasi applicazione compatibile con MCP. Con l&#39;integrazione MCP [!DNL Adobe Journey Optimizer], utenti tipo diversi possono collaborare agli stessi dati di orchestrazione, senza scrivere query sull&#39;API REST [!DNL Adobe Journey Optimizer] o navigare in più schermate dell&#39;interfaccia utente. I clienti possono descrivere il proprio intento conversazionalmente e consentire al LLM di richiamare gli strumenti MCP appropriati.

## Funzionalità principali {#mcp-capabilities}

Il server MCP [!DNL Adobe Journey Optimizer] ti consente di esaminare, riepilogare e risolvere i problemi relativi a campagne e offerte direttamente dall&#39;assistente AI. Tutte le operazioni sono **di sola lettura**. Le superfici del server MCP recuperano le API come risposte in linguaggio semplice per consentire di:

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **Ottieni visibilità immediata della campagna**: chiedi informazioni sugli stati delle campagne e sulle configurazioni dei canali in linguaggio semplice e ottieni risposte istantaneamente, senza navigare nei menu o richiamare i report manualmente.
* **Problemi spot in anticipo**: campagne interrotte, bozze orfane e problemi di configurazione dei canali nel momento in cui lo chiedi, in modo che il tuo team possa agire rapidamente.
* **Collabora con i dati live**: gli addetti al marketing, i manager delle campagne e le parti interessate possono eseguire query sugli stessi dati live [!DNL Adobe Journey Optimizer] tramite il proprio assistente AI, semplificando l&#39;allineamento, la decisione e lo spostamento.
* **Controlla il tuo portfolio di orchestrazioni**: controlla lo stato completo delle campagne senza analizzare JSON o passare da uno schermo all&#39;altro del prodotto.

## Strumenti disponibili {#mcp-tools}

I seguenti strumenti sono esposti dal server MCP [!DNL Adobe Journey Optimizer]:

| Strumento | Descrizione |
|---|---|
| **Elenca campagne** | Sfoglia le tue campagne marketing di [!DNL Adobe Journey Optimizer]. Supporta il filtraggio per stato (BOZZA, LIVE, INTERROTTO, COMPLETATO). |
| **Ottieni campagna** | Recupera i dettagli e la configurazione completi per una campagna specifica per ID, incluse le impostazioni di targeting del pubblico, pianificazione, canale e contenuto. |
| **Elenca configurazioni canale** | Visualizza i predefiniti di superficie e le impostazioni di branding per i canali e-mail, SMS, push o WhatsApp. |

>[!NOTE]
>
>Tutti gli strumenti sono di sola lettura. Le operazioni di scrittura (creazione, aggiornamento o eliminazione di oggetti) non sono supportate nella versione corrente di Beta.

## Casi d’uso {#mcp-use-cases}

Gli esempi seguenti mostrano come interagire con il server MCP [!DNL Adobe Journey Optimizer] utilizzando il linguaggio naturale:

| Obiettivo | Esempio di prompt |
|---|---|
| **Panoramica campagna** | &quot;Mostra tutte le mie campagne AJO&quot; / &quot;Quante campagne sono impostate in AJO?&quot; |
| **Controllo dello stato** | &quot;Quali campagne sono attualmente live?&quot; / &quot;Elenca tutte le campagne in pausa o interrotte.&quot; |
| **Dettagli campagna** | &quot;Ottieni i dettagli completi della campagna [ID]&quot; / &quot;Visualizza tutte le impostazioni configurate nella campagna [ID].&quot; |
| **Pubblico e targeting** | &quot;A quale pubblico è destinata la campagna [ID]?&quot; / &quot;Quali regole di idoneità sono impostate per la campagna [ID]?&quot; |
| **Pianificazione e tempistica** | &quot;Quando è pianificata l&#39;esecuzione della campagna [ID]?&quot; / &quot;La campagna [ID] è una campagna inviata una tantum o ricorrente?&quot; |
| **Risoluzione dei problemi** | &quot;Perché la campagna [ID] non può essere inviata?&quot; / &quot;Rivedi la configurazione della campagna [ID] per eventuali problemi.&quot; |
| **Configurazione del canale** | &quot;Quali predefiniti di canale sono disponibili nella sandbox?&quot; / &quot;Mostra tutte le configurazioni del canale e-mail&quot;. |
| **Controllo del canale** | &quot;Quali configurazioni di canale sono mancanti o incomplete?&quot; / &quot;Quante configurazioni di canale ho su tutti i canali?&quot; |

## Prerequisiti {#mcp-prerequisites}

Prima di collegare il server MCP [!DNL Adobe Journey Optimizer] al client MCP, verificare quanto segue:

* Hai una licenza di [!DNL Adobe Journey Optimizer] attiva.
* È possibile accedere a un&#39;applicazione compatibile con MCP supportata (attualmente Claude Web o Claude Desktop).
* In [!DNL Adobe Journey Optimizer] si dispone delle autorizzazioni necessarie per visualizzare campagne e offerte.

## Connetti il server MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Questa integrazione è in Beta. I passaggi di configurazione dettagliati verranno pubblicati quando si raggiunge la disponibilità generale. Contatta il rappresentante Adobe per richiedere l’accesso anticipato e ricevere le istruzioni di configurazione.

Durante la fase Beta, il rappresentante Adobe fornirà:

* L’URL dell’endpoint del server MCP specifico per la tua organizzazione.
* Credenziali di autenticazione per la connessione dell&#39;assistente AI a [!DNL Adobe Journey Optimizer].
* Linee guida per la configurazione del server MCP in Claude Desktop o Claude Web.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Limitazioni note (Beta) {#mcp-limitations}

Le seguenti limitazioni si applicano alla versione corrente di Beta del server MCP [!DNL Adobe Journey Optimizer]:

| Limitazione | Descrizione | Soluzione alternativa |
|---|---|---|
| **Nessun coinvolgimento o metrica delle prestazioni** | Il server MCP non espone dati di reporting. Gli strumenti non restituiscono impression, tassi di click-through, conversioni o stati di consegna. | Utilizza l’interfaccia utente di AJO per la generazione di rapporti, CJA MCP o Adobe Analytics MCP per le metriche. AEP Query Service può eseguire query sui dati dell’evento non elaborati utilizzando l’ID di esecuzione della campagna. |
| **La paginazione dell&#39;elenco delle campagne è limitata** | `List Campaigns` restituisce sempre la prima pagina dei risultati (fino a 50 campagne, ordinate alfabeticamente). I valori di offset e limite non vengono applicati, rendendo l’enumerazione completa poco pratica per le sandbox di grandi dimensioni. | Utilizza `Get Campaign` direttamente se l&#39;ID o il nome della campagna è noto. Utilizza l’interfaccia utente di AJO per sfogliare e filtrare l’elenco completo. |
| **Nessun filtro lato server per data, canale o pianificazione** | `List Campaigns` supporta solo il filtro per stato. Il filtro per data di pubblicazione, data di pianificazione, canale o tipo di campagna non è disponibile sul lato server. | Utilizza l’elenco delle campagne dell’interfaccia utente di AJO, che supporta il filtro nativo di data e canale. |
| **Impossibile recuperare il contenuto del messaggio** | Lo strumento per il contenuto dei messaggi restituisce HTTP 502 per tutti i tipi di canale (e-mail, basati su codice e altri). Non è possibile recuperare tramite MCP il HTML dei messaggi, le righe dell’oggetto, i token di personalizzazione e il contenuto dell’offerta. | Visualizza il contenuto del messaggio e i token di personalizzazione direttamente nell&#39;interfaccia utente di AJO in **Campagne > [Campagna] > Contenuto**. |

## Domande frequenti {#mcp-faq}

+++Quali client MCP sono supportati?

Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile per **Claude Web** e **Claude Desktop**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
+++

+++A quali [!DNL Adobe Journey Optimizer] oggetti posso accedere tramite MCP?

Puoi accedere a campagne, offerte, dati fedeltà e informazioni sandbox. Le operazioni sono di sola lettura (recupero API); le operazioni di scrittura non sono supportate nella versione corrente.
+++

+++È necessario l&#39;accesso per sviluppatori per utilizzare il server MCP [!DNL Adobe Journey Optimizer]?

No. Il server MCP è progettato sia per utenti tecnici che di marketing. Gli addetti al marketing possono interagire con esso utilizzando prompt in linguaggio naturale in qualsiasi client MCP supportato, mentre gli sviluppatori possono utilizzarlo anche in strumenti per sviluppatori che supportano MCP.
+++

+++I dati vengono inviati al provider client MCP?

Quando si invia una richiesta, il client MCP può inviare il contesto rilevante (inclusi i dati [!DNL Adobe Journey Optimizer] restituiti dal server MCP) al proprio modello per l&#39;elaborazione. Rivedi le politiche sulla privacy e la gestione dei dati del provider client MCP prima di connetterti ai dati di produzione.
+++

+++Di quali autorizzazioni ho bisogno in [!DNL Adobe Journey Optimizer]?

Sono necessarie almeno le autorizzazioni **Visualizza** per gli oggetti di cui si desidera eseguire la query, campagne o offerte. Non sono necessarie autorizzazioni di scrittura perché il server MCP esegue solo operazioni di lettura. Contattare l&#39;amministratore [!DNL Adobe Journey Optimizer] in caso di dubbi sul livello di accesso corrente.
+++

+++Posso utilizzare il server MCP in ambienti sandbox?

Sì. Il server MCP rispetta la configurazione sandbox [!DNL Adobe Journey Optimizer]. Puoi eseguire query sui dati specifici della sandbox specificando la sandbox nel prompt o connettendoti con le credenziali con ambito a una particolare sandbox.
+++

