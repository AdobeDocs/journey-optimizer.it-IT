---
solution: Journey Optimizer
product: journey optimizer
title: Limitazioni del percorso
description: Ulteriori informazioni sulle limitazioni del Percorso
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: percorsi, limitazione
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1276
ht-degree: 20%

---

# Limitazioni {#journey-limitations}

>[!BEGINSHADEBOX]

**In questa pagina:** Rivedi le limitazioni e i guardrail che si applicano ai percorsi, incluse le azioni, le versioni, le azioni personalizzate, gli eventi e le origini dati.

>[!ENDSHADEBOX]

Di seguito sono riportate le limitazioni relative all’utilizzo dei percorsi.

## Limitazioni delle azioni generali {#action-limitations}

* Non esiste alcuna limitazione di invio.
* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto.
* L&#39;evento predefinito **Reaction** ti consente di reagire alle azioni predefinite (vedi questa [pagina](../building-journeys/reaction-events.md)). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato.
* Non è possibile inserire due azioni in parallelo, è necessario aggiungerle una dopo l’altra.


## Limitazioni delle versioni di percorso {#journey-versions-limitations}

* Un percorso che inizia con un’attività evento nella versione v1, nelle altre versioni non può iniziare con un elemento diverso. Impossibile avviare un percorso con un evento **Qualificazione del pubblico**.
* Un percorso che inizia con un&#39;attività **Qualificazione del pubblico** nella versione v1 deve sempre iniziare con una **Qualificazione del pubblico** nelle altre versioni.
* Il pubblico e lo spazio dei nomi scelti in **Qualificazione del pubblico** (primo nodo) non possono essere modificati nelle nuove versioni.
* La regola di reingresso deve essere la stessa in tutte le versioni del percorso.
* Un percorso che inizia con un’attività di **Leggi pubblico** non può iniziare con un altro evento nelle versioni successive.

## Limitazioni delle azioni personalizzate {#custom-actions-limitations}

* L’URL dell’azione personalizzata non supporta i parametri dinamici. 
* Sono supportati solo i metodi di chiamata POST e PUT. 
* Il nome del parametro o dell&#39;intestazione della query non deve iniziare con &quot;.&quot; o &quot;$&quot;. 
* Gli indirizzi IP non sono consentiti. 
* Indirizzi interni di Adobe (.adobe.) non sono consentiti.

## Limitazioni degli eventi {#events-limitations}

* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso del cliente devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in [!DNL Adobe Experience Platform]. Questa limitazione non si applica agli eventi basati su regole.

## Limitazioni degli eventi di reazione {#reaction-limitations}

* Le attività **[!UICONTROL Reaction]** devono essere inserite immediatamente dopo un&#39;attività [channel action](../building-journeys/journey-action.md) nell&#39;area di lavoro del percorso. Il posizionamento di un&#39;attività **[!UICONTROL Wait]** o di qualsiasi altra attività tra l&#39;azione del canale e l&#39;attività **[!UICONTROL Reaction]** non è supportato e potrebbe impedire il funzionamento previsto dell&#39;attività Reaction. Ulteriori informazioni in [questa sezione](../building-journeys/reaction-events.md).

## Limitazioni delle origini dati {#data-sources-limitations}

* Le origini dati esterne possono essere sfruttate all’interno di un percorso di clienti per ricercare dati esterni in tempo reale. Queste origini devono essere utilizzabili tramite API REST, supportare JSON ed essere in grado di gestire il volume delle richieste.

## Percorsi che iniziano contemporaneamente alla creazione di un profilo {#journeys-limitation-profile-creation}

Ritardo associato alla creazione/aggiornamento del profilo basato su API in [!DNL Adobe Experience Platform]. Il target livello di servizio (Service Level Target, SLT) in termini di latenza è &lt; di 1 minuto dall’acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di 20.000 richieste al secondo (RPS).

Se un Percorso viene attivato simultaneamente per la creazione di un profilo e immediatamente controlla/recupera le informazioni dal servizio profili, potrebbe non funzionare correttamente.

Puoi scegliere una delle due soluzioni seguenti:

* Aggiungi un&#39;attività Attendi dopo il primo evento, per dare a [!DNL Adobe Experience Platform] il tempo necessario per eseguire l&#39;acquisizione nel servizio profili.

* Impostare un percorso che non sfrutta immediatamente il profilo. Ad esempio, se il percorso è progettato per confermare la creazione di un account, l’evento esperienza potrebbe contenere le informazioni necessarie per inviare il primo messaggio di conferma (nome, cognome, indirizzo e-mail, ecc.).

## Limitazioni del pubblico di lettura {#read-audiences-limitations}

* I tipi di pubblico in streaming sono sempre aggiornati, ma i tipi di pubblico in batch non verranno calcolati al momento del recupero. Vengono valutati ogni giorno solo al momento della valutazione giornaliera del batch.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina sono elencate le limitazioni tecniche rigide applicabili alle azioni del percorso, alle versioni del percorso, alle azioni personalizzate, agli eventi, agli eventi di reazione, alle origini dati e alla lettura del pubblico in Adobe Journey Optimizer.

**Intenti:**

* Comprendere i limiti di invio e di nuovo tentativo per le azioni di percorso
* Scopri quali transizioni di versione del percorso sono consentite o bloccate
* Identificare le restrizioni per la configurazione di URL, metodo ed intestazione delle azioni personalizzate
* Comprendere i requisiti dell&#39;origine dati per l&#39;integrazione del sistema esterno
* Evitare problemi di tempistica quando si avvia un percorso nello stesso momento in cui si crea il profilo

**Glossario:**

* **Evento di reazione**: un&#39;attività di percorso che ascolta l&#39;interazione di un profilo con un&#39;azione del canale (ad esempio, apertura e-mail o clic); deve essere inserita immediatamente dopo l&#39;attività dell&#39;azione del canale. *(specifico per prodotto)*
* **Evento basato su regole**: tipo di evento in cui il trigger è definito da una condizione logica anziché da un ID di orchestrazione generato dal sistema. *(specifico per prodotto)*
* **SLT (Service Level Target)**: il benchmark di latenza per la creazione/aggiornamento di profili basati su API in Adobe Experience Platform, a meno di 1 minuto dall&#39;acquisizione al profilo unificato al 95° percentile per RPS 20.000.

**Guardrail:**

* Non viene applicata alcuna limitazione all’invio; tre tentativi vengono eseguiti automaticamente in caso di errore e non possono essere regolati
* Due azioni non possono essere eseguite in parallelo; devono essere aggiunte in sequenza
* Un percorso che inizia con un’attività evento nella versione v1 non può iniziare con un’attività non evento nelle versioni successive
* Un percorso che inizia con una Qualificazione del pubblico nella versione v1 deve sempre iniziare con Qualificazione del pubblico in tutte le versioni successive; il pubblico e lo spazio dei nomi non possono essere modificati
* Un percorso che inizia con Read Audience non può iniziare con un evento diverso nelle versioni successive
* L’URL dell’azione personalizzata non supporta i parametri dinamici; sono supportati solo i metodi di chiamata POST e PUT
* I nomi dei parametri e delle intestazioni della query di azione personalizzata non devono iniziare con &quot;.&quot; o &quot;$&quot;; indirizzi IP e indirizzi Adobe interni (.adobe.) non sono consentiti
* Le attività di reazione devono essere inserite immediatamente dopo un’attività di azione del canale; l’inserimento di un’attività Attendi o di altro tipo tra di esse non è supportato
* Le origini dati esterne devono essere accessibili tramite API REST, supportare JSON e gestire il volume della richiesta
* I tipi di pubblico batch vengono valutati una sola volta al giorno al momento della valutazione batch giornaliera e non vengono ricalcolati al momento del recupero
* Quando un percorso viene attivato contemporaneamente alla creazione di un profilo, i dati del profilo potrebbero non essere ancora disponibili a causa della latenza di acquisizione di Platform

**Terminologia:**

* Nome canonico: limitazioni di Percorso — Acronimo: none — varianti: protezioni di percorso, limitazioni di percorso
* Non confondere: &quot;Limitazione dell’evento di reazione&quot; ≠ &quot;Limitazione dell’azione generale&quot; — L’evento di reazione deve essere posizionato direttamente dopo un’azione del canale; la limitazione dell’azione generale copre tentativi, parallelismo e limitazione

**Domande frequenti:**

* **D: quante volte Journey Optimizer ritenta un&#39;azione non riuscita?** — Vengono eseguiti automaticamente tre tentativi; il numero di tentativi non può essere configurato.
* **Q: posso inserire un&#39;attività Attendi tra un&#39;azione del canale e un evento Reazione?** — No; l&#39;evento Reazione deve essere inserito immediatamente dopo l&#39;attività di azione del canale. L’aggiunta di attività nel periodo intermedio non è supportata e potrebbe impedire il funzionamento previsto dell’evento Reazione.
* **Q: è possibile modificare il primo tipo di evento durante la creazione di una nuova versione del percorso?** — No; il meccanismo di entrata impostato in v1 deve essere mantenuto in tutte le versioni successive. Un percorso che inizia con un evento deve continuare a iniziare con un evento, e un percorso che inizia con Qualificazione del pubblico deve sempre iniziare con Qualificazione del pubblico.
* **D: perché il mio percorso potrebbe non funzionare quando viene attivato contemporaneamente alla creazione di un profilo?** — La creazione di profili tramite API ha una latenza prima che i dati siano disponibili in Unified Profile (SLT &lt; 1 minuto al 95° percentile). L’aggiunta di un’attività Wait dopo il primo evento offre a Platform il tempo di completare l’acquisizione.
* **Q: i tipi di pubblico in streaming sono sempre correnti nei percorsi?** — Sì; il pubblico in streaming è sempre aggiornato. I tipi di pubblico batch, tuttavia, vengono valutati solo una volta al giorno al momento della valutazione batch giornaliera, non al momento del recupero.

+++
