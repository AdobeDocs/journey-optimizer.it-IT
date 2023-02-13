---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla consegna
description: Scopri le linee guida per il recapito messaggi
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 2%

---

# Introduzione alla consegna {#manage-deliverability}

Il recapito messaggi è una misura del successo delle consegne nelle caselle in entrata dei destinatari.

>[!NOTE]
>
>Per i clienti che dispongono di licenze per Healthcare Shield, Adobe utilizza TLS 1.2 per proteggere lo scambio di dati tra i sistemi degli utenti (destinatari) e Journey Optimizer (mittente). Se il server di posta ricevente non supporta TLS 1.2, i clienti riscontreranno problemi di recapito dei messaggi, tra cui il rimbalzo dell’e-mail al mittente originario.

**Consegna e-mail** si riferisce al set di caratteristiche che determinano la capacità di un messaggio di raggiungere la sua destinazione, tramite un indirizzo e-mail personale, in un breve periodo di tempo e con la qualità prevista in termini di contenuto e formato. Queste caratteristiche rientrano in quattro categorie principali: qualità dei dati, messaggi e contenuti, infrastruttura di invio e reputazione. Insieme, costituiscono la base di un programma di recapito messaggi e-mail di successo.

La **tasso di consegna** è il numero di messaggi che hanno colpito le caselle in entrata dei destinatari rispetto al numero di messaggi inviati. Dipende da numerosi fattori, in particolare:

* Lamentele di spam limitate
* Bassi tassi di rimbalzo
* Qualità degli indirizzi interessati
* Contenuto del messaggio
* reputazione del mittente

Ottimizzazione del recapito messaggi [!DNL Journey Optimizer] esperienze, consigliamo di utilizzare le best practice elencate in questa sezione. I problemi di recapito sono generalmente collegati alla protezione contro lo spam implementata dai provider di servizi Internet (ISP) e dagli amministratori dei server di posta.

Per informazioni più approfondite su cosa sia il recapito messaggi e per ulteriori informazioni su termini, concetti e approcci chiave per il recapito messaggi, consulta [Guida alle best practice per il recapito messaggi di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=it){target="_blank"}.

## Riduzione del tasso di reclamo {#reduce-complaint-rate}

Gli ISP di solito hanno un modo prominente di segnalare un messaggio ricevuto come spam. Questo permette di identificare fonti inaffidabili. Rispettando rapidamente le richieste di rinuncia e mostrando quindi che sei un mittente affidabile, puoi ridurre i tassi di reclamo. [Ulteriori informazioni sulla gestione delle rinunce](../privacy/opt-out.md#opt-out-management).

Come regola generale, non cercare di ostacolare i destinatari che desiderano rinunciare richiedendo loro di compilare campi come ad esempio il loro indirizzo e-mail o nome. La pagina di destinazione per l’annullamento dell’abbonamento deve avere un solo pulsante di convalida.

Presta ulteriore attenzione quando richiedi ulteriore conferma: un utente può avere due indirizzi e-mail reindirizzati alla stessa casella (ad esempio: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se il profilo è in grado di ricordare solo il primo indirizzo e desidera annullare l’iscrizione tramite un messaggio inviato all’altro, questo verrà rifiutato dal modulo perché l’identificatore crittografato e l’indirizzo e-mail inserito non corrisponderanno.

## Sfruttare gli elenchi di soppressione {#suppression-lists}

[!DNL Journey Optimizer] gestisce una lista di soppressione che raccoglie reclami di spam, rimbalzi duri e rimbalzi morbidi che si verificano in modo coerente.

Per proteggere il recapito messaggi, i destinatari i cui indirizzi si trovano nell’elenco di soppressione sono esclusi per impostazione predefinita da tutte le consegne future, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio.

[Ulteriori informazioni sull&#39;elenco di soppressione](suppression-list.md).

## Utilizzare gli strumenti di monitoraggio {#monitoring-tools}

Utilizzare le funzioni offerte da [!DNL Journey Optimizer] per monitorare il recapito messaggi.

La **[!UICONTROL Esecuzioni]** la scheda dell’elenco dei messaggi ti consente di controllare le prestazioni delle consegne attraverso un set di indicatori in tempo reale. Questa scheda mostra, tra l’altro:
* Numero di messaggi eseguiti, inviati e consegnati correttamente.
* Il numero di messaggi aperti e il numero di messaggi o collegamenti su cui è stato fatto clic.

## Adattare il contenuto dei messaggi {#adapt-message-content}

In misura minore, il contenuto di alcuni messaggi può essere rilevato come spam.

Per migliorare il tasso di recapito messaggi e assicurarsi che le e-mail raggiungano i destinatari, segui i principi riportati di seguito durante la progettazione del contenuto del messaggio:

* **Nome e indirizzo del mittente**: L&#39;indirizzo deve identificare esplicitamente il mittente. Il dominio deve essere di proprietà e registrato al mittente. Il registro di dominio non deve essere privatizzato.

* **Annulla l’abbonamento e la pagina di destinazione**: Il collegamento di annullamento dell’abbonamento è essenziale. Deve essere visibile e valido e il modulo deve essere funzionale.

[Ulteriori informazioni sulla progettazione del contenuto delle e-mail](../email/get-started-email-design.md).

## Stabilisci la tua reputazione come mittente

Se ti sei recentemente trasferito in un altro provider di servizi e-mail, indirizzo IP o dominio e-mail o sottodominio, devi stabilire la tua reputazione come mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella spam della cassetta postale dei destinatari.

Per scaldare l’IP, puoi gradualmente aumentare il numero delle consegne. Vedi questo [caso d&#39;uso](../building-journeys/ramp-up-deliveries-uc.md).
