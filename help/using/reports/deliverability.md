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

Il recapito messaggi misura il successo delle consegne che raggiungono le caselle in entrata dei destinatari.

>[!NOTE]
>
>Per i clienti che acquistano la licenza di Healthcare Shield, Adobe utilizza Transport Layer Security (TLS) 1.2 per proteggere lo scambio di dati tra i sistemi degli utenti (destinatari) e Journey Optimizer (mittente). Se il server di posta ricevente non supporta TLS 1.2, i clienti riscontreranno problemi di recapito, inclusa la recapito dell’e-mail al mittente di origine.

**Recapito messaggi e-mail** si riferisce all’insieme di caratteristiche che determinano la capacità di un messaggio di raggiungere la sua destinazione, tramite un indirizzo e-mail personale, in un breve lasso di tempo e con la qualità prevista in termini di contenuto e formato. Queste caratteristiche si suddividono in quattro categorie principali: qualità dei dati, messaggi e contenuti, infrastruttura di invio e reputazione. Insieme, costituiscono la base di un programma di consegna e-mail di successo.

Il **tasso di consegna** è il numero di messaggi che raggiungono le caselle in entrata dei destinatari rispetto al numero di messaggi consegnati. Dipende da numerosi fattori, in particolare:

* Reclami limitati di spam
* Basse percentuali di mancati recapiti permanenti
* Qualità degli indirizzi target
* Contenuto del messaggio
* Reputazione mittente

Ottimizzare il recapito messaggi [!DNL Journey Optimizer] esperienze, consigliamo di utilizzare le best practice elencate in questa sezione. I problemi di recapito dei messaggi sono generalmente legati alla protezione contro la posta indesiderata implementata dai provider di servizi Internet (ISP) e dagli amministratori dei server di posta.

Per informazioni più approfondite sulla consegna dei messaggi e per ulteriori informazioni sui termini, i concetti e gli approcci chiave, consulta [Guida alle procedure consigliate per la consegna dei messaggi di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=it){target="_blank"}.

## Riduci la percentuale di reclami {#reduce-complaint-rate}

Gli ISP di solito dispongono di un mezzo importante per segnalare un messaggio ricevuto come spam. In questo modo è possibile individuare fonti inaffidabili. Rispettando rapidamente le richieste di rinuncia e dimostrando quindi di essere un mittente affidabile, puoi ridurre la percentuale di reclami. [Ulteriori informazioni sulla gestione delle rinunce](../privacy/opt-out.md#opt-out-management).

Come regola generale, non cercare di intralciare i destinatari che desiderano rinunciare richiedendo loro di compilare campi come il loro indirizzo e-mail o nome, ad esempio. La pagina di destinazione per l’annullamento dell’abbonamento deve avere un solo pulsante di convalida.

Presta particolare attenzione quando richiedi una conferma aggiuntiva: un utente può avere due indirizzi e-mail reindirizzati alla stessa casella (ad esempio: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se il profilo è in grado di ricordare solo il primo indirizzo e desidera annullare l’abbonamento tramite un messaggio inviato all’altro, il modulo lo rifiuterà perché l’identificatore crittografato e l’indirizzo e-mail inserito non corrisponderanno.

## Sfruttare gli elenchi di soppressione {#suppression-lists}

[!DNL Journey Optimizer] gestisce un elenco di soppressione che raccoglie i reclami di spam, i mancati recapiti permanenti e i mancati recapiti non permanenti che si verificano in modo coerente.

Per proteggere il recapito messaggi, i destinatari i cui indirizzi sono inclusi nell’elenco di soppressione sono esclusi per impostazione predefinita da tutte le consegne future, perché l’invio a tali contatti potrebbe danneggiare la reputazione del mittente.

[Ulteriori informazioni sull’elenco di soppressione](suppression-list.md).

## Utilizzare gli strumenti di monitoraggio {#monitoring-tools}

Utilizza le funzioni offerte da [!DNL Journey Optimizer] per monitorare il recapito messaggi.

Il **[!UICONTROL Esecuzioni]** dell’elenco dei messaggi ti consente di controllare le prestazioni delle consegne tramite una serie di indicatori in tempo reale. Questa scheda mostra, tra l’altro:
* Il numero di messaggi eseguiti, inviati e consegnati correttamente.
* Il numero di messaggi aperti e il numero di messaggi/collegamenti su cui è stato fatto clic.

## Adattare il contenuto del messaggio {#adapt-message-content}

In misura minore, il contenuto di determinati messaggi può essere rilevato come spam.

Per migliorare il tasso di recapito dei messaggi e assicurarti che le e-mail arrivino ai destinatari, segui i principi riportati di seguito durante la progettazione del contenuto del messaggio:

* **Nome e indirizzo del mittente**: l’indirizzo deve identificare esplicitamente il mittente. Il dominio deve essere di proprietà del mittente e deve essere registrato presso di esso. Impossibile privatizzare il Registro di sistema del dominio.

* **Collegamento e pagina di destinazione per annullare l’abbonamento**: il collegamento per annullare l’abbonamento è essenziale. Deve essere visibile e valido e il modulo deve essere funzionale.

[Ulteriori informazioni sulla progettazione di contenuti e-mail](../email/get-started-email-design.md).

## Stabilisci la tua reputazione di mittente

Se recentemente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, devi stabilire la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella di posta indesiderata della cassetta postale dei destinatari.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Vedi questo [caso d’uso](../building-journeys/ramp-up-deliveries-uc.md).
