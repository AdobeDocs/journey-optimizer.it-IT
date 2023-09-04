---
solution: Journey Optimizer
product: journey optimizer
title: Limitazioni del percorso
description: Ulteriori informazioni sulle limitazioni del Percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: percorsi, limitazione
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 64abe386cd0d7b7e849fb6f6cdc70c00b4365feb
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 71%

---

# Limitazioni  {#journey-limitations}

Di seguito sono riportate le limitazioni relative all’utilizzo dei percorsi.

## Limitazioni delle azioni generali {#action-limitations}

* Non esiste alcuna limitazione di invio. 
* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto. 
* Il sistema integrato **Reazione** consente di reagire alle azioni predefinite (vedi questo [pagina](../building-journeys/reaction-events.md)). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato. 
* Non è possibile inserire due azioni in parallelo, è necessario aggiungerle una dopo l’altra.

## Limitazioni delle versioni di percorso {#journey-versions-limitations}

* Un percorso che inizia con un’attività evento nella versione v1, nelle altre versioni non può iniziare con un elemento diverso. Impossibile avviare un percorso con un **Qualificazione del pubblico** evento.
* Un percorso che inizia con **Qualificazione del pubblico** l&#39;attività nella versione 1 deve sempre iniziare con un **Qualificazione del pubblico** in altre versioni.
* Il pubblico e lo spazio dei nomi scelti in **Qualificazione del pubblico** (primo nodo) non può essere modificato nelle nuove versioni.
* La regola di reingresso deve essere la stessa in tutte le versioni del percorso.
* Un percorso che inizia con un’attività di **Leggi pubblico** non può iniziare con un altro evento nelle versioni successive.

## Limitazioni delle azioni personalizzate {#custom-actions-limitations}

* L’URL dell’azione personalizzata non supporta i parametri dinamici. 
* Sono supportati solo i metodi di chiamata POST e PUT. 
* Il nome del parametro o dell’intestazione della query non deve iniziare con “.” oppure “$”. 
* Gli indirizzi IP non sono consentiti. 
* Gli indirizzi interni di Adobe (.adobe.) non sono consentiti.

## Eventi limitazioni {#events-limitations}

* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso del cliente devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in Adobe Experience Platform. Questa limitazione non si applica agli eventi basati su regole.

## Limitazioni delle origini dati {#data-sources-limitations}

* Le origini dati esterne possono essere sfruttate all’interno di un percorso di clienti per ricercare dati esterni in tempo reale. Queste origini devono essere utilizzabili tramite API REST, supportare JSON ed essere in grado di gestire il volume delle richieste.

## Percorsi che iniziano contemporaneamente alla creazione di un profilo {#journeys-limitation-profile-creation}

In Adobe Experience Platform si verifica un ritardo associato alla creazione/aggiornamento dei profili basati su API. Il target livello di servizio (Service Level Target, SLT) in termini di latenza è &lt; di 1 minuto dall’acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di 20.000 richieste al secondo (RPS).

Se un Percorso viene attivato simultaneamente per la creazione di un profilo e immediatamente controlla/recupera le informazioni dal servizio profili, potrebbe non funzionare correttamente.

Puoi scegliere una delle due soluzioni seguenti:

* Aggiungi un’attività di attesa dopo il primo evento, per dare ad Adobe Experience Platform il tempo necessario per eseguire l’acquisizione nel servizio profilo.

* Impostare un percorso che non sfrutta immediatamente il profilo. Ad esempio, se il percorso è progettato per confermare la creazione di un account, l’evento esperienza potrebbe contenere le informazioni necessarie per inviare il primo messaggio di conferma (nome, cognome, indirizzo e-mail, ecc).

## Limitazioni del pubblico di lettura {#read-audiences-limitations}

* I tipi di pubblico in streaming sono sempre aggiornati, ma i tipi di pubblico in batch non verranno calcolati al momento del recupero. Vengono valutati ogni giorno solo al momento della valutazione giornaliera del batch.
