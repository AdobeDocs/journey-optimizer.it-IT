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
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 11%

---

# Record DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Impostare il record DMARC"
>abstract="DMARC è un metodo di autenticazione delle e-mail che consente ai proprietari di dominio di proteggerlo da utilizzi non autorizzati ed evitare problemi di recapitabilità con i provider di posta elettronica.<br>Come parte dell’applicazione delle best practice del settore, Google e Yahoo richiedono entrambi di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail."

## Cos’è DMARC? {#what-is-dmarc}

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati. Offrendo una politica chiara ai provider di posta elettronica e di servizi Internet (ISP), aiuta a evitare che gli attori malintenzionati inviino e-mail che affermano di appartenere al tuo dominio. L’implementazione di DMARC riduce il rischio che le e-mail legittime vengano contrassegnate come spam o vengano rifiutate, inoltre migliora il recapito dei messaggi e-mail.

DMARC offre anche rapporti sui messaggi che non superano l&#39;autenticazione, insieme al controllo sulla gestione delle e-mail che non superano DMARC convalida. A seconda del regola[&#128279;](#dmarc-policies) DMARC implementato, queste e-mail possono essere monitorate, messe in quarantena o rifiutate. Queste funzionalità consentono di intraprendere azioni per mitigare e risolvere potenziali errori.

Per aiutarti a prevenire problemi di recapito mentre ottieni il controllo sulla posta che non riesce l&#39;autenticazione, [!DNL Journey Optimizer] ora supporta la tecnologia DMARC direttamente nella sua interfaccia di amministrazione. [Ulteriori informazioni](#implement-dmarc)

### Come funziona DMARC? {#how-dmarc-works}

SPF e DKIM vengono entrambi utilizzati per associare un’e-mail a un dominio e collaborare per l’autenticazione delle e-mail. DMARC fa un ulteriore passo in avanti e aiuta a prevenire lo spoofing facendo corrispondere il dominio controllato da DKIM e SPF.

>[!NOTE]
>
>In Journey Optimizer, SPF e DKIM sono configurati per te.

Per passare DMARC, un messaggio deve passare SPF o DKIM:

* SPF (Sender Policy Framework) consente di verificare che il messaggio di posta elettronica provenga da un&#39;origine autorizzata controllando l&#39;indirizzo IP del server di invio rispetto a un elenco di indirizzi IP autorizzati per il dominio.
* DKIM (DomainKeys Identified Mail) aggiunge una firma digitale ai messaggi di posta elettronica, consentendo al destinatario di verificare l&#39;integrità e l&#39;autenticità del messaggio.

Se entrambi o uno di questi falliscono l&#39;autenticazione, DMARC avrà esito negativo e l&#39;e-mail verrà consegnata in base al regola DMARC selezionato.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Criteri di DMARC {#dmarc-policies}

Se un messaggio e-mail non riesce a eseguire l’autenticazione di DMARC, puoi decidere quale azione verrà applicata a quel messaggio. DMARC dispone di tre opzioni di criteri:

* Monitoraggio (p=none): indica al provider di cassette postali/ISP di eseguire le operazioni normalmente eseguite sul messaggio.
* Quarantena (p=quarantena): indica al provider di cassette postali/ISP di recapitare la posta che non passa DMARC alla cartella spam o posta indesiderata del destinatario.
* Rifiuta (p = rifiuto): indica al provider di cassette postali/ISP di bloccare la posta che non passa DMARC con conseguente rimbalzo.

>[!NOTE]
>
>Scopri come impostare i criteri di DMARC con [!DNL Journey Optimizer] in [questa sezione](#set-up-dmarc).

## Aggiornamento requisiti DMARC {#dmarc-update}

Come parte delle best practice di settore, Google e Yahoo! richiedono entrambi di disporre di un **record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito si applica a partire dal **1° febbraio 2024**.

>[!CAUTION]
>
>Non rispettare questo nuovo requisito da parte di Gmail e Yahoo! dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata oppure il blocco.

Di conseguenza, Adobe Systems consiglia vivamente di intraprendere le seguenti azioni:

* Assicurati di avere il record **DMARC impostato per** tutti i sottodomini che hai già delegato **a Adobe Systems in [!DNL Journey Optimizer].** [Scopri come](#check-subdomains-for-dmarc)

* Quando **delega un nuovo sottodominio** ad Adobe, puoi **configurare DMARC** direttamente **nell&#39;interfaccia di amministrazione [!DNL Journey Optimizer]**. [Scopri come](#implement-dmarc)

## Implementare DMARC in [!DNL Journey Optimizer] {#implement-dmarc}

L&#39;interfaccia di amministrazione di [!DNL Journey Optimizer] consente di impostare il record DMARC per tutti i sottodomini che hai già delegato o che stai delegando ad Adobe. I passaggi dettagliati sono descritti di seguito.

### Controlla i tuoi sottodomini esistenti per DMARC {#check-subdomains-for-dmarc}

Per assicurarti di avere un record DMARC impostato per tutti i sottodomini che hai delegato in [!DNL Journey Optimizer], seguire la procedura seguente.

1. Accedi alle **[!UICONTROL impostazioni]** di Amministrazione **>**&#x200B;[!UICONTROL &#x200B; canali &#x200B;]&#x200B;**>** e-mail > **[!UICONTROL menu Sottodomini]**, quindi fai clic su **[!UICONTROL Configura sottodominio]**.

1. Per ogni sottodominio delegato, controllare la **[!UICONTROL colonna Record]** DMARC. Se non è stato trovato alcun record per un determinato sottodominio, viene riprodotto un avviso.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Per soddisfare i nuovi requisiti di Gmail e Yahoo! ed evitare problemi di recapito messaggi con i principali ISP, si consiglia di impostare il record DMARC per tutti i sottodomini delegati. [Ulteriori informazioni](dmarc-record-update.md)

1. Seleziona un sottodominio a cui non è associato alcun record DMARC e compila la **[!UICONTROL sezione record]** DMARC in base alle esigenze della tua organizzazione. I passaggi per popolare i campi del record DMARC sono descritti in dettaglio in [questa sezione](#implement-dmarc).

   <!--![](assets/dmarc-record-edit-full.png)-->

   >[!NOTE]
   >
   >A seconda che un record DMARC venga trovato o meno con il dominio padre, è possibile scegliere di utilizzare i valori del dominio padre o di avere Adobe Systems gestire record DMARC. [Ulteriori informazioni](#implement-dmarc)

1. Se stai modificando un sottodominio:

   * [Delega completa](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, non sono necessarie ulteriori azioni.

   * Configurato con [CNAME,](delegate-subdomain.md#cname-subdomain-delegation) è necessario copiare il record DNS per DMARC nella soluzione di hosting per generare i record DNS corrispondenti.

     ![](assets/dmarc-record-edit-cname.png)

     Assicurati che il record DNS sia stato generato nella tua soluzione di hosting del dominio e seleziona la casella &quot;Confermo...&quot;.

1. Salva le modifiche.

### Configurare DMARC per nuovi sottodomini {#set-up-dmarc}

Durante la delega di nuovi sottodomini ad Adobe in [!DNL Journey Optimizer], verrà creato un record DMARC nel DNS per il dominio. Segui i passaggi riportati di seguito per implementare DMARC.

>[!CAUTION]
>
>Per rispettare i nuovi requisiti di Gmail e Yahoo! ed evitare problemi di recapito con i principali ISP, si consiglia di impostare il record DMARC per tutti i sottodomini delegati. [Ulteriori informazioni](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Imposta un nuovo sottodominio. [Scopri come](delegate-subdomain.md)

1. Vai alla **[!UICONTROL sezione record]** DMARC.

1. Se un record DMARC è disponibile nel dominio padre associato al sottodominio, vengono visualizzate due opzioni:

   ![](assets/dmarc-record-found.png)

   * **[!UICONTROL Gestisci con Adobe]**: Adobe può gestire il record DMARC del tuo sottodominio. Segui i passaggi descritti in [questa sezione](#manage-dmarc-with-adobe).

   * **[!UICONTROL Gestisci autonomamente]**: <!--This option is selected by default.-->Questa opzione consente di gestire il record DMARC all&#39;esterno di [!DNL Journey Optimizer], utilizzando i valori del dominio padre. Questi valori vengono visualizzati nell’interfaccia, ma non è possibile modificarli.

     ![](assets/dmarc-record-found-own.png){width="80%"}

1. Se non viene trovato alcun record DMARC nel dominio padre, è disponibile solo l&#39;opzione **[!UICONTROL Gestisci con Adobe Systems]** . Segui i passaggi [riportati di seguito](#manage-dmarc-with-adobe) per configurare il record DMARC per il tuo sottodominio.

   ![](assets/dmarc-record-not-found.png){width="80%"}

### Gestisci il record DMARC con Adobe Systems {#manage-dmarc-with-adobe}

Per consentire ad Adobe di gestire il record DMARC, seleziona l&#39;opzione **[!UICONTROL Gestisci con Adobe]** e segui i passaggi indicati di seguito.

>[!NOTE]
>
>Se recuperato da [!DNL Journey Optimizer], puoi utilizzare gli stessi valori evidenziati nell&#39;interfaccia o modificarli in base alle esigenze.

![](assets/dmarc-record-with-adobe-ex.png){width="80%"}

>[!NOTE]
>
>Se non aggiungi alcun valore, verranno utilizzati i valori predefiniti precompilati.

1. Definisci l’azione che il server destinatario eseguirà se DMARC non riesce. A seconda del [criterio DMARC](#dmarc-policies) che si desidera applicare, selezionare una delle tre opzioni seguenti:

   * **[!UICONTROL Nessuno]** (valore predefinito): indica al destinatario di non eseguire azioni sui messaggi che non superano l&#39;autenticazione di DMARC, ma di inviare comunque i report e-mail al mittente.
   * **[!UICONTROL Quarantena]**: indica al server di posta elettronica ricevente di mettere in quarantena la posta elettronica che non supera l&#39;autenticazione DMARC - questo generalmente significa inserire quei messaggi nella cartella spam o posta indesiderata del destinatario.
   * **[!UICONTROL Rifiuto]**: indica al destinatario di negare completamente (rimbalzare) qualsiasi e-mail per il dominio che non riesce l&#39;autenticazione. Con questa regola abilitata, solo l&#39;email verificata come autenticata al 100% dal tuo dominio lineare avrà la possibilità di casella in entrata posizionamento.

   >[!NOTE]
   >
   >Come procedura consigliata, si consiglia di implementare lentamente i implementazione DMARC aumentando il regola DMARC da **Nessuno**, a **Quarantena**, a **Rifiuta** man mano che si acquisisce la comprensione del potenziale impatto di DMARC.

1. Facoltativamente, aggiungi uno o più indirizzi e-mail di tua scelta per indicare dove **rapporti DMARC** nelle e-mail che [non riescono a eseguire l&#39;autenticazione](#how-dmarc-works) devono essere inviati all&#39;interno della tua organizzazione. Puoi aggiungere fino a cinque indirizzi per ogni rapporto.

   >[!NOTE]
   >
   >Assicurati di avere un casella in entrata autentico (non Adobe Systems) sotto il tuo controllo dove puoi ricevere tali rapporti.

   Esistono due diversi report generati dagli ISP che i mittenti possono ricevere tramite i tag RUA/RUF nel loro regola DMARC:

   * **Rapporti** aggregati (RUA): non contengono PII (informazioni di identificazione personale) che potrebbero essere sensibili GDPR.
   * **Rapporti** sui guasti forensi (RUF): contengono indirizzi e-mail sensibili ai GDPR. Prima dell&#39;uso, controlla internamente come gestire le informazioni che devono essere conformi ai GDPR.

   >[!NOTE]
   >
   >Questi report altamente tecnici forniscono una panoramica delle e-mail che tentano di effettuare lo spoofing. È meglio digerirli attraverso un strumento di terze parti.

1. Seleziona la **percentuale applicabile** di e-mail per DMARC.

   Questa percentuale dipende dalla fiducia nell’infrastruttura e-mail e dalla tolleranza per i falsi positivi (le e-mail legittime vengono contrassegnate come fraudolente). È comune per le organizzazioni iniziare con DMARC regola impostato su **Nessuno**, aumentare gradualmente la percentuale di regola DMARC e monitorare attentamente l&#39;impatto sul recapito legittimo delle e-mail.

   >[!NOTE]
   >
   >Collabora con gli amministratori della posta elettronica e i team IT per aumentare gradualmente la percentuale man mano che acquisisci fiducia nelle tue procedure di autenticazione della posta elettronica.

   Come best practice, mirare a un elevato tasso di conformità DMARC, idealmente vicino al 100%, per massimizzare i vantaggi in termini di sicurezza riducendo al minimo il rischio di falsi positivi.

1. Seleziona un **intervallo** di reporting compreso tra 24 e 168 ore. Consente ai proprietari del dominio di ricevere aggiornamenti regolari sui risultati dell’autenticazione e-mail e di intraprendere le azioni necessarie per migliorare la sicurezza e-mail.

<!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

The default value (24 hours) is generally the email providers' expectation.

**********

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
