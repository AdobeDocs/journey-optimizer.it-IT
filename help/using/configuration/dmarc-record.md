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
source-git-commit: b3716265282599604de629be540ca68971daa343
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 9%

---

# Record DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Impostare il record DMARC"
>abstract="DMARC è un metodo di autenticazione delle e-mail che consente ai proprietari di dominio di proteggerlo da utilizzi non autorizzati ed evitare problemi di recapitabilità con i provider di posta elettronica.<br>Come parte dell’applicazione delle best practice del settore, Google e Yahoo richiedono entrambi di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail."

## Cos’è DMARC? {#what-is-dmarc}

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati. Offrendo una politica chiara ai provider di posta elettronica e di servizi Internet (ISP), aiuta a evitare che gli attori malintenzionati inviino e-mail che affermano di appartenere al tuo dominio. L’implementazione di DMARC riduce il rischio che le e-mail legittime vengano contrassegnate come spam o rifiutate e migliora il recapito dei messaggi e-mail.

DMARC offre anche rapporti sui messaggi che non superano l’autenticazione, oltre a un controllo sulla gestione delle e-mail che non superano la convalida DMARC. A seconda del [criterio DMARC](#dmarc-policies) implementato, queste e-mail possono essere monitorate, messe in quarantena o rifiutate. Queste funzionalità consentono di intraprendere azioni per mitigare e risolvere potenziali errori.

Per evitare problemi di recapito messaggi e ottenere il controllo della posta che non riesce l&#39;autenticazione, [!DNL Journey Optimizer] ora supporta la tecnologia DMARC direttamente nell&#39;interfaccia di amministrazione. [Ulteriori informazioni](#implement-dmarc)

### Come funziona DMARC? {#how-dmarc-works}

SPF e DKIM vengono entrambi utilizzati per associare un’e-mail a un dominio e collaborare per l’autenticazione delle e-mail. DMARC fa un ulteriore passo in avanti e aiuta a prevenire lo spoofing facendo corrispondere il dominio controllato da DKIM e SPF.

>[!NOTE]
>
>In Journey Optimizer, SPF e DKIM sono configurati per te.

Per trasmettere DMARC, un messaggio deve trasmettere SPF o DKIM:

* SPF (Sender Policy Framework) consente di verificare che il messaggio di posta elettronica provenga da una fonte autorizzata controllando l&#39;indirizzo IP del server di invio rispetto a un elenco di indirizzi IP autorizzati per il dominio.
* DKIM (DomainKeys Identified Mail) aggiunge una firma digitale ai messaggi e-mail, consentendo al destinatario di verificarne l’integrità e l’autenticità.

Se entrambi o uno di questi errori di autenticazione, DMARC avrà esito negativo e l’e-mail verrà consegnata in base ai criteri di DMARC selezionati.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Criteri di DMARC {#dmarc-policies}

Se un messaggio e-mail non riesce a eseguire l’autenticazione di DMARC, puoi decidere quale azione verrà applicata a quel messaggio. DMARC dispone di tre opzioni di criteri:

* Monitoraggio (p=none): indica al provider di cassette postali/ISP di eseguire le operazioni normalmente eseguite sul messaggio.
* Quarantena (p=quarantena): indica al provider della cassetta postale o all&#39;ISP di recapitare la posta che non passa DMARC alla cartella di posta indesiderata o indesiderata del destinatario.
* Rifiuta (p=rifiuta): indica al provider di cassette postali/ISP di bloccare la posta che non passa DMARC causando un mancato recapito.

>[!NOTE]
>
>Scopri come impostare i criteri di DMARC con [!DNL Journey Optimizer] in [questa sezione](#set-up-dmarc).

## Aggiornamento requisiti DMARC {#dmarc-update}

Come parte delle best practice di settore, Google e Yahoo! richiedono entrambi di disporre di un **record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito si applica a partire dal **1° febbraio 2024**.

>[!CAUTION]
>
>Non rispettare questo nuovo requisito da parte di Gmail e Yahoo! dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata oppure il blocco.

Di conseguenza, Adobe consiglia vivamente di effettuare le seguenti operazioni:

* Assicurati di avere **record DMARC** configurato per **tutti i sottodomini che hai già delegato** ad Adobe in [!DNL Journey Optimizer]. [Scopri come](#check-subdomains-for-dmarc)

* Quando **delega un nuovo sottodominio** ad Adobe, puoi **configurare DMARC** direttamente nell&#39;interfaccia di amministrazione [!DNL Journey Optimizer]. [Scopri come](#set-up-dmarc)

## Implementare DMARC in [!DNL Journey Optimizer] {#implement-dmarc}

L&#39;interfaccia di amministrazione di [!DNL Journey Optimizer] consente di impostare il record DMARC per tutti i sottodomini che hai già delegato o che stai delegando ad Adobe. I passaggi dettagliati sono descritti di seguito.

### Controlla i sottodomini esistenti per DMARC {#check-subdomains-for-dmarc}

Per verificare che il record DMARC sia impostato per tutti i sottodomini delegati in [!DNL Journey Optimizer], attenersi alla procedura seguente.

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**, quindi fai clic su **[!UICONTROL Configura sottodominio]**.

1. Per ogni sottodominio delegato, controlla la colonna **[!UICONTROL Record DMARC]**. Se non è stato trovato alcun record per un determinato sottodominio, viene visualizzato un avviso.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Per soddisfare i nuovi requisiti di Gmail e Yahoo! ed evitare problemi di recapito messaggi con i principali ISP, si consiglia di impostare il record DMARC per tutti i sottodomini delegati. [Ulteriori informazioni](dmarc-record-update.md)

1. Seleziona un sottodominio a cui non è associato alcun record DMARC e compila la sezione **[!UICONTROL Record DMARC]** in base alle esigenze della tua organizzazione. I passaggi per compilare i campi dei record di DMARC sono descritti in [questa sezione](#set-up-dmarc).

   <!--![](assets/dmarc-record-edit-full.png)-->

   >[!NOTE]
   >
   >A seconda che venga trovato o meno un record DMARC con il dominio principale, puoi scegliere di utilizzare i valori del dominio principale o di fare in modo che Adobe gestisca il record DMARC. [Ulteriori informazioni](#manage-dmarc-with-adobe)

1. Se stai modificando un sottodominio:

   * [Delega completa](delegate-subdomain.md#set-up-subdomain) ad Adobe, non sono necessarie ulteriori azioni.

   * Configurato con [CNAME](delegate-subdomain.md#cname-subdomain-setup), è necessario copiare il record DNS per DMARC nella soluzione di hosting per generare i record DNS corrispondenti.

     ![](assets/dmarc-record-edit-cname.png)

     Assicurati che il record DNS sia stato generato nella soluzione di hosting del tuo dominio e seleziona la casella &quot;Confermo...&quot;.

1. Salva le modifiche.

### Configurare DMARC per i nuovi sottodomini {#set-up-dmarc}

Durante la delega di nuovi sottodomini ad Adobe in [!DNL Journey Optimizer], verrà creato un record DMARC nel DNS per il dominio. Per implementare DMARC, segui i passaggi indicati di seguito.

>[!CAUTION]
>
>Per soddisfare i nuovi requisiti di Gmail e Yahoo! ed evitare problemi di recapito messaggi con i principali ISP, si consiglia di impostare il record DMARC per tutti i sottodomini delegati. [Ulteriori informazioni](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Configura un nuovo sottodominio. [Scopri come](delegate-subdomain.md)

1. Passare alla sezione **[!UICONTROL Record DMARC]**.

1. Se nel dominio principale associato al sottodominio è disponibile un record DMARC, vengono visualizzate due opzioni:

   ![](assets/dmarc-record-found.png)

   * **[!UICONTROL Gestisci con Adobe]**: Adobe può gestire il record DMARC del tuo sottodominio. Segui i passaggi descritti in [questa sezione](#manage-dmarc-with-adobe).

   * **[!UICONTROL Gestisci autonomamente]**: <!--This option is selected by default.-->Questa opzione consente di gestire il record DMARC all&#39;esterno di [!DNL Journey Optimizer], utilizzando i valori del dominio padre. Questi valori vengono visualizzati nell’interfaccia, ma non è possibile modificarli.

     ![](assets/dmarc-record-found-own.png){width="80%"}

1. Se non viene trovato alcun record DMARC nel dominio padre, è disponibile solo l&#39;opzione **[!UICONTROL Gestisci con Adobe]**. Segui i passaggi [indicati di seguito](#manage-dmarc-with-adobe) per configurare il record DMARC per il tuo sottodominio.

   ![](assets/dmarc-record-not-found.png){width="80%"}

### Gestire i record DMARC con Adobe {#manage-dmarc-with-adobe}

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
   * **[!UICONTROL Quarantena]**: indica al server e-mail ricevente di mettere in quarantena le e-mail che non riescono a eseguire l&#39;autenticazione di DMARC. Ciò in genere significa inserire tali messaggi nella cartella di posta indesiderata o indesiderata del destinatario.
   * **[!UICONTROL Rifiuta]**: indica al destinatario di negare completamente (non recapitare) qualsiasi messaggio e-mail per il dominio che non supera l&#39;autenticazione. Con questo criterio abilitato, solo i messaggi e-mail verificati come autenticati al 100% dal dominio avranno anche la possibilità di inserire messaggi nella casella in entrata.

   >[!NOTE]
   >
   >Come best practice, si consiglia di eseguire il rollout lento dell&#39;implementazione di DMARC aumentando il livello dei criteri di DMARC da **None** a **Quarantine** e a **Rifiuta** per comprendere il potenziale impatto di DMARC.

1. Facoltativamente, aggiungi uno o più indirizzi e-mail di tua scelta per indicare dove **rapporti DMARC** nelle e-mail che [non riescono a eseguire l&#39;autenticazione](#how-dmarc-works) devono essere inviati all&#39;interno della tua organizzazione. Puoi aggiungere fino a cinque indirizzi per ogni rapporto.

   >[!NOTE]
   >
   >Assicurati di avere una casella in entrata autentica (non Adobe) nel controllo in cui puoi ricevere tali rapporti.

   Esistono due diversi rapporti generati dagli ISP che i mittenti possono ricevere tramite i tag RUA/RUF nei loro criteri di DMARC:

   * **Rapporti aggregati** (RUA): non contengono dati PII (personalmente identificabili) che potrebbero essere sensibili ai requisiti RGPD.
   * **Rapporti sugli errori forensi** (RUF): contengono indirizzi e-mail sensibili ai requisiti RGPD. Prima di utilizzare, controlla internamente come gestire le informazioni che devono essere conformi ai requisiti RGPD.

   >[!NOTE]
   >
   >Questi rapporti altamente tecnici forniscono una panoramica delle e-mail che vengono tentate di spoofing. È consigliabile digerirli attraverso uno strumento di terze parti.

1. Seleziona la **percentuale applicabile** di e-mail per DMARC.

   Questa percentuale dipende dalla fiducia nell’infrastruttura e-mail e dalla tolleranza per i falsi positivi (le e-mail legittime vengono contrassegnate come fraudolente). In genere le organizzazioni iniziano con i criteri di DMARC impostati su **Nessuno**, aumentano gradualmente la percentuale di criteri di DMARC e monitorano da vicino l&#39;impatto sulla consegna di e-mail legittime.

   >[!NOTE]
   >
   >Collabora con i tuoi amministratori e-mail e il team IT per aumentare gradualmente la percentuale man mano che acquisisci fiducia nelle tue pratiche di autenticazione e-mail.

   Come best practice, cerca un elevato tasso di conformità DMARC, idealmente vicino al 100%, per massimizzare i vantaggi in termini di sicurezza e ridurre al minimo il rischio di falsi positivi.

1. Seleziona un **intervallo di reporting** compreso tra 24 e 168 ore. Consente ai proprietari del dominio di ricevere aggiornamenti regolari sui risultati dell’autenticazione e-mail e di intraprendere le azioni necessarie per migliorare la sicurezza e-mail.

### Risoluzione dei problemi {#troubleshooting}

Quando si imposta un record DMARC, alle impostazioni DNS del dominio viene aggiunto un record TXT DNS che specifica il criterio DMARC.

**Tempistica propagazione DNS**

La propagazione delle modifiche DNS su Internet richiede tempo, in genere da pochi minuti a 48 ore. Se hai appena apportato una modifica alla configurazione di DMARC e cerchi di verificare immediatamente l’aggiornamento, potrebbero verificarsi degli errori o le modifiche potrebbero non essere ancora state rilevate.

Attendere che i record DNS si propaghino per un tempo sufficiente prima di provare a verificare la configurazione di DMARC. Se riscontri ancora problemi dopo 48 ore, verifica che i record DNS siano stati aggiunti correttamente alla soluzione di hosting.

<!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

The default value (24 hours) is generally the email providers' expectation.-->

<!--

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

* DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

* It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.-->
