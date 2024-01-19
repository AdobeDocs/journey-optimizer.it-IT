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
source-git-commit: 49cb9734d66dc1aa2a3531c71a687aac00834d82
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Record DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Impostare il record DMARC"
>abstract="Imposta il record DMARC per evitare problemi di recapito messaggi con gli ISP"

>[!CAUTION]
>
>A seguito dei recenti annunci Gmail e Yahoo per mittenti in blocco, Journey Optimizer ora supporta la tecnologia di autenticazione DMARC. //È necessario aggiornare tutti i sottodomini già creati nell’istanza per includere il supporto DMARC.//

È importante farlo entro il 1° febbraio. Il doc arriverà presto

A partire dal

Sono disponibili 2 opzioni:

* Per eseguire questa operazione da soli: è possibile configurarla con il reparto IT in qualsiasi momento

* Fallo in AJO - ma in questo caso è necessario aspettare fino al 30 gennaio

   * Delega completa: puoi farlo il 30 gennaio (versione AJO)

   * CNAME pianifica il progetto con il reparto IT in modo da non richiedere tempo, ma è necessario pianificarlo

Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno entrambi di avere un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito inizia il **1 febbraio 2024**.

Ulteriori informazioni sui requisiti di Google e Yahoo per il record DMARC in [questa sezione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Ulteriori informazioni sulle modifiche annunciate in Google e Yahoo su [questa pagina](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, che sta per **Autenticazione, reporting e conformità dei messaggi basati su dominio**, è un protocollo di autenticazione e-mail che aiuta a proteggere da spoofing delle e-mail, phishing e altre attività fraudolente.

* Autenticazione e-mail:

   * SPF (Sender Policy Framework): DMARC si basa su SPF per autenticare l&#39;identità del server di posta elettronica di invio. SPF consente di verificare che il messaggio e-mail provenga da un’origine autorizzata controllando l’indirizzo IP del server di invio in base a un elenco di indirizzi IP autorizzati per il dominio.
   * DKIM (DomainKeys Identified Mail): DMARC utilizza anche DKIM per aggiungere una firma digitale ai messaggi e-mail, consentendo al destinatario di verificarne l’integrità e l’autenticità.

* DMARC impedisce ad attori dannosi di inviare e-mail che sembrano provenire dal tuo dominio. Configurando il DMARC, puoi specificare in che modo i provider di posta elettronica devono gestire i messaggi che non superano i controlli di autenticazione, riducendo la probabilità che le e-mail di phishing raggiungano i destinatari.

* DMARC aiuta a migliorare il recapito messaggi e-mail fornendo una chiara policy che i provider e-mail possono seguire quando si incontrano messaggi che affermano di provenire dal tuo dominio. Questo può ridurre le possibilità che le e-mail legittime vengano contrassegnate come spam o rifiutate.

* Implementando DMARC, puoi proteggere la reputazione del tuo marchio assicurandoti che le parti non autorizzate non possano abusare del tuo dominio per phishing o altre attività dannose. Ciò è particolarmente importante per le aziende e le organizzazioni che si affidano alla comunicazione via e-mail con clienti e partner.

L&#39;impostazione di un record DMARC comporta l&#39;aggiunta di un record TXT DNS alle impostazioni DNS del dominio. Questo record specifica i criteri DMARC, ad esempio se mettere in quarantena o rifiutare i messaggi che non superano l&#39;autenticazione. L’implementazione di DMARC è un passaggio proattivo per migliorare la sicurezza delle e-mail e proteggere l’organizzazione e i destinatari dalle minacce basate su e-mail.

[Per ulteriori informazioni su DMARC, consulta la Guida alle best practice per la consegna dei messaggi.](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} per comprendere meglio l’impatto di DMARC sul recapito messaggi e-mail.

Se non aggiungi DMARC, verrai messo in quarantena (almeno).

verifica di disporre di una casella in entrata autentica da cui ricevere il controllo. gestisci questa casella in entrata (non dovrebbe essere una casella in entrata Adobe)

Il consiglio è di 24 perché generalmente, se inferiore, valuta la capacità / controlla il > chat GPT

Google e Yahoo, e probabilmente tutti gli altri ISP principali

per CNAME nel flusso dell’edizione è necessario scaricare nuovamente il file CSV (non per una delega completa)

nuovo record DMARC

In RN > Inserisci per primo Tutti i sottodomini devono essere aggiornati con il supporto DMARC



