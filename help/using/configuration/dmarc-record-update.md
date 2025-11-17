---
solution: Journey Optimizer
product: journey optimizer
title: Conformità al nuovo requisito DMARC
description: Scopri perché e quando impostare il record DMARC in Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, dominio, posta, dmarc, record
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '431'
ht-degree: 100%

---

# Conformità al nuovo requisito DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Ulteriori informazioni sull’aggiornamento DMARC obbligatorio"
>abstract="Come parte dell’applicazione delle best practice del settore, Google e Yahoo richiedono entrambi di disporre di un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail, a partire dal **1 febbraio 2024**.<br>Di conseguenza, devi assicurarti di aver impostato il record DMARC per tutti i sottodomini che hai delegato ad Adobe in Journey Optimizer."

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati. Offrendo una politica chiara ai provider di posta elettronica/ISP, aiuta a evitare che malintenzionati inviino e-mail che affermano di arrivare dal tuo dominio. L’implementazione di DMARC riduce il rischio che le e-mail legittime vengano contrassegnate come spam o vengano rifiutate, inoltre migliora il recapito dei messaggi e-mail.

Come parte delle best practice di settore, Google e Yahoo! richiedono entrambi di disporre di un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito si applica a partire dal **1° febbraio 2024**.

>[!CAUTION]
>
>Non rispettare questo nuovo requisito da parte di Gmail e Yahoo! dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata oppure il blocco.

Di conseguenza, Adobe consiglia vivamente di assicurarsi di aver impostato il record DMARC per tutti i sottodomini delegati ad Adobe in [!DNL Journey Optimizer]. Segui i passaggi seguenti che si applicano al tuo caso:

* Se l’invio dei sottodomini è stato [completamente delegato](delegate-subdomain.md#set-up-subdomain) ad Adobe, esegui una delle opzioni seguenti:

   * Configura DMARC nel dominio principale dei sottodomini delegati **nella soluzione di hosting**.
oppure
   * Configura DMARC nei sottodomini delegati **nell’interfaccia utente di configurazione di[!DNL Journey Optimizer]**, senza alcun intervento aggiuntivo sulla soluzione di hosting. [Scopri come](dmarc-record.md#implement-dmarc)

* Se hai impostato i sottodomini di invio con [CNAME](delegate-subdomain.md#cname-subdomain-setup), esegui una delle opzioni seguenti:

   * Configura DMARC nei sottodomini o nel dominio principale dei sottodomini **nella soluzione di hosting**.
oppure
   * Configura DMARC nei sottodomini delegati **nell’interfaccia utente di configurazione di[!DNL Journey Optimizer]**. [Scopri come](dmarc-record.md#implement-dmarc)

  Tuttavia, la configurazione del CNAME richiede anche delle voci aggiuntive nella soluzione di hosting. Di conseguenza, assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l’aggiornamento descritto in [questa sezione](dmarc-record.md#implement-dmarc).

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>In caso di domande o se hai bisogno di supporto, contatta il tuo consulente del team Deliverability di Adobe o il tuo rappresentante di Adobe.

**Link utili**

* Ulteriori informazioni su DMARC sono disponibili nella [guida alle best practice per la recapitabilità](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=it#about){target="_blank"}
* Leggi l’[annuncio di Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Leggi l’[annuncio di Yahoo!](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
