---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni di Journey Optimizer
description: Ulteriori informazioni sui guardrail di Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 92%

---

# Guardrail e limitazioni {#limitations}

I diritti, le limitazioni del prodotto e i guardrail relativi alle prestazioni sono elencati nella [pagina di descrizione del prodotto di Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

Prima di iniziare, è inoltre necessario essere a conoscenza di [guardrail dati Profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=it){target="_blank"}.

Di seguito sono riportati ulteriori guardrail e limitazioni relativi all’utilizzo di [!DNL Adobe Journey Optimizer].

## Guardrail messaggi {#message-guardrails}

* Con [!DNL Journey Optimizer] non è possibile aggiungere allegati a un messaggio e-mail.
* Non è possibile utilizzare lo stesso dominio di invio per inviare messaggi da [!DNL Adobe Journey Optimizer] e da un altro prodotto, come [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage] ad esempio.


## Guardrail di gestione delle decisioni {#offer-guardrails}

I guardrail delle prestazioni e i limiti statici per il processo decisionale sono elencati nella [pagina di descrizione del prodotto Adobe Offer Decisioning App Service](https://helpx.adobe.com/it/legal/product-descriptions/offer-decisioning-app-service.html){target="_blank"}.


## Guardrail delle pagine di destinazione {#lp-guardrails}

* Solo un componente **Modulo** può essere utilizzato in una singola pagina principale.
* Il componente **Modulo** non può essere utilizzato nelle pagine secondarie.
* Non puoi aggiungere un preheader a una pagina di destinazione.
* Non è possibile selezionare l’opzione **Crea il codice** durante la progettazione di una pagina di destinazione principale.

## Guardrail di percorso {#journeys-guardrails}

### Guardrail di percorso generale {#journeys-guardrails-journeys}

* Il numero di attività in un percorso è limitato a 50. Il numero di attività viene visualizzato nella sezione in alto a sinistra dell’area di lavoro del percorso.
* Numero di **percorsi vivi** in un’organizzazione è limitato a 100 per sandbox. Una volta raggiunto questo limite, non puoi più pubblicare un nuovo percorso.

### Azioni generali {#general-actions-g}

* Non esiste alcuna limitazione di invio.
* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto.
* L’evento **Reazione** incorporato ti consente di reagire alle azioni predefinite. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/reaction-events.md). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato.
* Non è possibile inserire due azioni in parallelo, è necessario aggiungerle una dopo l’altra.
* In genere, un profilo non può essere presente più volte nello stesso percorso contemporaneamente. Se è stato abilitato il rientro, un profilo può rientrare in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso. [Ulteriori informazioni](../building-journeys/end-journey.md)

### Versioni del percorso {#journey-versions-g}

* Un percorso che inizia con un’attività evento nella versione v1, nelle altre versioni non può iniziare con un elemento diverso. Non è possibile avviare un percorso con un evento **Qualificazione del segmento**.
* Un percorso che inizia con un’attività di **Qualificazione del segmento** nella versione v1 deve sempre iniziare con una **Qualificazione del segmento** nelle altre versioni.
* Il segmento e lo spazio dei nomi scelti nella **Qualificazione del segmento** (primo nodo) non possono essere modificati nelle nuove versioni.
* La regola di rientro deve essere la stessa in tutte le versioni del percorso.
* Un percorso che inizia con un’attività di **Lettura segmento** non può iniziare con un altro evento nelle versioni successive.
* Non puoi creare una nuova versione di un percorso di segmenti di lettura con lettura incrementale. È necessario duplicare il percorso.

### Azioni personalizzate {#custom-actions-g}

* L’URL dell’azione personalizzata non supporta i parametri dinamici.
* Sono supportati solo i metodi di chiamata POST e PUT
* Il nome del parametro o dell’intestazione della query non deve iniziare con “.” oppure “$”
* Gli indirizzi IP non sono consentiti
* Non sono consentiti indirizzi di Adobe interni (`.adobe.*`) negli URL e nelle API.
* Non è possibile rimuovere le azioni personalizzate incorporate.

### Eventi {#events-g}

* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso del cliente devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in Adobe Experience Platform. Questa limitazione non si applica agli eventi basati su regole.
* Gli eventi di business non possono essere utilizzati in combinazione con eventi unitari o attività di qualificazione dei segmenti.
* I percorsi unitari (a partire da un evento o da una qualificazione del segmento) includono un guardrail che impedisce che i percorsi siano erroneamente attivati più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.
* Journey Optimizer richiede che gli eventi vengano inviati in streaming al servizio core di raccolta dati (DCCS) per poter attivare un percorso. Eventi acquisiti in batch o eventi da set di dati interni di Journey Optimizer (feedback messaggi, tracciamento e-mail, ecc.) non possono essere utilizzati per attivare un percorso. Per i casi d’uso in cui non è possibile ricevere eventi in streaming, crea un segmento basato su tali eventi e utilizza l’attiviità **Leggi segmento**. Tecnicamente, è possibile usare la qualificazione dei segmenti, ma potrebbe causare problemi a valle in base alle azioni utilizzate.

### Origini dati {#data-sources-g}

* Le origini dati esterne possono essere sfruttate all’interno di un percorso del cliente per ricercare dati esterni in tempo reale. Queste origini devono essere utilizzabili tramite API REST, supportare JSON ed essere in grado di gestire il volume delle richieste.
* Non sono consentiti indirizzi di Adobe interni (`.adobe.*`) negli URL e nelle API.

### Creazione di percorsi e profili {#journeys-limitation-profile-creation}

In Adobe Experience Platform si verifica un ritardo associato alla creazione/aggiornamento dei profili basati su API. Il target livello di servizio (Service Level Target, SLT) in termini di latenza è &lt; di 1 minuto dall’acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di 20.000 richieste al secondo (RPS).

Se un percorso viene attivato simultaneamente per la creazione di un profilo e immediatamente controlla/recupera le informazioni dal Servizio profili, potrebbe non funzionare correttamente.

Puoi scegliere una delle due soluzioni seguenti:

* Aggiungi un’attività di attesa dopo il primo evento, per dare ad Adobe Experience Platform il tempo necessario per eseguire l’acquisizione nel servizio profilo.

* Impostare un percorso che non sfrutta immediatamente il profilo. Ad esempio, se il percorso è progettato per confermare la creazione di un account, l’evento esperienza potrebbe contenere le informazioni necessarie per inviare il primo messaggio di conferma (nome, cognome, indirizzo e-mail, ecc.).

### Leggi segmento {#read-segment-g}

* I segmenti in streaming sono sempre aggiornati, ma i segmenti batch non verranno calcolati al momento del recupero. Vengono valutati solo ogni giorno al momento della valutazione giornaliera del batch.
* Per i percorsi che utilizzano un’attività di lettura del segmento, esiste un numero massimo di percorsi che possono avviare contemporaneamente. I tentativi verranno eseguiti dal sistema, ma evita di disporre di più di cinque percorsi (con Leggi segmento, programmato o che inizia “non appena possibile”) che si avviano nello stesso momento distribuendoli nel tempo, ad esempio a 5-10 minuti di distanza.

### Editor espressioni {#expression-editor}

* I gruppi di campo di evento esperienza non possono più essere utilizzati nei percorsi che iniziano con un’attività Leggi segmento, Qualificazione del segmento o Evento di business. È necessario creare un nuovo segmento e utilizzare una condizione di segmento nel percorso.


