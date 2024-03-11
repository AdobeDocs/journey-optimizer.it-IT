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
source-git-commit: 745474d6232f01ee959db8d706110477ed0220e2
workflow-type: ht
source-wordcount: '561'
ht-degree: 100%

---

# Conformità al nuovo requisito DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Scopri di più sull’aggiornamento DMARC obbligatorio"
>abstract="Come parte dell’applicazione delle best practice del settore, Google e Yahoo richiedono entrambi di disporre di un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail, a partire dal **1 febbraio 2024**.<br>Di conseguenza, devi assicurarti di aver impostato il record DMARC per tutti i sottodomini che hai delegato ad Adobe in Journey Optimizer."

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati. Offrendo una politica chiara ai provider di posta elettronica/ISP, aiuta a evitare che malintenzionati inviino e-mail che affermano di arrivare dal tuo dominio. L’implementazione di DMARC riduce il rischio che le e-mail legittime vengano contrassegnate come spam o vengano rifiutate, inoltre migliora il recapito dei messaggi e-mail.

Come parte delle best practice di settore, Google e Yahoo! richiedono entrambi di disporre di un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito si applica a partire dal **1° febbraio 2024**.

>[!CAUTION]
>
>Non rispettare questo nuovo requisito da parte di Gmail e Yahoo! dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata oppure il blocco.

Di conseguenza, Adobe consiglia vivamente di assicurarsi di aver impostato il record DMARC per tutti i sottodomini delegati ad Adobe in [!DNL Journey Optimizer]. Segui i passaggi seguenti che si applicano al tuo caso:

* Se l’invio dei sottodomini è stato [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, esegui una delle opzioni seguenti:

   * Configura DMARC nel dominio principale dei sottodomini delegati **nella soluzione di hosting**.
oppure
   * Configura DMARC nei sottodomini delegati **nell’interfaccia utente di configurazione di[!DNL Journey Optimizer]**, senza alcun intervento aggiuntivo sulla soluzione di hosting. [Scopri come](dmarc-record.md#implement-dmarc)

* Se hai impostato i sottodomini di invio con [CNAME](delegate-subdomain.md#cname-subdomain-delegation), esegui una delle opzioni seguenti:

   * Configura DMARC nei sottodomini o nel dominio principale dei sottodomini **nella soluzione di hosting**.
oppure
   * Configura DMARC nei sottodomini delegati **nell’interfaccia utente di configurazione di[!DNL Journey Optimizer]**. [Scopri come](dmarc-record.md#implement-dmarc)

  >[!IMPORTANT]
  >
  >Tuttavia, la configurazione del CNAME richiede anche delle voci aggiuntive nella soluzione di hosting. Di conseguenza, assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l’aggiornamento descritto in [questa sezione](dmarc-record.md#implement-dmarc).

Le timeline più recenti condivise da Google e Yahoo! sono le seguenti:

* Google:

   * **Febbraio 2024**: iniziano i mancati recapiti temporanei destinati a segnalare la mancata conformità. Le e-mail continueranno a essere consegnate come di consueto dopo un breve ritardo se non sei ancora in regola con le normative. Se sei pienamente conforme, non ci saranno mancati recapiti temporanei e non ne risentirai.

   * **Aprile 2024**: inizieranno i blocchi per i mittenti che non sono conformi ai requisiti DMARC. Inizialmente verrà bloccata solo una parte dei messaggi e-mail non conformi, con la percentuale di messaggi bloccati che aumenterà nel tempo.

   * **1 giugno 2024**: qualsiasi mittente non pienamente conforme subirà un blocco.

* Yahoo! non ha fornito date esatte, ma ha affermato che “l’implementazione dell’applicazione inizierà a febbraio 2024. L’applicazione sarà introdotta gradualmente”.

>[!NOTE]
>
>In caso di domande o se hai bisogno di supporto, contatta il tuo consulente del team Deliverability di Adobe o il tuo rappresentante di Adobe.

**Link utili**

* Ulteriori informazioni su DMARC sono disponibili nella [Guida alle best practice per il recapito dei messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=it#about){target="_blank"}
* Leggi l’[annuncio di Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Leggi l’[annuncio di Yahoo](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
