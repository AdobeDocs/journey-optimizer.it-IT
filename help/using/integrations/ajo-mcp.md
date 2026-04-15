---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo dei client MCP
description: Scopri come collegare Adobe Journey Optimizer ai client MCP utilizzando il server MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 7ae497e7a0e4d1652413a5a6dbd5d617a3ec31fe
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# Utilizzo dei client MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile solo in **Claude Web** e **Claude Desktop**. Il supporto per ulteriori applicazioni compatibili con MCP verrà aggiunto nelle prossime versioni.

L&#39;integrazione MCP [!DNL Adobe Journey Optimizer] consente di eseguire query su campagne, percorsi e offerte utilizzando prompt in linguaggio semplice, senza scrivere chiamate API o navigare tra le schermate dei prodotti. Questa pagina spiega come funziona l’integrazione, cosa puoi farci e come iniziare.

## Che cos&#39;è Model Context Protocol? {#mcp-overview}

I team di marketing ed esperienza del cliente si affidano sempre di più ad applicazioni basate su chat e a strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Journey Optimizer] ora fornisce un server MCP che riunisce le operazioni di campagna, percorso, fedeltà e sandbox direttamente in qualsiasi applicazione compatibile con MCP. Con l&#39;integrazione MCP [!DNL Adobe Journey Optimizer], utenti tipo diversi possono collaborare agli stessi dati di orchestrazione, senza scrivere query sull&#39;API REST [!DNL Adobe Journey Optimizer] o navigare in più schermate dell&#39;interfaccia utente. I clienti possono descrivere il proprio intento conversazionalmente e consentire al LLM di richiamare gli strumenti MCP appropriati.

## Funzionalità principali {#mcp-capabilities}

Il server MCP [!DNL Adobe Journey Optimizer] consente di esaminare, riepilogare e risolvere i problemi di percorsi, campagne e offerte direttamente dall&#39;assistente AI. Tutte le operazioni sono **di sola lettura**. Le superfici del server MCP recuperano le API come risposte in linguaggio semplice per consentire di:

* **Comprendere la logica di percorso**: ottieni un riepilogo leggibile dei rami, delle condizioni e delle azioni di qualsiasi percorso.
* **Verifica preparazione campagna** — Identifica i blocchi che impediscono la pubblicazione di una campagna.
* **Spazi vuoti di copertura spot**: scopri quali canali vengono coperti nei tuoi percorsi live e nelle tue campagne e dove esistono spazi vuoti.
* **Controlla il tuo portfolio di orchestrazioni**: controlla lo stato completo delle campagne e dei percorsi senza analizzare il JSON o passare da uno schermo all&#39;altro del prodotto.

## Casi d’uso {#mcp-use-cases}

Gli esempi seguenti mostrano come interagire con il server MCP [!DNL Adobe Journey Optimizer] utilizzando il linguaggio naturale:

| Obiettivo | Esempio di prompt |
|---|---|
| **Riepiloga dettagli campagna** | &quot;Ottieni campaign cmp456 e riepiloga pubblico, pianificazione, stato e pacchetti.&quot; |
| **Controllo inventario e stato** | &quot;Che cosa abbiamo e in quale stato? Mostra i conteggi in tempo reale rispetto alle bozze e ai conteggi completati/interrotti/archiviati per le campagne.&quot; |
| **Verifica preparazione pubblicazione** | &quot;Perché campaign cmp456 non è pronto per la pubblicazione? Mostratemi i bloccanti.&quot; |
| **Confronta oggetti** | &quot;Confrontare le campagne abc123 e xyz789: cosa è cambiato nello stato e nella pianificazione?&quot; |
| **Controlla il tuo portfolio** | &quot;In tutti i percorsi e le campagne live, quali canali vengono coperti e dove sono le differenze?&quot; |
| **Copertura e combinazione dei canali** | &quot;Mostra l’impatto del canale su percorsi, campagne e posizionamenti di offerte: solo e-mail rispetto a multicanale, utilizzo di push/SMS/in-app e mancata corrispondenza tra i canali del percorso.&quot; |

## Prerequisiti {#mcp-prerequisites}

Prima di collegare il server MCP [!DNL Adobe Journey Optimizer] al client MCP, verificare quanto segue:

* Hai una licenza di [!DNL Adobe Journey Optimizer] attiva.
* È possibile accedere a un&#39;applicazione compatibile con MCP supportata (attualmente Claude Web o Claude Desktop).
* In [!DNL Adobe Journey Optimizer] si dispone delle autorizzazioni necessarie per visualizzare campagne, percorsi e offerte.

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

## Domande frequenti {#mcp-faq}

+++Quali client MCP sono supportati?

Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile per **Claude Web** e **Claude Desktop**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
+++

+++A quali [!DNL Adobe Journey Optimizer] oggetti posso accedere tramite MCP?

Puoi accedere a campagne, percorsi, offerte, dati fedeltà e informazioni sandbox. Le operazioni sono di sola lettura (recupero API); le operazioni di scrittura non sono supportate nella versione corrente.
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
