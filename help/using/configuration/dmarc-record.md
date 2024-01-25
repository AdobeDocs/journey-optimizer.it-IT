---
solution: Journey Optimizer
product: journey optimizer
title: Record DMARC
description: Scopri come impostare il record DMARC in Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, dominio, posta, dmarc, record
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 5%

---

# Record DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Impostare il record DMARC"
>abstract="Imposta il record DMARC per evitare problemi di recapito con gli ISP. Come parte dell’applicazione delle best practice del settore, Google e Yahoo richiedono entrambi di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail."

>[!CAUTION]
>
>A seguito dei recenti annunci Gmail e Yahoo per mittenti in blocco, Journey Optimizer ora supporta la tecnologia di autenticazione DMARC.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno che tu abbia un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito inizia il **1 febbraio 2024**.

Ulteriori informazioni sui requisiti di Google e Yahoo in [questa sezione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Il mancato rispetto di questo nuovo requisito da parte di Gmail e Yahoo dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata o il blocco.

Di conseguenza, Adobe consiglia vivamente di disporre di un record DMARC configurato per tutti i sottodomini a cui hai delegato l’Adobe in [!DNL Journey Optimizer]. Segui i passaggi seguenti che si applicano al tuo caso:

* Se è stato [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, per l’invio dei sottodomini, segui una delle due opzioni seguenti:

   * Configurare DMARC nel dominio principale dei sottodomini delegati **nella soluzione di hosting**.

   * Configurare DMARC nei sottodomini delegati **utilizzo della funzionalità in arrivo in [!DNL Journey Optimizer] interfaccia utente di amministrazione** - senza alcun lavoro aggiuntivo sulla soluzione di hosting.

* Se hai impostato [Delega CNAME](delegate-subdomain.md#cname-subdomain-delegation) per i sottodomini di invio, segui una delle due opzioni seguenti:

   * Configurare DMARC nei sottodomini o nel dominio principale dei sottodomini **nella soluzione di hosting**.

   * Configurare DMARC nei sottodomini delegati **utilizzo della funzionalità in arrivo in [!DNL Journey Optimizer] interfaccia utente di amministrazione**. Tuttavia, richiederà anche l’ingresso nella soluzione di hosting. Di conseguenza, assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l’aggiornamento non appena [!DNL Journey Optimizer] (il 30 gennaio). <!--and be ready on February 1st, 2024-->

**Maggiori dettagli sulla [!DNL Journey Optimizer] La prossima funzionalità di DMARC sarà presto disponibile.**

>[!NOTE]
>
>Ulteriori informazioni sull&#39;implementazione di DMARC in [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} per comprendere meglio l’impatto sul recapito messaggi e-mail.

## Che cos&#39;è DMARC?

DMARC, che sta per **Autenticazione, reporting e conformità dei messaggi basati su dominio**, è un metodo/protocollo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati.

Offrendo un modo per autenticare il dominio del mittente, impedisce ad attori dannosi di inviare e-mail che sembrano provenire dal tuo dominio.

DMARC fornisce inoltre un feedback sullo stato di autenticazione delle e-mail e consente ai mittenti di controllare cosa accade alle e-mail che non superano l’autenticazione. Ciò include opzioni per monitorare, mettere in quarantena o rifiutare la posta a seconda del criterio DMARC implementato.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC dispone di tre opzioni:

* Monitoraggio (p=none): indica al provider di cassette postali/ISP di eseguire le operazioni normalmente eseguite sul messaggio.
* Quarantena (p=quarantena): indica al provider della cassetta postale o all&#39;ISP di recapitare messaggi che non passano DMARC alla cartella di posta indesiderata o indesiderata del destinatario.
* Rifiuta (p=rifiuta): indica al provider di cassette postali/ISP di bloccare la posta che non passa DMARC causando un mancato recapito.

## Come funziona DMARC?

SPF e DKIM vengono entrambi utilizzati per associare un’e-mail a un dominio e collaborare per l’autenticazione dell’e-mail. DMARC compie un ulteriore passo avanti e aiuta a prevenire lo spoofing facendo corrispondere il dominio controllato da DKIM e SPF. Per passare il DMARC, un messaggio deve passare SPF o DKIM. Se entrambe queste operazioni non riescono, l’autenticazione DMARC avrà esito negativo e l’e-mail verrà recapitata in base ai criteri DMARC selezionati.

* SPF (Sender Policy Framework): DMARC si basa su SPF per autenticare l&#39;identità del server di posta elettronica di invio. SPF consente di verificare che il messaggio e-mail provenga da un’origine autorizzata controllando l’indirizzo IP del server di invio in base a un elenco di indirizzi IP autorizzati per il dominio.
* DKIM (DomainKeys Identified Mail): DMARC utilizza anche DKIM per aggiungere una firma digitale ai messaggi e-mail, consentendo al destinatario di verificarne l’integrità e l’autenticità.

>[!NOTE]
>
>DMARC richiede l&#39;allineamento tra l&#39;indirizzo &#39;From&#39; e &#39;Return-Path&#39;.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## Implementazione DMARC {#implement-dmarc}

Per implementare DMARC, segui i passaggi riportati di seguito che si applicano al tuo caso.

* Se non aggiungi DMARC, verrai messo in quarantena (almeno).

### Sottodomini completamente delegati

Impostare l&#39;azione che verrà eseguita dal server dei destinatari se DMARC non riesce.

DMARC dispone di tre opzioni:

* Monitoraggio (p=none): indica al provider di cassette postali/ISP di eseguire le operazioni normalmente eseguite sul messaggio. Questo è il valore predefinito.
* Quarantena (p=quarantena): indica al provider della cassetta postale o all&#39;ISP di recapitare messaggi che non passano DMARC alla cartella di posta indesiderata o indesiderata del destinatario.
* Rifiuta (p=rifiuta): indica al provider di cassette postali/ISP di bloccare la posta che non passa DMARC causando un mancato recapito.

E-mail per ricevere report DMARC aggregati e report di errori DMARC forensi: puoi aggiungere fino a 5 indirizzi.

* Assicurati di disporre di una casella in entrata autentica in cui ricevere il controllo: gestisci questa casella in entrata (non dovrebbe essere una casella in entrata Adobe)

Percentuale applicabile di e-mail per applicare DMARC:

Intervallo di reporting: il consiglio è di 24 perché in genere questo è ciò che hanno gli ISP.
se meno, valuta la capacità / controlla il tuo > chat GPT

Se viene rilevato un record DMARC, è possibile copiare e incollare gli stessi valori elencati o modificarli, se necessario.

Se non si inserisce alcun valore, verranno utilizzati i valori predefiniti.

### Sottodomini delegati tramite CNAME

per CNAME nel flusso dell’edizione è necessario scaricare nuovamente il file CSV (non per una delega completa)





