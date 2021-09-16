---
title: Limiti Journey Optimizer
description: Ulteriori informazioni sulle limitazioni di Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: f177c9b2c7c7a7fa6182d07e773efd0683886d34
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 2%

---

# Limitazioni  {#limitations}

Le autorizzazioni, le limitazioni del prodotto e le protezioni delle prestazioni sono elencate nella pagina di descrizione del prodotto di Adobe Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.[

Di seguito sono riportate ulteriori limitazioni durante l’utilizzo di [!DNL Adobe Journey Optimizer].

## Limitazioni nei messaggi

* Non è possibile aggiungere allegati a un messaggio e-mail con [!DNL Journey Optimizer].
* Ccn e-mail non supportato in [!DNL Journey Optimizer].

## Limitazioni nei percorsi

### Azioni generali

* Non esiste alcuna limitazione di invio. 
* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto. 
* L&#39;evento **Reaction** integrato consente di reagire alle azioni predefinite. Per ulteriori informazioni, consulta [questa pagina](building-journeys/reaction-events.md). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato. 
* Non è possibile inserire due azioni in parallelo, ma è necessario aggiungerle una dopo l’altra.

### Azione messaggio

* Quando aggiungi un messaggio multicanale, vengono inviati due messaggi.

### Versioni del percorso {#journey-versions-limitations}

* Un percorso che inizia con un’attività evento nella versione 1 non può iniziare con un elemento diverso da un evento in ulteriori versioni. Non è possibile avviare un percorso con un evento **Qualificazione del segmento**.
* Un percorso che inizia con un&#39;attività **Qualifica segmento** nella versione 1 deve sempre iniziare con una **Qualificazione segmento** in ulteriori versioni.
* Il segmento e lo spazio dei nomi scelti in **Qualificazione del segmento** (primo nodo) non possono essere modificati nelle nuove versioni.
* La regola di rientro deve essere la stessa in tutte le versioni del percorso.
* Un percorso che inizia con un **Leggi segmento** non può iniziare con un altro evento nelle versioni successive.
 

### Azioni personalizzate

* L&#39;URL dell&#39;azione personalizzata non supporta i parametri dinamici. 
* Sono supportati solo i metodi di chiamata POST e PUT. 
* Il nome del parametro o dell&#39;intestazione della query non deve iniziare con &quot;.&quot; oppure &quot;$&quot;. 
* Gli indirizzi IP non sono consentiti. 
* Indirizzi di Adobe interni (.adobe.) non sono consentiti.
 

### Eventi

* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso di clienti devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in Adobe Experience Platform. Questa limitazione non si applica agli eventi basati su regole.
 

### Origini dati

* Le origini dati esterne possono essere utilizzate all’interno di un percorso di clienti per cercare dati esterni in tempo reale. Queste sorgenti devono essere utilizzabili tramite API REST, supportare JSON e poter gestire il volume di richieste.

### Percorsi che iniziano contemporaneamente alla creazione di un profilo {#journeys-limitation-profile-creation}

In Adobe Experience Platform si verifica un ritardo associato alla creazione/aggiornamento dei profili basati su API. L’obiettivo a livello di servizio (SLT) in termini di latenza è &lt; 1 minuto dall’acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di 20.000 richieste al secondo (RPS).

Se un percorso viene attivato simultaneamente per la creazione di un profilo e controlla/recupera immediatamente le informazioni dal Servizio profili, potrebbe non funzionare correttamente.

Puoi scegliere una delle due soluzioni seguenti:

* Aggiungi un’attività di attesa dopo il primo evento, per dare a Adobe Experience Platform il tempo necessario per eseguire l’acquisizione in Profile Service.

* Imposta un percorso che non sfrutta immediatamente il profilo. Ad esempio, se il percorso è progettato per confermare la creazione di un account, l’evento esperienza potrebbe contenere le informazioni necessarie per inviare il primo messaggio di conferma (nome, cognome, indirizzo e-mail, ecc.).

### Leggi segmento

* I segmenti in streaming sono sempre aggiornati, ma i segmenti batch non verranno calcolati al momento del recupero. Vengono valutati solo ogni giorno al momento della valutazione giornaliera del lotto.
