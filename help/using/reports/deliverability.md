---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla recapitabilità
description: Scopri le linee guida per il recapito messaggi
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: e34c39c02f71361277f28b1a116a54390875f93d
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 1%

---

# Introduzione alla recapitabilità {#manage-deliverability}

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

Per informazioni più approfondite sulla consegna dei messaggi e per ulteriori informazioni sui termini, i concetti e gli approcci chiave, consulta [Guida alle procedure consigliate per la consegna dei messaggi di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html){target="_blank"}.

## Riduci la percentuale di reclami {#reduce-complaint-rate}

Gli ISP di solito dispongono di un mezzo importante per segnalare un messaggio ricevuto come spam. In questo modo è possibile individuare fonti inaffidabili. Rispettando rapidamente le richieste di rinuncia e dimostrando quindi di essere un mittente affidabile, puoi ridurre la percentuale di reclami. [Ulteriori informazioni sulla gestione delle rinunce](../privacy/opt-out.md#opt-out-management)

Come regola generale, non cercare di intralciare i destinatari che desiderano rinunciare richiedendo loro di compilare campi come il loro indirizzo e-mail o nome, ad esempio. La pagina di destinazione per l’annullamento dell’abbonamento deve avere un solo pulsante di convalida.

Presta particolare attenzione quando richiedi una conferma aggiuntiva: un utente può avere due indirizzi e-mail reindirizzati alla stessa casella (ad esempio: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se il profilo è in grado di ricordare solo il primo indirizzo e desidera annullare l’abbonamento tramite un messaggio inviato all’altro, il modulo lo rifiuterà perché l’identificatore crittografato e l’indirizzo e-mail inserito non corrisponderanno.

## Sfruttare gli elenchi di soppressione {#suppression-lists}

[!DNL Journey Optimizer] gestisce un elenco di soppressione che raccoglie i reclami di spam, i mancati recapiti permanenti e i mancati recapiti non permanenti che si verificano in modo coerente.

Per proteggere il recapito messaggi, i destinatari i cui indirizzi sono inclusi nell’elenco di soppressione sono esclusi per impostazione predefinita da tutte le consegne future, perché l’invio a tali contatti potrebbe danneggiare la reputazione del mittente.

[Ulteriori informazioni sull’elenco di soppressione](suppression-list.md)

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

[Ulteriori informazioni sulla progettazione di contenuti e-mail](../email/get-started-email-design.md)

## Stabilisci la tua reputazione di mittente {#reputation}

Se recentemente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, devi stabilire la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella di posta indesiderata della cassetta postale dei destinatari.

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## Implementazione DMARC {#dmarc}

Per attenuare il rischio che le e-mail legittime vengano contrassegnate come spam o rifiutate e per evitare problemi di recapito, [!DNL Journey Optimizer] consente di impostare un record DMARC per tutti i sottodomini a cui deleghi Adobe.

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio dall&#39;uso non autorizzato da parte di utenti malintenzionati.

[Ulteriori informazioni sul record DMARC](../configuration/dmarc-record.md)

## Scopri i cicli di feedback {#feedback-loops}

Un feedback loop (FBL) è un servizio offerto da alcuni ISP che consente al mittente dell’e-mail di ricevere automaticamente una notifica quando l’utente che riceve un’e-mail sceglie di contrassegnarla come spam (noto anche come &quot;reclamo&quot;).

Dopo che un utente finale genera un reclamo che viene rimandato all&#39;Adobe dall&#39;ISP, l&#39;indirizzo e-mail viene aggiunto automaticamente al [elenco di soppressione](../reports/suppression-list.md) ed esclusi dalle consegne future. In effetti, l’invio di e-mail agli utenti che le hanno contrassegnate come spam influisce negativamente sulla reputazione del mittente e può causare problemi di recapito messaggi. [Ulteriori informazioni sui reclami di spam](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Non tutti gli ISP forniscono un FBL tradizionale, come ad esempio Gmail. Gmail non offre feedback a livello individuale e non può essere utilizzato per tenere traccia dei reclami spam per singoli destinatari, concentrandosi invece sul reporting a livello aggregato all’interno dei loro strumenti Google Postmaster. [Ulteriori informazioni](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Tutti i clienti Adobe vengono automaticamente iscritti ai FBL tradizionali dei seguenti ISP:

* 1&amp;1

* AOL

* Cravatta blu

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (violoncello, UPC, Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackspace

* SEZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* Telecom Italia

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* Elementi multimediali vergini

* Yahoo

* Ziggo

L’Adobe controlla regolarmente questi FBL per garantire che vengano aggiunti i più recenti FBL disponibili.
