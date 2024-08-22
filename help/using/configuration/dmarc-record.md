---
solution: Journey Optimizer
product: journey optimizer
title: Record DMARC
description: Scopri come impostare il record DMARC in Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, dominio, posta, dmarc, record
exl-id: f9e217f8-5aa8-4d3a-96fc-65defcb5d340
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 12%

---

# Record DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Impostare il record DMARC"
>abstract="DMARC è un metodo di autenticazione delle e-mail che consente ai proprietari di dominio di proteggerlo da utilizzi non autorizzati ed evitare problemi di recapitabilità con i provider di posta elettronica.<br>Come parte dell’applicazione delle best practice del settore, Google e Yahoo richiedono entrambi di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail."

## Che cos&#39;è DMARC? {#what-is-dmarc}

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati. Offrendo una politica chiara ai provider di posta elettronica e di servizi Internet (ISP), aiuta a evitare che gli attori malintenzionati inviino e-mail che affermano di appartenere al tuo dominio. L’implementazione di DMARC riduce il rischio che le e-mail legittime vengano contrassegnate come spam o vengano rifiutate, inoltre migliora il recapito dei messaggi e-mail.

DMARC offre anche rapporti sui messaggi che non superano l’autenticazione, oltre al controllo sulla gestione delle e-mail che non superano la convalida DMARC. A seconda dei [criteri DMARC](#dmarc-policies) implementati, queste e-mail possono essere monitorate, messe in quarantena o rifiutate. Queste funzionalità consentono di intraprendere azioni per mitigare e risolvere potenziali errori.

Per evitare problemi di recapito messaggi e ottenere il controllo dei messaggi che non riescono a eseguire l&#39;autenticazione, [!DNL Journey Optimizer] ora supporta la tecnologia DMARC direttamente nell&#39;interfaccia di amministrazione. [Ulteriori informazioni](#implement-dmarc)

### Come funziona DMARC? {#how-dmarc-works}

SPF e DKIM vengono entrambi utilizzati per associare un’e-mail a un dominio e collaborare per l’autenticazione dell’e-mail. DMARC compie un ulteriore passo avanti e aiuta a prevenire lo spoofing facendo corrispondere il dominio controllato da DKIM e SPF.

>[!NOTE]
>
>In Journey Optimizer, SPF e DKIM sono configurati per te.

Per passare il DMARC, un messaggio deve trasmettere SPF o DKIM:

* SPF (Sender Policy Framework) consente di verificare che il messaggio di posta elettronica provenga da una fonte autorizzata controllando l&#39;indirizzo IP del server di invio rispetto a un elenco di indirizzi IP autorizzati per il dominio.
* DKIM (DomainKeys Identified Mail) aggiunge una firma digitale ai messaggi e-mail, consentendo al destinatario di verificarne l’integrità e l’autenticità.

In caso di errore di autenticazione di entrambe o di una di queste, DMARC avrà esito negativo e l’e-mail verrà consegnata in base ai criteri DMARC selezionati.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Criteri DMARC {#dmarc-policies}

Se l&#39;autenticazione DMARC di un messaggio e-mail non riesce, puoi decidere quale azione verrà applicata al messaggio. DMARC dispone di tre opzioni:

* Monitoraggio (p=none): indica al provider di cassette postali/ISP di eseguire le operazioni normalmente eseguite sul messaggio.
* Quarantena (p=quarantena): indica al provider della cassetta postale o all&#39;ISP di recapitare messaggi che non passano DMARC alla cartella di posta indesiderata o indesiderata del destinatario.
* Rifiuta (p=rifiuta): indica al provider di cassette postali/ISP di bloccare la posta che non passa DMARC causando un mancato recapito.

>[!NOTE]
>
>Scopri come impostare i criteri DMARC con [!DNL Journey Optimizer] in [questa sezione](#set-up-dmarc).

## Aggiornamento requisiti DMARC {#dmarc-update}

Come parte delle best practice di settore, Google e Yahoo! richiedono entrambi di disporre di un **record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito si applica a partire dal **1° febbraio 2024**.

>[!CAUTION]
>
>Non rispettare questo nuovo requisito da parte di Gmail e Yahoo! dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata oppure il blocco.

Di conseguenza, Adobe consiglia vivamente di effettuare le seguenti operazioni:

* Assicurati di avere **record DMARC** configurato per **tutti i sottodomini già delegati** all&#39;Adobe in [!DNL Journey Optimizer]. [Scopri come](#check-subdomains-for-dmarc)

* Quando **si delega un nuovo sottodominio** ad Adobe, è possibile **configurare DMARC** direttamente **nell&#39;interfaccia di amministrazione [!DNL Journey Optimizer]**. [Scopri come](#implement-dmarc)

## Implementare DMARC in [!DNL Journey Optimizer] {#implement-dmarc}

L&#39;interfaccia di amministrazione [!DNL Journey Optimizer] consente di impostare il record DMARC per tutti i sottodomini già delegati o che si sta delegando ad Adobe. I passaggi dettagliati sono descritti di seguito.

### Verifica la presenza di DMARC nei sottodomini esistenti {#check-subdomains-for-dmarc}

Per verificare che il record DMARC sia impostato per tutti i sottodomini delegati in [!DNL Journey Optimizer], eseguire la procedura seguente.

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**, quindi fai clic su **[!UICONTROL Configura sottodominio]**.

1. Per ogni sottodominio delegato, controlla la colonna **[!UICONTROL Record DMARC]**. Se non è stato trovato alcun record per un determinato sottodominio, viene visualizzato un avviso.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Per soddisfare i nuovi requisiti di Gmail e Yahoo! ed evitare problemi di recapito messaggi con i principali ISP, si consiglia di impostare un record DMARC per tutti i sottodomini delegati. [Ulteriori informazioni](dmarc-record-update.md)

1. Seleziona un sottodominio a cui non è associato alcun record DMARC e compila la sezione **[!UICONTROL Record DMARC]** in base alle esigenze della tua organizzazione. I passaggi per compilare i campi del record DMARC sono descritti in [questa sezione](#implement-dmarc).

1. Considera le due opzioni seguenti:

   * Se stai modificando un sottodominio configurato con [CNAME](delegate-subdomain.md#cname-subdomain-delegation), devi copiare il record DNS per DMARC nella soluzione di hosting per generare i record DNS corrispondenti.

     ![](assets/dmarc-record-edit-cname.png)

     Assicurati che il record DNS sia stato generato nella soluzione di hosting del tuo dominio e seleziona la casella &quot;Confermo...&quot;.

   * Se stai modificando un sottodominio [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, compila semplicemente i campi **[!UICONTROL record DMARC]** descritti in [questa sezione](#implement-dmarc). Non sono necessarie ulteriori azioni.

     ![](assets/dmarc-record-edit-full.png)

1. Salva le modifiche.

### Configurare DMARC per i nuovi sottodomini {#set-up-dmarc}

Quando si delegano nuovi sottodomini ad Adobe in [!DNL Journey Optimizer], verrà creato un record DMARC in DNS per il dominio. Per implementare DMARC, segui i passaggi indicati di seguito.

>[!CAUTION]
>
>Per soddisfare i nuovi requisiti di Gmail e Yahoo! ed evitare problemi di recapito messaggi con i principali ISP, si consiglia di impostare un record DMARC per tutti i sottodomini delegati. [Ulteriori informazioni](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Configura un nuovo sottodominio. [Scopri come](delegate-subdomain.md)

1. Passare alla sezione **[!UICONTROL Record DMARC]**.

   Se il sottodominio ha un record DMARC esistente e viene recuperato da [!DNL Journey Optimizer], è possibile utilizzare gli stessi valori evidenziati nell&#39;interfaccia o modificarli in base alle esigenze.

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >Se non aggiungi alcun valore, verranno utilizzati i valori predefiniti precompilati.

1. Definire l&#39;azione che il server destinatario eseguirà se DMARC non riesce. A seconda dei [criteri DMARC](#dmarc-policies) che si desidera applicare, selezionare una delle tre opzioni seguenti:

   * **[!UICONTROL Nessuno]** (valore predefinito): indica al destinatario di non eseguire azioni sui messaggi che non superano l&#39;autenticazione DMARC, ma di inviare comunque i report e-mail al mittente.
   * **[!UICONTROL Quarantena]**: indica al server e-mail ricevente di mettere in quarantena l&#39;e-mail che non riesce l&#39;autenticazione DMARC. Ciò in genere significa inserire tali messaggi nella cartella di posta indesiderata o indesiderata del destinatario.
   * **[!UICONTROL Rifiuta]**: indica al destinatario di negare completamente (non recapitare) qualsiasi messaggio e-mail per il dominio che non supera l&#39;autenticazione. Con questo criterio abilitato, solo i messaggi e-mail verificati come autenticati al 100% dal dominio avranno anche la possibilità di inserire messaggi nella casella in entrata.

   >[!NOTE]
   >
   >Come best practice, si consiglia di eseguire il rollout dell&#39;implementazione DMARC eseguendo l&#39;escalation dei criteri DMARC da **None** a **Quarantine** e a **Rifiuta** per comprendere il potenziale impatto di DMARC.

1. Facoltativamente, aggiungi uno o più indirizzi e-mail di tua scelta per indicare dove **rapporti DMARC** nelle e-mail che [non riescono a eseguire l&#39;autenticazione](#how-dmarc-works) devono essere inviati all&#39;interno della tua organizzazione. Puoi aggiungere fino a cinque indirizzi per ogni rapporto.

   >[!NOTE]
   >
   >Assicurati di avere una casella in entrata autentica (non Adobe) nel controllo in cui puoi ricevere tali rapporti.

   Esistono due diversi rapporti generati dagli ISP che i mittenti possono ricevere tramite i tag RUA/RUF nei loro criteri DMARC:

   * **Rapporti aggregati** (RUA): non contengono dati PII (personalmente identificabili) che potrebbero essere sensibili ai requisiti RGPD.
   * **Rapporti sugli errori forensi** (RUF): contengono indirizzi e-mail sensibili ai requisiti RGPD. Prima di utilizzare, controlla internamente come gestire le informazioni che devono essere conformi ai requisiti RGPD.

   >[!NOTE]
   >
   >Questi rapporti altamente tecnici forniscono una panoramica delle e-mail che vengono tentate di spoofing. È consigliabile digerirli attraverso uno strumento di terze parti.

1. Seleziona la **percentuale applicabile** di e-mail per DMARC.

   Questa percentuale dipende dalla fiducia nell’infrastruttura e-mail e dalla tolleranza per i falsi positivi (le e-mail legittime vengono contrassegnate come fraudolente). In genere le organizzazioni iniziano con i criteri DMARC impostati su **Nessuno**, aumentano gradualmente la percentuale di criteri DMARC e monitorano attentamente l&#39;impatto sulla consegna di e-mail legittime.

   >[!NOTE]
   >
   >Collabora con i tuoi amministratori e-mail e il team IT per aumentare gradualmente la percentuale man mano che acquisisci fiducia nelle tue pratiche di autenticazione e-mail.

   Come best practice, è consigliabile ottenere un tasso di conformità DMARC elevato, idealmente vicino al 100%, per ottimizzare i vantaggi in termini di sicurezza e ridurre al minimo il rischio di falsi positivi.

1. Seleziona un **intervallo di reporting** compreso tra 24 e 168 ore. Consente ai proprietari del dominio di ricevere aggiornamenti regolari sui risultati dell’autenticazione e-mail e di intraprendere le azioni necessarie per migliorare la sicurezza e-mail.

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->
