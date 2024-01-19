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
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Record DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Impostare il record DMARC"
>abstract="Imposta il record DMARC per evitare problemi di consegna con gli ISP. Come parte delle procedure ottimali di settore, Google e Yahoo richiedono entrambi di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail."

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

Di conseguenza, Adobe consiglia vivamente di disporre di un record DMARC configurato per tutti i sottodomini a cui hai delegato l’Adobe in [!DNL Journey Optimizer]. Segui una delle due opzioni seguenti:

* Configurare DMARC nei sottodomini o nel dominio principale dei sottodomini; **nella soluzione di hosting**.

* Configurare DMARC nei sottodomini delegati **utilizzo della nuova funzionalità in [!DNL Journey Optimizer] interfaccia utente di amministrazione** - senza alcun lavoro aggiuntivo sulla soluzione di hosting. [Ulteriori informazioni](#implement-dmarc)

  >[!CAUTION]
  >
  >Se hai impostato [Delega CNAME](delegate-subdomain.md#cname-subdomain-delegation) per i sottodomini di invio, sarà necessario anche un certo numero di ingressi nella soluzione di hosting. Assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l&#39;aggiornamento non appena [!DNL Journey Optimizer] (il 30 gennaio 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>Ulteriori informazioni sull&#39;implementazione di DMARC in [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} per comprendere meglio l’impatto sul recapito messaggi e-mail.

## Che cos&#39;è DMARC?

DMARC, che sta per **Autenticazione, reporting e conformità dei messaggi basati su dominio**, è un protocollo di autenticazione e-mail che aiuta a proteggere da spoofing delle e-mail, phishing e altre attività fraudolente.

* Autenticazione e-mail:

   * SPF (Sender Policy Framework): DMARC si basa su SPF per autenticare l&#39;identità del server di posta elettronica di invio. SPF consente di verificare che il messaggio e-mail provenga da un’origine autorizzata controllando l’indirizzo IP del server di invio in base a un elenco di indirizzi IP autorizzati per il dominio.
   * DKIM (DomainKeys Identified Mail): DMARC utilizza anche DKIM per aggiungere una firma digitale ai messaggi e-mail, consentendo al destinatario di verificarne l’integrità e l’autenticità.

* DMARC impedisce ad attori dannosi di inviare e-mail che sembrano provenire dal tuo dominio. Configurando il DMARC, puoi specificare in che modo i provider di posta elettronica devono gestire i messaggi che non superano i controlli di autenticazione, riducendo la probabilità che le e-mail di phishing raggiungano i destinatari.

* DMARC aiuta a migliorare il recapito messaggi e-mail fornendo una chiara policy che i provider e-mail possono seguire quando si incontrano messaggi che affermano di provenire dal tuo dominio. Questo può ridurre le possibilità che le e-mail legittime vengano contrassegnate come spam o rifiutate.

* Implementando DMARC, puoi proteggere la reputazione del tuo marchio assicurandoti che le parti non autorizzate non possano abusare del tuo dominio per phishing o altre attività dannose. Ciò è particolarmente importante per le aziende e le organizzazioni che si affidano alla comunicazione via e-mail con clienti e partner.

L&#39;impostazione di un record DMARC comporta l&#39;aggiunta di un record TXT DNS alle impostazioni DNS del dominio. Questo record specifica i criteri DMARC, ad esempio se mettere in quarantena o rifiutare i messaggi che non superano l&#39;autenticazione. L’implementazione di DMARC è un passaggio proattivo per migliorare la sicurezza delle e-mail e proteggere l’organizzazione e i destinatari dalle minacce basate su e-mail.

## Implementazione DMARC {#implement-dmarc}

* Se non aggiungi DMARC, verrai messo in quarantena (almeno).

* Assicurati di disporre di una casella in entrata autentica in cui ricevere il controllo: gestisci questa casella in entrata (non dovrebbe essere una casella in entrata Adobe)

La raccomandazione è 24 perché in generale questo è ciò che hanno gli ISP.
se meno, valuta la capacità / controlla il tuo > chat GPT

Se viene rilevato un record DMARC, è possibile copiare e incollare gli stessi valori elencati o modificarli, se necessario.

Se non si inserisce alcun valore, verranno utilizzati i valori predefiniti.

### Sottodomini completamente delegati

### Sottodomini delegati tramite CNAME

per CNAME nel flusso dell’edizione è necessario scaricare nuovamente il file CSV (non per una delega completa)





