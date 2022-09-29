---
title: Garanzie e limitazioni di Journey Optimizer
description: Ulteriori informazioni sulle protezioni Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9c0f604680787dbdf5fb820074408edad78f8bfb
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 3%

---

# Guardrail e limitazioni {#limitations}

Le autorizzazioni, le limitazioni dei prodotti e le protezioni delle prestazioni sono elencate in [Pagina di descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Di seguito sono riportati ulteriori guardrail e limitazioni relativi all’utilizzo di [!DNL Adobe Journey Optimizer].

## Garanzie messaggi {#message-guardrails}

* Non è possibile aggiungere allegati a un messaggio e-mail con [!DNL Journey Optimizer].
* Non è possibile utilizzare lo stesso dominio di invio per inviare messaggi da [!DNL Adobe Journey Optimizer] e da un altro prodotto, quali [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage] ad esempio.


## Garanzie di gestione delle decisioni {#offer-guardrails}

Le protezioni delle prestazioni e i limiti statici per il processo decisionale sono elencati nella [Adobe pagina di descrizione del prodotto Servizio app di Offer Decisioning](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Guardrail delle pagine di destinazione {#lp-guardrails}

* Solo uno **Modulo** può essere utilizzato in una singola pagina primaria.
* La **Modulo** non può essere utilizzato nelle pagine secondarie.
* Non puoi aggiungere una preintestazione a una pagina di destinazione.
* Non è possibile selezionare la **Codice personalizzato** durante la progettazione di una pagina principale di destinazione.

## guardrail di percorso {#journeys-guardrails}

### Azioni generali {#general-actions-g}

* Non esiste alcuna limitazione di invio.
* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto.
* Incorporato **Reazione** ti consente di reagire alle azioni predefinite. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/reaction-events.md). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato.
* Non è possibile inserire due azioni in parallelo, ma è necessario aggiungerle una dopo l’altra.
* Nella maggior parte dei casi, un profilo non può essere presente più volte nello stesso percorso e allo stesso tempo. Se la reintroduzione è abilitata, un profilo può rientrare in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso. [Ulteriori informazioni](../building-journeys/journey-end.md)

### Versioni del percorso {#journey-versions-g}

* Un percorso che inizia con un’attività evento nella versione 1 non può iniziare con un elemento diverso da un evento in ulteriori versioni. Non è possibile avviare un percorso con un **Qualificazione del segmento** evento.
* Un percorso che inizia con un **Qualificazione del segmento** l’attività nella versione v1 deve sempre iniziare con un **Qualificazione del segmento** in ulteriori versioni.
* Segmento e spazio dei nomi scelti in **Qualificazione del segmento** (primo nodo) non può essere modificato nelle nuove versioni.
* La regola di rientro deve essere la stessa in tutte le versioni del percorso.
* Un percorso che inizia con un **Leggi segmento** impossibile iniziare con un altro evento nelle versioni successive.

### Azioni personalizzate {#custom-actions-g}

* L&#39;URL dell&#39;azione personalizzata non supporta i parametri dinamici.
* Sono supportati solo i metodi di chiamata POST e PUT
* Il nome del parametro o dell&#39;intestazione della query non deve iniziare con &quot;.&quot; oppure &quot;$&quot;
* Gli indirizzi IP non sono consentiti
* Indirizzi di Adobe interni (.adobe.) non sono consentiti.

### Eventi {#events-g}

* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso di clienti devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in Adobe Experience Platform. Questa limitazione non si applica agli eventi basati su regole.
* Gli eventi aziendali non possono essere utilizzati in combinazione con eventi unitari o attività di qualificazione dei segmenti.
* I percorsi unitari (a partire da un evento o da una qualifica di segmento) includono una guardrail che impedisce l’attivazione errata dei percorsi più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.

### Origini dati {#data-sources-g}

* Le origini dati esterne possono essere sfruttate all’interno di un percorso di clienti per cercare dati esterni in tempo reale. Queste sorgenti devono essere utilizzabili tramite API REST, supportare JSON e poter gestire il volume di richieste.

### Creazione di percorsi e profili {#journeys-limitation-profile-creation}

In Adobe Experience Platform si verifica un ritardo associato alla creazione/aggiornamento dei profili basati su API. L’obiettivo a livello di servizio (SLT) in termini di latenza è &lt; 1 minuto dall’acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di 20.000 richieste al secondo (RPS).

Se un percorso viene attivato simultaneamente per la creazione di un profilo e controlla/recupera immediatamente le informazioni dal Servizio profili, potrebbe non funzionare correttamente.

Puoi scegliere una delle due soluzioni seguenti:

* Aggiungi un’attività di attesa dopo il primo evento, per dare a Adobe Experience Platform il tempo necessario per eseguire l’acquisizione in Profile Service.

* Imposta un percorso che non sfrutta immediatamente il profilo. Ad esempio, se il percorso è progettato per confermare la creazione di un account, l’evento esperienza potrebbe contenere le informazioni necessarie per inviare il primo messaggio di conferma (nome, cognome, indirizzo e-mail, ecc.).

### Leggi segmento {#read-segment-g}

* I segmenti in streaming sono sempre aggiornati, ma i segmenti batch non verranno calcolati al momento del recupero. Vengono valutati solo ogni giorno al momento della valutazione giornaliera del lotto.
* Per i percorsi che utilizzano un’attività Read Segment , esiste un numero massimo di percorsi che possono iniziare contemporaneamente. I tentativi verranno eseguiti dal sistema, ma si prega di evitare di avere più di cinque percorsi (con Leggi segmento, programmato o partendo &quot;il più presto possibile&quot;) a partire allo stesso tempo distribuendoli nel tempo, ad esempio 5 a 10 minuti di distanza.

### Editor espressioni {#expression-editor}

* I gruppi di campi evento esperienza non possono essere utilizzati nei percorsi che iniziano con un segmento Read , una qualifica Segment o un’attività dell’evento aziendale.

