---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare gli assistenti AI tramite MCP
description: Scopri come collegare Adobe Journey Optimizer agli assistenti AI tramite il server MCP (Model Context Protocol)
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Disponibilità limitata" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: b92ef33b03e0bdcd6e615846cd7654aaab1b4a1a
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---

# Utilizzare gli assistenti AI tramite MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile solo in **Claude Web** e **Claude Desktop**.

## Che cos&#39;è Model Context Protocol? {#mcp-overview}

I team di marketing ed esperienza del cliente si affidano sempre di più ad applicazioni basate su chat e a strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Journey Optimizer] ora fornisce un server MCP che riunisce le operazioni di campagna, percorso, fedeltà e sandbox direttamente in qualsiasi applicazione compatibile con MCP. Con l&#39;integrazione MCP [!DNL Adobe Journey Optimizer], utenti tipo diversi possono collaborare agli stessi dati di orchestrazione, senza scrivere query sull&#39;API REST [!DNL Adobe Journey Optimizer] o navigare in più schermate dell&#39;interfaccia utente. I clienti possono descrivere il proprio intento conversazionalmente e consentire al LLM di richiamare gli strumenti MCP appropriati.

## Funzionalità principali {#mcp-capabilities}

Il server MCP [!DNL Adobe Journey Optimizer] ti consente di esaminare, riepilogare e risolvere i problemi di [!DNL Adobe Journey Optimizer] percorsi, campagne e offerte direttamente dall&#39;assistente AI. Le API di recupero di [!DNL Adobe Journey Optimizer] vengono trasformate in risposte in linguaggio semplice, in modo da poter:

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

Prima di collegare il server MCP [!DNL Adobe Journey Optimizer] all&#39;assistente AI, verificare quanto segue:

* Hai una licenza di [!DNL Adobe Journey Optimizer] attiva.
* È possibile accedere a un&#39;applicazione compatibile con MCP supportata (attualmente Claude Web o Claude Desktop).
* In [!DNL Adobe Journey Optimizer] si dispone delle autorizzazioni necessarie per visualizzare campagne, percorsi e offerte.

## Connetti il server MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Verranno aggiunti passaggi di configurazione dettagliati una volta che l’integrazione sarà generalmente disponibile. Contatta il tuo rappresentante Adobe per accedervi in anteprima.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Domande frequenti {#mcp-faq}

+++Quali assistenti AI sono supportati?

Il server MCP [!DNL Adobe Journey Optimizer] è attualmente disponibile per **Claude Web** e **Claude Desktop**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
+++

+++A quali [!DNL Adobe Journey Optimizer] oggetti posso accedere tramite MCP?

Puoi accedere a campagne, percorsi, offerte, dati fedeltà e informazioni sandbox. Le operazioni sono di sola lettura (recupero API); le operazioni di scrittura non sono supportate nella versione corrente.
+++

+++È necessario l&#39;accesso per sviluppatori per utilizzare il server MCP [!DNL Adobe Journey Optimizer]?

No. Il server MCP è progettato sia per utenti tecnici che di marketing. Gli addetti al marketing possono interagire con esso utilizzando prompt in linguaggio naturale in Claude, mentre gli sviluppatori possono utilizzarlo anche in strumenti per sviluppatori che supportano MCP.
+++

+++I miei dati vengono inviati al provider dell’assistente di IA?

Quando si invia una richiesta, l&#39;assistente AI può inviare il contesto pertinente (inclusi i dati [!DNL Adobe Journey Optimizer] restituiti dal server MCP) al proprio modello per l&#39;elaborazione. Esamina le politiche sulla privacy e sulla gestione dei dati del provider di assistenza AI prima di connetterti ai dati di produzione.
+++

