---
title: Monitoraggio dell’esecuzione dei messaggi
description: Informazioni sul monitoraggio e sulle linee guida per il recapito messaggi
feature: Consegna
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Gestire il recapito messaggi {#manage-deliverability}

![](assets/do-not-localize/badge.png)

Il recapito messaggi è una misura del successo delle consegne nelle caselle in entrata dei destinatari.

**La** consegna e-mail si riferisce al set di caratteristiche che determinano la capacità di un messaggio di raggiungere la sua destinazione, tramite un indirizzo e-mail personale, entro un breve periodo di tempo e con la qualità prevista in termini di contenuto e formato. Queste caratteristiche rientrano in quattro categorie principali: qualità dei dati, messaggi e contenuti, infrastruttura di invio e reputazione. Insieme, costituiscono la base di un programma di recapito messaggi e-mail di successo.

Il **tasso di recapito** è il numero di messaggi che hanno colpito le caselle in entrata dei destinatari rispetto al numero di messaggi inviati. Dipende da numerosi fattori, in particolare:

* Lamentele di spam limitate
* Bassi tassi di rimbalzo
* Qualità degli indirizzi interessati
* Contenuto del messaggio
* reputazione del mittente

Per ottimizzare il recapito messaggi delle esperienze [!DNL Journey Optimizer] , si consiglia di utilizzare le best practice elencate in questa sezione. I problemi di recapito sono generalmente collegati alla protezione contro lo spam implementata dai provider di servizi Internet (ISP) e dagli amministratori dei server di posta.

## Riduzione del tasso di reclamo {#reduce-complaint-rate}

Gli ISP di solito hanno un modo prominente di segnalare un messaggio ricevuto come spam. Questo permette di identificare fonti inaffidabili. Rispettando rapidamente le richieste di rinuncia e mostrando quindi che sei un mittente affidabile, puoi ridurre i tassi di reclamo. [Ulteriori informazioni sulla gestione](consent.md#opt-out-management) delle rinunce.

Come regola generale, non cercare di ostacolare i destinatari che desiderano rinunciare richiedendo loro di compilare campi come ad esempio il loro indirizzo e-mail o nome. La pagina di destinazione per l’annullamento dell’abbonamento deve avere un solo pulsante di convalida.

Presta ulteriore attenzione quando richiedi ulteriore conferma: un utente può avere due indirizzi e-mail reindirizzati alla stessa casella (ad esempio: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se il profilo è in grado di ricordare solo il primo indirizzo e desidera annullare l’iscrizione tramite un messaggio inviato all’altro, questo verrà rifiutato dal modulo perché l’identificatore crittografato e l’indirizzo e-mail inserito non corrisponderanno.

## Sfruttare gli elenchi di soppressione {#suppression-lists}

[!DNL Journey Optimizer] gestisce una lista di soppressione che raccoglie reclami di spam, rimbalzi duri e rimbalzi morbidi che si verificano in modo coerente.

Per proteggere il recapito messaggi, i destinatari i cui indirizzi si trovano nell’elenco di soppressione sono esclusi per impostazione predefinita da tutte le consegne future, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio.

[Ulteriori informazioni sull&#39;elenco](suppression-list.md) di soppressione.

## Utilizzare gli strumenti di monitoraggio {#monitoring-tools}

Utilizza le funzioni offerte da [!DNL Journey Optimizer] per monitorare il recapito messaggi.

La scheda **[!UICONTROL Executions]** dell’elenco dei messaggi ti consente di controllare le prestazioni delle consegne tramite un set di indicatori in tempo reale. Questa scheda mostra, tra l’altro:
* Numero di messaggi eseguiti, inviati e consegnati correttamente.
* Il numero di messaggi aperti e il numero di messaggi o collegamenti su cui è stato fatto clic.

[Ulteriori informazioni sul monitoraggio dell’esecuzione](message-monitoring.md) dei messaggi.

## Adatta il contenuto del messaggio {#adapt-message-content}

In misura minore, il contenuto di alcuni messaggi può essere rilevato come spam.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Per migliorare il tasso di recapito messaggi e assicurarsi che le e-mail raggiungano i destinatari, segui i principi riportati di seguito durante la progettazione del contenuto del messaggio:

* **Nome e indirizzo** del mittente: L&#39;indirizzo deve identificare esplicitamente il mittente. Il dominio deve essere di proprietà e registrato al mittente. Il registro di dominio non deve essere privatizzato.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Annulla sottoscrizione collegamento e pagina** di destinazione: Il collegamento di annullamento dell’abbonamento è essenziale. Deve essere visibile e valido e il modulo deve essere funzionale.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Ulteriori informazioni sulla progettazione del contenuto](design-emails.md) e-mail.
